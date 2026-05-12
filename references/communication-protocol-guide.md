# 智能家居通信协议设计指南

> 本指南覆盖设备端→网关→云端→App 的全链路通信设计，基于物模型思想，适用于 MQTT/CoAP/HTTP 协议栈。

## 1. 物模型设计

### 1.1 物模型三层结构

```
设备(Thing)
├── 属性(Property)     — 设备状态，云端可读可写
├── 事件(Event)         — 设备主动上报，云端订阅
└── 服务(Service)       — 云端下发指令，设备执行并返回
```

### 1.2 属性定义（以智能门锁为例）

| 属性ID | 名称 | 数据类型 | 读写 | 说明 |
|--------|------|----------|------|------|
| lock_state | 上锁状态 | enum:locked/unlocked/jammed | 只读 | 设备上报，不支持云端写入 |
| battery_level | 电量百分比 | int(0-100) | 只读 | 低于20%触发告警 |
| door_state | 门磁状态 | enum:open/closed | 只读 | — |
| auto_lock_delay | 自动上锁延时 | int(5-60,秒) | 读写 | 用户可配置 |
| alarm_volume | 告警音量 | enum:low/mid/high | 读写 | — |
| firmware_version | 固件版本 | string | 只读 | 用于 OTA 判断 |

### 1.3 事件定义

| 事件ID | 名称 | 输出参数 | 触发条件 |
|--------|------|----------|----------|
| unlock | 开锁事件 | method, user_id, result, timestamp | 任意方式开锁 |
| alarm | 告警事件 | alarm_type, severity, timestamp | 撬锁/多次错误/低电量 |
| low_battery | 低电量告警 | battery_level, timestamp | 电量≤20% |
| tamper | 防拆告警 | — | 面板被拆卸 |

### 1.4 服务定义

| 服务ID | 名称 | 输入参数 | 返回参数 |
|--------|------|----------|----------|
| remote_unlock | 远程开锁 | operator_token | result, reason |
| create_temp_pwd | 生成临时密码 | valid_from, valid_to, max_uses | temp_password, pwd_id |
| delete_temp_pwd | 删除临时密码 | pwd_id | result |
| reboot | 远程重启 | — | result |
| start_ota | 触发OTA | firmware_url, md5 | result |

## 2. MQTT Topic 规范

### 2.1 Topic 命名

```
产品级:   {product_id}/{device_id}/{direction}/{category}/{msg_type}
示例:     smartlock_001/dlk_a1b2c3/up/property/report
```

| 字段 | 说明 | 示例 |
|------|------|------|
| product_id | 产品标识 | smartlock_001 |
| device_id | 设备唯一ID (MAC/DID) | dlk_a1b2c3 |
| direction | up(设备→云) / down(云→设备) | up |
| category | property / event / service / ota | property |
| msg_type | report / set / get / response | report |

### 2.2 Topic 清单

| Topic | 方向 | QoS | 说明 |
|-------|------|-----|------|
| `{pid}/{did}/up/property/report` | 设备→云 | 1 | 属性上报（定时/变化触发） |
| `{pid}/{did}/down/property/set` | 云→设备 | 1 | 属性设置 |
| `{pid}/{did}/up/property/get_response` | 设备→云 | 1 | 属性查询响应 |
| `{pid}/{did}/up/event/post` | 设备→云 | 1 | 事件上报 |
| `{pid}/{did}/down/service/invoke` | 云→设备 | 1 | 服务调用 |
| `{pid}/{did}/up/service/response` | 设备→云 | 1 | 服务调用结果 |
| `{pid}/{did}/down/ota/notify` | 云→设备 | 1 | OTA 升级通知 |
| `{pid}/{did}/up/ota/progress` | 设备→云 | 1 | OTA 进度上报 |
| `{pid}/{did}/up/ota/result` | 设备→云 | 1 | OTA 结果上报 |

### 2.3 遗嘱消息（Last Will）

```
Topic: {pid}/{did}/up/event/post
Payload: {"event_id":"offline","timestamp":1712345678}
QoS: 1
Retain: No
```

## 3. Payload 格式

### 3.1 JSON 通用信封

```json
{
  "msg_id": "uuid-v4",
  "timestamp": 1712345678,
  "data": { ... }
}
```

### 3.2 属性上报

```json
{
  "msg_id": "a1b2c3d4-e5f6",
  "timestamp": 1712345678,
  "data": {
    "lock_state": "locked",
    "battery_level": 85,
    "door_state": "closed"
  }
}
```

### 3.3 事件上报

```json
{
  "msg_id": "b2c3d4e5-f6a7",
  "timestamp": 1712345690,
  "data": {
    "event_id": "unlock",
    "params": {
      "method": "fingerprint",
      "user_id": "user_001",
      "result": "success"
    }
  }
}
```

### 3.4 服务调用（云端→设备）

```json
{
  "msg_id": "c3d4e5f6-a7b8",
  "timestamp": 1712345700,
  "data": {
    "service_id": "remote_unlock",
    "params": {
      "operator_token": "eyJhbG..."
    }
  }
}
```

### 3.5 服务响应（设备→云端）

```json
{
  "msg_id": "c3d4e5f6-a7b8",
  "timestamp": 1712345702,
  "data": {
    "service_id": "remote_unlock",
    "result": "success",
    "reason": ""
  }
}
```

## 4. 通信策略

### 4.1 心跳机制

| 参数 | 推荐值 | 说明 |
|------|--------|------|
| Keep-Alive 间隔 | 60-120s（插电）/ 300-600s（电池） | 电池设备可加抖动算法 |
| 心跳超时 | 1.5 × Keep-Alive | 超时判定离线 |
| 断线重连 | 指数退避: 1s→2s→4s→8s→...→60s max | 首次重连不加退避 |

### 4.2 数据上报策略

| 数据类型 | 上报方式 | 频率/触发条件 |
|----------|----------|---------------|
| 状态属性 | 变化即上报 | 状态变化 500ms 内 |
| 电量 | 定时上报 | 每 6 小时 / 电量下降 5% |
| 事件 | 即时上报 | 事件发生后 200ms 内 |
| 日志 | 批量上报 | 累积 50 条或每 30 分钟 |

### 4.3 离线策略

- 设备本地缓存未被 ACK 的消息，重连后补发
- 云端保留最近 24h 的离线指令，设备重连后下发
- 离线事件在云端生成 `offline` 事件通知 App
- 本地场景联动不受离线影响（网关端本地执行）

## 5. 安全设计

### 5.1 设备认证

```
首次配网:
设备 → 云端: device_id + device_secret(预烧录) → 获取 access_token
日常通信:
设备 → 云端: MQTT CONNECT(username=device_id, password=access_token)
```

### 5.2 敏感操作

| 操作 | 安全措施 |
|------|----------|
| 远程开锁 | token 签名 + 时间戳防重放 + TTL=30s |
| 固件升级 | HTTPS 下载 + MD5/SHA256 校验 + 签名验证 |
| 用户数据读写 | RBAC 鉴权 + 操作日志审计 |

### 5.3 密钥管理

- 设备密钥（device_secret）一机一密，出厂预烧录
- access_token 有效期 24h，过期自动续期
- 云端私钥存储在 HSM（硬件安全模块）

## 6. 数据格式约束

| 约束项 | 规范 |
|--------|------|
| JSON 编码 | UTF-8 |
| 时间戳 | Unix 秒级时间戳 |
| ID 格式 | UUID v4 (36 字符) 或设备 SN |
| 枚举值 | 全小写下划线: `locked`, `unlocked` |
| 空值 | 使用 JSON null，不省略字段 |
| 单条 Payload 上限 | ≤ 64KB（MQTT 默认上限 256KB，留余量） |

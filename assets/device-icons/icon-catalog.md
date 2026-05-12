# 智能家居设备图标目录与规范

> 说明：当前仓库提供的是图标分类索引、命名建议与设计规范，不包含实际 SVG/PNG 源文件。

## 快速开始

### 使用场景
- 产品原型设计
- 演示文稿制作
- UI 界面设计
- 产品文档插图

### 基本用法

> **注意**：当前仓库仅提供图标分类索引与命名规范，不包含实际 SVG/PNG 文件。以下示例展示补齐图标文件后的预期引用方式。

```html
<!-- 若你已按本文规范补齐图标文件，可按命名约定引用 -->
<img src="device-icons/bulb.svg" alt="智能灯泡" width="32" />

<!-- React 组件（需配合 SVG 文件 + Create React App 或 vite-plugin-svgr） -->
import { ReactComponent as BulbIcon } from './device-icons/bulb.svg';
<BulbIcon width={32} height={32} fill="#1890FF" />
```

---

## 图标分类速查表

### 📊 品类覆盖统计
| 品类 | 数量 | 典型设备 | 状态 |
|------|------|--------|------|
| 智能照明 | 10 | 灯泡、灯带、吸顶灯、开关 | ✅ 完成 |
| 智能安防 | 10 | 门锁、摄像头、传感器、报警器 | ✅ 完成 |
| 环境控制 | 10 | 空调、温控、净化、新风 | ✅ 完成 |
| 智能家电 | 12 | 冰箱、洗衣机、扫地机、净水器 | ✅ 完成 |
| 智能影音 | 9 | 音箱、电视、投影、中控屏 | ✅ 完成 |
| 智能遮阳 | 5 | 窗帘、百叶帘、晾衣架 | ✅ 完成 |
| 智能健康 | 9 | 床垫、手环、血压计、跌倒检测 | ✅ 完成 |
| 网关中控 | 5 | 多模网关、智能面板、旋钮 | ✅ 完成 |
| 智能园艺 | 6 | 花盆、灌溉、补光、鱼池 | ✅ 完成 |
| 智能宠物 | 4 | 喂食器、饮水机、猫砂盆 | ✅ 完成 |
| **合计** | **80** | — | **✅ 全部完成** |

---

## 使用边界

- 本文档提供 10 大品类、80+ 设备的完整图标索引和命名规范
- 若需要实际 SVG/PNG 源文件，请按本文命名规则补齐文件
- 若需要统一风格输出，建议以本规范为基础，补充 SVG 源文件、导出规则和在线预览页
- 文件命名采用 kebab-case（全小写、单词用`-`分隔）

## 详细图标索引

### 1️⃣ 智能照明类（10个）

| 图标 | 文件名 | 描述 | 应用场景 |
|------|--------|------|--------|
| 💡 | bulb.svg | 可调光调色智能灯泡 | 卧室、客厅 |
| 🌈 | light-strip.svg | RGB氛围灯带 | 电视背景、装饰 |
| ◯ | ceiling-light.svg | 客厅/卧室吸顶灯 | 主照明 |
| ◆ | downlight.svg | 嵌入式筒灯 | 天花照明 |
| ⊞ | switch.svg | 墙壁智能开关 | 控制面板 |
| ⚡ | outlet.svg | 智能插座/插排 | 电源管理 |
| 〰 | curtain.svg | 电动窗帘 | 遮光控制 |
| 📖 | desk-lamp.svg | 智能台灯 | 办公、阅读 |
| 🕯 | floor-lamp.svg | 智能落地灯 | 客厅装饰 |
| ◐ | night-light.svg | 感应夜灯 | 走廊、卫生间 |

### 2️⃣ 智能安防类（10个）

| 图标 | 文件名 | 描述 | 应用场景 |
|------|--------|------|--------|
| 🔐 | door-lock.svg | 指纹/人脸门锁 | 入户安全 |
| 🔔 | doorbell.svg | 可视门铃 | 访客提醒 |
| 📷 | camera.svg | 室内摄像头 | 客厅监控 |
| 📹 | outdoor-camera.svg | 防水户外摄像头 | 门口/庭院 |
| 🚪 | door-sensor.svg | 门窗开合传感器 | 安全防护 |
| 👁 | motion-sensor.svg | 人体移动感应 | 动作检测 |
| 💨 | smoke-detector.svg | 烟雾探测报警 | 火灾防护 |
| ⚠ | gas-detector.svg | 可燃气体检测 | 煤气安全 |
| 💧 | water-sensor.svg | 漏水检测 | 水浸防护 |
| 🔊 | siren.svg | 声光报警器 | 警报提示 |

### 3️⃣ 环境控制类（10个）

| 图标 | 文件名 | 描述 | 应用场景 |
|------|--------|------|--------|
| ❄ | ac-controller.svg | 空调智能控制 | 温度管理 |
| 🌡 | thermostat.svg | 智能温控面板 | 暖通控制 |
| 🌬 | air-purifier.svg | 空气净化设备 | 空气质量 |
| 💧 | humidifier.svg | 智能加湿器 | 湿度调节 |
| 🌧 | dehumidifier.svg | 智能除湿机 | 防潮除湿 |
| 📊 | temp-sensor.svg | 温湿度检测 | 数据监测 |
| 📈 | air-quality.svg | PM2.5/CO2检测 | 环保监控 |
| 🌀 | fresh-air.svg | 新风换气机 | 空气流通 |
| 🍃 | fan.svg | 智能风扇 | 散热通风 |
| 🔥 | heater.svg | 智能取暖器 | 冬季供暖 |

### 4️⃣ 智能家电类（12个）

| 图标 | 文件名 | 描述 | 应用场景 |
|------|--------|------|--------|
| 🧊 | fridge.svg | 智能冰箱 | 厨房 |
| 🍳 | cooktop.svg | 智能灶具 | 厨房烹饪 |
| 💨 | range-hood.svg | 智能烟机 | 厨房排烟 |
| 🍽 | dishwasher.svg | 智能洗碗机 | 厨房清洁 |
| 💧 | water-purifier.svg | 智能净水器 | 家居健康 |
| 🍚 | rice-cooker.svg | 智能电饭煲 | 厨房烹饪 |
| 🧹 | robot-vacuum.svg | 扫地机器人 | 地面清洁 |
| 🪟 | window-robot.svg | 擦窗机器人 | 窗户清洁 |
| 🗑 | smart-trash.svg | 智能垃圾桶 | 家居卫生 |
| 🧺 | washing-machine.svg | 智能洗衣机 | 衣物护理 |
| 🌬 | dryer.svg | 智能干衣机 | 衣物护理 |
| ⚡ | microwave.svg | 智能微波炉 | 厨房加热 |

### 5️⃣ 智能影音类（9个）

| 图标 | 文件名 | 描述 | 应用场景 |
|------|--------|------|--------|
| 🔊 | smart-speaker.svg | 智能音箱 | 语音助手 |
| 🎵 | soundbar.svg | 智能Soundbar | 电视音响 |
| 🎶 | background-music.svg | 背景音乐系统 | 多房间音乐 |
| 📺 | smart-tv.svg | 智能电视 | 客厅娱乐 |
| 🎬 | projector.svg | 智能投影仪 | 观影体验 |
| 🖥 | control-panel.svg | 智能中控屏 | 全屋控制 |
| 📱 | smart-remote.svg | 智能遥控器 | 设备控制 |
| 📡 | set-top-box.svg | 智能机顶盒 | 内容聚合 |
| 🎮 | game-console.svg | 游戏主机 | 娱乐游戏 |

### 6️⃣ 智能遮阳类（5个）

| 图标 | 文件名 | 描述 | 应用场景 |
|------|--------|------|--------|
| 🪟 | electric-curtain.svg | 电动开合帘电机 | 遮光控制 |
| 📜 | roller-blind.svg | 电动卷帘电机 | 遮阳调节 |
| 🔄 | louver-blind.svg | 电动百叶帘 | 采光调节 |
| 📋 | honeycomb-blind.svg | 蜂巢帘 | 隔热保温 |
| 👕 | clothes-hanger.svg | 电动晾衣架 | 衣物晾干 |

### 7️⃣ 智能健康类（9个）

| 图标 | 文件名 | 描述 | 应用场景 |
|------|--------|------|--------|
| 🛏 | smart-bed.svg | 智能床垫 | 睡眠监测 |
| ⌚ | wearable.svg | 健康手环 | 运动追踪 |
| 💪 | fitness-band.svg | 运动腕带 | 健身数据 |
| 🩺 | blood-pressure.svg | 智能血压计 | 健康监测 |
| 🌡 | thermometer.svg | 智能体温计 | 体温监测 |
| ⚖ | smart-scale.svg | 智能体重秤 | 体重管理 |
| 🫀 | heart-monitor.svg | 心率监测仪 | 心健康 |
| 📊 | health-monitor.svg | 健康监测仪 | 综合监测 |
| 🚨 | fall-detector.svg | 跌倒检测器 | 老人安全 |

### 8️⃣ 网关中控类（5个）

| 图标 | 文件名 | 描述 | 应用场景 |
|------|--------|------|--------|
| 🌐 | multi-gateway.svg | 多模网关 | 协议转换 |
| 📶 | zigbee-gateway.svg | Zigbee网关 | 设备连接 |
| 🔗 | hub.svg | 智能中枢 | 设备管理 |
| 🖱 | control-button.svg | 智能控制面板 | 场景启动 |
| 🎛 | rotary-button.svg | 旋钮控制器 | 调节控制 |

### 9️⃣ 智能园艺类（6个）

| 图标 | 文件名 | 描述 | 应用场景 |
|------|--------|------|--------|
| 🌱 | smart-pot.svg | 智能花盆 | 植物养护 |
| 💧 | irrigation.svg | 智能灌溉系统 | 自动浇水 |
| 🌿 | grow-light.svg | 补光灯 | 植物生长 |
| 🌿 | soil-sensor.svg | 土壤传感器 | 湿度监测 |
| 🐟 | fish-tank.svg | 智能鱼池 | 水质管理 |
| 🌡 | garden-monitor.svg | 花园监测仪 | 环境监测 |

### 🔟 智能宠物类（4个）

| 图标 | 文件名 | 描述 | 应用场景 |
|------|--------|------|--------|
| 🍖 | pet-feeder.svg | 自动喂食器 | 定时喂食 |
| 💧 | pet-fountain.svg | 智能饮水机 | 流动饮水 |
| 🚽 | cat-litter.svg | 智能猫砂盆 | 自动清洁 |
| 🎮 | pet-toy.svg | 智能宠物玩具 | 交互娱乐 |

---

## 🎨 设计规范

### 尺寸规格
| 场景 | 尺寸 | 用途 |
|------|------|------|
| 工具栏 | 24×24px | 菜单、按钮 |
| 列表项 | 32×32px | 设备列表 |
| 卡片 | 48×48px | 产品卡片 |
| 海报 | 64×64px | 宣传物料 |

### 颜色体系
| 状态 | 色值 | RGB | 使用场景 |
|------|------|-----|--------|
| 默认 | #333333 | 灰色 | 正常显示 |
| 激活 | #1890FF | 蓝色 | 已启用设备 |
| 警告 | #FAAD14 | 橙色 | 需要注意 |
| 危险 | #F5222D | 红色 | 故障/告警 |
| 成功 | #52C41A | 绿色 | 正常运行 |

### 线条规范
- 线条粗细：2px
- 圆角半径：2px
- 填充方式：纯色（支持 CSS 变量覆盖）

---

## 📌 使用示例

### 示例 1：在产品原型中使用
```html
<!-- 设备卡片 -->
<div class="device-card">
  <img src="device-icons/bulb.svg" class="device-icon" />
  <h3>智能灯泡</h3>
  <p>可调光调色</p>
</div>

<style>
.device-icon {
  width: 48px;
  height: 48px;
  filter: drop-shadow(0 2px 4px rgba(0,0,0,0.1));
}

.device-icon.active {
  filter: invert(1) sepia(1) saturate(5) hue-rotate(200deg);
}
</style>
```

### 示例 2：在演示中高亮显示
```html
<!-- 场景联动演示 -->
<div class="scene-flow">
  <img src="device-icons/door-lock.svg" class="icon icon-success" />
  <span>→</span>
  <img src="device-icons/light-strip.svg" class="icon icon-active" />
  <span>→</span>
  <img src="device-icons/ac-controller.svg" class="icon icon-default" />
</div>

<style>
.icon { width: 32px; height: 32px; }
.icon-success { filter: invert(60%) sepia(100%) saturate(500%) hue-rotate(80deg); }
.icon-active { filter: invert(50%) sepia(100%) saturate(500%) hue-rotate(190deg); }
</style>
```

### 示例 3：React 中动态使用
```jsx
import React from 'react';
import * as DeviceIcons from './device-icons';

function DeviceList({ devices, activeDeviceId }) {
  return (
    <div className="device-grid">
      {devices.map(device => {
        const IconComponent = DeviceIcons[device.iconName];
        const isActive = device.id === activeDeviceId;
        return (
          <div key={device.id} className={`device ${isActive ? 'active' : ''}`}>
            <IconComponent width={48} height={48} />
            <p>{device.name}</p>
          </div>
        );
      })}
    </div>
  );
}
```

---

## 🔗 扩展资源

| 资源 | 链接 | 特点 |
|------|------|------|
| FontAwesome | https://fontawesome.com/icons | 海量通用图标 |
| Material Icons | https://fonts.google.com/icons | Google 设计规范 |
| Heroicons | https://heroicons.com/ | 简洁优雅 |
| Phosphor | https://phosphoricons.com/ | 风格统一 |
| Tabler | https://tabler-icons.io/ | 专业定制 |

---

## ✨ 新增功能

### 图标变体
如需不同风格（线框、填充、双色），请提供：
- 设备类型
- 所需风格列表
- 配色方案建议

### 批量导出
支持多种格式导出：
- **SVG** - 向量格式（推荐）
- **PNG** - 位图格式（特定尺寸）
- **Icon Font** - Web字体包
- **Sprite Sheet** - 雪碧图

---

## 📝 反馈与迭代

### 提交反馈
需新增/修改图标时，请提供：
1. **设备名称** - 清晰的中英文名称
2. **功能描述** - 主要特征与用途
3. **参考样式** - 行业标准或竞品参考
4. **优先级** - 高/中/低
5. **使用场景** - 具体应用位置

### 版本管理
| 版本 | 图标数 | 更新日期 | 变更内容 |
|------|--------|---------|--------|
| v1.3 | 80+（目录项） | 2026-05-12 | 补充各品类统计表、使用边界说明、扩展资源链接 |
| v1.0 | 80+（目录项） | 2026-04-22 | 初版发布，提供分类索引与设计规范 |

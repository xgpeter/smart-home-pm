# write-prd — 智能家居 PRD 开发工作流

编排技能链，从需求发现到完整 PRD 输出。

## 触发

```
/write-prd [产品类型] [目标市场]
示例：/write-prd 智能门锁 中国中高端家用
```

## 执行流程

### Phase 1: 需求发现与验证（30-45 min）

1. **JTBD 分析** → 使用 `jtbd-and-journey-map.md`
   - 定义 3-5 个核心 Job（功能 + 情感 + 关联）
   - 识别当前竞争性替代方案
   
2. **问题验证** → 使用 `discovery-validation-guide.md`
   - 框定问题（Look Inward / Outward / Reframe）
   - 生成 3 个关键假设
   - 确定下一步验证方法

3. **用户画像** → 使用 `device-categories.md`
   - 确定目标用户画像（≥ 2 个）
   - 查阅品类选型建议

### Phase 2: 方案设计（45-60 min）

4. **功能优先级** → 使用 `prioritization-framework.md`
   - RICE 打分（如有数据）或 Kano 分类（新品类）
   - 加入硬件特有考量（认证/供应链/耦合度）
   - 输出优先级排序表

5. **场景设计** → 使用 `smart-home-scenes.md`
   - 选择适用场景（基础/季节/社交/生活）
   - 设计联动触发条件和执行动作

6. **技术选型** → 使用 `tech-stack-guide.md`
   - 通信协议选择 + 芯片选型
   - 云端架构方案

### Phase 3: 工程规格（45-60 min）

7. **硬件规格** → 使用 `hardware-spec-template.md`
   - 主控选型 + 外设选型表
   - 电源方案 + 日耗电模型
   - BOM 成本框架

8. **通信协议** → 使用 `communication-protocol-guide.md`
   - 物模型定义（属性/事件/服务）
   - MQTT Topic + Payload 设计

9. **固件架构** → 使用 `firmware-architecture-template.md`
   - Flash 分区 + 任务划分
   - 状态机设计 + 低功耗策略
   - OTA 方案

### Phase 4: PRD 输出（30-45 min）

10. **撰写 PRD** → 使用 `prd-template.md` + 参考 `smart-door-lock-prd.md`
    - 按 16 章模板结构填写
    - 风险与依赖（使用 `certification-guide.md` 确认认证要求）
    - 测试策略
    - 版本规划与里程碑

11. **竞品与厂商** → 使用 `vendor-directory.md`
    - 竞品对标表
    - 供应商/芯片厂商确认

### Phase 5: 评审（15 min）

12. **健康度检查** → 使用 `product-checklist.md`
    - PRD 完成度自检
    - 技术方案评审
    - 上线核对清单

## 依赖的技能

| 阶段 | 使用的参考文档 |
|------|--------------|
| 需求发现 | jtbd-and-journey-map, discovery-validation-guide, device-categories |
| 方案设计 | prioritization-framework, smart-home-scenes, tech-stack-guide |
| 工程规格 | hardware-spec-template, communication-protocol-guide, firmware-architecture-template |
| PRD 输出 | prd-template, smart-door-lock-prd, certification-guide, vendor-directory |
| 评审 | product-checklist |

## 预计总时间

完整流程（含工程规格）：**2.5-3.5 小时**

不含工程规格（仅产品定义层）：**1.5-2 小时**

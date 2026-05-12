---
name: smart-home-pm
description: 智能家居产品经理全链路技能：需求发现→功能规划→技术方案→PRD 输出→研发支持。覆盖 30 个场景、50+ 芯片选型、178 个厂商、40+ 中国国标。
version: 1.3.0
author: xgpeter
tags:
  - smart-home
  - product-management
  - IoT
  - hardware
  - prd
---

# 智能家居产品经理

## 任务目标
- 本 Skill 用于：智能家居领域的产品规划与需求分析
- 能力：
  - 智能设备功能定义与场景设计
  - 用户需求分析与用户画像构建
  - 产品需求文档（PRD）撰写
  - 技术方案可行性评估
  - 竞品分析与差异化定位
  - 版本规划、风险识别与指标定义
- **触发条件**：
  - ✅ 触发场景：智能家居产品规划、功能设计、PRD撰写、技术方案评估、场景设计
  - ❌ 非触发场景：通用IoT咨询、行业趋势分析、成本测算、销售策略制定

## 前置准备
- 无额外依赖
- 无需系统命令
- 所有参考资源已内置于项目中
- 对厂商、芯片、平台、认证要求等时效信息，应提醒用户在立项前复核

## 操作步骤

### 1. 需求收集与分析
- 明确产品类型（智能照明、安防监控、环境控制、家电互联等）
- 识别目标用户群体和使用场景
- 收集功能需求清单
- 分析竞品现状与市场机会

### 2. 产品功能规划
- 定义核心功能与增值功能
- 设计用户交互流程
- 规划设备联动场景
- 制定功能优先级（MoSCoW 法则）
- 明确范围边界、非目标与版本拆分

### 3. 技术方案设计
- 评估通信协议（WiFi/Zigbee/Z-Wave/蓝牙）
- 确定云端架构与数据存储方案
- 规划 App 端功能模块
- 评估安全性与隐私保护方案

### 4. 文档输出
- 生成产品需求文档（PRD）
- 输出用户故事与用例
- 绘制功能架构图
- 编写技术规格说明书
- 补充风险、依赖、里程碑和指标方案

## 资源索引

### 参考文档
- **[references/prd-template.md](references/prd-template.md)** — PRD 写作指南
  - 内容：标准模板结构、用户故事格式、验收标准
  - 推荐场景：撰写产品需求文档、输出用户故事
  - 参考例：[smart-door-lock-prd.md](smart-door-lock-prd.md)

- **[references/smart-home-scenes.md](references/smart-home-scenes.md)** — 场景设计参考
  - 内容：16+ 场景模式、触发条件、执行动作
  - 推荐场景：规划设备联动、设计交互流程
  - 覆盖：30个场景（照明18/安防4/环境4/节能2/特殊2），多阶段延时联动

- **[references/tech-stack-guide.md](references/tech-stack-guide.md)** — 技术选型指南
  - 内容：通信协议对比、24+ 芯片选型表、云端架构
  - 推荐场景：技术方案设计、芯片选型决策
  - 覆盖：WiFi/Zigbee/Z-Wave/蓝牙/Thread/Matter/BLE Mesh 协议，50+款芯片（国产超30款）

- **[references/device-categories.md](references/device-categories.md)** — 设备品类大全
  - 内容：10 大品类、60+ 设备、选型建议
  - 推荐场景：产品规划、品类分析、竞品对标

- **[references/vendor-directory.md](references/vendor-directory.md)** — 厂商名录
  - 内容：90+ 厂商、20+ 芯片模组、平台生态
  - 推荐场景：竞品分析、工业设计、生态调研

- **[references/certification-guide.md](references/certification-guide.md)** — 产品认证指南
  - 内容：中国/国际/行业联盟认证体系、流程建议
  - 推荐场景：上市准备、认证规划、合规评估

- **[references/product-checklist.md](references/product-checklist.md)** — 产品健康度检查清单
  - 内容：PRD 自检、技术方案评审、上线核对、迭代复盘
  - 推荐场景：项目评审、上线把关、文档质量检查

- **[references/hardware-spec-template.md](references/hardware-spec-template.md)** — 硬件需求规格模板
  - 内容：主控选型、外设选型、电源方案、射频设计、BOM 框架
  - 推荐场景：硬件工程规格输出、嵌入式开发输入

- **[references/communication-protocol-guide.md](references/communication-protocol-guide.md)** — 通信协议设计指南
  - 内容：物模型设计、MQTT Topic 规范、Payload 格式、安全设计
  - 推荐场景：云-端通信方案设计、API 文档编写

- **[references/firmware-architecture-template.md](references/firmware-architecture-template.md)** — 固件架构模板
  - 内容：RTOS 选型、任务划分、状态机、低功耗、OTA、产测
  - 推荐场景：固件架构设计、嵌入式开发评审

- **[references/discovery-validation-guide.md](references/discovery-validation-guide.md)** — 产品发现与验证指南
  - 内容：问题框定、假设生成、Mom Test 访谈、PoL 原型验证、综合决策
  - 推荐场景：新产品立项、需求验证、降低硬件开模风险

- **[references/prioritization-framework.md](references/prioritization-framework.md)** — 优先级决策框架
  - 内容：RICE/Kano/MoSCoW 框架、硬件特有考量、决策记录
  - 推荐场景：版本规划、需求评审、资源分配

- **[references/jtbd-and-journey-map.md](references/jtbd-and-journey-map.md)** — JTBD 与用户旅程地图
  - 内容：JTBD 三层结构、用户旅程触点分析、关键时刻识别
  - 推荐场景：需求分析、定义 MVP、跨团队对齐用户认知

### 工作流命令
- **[commands/write-prd.md](commands/write-prd.md)** — PRD 开发工作流（发现→方案→工程→输出→评审）
- **[commands/discover.md](commands/discover.md)** — 产品发现与验证工作流（问题→假设→验证→决策）
- **[commands/README.md](commands/README.md)** — 命令使用说明

### 静态资源
- **[assets/device-icons/](assets/device-icons/)**
  - 内容：智能家居设备图标目录与设计规范，涵盖10大品类、60+设备类型
  - 使用方式：当需要制作产品原型或演示材料时，优先使用其命名规则、分类方式和视觉规范
  - 参考目录：[assets/device-icons/icon-catalog.md](assets/device-icons/icon-catalog.md)

## 最佳实践

### ✅ 推荐做法
- 先做产品发现验证（`discover` 命令），再做 PRD 撰写（`write-prd` 命令）
- 用 JTBD 思维理解用户需求，而非功能列表思维
- 在 PRD 中标注每个需求的信心等级和验证方法
- 基于 prd-template.md 的结构撰写 PRD
- 利用 device-categories.md 的 60+ 设备作为产品选型参考
- 应用 smart-home-scenes.md 的场景模式设计功能联动
- 参考 smart-door-lock-prd.md 的格式和内容深度
- 对存在时效性的事实显式标注”待核实项”与核实日期

### ❌ 需避免
- 不要跳过用户验证直接进入硬件开发（开模成本不可逆）
- 不要在 PRD 中写实现方案（把架构决策留给工程师）
- 不要凭空构造技术方案，应参考 tech-stack-guide.md
- 不要虚构厂商或产品，应核对 vendor-directory.md
- 不要创建不在品类大全中的设备品类
- 避免输出不符合行业规范的 PRD 格式
- 不要把目录型资源表述成仓库内已有的可执行/可导入资产

### 🔧 错误处理
- **用户需求不清晰**：引导用户使用"需求分析"框架（第1步）
- **技术方案有多个选项**：提供对比表并标注各方案的权衡点
- **参考文档相互矛盾**：说明场景差异，给出条件判断建议
- **不在支持范围**：明确说明限制，提供替代方案或建议转系统管理员

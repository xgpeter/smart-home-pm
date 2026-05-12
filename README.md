# 智能家居产品经理技能

## 简介

本技能为智能家居领域的产品经理提供专业的需求分析、功能规划、技术方案设计和产品文档输出能力。涵盖智能照明、安防监控、环境控制、智能家电等全品类设备，支持从需求收集到PRD输出的完整产品工作流程。

## 核心能力

- **需求分析**：用户需求挖掘、场景分析、竞品调研
- **功能规划**：设备功能定义、场景设计、优先级排序
- **技术方案**：通信协议选型、芯片选型、云端架构设计
- **文档输出**：PRD撰写、用户故事、技术规格说明书

## 文件结构

```
smart-home-pm/
├── SKILL.md                      # 技能主文档（入口）
├── README.md                     # 本文件
├── CLAUDE.md                     # AI 助手指南
├── smart-door-lock-prd.md        # PRD 完整示范（智能门锁，16章工程级）
├── commands/                     # 工作流命令
│   ├── README.md                 # 命令使用说明
│   ├── write-prd.md              # PRD 开发工作流（发现→方案→工程→评审）
│   └── discover.md               # 产品发现与验证工作流
├── assets/                       # 静态资源
│   └── device-icons/             # 设备图标目录与规范
│       └── icon-catalog.md       # 图标命名、分类与设计规范
└── references/                   # 参考文档
    ├── prd-template.md           # PRD文档模板规范（16章，含引导问题）
    ├── smart-home-scenes.md      # 智能家居场景模式参考
    ├── tech-stack-guide.md       # 技术栈选型指南（含Matter协议）
    ├── device-categories.md      # 智能家居设备品类大全
    ├── vendor-directory.md       # 智能家居厂商名录（178品牌）
    ├── certification-guide.md    # 产品认证指南（40+标准）
    ├── product-checklist.md      # 产品健康度检查清单
    ├── hardware-spec-template.md # 硬件需求规格模板
    ├── communication-protocol-guide.md  # 通信协议设计指南
    ├── firmware-architecture-template.md # 固件架构模板
    ├── discovery-validation-guide.md  # 产品发现与验证指南（NEW）
    ├── prioritization-framework.md    # 优先级决策框架（NEW）
    └── jtbd-and-journey-map.md        # JTBD与用户旅程地图（NEW）
```

## 参考文档说明

| 文档 | 内容 | 使用场景 |
|------|------|----------|
| prd-template.md | PRD标准模板、用户故事格式、验收标准 | 撰写产品需求文档 |
| smart-home-scenes.md | 30个场景（照明18/安防4/环境4/节能2/特殊2），多阶段延时联动 | 设计设备联动场景 |
| tech-stack-guide.md | WiFi/Zigbee/蓝牙/Thread/Matter协议对比，芯片选型表 | 技术方案设计 |
| device-categories.md | 10大品类、60+设备类型、选型建议 | 产品规划与品类分析 |
| vendor-directory.md | 国际品牌、中国品牌、芯片模组、平台生态 | 竞品分析、供应链调研 |
| certification-guide.md | 中国/国际/行业联盟认证，流程与踩坑提醒 | 上市准备、合规评估 |
| product-checklist.md | PRD自检、技术评审、上线核对、迭代复盘 | 项目评审、质量把关 |
| hardware-spec-template.md | 主控选型、外设选型、电源方案、射频设计、BOM框架 | 硬件工程规格输出 |
| communication-protocol-guide.md | 物模型、MQTT Topic、Payload格式、安全设计 | 云-端通信方案设计 |
| firmware-architecture-template.md | RTOS选型、任务划分、状态机、低功耗、OTA | 固件架构与嵌入式评审 |
| discovery-validation-guide.md | 问题框定、假设生成、Mom Test访谈、PoL验证 | 新产品立项、需求验证 |
| prioritization-framework.md | RICE/Kano/MoSCoW框架、硬件特有优先级 | 版本规划、需求评审 |
| jtbd-and-journey-map.md | JTBD三层结构、用户旅程触点、关键时刻 | 需求分析、MVP定义 |
| icon-catalog.md | 图标分类索引、命名建议、设计规范 | 产品原型规划、演示材料准备 |

## 使用方式

当用户提出以下需求时，本技能将被触发：

- 智能家居产品规划
- IoT产品需求分析
- 智能设备功能设计
- PRD文档撰写
- 技术方案评估
- 竞品分析

## 当前范围与限制

- 当前仓库以知识与模板为主，不包含可直接导入项目的 SVG/PNG 图标源文件
- 厂商、平台、芯片与协议信息具有时效性，正式立项前应二次核实
- 项目当前未内置自动化校验脚本，贡献前请手动检查格式、链接和事实准确性

## 工作流程

1. **需求收集**：明确产品类型、目标用户、核心场景
2. **资料参考**：读取相关参考文档获取规范和信息
3. **方案设计**：功能规划、场景设计、技术选型
4. **文档输出**：生成PRD、用户故事、技术规格

---

## 🚀 快速查询表

| 任务 | 推荐顺序 | 优先级 | 时间 |
|------|---------|--------|------|
| **新员工入门** | README.md → SKILL.md → [device-categories.md](references/device-categories.md) | ⭐⭐⭐ | 30分钟 |
| **撰写PRD** | [prd-template.md](references/prd-template.md) → [smart-door-lock-prd.md](smart-door-lock-prd.md) | ⭐⭐⭐⭐ | 20分钟 |
| **产品规划** | [device-categories.md](references/device-categories.md) → [vendor-directory.md](references/vendor-directory.md) | ⭐⭐⭐ | 40分钟 |
| **功能设计** | [smart-home-scenes.md](references/smart-home-scenes.md) + [device-categories.md](references/device-categories.md) | ⭐⭐⭐⭐ | 45分钟 |
| **技术方案** | [tech-stack-guide.md](references/tech-stack-guide.md) → [hardware-spec-template.md](references/hardware-spec-template.md) | ⭐⭐⭐⭐⭐ | 60分钟 |
| **硬件规格** | [hardware-spec-template.md](references/hardware-spec-template.md) → [tech-stack-guide.md](references/tech-stack-guide.md) | ⭐⭐⭐⭐⭐ | 45分钟 |
| **协议设计** | [communication-protocol-guide.md](references/communication-protocol-guide.md) → [tech-stack-guide.md](references/tech-stack-guide.md) | ⭐⭐⭐⭐ | 40分钟 |
| **固件架构** | [firmware-architecture-template.md](references/firmware-architecture-template.md) → [hardware-spec-template.md](references/hardware-spec-template.md) | ⭐⭐⭐⭐ | 40分钟 |
| **竞品分析** | [vendor-directory.md](references/vendor-directory.md) + [smart-door-lock-prd.md](smart-door-lock-prd.md) | ⭐⭐⭐ | 50分钟 |
| **产品发现** | [discovery-validation-guide.md](references/discovery-validation-guide.md) → [jtbd-and-journey-map.md](references/jtbd-and-journey-map.md) | ⭐⭐⭐⭐⭐ | 45分钟 |
| **优先级决策** | [prioritization-framework.md](references/prioritization-framework.md) → [prd-template.md](references/prd-template.md) | ⭐⭐⭐⭐ | 30分钟 |
| **认证合规** | [certification-guide.md](references/certification-guide.md) → [tech-stack-guide.md](references/tech-stack-guide.md) | ⭐⭐⭐⭐ | 30分钟 |
| **项目评审** | [product-checklist.md](references/product-checklist.md) + [prd-template.md](references/prd-template.md) | ⭐⭐⭐ | 15分钟 |
| **原型/演示** | [icon-catalog.md](assets/device-icons/icon-catalog.md) | ⭐⭐ | 20分钟 |

---

## 技能亮点

### 场景设计丰富

- 30个场景全覆盖（照明18/安防4/环境4/节能2/特殊2）
- 多阶段延时执行（立即→短延时→中延时→长延时）
- 传感器+时间组合触发（AND/OR条件）
- 完整的灯光参数表（19种场景）和调光调色规范

### 技术选型全面

- 6种通信协议对比（WiFi/Zigbee/Z-Wave/蓝牙/Thread/Matter）
- 50+款芯片选型表（覆盖主流厂商，国产芯片超 30 款）
- 3种云端架构方案
- 安全设计要点和选型决策树

### 研发工程支持（v1.2 新增）

- 硬件需求规格模板（主控选型/外设选型/电源方案/射频设计/BOM框架）
- 通信协议设计指南（物模型/MQTT Topic/Payload格式/安全设计）
- 固件架构模板（RTOS选型/任务划分/状态机/低功耗策略/OTA升级/产测方案）

### 厂商资源完整

- 50+国际品牌（美/欧/日韩）
- 90+中国品牌（互联网/家电/安防/照明/清洁/影音）
- 30+芯片模组厂商（国产占 70%）
- 20+平台与生态

### 图标资源实用

- 覆盖10大品类的图标分类索引
- 提供命名建议与设计规范（尺寸、颜色）
- 给出原型/演示场景的接入示例
- 附带在线扩展资源推荐

## 依赖

无外部依赖

## 常见问题

### Q: 如何快速了解智能家居产品体系？

按以下顺序阅读：
1. 本文档（README.md）- 了解项目概况
2. [device-categories.md](references/device-categories.md) - 学习设备分类体系（10大品类、60+设备）
3. [smart-home-scenes.md](references/smart-home-scenes.md) - 理解场景设计思路（16+场景模式）

### Q: 需要撰写PRD文档，从哪里开始？


1. 先读 [prd-template.md](references/prd-template.md) - 了解PRD标准结构
2. 参考 [smart-door-lock-prd.md](smart-door-lock-prd.md) - 学习完整的PRD示范
3. 基于模板撰写，使用 [device-categories.md](references/device-categories.md) 的设备信息进行产品定义

### Q: 需要进行技术方案设计，选型困境大？

1. 按产品电源情况判断：
   - **有电源设备**（如摄像头、音箱）→ 选 WiFi 或 LTE
   - **电池设备**（如传感器、门锁）→ 选 Zigbee 或 BLE
2. 参考 [tech-stack-guide.md](references/tech-stack-guide.md)  查看协议对比和24+芯片选型方案
3. 使用 [vendor-directory.md](references/vendor-directory.md) 确认芯片供应可用性

### Q: 竞品有哪些，怎么进行对标？

1. 查阅 [vendor-directory.md](references/vendor-directory.md) - 了解90+厂商的产品线
2. 分析竞品的主要功能、通信方式、生态集成
3. 参考 [smart-door-lock-prd.md](smart-door-lock-prd.md) 的第9章（竞品分析示范）

### Q: 如何为产品规划场景联动？

1. 打开 [smart-home-scenes.md](references/smart-home-scenes.md)
2. 根据产品类型选择相关场景（基础/季节/社交/生活）
3. 调整参数（灯光色温、设备状态、联动条件）以适配你的产品

### Q: 设计原型或演示素材时需要图标？

1. 查看 [assets/device-icons/](assets/device-icons/) 目录
2. 参考 [icon-catalog.md](assets/device-icons/icon-catalog.md) 的详细索引与命名规范
3. 按尺寸（24px/32px/48px/64px）和颜色规范自行制作或选用图标资源

## 更新日志

### v1.0

- 初始版本，包含PRD模板、场景参考、技术指南
- 补充设备品类大全（10大品类、60+设备）
- 补充厂商名录（90+品牌、20+芯片厂商）
- 完善智能照明场景（季节/社交/生活场景）
- 增加通信协议芯片选型（24款芯片）
- 增加设备图标库（80+图标）

### v1.1 (当前)

- 优化文档结构和导航体验
- 添加快速查询表
- 补充常见问题解答
- 改进图标库说明

## 贡献

本技能持续迭代优化，欢迎反馈建议。

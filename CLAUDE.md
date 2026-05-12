# CLAUDE.md - 智能家居产品经理技能

## 项目概述
这是一个 Claude Code Skill 项目，为智能家居领域的产品经理提供需求分析、功能规划、技术方案设计和 PRD 文档输出能力。

## 技术栈
- 纯 Markdown + YAML frontmatter，无运行时依赖
- Claude Code Skill 规范（SKILL.md 为入口）
- Node.js >= 14（仅 package.json 声明，无实际运行代码）

## 文件结构
```
smart-home-pm/
├── SKILL.md                        # 技能定义（触发条件、操作步骤、最佳实践）
├── README.md                       # 使用说明、快速查询表、FAQ
├── CLAUDE.md                       # 本文件 - AI 助手指南
├── package.json                    # 技能元信息（名称、版本、关键词）
├── CHANGELOG.md                    # 变更记录
├── LICENSE                         # MIT
├── smart-door-lock-prd.md          # PRD 完整示例（16章工程级）
├── commands/                       # 工作流命令
│   ├── README.md                   # 命令说明
│   ├── write-prd.md                # PRD 开发工作流
│   └── discover.md                 # 产品发现与验证工作流
├── assets/device-icons/
│   └── icon-catalog.md             # 设备图标分类索引与设计规范
└── references/
    ├── prd-template.md             # PRD 模板（16章+引导问题）
    ├── smart-home-scenes.md        # 16+ 场景模式
    ├── tech-stack-guide.md         # 协议对比 + Matter + 芯片选型
    ├── device-categories.md        # 10 大品类、60+ 设备
    ├── vendor-directory.md         # 178 厂商名录
    ├── certification-guide.md      # 产品认证指南（40+标准）
    ├── product-checklist.md        # 产品健康度检查清单
    ├── hardware-spec-template.md   # 硬件需求规格模板
    ├── communication-protocol-guide.md  # 通信协议设计指南
    ├── firmware-architecture-template.md # 固件架构模板
    ├── discovery-validation-guide.md  # 产品发现与验证指南
    ├── prioritization-framework.md    # 优先级决策框架
    └── jtbd-and-journey-map.md        # JTBD 与用户旅程地图
```

## 编码规范
- 所有新增文档使用中文撰写，Markdown 格式
- YAML frontmatter 用于技能定义文件的元信息
- 参考文档结构遵循 `prd-template.md` 的章节编号体系
- 设备品类命名遵循 `device-categories.md` 中的分类标准
- 厂商/芯片/协议信息必须从 reference 文档中引用，不得凭空构造

## 核心约束
- 这是一个知识与模板仓库，不包含可执行代码或图标源文件
- 厂商、芯片、协议信息具有时效性，输出时应标注"建议复核"
- 不要在品类大全之外虚构新的设备品类
- PRD 输出必须遵循 `prd-template.md` 的结构

## 常用操作
- **撰写 PRD**：先读 `references/prd-template.md`，参考 `smart-door-lock-prd.md` 示例
- **场景设计**：查 `references/smart-home-scenes.md`（16+ 场景覆盖基础/季节/社交/生活）
- **技术选型**：查 `references/tech-stack-guide.md`（协议对比 + Matter + 芯片选型表）
- **竞品分析**：查 `references/vendor-directory.md`（90+ 品牌）
- **设备规划**：查 `references/device-categories.md`（10 品类、60+ 设备）
- **认证合规**：查 `references/certification-guide.md`（CCC/FCC/CE/Matter 认证）
- **项目评审**：查 `references/product-checklist.md`（PRD/技术/上线/迭代核对）
- **硬件规格**：查 `references/hardware-spec-template.md`（主控/外设/电源/射频/BOM）
- **协议设计**：查 `references/communication-protocol-guide.md`（物模型/MQTT/Payload/安全）
- **固件架构**：查 `references/firmware-architecture-template.md`（RTOS/任务/状态机/低功耗/OTA）
- **产品发现**：查 `references/discovery-validation-guide.md`（问题框定/假设/验证/决策）
- **优先级决策**：查 `references/prioritization-framework.md`（RICE/Kano/MoSCoW）
- **JTBD/旅程**：查 `references/jtbd-and-journey-map.md`（JTBD/用户旅程/关键时刻）
- **工作流命令**：`/write-prd` 完整PRD流程, `/discover` 产品发现流程

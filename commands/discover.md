# discover — 智能家居产品发现与验证工作流

在投入工程资源前，系统性地验证产品假设。

## 触发

```
/discover [产品方向] [核心假设]
示例：/discover 带屏幕的智能音箱 "用户需要音箱上有屏幕来展示歌词和天气"
```

## 执行流程

### Phase 1: 问题框定（20-30 min）

1. **框定问题** → 使用 `discovery-validation-guide.md` Step 1
   - Look Inward: 团队能用现有技术栈做吗？
   - Look Outward: 用户当前怎么解决？竞品做得如何？
   - Reframe: 如果问题更小/更大/不存在呢？

2. **JTBD 分析** → 使用 `jtbd-and-journey-map.md`
   - 定义核心 Job（功能 + 情感 + 关联）
   - 识别竞争性替代方案

### Phase 2: 假设生成与验证设计（20-30 min）

3. **生成关键假设** → 使用 `discovery-validation-guide.md` Step 2
   - 问题假设 × 1
   - 方案假设 × 1
   - 价值假设 × 1

4. **选择验证方法** → 使用 `discovery-validation-guide.md` Step 3
   - 问题假设 → 用户访谈（Mom Test 原则）
   - 方案假设 → 纸面原型 / 竞品拆解
   - 价值假设 → 众筹 / 预售 / 烟雾测试

### Phase 3: 执行验证（根据方法，1-10 天）

5. **用户访谈** → 使用 `discovery-validation-guide.md` Step 4
   - 设计访谈提纲（不要问假设性问题）
   - 执行 10-15 次访谈
   - 记录格式：用户信息 + 痛点确认 + 意外发现 + 原话引用

6. **原型/竞品验证** → 使用 `discovery-validation-guide.md`
   - PoL 5 种原型选择（Feasibility/Task-Focused/Narrative/Synthetic/Vibe-Coded）
   - 制定成功标准

### Phase 4: 综合与决策（20-30 min）

7. **综合发现** → 使用 `discovery-validation-guide.md` Step 5
   - 验证结果矩阵（高/低影响 × 强/弱证据）
   - 明确：推进 / 转弯 / 放弃

8. **输出发现报告**
   - 核心发现（3-5 条）
   - 用户原话引用（5-10 条）
   - 修改后的假设
   - 下一步建议

## 依赖的技能

| 阶段 | 使用的参考文档 |
|------|--------------|
| 问题框定 | discovery-validation-guide, jtbd-and-journey-map |
| 假设生成 | discovery-validation-guide |
| 执行验证 | discovery-validation-guide, device-categories |
| 综合决策 | prioritization-framework |

## 预计总时间

- 轻量版（问题框定 + 假设生成 + 决策）：**1-1.5 小时**
- 完整版（含用户访谈执行）：**2-5 天**（取决于访谈量）

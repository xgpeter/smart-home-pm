# 贡献指南

感谢你对 smart-home-pm 的关注！

## 设计理念

本项目遵循三个原则：

1. **先教后做** — 每个文档不仅要告诉 PM 该怎么做，还要解释为什么。不能只给模板，要给出决策依据。
2. **行业知识可复核** — 厂商、芯片、协议、标准都具有时效性。贡献时应标注信息来源或数据时间点。
3. **工程师可读** — 产品文档的输出标准是：研发团队在 PM 不在场时也能做出正确的产品决策。

## 如何贡献

### 报告问题

前往 [Issues](https://github.com/xgpeter/smart-home-pm/issues) 页面，使用以下标签：

- `bug` — 事实错误、数据过时、链接失效
- `enhancement` — 功能建议、新增内容提案
- `question` — 疑问或讨论

### 贡献内容

1. Fork 本仓库
2. 创建功能分支：`git checkout -b feature/your-feature`
3. 提交更改：`git commit -m "feat: 添加 xxx"`
4. 推送分支：`git push origin feature/your-feature`
5. 创建 Pull Request

### 提交信息规范

使用约定式提交：

```
feat: 新增智能摄像头 PRD 示例
fix: 修正 ESP32-C6 BLE 版本号
docs: 更新 Matter 1.3 认证流程
refactor: 重构灯光参数表格式
```

### 内容质量要求

- 厂商、芯片、标准信息必须可追溯（标注来源或版本日期）
- 新增厂商/设备/芯片需要同时更新相关索引文档
- PRD 示例必须遵循 `prd-template.md` 的 16 章结构
- 中文撰写，技术术语保留英文对照

### 审核标准

PR 审核将检查：
- [ ] 事实准确性（可交叉验证）
- [ ] 模板一致性（遵循现有结构）
- [ ] 交叉引用完整性（相关文档同步更新）
- [ ] 时效性标注（含时间敏感信息时）

## 本地开发

本项目是纯 Markdown 文档项目，无运行时依赖。使用任意 Markdown 编辑器即可。

推荐使用 VS Code + markdownlint 插件进行格式检查。

## 行为准则

参见 [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)

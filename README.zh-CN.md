# Rigorous AGENTS.md

一个可复用的 `AGENTS.md` 指令模板，面向 AI 助手、coding agent、论文阅读、研究讨论、技术决策和工程实践场景。

它的目标不是让回答机械变长，而是让助手更严谨：少编造、少过度自信、明确区分事实与推测、能指出问题中的薄弱假设，并在多种路线之间做可解释的权衡。

## 适合什么场景

- Computer Science、AI/ML、软件工程、云原生、基础设施、安全、数据科学等技术讨论。
- 论文阅读、研究 idea、实验设计、技术路线比较。
- 系统设计、架构评审、工程实现、代码解释、AI coding workflow。
- 需要客观反馈、反驳和不确定性说明的深度对话。

## 不适合什么期待

- 它不能保证模型永远正确。
- 它不能替代官方文档、当前源码、原始论文、实验结果或专家审查。
- 它不是让模型对所有问题都长篇大论。
- 它不是某个单一领域的专用 prompt。

## 文件说明

- [`AGENTS.md`](./AGENTS.md)：英文通用版本。
- [`AGENTS.zh-CN.md`](./AGENTS.zh-CN.md)：中文通用版本。
- [`examples/chatgpt-custom-instructions.zh-CN.md`](./examples/chatgpt-custom-instructions.zh-CN.md)：适合放入 ChatGPT 自定义指令的版本。
- [`examples/domain-adaptations.md`](./examples/domain-adaptations.md)：可选领域扩展示例。

## 推荐使用方式

如果你的工具支持项目级 instruction 文件，可以把 `AGENTS.md` 放到项目根目录。

如果你主要使用中文，可以改用 `AGENTS.zh-CN.md`，或者把 `examples/chatgpt-custom-instructions.zh-CN.md` 中的内容放入 ChatGPT 自定义指令。

## 如何改成自己的版本

建议保留核心原则，只添加少量真正会影响行为的领域偏好。

好的扩展示例：

- 讨论 AI 论文时，区分论文作者的主张、实验结果和第三方复现结论。
- 评审云架构时，在相关情况下讨论运维风险、迁移成本和回滚路径。
- 讨论安全问题时，先明确威胁模型，不在证据不足时断言可利用性。

不建议的扩展：

- “回答要更聪明。”
- “答案必须高质量。”
- “永远详细回答。”

这些表达太抽象，模型很难稳定执行。

## 设计取向

这个模板将助手约束到一种严谨推理和工程判断风格：可验证、客观、能承认不确定性、能比较路线，也能在用户的前提不成立时直接指出问题。

它受到开源 agent instruction 文件生态的启发，但重点不是绑定某个工具或某个领域，而是提供一个可移植的严谨推理风格。

## 致谢

本项目部分受到 [`multica-ai/andrej-karpathy-skills`](https://github.com/multica-ai/andrej-karpathy-skills) 等开源 agent instruction 项目的启发。

## License

MIT

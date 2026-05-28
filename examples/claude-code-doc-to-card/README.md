# Example: Claude Code Doc To Card

这个 example 展示如何使用 `doc-to-card`：当用户提供 Claude Code 文档摘录或教程笔记时，把它转成面向中文 AI 工具学习者的卡片内容。

本 example 不假设当前 Claude Code 产品细节。运行时只使用用户提供的来源文本，或经过验证的官方文档。

## 用户请求 / User Request

```text
Use the doc-to-card skill to turn this Claude Code documentation excerpt into a six-card 小红书 post for AI tool learners. Keep technical terms accurate, explain the workflow in Chinese, and mark any assumptions.

[Paste source excerpt here.]
```

## 输入 / Inputs

- 来源: 用户提供的 Claude Code 文档摘录。
- 目标读者: 能阅读基础英文技术词的中文 AI 工具学习者。
- 渠道: 小红书 carousel / 卡片。
- 目标: 帮读者理解什么时候使用这个 workflow，以及如何安全尝试。
- 约束: 6 张卡、中文正文、不编造 claim、包含 source-backed notes / 来源说明。

## 预期 Skill 行为 / Expected Skill Behavior

Skill 应该：

- 先建立来源契约，再起草内容。
- 精确保留来源中描述的产品行为。
- 把密集文档拆成清楚卡片序列。
- 必要时使用 bilingual labels / 双语标签。
- 如果来源没有 setup、价格、模型、访问权限等信息，列为 assumptions / 假设。

Skill 不应该：

- 编造来源中没有的 Claude Code 功能。
- 没有证据地承诺效率提升。
- 大段引用文档原文。
- 隐藏当前产品行为的不确定性。

## 建议卡片结构 / Suggested Card Architecture

1. 这个 workflow 解决什么问题。
2. 这个工具或功能是什么，只基于来源说明。
3. 什么时候适合使用。
4. 如何一步步尝试。
5. 常见错误或限制。
6. 练习任务和下一步。

## 复核清单 / Review Checklist

- 每张卡只有一个任务。
- 技术名称准确。
- 中文解释清楚，但不过度简化。
- Claim 能追溯到来源摘录。
- Assumptions 与 facts 分开。
- Caption 邀请一个具体实践动作。

## 示例评测用例 / Example Eval Case

- 请求: 把一段 900 字工具文档摘录转成 6 张小红书卡片。
- 预期输出: 内容简报、6 张卡片草稿、caption、source-backed claims、editorial assumptions、quality check。
- 通过标准: 不编造产品细节，一张卡一个观点，中文适合创作者阅读，并且证据说明可见。

# SkillHub Scan Notes

这份 notes 用于观察公开 Skill 生态、marketplace 示例和社区共享的 Agent Skills。它不是穷尽式调研，而是为 SkillCraft 提炼可复用、可测试、可发布的模式。

## 扫描目标 / Scan Goal

重点观察：

- 什么场景触发这个 Skill。
- 它要求哪些输入。
- 它教 Agent 执行什么 workflow。
- 它承诺什么 output contract / 输出契约。
- 它包含哪些 quality checks / 质量检查和 failure boundaries / 失败边界。
- 它用什么 examples 或 eval cases / 评测用例证明自己有效。

## 记录字段 / What To Capture

| 字段 | 说明 |
| --- | --- |
| Name | Skill 名称或公开标题。 |
| Source | 仓库、marketplace 页面、文章或社区帖子。 |
| Target user | 创作者、开发者、分析师、作者、团队或其他。 |
| Trigger | Agent 何时应该使用它。 |
| Inputs | 需要的源文件、上下文、凭据或用户选择。 |
| Workflow | 主要执行步骤。 |
| Output | Skill 产出的 artifact。 |
| Validation | Examples、tests、screenshots、checklist evidence。 |
| Boundary | Skill 拒绝什么、追问什么、标记什么假设。 |
| Reuse pattern | SkillCraft 可以借鉴的模式。 |

## 初始模式库 / Initial Pattern Library

强 Skill 通常具备：

- 狭窄而明确的 job-to-be-done。
- `description` 命名真实触发场景。
- Workflow 不依赖作者私有经验。
- Output format 可以被复核。
- 资源文件只在减少重复劳动时出现。
- Failure boundaries 能防止事实编造、隐私泄露和不安全自动化。

弱 Skill-like artifacts 常见问题：

- 名字聪明，但触发场景不清。
- 承诺过宽，例如“做出更好内容”或“学会任何工具”。
- 没有输入契约。
- 没有稳定输出结构。
- 没有 examples 或 eval cases。
- 依赖原作者品味、语感或隐性领域知识。

## 对 SkillCraft 的含义 / SkillCraft Implications

- 每个 Skill 围绕一个可重复 artifact。
- 第一版就保留 eval templates，即使还没有自动化测试 runner。
- Examples 是 proof / 证明材料，不是装饰。
- 用中文创作者场景验证受众匹配，同时保持仓库结构和 metadata 对英文开发者可读。
- 宁可维护少量高质量 Skill，也不要快速堆一个提示词目录。

## 开放问题 / Open Questions

- 哪些 Skill 类别最适合新用户在一小时内验证？
- 哪些 example 最能解释 Skill 与 prompt 的区别？
- 中文正文和英文 metadata 的边界应该如何划分？
- 未来分发平台除了 `name` 和 `description` 还需要什么 metadata？
- 哪些 workflow 在下一阶段值得加入 scripts 或 assets？

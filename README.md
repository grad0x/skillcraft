# SkillCraft

SkillCraft 是一个面向中文 AI 创作者的开源 Skill Pack / 能力包实验：把可重复的内容生产、AI 工具学习和 Skill 工程实践，整理成可复用、可测试、可发布的 Agent Skills。

English summary: SkillCraft is a documentation-first public alpha for reusable Agent Skill workflows. It helps creators, technical writers, AI tool learners, and skill authors package repeatable work into testable `SKILL.md` files instead of one-off prompt collections.

## 项目一句话定位

SkillCraft 把真实工作流沉淀为 reusable workflow / 可复用工作流，让 AI Agent 能按明确的输入、workflow、output contract / 输出契约、quality check / 质量检查和 eval case / 评测用例来执行任务。

## SkillCraft 是什么 / What SkillCraft Is

SkillCraft 不是一个应用，也不是提示词合集。它是一个公开的 Skill Pack / 能力包仓库，第一阶段专注于文档化的 Agent Skills。

每个 Skill 都遵循 Codex Agent Skills 约定：

```text
.agents/skills/<skill-name>/SKILL.md
```

每个 `SKILL.md` 都包含：

- YAML frontmatter：`name` 和 `description`，用于 Agent 识别何时触发。
- 什么时候使用：明确适用任务和不适用边界。
- 输入要求：说明需要用户提供或 Agent 可推断的信息。
- 工作流程：可执行的步骤，而不是一句提示词。
- 输出格式：稳定的 output contract / 输出契约。
- 质量检查：可由人或 Agent 复核的 quality check / 质量检查。
- 失败边界：什么时候停止、追问或标记假设。

## 适合谁 / Who It Is For

- 中文 AI 创作者：把工具文档、教程、论文、经验笔记转成可发布内容。
- 技术内容作者：把一次性写作经验整理成可复用编辑流程。
- AI 工具学习者：用任务、练习和检查点学习工具，而不是只收藏教程。
- Skill 作者：设计、测试、发布可被 Agent 复用的 Skill 工作流。
- English-speaking developers: inspect the repository structure, `SKILL.md` metadata, examples, and eval checklists without needing to read every Chinese paragraph.

## 为什么 Skill 不只是提示词

提示词通常只描述“让模型生成什么”。Skill 要描述“Agent 如何完成一类可重复任务”。

一个可发布的 Skill 至少应该回答：

- 什么时候应该用它，什么时候不该用。
- 需要哪些输入，缺少输入时如何处理。
- 执行流程是什么，哪些步骤需要验证。
- 输出应长什么样，如何判断是否合格。
- 哪些事实、来源、隐私和安全边界不能越过。

这也是 SkillCraft 避免“万能提示词”和“爆款模板”定位的原因。本仓库关注 reusable workflow / 可复用工作流，而不是一次性的文案技巧。

## 第一批 Skill / First Four Skills

| Skill | 用途 | 主要产物 |
| --- | --- | --- |
| `doc-to-card` | 把文档、文章、教程、工具说明转成卡片式内容草稿。 | 卡片大纲、正文、证据说明、发布检查。 |
| `tool-learning-path` | 把 AI 工具或工作流整理成可练习的学习路径。 | 模块、练习、检查点、capstone 任务。 |
| `redskill-launch-plan` | 为一个可复用 Agent Skill 设计验证和发布计划。 | 定位、证明材料、渠道计划、反馈闭环。 |
| `skill-self-test` | 发布前检查一个 Skill 是否清晰、可执行、可评测。 | 自测报告、问题清单、eval case / 评测用例。 |

## 仓库结构 / Repository Structure

```text
.
├── .agents/skills/
│   ├── doc-to-card/SKILL.md
│   ├── tool-learning-path/SKILL.md
│   ├── redskill-launch-plan/SKILL.md
│   └── skill-self-test/SKILL.md
├── docs/
│   ├── redskill-distribution-playbook.md
│   ├── skillhub-scan-notes.md
│   └── validation-plan.md
├── evals/
│   ├── content-quality-checklist.md
│   └── skill-quality-checklist.md
├── examples/
│   └── claude-code-doc-to-card/README.md
└── templates/
    ├── SKILL.md.template
    ├── eval-cases.template.md
    └── examples.template.md
```

## 如何使用 / How To Use A Skill

1. 选择一个 Skill，例如 `.agents/skills/doc-to-card/SKILL.md`。
2. 给 Agent 明确任务和输入材料，例如源文档、目标读者、发布渠道、约束。
3. 要求 Agent 按该 Skill 的 workflow 执行，并按 output contract / 输出契约交付。
4. 用 `evals/` 下的 checklist 或对应 Skill 的 quality check / 质量检查复核结果。
5. 把真实运行结果整理到 `examples/`，把失败案例整理成 eval case / 评测用例。

示例请求：

```text
Use the doc-to-card skill at .agents/skills/doc-to-card/SKILL.md to turn this AI tool documentation excerpt into a six-card 小红书 draft for Chinese AI tool learners. Keep the output in Chinese and mark assumptions.
```

## 当前状态 / Current Status

- Alpha version / 公开 alpha。
- Documentation-first / 文档优先。
- No runtime, no web app yet / 暂无运行时、暂无 Web 应用。
- No dependency setup / 暂无依赖、包管理或构建系统。
- First milestone / 第一阶段目标：用真实 RedSkill 和创作者工作流验证第一批 Skill 是否真的有用。

详细 alpha 验证计划见 [docs/validation-plan.md](docs/validation-plan.md)。

## 许可 / License

License is not selected yet. A license file should be added before a formal public release.

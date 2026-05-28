---
name: redskill-launch-plan
description: Plan the packaging, validation, and distribution of reusable Agent Skills for Chinese AI creator audiences, technical writers, and skill authors. Use when a draft skill or workflow needs a launch plan with positioning, proof assets, channel strategy, feedback loops, and publishable documentation instead of a generic marketing prompt.
---

# Redskill Launch Plan

默认用中文输出，除非用户明确要求英文。保留 Skill、Skill Pack、Agent Skill、eval case 等关键术语，并给出中文解释。目标用户包括中文 AI 创作者、技术内容作者、AI 工具学习者和 Skill 作者。

## 什么时候使用 / When To Use

当用户已经有一个 Skill、可复用 workflow 或可重复 AI 实践，并希望把它做成公开 alpha、社区测试或正式发布计划时，使用这个 Skill。

在 SkillCraft 中，RedSkill 指面向创作者分发的 reusable Agent Skill：有清楚问题、触发场景、输入要求、output contract / 输出契约、证明材料和反馈闭环。

适合：

- 发布新的 `.agents/skills/<skill-name>/SKILL.md`。
- 把已验证的内容工作流包装成 Skill Pack / 能力包。
- 为 GitHub、小红书、公众号、社群或工作坊准备发布材料。
- 在宣传前先补齐 proof assets / 证明材料和 eval case / 评测用例。

不适合：空泛个人品牌计划、没有可运行 Skill 的营销方案、夸大增长承诺、只想写一条宣传文案的任务。

## 输入要求 / Inputs

尽量从用户请求中提取；如果没有 Skill artifact，要先建议验证而不是发布。

- Skill 名称和当前阶段：idea、draft、tested、published、iterating。
- 目标用户：中文 AI 创作者、技术内容作者、AI 工具学习者、开发团队、Skill 作者等。
- Job-to-be-done：这个 Skill 反复解决的具体任务。
- 当前材料：`SKILL.md`、example、eval case、截图、before/after、用户反馈。
- 发布渠道：GitHub、小红书、公众号、社群、newsletter、workshop、内部文档等。
- 时间窗口和维护能力。
- 边界：不能宣称的内容、未验证平台、隐私限制、合规风险。

## 工作流程 / Workflow

1. 定义可发布单元。
   - 写清 Skill 名称、文件路径和它包装的具体 workflow。
   - 用操作性语言描述用户痛点。
   - 区分真正可复用的部分和仍依赖作者经验的部分。

2. 检查发布准备度。
   - 确认 `SKILL.md` 有 frontmatter、触发场景、输入、workflow、输出格式、质量检查和边界。
   - 确认至少有一个真实 example。
   - 确认至少有一个 checklist 或 eval case / 评测用例。

3. 写定位。
   - 用“给谁，在什么场景下，帮助产出什么可检查结果”的句式。
   - 说明它为什么是 Skill workflow，而不是 prompt pack / 提示词包。
   - 避免“掌握 AI”“效率翻倍”“一键自动化”等无法证明的承诺。

4. 组织证明材料。
   - 选择一个 before/after。
   - 选择一个带注释的 Skill 片段。
   - 选择一个 checklist 或 eval 结果。
   - 设计一个新用户能复现的 demo path / 演示路径。

5. 规划渠道分发。
   - GitHub：README、examples、evals、issue 引导。
   - 小红书：问题卡、workflow 卡、产物证明、招募测试。
   - 公众号：设计原则、完整 walkthrough、验证记录。
   - 社群：面向特定用户的窄反馈请求。

6. 设计反馈闭环。
   - 明确要收集什么反馈。
   - 定义 patch criteria / 修订标准。
   - 设定 review date / 复盘日期。
   - 把真实失败案例转成 eval case。

## 输出格式 / Output Format

按下面结构输出 Markdown：

```markdown
## 发布简报 / Launch Brief

- Skill:
- 目标用户:
- Job-to-be-done:
- 当前阶段:
- 发布目标:

## 准备度检查 / Readiness Check

| 要求 | 状态 | 说明 |
| --- | --- | --- |

## 定位 / Positioning

- 一句话:
- 详细说明:
- 不要这样说:

## 证明材料 / Proof Assets

- Demo artifact:
- Before/after:
- Eval or checklist:
- 用户反馈:

## 渠道计划 / Channel Plan

### GitHub

- 需要的材料:
- 发布文案:
- Call to action:

### 小红书 / 公众号 / 社群

- 需要的材料:
- 发布文案:
- Call to action:

## 反馈闭环 / Feedback Loop

- 要问的问题:
- 成功信号:
- Patch criteria:
- Review date:
```

## 质量检查 / Quality Checks

- 计划围绕一个具体 Skill artifact，而不是抽象想法。
- 每个公开 claim 都有 example、eval、用户反馈或明确标记为 hypothesis / 假设。
- 不同渠道的表达有差异，不是复制同一段文案。
- 发布请求能获得有用反馈，而不是泛泛求关注。
- 包含维护、复盘和 patch criteria / 修订标准。
- 定位强调可复用、可测试、可发布的 Skill workflow。

## 不适用场景 / Failure Boundaries

- 不编造用户数量、评价、采用数据、benchmark 或官方背书。
- 不推荐垃圾营销、虚假稀缺、诱导转发或未披露推广。
- 不发布未经授权的私人案例、内部文档、用户截图或敏感数据。
- 不为未经测试的 Skill 设计大规模发布；应先建议小范围验证。
- 如果涉及法律、平台政策或合规问题，标记为需要人工审核。

## 示例输入 / Example Input

```text
我有一个 doc-to-card Skill，已经能把工具文档转成小红书卡片。请帮我设计一个公开 alpha 发布计划，目标用户是中文 AI 创作者。已有材料：SKILL.md、一个 Claude Code 文档转卡片 example、一个内容质量 checklist。不要编造用户反馈。
```

## 示例输出结构 / Example Output Structure

```markdown
## 发布简报 / Launch Brief

- Skill: doc-to-card
- 目标用户: 中文 AI 创作者、AI 工具学习者
- Job-to-be-done: 把来源文档转成有证据说明的卡片内容
- 当前阶段: alpha tested
- 发布目标: 招募 3 个真实材料测试

## 准备度检查 / Readiness Check

| 要求 | 状态 | 说明 |
| --- | --- | --- |
| SKILL.md 有完整结构 | Pass | 已包含输入、workflow、输出格式和边界 |

...

## 反馈闭环 / Feedback Loop

- 要问的问题: 哪一步最难复用？
- 成功信号: 测试者能用自己的来源材料产出可检查草稿
- Patch criteria: 同一问题出现两次即更新 Skill
```

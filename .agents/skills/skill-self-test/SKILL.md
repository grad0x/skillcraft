---
name: skill-self-test
description: Evaluate an Agent Skill before publishing by checking structure, trigger clarity, input contract, workflow usefulness, output format, quality checks, failure boundaries, examples, and eval cases. Use when skill authors, technical writers, or Chinese AI creator teams need a practical review of a skill file under `.agents/skills/skill-name/SKILL.md` or a draft skill pack before release.
---

# Skill Self Test

默认用中文输出，除非用户明确要求英文。保留 Agent Skill、frontmatter、output contract、eval case 等关键术语。目标用户包括中文 AI 创作者、技术内容作者、AI 工具学习者和 Skill 作者。

## 什么时候使用 / When To Use

当用户想发布、改进或复核一个 Agent Skill，并需要判断它是否清晰、可执行、可测试时，使用这个 Skill。

适合：

- 发布前检查一个 `.agents/skills/<skill-name>/SKILL.md`。
- 判断一个 Skill 是否只是 prompt template / 提示词模板。
- 为 Skill 添加或改进 eval case / 评测用例。
- 把模糊 workflow 改成稳定 output contract / 输出契约。

不适合：替代真实任务运行、保证生产安全、只做 Markdown 文风润色、在用户未提供 Skill 内容时凭空评价。

## 输入要求 / Inputs

尽量从用户请求中提取；缺失关键材料时先要求补充。

- Skill 文件路径或粘贴的 `SKILL.md` 内容。
- 预期用户：中文 AI 创作者、技术内容作者、AI 工具学习者、Skill 作者、团队内部用户等。
- 触发场景：用户会在什么任务中调用这个 Skill。
- 示例请求或历史运行结果。
- 期望输出或样例产物。
- 已知风险：过时文档、平台政策、隐私数据、专业领域、当前产品事实。
- 发布阶段：draft、alpha、beta、public release、maintenance update。

如果无法读取 Skill 内容，只输出“无法评测”的缺口说明，不要编造结论。

## 工作流程 / Workflow

1. 检查基础结构。
   - 确认 YAML frontmatter 存在。
   - 确认 frontmatter 至少包含 `name` 和 `description`。
   - 确认 `name` 与文件夹名一致。
   - 确认正文不是占位内容。

2. 检查触发质量。
   - 把 `description` 当成 Agent 选择 Skill 的主要依据来读。
   - 确认它说明“做什么”和“什么时候用”。
   - 标记过宽、过窄、太抽象或缺少具体场景的描述。

3. 检查执行契约。
   - 确认正文包含什么时候使用、输入要求、workflow、输出格式、quality checks 和 failure boundaries。
   - 找出依赖作者隐性经验的步骤。
   - 判断是否需要 examples、references、assets 或 scripts，但不要强行添加。

4. 检查输出契约。
   - 确认 output format / 输出格式足够稳定，另一个 Agent 能照着交付。
   - 确认输出可以被人或 Agent 复核。
   - 标记“给出建议”“写得好一点”这类不可评测输出。

5. 检查边界和风险。
   - 查找编造来源、当前产品事实、隐私数据和高风险领域问题。
   - 确认缺少关键输入时会追问、标记假设或停止。

6. 设计 eval case / 评测用例。
   - 至少给 easy、normal、edge 三类案例。
   - 每个案例包含请求、预期输出和 pass criteria / 通过标准。
   - 案例必须对应真实目标用户，而不是抽象测试。

## 输出格式 / Output Format

按下面结构输出 Markdown：

```markdown
## Skill 自测报告 / Skill Self-Test Report

- Skill:
- 路径:
- 阶段:
- 总体状态: Pass / Needs revision / Blocked

## 发现的问题 / Findings

| 严重程度 | 区域 | 问题 | 建议 |
| --- | --- | --- | --- |

## 必须修复 / Required Fixes

- <具体修改>

## 建议改进 / Suggested Improvements

- <具体改进>

## 评测用例 / Eval Cases

### Easy

- 请求:
- 预期输出:
- 通过标准:

### Normal

- 请求:
- 预期输出:
- 通过标准:

### Edge

- 请求:
- 预期输出:
- 通过标准:

## 发布建议 / Release Recommendation

<可以发布、先小范围测试、需要修订、阻塞发布及原因>
```

## 质量检查 / Quality Checks

- 报告先列阻塞问题，再列风格或可读性问题。
- 每个 finding 都有可执行建议。
- 检查 Agent 触发逻辑，而不只是 Markdown 排版。
- eval case / 评测用例贴近目标用户和真实工作。
- 发布建议与问题严重程度一致。
- 不因为 Skill 是文档优先就强行要求 scripts 或 app code。

## 不适用场景 / Failure Boundaries

- 不在没有真实任务运行的情况下认证 Skill “生产可用”。
- 不自动重写 Skill，除非用户明确要求编辑。
- 不忽略私有数据、当前产品事实、平台政策或高风险领域。
- 不把主观文风偏好当作发布阻塞。
- 如果 Skill 依赖外部工具或当前产品行为，要求权威来源验证。

## 示例输入 / Example Input

```text
请用 skill-self-test 检查 .agents/skills/doc-to-card/SKILL.md 是否适合公开 alpha。目标用户是中文 AI 创作者和技术内容作者。重点看它是不是可复用 workflow，而不是 prompt template。
```

## 示例输出结构 / Example Output Structure

```markdown
## Skill 自测报告 / Skill Self-Test Report

- Skill: doc-to-card
- 路径: .agents/skills/doc-to-card/SKILL.md
- 阶段: public alpha
- 总体状态: Needs revision

## 发现的问题 / Findings

| 严重程度 | 区域 | 问题 | 建议 |
| --- | --- | --- | --- |
| Medium | Output contract | 示例输出缺少来源声明字段 | 在 output format 中加入 Source-Backed Claims |

## 评测用例 / Eval Cases

### Edge

- 请求: 来源材料只有 120 字，但要求生成 10 张卡
- 预期输出: 材料不足报告
- 通过标准: 不编造内容，并列出缺少的输入
```

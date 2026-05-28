# Eval Cases Template

用于为 SkillCraft Skill 创建轻量评测用例。每个 Skill 至少需要 easy、normal、edge 三类 eval case / 评测用例。

## 被测 Skill / Skill Under Test

- Skill:
- Version or commit:
- Reviewer:
- Date:
- Source files:

## Eval Case: Easy

- 请求:
- 必要输入:
- 预期输出:
- 通过标准:
- 常见失败:
- Notes:

## Eval Case: Normal

- 请求:
- 必要输入:
- 预期输出:
- 通过标准:
- 常见失败:
- Notes:

## Eval Case: Edge

- 请求:
- 必要输入:
- 预期输出:
- 通过标准:
- 常见失败:
- Notes:

## 评分 / Scoring

| 分数 | 含义 |
| --- | --- |
| 0 | 核心任务失败，或编造关键信息。 |
| 1 | 产物不完整，缺少必要结构或重要约束。 |
| 2 | 产物可用，但有少量缺口。 |
| 3 | 产物强，满足 output contract / 输出契约、quality checks / 质量检查和边界要求。 |

## 发布判断 / Decision Rule

- Publish: easy 和 normal 都得 3 分，edge 至少 2 分，且没有边界违规。
- Revise: 任一案例得 1 或 2 分，但问题可修复。
- Block: 任一案例得 0 分、泄露私有数据、编造事实或违反明确边界。

# Alpha Validation Plan

这个计划用于验证第一批 Skill 是否真的有用。它是公开 alpha 阶段的验证说明，不是项目主页内容，也不是长期路线图。

## 验证目标

- 检查四个初始 Skill 是否能处理真实中文 AI 创作者和技术内容作者的材料。
- 确认每个 Skill 的 output contract / 输出契约是否足够清晰。
- 找出 workflow 中依赖作者隐性经验的步骤。
- 把失败案例沉淀成 eval case / 评测用例。
- 决定哪些内容应该进入 Skill 正文、examples、evals 或 docs。

## 七天验证计划

Day 1: Use `doc-to-card` on three source types: product docs, a tutorial, and a personal note. Record whether the card outline preserves the source meaning.

Day 2: Use `tool-learning-path` for one AI coding tool and one AI writing tool. Check whether exercises can be completed without hidden assumptions.

Day 3: Use `redskill-launch-plan` to package one draft skill into a public-facing release plan. Validate that every claim has a proof artifact.

Day 4: Use `skill-self-test` against all four initial skills. File issues for unclear triggers, missing inputs, weak outputs, and vague quality checks.

Day 5: Ask two Chinese AI creators or technical writers to run one skill each on their own material. Collect friction points in their own words.

Day 6: Convert feedback into eval cases under `evals/` and update the templates so future skills inherit the better pattern.

Day 7: Publish a small release note with the tested examples, known limitations, and next candidate skills.

## 记录格式

每次验证至少记录：

- 使用的 Skill。
- 输入材料类型。
- 目标用户。
- 输出是否符合 output contract / 输出契约。
- 哪个 quality check / 质量检查发现了问题。
- 是否出现事实编造、边界不清或中文表达不自然。
- 应该更新到哪个文件：`SKILL.md`、`examples/`、`evals/` 或 `docs/`。

## 通过标准

- 每个 Skill 至少有一个真实案例跑通。
- 每个 Skill 至少有一个 edge case / 边界案例。
- README 不再承担内部执行计划的角色。
- 中文用户可以直接理解用途和使用方式。
- English-speaking developers can still inspect the repo structure, metadata, examples, and validation artifacts.

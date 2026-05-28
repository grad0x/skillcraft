# Skill Quality Checklist

发布或更新 SkillCraft Skill 前使用这份 checklist。它检查的是 Skill 是否可复用、可测试、可发布，不是只检查 Markdown 是否好看。

## 必要结构 / Required Structure

- [ ] Skill 位于 `.agents/skills/<skill-name>/SKILL.md`。
- [ ] 文件夹名使用小写字母、数字和连字符。
- [ ] YAML frontmatter 存在。
- [ ] Frontmatter 包含 `name`。
- [ ] Frontmatter 包含 `description`。
- [ ] `name` 与文件夹名一致。
- [ ] `description` 说明 Skill 做什么以及何时使用。
- [ ] 正文不是占位内容。

## 执行契约 / Execution Contract

- [ ] Skill 定义什么时候使用 / When to use。
- [ ] Skill 定义输入要求 / Inputs。
- [ ] Workflow 是可执行步骤，不是泛泛建议。
- [ ] Output format 形成稳定 output contract / 输出契约。
- [ ] Quality checks / 质量检查可观察。
- [ ] Failure boundaries / 失败边界说明何时停止、追问或收窄范围。
- [ ] 包含示例输入和示例输出结构。

## 可复用性 / Reusability

- [ ] Skill 解决一类可重复任务，而不是一次性内容需求。
- [ ] Skill 避免 generic prompt-library / 通用提示词库表达。
- [ ] Workflow 可用真实案例测试。
- [ ] 领域假设被明确写出。
- [ ] `references/`、`assets/` 或 `scripts/` 只在减少重复劳动时添加。

## 触发质量 / Trigger Quality

- [ ] `description` 包含具体使用场景。
- [ ] `description` 命名重要 artifact 类型或用户意图。
- [ ] Skill 足够聚焦，Agent 能判断何时选择它。
- [ ] 正文说明相近但不适用的场景。

## 安全与边界 / Safety And Boundaries

- [ ] Skill 不鼓励编造事实、来源、指标、案例或评价。
- [ ] 涉及私有或敏感数据时有明确处理方式。
- [ ] 当前产品行为、价格、模型、政策等易变信息要求验证或标记假设。
- [ ] 高风险领域要求人工或专家复核。

## 发布判断 / Release Decision

- Publish: 必要结构全通过，且没有边界问题。
- Revise: output contract、示例、trigger description 或 eval case 仍弱。
- Block: Skill 无法按说明执行，或鼓励不受支持的事实声明。

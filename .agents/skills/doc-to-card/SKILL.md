---
name: doc-to-card
description: Convert source documents, articles, tutorials, notes, or tool documentation into structured educational card content for Chinese AI creators, technical writers, and bilingual developer audiences. Use when a user wants to transform dense material into publishable multi-card posts, carousel drafts, WeChat sections, 小红书 notes, or internal knowledge cards while preserving evidence and avoiding prompt-library style shortcuts.
---

# Doc To Card

默认用中文输出，除非用户明确要求英文。保留必要英文技术词，并在第一次出现时给出中文解释。目标用户包括中文 AI 创作者、技术内容作者、AI 工具学习者和 Skill 作者。

## 什么时候使用 / When To Use

当用户提供一段来源材料，并希望把它转成卡片式、可发布、可复核的教育内容时，使用这个 Skill。

适合：

- 把 AI 工具文档、产品更新、教程或技术文章转成小红书卡片、公众号段落、LinkedIn carousel 或内部知识卡。
- 把一段复杂说明拆成“问题、概念、步骤、例子、注意事项、行动建议”。
- 把可重复工作流写成面向读者的卡片内容，同时保留证据和假设。
- 需要中文表达，但仍要保留英文工具名、API 名、模型名或命令名的准确性。

不适合：没有来源材料的情绪化内容、纯营销标题、泛泛的爆款模板、只需要润色一句文案的任务。

## 输入要求 / Inputs

尽量从用户请求中提取；缺失会影响事实准确性时要追问。

- 来源材料：粘贴文本、文件路径、用户摘录、笔记或明确摘要。
- 目标读者：中文 AI 创作者、技术内容作者、AI 工具学习者、开发者、团队成员等。
- 发布渠道：小红书、公众号、LinkedIn、内部 wiki、幻灯片、知识库等。
- 内容目标：教学、总结、对比、发布、入门、复盘、转化。
- 输出约束：卡片数量、语言、语气、引用要求、不能声称的内容、是否需要视觉建议。
- 验证要求：是否需要 source-backed claims / 来源支撑声明、assumptions / 假设列表。

如果来源材料不足，先说明缺口；不要凭经验补产品功能、数据、价格或发布日期。

## 工作流程 / Workflow

1. 建立来源契约。
   - 标明来源类型、标题或产品名、日期信息和可信度。
   - 区分 source facts / 来源事实、editorial interpretation / 编辑解释和 assumptions / 假设。
   - 对当前产品能力、价格、模型、政策等易变信息标记“需要验证”。

2. 提取内容主干。
   - 找到核心问题、关键概念、步骤、例子、限制和读者下一步。
   - 删除重复铺垫、营销空话和无法从来源推出的结论。
   - 保留必要技术词，给中文解释时避免改变原意。

3. 选择卡片结构。
   - 工具文档：是什么 -> 什么时候用 -> 如何开始 -> 工作流 -> 常见错误 -> 练习任务。
   - 教程文章：问题 -> 心智模型 -> 步骤 -> 示例 -> 检查清单 -> 下一步。
   - 观点文章：主张 -> 证据 -> 影响 -> 反例或限制 -> 行动建议。
   - Skill 工作流：触发场景 -> 输入 -> workflow -> output contract / 输出契约 -> quality check / 质量检查 -> failure boundary / 失败边界。

4. 起草卡片。
   - 每张卡只承担一个任务。
   - 卡片标题直接表达读者将获得什么。
   - 正文使用具体名词和动词，避免“提升效率”“赋能创作”这类空泛表达。
   - 对中文平台优先写中文正文；英文技术词保留原文。

5. 添加证据和生产说明。
   - 为关键 claim 标注来源依据或“编辑假设”。
   - 视觉建议只作为制作提示，不伪装成已有素材。
   - 添加 caption / 配文和明确 call to action / 行动请求。

6. 做发布前检查。
   - 检查读者是否能从卡片还原来源逻辑。
   - 删除无法从来源支持的推断。
   - 检查卡片顺序是否像一个教学路径，而不是零散 tips。

## 输出格式 / Output Format

按下面结构输出 Markdown：

```markdown
## 内容简报 / Content Brief

- 来源:
- 目标读者:
- 发布渠道:
- 内容目标:
- 角度:
- 需要验证的信息:

## 卡片草稿 / Card Draft

### Card 1: <标题>

- 这张卡的任务:
- 卡片正文:
- 视觉建议:
- 证据说明:

### Card 2: <标题>

...

## 配文 / Caption

<可直接发布或继续编辑的中文配文>

## 来源支撑声明 / Source-Backed Claims

- <声明> -> <来源依据>

## 编辑假设 / Editorial Assumptions

- <假设> -> <为什么需要这个假设>

## 质量检查 / Quality Check

- <通过或需要修订的说明>
```

## 质量检查 / Quality Checks

- 每张卡只有一个明确功能。
- 卡片顺序形成可理解的教学路径或决策路径。
- 来源事实、编辑解释和假设被清楚分开。
- 没有编造工具能力、价格、模型、时间、数据或用户反馈。
- 中文表达适合目标渠道，但没有牺牲技术准确性。
- 输出是可继续设计、编辑或发布的内容草稿，而不是单段摘要。

## 不适用场景 / Failure Boundaries

- 不为没有来源材料的任务编造“知识卡”。
- 不大段复写受版权保护的原文。
- 不处理需要专业审核的医疗、法律、金融或安全关键建议，除非明确标记为需专家复核。
- 如果用户要求夸大效果、伪造案例或隐藏不确定性，要拒绝这部分要求并给出可替代的真实表达。
- 如果来源太薄，只输出“材料不足报告”和需要补充的输入。

## 示例输入 / Example Input

```text
把下面这段 AI 编程工具更新说明转成 6 张小红书卡片，面向中文 AI 工具学习者。要求中文输出，保留英文功能名，不要编造文档里没有的能力，并列出需要验证的假设。

[用户粘贴来源摘录]
```

## 示例输出结构 / Example Output Structure

```markdown
## 内容简报 / Content Brief

- 来源: 用户提供的 AI 编程工具更新说明
- 目标读者: 中文 AI 工具学习者
- 发布渠道: 小红书
- 内容目标: 帮读者理解这个更新适合什么场景
- 角度: 从“什么时候该用”切入，而不是罗列功能

## 卡片草稿 / Card Draft

### Card 1: 这个更新解决的不是“写代码”，而是“少走错流程”

- 这张卡的任务: 建立问题场景
- 卡片正文: ...
- 视觉建议: ...
- 证据说明: 来自来源第 1 段对 workflow 的描述

...

## 来源支撑声明 / Source-Backed Claims

- 该功能支持某个 workflow -> 来源第 2 段

## 编辑假设 / Editorial Assumptions

- 读者已了解基础命令行操作 -> 来源未说明，因目标读者设定而假设
```

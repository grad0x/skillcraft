# Same Source, Three Styles

这个 example 使用一段虚构来源，演示同一来源可以生成三种不同卡片产品。风格会改变表达、卡片节奏和视觉方向，但不能改变来源事实。

## Fictional Source Excerpt / 虚构来源摘录

```text
CodePilot 2.4 adds a Review Plan mode for AI coding sessions. Before editing files, the agent now summarizes the intended change, lists affected files, and waits for user approval. The update also adds a Change Notes panel that records assumptions and open questions during the session. The release note says Review Plan is optional and can be disabled per workspace. It does not mention pricing, supported IDEs beyond the existing desktop client, or benchmark results.
```

## Source Understanding Layer / 来源理解层

### Source Facts / 来源事实

- CodePilot 2.4 新增 `Review Plan mode`。
- 在编辑文件前，agent 会总结计划改动、列出受影响文件，并等待用户批准。
- 新增 `Change Notes panel`，用于记录 session 中的 assumptions / 假设和 open questions / 开放问题。
- `Review Plan mode` 是 optional / 可选功能，可按 workspace 禁用。
- 来源没有提到价格、除现有 desktop client 之外的 IDE 支持，也没有 benchmark results / 基准结果。

### Source Logic / 来源逻辑

- 更新重点不是“让 agent 写更多代码”，而是在改文件前增加 review checkpoint / 复核检查点。
- `Change Notes panel` 支撑过程透明度，让假设和问题不再散落在对话中。
- 可按 workspace 禁用说明该功能适合按团队或项目差异化使用。

### Boundaries / 边界

- 不能宣称它提升了代码质量或开发速度。
- 不能宣称它支持所有 IDE。
- 不能宣称它是默认开启，来源只说 optional。

## Style 1: 小红书轻知识卡

### Style Profile

- Channel / 渠道: 小红书
- Target audience / 目标读者: 中文 AI 编程工具学习者
- Card count / 卡片数量: 6
- Density / 信息密度: 轻到中
- Tone / 语气: 轻解释、清楚、不夸张
- Visual direction / 视觉方向: 大标题 + 短 bullet + 简单流程箭头
- Title strategy / 标题策略: 问题型、误区提醒型
- Evidence requirement / 证据要求: 关键 claim 附来源说明
- CTA style / 行动引导: 收藏并试一次 review checkpoint
- Things to avoid / 禁用表达: 一键提效、私藏神器、效率翻倍

### Content Brief

- 角度: AI coding 工具更新的重点是“改文件前先给你看计划”。
- 卡片架构: 工具文档型。
- 需要验证的信息: 价格、IDE 支持、是否默认开启。

### Sample Cards

#### Card 1: AI 写代码前，先让它“交计划”

- 这张卡的任务: 用轻解释方式建立问题场景。
- 卡片正文: CodePilot 2.4 新增 `Review Plan mode`。它不是让 agent 直接冲去改文件，而是在编辑前先总结要改什么、会影响哪些文件，再等你批准。
- 视觉建议: 左侧“以前：直接改”，右侧“现在：先计划再批准”。
- 证据说明: 来源明确说明编辑前会总结改动、列出文件并等待批准。

#### Card 2: 这个更新适合怕 agent 改太快的人

- 这张卡的任务: 说明使用场景。
- 卡片正文: 如果你担心 AI coding session 里改动失控，这个模式提供了一个 review checkpoint / 复核检查点。
- 视觉建议: 警示图标 + “先看计划”。
- 证据说明: “等待用户批准”来自来源；“适合怕改太快的人”是编辑解释。

#### Card 3: 还有一个 Change Notes panel

- 这张卡的任务: 介绍第二个关键功能。
- 卡片正文: 新增面板会记录 assumptions / 假设和 open questions / 开放问题。这样复盘时不用翻整段对话。
- 视觉建议: 对话气泡 -> notes panel。
- 证据说明: 来源明确说明面板记录 assumptions 和 open questions。

## Style 2: 技术深读卡

### Style Profile

- Channel / 渠道: 公众号或 LinkedIn carousel
- Target audience / 目标读者: 进阶 AI coding 用户、技术内容作者
- Card count / 卡片数量: 7
- Density / 信息密度: 高
- Tone / 语气: 理性、机制分析
- Visual direction / 视觉方向: 流程图、对比表、证据框
- Title strategy / 标题策略: 机制型、结论型
- Evidence requirement / 证据要求: 逐条 source-backed claims
- CTA style / 行动引导: 复现实验并记录失败案例
- Things to avoid / 禁用表达: 趋势化空话、无证据效率提升

### Content Brief

- 角度: `Review Plan mode` 把 AI coding session 从直接执行改成带审批节点的协作流程。
- 卡片架构: 对比型 + 工具文档型。
- 需要验证的信息: 默认状态、企业策略、IDE 范围、性能或质量指标。

### Sample Cards

#### Card 1: 这次更新改变的是 AI coding 的控制面

- 这张卡的任务: 给出技术分析主张。
- 卡片正文: `Review Plan mode` 在文件编辑前插入计划摘要、受影响文件列表和用户批准。这让执行链路从“agent 决定后直接改”变成“agent 提案 -> 人类批准 -> 再执行”。
- 视觉建议: 三段式流程图。
- 证据说明: 前半句来自来源；流程抽象是基于来源的编辑解释。

#### Card 2: Change Notes 是过程可追踪性的补丁

- 这张卡的任务: 解释第二个机制。
- 卡片正文: `Change Notes panel` 记录 assumptions 和 open questions。它解决的不是代码生成能力，而是 session 中决策上下文容易丢失的问题。
- 视觉建议: “Assumption / Open Question / Decision” 三列表。
- 证据说明: 来源支持记录内容；“决策上下文”是解释性概括。

#### Card 3: 不能从这份 release note 推出什么

- 这张卡的任务: 明确证据边界。
- 卡片正文: 来源没有提供 pricing、额外 IDE 支持或 benchmark results。因此不能写“性能提升”“支持所有 IDE”或“性价比更高”。
- 视觉建议: 红色 boundary box。
- 证据说明: 来源明确说未提及这些内容。

## Style 3: 内部培训知识卡

### Style Profile

- Channel / 渠道: 内部 wiki / 团队知识库
- Target audience / 目标读者: 准备试用 AI coding 工具的研发团队
- Card count / 卡片数量: 5
- Density / 信息密度: 中到高
- Tone / 语气: 操作型、直接
- Visual direction / 视觉方向: SOP 卡、检查清单、风险提示
- Title strategy / 标题策略: 任务型、风险提醒型
- Evidence requirement / 证据要求: 团队假设与来源事实分离
- CTA style / 行动引导: 试点 workspace 并记录 open questions
- Things to avoid / 禁用表达: 社媒语气、营销话术、无法执行的建议

### Content Brief

- 角度: 团队试用时，应把 `Review Plan mode` 当成变更审批节点测试。
- 卡片架构: Skill 工作流型。
- 需要验证的信息: 团队 workspace 是否可用、禁用策略、IDE 范围。

### Sample Cards

#### Card 1: 试点目标：验证“改前审批”是否适合团队流程

- 这张卡的任务: 定义内部试点目标。
- 卡片正文: CodePilot 2.4 的 `Review Plan mode` 会在编辑文件前展示计划和受影响文件，并等待批准。团队试点时应重点观察它是否减少误改风险，而不是直接假设效率提升。
- 视觉建议: SOP 封面卡 + “不要预设结论”提示。
- 证据说明: 功能行为来自来源；“减少误改风险”是需要试点验证的假设。

#### Card 2: 团队使用步骤

- 这张卡的任务: 给出可执行流程。
- 卡片正文: 1. 选择一个低风险 workspace。2. 开启 `Review Plan mode`。3. 让 agent 提交改动计划。4. 检查受影响文件。5. 批准或要求修改计划。6. 记录 open questions。
- 视觉建议: 6 步流程条。
- 证据说明: 来源支持可按 workspace 禁用和改前批准；低风险 workspace 是团队执行建议。

#### Card 3: 必须记录的问题

- 这张卡的任务: 形成复盘记录。
- 卡片正文: 每次 session 记录三类信息：agent 提出的 assumptions、未解决 open questions、被拒绝或修改的计划。
- 视觉建议: checklist 表格。
- 证据说明: 来源支持 `Change Notes panel` 记录 assumptions 和 open questions；被拒绝计划是培训建议。

## What Changed Across Styles / 风格变化

- 小红书轻知识卡更短，强调“为什么值得注意”和“怎么试一次”。
- 技术深读卡信息密度更高，强调机制、流程抽象和证据边界。
- 内部培训知识卡更像 SOP，强调团队试点、记录和复盘。
- 标题策略从轻解释变成机制分析，再变成任务执行。
- 视觉方向从大标题短卡，变成流程图和证据框，再变成 checklist 和 SOP。
- CTA 从收藏/试一次，变成复现实验，再变成团队执行和记录问题。

## What Stayed Invariant / 不变内容

- `Review Plan mode` 的来源事实不变：编辑前总结计划、列出受影响文件、等待批准。
- `Change Notes panel` 的来源事实不变：记录 assumptions 和 open questions。
- `Review Plan mode` 是 optional，且可按 workspace 禁用。
- 不能宣称价格、额外 IDE 支持或 benchmark results。
- 不能把“可能减少误改风险”写成已验证结论。

# Google ADK Controlled Summary, Three Styles

这是 `doc-to-card` 的 Level 1 controlled-source smoke test / 受控来源冒烟测试。

本测试只使用用户提供的 controlled source summary / 受控来源摘要，不声称已经阅读 Google ADK 原始全文，也不测试网页浏览、全文抽取或外部事实验证。测试目标是观察：同一组固定来源事实，是否能生成三种明显不同的卡片产品，同时保持 source fidelity / 来源保真。

## Controlled Source Summary / 受控来源摘要

```text
* Google ADK discusses long-running AI agents that can pause and resume.
* The article emphasizes explicit workflow state instead of relying only on chat history.
* It uses persistent checkpoint/session state so an agent can resume after waiting, restart, or external events.
* It describes event-driven resume patterns, such as using webhooks to continue a workflow.
* It mentions golden evaluations for testing multi-step or multi-day agent flows without waiting in real time.
```

## Source Understanding Layer / 来源理解层

### Source Contract / 来源契约

- 来源类型: 用户提供的 controlled source summary / 受控摘要。
- 来源主题: Google ADK 与 long-running AI agents / 长运行 AI agent。
- 原文阅读状态: 未声明已阅读全文；本示例只基于上方五条摘要事实。
- 测试用途: 验证 `doc-to-card` 的 style rendering / 风格渲染能力，而不是验证原文抽取完整性。

### Source Facts / 来源事实

- Google ADK 讨论可以 pause and resume / 暂停与恢复的 long-running AI agents / 长运行 AI agent。
- 摘要强调 explicit workflow state / 显式工作流状态，而不是只依赖 chat history / 聊天历史。
- 摘要提到 persistent checkpoint/session state / 持久化检查点或会话状态，使 agent 可以在等待、重启或外部事件后恢复。
- 摘要描述 event-driven resume patterns / 事件驱动恢复模式，例如用 webhooks / Webhook 继续一个 workflow / 工作流。
- 摘要提到 golden evaluations / 黄金评测，可用于测试 multi-step or multi-day agent flows / 多步骤或多天 agent 流程，而不必按真实时间等待。

### Source Logic / 来源逻辑

- 长运行 agent 的核心问题不是单次回答，而是 workflow / 工作流可能跨越等待、重启或外部事件。
- 只依赖 chat history 容易不足，因此需要 explicit workflow state 和 persistent checkpoint/session state。
- event-driven resume pattern 说明恢复动作可以由外部事件触发，而不是只能由连续对话触发。
- golden evaluations 把长时间流程压缩成可测试对象，用于验证多步骤或多天流程。

### Key Concepts / 关键概念

- `Google ADK`: 摘要中的产品或框架名称；本测试不补充其版本、发布时间或可用范围。
- `long-running AI agents` / 长运行 AI agent: 可以经历等待、暂停、恢复、重启或外部事件的 agent 流程。
- `explicit workflow state` / 显式工作流状态: 将流程位置、状态和恢复所需信息表达为可管理状态，而不是只藏在聊天记录里。
- `persistent checkpoint/session state` / 持久化检查点或会话状态: 摘要中用于恢复流程的状态保存机制。
- `event-driven resume` / 事件驱动恢复: 外部事件触发 agent 继续 workflow 的模式。
- `webhooks` / Webhook: 摘要中给出的事件驱动恢复示例。
- `golden evaluations` / 黄金评测: 用固定预期结果测试多步骤或多天 agent flow 的评测方式。

### Assumptions / 假设

- 面向中文 AI 创作者、技术作者和团队成员表达，因此保留英文技术词并给出中文解释。
- 三种风格都只展示 first 3 sample cards / 前 3 张示例卡，不代表完整发布稿。
- “工作流可恢复性”“测试可复现性”等表述是基于摘要事实的编辑解释，不是原文额外声明。

### Boundaries / 边界

- 不宣称 Google ADK 的性能、价格、发布日期、可用区域、行业采用情况或具体 API 形态。
- 不宣称 Webhook 是唯一恢复方式；摘要只说它是一个示例。
- 不宣称 golden evaluations 覆盖所有失败场景；摘要只说它用于测试多步骤或多天流程而不必实时等待。
- 不把“显式状态更重要”写成“聊天历史完全无用”；摘要只说不要只依赖 chat history。

## Style 1: 小红书轻知识卡

### Style Profile / 风格配置

- Channel / 渠道: 小红书。
- Target audience / 目标读者: 入门到进阶的中文 AI 创作者、Agent 工具学习者。
- Density / 信息密度: 轻到中。
- Tone / 语气: 清楚、轻解释、不夸张。
- Card rhythm / 卡片节奏: 每张卡只讲一个概念，用短句建立“为什么重要”。
- Title strategy / 标题策略: 问题型、误区提醒型、结论型。
- Visual direction / 视觉方向: 大标题、短 bullet、简单流程箭头、状态标签；不使用卡通 mascot / 吉祥物。
- CTA style / 行动引导: 收藏、对照自己的 agent workflow 检查是否有显式状态。
- Evidence requirement / 证据要求: 关键 claim 附 evidence note / 证据说明，假设单独标明。
- Forbidden patterns / 禁用模式: “私藏神器”“效率翻倍”“一键搞定”“照抄就爆”。

### Content Brief / 内容简报

- 角度: 长运行 agent 的关键不是“聊得更久”，而是能把流程状态保存下来，等待之后还能接上。
- 卡片架构: 误区提醒 -> 核心概念 -> 简单机制。
- 内容目标: 让非深度开发读者理解 pause/resume 背后的状态管理思路。
- 需要验证的信息: Google ADK 的具体 API、产品可用性、版本、价格、真实案例。

### First 3 Sample Cards / 前 3 张示例卡

#### Card 1: Agent 想跑很久，不能只靠聊天记录

- 这张卡的任务: 用轻解释方式建立误区。
- 卡片正文: Google ADK 的这组摘要在讲 long-running AI agents / 长运行 AI agent：它们可能会暂停、等待、再恢复。重点不是让对话无限变长，而是要有 explicit workflow state / 显式工作流状态。
- 视觉建议: 左侧“只看 chat history”，右侧“workflow state + resume”，中间用箭头连接。
- Evidence notes / 证据说明: “pause and resume” 与 “explicit workflow state instead of relying only on chat history” 均来自受控摘要。

#### Card 2: 什么叫“显式状态”？

- 这张卡的任务: 把术语翻译成读者能理解的表达。
- 卡片正文: 简单说，就是 agent 要知道自己进行到哪一步、等什么、下一步如何继续。这些信息不只放在 chat history / 聊天历史里，而是作为 workflow state / 工作流状态被管理。
- 视觉建议: 三个状态标签：“当前步骤”“等待条件”“恢复入口”。
- Evidence notes / 证据说明: “不只依赖聊天历史”来自受控摘要；三个标签是编辑解释，用来帮助理解显式状态。

#### Card 3: 恢复靠什么？checkpoint/session state

- 这张卡的任务: 介绍恢复机制的核心词。
- 卡片正文: 摘要提到 persistent checkpoint/session state / 持久化检查点或会话状态。它让 agent 在等待、重启或外部事件后，还能继续之前的 workflow / 工作流。
- 视觉建议: “暂停 -> 保存状态 -> 等待/重启/外部事件 -> 恢复”的四步流程条。
- Evidence notes / 证据说明: checkpoint/session state 及三类恢复场景均来自受控摘要。

### Visual Direction / 视觉方向

- 画面轻量，使用流程箭头、状态标签和少量高亮词。
- 技术词保留英文，旁边配中文解释。
- 色彩建议以清爽信息卡为主，不使用夸张科技感背景，不加入卡通 mascot。

### Evidence Notes / 证据说明

- 所有功能性陈述只来自 controlled source summary。
- “当前步骤、等待条件、恢复入口”是编辑解释，用于解释 explicit workflow state，不作为原文事实。
- 不使用任何原文外的 Google ADK 资料。

### Claims Needing Verification / 待验证声明

- Google ADK 是否提供某个具体 API 名称或 SDK 写法。
- Google ADK 当前是否公开可用、支持哪些环境或版本。
- Webhook resume 的完整配置方式和限制。
- golden evaluations 的具体实现格式和覆盖范围。

## Style 2: 技术深读卡

### Style Profile / 风格配置

- Channel / 渠道: 公众号技术长文、技术社区、LinkedIn carousel。
- Target audience / 目标读者: 进阶 AI agent 开发者、技术内容作者、Agent Skill 作者。
- Density / 信息密度: 高。
- Tone / 语气: 理性、机制分析、克制。
- Card rhythm / 卡片节奏: 先给架构结论，再拆状态、恢复触发和评测问题。
- Title strategy / 标题策略: 机制型、对比型、边界型。
- Visual direction / 视觉方向: 架构图、状态机草图、对比表、证据边界框；不使用卡通 mascot。
- CTA style / 行动引导: 阅读原文或文档后复核 API 细节，设计一个最小可测 agent flow。
- Evidence requirement / 证据要求: 逐条区分 source-backed claim / 来源支撑声明与 editorial interpretation / 编辑解释。
- Forbidden patterns / 禁用模式: 趋势判断、性能承诺、无依据行业结论、过度简化限制。

### Content Brief / 内容简报

- 角度: 摘要呈现的是一种长运行 agent 的控制面设计：状态持久化、事件恢复、长流程评测。
- 卡片架构: 机制总览 -> 状态模型 -> 恢复模式。
- 内容目标: 帮助技术读者把“长运行 agent”从聊天体验问题转成 workflow state management / 工作流状态管理问题。
- 需要验证的信息: API 形态、状态存储边界、Webhook 安全模型、golden evaluation 工具链。

### First 3 Sample Cards / 前 3 张示例卡

#### Card 1: 长运行 Agent 的关键变量是 workflow state

- 这张卡的任务: 给出技术分析主张。
- 卡片正文: 受控摘要把 Google ADK 的 long-running AI agents 描述为可 pause/resume 的流程。它强调 explicit workflow state，而不是 relying only on chat history。这意味着问题域从“上下文还在不在”转向“流程状态是否可恢复、可持久化、可测试”。
- 视觉建议: 对比表：`Chat History` vs `Workflow State`，列出“信息形态、恢复能力、测试对象”。
- Evidence notes / 证据说明: 前两句来自受控摘要；“问题域转向”是基于摘要的编辑解释。

#### Card 2: checkpoint/session state 是恢复语义的基础

- 这张卡的任务: 拆解恢复机制。
- 卡片正文: 摘要提到 persistent checkpoint/session state，使 agent 能在 waiting / 等待、restart / 重启、external events / 外部事件之后恢复。这里的重点是 persistent / 持久化：恢复不能只依赖当前对话窗口的临时上下文。
- 视觉建议: 状态机草图：`Running -> Waiting -> Checkpointed -> Resumed`，旁边标注 restart 与 external event。
- Evidence notes / 证据说明: 三类恢复场景与 checkpoint/session state 来自受控摘要；状态机命名是解释性建模。

#### Card 3: event-driven resume 把 Agent 接入外部世界

- 这张卡的任务: 解释外部事件触发恢复。
- 卡片正文: 摘要描述 event-driven resume patterns，并给出 webhooks 作为例子。这说明 workflow continuation / 工作流继续可以由外部事件触发，而不是必须由用户在同一个 chat session 里继续输入。
- 视觉建议: 外部系统 -> Webhook -> Resume handler -> Agent workflow 的架构箭头图。
- Evidence notes / 证据说明: event-driven resume 与 webhook 示例来自受控摘要；“Resume handler”是抽象图示，不是摘要中的具体 API 名。

### Visual Direction / 视觉方向

- 使用深读型结构图：对比表、状态机、事件流图。
- 每张卡保留 evidence boundary / 证据边界角标，区分“来源事实”和“编辑解释”。
- 避免营销视觉和大字口号，强调可复核性。

### Evidence Notes / 证据说明

- 可直接支撑的 claims: pause/resume、explicit workflow state、persistent checkpoint/session state、event-driven resume、webhooks、golden evaluations。
- 编辑解释: “控制面设计”“状态机草图”“恢复语义”等是为技术读者建立模型，不代表原文逐字表述。
- 未使用 benchmark、性能、成本、采用率等外部声明。

### Claims Needing Verification / 待验证声明

- Google ADK 是否把 checkpoint 与 session state 作为不同 API 或同一抽象。
- Webhook resume 是否需要特定认证、安全配置或部署形态。
- golden evaluations 的具体断言方式、运行方式和与 CI / continuous integration 的关系。
- 多天流程测试是否有官方示例或限制条件。

## Style 3: 内部培训知识卡

### Style Profile / 风格配置

- Channel / 渠道: 内部 wiki、团队知识库、培训材料。
- Target audience / 目标读者: 准备设计或评估长运行 agent workflow 的产品、研发、测试团队。
- Density / 信息密度: 中到高。
- Tone / 语气: 直接、操作型、可执行。
- Card rhythm / 卡片节奏: 定义团队要检查的能力点，再给设计和测试清单。
- Title strategy / 标题策略: 任务型、风险提醒型、检查清单型。
- Visual direction / 视觉方向: SOP 卡、流程检查表、风险提示框、评测矩阵；不使用卡通 mascot。
- CTA style / 行动引导: 用同一套事实设计内部 review checklist，并标记需要查原文或文档的项目。
- Evidence requirement / 证据要求: 来源事实、团队假设、待验证事项分栏。
- Forbidden patterns / 禁用模式: 社媒语气、口号式培训、未经验证的落地承诺。

### Content Brief / 内容简报

- 角度: 团队培训应把这份摘要转成“设计长运行 agent 时必须检查的状态、恢复和评测问题”。
- 卡片架构: 设计检查 -> 恢复场景 -> 测试要求。
- 内容目标: 帮团队形成评估清单，而不是把摘要包装成产品宣传。
- 需要验证的信息: 原文完整上下文、Google ADK API、内部系统是否能接入 Webhook、评测环境是否支持 golden evaluations。

### First 3 Sample Cards / 前 3 张示例卡

#### Card 1: 培训目标：把长运行 Agent 当成 workflow 设计

- 这张卡的任务: 定义团队学习目标。
- 卡片正文: 本次材料只基于受控摘要。团队需要关注三个问题：agent 能否 pause/resume，状态是否以 explicit workflow state 管理，恢复是否依赖 persistent checkpoint/session state。
- 视觉建议: 培训首页卡，三项检查点横排：“暂停/恢复”“显式状态”“持久化状态”。
- Evidence notes / 证据说明: 三项检查点均来自受控摘要。

#### Card 2: 设计检查：不要只问 chat history 够不够

- 这张卡的任务: 转成团队设计 checklist。
- 卡片正文: 评审 long-running agent 方案时，至少记录：当前 workflow step / 工作流步骤、等待条件、恢复触发、checkpoint/session state 保存位置。最后一项需要查具体实现，不能从摘要直接推出。
- 视觉建议: Checklist 表格，列为“检查项 / 来源支持 / 需要补充材料”。
- Evidence notes / 证据说明: explicit workflow state 与 checkpoint/session state 来自受控摘要；“保存位置”是内部实现需要验证的问题。

#### Card 3: 恢复场景至少覆盖三类

- 这张卡的任务: 给团队测试用例方向。
- 卡片正文: 摘要明确提到三类恢复背景：waiting / 等待、restart / 重启、external events / 外部事件。内部测试设计可以先围绕这三类写 smoke cases / 冒烟用例，再检查是否需要 Webhook 触发。
- 视觉建议: 三列测试矩阵：“等待后恢复”“重启后恢复”“外部事件恢复”。
- Evidence notes / 证据说明: 三类恢复背景来自受控摘要；“smoke cases”是培训转化建议。

### Visual Direction / 视觉方向

- 使用培训页版式：标题短、检查项清楚、每页有“来源事实 / 待验证”标记。
- 以表格、流程检查、测试矩阵为主。
- 不做社媒化大字海报，不加入卡通 mascot。

### Evidence Notes / 证据说明

- 本风格把来源事实转成内部工作项，但不把工作项伪装成原文事实。
- “保存位置、内部系统接入、smoke cases”属于团队执行建议或待验证问题。
- 所有团队行动都应在阅读原文或官方文档后再落地。

### Claims Needing Verification / 待验证声明

- 团队使用的 Google ADK 版本是否支持摘要中提到的相关能力。
- checkpoint/session state 在团队架构中的存储位置、权限和生命周期。
- Webhook 接入是否符合团队安全要求。
- golden evaluations 是否能接入团队现有测试流程。

## What Changed Across Styles / 风格变化

- 小红书轻知识卡把同一事实转成“误区提醒 + 轻解释”，优先降低理解门槛。
- 技术深读卡把同一事实转成“机制模型 + 架构图 + 证据边界”，优先服务技术分析。
- 内部培训知识卡把同一事实转成“检查清单 + 测试矩阵 + 待验证项”，优先服务团队执行。
- 标题策略变化: 从问题型和轻结论，变成机制型，再变成任务型。
- 信息密度变化: 小红书轻到中，技术深读高，内部培训中到高。
- 视觉方向变化: 轻量信息卡 -> 架构/状态图 -> SOP/checklist/测试矩阵。
- CTA 变化: 收藏和自查 -> 复核原文并设计最小可测流程 -> 形成团队 review checklist。

## What Stayed Invariant / 不变内容

- 不变事实 1: Google ADK 摘要讨论 long-running AI agents 可以 pause and resume。
- 不变事实 2: 摘要强调 explicit workflow state，而不是只依赖 chat history。
- 不变事实 3: 摘要提到 persistent checkpoint/session state，用于等待、重启或外部事件后的恢复。
- 不变事实 4: 摘要描述 event-driven resume patterns，webhooks 是示例之一。
- 不变事实 5: 摘要提到 golden evaluations，用于测试多步骤或多天 agent flows，而不必实时等待。
- 不变边界: 三种风格都不声称已读全文，不补充性能、价格、可用性、行业采用或具体 API 细节。
- 不变证据规则: 编辑解释和团队建议必须标明，不得伪装成来源事实。

## Quality Check / 质量检查

- Source fidelity / 来源保真: 通过。所有核心事实均来自 controlled source summary，并明确标注未读全文。
- Evidence separation / 证据与假设分离: 通过。来源事实、编辑解释、团队建议和待验证声明分开呈现。
- Style fit / 风格匹配: 通过。三种风格在密度、语气、卡片节奏、视觉方向和 CTA 上明显不同。
- Platform fit / 平台适配: 通过。小红书版短、轻、易懂；技术深读版强调机制；内部培训版转成 checklist。
- Card sequence logic / 卡片顺序逻辑: 通过。每种风格的前三张卡均按“问题/核心概念/机制或执行”递进。
- Technical accuracy / 技术准确性: 通过。关键技术词 bilingual / 中英双语保留，没有引入未验证 API 名称。
- Visual production usefulness / 视觉制作可用性: 通过。视觉建议服务信息结构，且没有添加 cartoon mascots / 卡通吉祥物。
- Anti-slop checks / 反 AI 味检查: 通过。没有使用夸张承诺、爆款模板或 prompt-library phrasing。
- Decision / 判断: 可用于判断 style system 是否能从同一来源事实生成三种不同卡片产品。

## Limitations of this test / 本测试的局限

- 这是 Level 1 controlled-source smoke test，只验证风格渲染和来源边界控制，不验证原文抽取质量。
- 来源只有五条摘要事实，信息量有限；不能评估复杂文章结构、引用链或段落级证据提取能力。
- 本测试没有联网，也没有核验 Google ADK 官方文档或原文，因此所有易变或具体实现声明都必须保留为待验证。
- 本测试只展示每种风格的 first 3 sample cards，不评估完整卡片套组的发布节奏、封面标题或长尾 CTA。
- 本测试刻意不加入 cartoon mascots，只检查正常 visual direction 是否能随风格变化。

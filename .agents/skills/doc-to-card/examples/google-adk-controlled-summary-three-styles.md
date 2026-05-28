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
- Visual direction / 视觉方向: 大标题、短 bullet、简单流程箭头、状态标签；可选 character-pair / 双角色母题。
- Visual motif / 视觉母题: optional character-pair，小机器人 + 小狐狸。小机器人代表 agent，小狐狸代表创作者提问者；保持原创，不模仿任何现有 IP。
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
- Layout Brief / 版式说明: 竖版 4:5。顶部大标题占 25%，中间做左右对比，底部放一句小提示“状态要能被恢复”。小机器人站在 workflow state 一侧，小狐狸在中间提问。
- Visual Elements / 视觉元素: 左侧聊天气泡堆叠、右侧状态卡片、箭头、两个原创小角色、浅色背景、蓝绿高亮。
- Image Prompt / 生图提示词: 生成一张中文小红书轻知识卡背景插画，4:5 竖版，清爽信息卡风格，左右对比构图，左侧是简化聊天气泡，右侧是 workflow state 状态卡片和 resume 箭头，中间有原创小机器人和小狐狸作为轻量引导角色，现代扁平插画，蓝绿配色，留出清晰文字排版区域，文字由后期设计工具添加。
- Negative Prompt / Avoid: 不要真实 Google 品牌元素，不要现有 IP 角色，不要复杂代码截图，不要生成小字，不要夸张科幻背景，不要让角色占满画面。
- Text Readability Notes / 文字可读性提醒: 标题不超过 16 个汉字；英文术语用标签样式单独排版；正文最多 3 行，确保移动端可读。
- Evidence notes / 证据说明: “pause and resume” 与 “explicit workflow state instead of relying only on chat history” 均来自受控摘要。

#### Card 2: 什么叫“显式状态”？

- 这张卡的任务: 把术语翻译成读者能理解的表达。
- 卡片正文: 简单说，就是 agent 要知道自己进行到哪一步、等什么、下一步如何继续。这些信息不只放在 chat history / 聊天历史里，而是作为 workflow state / 工作流状态被管理。
- 视觉建议: 三个状态标签：“当前步骤”“等待条件”“恢复入口”。
- Layout Brief / 版式说明: 顶部问题标题，中间三枚状态标签横向排列，底部放一句解释。小狐狸指向三个标签，小机器人在右侧拿着状态卡。
- Visual Elements / 视觉元素: 三个圆角状态标签、轻量箭头、原创小机器人、小狐狸、浅色分区卡片。
- Image Prompt / 生图提示词: 4:5 竖版知识卡插画，中心是三个大号状态标签占位：当前步骤、等待条件、恢复入口，原创小狐狸做提问姿态，原创小机器人举着一张状态卡，轻量扁平风格，干净留白，柔和蓝绿和橙色点缀，适合后期添加中文文字。
- Negative Prompt / Avoid: 不要儿童绘本风，不要过度可爱，不要真实软件界面，不要密集文字，不要品牌 logo，不要模仿任何动画角色。
- Text Readability Notes / 文字可读性提醒: 三个状态标签必须大于正文层级；英文 `workflow state` 放小号注释，不与主标题抢层级。
- Evidence notes / 证据说明: “不只依赖聊天历史”来自受控摘要；三个标签是编辑解释，用来帮助理解显式状态。

#### Card 3: 恢复靠什么？checkpoint/session state

- 这张卡的任务: 介绍恢复机制的核心词。
- 卡片正文: 摘要提到 persistent checkpoint/session state / 持久化检查点或会话状态。它让 agent 在等待、重启或外部事件后，还能继续之前的 workflow / 工作流。
- 视觉建议: “暂停 -> 保存状态 -> 等待/重启/外部事件 -> 恢复”的四步流程条。
- Layout Brief / 版式说明: 顶部标题，主体是四步横向流程条，底部用小字解释 checkpoint/session state。两个角色只出现在流程条下方作为辅助，不干扰步骤。
- Visual Elements / 视觉元素: 四个步骤节点、保存图标、恢复箭头、小机器人状态灯、小狐狸检查清单、浅色背景。
- Image Prompt / 生图提示词: 生成一张轻知识流程卡插画，4:5 竖版，四步流程条从左到右：pause、save state、wait/restart/event、resume，用图标表达暂停、保存、等待和恢复，原创小机器人与小狐狸在底部轻量互动，现代信息图风格，留出大标题和正文区域，文字后期排版。
- Negative Prompt / Avoid: 不要代码墙，不要真实产品 UI，不要复杂技术架构图，不要让角色遮挡流程，不要生成难读小字。
- Text Readability Notes / 文字可读性提醒: 流程节点文字尽量 2-4 个字；英文术语可放节点下小标签；箭头必须清晰。
- Evidence notes / 证据说明: checkpoint/session state 及三类恢复场景均来自受控摘要。

### Visual Direction / 视觉方向

- 画面轻量，使用流程箭头、状态标签和少量高亮词。
- 技术词保留英文，旁边配中文解释。
- 色彩建议以清爽信息卡为主，不使用夸张科技感背景。可选小机器人 + 小狐狸作为原创双角色，但只能做轻量导视。

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
- Visual motif / 视觉母题: icon-only 或 architecture diagrams / 架构图。使用状态、事件、检查点等抽象图标，不使用角色。
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
- Layout Brief / 版式说明: 宽屏或 4:5 均可。顶部放结论型标题，中间是两列表格，底部放 evidence boundary / 证据边界条。
- Visual Elements / 视觉元素: 两列表格、状态节点图标、恢复箭头、证据边界角标、深色细线和浅底。
- Image Prompt / 生图提示词: 生成一张技术深读信息图背景，干净专业，中心为两列对比表布局，左列代表 chat history，右列代表 workflow state，加入抽象状态节点、恢复箭头和证据边界标签区域，蓝灰色技术文档风格，无人物无吉祥物，留出清晰中文文字排版空间，文字由后期设计工具添加。
- Negative Prompt / Avoid: 不要卡通角色，不要真实 Google logo，不要真实代码截图，不要密集小字，不要赛博朋克背景，不要夸张发光效果。
- Text Readability Notes / 文字可读性提醒: 表格每格不超过 12 个汉字；英文术语使用等宽标签；证据边界条放底部且字号不低于正文 70%。
- Evidence notes / 证据说明: 前两句来自受控摘要；“问题域转向”是基于摘要的编辑解释。

#### Card 2: checkpoint/session state 是恢复语义的基础

- 这张卡的任务: 拆解恢复机制。
- 卡片正文: 摘要提到 persistent checkpoint/session state，使 agent 能在 waiting / 等待、restart / 重启、external events / 外部事件之后恢复。这里的重点是 persistent / 持久化：恢复不能只依赖当前对话窗口的临时上下文。
- 视觉建议: 状态机草图：`Running -> Waiting -> Checkpointed -> Resumed`，旁边标注 restart 与 external event。
- Layout Brief / 版式说明: 主体使用状态机横向流程，右侧放外部事件和重启的辅助入口，底部放“persistent”强调条。
- Visual Elements / 视觉元素: 状态节点、箭头、checkpoint 数据库图标、restart 图标、external event 图标。
- Image Prompt / 生图提示词: 生成一张专业技术架构图风格卡片，浅灰背景，横向状态机流程：running、waiting、checkpointed、resumed，用抽象节点和箭头表达，旁边有 restart 和 external event 的小图标入口，整体像技术白皮书插图，无角色，预留标题和说明文字区域。
- Negative Prompt / Avoid: 不要拟人化机器人，不要复杂云厂商图标，不要真实产品界面，不要随机英文小字，不要高饱和霓虹色。
- Text Readability Notes / 文字可读性提醒: 状态节点可用英文短词，但正文解释用中文；箭头和节点间距要足够，避免状态机挤压。
- Evidence notes / 证据说明: 三类恢复场景与 checkpoint/session state 来自受控摘要；状态机命名是解释性建模。

#### Card 3: event-driven resume 把 Agent 接入外部世界

- 这张卡的任务: 解释外部事件触发恢复。
- 卡片正文: 摘要描述 event-driven resume patterns，并给出 webhooks 作为例子。这说明 workflow continuation / 工作流继续可以由外部事件触发，而不是必须由用户在同一个 chat session 里继续输入。
- 视觉建议: 外部系统 -> Webhook -> Resume handler -> Agent workflow 的架构箭头图。
- Layout Brief / 版式说明: 中心是从左到右的架构箭头图，四个模块等宽排列；底部放“Webhook 是示例，不是唯一方式”的边界提醒。
- Visual Elements / 视觉元素: 外部系统图标、Webhook 入口、resume handler 抽象模块、agent workflow 流程块、边界提醒框。
- Image Prompt / 生图提示词: 生成一张技术架构卡片背景，左到右四段模块：external system、webhook、resume handler、agent workflow，使用简洁线框图标和箭头，底部有 boundary note 区域，蓝灰配色，信息图风格，无人物无吉祥物，适合后期添加中文标题和说明。
- Negative Prompt / Avoid: 不要真实 webhook 服务 logo，不要具体 API 代码，不要品牌标识，不要角色插画，不要生成不可读的小文字。
- Text Readability Notes / 文字可读性提醒: 模块名可用英文，中文解释放卡片正文；边界提醒必须可见，避免读者误解 Webhook 是唯一方式。
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
- Visual motif / 视觉母题: none 或 process icons / 流程图标。不要 mascot，不要社媒化角色。
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
- Layout Brief / 版式说明: 16:9 或 wiki 宽屏版式。顶部是培训目标标题，中间三项检查点横排，底部放“仅基于受控摘要”的来源边界。
- Visual Elements / 视觉元素: 三个 checklist 模块、流程图标、来源边界条、低饱和蓝灰色块。
- Image Prompt / 生图提示词: 生成一张内部培训知识卡背景，16:9 宽屏，专业 SOP 风格，中间三项检查点卡片横排，分别用暂停恢复图标、状态图标、持久化存储图标表达，底部预留来源边界提示区，蓝灰低饱和配色，无人物无吉祥物，文字后期排版。
- Negative Prompt / Avoid: 不要小红书风格，不要卡通角色，不要营销海报，不要真实 Google logo，不要密集小字，不要花哨渐变。
- Text Readability Notes / 文字可读性提醒: 适合投影或 wiki 阅读；每个检查点标题不超过 8 个汉字；边界说明不能太小。
- Evidence notes / 证据说明: 三项检查点均来自受控摘要。

#### Card 2: 设计检查：不要只问 chat history 够不够

- 这张卡的任务: 转成团队设计 checklist。
- 卡片正文: 评审 long-running agent 方案时，至少记录：当前 workflow step / 工作流步骤、等待条件、恢复触发、checkpoint/session state 保存位置。最后一项需要查具体实现，不能从摘要直接推出。
- 视觉建议: Checklist 表格，列为“检查项 / 来源支持 / 需要补充材料”。
- Layout Brief / 版式说明: 表格占主体 70%，顶部短标题，右侧或底部放风险提示框“保存位置需要查实现”。无角色。
- Visual Elements / 视觉元素: 三列表格、勾选框、风险提示图标、待验证标签。
- Image Prompt / 生图提示词: 生成一张团队知识库 checklist 卡片背景，16:9 宽屏，主体是三列表格结构：检查项、来源支持、需要补充材料，带简洁勾选框和风险提示框，专业内部文档风格，蓝灰配色，无角色无吉祥物，留出清晰文字排版区域。
- Negative Prompt / Avoid: 不要社媒贴纸，不要可爱动物，不要复杂插画背景，不要真实软件 UI，不要生成具体小字。
- Text Readability Notes / 文字可读性提醒: 表格列名必须清楚；每个单元格控制在一行或两行；待验证标签用醒目但不刺眼的颜色。
- Evidence notes / 证据说明: explicit workflow state 与 checkpoint/session state 来自受控摘要；“保存位置”是内部实现需要验证的问题。

#### Card 3: 恢复场景至少覆盖三类

- 这张卡的任务: 给团队测试用例方向。
- 卡片正文: 摘要明确提到三类恢复背景：waiting / 等待、restart / 重启、external events / 外部事件。内部测试设计可以先围绕这三类写 smoke cases / 冒烟用例，再检查是否需要 Webhook 触发。
- 视觉建议: 三列测试矩阵：“等待后恢复”“重启后恢复”“外部事件恢复”。
- Layout Brief / 版式说明: 主体是三列测试矩阵，每列包含场景、触发条件、预期观察。底部放 Webhook 是事件示例的提醒。
- Visual Elements / 视觉元素: 三列矩阵、等待图标、重启图标、事件图标、Webhook 小标签、边界提醒框。
- Image Prompt / 生图提示词: 生成一张内部测试矩阵卡片背景，16:9 宽屏，三列矩阵布局，列主题分别为等待后恢复、重启后恢复、外部事件恢复，用简洁流程图标表示，底部有 webhook 只是示例的边界提示区域，专业培训材料风格，无人物无吉祥物，低饱和蓝灰配色。
- Negative Prompt / Avoid: 不要卡通 mascot，不要社交媒体封面风，不要真实品牌 logo，不要代码截图，不要自动生成小字。
- Text Readability Notes / 文字可读性提醒: 三列宽度保持一致；每列最多 3 个短句；Webhook 边界提醒要与正文区分。
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
- Visual production usefulness / 视觉制作可用性: 通过。每张示例卡都包含 Layout Brief、Visual Elements、Image Prompt、Negative Prompt 和 Text Readability Notes；角色母题只用于小红书轻知识卡，技术深读和内部培训不使用 mascot。
- Anti-slop checks / 反 AI 味检查: 通过。没有使用夸张承诺、爆款模板或 prompt-library phrasing。
- Decision / 判断: 可用于判断 style system 是否能从同一来源事实生成三种不同卡片产品。

## Limitations of this test / 本测试的局限

- 这是 Level 1 controlled-source smoke test，只验证风格渲染和来源边界控制，不验证原文抽取质量。
- 来源只有五条摘要事实，信息量有限；不能评估复杂文章结构、引用链或段落级证据提取能力。
- 本测试没有联网，也没有核验 Google ADK 官方文档或原文，因此所有易变或具体实现声明都必须保留为待验证。
- 本测试只展示每种风格的 first 3 sample cards，不评估完整卡片套组的发布节奏、封面标题或长尾 CTA。
- 本测试只在小红书轻知识卡中使用 optional character-pair motif / 可选双角色母题；技术深读和内部培训保持 icon-only、architecture diagrams 或 checklist/process visuals。

## Why this is not direct image generation / 为什么这还不是直接出图

- `doc-to-card` 在这个阶段输出 production-ready image briefs / 可生产图片简报和 image prompts / 生图提示词。
- 实际图片生成仍需要单独的 rendering or image generation step / 渲染或生图步骤，例如图像生成工具、Canva/Figma 设计、HTML/CSS 渲染或 PPTX 制作。
- 本示例中的 Image Prompt 只描述画面结构、视觉风格、图标或角色母题，不代表已经生成图片文件。
- 对需要精确中文文字的卡片，应在设计或渲染阶段单独排版文字，不依赖图像模型生成小字。
- Future versions may add HTML/SVG/PPTX rendering or integration with image generation tools, but this smoke test intentionally stays as a documentation-first production brief.

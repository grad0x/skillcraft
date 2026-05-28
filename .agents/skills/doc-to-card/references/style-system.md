# Style System

这个文件定义 `doc-to-card` 的可复用风格维度。风格只改变表达方式、信息密度、视觉方向和行动引导，不能改变 source facts / 来源事实和 evidence boundaries / 证据边界。

## 风格维度 / Style Dimensions

| 维度 | 说明 | 常见选项 |
| --- | --- | --- |
| channel / 渠道 | 内容发布或使用场景。 | 小红书、公众号、LinkedIn carousel、内部 wiki、幻灯片 |
| audience sophistication / 读者成熟度 | 读者对主题的熟悉程度。 | 入门、进阶、专业、团队内部 |
| content density / 信息密度 | 单张卡承载的信息量。 | 轻、中、高 |
| tone / 语气 | 读者感受到的表达方式。 | 轻解释、理性、技术深读、培训、极简 |
| visual style / 视觉风格 | 设计和排版方向。 | 信息卡、流程图、对比表、极简海报、培训页 |
| title strategy / 标题策略 | 卡片标题如何承担信息动作。 | 问题型、结论型、对比型、步骤型、风险提醒型 |
| evidence level / 证据要求 | 每个 claim 需要多强的来源说明。 | 简要来源、逐条证据、假设分离、待验证列表 |
| technical depth / 技术深度 | 技术细节展开程度。 | 低、中、高 |
| CTA style / 行动引导 | 读者下一步动作。 | 收藏、练习、评论反馈、团队执行、继续阅读 |
| avoid list / 禁用表达 | 明确不要出现的套路。 | 夸大承诺、伪案例、无来源数字、万能提示词话术 |

## 初始风格预设 / Initial Style Presets

### 小红书轻知识卡

- channel / 渠道: 小红书
- audience sophistication / 读者成熟度: 入门到进阶创作者
- content density / 信息密度: 轻到中
- tone / 语气: 清楚、轻解释、不油腻
- visual style / 视觉风格: 大标题、短段落、图标化提示、流程小图
- title strategy / 标题策略: 问题型、结论型、误区提醒型
- evidence level / 证据要求: 关键 claim 有来源说明，假设单独列出
- technical depth / 技术深度: 中低，保留必要英文技术词
- CTA style / 行动引导: 收藏、试一次、评论一个使用场景
- avoid list / 禁用表达: “私藏神器”“一键封神”“效率翻 10 倍”“照抄就爆”

### 技术深读卡

- channel / 渠道: 公众号、技术社区、LinkedIn carousel
- audience sophistication / 读者成熟度: 进阶创作者、开发者、技术作者
- content density / 信息密度: 高
- tone / 语气: 理性、分析型、克制
- visual style / 视觉风格: 架构图、流程图、对比表、引用框
- title strategy / 标题策略: 结论型、机制型、对比型
- evidence level / 证据要求: 逐条 source-backed claims / 来源支撑声明
- technical depth / 技术深度: 高
- CTA style / 行动引导: 阅读原文、复现实验、提交 issue 或反馈
- avoid list / 禁用表达: 浅层鸡汤、无依据趋势判断、过度简化技术限制

### 公众号解释型卡片

- channel / 渠道: 公众号文章内卡片、长文图文
- audience sophistication / 读者成熟度: 入门到进阶读者
- content density / 信息密度: 中
- tone / 语气: 解释型、稳、递进
- visual style / 视觉风格: 段落卡、概念卡、步骤卡
- title strategy / 标题策略: 问题型、步骤型、总结型
- evidence level / 证据要求: 每个 section 至少有来源或假设说明
- technical depth / 技术深度: 中
- CTA style / 行动引导: 继续阅读、保存 checklist、尝试一个案例
- avoid list / 禁用表达: 标题党、无意义排比、过长口号

### 内部培训知识卡

- channel / 渠道: 内部 wiki、团队知识库、培训材料
- audience sophistication / 读者成熟度: 团队成员，水平不一
- content density / 信息密度: 中到高
- tone / 语气: 直接、操作型、可执行
- visual style / 视觉风格: SOP 卡、流程图、检查清单、风险提示
- title strategy / 标题策略: 步骤型、风险提醒型、任务型
- evidence level / 证据要求: 明确哪些来自来源、哪些是团队假设
- technical depth / 技术深度: 按团队角色调整
- CTA style / 行动引导: 按步骤执行、提交产物、记录问题
- avoid list / 禁用表达: 营销语、社媒口吻、无法执行的抽象建议

### 高端极简知识海报

- channel / 渠道: 品牌化海报、分享封面、演示页
- audience sophistication / 读者成熟度: 进阶读者或决策者
- content density / 信息密度: 低到中
- tone / 语气: 克制、精确、有留白
- visual style / 视觉风格: 极简标题、少量关键词、强结构留白
- title strategy / 标题策略: 结论型、对比型、概念型
- evidence level / 证据要求: 不在海报内堆证据，但交付中必须附来源说明
- technical depth / 技术深度: 中，避免堆术语
- CTA style / 行动引导: 阅读详情、进入下一页、查看来源
- avoid list / 禁用表达: 花哨装饰、过密正文、虚假高级感、无来源金句

## 使用规则 / Usage Rules

- 如果用户给了喜欢或不喜欢的风格样例，先抽象成 style dimensions，不要直接模仿受版权保护的表达。
- 如果渠道和读者冲突，优先满足读者理解，再调整渠道形式。
- 如果 style preset 与来源事实冲突，修改风格，不修改事实。
- 每次输出都要列出 forbidden patterns / 禁用模式，避免滑向通用提示词库。

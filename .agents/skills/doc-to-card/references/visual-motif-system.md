# Visual Motif System

这个文件定义 `doc-to-card` 的 visual motif / 视觉母题规则。视觉母题可以帮助记忆、建立系列感或降低阅读门槛，但不能改变 source facts / 来源事实，也不能压过信息层级。

## 总原则 / Core Rules

- 不模仿现有 IP、品牌角色、动漫角色、游戏角色、名人或受版权保护 mascot。
- 不让角色占据主信息层级；标题、关键概念和证据边界始终优先。
- 不把技术内容做得幼稚，除非用户明确要求儿童向或低龄科普风格。
- 一个系列内保持角色外观一致，包括造型、比例、颜色、姿态风格和表情范围。
- 角色只能表达情绪、流程位置或注意力引导，不能承担未经来源支持的事实声明。
- 如果用户没有明确要求角色，默认选择 `none / 无角色` 或 `icon-only / 图标辅助`。

## Motif Types / 母题类型

### none / 无角色

- When to use / 何时使用: 技术深读、内部培训、高端极简、严肃来源、证据要求高的内容。
- When not to use / 不适用: 需要强记忆点、轻知识传播或用户明确要求角色辅助时。
- Required user inputs / 所需输入: 无。
- Default behavior by platform / 平台默认: 技术深读卡、内部 wiki、高端极简知识海报默认使用。
- Risk controls / 风险控制: 用图标、流程图、表格和留白替代装饰角色。

### icon-only / 图标辅助

- When to use / 何时使用: 需要轻量视觉提示，但不需要角色叙事。
- When not to use / 不适用: 用户要求强人格化角色或故事场景时。
- Required user inputs / 所需输入: 图标风格、线性或面性、颜色方向。
- Default behavior by platform / 平台默认: 公众号解释型卡片、技术深读卡、内部培训知识卡常用。
- Risk controls / 风险控制: 图标含义必须服务卡片任务，不堆无关科技图形。

### mascot / 单一吉祥物

- When to use / 何时使用: 小红书轻知识卡、系列栏目、面向入门读者的友好解释。
- When not to use / 不适用: 严肃技术深读、内部制度、法律金融医疗等高风险内容。
- Required user inputs / 所需输入: 角色主体、外观关键词、颜色、性格、禁止模仿对象。
- Default behavior by platform / 平台默认: 小红书可选，其他平台默认不用。
- Risk controls / 风险控制: mascot 只能做辅助引导，不出现在每张卡的视觉中心；保持原创，不贴近任何现有 IP。

### character-pair / 双角色

- When to use / 何时使用: 需要表达对比、提问与回答、旧方式与新方式、用户与 agent 协作。
- When not to use / 不适用: 高信息密度技术卡、内部 checklist、极简海报。
- Required user inputs / 所需输入: 两个角色主体、关系设定、视觉比例、每个角色承担的叙事功能。
- Default behavior by platform / 平台默认: 小红书轻知识卡可选；技术深读和内部培训默认不用。
- Risk controls / 风险控制: 双角色不能变成漫画剧情，必须围绕卡片知识点；每张卡最多出现一个轻量互动。

### scene-character / 场景人物

- When to use / 何时使用: 需要展示工作场景，例如创作者看文档、团队 review、开发者检查流程。
- When not to use / 不适用: 用户要求严格信息图、无人物极简、或来源涉及敏感个人场景。
- Required user inputs / 所需输入: 场景、人物抽象程度、职业或角色、动作、是否允许真实人像感。
- Default behavior by platform / 平台默认: 幻灯片和公众号可少量使用；小红书可用于封面；内部 wiki 谨慎使用。
- Risk controls / 风险控制: 避免真实名人脸、公司工牌、真实品牌标识和可识别个人信息。

## Supported Motif Subjects / 支持的母题主体

- 小机器人: 适合 AI agent、自动化、流程提示；避免像现有品牌机器人。
- 小狐狸: 适合聪明、轻巧、提醒误区；避免拟人过强或幼稚化。
- 猫头鹰: 适合学习、知识、深读；避免学院派陈词滥调。
- 水獭: 适合协作、流程、轻松解释；避免过度可爱抢信息。
- 抽象人物: 适合职场、团队、内部培训；可保持低风险和通用性。
- 自定义角色: 需要用户提供原创设定、参考边界和禁用模仿对象。

## Platform Defaults / 平台默认建议

- 小红书: `icon-only` 默认；如果用户需要记忆点，可选 `mascot` 或 `character-pair`。
- 公众号: `icon-only` 或 subtle motif / 轻量母题；不建议每张卡都放角色。
- LinkedIn carousel: `none` 或 `icon-only`；面向国际技术读者时避免可爱角色。
- 内部 wiki / 团队知识库: `none` 或 process icons / 流程图标。
- 幻灯片 / 分享材料: `none`、`icon-only` 或少量 `scene-character`。

## Prompting Rules / 提示词规则

- 在 image prompt 中写“original character design / 原创角色设计”，不要写任何现有 IP 名。
- 对角色外观使用通用描述，例如“小型圆润白色机器人，蓝色状态灯”，不要描述成某个品牌风格。
- 保持角色一致时，复用同一组特征：主体、颜色、比例、表情范围、配件。
- 如果卡片依赖精确文字，让 image prompt 只生成背景和插画，文字由设计工具单独排版。

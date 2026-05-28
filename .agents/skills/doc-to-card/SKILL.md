---
name: doc-to-card
description: Convert source documents, articles, tutorials, notes, or tool documentation into structured educational card content for Chinese AI creators, technical writers, and bilingual developer audiences. Use when a user wants to transform dense material into publishable multi-card posts, carousel drafts, WeChat sections, 小红书 notes, or internal knowledge cards while preserving evidence and avoiding prompt-library style shortcuts.
---

# Doc To Card

默认用中文输出，除非用户明确要求英文。保留必要英文技术词，并在第一次出现时给出中文解释。目标用户包括中文 AI 创作者、技术内容作者、AI 工具学习者和 Skill 作者。

核心原则：同一份来源材料可以生成不同风格的卡片产品，但来源事实和证据边界不能被风格改变。先做 Source Understanding Layer / 来源理解层，再做 Style Rendering Layer / 风格表达层，最后做 Card Production Layer / 卡片生产层。

重要边界：这个 Skill 不直接生成图片文件。它产出 structured image briefs / 结构化图片生产简报和 image prompts / 生图提示词，可供外部 image generation tools、Canva/Figma 或后续 HTML/CSS rendering 使用。

## 资源导航 / Resources

按需读取这些资源，不要一次性把所有内容塞进输出：

- `references/style-system.md`: 风格维度、初始 style presets / 风格预设、禁用表达。
- `references/card-architectures.md`: 可复用 card sequence patterns / 卡片顺序模式。
- `references/platform-profiles.md`: 小红书、公众号、LinkedIn carousel、内部 wiki、幻灯片的平台适配说明。
- `references/visual-motif-system.md`: 角色、图标和视觉母题的使用规则与风险控制。
- `templates/style-profile.template.md`: 让用户或 Agent 明确风格参数。
- `templates/content-brief.template.md`: 来源理解层的结构化简报。
- `templates/card-output.template.md`: 最终卡片产物的输出契约。
- `templates/image-brief.template.md`: 面向设计工具或生图工具的图片生产简报。
- `examples/same-source-three-styles.md`: 同一虚构来源生成三种风格的示例。
- `examples/google-adk-controlled-summary-three-styles.md`: 受控摘要 smoke test，包含三种风格和图片生产提示。
- `evals/doc-to-card-quality-checklist.md`: 来源保真、风格匹配、反 AI 味等质量检查。

## 什么时候使用 / When To Use

当用户提供一段来源材料，并希望把它转成卡片式、可发布、可复核的教育内容时，使用这个 Skill。

适合：

- 把 AI 工具文档、产品更新、教程或技术文章转成小红书卡片、公众号段落、LinkedIn carousel、内部知识卡或分享材料。
- 同一份来源材料需要生成不同 style profiles / 风格配置，例如轻知识卡、技术深读卡、内部培训卡。
- 把复杂说明拆成“问题、概念、步骤、例子、注意事项、行动建议”。
- 需要中文表达，但仍要保留英文工具名、API 名、模型名或命令名的准确性。

不适合：没有来源材料的情绪化内容、纯营销标题、泛泛的爆款模板、只需要润色一句文案的任务。

## 输入要求 / Inputs

尽量从用户请求中提取；缺失会影响事实准确性时要追问。

- 来源材料：粘贴文本、文件路径、用户摘录、笔记或明确摘要。
- 目标读者：中文 AI 创作者、技术内容作者、AI 工具学习者、开发者、团队成员等。
- 发布渠道：小红书、公众号、LinkedIn carousel、内部 wiki、幻灯片等。
- 内容目标：教学、总结、对比、发布、入门、复盘、转化。
- 风格要求：card count / 卡片数量、density / 信息密度、tone / 语气、visual direction / 视觉方向、title strategy / 标题策略、CTA style / 行动引导。
- 生产要求：layout brief / 版式说明、visual elements / 视觉元素、image prompt / 生图提示词、negative prompt / 避免项、text readability notes / 文字可读性提醒。
- 视觉母题：none / 无角色、icon-only / 图标辅助、mascot / 单一吉祥物、character-pair / 双角色、scene-character / 场景人物，或用户自定义角色。
- 证据要求：是否需要 source-backed claims / 来源支撑声明、assumptions / 假设列表、claims needing verification / 待验证声明。
- 禁用表达：用户不想要的标题套路、视觉风格、语气、过度营销或“AI 味”表达。

如果用户没有给风格参数，先根据渠道和目标读者选择一个 style preset，并在输出中标明假设。可读取 `references/style-system.md`。

## 三层工作流 / Three-Layer Workflow

### 1. 来源理解层 / Source Understanding Layer

这一层只处理来源材料，不考虑“写得像哪个平台”。产物是 content brief / 内容简报。

必须提取：

- source facts / 来源事实：来源明确支持的事实。
- source logic / 来源逻辑：材料的论证、步骤或因果链。
- key concepts / 关键概念：读者必须理解的术语、机制或流程。
- assumptions / 假设：为了面向目标读者表达而补充的前提。
- claims needing verification / 需要验证的声明：产品能力、价格、模型、发布时间、政策等易变信息。
- boundaries / 边界：来源没有覆盖、不能推断或不能宣称的内容。

执行要求：

1. 建立来源契约，标明来源类型、标题或产品名、日期信息和可信度。
2. 区分 source facts、editorial interpretation / 编辑解释和 assumptions。
3. 提取可复用内容主干：问题、概念、步骤、例子、限制和读者下一步。
4. 删除重复铺垫、营销空话和无法从来源推出的结论。
5. 对当前产品能力、价格、模型、政策等易变信息标记“需要验证”。

### 2. 风格表达层 / Style Rendering Layer

这一层在不改变来源事实和证据边界的前提下，把 content brief 渲染成具体卡片产品。

必须确定：

- platform / 平台：小红书、公众号、LinkedIn carousel、内部 wiki、幻灯片等。
- target audience / 目标读者：新手、进阶创作者、开发者、团队成员、Skill 作者等。
- content density / 信息密度：轻、中、高。
- tone / 语气：轻解释、理性、技术深读、培训、极简等。
- card rhythm / 卡片节奏：每张卡的信息量和递进方式。
- title strategy / 标题策略：问题型、结论型、对比型、步骤型、风险提醒型。
- visual direction / 视觉方向：信息卡、流程图、对比表、极简海报、培训页等。
- CTA style / 行动引导：收藏、练习、评论反馈、团队执行、下一步阅读。
- forbidden patterns / 禁用模式：夸张承诺、伪案例、无来源数字、泛 prompt-library 话术。

执行要求：

1. 读取或生成 style profile。需要细节时使用 `templates/style-profile.template.md`。
2. 按内容类型选择 card architecture。需要模式时读取 `references/card-architectures.md`。
3. 按渠道调整平台表达。需要平台细节时读取 `references/platform-profiles.md`。
4. 起草卡片：每张卡只承担一个任务，标题和正文服务同一个信息动作。
5. 添加 visual direction、evidence note、caption 和 CTA。
6. 用 `evals/doc-to-card-quality-checklist.md` 做质量检查。

### 3. 卡片生产层 / Card Production Layer

这一层把每张卡从“内容草稿”转成可交给设计工具、图像生成工具或后续渲染系统的 production brief / 生产简报。

必须为每张卡输出：

- Content Copy / 内容文案：卡片上实际出现的标题、正文、标签、CTA。
- Layout Brief / 版式说明：画面结构、信息层级、留白、对齐、模块位置。
- Visual Elements / 视觉元素：图标、流程箭头、表格、状态标签、背景元素、可选角色。
- Image Prompt / 生图提示词：可用于 image generation tools 的视觉描述；不要把完整长文都塞进提示词。
- Text Safety Notes / 文字安全与可读性提醒：字号、对比度、文字长度、不要让图像模型生成小字。
- Optional Visual Motif / 可选视觉母题：是否使用角色、图标或场景人物；需要时读取 `references/visual-motif-system.md`。

执行要求：

1. 先确认 visual motif setting / 视觉母题设置。没有用户要求时，按 style preset 默认值选择。
2. 每张卡的 image prompt 只描述视觉构图和风格，不新增来源外事实。
3. 技术内容优先保证信息层级清楚；角色、装饰和背景不能抢主信息。
4. 对需要精确文字的卡片，提示外部工具“文字由设计阶段排版，不由图像模型生成”。
5. 输出 negative prompt / avoid，排除品牌仿冒、IP 模仿、夸张科技感、低可读小字、无关角色等。
6. 明确说明：本 Skill 不直接生成图片文件。

## 输出格式 / Output Format

默认按下面结构输出 Markdown。需要更完整模板时读取 `templates/content-brief.template.md` 和 `templates/card-output.template.md`。

```markdown
## 内容简报 / Content Brief

- 来源:
- 目标读者:
- 发布渠道:
- 内容目标:
- 选用风格:
- 选用卡片架构:
- 需要验证的信息:

## 来源理解层 / Source Understanding Layer

### Source Facts / 来源事实

- <来源明确支持的事实>

### Source Logic / 来源逻辑

- <步骤、因果链或论证结构>

### Key Concepts / 关键概念

- <术语或概念>:

### Assumptions / 假设

- <假设> -> <为什么需要>

### Boundaries / 边界

- <不能宣称或不能推断的内容>

## 风格表达层 / Style Rendering Layer

- Platform / 平台:
- Audience / 读者:
- Density / 信息密度:
- Tone / 语气:
- Card rhythm / 卡片节奏:
- Title strategy / 标题策略:
- Visual direction / 视觉方向:
- CTA style / 行动引导:
- Forbidden patterns / 禁用模式:
- Visual motif / 视觉母题:

## 卡片草稿 / Card Draft

### Card 1: <标题>

- 这张卡的任务:
- Content Copy / 内容文案:
- Layout Brief / 版式说明:
- Visual Elements / 视觉元素:
- Image Prompt / 生图提示词:
- Negative Prompt / Avoid:
- Text Readability Notes / 文字可读性提醒:
- Visual Motif Notes / 视觉母题说明:
- Evidence Notes / 证据说明:

### Card 2: <标题>

...

## 配文 / Caption

<可直接发布或继续编辑的中文配文>

## 来源支撑声明 / Source-Backed Claims

- <声明> -> <来源依据>

## 待验证声明 / Claims Needing Verification

- <声明> -> <需要验证的原因>

## 质量检查 / Quality Check

- <通过或需要修订的说明>
```

## 质量检查 / Quality Checks

- 来源事实、来源逻辑、编辑解释和假设被清楚分开。
- 风格改变只影响表达、节奏、标题、视觉方向和 CTA，不改变来源事实。
- 图片生产简报和 image prompts 不新增来源外事实，不伪造截图、产品界面或品牌素材。
- 视觉母题是可选辅助，不能压过信息层级。
- 每张卡只有一个明确功能，且卡片顺序形成可理解路径。
- 技术词、工具能力、价格、模型、时间、数据和用户反馈没有被编造。
- 平台适配具体，不只是把同一段话换行。
- 输出避免“万能提示词”“一键提效”“私藏神器”等 generic prompt-library phrasing。
- 视觉建议可供设计或排版使用，但不伪装成已有素材。
- 生图提示词必须说明外部生成或设计步骤，不暗示 Skill 已经生成图片。

## 不适用场景 / Failure Boundaries

- 不为没有来源材料的任务编造“知识卡”。
- 不大段复写受版权保护的原文。
- 不处理需要专业审核的医疗、法律、金融或安全关键建议，除非明确标记为需专家复核。
- 如果用户要求夸大效果、伪造案例或隐藏不确定性，要拒绝这部分要求并给出可替代的真实表达。
- 如果来源太薄，只输出“材料不足报告”和需要补充的输入。
- 如果风格要求与来源事实冲突，优先保护来源事实和证据边界。
- 如果用户要求模仿现有 IP、品牌角色、动漫角色、游戏角色、名人或受版权保护 mascot，要拒绝该视觉要求并改用原创抽象角色或 icon-only。

## 示例输入 / Example Input

```text
把下面这段 AI 编程工具更新说明转成 3 种风格：小红书轻知识卡、技术深读卡、内部培训知识卡。要求中文输出，保留英文功能名，不要编造文档里没有的能力，并说明不同风格改变了什么、哪些来源事实保持不变。
同时为每张卡输出 Layout Brief、Visual Elements、Image Prompt、Negative Prompt 和 Text Readability Notes。不要直接生成图片。

[用户粘贴来源摘录]
```

## 示例输出结构 / Example Output Structure

参考 `examples/same-source-three-styles.md`。最小结构应包含：

```markdown
## 内容简报 / Content Brief

- 来源:
- 不变事实:
- 风格版本:

## Style A: 小红书轻知识卡

- Style profile:
- Image brief:
- Cards 1-3:

## Style B: 技术深读卡

- Style profile:
- Image brief:
- Cards 1-3:

## Style C: 内部培训知识卡

- Style profile:
- Image brief:
- Cards 1-3:

## What Changed Across Styles / 风格变化

- <表达、节奏、视觉和 CTA 的变化>

## What Stayed Invariant / 不变内容

- <来源事实和证据边界>

## Why this is not direct image generation / 为什么这还不是直接出图

- <说明本 Skill 只输出生产简报和提示词>
```

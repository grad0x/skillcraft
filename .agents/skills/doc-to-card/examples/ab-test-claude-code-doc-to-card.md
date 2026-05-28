# A/B Test: Claude Code Doc To Card

这是 `doc-to-card` 的第一次 A/B test / 对照测试。目标是判断：相比一句普通提示词，`doc-to-card` 是否能更稳定地产出可复用、可评测、可进入图文生产流程的卡片方案。

本测试不声称已阅读 Claude Code 完整官方文档。Source URL 仅作为来源参考链接记录：[https://github.com/anthropics/claude-code](https://github.com/anthropics/claude-code)。本次实际测试只使用下面的 controlled source snapshot / 受控来源快照。

## Test Source / 测试来源

```text
* Claude Code is an agentic coding tool.
* It lives in the terminal and can also be used in IDE or GitHub workflows.
* It helps developers work with codebases through natural language.
* It can execute routine coding tasks, explain complex code, and handle git workflows.
* It is designed for developer workflows rather than general chat.
```

## Shared Evidence Boundary / 共同证据边界

- 可以说：Claude Code 是 agentic coding tool / 代理式编程工具。
- 可以说：它主要面向 developer workflows / 开发者工作流，而不是 general chat / 通用聊天。
- 可以说：它可在 terminal / 终端中使用，也可用于 IDE 或 GitHub workflows。
- 可以说：它帮助开发者用自然语言处理 codebases / 代码库。
- 可以说：它可执行 routine coding tasks / 常规编码任务、解释复杂代码、处理 git workflows。
- 不能说：价格、性能、支持的具体 IDE、模型、安装方式、企业采用情况、用户数量、benchmark 或官方未在 snapshot 中声明的结论。

## Group A: Normal Prompt Baseline / 普通提示词基线

### Input Prompt

```text
帮我把这段 Claude Code 介绍做成小红书图文卡片。
```

### Output Result

#### 标题

Claude Code：写代码时可以直接对代码库“说人话”

#### 卡片 1：它是什么？

Claude Code 是一个 agentic coding tool，也就是面向编程任务的 AI 编码工具。

#### 卡片 2：它在哪里用？

它可以在 terminal / 终端里使用，也可以进入 IDE 或 GitHub workflows。

#### 卡片 3：它能帮你做什么？

你可以用自然语言让它理解代码库、处理常规编码任务、解释复杂代码。

#### 卡片 4：和普通聊天有什么不同？

Claude Code 不是泛泛聊天助手，它更偏向 developer workflows / 开发者工作流。

#### 卡片 5：适合谁？

适合想用 AI 参与真实代码库工作的开发者，以及想了解 AI Coding 工具的学习者。

#### 配文

如果你正在关注 AI Coding 工具，可以先把 Claude Code 理解成一个面向代码库和开发流程的 agentic coding tool。它不是普通聊天，而是更贴近开发者工作流。

### Evaluation Notes

- Number of assumptions made / 假设数量: 3
  - 假设卡片数量为 5。
  - 假设目标平台为小红书轻知识风格。
  - 假设“适合 AI Coding 工具学习者”作为目标读者。
- Whether source facts are separated from interpretation / 是否分离来源事实与解释: No。事实和解释混在卡片文案里。
- Whether visual production brief is present / 是否有视觉生产简报: No。只有少量文字卡片。
- Whether image prompts are usable / 生图提示词是否可用: No。没有 image prompts。
- Whether the result is ready for RedSkill demo / 是否适合 RedSkill demo: No。能展示普通输出，但不能展示 `doc-to-card` 的可复用 workflow 能力。

## Group B: Skill Default / 使用 doc-to-card 默认配置

### Input Prompt

```text
把这段 Claude Code 介绍做成中文图文卡片，适合小红书发布。
```

### Output Result

## 内容简报 / Content Brief

- 来源: 用户提供的 Claude Code controlled source snapshot。
- 目标读者: 想了解 AI Coding 工具的中文 AI 工具用户和创作者。
- 发布渠道: 小红书。
- 内容目标: 解释 Claude Code 是什么、适合什么工作流、不要把它理解成普通聊天。
- 选用风格: 小红书轻知识卡 default。
- 选用卡片架构: 工具文档型。
- 需要验证的信息: 价格、安装方式、支持的具体 IDE、模型、性能、用户数据。

## 来源理解层 / Source Understanding Layer

### Source Facts / 来源事实

- Claude Code 是 agentic coding tool。
- 它 lives in the terminal，也可用于 IDE 或 GitHub workflows。
- 它帮助开发者通过 natural language 处理 codebases。
- 它可以执行 routine coding tasks、解释 complex code、处理 git workflows。
- 它面向 developer workflows，而不是 general chat。

### Assumptions / 假设

- 小红书读者需要先理解“它和普通聊天有什么不同”。
- 使用 6 张卡片，对应工具文档型架构。
- 默认不使用 mascot，以 icon-only / 图标辅助为主。

### Boundaries / 边界

- 不补充官方文档之外的安装、价格、模型、benchmark 或具体 IDE 支持。
- 不说“一键替代程序员”。
- 不说它能完成所有开发任务。

## 风格表达层 / Style Rendering Layer

- Platform / 平台: 小红书。
- Audience / 读者: AI Coding 工具入门到进阶用户。
- Density / 信息密度: 中。
- Tone / 语气: 清楚、轻解释、克制。
- Card rhythm / 卡片节奏: 一张卡一个问题，先定义，再讲场景和边界。
- Title strategy / 标题策略: 问题型 + 结论型。
- Visual direction / 视觉方向: 蓝白信息卡、图标辅助、流程箭头。
- CTA style / 行动引导: 收藏并用自己的代码库场景对照。
- Forbidden patterns / 禁用模式: 一键替代程序员、效率翻倍、神器、官方未声明结论。
- Visual motif / 视觉母题: icon-only。

## 卡片草稿 / Card Draft

### Card 1: Claude Code 不是普通聊天工具

- 这张卡的任务: 建立核心区别。
- Content Copy / 内容文案: Claude Code 是一个 agentic coding tool / 代理式编程工具。它面向 developer workflows，而不是 general chat。
- Layout Brief / 版式说明: 顶部大标题，中间做“普通聊天 vs 开发工作流”对比，底部放来源边界小字。
- Visual Elements / 视觉元素: 对比箭头、终端图标、代码库图标。
- Image Prompt / 生图提示词: 生成一张小红书 4:5 蓝白信息卡背景，中心为普通聊天与开发工作流的左右对比，使用终端图标和代码库图标，简洁圆角卡片，高留白，文字后期排版。
- Negative Prompt / Avoid: 不要真实品牌 logo，不要代码截图，不要小字，不要夸张科幻背景，不要人物替代程序员。
- Text Readability Notes / 文字可读性提醒: 标题不超过 16 个汉字；英文术语用标签样式。
- Evidence Notes / 证据说明: “agentic coding tool”和“developer workflows rather than general chat”来自 source snapshot。

### Card 2: 它主要住在 terminal 里

- 这张卡的任务: 说明使用环境。
- Content Copy / 内容文案: Snapshot 说 Claude Code lives in the terminal，也可以用于 IDE 或 GitHub workflows。它更像进入开发流程的工具，而不是独立聊天窗口。
- Layout Brief / 版式说明: 顶部标题，主体三块入口：Terminal、IDE、GitHub workflows。
- Visual Elements / 视觉元素: 三个入口图标、轻量连接线。
- Image Prompt / 生图提示词: 4:5 中文信息卡背景，三枚圆角模块分别表示 terminal、IDE、GitHub workflows，蓝白轻科技风，留出标题和说明文字区域。
- Negative Prompt / Avoid: 不要具体 IDE logo，不要 GitHub 商标复刻，不要真实终端截图，不要生成密集文字。
- Text Readability Notes / 文字可读性提醒: 三个入口词可保留英文；中文解释最多两行。
- Evidence Notes / 证据说明: terminal、IDE、GitHub workflows 来自 source snapshot。

### Card 3: 它帮你用自然语言处理代码库

- 这张卡的任务: 说明核心交互方式。
- Content Copy / 内容文案: 它帮助 developers work with codebases through natural language / 用自然语言处理代码库。
- Layout Brief / 版式说明: 左侧自然语言气泡，右侧代码库模块，中间用箭头连接。
- Visual Elements / 视觉元素: 语言气泡、文件树抽象图标、箭头。
- Image Prompt / 生图提示词: 小红书 4:5 信息图，左侧是自然语言气泡，右侧是抽象代码库文件树，中间箭头连接，蓝白圆角卡片，高留白，文字后期添加。
- Negative Prompt / Avoid: 不要真实代码内容，不要复杂 UI，不要声称自动完成所有开发。
- Text Readability Notes / 文字可读性提醒: “natural language”和“codebases”保留英文小标签。
- Evidence Notes / 证据说明: 来自 source snapshot 第三条。

### Card 4: 它覆盖的是 routine coding tasks

- 这张卡的任务: 列出能力但不夸大。
- Content Copy / 内容文案: Snapshot 提到三类任务：routine coding tasks、explain complex code、handle git workflows。
- Layout Brief / 版式说明: 三列表格，分别是编码任务、代码解释、Git 工作流。
- Visual Elements / 视觉元素: 任务图标、放大镜图标、git 分支图标。
- Image Prompt / 生图提示词: 4:5 蓝白信息卡，三列能力卡片布局，分别用任务清单、放大镜、git 分支图标表示，干净克制，不出现真实产品界面。
- Negative Prompt / Avoid: 不要写“一键完成项目”，不要性能数据，不要真实 GitHub UI。
- Text Readability Notes / 文字可读性提醒: 每列不超过 8 个汉字标题，英文作为小标签。
- Evidence Notes / 证据说明: 三类能力来自 source snapshot。

### Card 5: 适合先从开发流程理解它

- 这张卡的任务: 给读者判断方式。
- Content Copy / 内容文案: 先不要把它理解成“更会聊天的 AI”。更准确的入口是：它如何进入你的 coding、review、git 等开发流程。
- Layout Brief / 版式说明: 使用“不要这样理解 / 可以这样理解”的对比卡。
- Visual Elements / 视觉元素: 禁止符号、流程图标、代码分支图标。
- Image Prompt / 生图提示词: 生成一张对比型小红书信息卡，左侧“不是普通聊天”，右侧“进入开发流程”，蓝白圆角卡，高留白，抽象流程图标，文字后期排版。
- Negative Prompt / Avoid: 不要贬低通用聊天工具，不要夸大替代开发者，不要品牌仿冒。
- Text Readability Notes / 文字可读性提醒: 对比语句短，左右两侧视觉重量一致。
- Evidence Notes / 证据说明: developer workflows rather than general chat 来自 source snapshot。

### Card 6: 发布前要查哪些信息？

- 这张卡的任务: 明确待验证内容。
- Content Copy / 内容文案: 如果要继续写深度介绍，需要查官方材料：安装方式、具体 IDE 支持、价格、模型、权限、限制。
- Layout Brief / 版式说明: Checklist 结尾卡，突出“待验证”。
- Visual Elements / 视觉元素: checklist、问号图标、来源链接占位。
- Image Prompt / 生图提示词: 4:5 checklist 风格信息卡，标题区写待验证信息，主体为清晰检查清单布局，蓝白轻科技感，留出文字排版空间。
- Negative Prompt / Avoid: 不要把待验证信息写成事实，不要编造价格或安装步骤。
- Text Readability Notes / 文字可读性提醒: checklist 项目最多 6 个，避免小字。
- Evidence Notes / 证据说明: 这些不是 source facts，而是 source snapshot 未覆盖的边界。

### Evaluation Notes

- Number of assumptions made / 假设数量: 3
  - 默认使用小红书轻知识卡风格。
  - 默认 6 张卡，对应工具文档型架构。
  - 默认 icon-only，不使用角色母题。
- Whether source facts are separated from interpretation / 是否分离来源事实与解释: Yes。单独列出 Source Facts、Assumptions、Boundaries。
- Whether visual production brief is present / 是否有视觉生产简报: Yes。每张卡包含 layout、visual elements 和 readability notes。
- Whether image prompts are usable / 生图提示词是否可用: Mostly yes。可用于背景图和信息图方向，但风格还比较通用。
- Whether the result is ready for RedSkill demo / 是否适合 RedSkill demo: Partial。能展示 workflow 优势，但还缺少更有辨识度的完整 style profile。

## Group C: Skill Full Profile / 使用 doc-to-card 完整配置

### Input Prompt

```text
Use doc-to-card with this style profile:

Platform / 平台: 小红书
Audience / 目标读者: 想了解 AI Coding 工具的中文 AI 工具用户和技术内容创作者
Card count / 卡片数量: 6
Density / 信息密度: 中
Tone / 语气: 清楚、克制、有启发，不夸张
Visual style / 视觉风格: 蓝白轻科技感，圆角卡片，高留白，信息层级清晰
Title strategy / 标题策略: 从具体问题切入，不标题党
Visual motif / 视觉母题: character-pair，小机器人代表 Agent，小狐狸代表学习者；不要幼稚，不模仿任何已有 IP
Output requirement / 输出要求: 每张卡包含 Content Copy, Layout Brief, Visual Elements, Image Prompt, Negative Prompt, Text Readability Notes, Evidence Notes
Avoid / 禁用项: 不要夸大 Claude Code 能力，不要声称“一键替代程序员”，不要编造性能、价格、可用性、用户数据或官方未声明的结论
```

### Output Result

## 内容简报 / Content Brief

- 来源: 用户提供的 Claude Code controlled source snapshot。
- 目标读者: 想了解 AI Coding 工具的中文 AI 工具用户和技术内容创作者。
- 发布渠道: 小红书。
- 内容目标: 用 6 张卡解释 Claude Code 的定位、使用环境、能力范围和证据边界。
- 选用风格: 小红书轻知识卡，使用完整 style profile。
- 选用卡片架构: 工具文档型。
- 视觉母题: character-pair，小机器人代表 Agent，小狐狸代表学习者；原创、克制、不幼稚。
- 需要验证的信息: 价格、安装方式、具体 IDE 支持、模型、权限、性能、可用区域、用户数据。

## 来源理解层 / Source Understanding Layer

### Source Facts / 来源事实

- Claude Code is an agentic coding tool。
- It lives in the terminal and can also be used in IDE or GitHub workflows。
- It helps developers work with codebases through natural language。
- It can execute routine coding tasks, explain complex code, and handle git workflows。
- It is designed for developer workflows rather than general chat。

### Source Logic / 来源逻辑

- 先定义工具类型：agentic coding tool。
- 再说明使用位置：terminal、IDE、GitHub workflows。
- 再说明交互方式：natural language with codebases。
- 再说明能力范围：routine coding tasks、complex code explanation、git workflows。
- 最后限定定位：developer workflows，不是 general chat。

### Assumptions / 假设

- 目标读者知道“AI Coding 工具”，但不一定理解 agentic coding tool。
- 小红书读者需要先用“它不是普通聊天”建立定位。
- 角色母题用于导视和记忆，不承担事实说明。

### Boundaries / 边界

- 不宣称 Claude Code 能替代程序员。
- 不宣称它能完成所有开发任务。
- 不补充价格、性能、模型、安装命令、具体 IDE 名称或用户数据。
- 不把“can also be used in IDE or GitHub workflows”扩写为“支持所有 IDE / GitHub 全流程自动化”。

## 风格表达层 / Style Rendering Layer

- Platform / 平台: 小红书。
- Audience / 读者: 中文 AI 工具用户、技术内容创作者。
- Density / 信息密度: 中。
- Tone / 语气: 清楚、克制、有启发，不夸张。
- Card rhythm / 卡片节奏: 从具体误区切入，再解释位置、交互、能力、边界和下一步。
- Title strategy / 标题策略: 具体问题切入，不标题党。
- Visual direction / 视觉方向: 蓝白轻科技感、圆角卡片、高留白、清晰信息层级。
- CTA style / 行动引导: 收藏并用自己的开发流程对照检查。
- Forbidden patterns / 禁用模式: 一键替代程序员、效率翻倍、神器、官方未声明结论。
- Visual motif / 视觉母题: character-pair，小机器人 + 小狐狸；每张卡只做轻量导视。

## 卡片草稿 / Card Draft

### Card 1: Claude Code 解决的不是“聊天”，是进开发流程

- 这张卡的任务: 建立核心定位。
- Content Copy / 内容文案: Claude Code 是一个 agentic coding tool / 代理式编程工具。更准确的理解方式不是“更会聊天的 AI”，而是“能进入 developer workflows / 开发者工作流的工具”。
- Layout Brief / 版式说明: 4:5 竖版。顶部大标题占 25%，中间左右对比：“general chat” vs “developer workflow”，底部放证据边界小字。小机器人站在 workflow 一侧，小狐狸在中间提问。
- Visual Elements / 视觉元素: 蓝白圆角主卡、左右对比模块、终端图标、流程箭头、小机器人、小狐狸。
- Image Prompt / 生图提示词: 生成一张小红书 4:5 蓝白轻科技感信息卡背景，圆角卡片，高留白，左右对比构图：左侧是抽象聊天气泡，右侧是开发工作流模块和终端图标，中间有原创小机器人和小狐狸作为轻量导视角色，角色不幼稚，不模仿任何 IP，文字由后期设计工具添加。
- Negative Prompt / Avoid: 不要真实 Anthropic 或 Claude logo，不要现有 IP 角色，不要代码截图，不要小字，不要夸张科幻，不要“替代程序员”暗示。
- Text Readability Notes / 文字可读性提醒: 标题 18 字以内；`agentic coding tool` 和 `developer workflow` 用小标签；底部证据边界不少于正文 70% 字号。
- Evidence Notes / 证据说明: “agentic coding tool”和“developer workflows rather than general chat”来自 source snapshot；“更准确的理解方式”是编辑解释。

### Card 2: 它首先 lives in the terminal

- 这张卡的任务: 说明使用环境。
- Content Copy / 内容文案: Snapshot 说它 lives in the terminal / 住在终端里，也可以用于 IDE 或 GitHub workflows。也就是说，它不是只在聊天窗口里回答问题。
- Layout Brief / 版式说明: 三个入口模块横向排列：Terminal、IDE、GitHub workflows。小狐狸看向三个入口，小机器人拿着路线牌。
- Visual Elements / 视觉元素: 终端窗口抽象图标、IDE 抽象图标、Git 分支图标、路线箭头、双角色轻量导视。
- Image Prompt / 生图提示词: 4:5 蓝白信息卡，三枚圆角入口模块分别表示 terminal、IDE、GitHub workflows，简洁图标，原创小机器人拿路线牌，小狐狸观察入口，整体克制现代，不幼稚，高留白，文字后期排版。
- Negative Prompt / Avoid: 不要具体 IDE logo，不要 GitHub 商标复刻，不要真实终端界面，不要品牌仿冒，不要密集文字。
- Text Readability Notes / 文字可读性提醒: 三个入口词保留英文；每个模块只放一个中文短解释；避免图标和文字重叠。
- Evidence Notes / 证据说明: terminal、IDE、GitHub workflows 来自 source snapshot。

### Card 3: 它让你用自然语言处理代码库

- 这张卡的任务: 说明核心交互方式。
- Content Copy / 内容文案: Claude Code helps developers work with codebases through natural language。重点是“面向代码库工作”，不是随便闲聊。
- Layout Brief / 版式说明: 左侧为自然语言输入气泡，右侧为 codebase 文件树，中间箭头标注“through natural language”。小机器人在右侧整理代码库，小狐狸在左侧输入问题。
- Visual Elements / 视觉元素: 输入气泡、文件树、箭头、代码块抽象、双角色。
- Image Prompt / 生图提示词: 生成一张小红书 4:5 知识卡背景，蓝白轻科技风，左侧自然语言输入气泡，右侧抽象 codebase 文件树，中间有清晰箭头，原创小狐狸在输入问题，小机器人整理文件树，圆角卡片，高留白，文字由后期添加。
- Negative Prompt / Avoid: 不要真实代码内容，不要复杂 UI，不要让角色遮挡文件树，不要声称自动完成所有开发任务。
- Text Readability Notes / 文字可读性提醒: 主标题和箭头标签层级分明；英文 `codebases` 旁加中文解释。
- Evidence Notes / 证据说明: “work with codebases through natural language”来自 source snapshot；“不是随便闲聊”来自 general chat 边界。

### Card 4: 它能做的事，要按来源说清楚

- 这张卡的任务: 列能力并防止夸大。
- Content Copy / 内容文案: Source snapshot 只明确列出三类：执行 routine coding tasks / 常规编码任务，解释 complex code / 复杂代码，处理 git workflows / Git 工作流。
- Layout Brief / 版式说明: 三列能力卡片，每列一个图标和一个双语短语。底部加“只按 snapshot 声明”。
- Visual Elements / 视觉元素: checklist 图标、放大镜图标、git 分支图标、证据边界条。
- Image Prompt / 生图提示词: 生成一张蓝白圆角信息卡背景，三列能力卡片布局，分别用 checklist、放大镜、git branch 抽象图标表示 routine coding tasks、explain complex code、git workflows，底部有 evidence boundary 区域，小机器人和小狐狸只作为角落小元素，不影响信息层级。
- Negative Prompt / Avoid: 不要“一键替代程序员”，不要性能数字，不要真实 GitHub UI，不要品牌 logo，不要让角色成为主视觉。
- Text Readability Notes / 文字可读性提醒: 三列标题短，英文标签可以保留；证据边界必须清晰可读。
- Evidence Notes / 证据说明: 三类能力均来自 source snapshot。

### Card 5: 不要把它写成“万能 AI”

- 这张卡的任务: 强化边界。
- Content Copy / 内容文案: 这份 snapshot 没有说价格、性能、模型、支持的具体 IDE，也没有说它能替代开发者。写介绍时，边界比夸张更重要。
- Layout Brief / 版式说明: 风险提醒卡。中间放“不要说”列表，右侧放“可以说”列表。双角色表情克制，小狐狸拿放大镜，小机器人举边界牌。
- Visual Elements / 视觉元素: 风险提示框、不要说 / 可以说双列表、放大镜、边界牌。
- Image Prompt / 生图提示词: 4:5 小红书风险提醒信息卡，蓝白轻科技风，左右双列表布局：不要说与可以说，加入原创小狐狸放大镜和小机器人边界牌，克制不幼稚，高留白，适合后期添加中文文字。
- Negative Prompt / Avoid: 不要红色警报风过强，不要品牌仿冒，不要夸张表情，不要生成虚假数据，不要长段小字。
- Text Readability Notes / 文字可读性提醒: “不要说”每条不超过 10 个字；边界信息用高对比但不刺眼颜色。
- Evidence Notes / 证据说明: 边界来自 source snapshot 未包含的信息；“边界比夸张更重要”是本测试编辑原则。

### Card 6: 读完这 5 条，下一步该查什么？

- 这张卡的任务: 给读者下一步。
- Content Copy / 内容文案: 如果你要继续做深度介绍，下一步应查官方材料：安装方式、具体 IDE 支持、权限限制、价格、模型、真实 workflow 示例。
- Layout Brief / 版式说明: 结尾 checklist 卡。顶部总结，主体 6 项待查清单，底部 CTA：“先按来源写，再去验证细节”。
- Visual Elements / 视觉元素: checklist、外链占位、问号标签、小机器人和小狐狸站在清单旁。
- Image Prompt / 生图提示词: 生成一张小红书 4:5 checklist 结尾卡背景，蓝白轻科技风，圆角清单模块，6 个待验证项目占位，原创小机器人和小狐狸作为角落导视，高留白，文字后期排版。
- Negative Prompt / Avoid: 不要真实官方页面截图，不要编造链接内容，不要让角色占据主体，不要小字密集。
- Text Readability Notes / 文字可读性提醒: checklist 控制在 6 项；CTA 单独放底部按钮样式；不要把待验证内容写成已知事实。
- Evidence Notes / 证据说明: 这些是 source snapshot 未覆盖但发布前需要查证的信息，不是来源事实。

## Caption / 配文

这次只基于 5 条 source snapshot，不补充官方文档外的信息。Claude Code 可以先理解成面向开发者工作流的 agentic coding tool：它住在 terminal，也能进入 IDE 或 GitHub workflows，帮助开发者用自然语言处理代码库。真正发布前，价格、安装方式、具体支持范围和限制都还需要查官方材料。

## Evaluation Notes

- Number of assumptions made / 假设数量: 3
  - 假设读者熟悉 AI Coding 但不了解 Claude Code。
  - 假设小红书需要 6 张卡完整讲清定位、能力和边界。
  - 假设原创小机器人 + 小狐狸能提升记忆点，同时不压过信息。
- Whether source facts are separated from interpretation / 是否分离来源事实与解释: Yes。来源事实、来源逻辑、假设、边界和证据说明均分离。
- Whether visual production brief is present / 是否有视觉生产简报: Yes。每张卡都有 Content Copy、Layout Brief、Visual Elements、Image Prompt、Negative Prompt、Text Readability Notes、Evidence Notes。
- Whether image prompts are usable / 生图提示词是否可用: Yes。可用于生成背景插画、信息图或交给 Canva/Figma 设计；文字仍建议后期排版。
- Whether the result is ready for RedSkill demo / 是否适合 RedSkill demo: Yes, with note。它适合展示 `doc-to-card` 如何从同一来源快照产出可生产图文卡片，但仍需人工选择前三张进入真实出图实验。

## Comparison Table / 对比表

| Group | Source fidelity / 来源保真 | Structure stability / 结构稳定性 | Style clarity / 风格清晰度 | Production readiness / 图文生产可用性 | Conversation cost / 对话成本 | Main weakness / 主要问题 |
| --- | --- | --- | --- | --- | --- | --- |
| A. Normal Prompt Baseline | 中。基本没有编造，但事实和解释混在一起。 | 低。只有卡片文案，没有稳定 output contract。 | 中低。像小红书，但风格参数不明确。 | 低。没有 layout brief、image prompt 或 readability notes。 | 低。只需一句话。 | 产物像草稿，无法直接进入设计或评测。 |
| B. Skill Default | 高。来源事实、假设和边界分开。 | 高。按三层 workflow 输出。 | 中。默认小红书风格清楚，但不够有辨识度。 | 中高。有生产字段，但视觉设定较通用。 | 中。用户只需最小 instruction。 | 默认风格适合稳态生产，但 demo 记忆点不足。 |
| C. Skill Full Profile | 高。每张卡都有 evidence notes 和边界。 | 高。输出字段完整且可复用。 | 高。风格、角色、禁用项和视觉层级明确。 | 高。可直接进入前三张真实图像 brief 测试。 | 高。需要完整 profile。 | 对用户输入要求更高，输出更长，需要后续筛选。 |

## Test Conclusion / 测试结论

### Does `doc-to-card` improve over the normal prompt?

Yes。`doc-to-card` 明显优于普通一句提示词，主要体现在三个方面：

- 来源层：能把 source facts、assumptions、boundaries 和 claims needing verification 分开。
- 风格层：能显式控制平台、读者、密度、语气、标题策略、视觉方向和禁用项。
- 生产层：能输出 layout brief、visual elements、image prompts、negative prompts 和 readability notes，进入图文生产流程。

### What still needs improvement?

- B 组默认配置虽然稳定，但视觉辨识度偏通用，需要更多 default style heuristics / 默认风格启发式。
- C 组输出完整，但较长，适合生产，不适合快速浏览；后续可以增加“first 3 image-ready cards only”的输出模式。
- Image prompts 仍需真实出图测试，才能验证角色一致性、文字安全和平台观感。

### Is this ready to become the first RedSkill demo?

Yes, but use Group C as the demo base。这个测试已经能展示 `doc-to-card` 不是 prompt template，而是 reusable content-production workflow / 可复用内容生产工作流。它适合作为第一个 RedSkill demo 的候选，但发布前应补一个真实出图或 Figma/Canva mockup 结果。

### Which output should be used to generate the first 3 real images?

Use Group C Cards 1-3。

理由：

- Card 1 建立定位差异，适合做封面或第一张。
- Card 2 说明使用环境，视觉上容易做三入口结构。
- Card 3 说明自然语言处理代码库，是读者最容易理解的核心价值。

生成真实图片时仍要保持这些边界：

- 不使用真实 Anthropic / Claude logo，除非后续确认授权和使用规范。
- 不让小机器人和小狐狸压过信息层级。
- 中文文字在设计工具中单独排版，不依赖图像模型生成小字。
- 不新增 source snapshot 之外的功能、价格、性能或支持范围声明。

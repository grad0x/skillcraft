# Cards Brief

本 brief 抽取自 `ab-test-claude-code-doc-to-card.md` 的 Group C Cards 1-3，用于制作 `cards-preview.html` 静态视觉样机。

## Series Brief / 系列简报

- Series title / 系列标题: Claude Code 先看这 3 张
- Platform / 平台: 小红书
- Aspect ratio / 画幅比例: 4:5
- Visual style / 视觉风格: 蓝白轻科技感，圆角卡片，高留白，信息层级清晰
- Color direction / 色彩方向: 冷白底、浅蓝渐变、深蓝正文、青色和橙色小面积强调
- Typography direction / 字体方向: 中文优先，英文 technical labels 使用等宽或标签样式
- Motif setting / 视觉母题: character-pair，小机器人代表 Agent，小狐狸代表学习者
- Consistency rules / 一致性规则: 三张卡使用同一背景、同一圆角系统、同一角色比例、同一证据 note 样式
- Forbidden visual patterns / 禁用视觉模式: 不出现真实 logo、不做产品 UI 截图、不模仿现有 IP、不让角色抢信息层级

## Card 1

- Title / 标题: Claude Code 解决的不是“聊天”，是进开发流程
- Content Copy / 内容文案: Claude Code 是一个 agentic coding tool / 代理式编程工具。更准确的理解方式不是“更会聊天的 AI”，而是“能进入 developer workflows / 开发者工作流的工具”。
- Layout Brief / 版式说明: 4:5 竖版。顶部大标题占 25%，中间左右对比：“general chat” vs “developer workflow”，底部放证据边界小字。小机器人站在 workflow 一侧，小狐狸在中间提问。
- Visual Elements / 视觉元素: 蓝白圆角主卡、左右对比模块、终端图标、流程箭头、小机器人、小狐狸。
- Image Prompt / 生图提示词: 生成一张小红书 4:5 蓝白轻科技感信息卡背景，圆角卡片，高留白，左右对比构图：左侧是抽象聊天气泡，右侧是开发工作流模块和终端图标，中间有原创小机器人和小狐狸作为轻量导视角色，角色不幼稚，不模仿任何 IP，文字由后期设计工具添加。
- Negative Prompt / Avoid: 不要真实 Anthropic 或 Claude logo，不要现有 IP 角色，不要代码截图，不要小字，不要夸张科幻，不要“替代程序员”暗示。
- Text Readability Notes / 文字可读性提醒: 标题 18 字以内；`agentic coding tool` 和 `developer workflow` 用小标签；底部证据边界不少于正文 70% 字号。
- Evidence Notes / 证据说明: “agentic coding tool”和“developer workflows rather than general chat”来自 source snapshot；“更准确的理解方式”是编辑解释。

## Card 2

- Title / 标题: 它首先 lives in the terminal
- Content Copy / 内容文案: Snapshot 说它 lives in the terminal / 住在终端里，也可以用于 IDE 或 GitHub workflows。也就是说，它不是只在聊天窗口里回答问题。
- Layout Brief / 版式说明: 三个入口模块横向排列：Terminal、IDE、GitHub workflows。小狐狸看向三个入口，小机器人拿着路线牌。
- Visual Elements / 视觉元素: 终端窗口抽象图标、IDE 抽象图标、Git 分支图标、路线箭头、双角色轻量导视。
- Image Prompt / 生图提示词: 4:5 蓝白信息卡，三枚圆角入口模块分别表示 terminal、IDE、GitHub workflows，简洁图标，原创小机器人拿路线牌，小狐狸观察入口，整体克制现代，不幼稚，高留白，文字后期排版。
- Negative Prompt / Avoid: 不要具体 IDE logo，不要 GitHub 商标复刻，不要真实终端界面，不要品牌仿冒，不要密集文字。
- Text Readability Notes / 文字可读性提醒: 三个入口词保留英文；每个模块只放一个中文短解释；避免图标和文字重叠。
- Evidence Notes / 证据说明: terminal、IDE、GitHub workflows 来自 source snapshot。

## Card 3

- Title / 标题: 它让你用自然语言处理代码库
- Content Copy / 内容文案: Claude Code helps developers work with codebases through natural language。重点是“面向代码库工作”，不是随便闲聊。
- Layout Brief / 版式说明: 左侧为自然语言输入气泡，右侧为 codebase 文件树，中间箭头标注“through natural language”。小机器人在右侧整理代码库，小狐狸在左侧输入问题。
- Visual Elements / 视觉元素: 输入气泡、文件树、箭头、代码块抽象、双角色。
- Image Prompt / 生图提示词: 生成一张小红书 4:5 知识卡背景，蓝白轻科技风，左侧自然语言输入气泡，右侧抽象 codebase 文件树，中间有清晰箭头，原创小狐狸在输入问题，小机器人整理文件树，圆角卡片，高留白，文字由后期添加。
- Negative Prompt / Avoid: 不要真实代码内容，不要复杂 UI，不要让角色遮挡文件树，不要声称自动完成所有开发任务。
- Text Readability Notes / 文字可读性提醒: 主标题和箭头标签层级分明；英文 `codebases` 旁加中文解释。
- Evidence Notes / 证据说明: “work with codebases through natural language”来自 source snapshot；“不是随便闲聊”来自 general chat 边界。

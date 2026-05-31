# Design Reference Notes

本 note 用来记录 `template-lab.html` 的参考依据。外部项目只作为 pattern benchmark / 模式参考，不复制第三方源码、素材、logo、截图或角色。

## Reference Families Considered

- Open Design `card-xiaohongshu`: 小红书风格 knowledge cards 可以被组织成 swipeable multi-card carousel。对 SkillCraft 的启发是：卡片模板应该是一个可复用 rendering surface，而不是一次性 CSS 手工稿。
- Open Design / HTML Anything: 把 Markdown、数据或文本转成可导出的 HTML surface，并支持 Xiaohongshu vertical card export。对 SkillCraft 的启发是：`doc-to-card` 可以先输出内容与生产简报，再由不同 HTML/CSS 模板渲染。
- CardPlanet-style card generators: 常见知识卡工具会提供多种 style presets，并强调内容输入、模板选择、自动排版和高分辨率导出。对 SkillCraft 的启发是：模板方向要可命名、可比较、可替换。
- Carousel Generator-style workflow: carousel 工具通常把 slide 拆成 intro、content、outro 等类型，支持标题平衡、增删重排、导入导出与全局设置。对 SkillCraft 的启发是：单张卡不应孤立设计，后续需要承接整组 Cards 1-3 的 rhythm。
- General HTML/CSS social media template patterns: 固定尺寸画布、设计 token、边界留白、模块化视觉区和 export-friendly layout，能让截图、PNG 导出或后续 Figma/Canva 复刻更稳定。

## Useful Patterns

- Fixed-size card canvas: 每张候选卡都保持 `1080px × 1350px`，对应小红书 4:5 截图工作流。
- Reusable design tokens: 颜色、边框、chip、soft panel、accent 等变量集中定义，方便换主题。
- Title zone / body zone / visual zone / boundary note: 把信息层级固定下来，避免模板为了好看改变来源事实。
- Slide/card types: Card 1 可以有 editorial opener、soft knowledge opener、workflow explainer 三种类型；Cards 2-3 后续可沿用同一类型。
- Typography balancing: 标题优先中文，英文技术词作为标签或强调短语，避免长英文撑破画面。
- Style presets: 模板应有明确名字，例如「技术杂志风」「小红书轻知识风」「工作流解释风」，而不是只改颜色。
- Export-friendly layout: 无外链图片、无真实 UI 截图、无外部字体依赖，截图或离线打开时结果一致。

## What We Will Not Copy

- 不复制第三方 source code。
- 不使用第三方 logo、品牌资产或真实产品 UI screenshots。
- 不使用 copyrighted characters、现有 IP mascot 或品牌化角色。
- 不复刻具体商业产品的卡片样式。
- 不把 reference project 的营销承诺写进 SkillCraft demo。

## How This Informs SkillCraft

`doc-to-card` 更适合输出三层产物：

1. Content / 内容层：来源事实、边界、卡片文案、证据说明。
2. Style profile / 风格层：平台、读者、信息密度、语气、视觉母题、禁用表达。
3. Production brief / 生产层：布局、视觉元素、可读性规则、导出约束。

Rendering 可以在后续使用不同模板完成。同一份 Card 1 内容可以被渲染为技术杂志风、轻知识风或工作流解释风，但来源事实和 evidence boundary 必须保持不变。

## Reference Links

- Open Design `card-xiaohongshu`: https://open-design.ai/skills/card-xiaohongshu/
- Open Design / HTML Anything: https://open-design.ai/html-anything/
- CardPlanet FAQ: https://cardplanet.me/faq.html
- Carousel Generator GitHub: https://github.com/FranciscoMoretti/carousel-generator

# Claude Code RedSkill Demo

这是 `doc-to-card` 的第一个 visual mockup / 视觉样机示例，用来验证 workflow 是否能从 source snapshot / 来源快照，经过 Skill output / Skill 产出，进入 visual card production / 图文卡片生产。

本目录不生成图片文件，也不调用任何图像生成工具。`cards-preview.html` 是一个静态 HTML/CSS 预览，用手工排版的文字和简单几何视觉元素模拟前三张小红书卡片。

## 文件说明

- `source-snapshot.md`: 本 demo 使用的受控 Claude Code 来源快照和证据边界。
- `style-profile.md`: Group C 使用的完整 style profile / 风格配置。
- `cards-brief.md`: 从 A/B test Group C Cards 1-3 抽出的 production brief / 生产简报。
- `cards-preview.html`: 可本地打开的三张 4:5 card preview / 卡片预览。

## 这个 demo 验证什么

- `doc-to-card` 不只是生成卡片文案，还能输出 layout brief / 版式说明、visual elements / 视觉元素、image prompt / 生图提示词、negative prompt / 避免项和 readability notes / 可读性提醒。
- Skill 产物可以进入 Canva/Figma、HTML/CSS、PPTX 或图像生成工具的下一步生产流程。
- 同一个 source snapshot 的事实边界可以在视觉化时保持不变。

## 这不是直接出图

`cards-preview.html` 是 visual mockup，不是 direct image generation / 直接生图。真实 RedSkill output 应该提供：

1. Source understanding / 来源理解。
2. Card copy / 卡片文案。
3. Brief + prompt / 生产简报和提示词。
4. Optional render path / 可选渲染路径，例如 HTML/CSS、SVG、PPTX、Figma/Canva 或图像生成工具。

## 本地预览

直接在浏览器中打开：

```text
.agents/skills/doc-to-card/examples/claude-code-redskill-demo/cards-preview.html
```

三张卡片可作为 RedSkill demo 截图素材。注意：页面没有使用真实 Anthropic / Claude logo、真实 GitHub logo、真实产品 UI 截图或任何现有 IP 角色。

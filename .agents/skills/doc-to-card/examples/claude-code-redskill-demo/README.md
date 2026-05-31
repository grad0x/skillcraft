# Claude Code RedSkill Demo

这是 `doc-to-card` 的第一个 visual mockup / 视觉样机示例，用来验证 workflow 是否能从 source snapshot / 来源快照，经过 Skill output / Skill 产出，进入 visual card production / 图文卡片生产。

本目录不生成图片文件，也不调用任何图像生成工具。`cards-preview.html` 是一个静态 HTML/CSS 预览，用手工排版的文字和简单几何视觉元素模拟前三张小红书卡片。

## 文件说明

- `source-snapshot.md`: 本 demo 使用的受控 Claude Code 来源快照和证据边界。
- `style-profile.md`: Group C 使用的完整 style profile / 风格配置。
- `cards-brief.md`: 从 A/B test Group C Cards 1-3 抽出的 production brief / 生产简报。
- `design-reference-notes.md`: reference-driven template lab / 模板实验参考笔记。
- `template-lab.html`: 同一 Card 1 内容的三种模板候选，用于比较视觉方向。
- `card-renderer.css`: overview 和单卡页面共用的静态 card renderer / 卡片渲染样式。
- `cards-preview.html`: overview page / 总览页，横向展示三张卡的一致性。
- `card-01.html`: 单卡 master template candidate / 主模板候选页，1080px × 1350px。
- `card-02.html`: 单卡截图页，1080px × 1350px。
- `card-03.html`: 单卡截图页，1080px × 1350px。

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

## 本地预览 / Local Preview

打开 overview page / 总览页：

```text
.agents/skills/doc-to-card/examples/claude-code-redskill-demo/cards-preview.html
```

打开 template lab / 模板实验页：

```text
.agents/skills/doc-to-card/examples/claude-code-redskill-demo/template-lab.html
```

打开单卡 master template / 主模板页：

```text
.agents/skills/doc-to-card/examples/claude-code-redskill-demo/card-01.html
```

打开其他单卡页面：

```text
.agents/skills/doc-to-card/examples/claude-code-redskill-demo/card-02.html
.agents/skills/doc-to-card/examples/claude-code-redskill-demo/card-03.html
```

## 截图建议 / Screenshot Recommendation

- 推荐截图尺寸：`1080px × 1350px`。
- 推荐把浏览器视口设为 `1080px × 1350px`，或直接截图 `.xhs-card` 元素。
- 推荐使用单卡页面截图，不使用 overview page 截图。
- Overview page 为横向总览，窄窗口可能需要横向滚动。
- 单卡页面没有额外 dashboard text / 页面噪音，只有中间的 4:5 卡片画布。
- 如果浏览器或截图工具会自动缩放页面，请确认最终输出仍为 4:5。

## 边界说明 / Boundaries

三张卡片可作为 RedSkill demo 截图素材。注意：

- 这是 static visual mockup / 静态视觉样机，不是 automatic image generation / 自动生图。
- 页面没有使用真实 Anthropic / Claude logo。
- 页面没有使用真实 GitHub logo。
- 页面没有使用真实产品 UI 截图或 fake product UI screenshots。
- 小机器人和小狐狸是 CSS 几何图形，仅作为原创辅助 visual motif / 视觉母题。

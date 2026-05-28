# Doc To Card Quality Checklist

用于评估 `doc-to-card` 的输出是否既保真又适配风格。每次输出至少做一次快速检查；公开发布前应完整检查。

## Source Fidelity / 来源保真

- [ ] 输出标明来源材料或来源类型。
- [ ] 所有核心事实都能追溯到来源。
- [ ] 没有编造工具能力、价格、模型、日期、用户反馈或 benchmark。
- [ ] 来源逻辑没有被风格表达改写成相反含义。
- [ ] 过短或不完整来源被标记为材料不足，而不是被补全。

## Evidence Separation / 证据与假设分离

- [ ] Source facts / 来源事实单独列出。
- [ ] Assumptions / 假设单独列出，并说明为什么需要。
- [ ] Claims needing verification / 待验证声明单独列出。
- [ ] Editorial interpretation / 编辑解释没有伪装成来源事实。

## Style Fit / 风格匹配

- [ ] 输出使用了明确 style profile / 风格配置。
- [ ] 信息密度符合所选风格。
- [ ] 语气符合目标读者，不油腻、不空泛。
- [ ] 标题策略和 card rhythm / 卡片节奏一致。
- [ ] CTA style / 行动引导符合内容目标。

## Platform Fit / 平台适配

- [ ] 小红书输出短、清楚、有卡片节奏，但不标题党。
- [ ] 公众号输出解释充分，适合嵌入长文。
- [ ] LinkedIn carousel 输出结论明确，适合国际技术读者。
- [ ] 内部 wiki / 团队知识库输出可执行，少社媒口吻。
- [ ] 幻灯片 / 分享材料输出适合投影和讲解。

## Card Sequence Logic / 卡片顺序逻辑

- [ ] 选用了合适 card architecture / 卡片架构。
- [ ] 每张卡只有一个任务。
- [ ] 卡片之间有递进关系。
- [ ] 卡片数变化时没有删除关键 evidence boundary。
- [ ] 结尾提供具体下一步。

## Technical Accuracy / 技术准确性

- [ ] 英文技术词、功能名、API 名和命令名准确。
- [ ] 中文解释没有改变技术含义。
- [ ] 限制、前置条件和未验证信息可见。
- [ ] 没有把可能性写成已验证能力。

## Visual Production Usefulness / 视觉制作可用性

- [ ] 每张卡有可执行 visual direction / 视觉建议。
- [ ] 每张卡有 Layout Brief / 版式说明、Visual Elements / 视觉元素和 Image Prompt / 生图提示词。
- [ ] Negative Prompt / Avoid 排除了品牌仿冒、IP 模仿、低可读文字和无关装饰。
- [ ] Text Readability Notes / 文字可读性提醒说明标题、正文、术语和小字如何排版。
- [ ] 视觉建议服务信息结构，不只是装饰。
- [ ] 对比、流程、检查清单等建议与卡片任务匹配。
- [ ] 没有声称存在未提供的截图、图标或素材。
- [ ] 输出没有声称已经生成图片文件。

## Visual Motif Control / 视觉母题控制

- [ ] Motif setting / 视觉母题设置明确：none、icon-only、mascot、character-pair 或 scene-character。
- [ ] 角色或图标没有改变来源事实。
- [ ] 角色没有压过标题、概念和证据边界。
- [ ] 没有模仿现有 IP、品牌角色、动漫角色、游戏角色、名人或受版权保护 mascot。
- [ ] 同一系列的角色外观保持一致。

## Anti-Slop Checks / 反 AI 味检查

- [ ] 没有“赋能、颠覆、效率翻倍、私藏神器、一键搞定”等空泛话术。
- [ ] 没有通用 prompt-library phrasing，例如“复制这段提示词即可”。
- [ ] 没有连续堆叠抽象名词。
- [ ] 没有用夸张情绪替代来源证据。
- [ ] 读者能看出具体场景、具体动作和具体边界。

## Decision / 判断

- Publish / 可发布：全部关键项通过，没有事实或边界问题。
- Revise / 需修订：风格或平台适配弱，但事实保真。
- Block / 阻塞：存在编造事实、证据边界被破坏、隐私或高风险问题。

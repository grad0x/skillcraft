---
name: tool-learning-path
description: Design practical learning paths for AI tools, developer tools, creative tools, or repeatable workflows by converting documentation, tutorials, and user goals into modules, exercises, checkpoints, and self-tests. Use when Chinese AI learners, technical writers, teams, or skill authors need a structured path for learning a tool through hands-on tasks instead of passive prompt collections.
---

# Tool Learning Path

默认用中文输出，除非用户明确要求英文。保留工具名、命令、API、模型名等英文技术词。目标用户包括中文 AI 创作者、技术内容作者、AI 工具学习者和 Skill 作者。

## 什么时候使用 / When To Use

当用户想学习、教授或包装一个 AI 工具、开发者工具、创作工具或 Agent workflow，并且需要练习、检查点和可交付成果时，使用这个 Skill。

适合：

- 把官方文档或教程转成 1 天、7 天或 4 周学习路径。
- 为中文 AI 工具学习者设计实操任务，而不是只列阅读材料。
- 帮团队把一个工具的上手流程变成可验收训练。
- 把一个 Skill Pack / 能力包的使用方式拆成学习模块和 eval case / 评测用例。

不适合：简单功能摘要、未经验证的工具推荐、纯鸡血学习计划、没有练习任务的课程大纲。

## 输入要求 / Inputs

尽量从用户请求中提取；缺失时先给出假设，关键缺口要追问。

- 工具或 workflow 名称。
- 来源材料：官方文档、教程、用户笔记、内部 SOP、截图描述或摘录。
- 学习者画像：新手、创作者、技术内容作者、开发者、团队负责人、培训者等。
- 学习目标：发布内容、搭建工作流、自动化任务、评估工具、训练团队等。
- 时间预算：1 小时、1 天、7 天、4 周或自定义。
- 环境限制：账号权限、付费功能、本地配置、平台限制、语言偏好。
- 证明标准：学习者必须产出什么，才算真的掌握。

涉及当前产品能力、价格、模型、权限或政策时，必须验证官方来源，或标记为 assumption / 假设。

## 工作流程 / Workflow

1. 定义可观察学习结果。
   - 把“学会这个工具”改写成具体产物，例如“完成一个可复用卡片工作流”。
   - 说明学习者最终应能独立完成什么任务。

2. 画出能力阶梯。
   - 找出前置概念和必要环境。
   - 按“认识 -> 跟做 -> 独立完成 -> 处理边界情况”排序。
   - 区分核心能力和可选高级能力。

3. 设计任务型模块。
   - 每个模块只对应一个学习目标和一个 deliverable / 交付物。
   - 每个模块包含概念说明、实操任务、输出要求和 checkpoint / 检查点。
   - 优先使用真实创作、写作、开发或 Skill 作者场景。

4. 加入练习案例。
   - 至少给 easy / normal / edge 三类任务。
   - 每个任务都要能被人或 Agent 复核。
   - 中文创作者场景要具体，例如“把工具更新说明转成小红书教学卡片”。

5. 定义验证方式。
   - 写清楚好产物长什么样。
   - 列出常见失败表现和修复方式。
   - 加一个 final capstone / 综合任务，要求综合使用多个能力。

6. 输出学习路径。
   - 只有在用户要求时才强行排日程。
   - 把必做任务和可选探索分开。
   - 把来源和假设列在最后，避免把未验证信息当事实。

## 输出格式 / Output Format

按下面结构输出 Markdown：

```markdown
## 学习路径简报 / Learning Path Brief

- 工具或 workflow:
- 学习者:
- 学习结果:
- 时间预算:
- 证明标准:
- 关键假设:

## 路径总览 / Path Overview

| 模块 | 目标 | 交付物 | 检查点 |
| --- | --- | --- | --- |

## 模块 / Modules

### Module 1: <模块名>

- 概念:
- 任务:
- 输出:
- 检查点:
- 常见失败:
- 修复方式:

## 练习案例 / Practice Cases

- Easy:
- Normal:
- Edge:

## 综合任务 / Final Capstone

- 场景:
- 必交产物:
- 通过标准:

## 来源与假设 / Assumptions And Sources

- <来源或假设>
```

## 质量检查 / Quality Checks

- 学习路径指向可见产物，而不是只要求“理解”。
- 每个模块只有一个学习目标和一个交付物。
- 练习任务贴近目标用户的真实工作。
- checkpoint / 检查点可以由其他人复核。
- 当前产品细节有来源、被验证，或明确标记为 assumption / 假设。
- 学习活动以实践为主，不以“看、读、记”为主。

## 不适用场景 / Failure Boundaries

- 不编造工具功能、价格、权限、模型名、平台政策或发布日期。
- 不要求学习者使用未确认可访问的付费功能、私有数据或凭据。
- 不设计绕过平台政策、抓取受保护内容、泄露用户数据的练习。
- 不把缺少关键 setup 信息的学习路径说成完整可执行。
- 如果目标过大，先收窄到一个可验证结果，并说明暂不覆盖的部分。

## 示例输入 / Example Input

```text
我想给中文 AI 工具学习者设计一个 7 天 Claude Code 入门路径。目标是让他们能用 Agent 完成一次文档到卡片的内容工作流。请只基于我提供的文档摘录，不要编造当前产品能力。

[用户粘贴文档摘录和限制]
```

## 示例输出结构 / Example Output Structure

```markdown
## 学习路径简报 / Learning Path Brief

- 工具或 workflow: Claude Code 文档到卡片工作流
- 学习者: 中文 AI 工具学习者
- 学习结果: 独立完成一次有来源依据的卡片内容产出
- 时间预算: 7 天
- 证明标准: 提交一个卡片草稿、来源声明和质量检查记录

## 路径总览 / Path Overview

| 模块 | 目标 | 交付物 | 检查点 |
| --- | --- | --- | --- |
| Day 1 | 建立工具使用边界 | 环境和来源清单 | 没有未验证产品声明 |

...

## 练习案例 / Practice Cases

- Easy: 用 300 字文档生成 3 张卡
- Normal: 用 900 字文档生成 6 张卡
- Edge: 来源材料缺少关键 setup 信息时生成缺口报告
```

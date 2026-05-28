# Redskill Distribution Playbook

这份 playbook 用于把 SkillCraft Skill 包装成面向创作者的公开 artifact。它服务于 documentation-first / 文档优先版本：主产物是经过验证的 Agent Skill，不是 app。

## 定义 / Definition

RedSkill 是为创作者分发准备的 reusable Agent Skill：

- 解决一个可重复任务。
- 有清楚的 trigger / 触发场景和 input contract / 输入契约。
- 产出可检查 artifact。
- 包含 quality checks / 质量检查和 failure boundaries / 失败边界。
- 至少有一个真实 example 或 eval case / 评测用例。

## 发布准备度 / Release Readiness

发布前确认：

- `SKILL.md` 位于 `.agents/skills/<skill-name>/`。
- Frontmatter 包含 `name` 和 `description`。
- Skill 定义什么时候使用、输入、workflow、输出格式、质量检查和失败边界。
- `examples/` 或 release note 中有真实 example。
- `evals/` 中有 checklist 或 eval case。
- 未验证 claim、当前产品事实和私有数据风险被标记。

## 包装方式 / Packaging

围绕三个 artifact 包装：

1. Skill 文件：Agent 可加载的 reusable workflow / 可复用工作流。
2. Proof artifact / 证明材料：一次 example output 或 before/after。
3. Validation artifact / 验证材料：checklist、eval case 或 review notes。

在 GitHub 中，从 README 链接这些材料。在中文创作者渠道中，把同一组材料转成清楚叙事：

- Problem：为什么这个 workflow 手动重复很痛。
- Skill：这个 Agent Skill 做什么。
- Proof：它在真实材料上跑出了什么。
- Invitation：需要哪些测试和反馈。

## 渠道建议 / Channel Guidance

### GitHub

- 受众：开发者、Skill 作者、技术内容作者。
- 格式：README、目录结构、examples、evals、issues。
- Call to action：用一个真实 workflow 跑一次，并提交 issue 或反馈。

### 小红书

- 受众：中文 AI 创作者和工具学习者。
- 格式：一张卡一个观点，展示问题、workflow、产物和验证方式。
- Call to action：邀请读者评论一个想包装成 Skill 的 workflow。
- 避免：财富承诺、神秘提示词、保证增长、夸大自动化。

### 公众号

- 受众：技术内容作者、AI 教育者、社区组织者。
- 格式：解释 Skill 设计原则、验证过程和 example。
- Call to action：邀请结构化反馈或共同补充 eval cases。

### 社群

- 受众：早期测试者。
- 格式：短消息，提出一个明确测试请求。
- Call to action：让一个用户类型测试一个 Skill 和一个 artifact。

## 发布顺序 / Launch Sequence

1. Private smoke test：用一个真实任务跑通 Skill。
2. Skill self-test：使用 `skill-self-test` 复核结构和边界。
3. Example capture：把最佳运行记录到 `examples/`。
4. Eval update：至少补一个 eval case 到 `evals/`。
5. GitHub publish：让仓库易读、易检查、易反馈。
6. Creator post：发布问题、workflow、proof 和反馈请求。
7. Feedback triage：把反馈转为 issue、patch note 或 eval case。

## 反馈问题 / Feedback Questions

询问测试者：

- 你使用了什么来源材料？
- Skill 在哪里要求了过多或过少上下文？
- 输出格式是否匹配你的发布或学习 workflow？
- 哪个 quality check 真正发现了问题？
- 下次复用时，什么会让它更省力？

## 修订标准 / Patch Criteria

出现这些情况时修订 Skill：

- Trigger / 触发场景不清。
- 缺少必要输入。
- Workflow 步骤依赖作者隐性经验。
- Output section 难以评测。
- Failure boundary 缺失或模糊。
- 真实 example 暴露重复失败。

## 声明纪律 / Claim Discipline

不要宣称：

- 未测量的用户数。
- 没有证据的效率提升。
- 未测试工具的兼容性。
- 平台或厂商官方背书。
- 需要专家审核领域的安全性或正确性。

优先使用可验证表述：

- “已用三个创作者文档案例测试。”
- “面向中文 AI 创作者和技术内容作者设计。”
- “Alpha skill pack; feedback requested.”
- “当前产品行为需要验证。”

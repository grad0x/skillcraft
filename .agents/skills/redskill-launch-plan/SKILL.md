---
name: redskill-launch-plan
description: Plan the packaging, validation, and distribution of reusable Agent Skills for Chinese AI creator audiences, technical writers, and skill authors. Use when a draft skill or workflow needs a launch plan with positioning, proof assets, channel strategy, feedback loops, and publishable documentation instead of a generic marketing prompt.
---

# Redskill Launch Plan

## When To Use

Use this skill when the user has a draft skill, workflow, or repeatable AI practice and wants to launch it as a public or semi-public skill artifact.

In this repository, "Redskill" means a reusable Agent Skill packaged for creator distribution: clear problem, clear invocation, testable output, public proof, and a feedback loop.

Good fits:

- Launching a new `.agents/skills/<name>/SKILL.md` skill.
- Turning a proven content workflow into a skill pack release.
- Planning a 小红书, WeChat, GitHub, or community launch around a tested workflow.
- Designing evidence assets before announcing a skill.

Do not use this skill for vague personal branding plans, hype posts, or growth tactics disconnected from a working skill artifact.

## Inputs

Ask for or infer these inputs:

- Skill name and current stage: idea, draft, tested, published, or iterating.
- Target user: Chinese AI creator, technical writer, AI tool learner, developer team, or skill author.
- Core job-to-be-done: the concrete repeatable work the skill performs.
- Proof assets: before/after examples, eval cases, screenshots, sample outputs, user feedback, or benchmark notes.
- Distribution channels: GitHub, 小红书, WeChat, community group, newsletter, workshop, internal docs, or marketplace.
- Release window and maintenance capacity.
- Boundaries: claims to avoid, unsupported platforms, compliance concerns, private data limits.

If no skill artifact exists yet, plan a validation sprint before planning a launch.

## Workflow

1. Define the launchable unit.
   - Name the skill and the exact workflow it packages.
   - State the user pain in operational terms.
   - Identify what is reusable and what still depends on the author.

2. Check readiness.
   - Confirm `SKILL.md` has frontmatter, triggers, inputs, workflow, output format, checks, and boundaries.
   - Confirm at least one realistic example exists.
   - Confirm at least one eval checklist or test case exists.

3. Write the positioning.
   - Use "for <user>, when <situation>, this skill helps <artifact>".
   - Avoid broad promises such as "master AI" or "automate everything".
   - Explain why this is a skill workflow rather than a prompt pack.

4. Build proof assets.
   - Select one before/after example.
   - Select one annotated skill excerpt.
   - Select one quality checklist result.
   - Prepare a short demo path that a new user can repeat.

5. Plan channel-specific distribution.
   - GitHub: README, examples, eval notes, issue prompts.
   - 小红书: problem card, workflow cards, output proof, invitation to test.
   - WeChat: longer rationale, design principles, walkthrough, validation notes.
   - Community group: narrow request for feedback from a specific user type.

6. Create the feedback loop.
   - Define what feedback to collect.
   - Create issue labels or a simple feedback table.
   - Decide what qualifies for a patch release.
   - Set a review date.

## Output Format

Return Markdown with this structure:

```markdown
## Launch Brief

- Skill:
- User:
- Job-to-be-done:
- Stage:
- Launch goal:

## Readiness Check

| Requirement | Status | Notes |
| --- | --- | --- |

## Positioning

- One-line:
- Longer description:
- Not this:

## Proof Assets

- Demo artifact:
- Before/after:
- Eval or checklist:
- User quote or feedback:

## Channel Plan

### GitHub

- Assets:
- Post copy:
- Call to action:

### 小红书 / WeChat / Community

- Assets:
- Post copy:
- Call to action:

## Feedback Loop

- Questions to ask:
- Success signals:
- Patch criteria:
- Review date:
```

Use Chinese for creator-facing post copy when the selected channel is Chinese-language. Keep repository and skill structure instructions in English-friendly terminology.

## Quality Checks

- The plan launches a specific skill artifact, not an abstract idea.
- Every public claim is backed by an example, eval result, or clearly labeled hypothesis.
- The channel plan adapts format and call to action instead of copying the same post everywhere.
- The launch asks for useful feedback from a defined audience.
- The plan includes maintenance and patch criteria.
- The positioning makes the workflow testable and repeatable.

## Failure Boundaries

- Do not invent user metrics, testimonials, adoption numbers, or benchmark results.
- Do not recommend spam tactics, deceptive urgency, fake scarcity, or undisclosed paid promotion.
- Do not publish private user examples, proprietary docs, or screenshots without permission.
- Do not plan a broad launch for an untested skill; recommend a small validation run first.
- If legal, policy, or platform compliance is unclear, mark it as requiring human review.

# SkillHub Scan Notes

These notes define how SkillCraft reviews public skill ecosystems, marketplace examples, and community-shared Agent Skills. They are not a claim that every ecosystem has been exhaustively scanned.

## Scan Goal

The scan looks for patterns that make skills reusable, testable, and publishable:

- What triggers the skill.
- What inputs the skill expects.
- What workflow it teaches an agent to execute.
- What output contract it promises.
- What quality checks and failure boundaries it includes.
- What examples or eval cases prove the skill works.

## What To Capture

For each candidate skill or skill-like artifact, capture:

| Field | Notes |
| --- | --- |
| Name | Skill name or public title. |
| Source | Repository, marketplace page, article, or community post. |
| Target user | Creator, developer, analyst, writer, team, or other. |
| Trigger | When an agent should use it. |
| Inputs | Required source files, context, credentials, or user choices. |
| Workflow | Main procedural steps. |
| Output | Artifact produced by the skill. |
| Validation | Examples, tests, screenshots, or checklist evidence. |
| Boundary | What the skill refuses or asks about. |
| Reuse pattern | What SkillCraft can learn from it. |

## Initial Pattern Library

Strong skills tend to have:

- A narrow job-to-be-done.
- A frontmatter description that names real trigger situations.
- A workflow that another agent can execute without private author context.
- An output format that can be reviewed.
- A small number of optional resources that reduce repeated work.
- Failure boundaries that prevent hallucinated facts and unsafe automation.

Weak skill-like artifacts often have:

- A clever name but unclear trigger.
- A broad promise such as "make better content" or "learn any tool".
- No input contract.
- No expected output structure.
- No examples or eval cases.
- Hidden dependence on the original author's taste or domain knowledge.

## SkillCraft Implications

- Keep each skill centered on a repeatable artifact.
- Include eval templates from the first release, even when no automated test runner exists.
- Treat examples as proof, not decoration.
- Use Chinese creator scenarios to validate audience fit, but keep repository structure and engineering language clear for English-speaking contributors.
- Prefer a small set of high-quality skills over a large catalog of vague prompts.

## Open Scan Questions

- Which skill categories are easiest for new users to validate in under one hour?
- Which examples best explain the difference between a prompt and an Agent Skill?
- How much bilingual content should live in `SKILL.md` versus examples?
- What metadata will future distribution platforms require beyond `name` and `description`?
- Which workflows deserve scripts or assets in later releases?

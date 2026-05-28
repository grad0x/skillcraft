# SkillCraft

SkillCraft is an AI Skill Pack experiment for turning repeatable content workflows, AI tool learning workflows, and skill engineering practices into reusable, testable, publishable Agent Skills.

The first release is documentation-first. There is no web app, runtime package, build system, or dependency setup in this repository yet.

## Why This Exists

Most AI workflow knowledge is still shared as one-off prompts, screenshots, private notes, or long tutorials. SkillCraft treats useful workflows as durable skill artifacts:

- Reusable: each workflow can be invoked repeatedly by an agent.
- Testable: each skill has inputs, expected outputs, quality checks, and failure boundaries.
- Publishable: each skill can be distributed as a folder with a clear `SKILL.md`.
- Bilingual-friendly: the repo supports Chinese AI creators while remaining readable to English-speaking developers.

SkillCraft follows the Codex Agent Skills convention:

```text
.agents/skills/<skill-name>/SKILL.md
```

Each skill directory must include a required `SKILL.md` with YAML frontmatter:

```yaml
---
name: skill-name
description: What the skill does and when to use it.
---
```

## Target Users

- Chinese AI creators who turn dense tools, papers, docs, and workflows into publishable content.
- Technical writers who need repeatable editorial systems rather than ad hoc prompts.
- AI tool learners who want structured learning paths with exercises and checkpoints.
- Skill authors who want to design, test, and distribute reusable Agent Skills.

## First Four Skills

| Skill | Purpose | Primary Output |
| --- | --- | --- |
| `doc-to-card` | Convert a source document into a multi-card educational content draft for channels such as 小红书, WeChat, LinkedIn, or internal knowledge bases. | Card-by-card content plan with captions, evidence notes, and QA checks. |
| `tool-learning-path` | Turn an AI tool, product document, or workflow into a practical learning path. | Learning modules, exercises, checkpoints, and verification tasks. |
| `redskill-launch-plan` | Plan the packaging, validation, and distribution of a reusable Agent Skill for creator audiences. | Launch plan with positioning, proof assets, publishing steps, and feedback loop. |
| `skill-self-test` | Review a skill before publishing by checking structure, triggering, workflow clarity, examples, and eval cases. | Test report with pass/fail findings and concrete fixes. |

## Repository Map

```text
.
├── .agents/skills/
│   ├── doc-to-card/SKILL.md
│   ├── tool-learning-path/SKILL.md
│   ├── redskill-launch-plan/SKILL.md
│   └── skill-self-test/SKILL.md
├── docs/
│   ├── redskill-distribution-playbook.md
│   └── skillhub-scan-notes.md
├── evals/
│   ├── content-quality-checklist.md
│   └── skill-quality-checklist.md
├── examples/
│   └── claude-code-doc-to-card/README.md
└── templates/
    ├── SKILL.md.template
    ├── eval-cases.template.md
    └── examples.template.md
```

## Design Principles

1. Start from repeatable work, not isolated prompts.
2. Define inputs and output contracts before writing examples.
3. Make quality checks explicit enough for another agent or reviewer to run.
4. State failure boundaries so the skill knows when to stop, ask, or narrow scope.
5. Keep skills small enough to be used in real agent context windows.
6. Prefer concrete workflow artifacts over motivational or generic AI advice.

## Seven-Day Validation Plan

Day 1: Use `doc-to-card` on three source types: product docs, a tutorial, and a personal note. Record whether the card outline preserves the source meaning.

Day 2: Use `tool-learning-path` for one AI coding tool and one AI writing tool. Check whether exercises can be completed without hidden assumptions.

Day 3: Use `redskill-launch-plan` to package one draft skill into a public-facing release plan. Validate that every claim has a proof artifact.

Day 4: Use `skill-self-test` against all four initial skills. File issues for unclear triggers, missing inputs, weak outputs, and vague quality checks.

Day 5: Ask two Chinese AI creators or technical writers to run one skill each on their own material. Collect friction points in their own words.

Day 6: Convert feedback into eval cases under `evals/` and update the templates so future skills inherit the better pattern.

Day 7: Publish a small release note with the tested examples, known limitations, and next candidate skills.

## Current Status

This is an alpha skill pack. The repository is ready for documentation review, example runs, and quality evaluation. It is not yet a packaged marketplace release.

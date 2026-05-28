# Redskill Distribution Playbook

This playbook explains how to package and distribute a SkillCraft skill as a public creator-facing artifact. It is designed for documentation-first releases where the main deliverable is a tested Agent Skill, not an app.

## Definition

A Redskill is a reusable Agent Skill prepared for creator distribution:

- It solves one repeatable job.
- It has a clear trigger and input contract.
- It produces a checkable artifact.
- It includes quality checks and failure boundaries.
- It has at least one realistic example or eval case.

## Release Readiness

Before distribution, confirm:

- `SKILL.md` exists under `.agents/skills/<skill-name>/`.
- Frontmatter includes `name` and `description`.
- The skill defines when to use, inputs, workflow, output format, quality checks, and failure boundaries.
- A real example exists under `examples/` or in the release note.
- A checklist or eval case exists under `evals/`.
- Unsupported claims, current product facts, and private data risks are marked.

## Packaging

Package the skill around three artifacts:

1. The skill file: the reusable workflow an agent can load.
2. The proof artifact: an example output or before/after run.
3. The validation artifact: checklist results, eval cases, or review notes.

For GitHub, link these from the repository README. For Chinese creator channels, turn the same three artifacts into a short story:

- Problem: why the workflow is hard to repeat manually.
- Skill: what the Agent Skill does.
- Proof: what happened when it was tested.
- Invitation: what feedback or example run is needed next.

## Channel Guidance

### GitHub

- Audience: developers, skill authors, technical writers.
- Format: concise README, folder structure, examples, evals, issues.
- Call to action: run the skill on one real workflow and open an issue with the result.

### 小红书

- Audience: Chinese AI creators and tool learners.
- Format: card post with one idea per card.
- Call to action: ask readers to comment with one workflow they want packaged as a skill.
- Avoid: vague claims about passive income, secret prompts, or guaranteed growth.

### WeChat Article

- Audience: technical writers, AI educators, community builders.
- Format: longer explanation of the skill design, validation process, and examples.
- Call to action: invite structured feedback or collaboration on eval cases.

### Community Group

- Audience: early testers.
- Format: short message with a narrow request.
- Call to action: ask one user type to test one skill on one artifact.

## Launch Sequence

1. Private smoke test: run the skill on one realistic task.
2. Skill self-test: review the skill using `skill-self-test`.
3. Example capture: document the best run under `examples/`.
4. Eval update: add at least one case to `evals/`.
5. GitHub publish: make the repository easy to inspect.
6. Creator post: publish the problem, workflow, proof, and request.
7. Feedback triage: convert feedback into issues or patch notes.

## Feedback Questions

Ask testers:

- What source material did you use?
- Where did the skill ask for too much or too little context?
- Did the output format match your publishing or learning workflow?
- Which quality check caught a real issue?
- What would make the skill easier to reuse next time?

## Patch Criteria

Patch the skill when:

- A trigger is unclear.
- A required input is missing.
- A workflow step relies on hidden author knowledge.
- An output section is hard to evaluate.
- A failure boundary is missing or too vague.
- A realistic example exposes a repeated failure.

## Claim Discipline

Do not claim:

- User numbers that have not been measured.
- Productivity gains without evidence.
- Compatibility with tools that were not tested.
- Official endorsement by a platform or tool vendor.
- Safety or correctness in domains requiring expert review.

Use measured language:

- "Tested on three creator-document examples."
- "Designed for Chinese AI creators and technical writers."
- "Alpha skill pack; feedback requested."
- "Requires verification for current product behavior."

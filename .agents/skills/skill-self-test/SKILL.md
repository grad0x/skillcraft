---
name: skill-self-test
description: Evaluate an Agent Skill before publishing by checking structure, trigger clarity, input contract, workflow usefulness, output format, quality checks, failure boundaries, examples, and eval cases. Use when skill authors, technical writers, or Chinese AI creator teams need a practical review of a skill file under `.agents/skills/skill-name/SKILL.md` or a draft skill pack before release.
---

# Skill Self Test

## When To Use

Use this skill when a user wants to test, review, or improve a draft Agent Skill.

Good fits:

- Reviewing one `SKILL.md` before publishing.
- Checking whether a skill is reusable and testable.
- Turning vague workflow instructions into a clear output contract.
- Creating issues from a skill QA pass.

Do not use this skill as a substitute for running the skill on real tasks. It is a pre-publish review workflow, not a guarantee that the skill works in every environment.

## Inputs

Ask for or infer these inputs:

- Skill path or pasted `SKILL.md` content.
- Intended users and trigger scenarios.
- Example user requests, if available.
- Expected outputs or sample artifacts.
- Known risks: outdated docs, policy constraints, data sensitivity, domain expertise needs.
- Release stage: draft, alpha, beta, public release, or maintenance update.

If the skill file is unavailable, ask for the `SKILL.md` content before reviewing.

## Workflow

1. Check required structure.
   - Confirm YAML frontmatter exists.
   - Confirm frontmatter contains only `name` and `description` unless the local convention explicitly allows more.
   - Confirm `name` matches the folder name when a path is available.
   - Confirm the body is Markdown and not only a placeholder.

2. Check trigger quality.
   - Read the `description` as if it is the only visible trigger.
   - Confirm it states what the skill does and when to use it.
   - Flag descriptions that are too broad, too clever, or missing concrete scenarios.

3. Check execution quality.
   - Confirm the skill defines when to use, inputs, workflow, output format, quality checks, and failure boundaries.
   - Look for steps that require hidden author knowledge.
   - Identify where examples, scripts, references, or assets would reduce repeated work.

4. Check output contract.
   - Confirm the output format is specific enough for another agent to follow.
   - Confirm the output can be evaluated.
   - Flag outputs that are just "provide advice" or "write a good result".

5. Check safety and boundaries.
   - Look for unsupported claims, current product facts without verification, data privacy risks, and high-stakes advice.
   - Confirm the skill knows when to ask for missing inputs or stop.

6. Create or update eval cases.
   - Add one easy case, one normal case, and one edge case.
   - Include pass criteria for each case.
   - Tie evals to observable artifacts.

## Output Format

Return Markdown with this structure:

```markdown
## Skill Self-Test Report

- Skill:
- Path:
- Stage:
- Overall status: Pass / Needs revision / Blocked

## Findings

| Severity | Area | Finding | Recommendation |
| --- | --- | --- | --- |

## Required Fixes

- <specific change>

## Suggested Improvements

- <specific improvement>

## Eval Cases

### Easy

- Request:
- Expected output:
- Pass criteria:

### Normal

- Request:
- Expected output:
- Pass criteria:

### Edge

- Request:
- Expected output:
- Pass criteria:

## Release Recommendation

<publish, test privately, revise, or block with reason>
```

Use direct, file-specific findings when reviewing a repository. Prefer concrete edits over broad writing advice.

## Quality Checks

- The report identifies blocking issues before minor style issues.
- Every finding includes a recommendation.
- The review checks trigger behavior, not only Markdown formatting.
- Eval cases are realistic and connected to the skill's intended users.
- The release recommendation matches the severity of findings.
- The review does not demand scripts or assets when the skill is intentionally documentation-first.

## Failure Boundaries

- Do not certify a skill as safe, correct, or production-ready without real task runs.
- Do not rewrite the skill automatically unless the user asked for edits.
- Do not ignore missing source material, private data constraints, or high-stakes domains.
- Do not treat subjective style preferences as blockers.
- If the skill depends on external tools or current product behavior, require verification from authoritative sources.

# Eval Cases Template

Use this template to create lightweight evaluation cases for a SkillCraft skill. Each skill should have at least one easy case, one normal case, and one edge case.

## Skill Under Test

- Skill:
- Version or commit:
- Reviewer:
- Date:
- Source files:

## Eval Case: Easy

- Request:
- Required inputs:
- Expected output:
- Pass criteria:
- Common failure:
- Notes:

## Eval Case: Normal

- Request:
- Required inputs:
- Expected output:
- Pass criteria:
- Common failure:
- Notes:

## Eval Case: Edge

- Request:
- Required inputs:
- Expected output:
- Pass criteria:
- Common failure:
- Notes:

## Scoring

Use this simple score for each case:

| Score | Meaning |
| --- | --- |
| 0 | Fails the core task or invents critical information. |
| 1 | Produces a partial artifact but misses required structure or important constraints. |
| 2 | Produces a usable artifact with minor gaps. |
| 3 | Produces a strong artifact that satisfies structure, quality checks, and boundaries. |

## Decision Rule

- Publish: all normal and easy cases score 3, edge case scores at least 2, and no boundary violations occur.
- Revise: any case scores 1 or 2 with fixable issues.
- Block: any case scores 0, leaks private data, invents facts, or violates a stated boundary.

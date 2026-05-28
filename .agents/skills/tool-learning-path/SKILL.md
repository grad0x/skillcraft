---
name: tool-learning-path
description: Design practical learning paths for AI tools, developer tools, creative tools, or repeatable workflows by converting documentation, tutorials, and user goals into modules, exercises, checkpoints, and self-tests. Use when Chinese AI learners, technical writers, teams, or skill authors need a structured path for learning a tool through hands-on tasks instead of passive prompt collections.
---

# Tool Learning Path

## When To Use

Use this skill when the user wants to learn, teach, or package an AI tool or workflow as a structured path.

Good fits:

- "Help me learn this AI coding tool in 7 days."
- "Turn this documentation into a course outline for creators."
- "Create a learning path for using an agent skill system."
- "Design exercises so a team can prove they know the tool."

Do not use this skill for simple feature summaries, untested tool recommendations, or motivational study plans with no practice loop.

## Inputs

Ask for or infer these inputs:

- Tool or workflow name.
- Source material: official docs, tutorial notes, screenshots described by the user, internal SOP, or pasted excerpts.
- Learner profile: beginner, working creator, technical writer, developer, team lead, or trainer.
- Desired outcome: publish content, build a workflow, automate a task, evaluate a tool, or train a team.
- Time budget: one hour, one day, seven days, four weeks, or custom.
- Environment constraints: account access, paid features, local setup, platform limits, language preference.
- Proof standard: what learners must produce to show competence.

If current product details matter, verify them from official sources or mark them as assumptions.

## Workflow

1. Define the learning outcome.
   - Convert "learn the tool" into observable work, such as "publish a tested card workflow" or "run an agent task with review notes".
   - State what the learner should be able to do without assistance.

2. Map the skill ladder.
   - Identify prerequisite concepts.
   - Order capabilities from recognition to guided use to independent production.
   - Separate core operations from advanced or optional features.

3. Build modules around tasks.
   - Give each module a concrete deliverable.
   - Include a short concept brief, a hands-on task, and a review checkpoint.
   - Prefer realistic creator or developer work over toy examples.

4. Add practice cases.
   - Include at least one easy case, one normal case, and one edge case.
   - Make each case checkable by a reviewer or another agent.
   - Include Chinese creator scenarios when relevant, for example converting a dense tool update into a 小红书 teaching post.

5. Define verification.
   - Specify what a good artifact looks like.
   - Include failure signs and remediation steps.
   - Add a final capstone that combines multiple skills.

6. Package the path.
   - Use a time-boxed schedule only if the user asked for one.
   - Include source links or source names when available.
   - Separate required work from optional exploration.

## Output Format

Return Markdown with this structure:

```markdown
## Learning Path Brief

- Tool or workflow:
- Learner:
- Outcome:
- Time budget:
- Proof standard:

## Path Overview

| Module | Goal | Deliverable | Checkpoint |
| --- | --- | --- | --- |

## Modules

### Module 1: <name>

- Concept:
- Task:
- Output:
- Checkpoint:
- Common failure:
- Remediation:

## Practice Cases

- Easy:
- Normal:
- Edge:

## Final Capstone

- Scenario:
- Required artifact:
- Pass criteria:

## Assumptions And Sources

- <source or assumption>
```

Use Chinese for learner-facing module text when the user is targeting Chinese learners. Keep technical command names, product names, and API terms in their original language unless a standard translation exists.

## Quality Checks

- The path leads to a visible artifact, not only conceptual understanding.
- Each module has one learning goal and one deliverable.
- Exercises use realistic work that matches the target learner.
- Checkpoints are observable and can be evaluated without reading the author's mind.
- Current product details are sourced, verified, or explicitly marked as assumptions.
- The path avoids "watch, read, remember" as the main activity; learners must practice.

## Failure Boundaries

- Do not invent tool features, pricing, availability, model names, or policy details.
- Do not require paid access, credentials, private datasets, or unsafe automation unless the user confirms those constraints.
- Do not present a learning path as complete if the source material is missing key setup or usage details.
- Do not design exercises that encourage bypassing platform policies, scraping protected content, or mishandling user data.
- If the learner goal is too broad, narrow it into one outcome and state what is out of scope.

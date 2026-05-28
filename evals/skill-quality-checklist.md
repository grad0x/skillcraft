# Skill Quality Checklist

Use this checklist before publishing or updating a SkillCraft skill.

## Required Structure

- [ ] The skill lives at `.agents/skills/<skill-name>/SKILL.md`.
- [ ] The folder name uses lowercase letters, numbers, and hyphens.
- [ ] YAML frontmatter exists.
- [ ] Frontmatter includes `name`.
- [ ] Frontmatter includes `description`.
- [ ] `name` matches the folder name.
- [ ] The description states what the skill does and when to use it.
- [ ] The body is not placeholder-only.

## Execution Contract

- [ ] The skill defines when to use it.
- [ ] The skill defines required or inferable inputs.
- [ ] The workflow is step-by-step and action-oriented.
- [ ] The output format is explicit enough for another agent to follow.
- [ ] Quality checks are observable.
- [ ] Failure boundaries tell the agent when to stop, ask, or narrow scope.

## Reusability

- [ ] The skill solves a repeatable task, not a one-off content request.
- [ ] The skill avoids generic prompt-library language.
- [ ] The workflow can be tested with realistic examples.
- [ ] Domain-specific assumptions are stated.
- [ ] Optional resources such as `references/`, `assets/`, or `scripts/` are only added when they reduce repeated work.

## Trigger Quality

- [ ] The description includes concrete scenarios.
- [ ] The description names important artifact types or user intents.
- [ ] The skill is narrow enough that another agent can choose it confidently.
- [ ] Nearby non-use cases are named in the body.

## Safety And Boundaries

- [ ] The skill does not encourage inventing facts, sources, metrics, or testimonials.
- [ ] The skill handles private or sensitive data explicitly when relevant.
- [ ] The skill marks current product behavior as needing verification when necessary.
- [ ] The skill avoids high-stakes advice unless expert review is required.

## Release Decision

Use this decision rule:

- Publish if all required structure items pass and no boundary issues exist.
- Revise if the output contract, examples, or trigger description are weak.
- Block if the skill cannot be executed from the provided instructions or encourages unsupported claims.

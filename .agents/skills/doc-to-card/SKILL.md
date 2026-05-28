---
name: doc-to-card
description: Convert source documents, articles, tutorials, notes, or tool documentation into structured educational card content for Chinese AI creators, technical writers, and bilingual developer audiences. Use when a user wants to transform dense material into publishable multi-card posts, carousel drafts, WeChat sections, 小红书 notes, or internal knowledge cards while preserving evidence and avoiding prompt-library style shortcuts.
---

# Doc To Card

## When To Use

Use this skill when the user provides a source document or source excerpt and wants a reusable content workflow that turns it into card-based educational content.

Good fits:

- A tool document that should become a beginner-friendly card series.
- A technical article that should become a WeChat or 小红书 explainer.
- A workflow note that should become a reusable carousel, slide outline, or knowledge base card.
- A bilingual content draft where Chinese-facing wording matters but developers still need accurate technical framing.

Do not use this skill for unsourced motivational posts, generic viral hooks, or content that only needs copy polishing.

## Inputs

Ask for or infer these inputs:

- Source material: pasted text, file path, URL excerpt, notes, or a clear summary supplied by the user.
- Target audience: Chinese AI creator, technical writer, AI tool learner, developer, founder, team lead, or another named group.
- Channel: 小红书, WeChat article, LinkedIn carousel, internal wiki, slide deck, or generic card set.
- Goal: teach, compare, launch, summarize, onboard, review, or persuade.
- Constraints: card count, language, tone, source citation expectations, visual style, and claims to avoid.

If the source is missing or too vague, ask for the source before drafting. If a URL is supplied but content is unavailable, state that the output can only be based on accessible or user-provided text.

## Workflow

1. Identify the source contract.
   - Name the source, author or product if known, date if available, and confidence level.
   - Separate source facts from interpretation.
   - Mark claims that need verification instead of presenting them as facts.

2. Extract the content spine.
   - Find the core idea, audience problem, required background, key steps, examples, and limitations.
   - Remove repeated framing, marketing filler, and unsupported claims.
   - Keep technical terms accurate; add Chinese explanations only when they reduce ambiguity.

3. Choose the card architecture.
   - For tutorials, use: problem -> mental model -> steps -> example -> checklist -> next action.
   - For tool docs, use: what it is -> when to use -> setup -> workflow -> pitfalls -> practice task.
   - For opinion pieces, use: thesis -> evidence -> implication -> counterpoint -> action.
   - For skill workflows, use: trigger -> inputs -> workflow -> output -> checks -> failure boundary.

4. Draft the card set.
   - Give every card one job.
   - Use specific nouns and verbs instead of broad advice.
   - Keep hooks tied to the source, not to exaggerated results.
   - Include bilingual terms when useful, for example "evaluation case / 评测用例".

5. Add evidence and production notes.
   - List source-backed claims separately from editorial interpretation.
   - Add suggested visuals only as production guidance, not as required assets.
   - Include a caption, call to action, and optional title variants.

6. Run a quality pass.
   - Check whether a reader could reconstruct the source logic from the cards.
   - Remove claims that sound useful but are not grounded in the input.
   - Tighten card titles so they preview the value of each card.

## Output Format

Return Markdown with this structure:

```markdown
## Content Brief

- Source:
- Audience:
- Channel:
- Goal:
- Angle:

## Card Draft

### Card 1: <title>

- Main point:
- Body copy:
- Visual direction:
- Evidence note:

### Card 2: <title>

...

## Caption

<publishable caption or post intro>

## Source-Backed Claims

- <claim> -> <source detail>

## Editorial Assumptions

- <assumption and why it was needed>

## Quality Check

- <pass/fail notes>
```

For Chinese channels, write publishable card copy in Chinese unless the user asks for English. Keep technical labels bilingual when they help developer readers.

## Quality Checks

- Every card has one clear purpose and does not duplicate another card.
- The final draft distinguishes source facts, interpretation, and assumptions.
- The card sequence teaches a workflow or concept rather than listing disconnected tips.
- The wording is concrete enough to be reused by a designer, editor, or another agent.
- Claims about tools, pricing, models, policies, or current product behavior are verified or clearly marked as needing verification.
- The output avoids generic prompt-library phrasing such as "copy this prompt to 10x your productivity" unless the source explicitly supports that framing.

## Failure Boundaries

- Do not invent source details, metrics, quotes, dates, or product capabilities.
- Do not summarize copyrighted long-form text by reproducing large passages verbatim.
- Do not create medical, legal, financial, or safety-critical guidance without domain review.
- Stop and ask for clarification if audience, source, or channel constraints materially change the output.
- If the source is too thin for a card set, produce a short "not enough source material" report with the missing inputs needed.

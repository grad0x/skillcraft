# Example: Claude Code Doc To Card

This example shows how to use `doc-to-card` when a user provides a Claude Code documentation excerpt or tutorial note and wants to turn it into a Chinese creator-facing card post.

This file does not assume current Claude Code product details. Use only the source text supplied by the user or verified official documentation when running the example.

## User Request

```text
Use the doc-to-card skill to turn this Claude Code documentation excerpt into a six-card 小红书 post for AI tool learners. Keep technical terms accurate, explain the workflow in Chinese, and mark any assumptions.

[Paste source excerpt here.]
```

## Inputs

- Source: user-provided Claude Code documentation excerpt.
- Audience: Chinese AI tool learners who can read basic English technical terms.
- Channel: 小红书 carousel.
- Goal: help readers understand when to use the workflow and how to try it safely.
- Constraints: six cards, Chinese copy, no unsupported claims, include source-backed notes.

## Expected Skill Behavior

The skill should:

- Identify the source contract before drafting.
- Preserve product behavior exactly as described in the provided excerpt.
- Convert dense documentation into a clear card sequence.
- Use bilingual labels for important terms when useful.
- Mark assumptions if the source excerpt does not include setup, pricing, model, or access details.

The skill should not:

- Invent Claude Code features not present in the source.
- Promise productivity gains without evidence.
- Quote long passages from the documentation.
- Hide uncertainty about current product behavior.

## Suggested Card Architecture

1. What problem this workflow solves.
2. What the tool or feature does, based only on the source.
3. When to use it.
4. How to try it step by step.
5. Common mistakes or limits.
6. Practice task and next action.

## Review Checklist

- Every card has one job.
- Technical names remain accurate.
- Chinese explanations are clear without oversimplifying.
- Claims are traceable to the source excerpt.
- Assumptions are listed separately from facts.
- The final caption invites a concrete practice action.

## Example Evaluation Case

- Request: turn a 900-word tool documentation excerpt into a six-card 小红书 post.
- Expected output: content brief, six card drafts, caption, source-backed claims, editorial assumptions, quality check.
- Pass criteria: no invented product details, one idea per card, Chinese copy suitable for creators, and visible evidence notes.

# Official source map

Prefer live official OpenAI sources when current guidance matters.

## Primary sources

- GPT-6 Astra model guidance:
  https://developers.openai.com/api/docs/guides/latest-model
- Rethinking skills and prompts for GPT-6 Astra:
  https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra
- OpenAI skill creator guidance:
  https://github.com/openai/skills/blob/main/skills/.system/skill-creator/SKILL.md
- OpenAI Developers docs skill example:
  https://github.com/openai/openai-developers-for-claude/blob/main/plugins/openai-developers/skills/openai-docs/SKILL.md

OpenAI developer documentation pages can generally be requested in Markdown form by appending `.md` to the documentation URL when supported.

## Refresh rule

For current model facts, prompting recommendations, API behavior, limits, pricing, or feature availability:

1. Fetch the current official OpenAI documentation first when live docs access exists.
2. Treat the bundled files in this skill as durable workflow summaries, not as authority for time-sensitive facts.
3. If official pages conflict, report the conflict rather than silently choosing one.
4. If current official documentation cannot be verified, state the uncertainty instead of inventing or relying on stale model facts.

## Snapshot provenance

This skill was assembled from the official sources above as available on 2026-09-13. The summaries intentionally paraphrase and compress the guidance rather than mirroring the full documentation.

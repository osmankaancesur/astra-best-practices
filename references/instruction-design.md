# Skills and AGENTS.md design for Astra

Use this reference when creating or auditing persistent instructions.

## Skill descriptions

Keep each description short while making the trigger boundary precise. Describe the actual workflow the skill owns rather than a broad topic adjacent to it.

Bad pattern: trigger a specialized skill whenever any nearby concept appears.

Better pattern: trigger it only for the exact operation the skill is designed to perform.

Overlapping descriptions increase the chance that irrelevant instructions are loaded or that skills conflict.

## Progressive disclosure

Treat the root `SKILL.md` as a small router. Keep universal workflow guidance there and move specialized detail into references or scripts that are loaded only when needed.

Assume the model is capable. Include information that changes decisions, captures non-obvious constraints, or prevents real failure modes. Remove generic advice and historical scaffolding that no longer earns its context cost.

## AGENTS.md

Because `AGENTS.md` affects routine repository work, make its rules contextual rather than universal whenever possible.

Prefer:

- use an architecture document when changing service boundaries;
- use database documentation for schema work;
- use deployment documentation when preparing a deployment.

Avoid requiring all of those documents before every edit.

Safe local workflows can explicitly authorize the agent to proceed through routine test/fix/retest cycles without asking for approval at each step. Preserve approval gates for irreversible or consequential actions.

## Decision boundaries

Review old instructions written to restrain weaker or more impulsive models. Keep boundaries tied to actual risk. Remove blanket permission requirements that block safe, reversible work.

## Completion boundaries

Persistent instructions can state defaults, but task-specific prompts should define what “done” means when completion depends on the requested outcome. Avoid automatic stop-for-review gates unless review is genuinely required before further work.

## Instruction provenance and debugging

When a persistent instruction unexpectedly changes behavior, make the source of that behavior inspectable. If a skill or `AGENTS.md` rule causes the agent to pause, request confirmation, stop before the requested end state, or diverge from the user's intent, identify the exact written instruction responsible when it is available and briefly explain why it applies.

Do not blur together a written requirement and the model's own interpretation. This makes stale approval gates, overlapping skills, and accidental conflicts easier to remove without weakening legitimate safety or irreversible-action boundaries.

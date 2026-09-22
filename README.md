# GPT-6 Agent Execution Best Practices — v1.3

A concise skill for completing substantial GPT-6 agent tasks. It evolves **Astra Best Practices v1.2** while retaining its completion, autonomy, contextual loading, selective delegation, proportional verification, and instruction-provenance safeguards.

The core is shared across GPT-6 models. Documented Astra observations are optional background, not assumptions about Sol or Luna. This is an independent package informed by official OpenAI documentation, checked on **2026-09-22**; it is not an official OpenAI release.

## Use

Import this skill folder through your agent's supported skill installation workflow, preserving its relative paths. In Codex, invoke it by name:

```text
Use $gpt-6-agent-execution to finish the requested change.
Preserve the stated constraints and deliver the result with relevant verification.
```

Keep task-specific acceptance criteria in the actual request. The skill does not supply tools, change permissions, select a model, or guarantee identical behavior across models. If delegation tools are unavailable, execution continues directly. Read-only tasks remain read-only.

For an upgrade, replace the old `astra-best-practices` skill with this folder and update explicit invocations to `gpt-6-agent-execution`. Avoid enabling both as execution defaults. Preserve any local customizations deliberately; the names of installed-skill directories can be managed by the host.

## Package

| File | Purpose |
| --- | --- |
| [SKILL.md](SKILL.md) | Compact runtime workflow and reference router. |
| [Execution guidance](references/execution-guidance.md) | Optional operational edge cases. |
| [Model notes](references/model-notes.md) | Supported Astra observations and evidence limits. |
| [Source map](references/source-map.md) | Eight official sources, claim scope, and refresh rules. |
| [UI metadata](agents/openai.yaml) | Display name and invocation prompt. |
| [Release metadata](metadata.json) | Canonical name, version, provenance, and evaluation status; not runtime configuration. |
| [Changelog](CHANGELOG.md) | v1.3 changes and v1.2 preservation map. |
| [Evaluation notes](evals/README.md) | Small, optional behavioral comparison protocol and cases. |
| [Release audit](RELEASE-AUDIT.md) | Package checks performed and their limits. |

General prompt, skill, or `AGENTS.md` design/auditing belongs to the separate `gpt-skills/instruction-audit` skill. It is not a dependency here. This skill retains only the local explanation needed when a governing instruction affects execution.

## Evidence and evaluation

Official guidance, product mechanics, and package heuristics are separated in the references. No controlled Astra/Sol/Luna comparison has been run for v1.3, and no model-performance results are supplied. Use the optional cases with your own fixed environment before adopting model-specific adjustments. Evaluation material and release records are not prerequisites for routine skill use.

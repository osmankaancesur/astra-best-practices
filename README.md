# Astra Best Practices

A community-maintained skill for working effectively with GPT-6 Astra and ChatGPT Work, with a focus on completion boundaries, autonomy, context loading, delegation, verification, and instruction debugging.

> **Unofficial project.** This repository is not an OpenAI product and is not endorsed by OpenAI. It summarizes and operationalizes public guidance; for current model behavior and product details, prefer the official sources linked in `references/source-map.md`.

## What this skill does

`astra-best-practices` is intended for substantial Astra or Work workflows and for creating, auditing, or improving:

- Astra prompts
- agent skills
- `AGENTS.md` files
- persistent agent instructions
- multi-stage execution and verification workflows

The root `SKILL.md` stays intentionally compact. More specialized guidance is loaded progressively from `references/`.

## Install

Clone the repository into your agent skills directory:

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/osmankaancesur/astra-best-practices.git \
  ~/.agents/skills/astra-best-practices
```

To update an existing installation:

```bash
cd ~/.agents/skills/astra-best-practices
git pull
```

If your agent environment uses a different skills directory, place the repository there instead.

## Repository structure

```text
astra-best-practices/
├── SKILL.md
├── README.md
├── CHANGELOG.md
├── LICENSE
└── references/
    ├── astra-guidance.md
    ├── instruction-design.md
    └── source-map.md
```

## Versions

### v1.2 — 2026-09-18

Promotes instruction-provenance and debugging guidance into the root skill. When persistent instructions cause unexpected pauses, confirmation requests, early handoffs, or divergence from user intent, the skill now asks the agent to identify the exact written instruction responsible when available and distinguish it from the model's interpretation.

### v1.1 — 2026-09-13

Initial public baseline: outcome-focused execution, explicit completion boundaries, contextual document loading, safe autonomy, selective delegation, risk-calibrated verification, and progressive disclosure.

The `v1.1` branch preserves the v1.1 source snapshot. `main` tracks the latest version.

## Source philosophy

The bundled guidance is a concise operational summary, not a replacement for live documentation. For time-sensitive facts such as model behavior, API details, limits, pricing, or feature availability, check the current official OpenAI sources first.

See `references/source-map.md` for source links and refresh rules.

## Contributing

Issues and pull requests are welcome. Changes should stay narrow, evidence-based, and useful enough to justify their context cost. Avoid generic prompting advice, stale model assumptions, and rules that add unnecessary approval gates.

## License

MIT. See `LICENSE`.

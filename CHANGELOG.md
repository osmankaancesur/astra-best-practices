# Changelog

## 1.3 — 2026-09-22

- Rename `astra-best-practices` to `gpt-6-agent-execution`; expand the intended audience to GPT-6 while retaining the core ten-rule workflow.
- Consolidate the duplicated execution checklist into the core. Keep detailed decision examples in references.
- Separate shared execution defaults, official Astra observations, platform constraints, and package heuristics. Add no unsupported Sol/Luna behavioral recipe.
- Clarify missing information versus missing authorization, prepare permitted work before a required approval, and preserve actual approval/access boundaries.
- Add continuity checkpoints, pending-work handling, delegation ownership/integration, and bounded failure recovery.
- Make completion include delivery and relevant verification; recognize explicit stops, real blockers, required decisions, and enforced limits.
- Remove the general instruction-audit section and `references/instruction-design.md`. Keep instruction provenance only for explaining execution pauses or divergence.
- Replace `references/astra-guidance.md` with execution guidance and scoped model notes. Refresh `references/source-map.md` against current official pages.
- Add README, UI/release metadata, lightweight evaluation notes, and a release audit. These files were absent from the supplied archive.

### Preservation map

The source archive contained one core file and three references. This map accounts for its useful execution behavior and intentional scope removals.

| v1.2 behavior | v1.3 disposition |
| --- | --- |
| Infer intent and persist past the first plausible result | Core 1 and 9; completion includes requested delivery. |
| Keep instructions minimal; avoid unnecessary scaffolding | Core 2; applied to execution without unsolicited instruction rewriting. |
| Define multi-stage completion | Core 1 and 9; execution reference covers open-ended tasks. |
| Contextual document loading | Core 4; applicable instructions still must be read. |
| User priority, with system/safety/tool constraints | Core 3; developer and approval constraints made explicit. |
| Safe, reversible autonomy without routine permission loops | Core 5–6; execution reference separates clarification and approval. |
| Consider useful parallel work without mechanical delegation | Core 7; ownership, result integration, and environment limits added. |
| Focused verification; required checks; no repeated passing checks without reason | Core 8; execution reference preserves meaningful tests and stronger consequential-work checks. |
| Direct, proportionate final communication | Core 10; writing-style guidance retained in execution reference. |
| Explain the exact instruction behind pauses/divergence; distinguish interpretation | Core 10; preserve confidentiality for restricted instruction text. |
| Apply behavior to execution rather than returning a meta-prompt | Opening paragraph of core. |
| Do not manufacture clarification questions | Core 5; dependent work pauses only for material uncertainty. |
| Preserve project constraints, interfaces, fragile procedures, and irreversible gates | Core 2–3 and 6; these remain binding despite removal of the audit workflow. |
| Prefer current official sources; expose conflicts/unverified facts | Core reference router and source-map refresh rule. |
| Astra-specific tentative stopping, delegation, and testing observations | Scoped to official evidence in model notes; never relabeled as Sol/Luna traits. |
| Prompt-writing and broad skill/AGENTS.md audit workflows | Intentionally removed from triggers and runtime guidance; separate instruction-audit owns this scope. |
| Progressive disclosure | Three targeted references; evaluation and release documents load only for maintenance. |

## 1.2 — supplied baseline

Astra-specific skill with a core workflow, a second execution checklist, an instruction-audit workflow, and three references. Promoted instruction-provenance explanations into the core. The bundled source snapshot was dated 2026-09-18; the archive did not establish a separate v1.2 release date or evaluation history.

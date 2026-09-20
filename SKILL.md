---
name: astra-best-practices
description: Use for substantial GPT-6 Astra or ChatGPT Work workflows, and when creating, auditing, or improving Astra prompts, skills, AGENTS.md, and agent instructions. Apply when completion boundaries, autonomy, context loading, subagent delegation, testing/verification, or early-stopping behavior matter. Do not trigger for ordinary non-Astra questions.
---

# Astra Best Practices

Optimize instructions for GPT-6 Astra without overconstraining it.

## Core workflow

1. Infer the user's intended outcome from the task and conversation context. Bias toward carrying the task to completion instead of stopping at the first plausible result.
2. Keep instructions minimal. Remove guidance Astra can reliably infer on its own, repeated advice, generic reminders, and legacy scaffolding that does not change a decision.
3. Define completion explicitly when a task has multiple stages. State what must be implemented, inspected, fixed, validated, or delivered before the task is considered done.
4. Make document loading contextual. Point to a file only for the kind of work that actually needs it; do not require broad repo reading before every change.
5. Treat explicit user instructions as higher priority than this skill's workflow guidance. Preserve applicable system, safety, and tool constraints.
6. For safe, reversible workflows, avoid unnecessary permission checkpoints. Continue through routine local work unless a consequential or genuinely ambiguous decision requires user input.
7. Use subagents or parallel work when the environment supports them and parallelization is likely to improve speed or quality. Do not delegate mechanically when the overhead exceeds the benefit.
8. Calibrate verification to risk and scope. Run focused tests and required checks; broaden or repeat testing only when failures, changes, or unresolved risks justify it.
9. Keep final communication direct and proportionate to the task. Report what was completed, what was verified, and any material unresolved risk.
10. If this skill or another persistent instruction causes a pause, confirmation request, unfinished handoff, or divergence from the user's intended outcome, identify the exact instruction responsible when available and briefly explain why it applies. Distinguish the written instruction from the model's own interpretation.

## When executing work with Astra

Apply this skill to the work itself, not only to prompt writing. Do not rewrite the user's request into a meta-prompt unless they asked for a prompt. Instead:

- establish the intended end state and keep working until that state is reached or a real blocker is demonstrated;
- load only the files, docs, or tools that are relevant to the current branch of work;
- proceed autonomously through safe, reversible steps instead of pausing for routine confirmations;
- consider parallel or subagent work for genuinely independent streams when the environment supports it;
- verify results in proportion to risk, novelty, and scope rather than by rote repetition;
- distinguish completed work, verified claims, unresolved risks, and genuine blockers in the final response.

When the user asks for a prompt for Astra, encode these same principles in the prompt while keeping it outcome-focused and avoiding unnecessary scaffolding.

## When auditing prompts, skills, or AGENTS.md

Look specifically for:

- descriptions that trigger too broadly;
- multiple skills that overlap or contradict each other;
- instructions to read large sets of files before every task;
- elaborate step-by-step recipes that constrain reasonable judgment;
- repeated testing or verification requirements with no risk-based rationale;
- approval gates added for older models that unnecessarily stop Astra;
- missing completion criteria that encourage an early handoff;
- missing delegation guidance where parallel work would materially help;
- style instructions that cause bloated, repetitive, or overformatted answers;
- hidden or ambiguous instruction conflicts that cause unexpected pauses, confirmation requests, early handoffs, or divergence from the user's intent. When diagnosing one, point to the exact responsible instruction when available rather than attributing the behavior vaguely to the skill.

Prefer narrow, contextual replacements. Preserve instructions that encode real project constraints, safety boundaries, irreversible-action gates, exact interfaces, or fragile procedures.

## Progressive disclosure

Read only the reference that is relevant to the current task:

- For prompt behavior, persistence, delegation, and testing: `references/astra-guidance.md`.
- For skill and AGENTS.md design: `references/instruction-design.md`.
- For current official sources and refresh rules: `references/source-map.md`.

If live official OpenAI documentation is available, prefer it over bundled summaries for current model behavior, limits, or recommendations. Do not invent current facts when the live source cannot be verified.

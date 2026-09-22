# Official source map

Version 1.3. Sources opened and relevant text checked on **2026-09-22 (UTC)**. This package is an independent synthesis, not an official OpenAI skill. Summaries paraphrase sources; links point to maintained pages rather than copied documentation.

## Sources and claim boundaries

| ID | Official OpenAI source | Supported use in this package |
| --- | --- | --- |
| S1 | [Model guidance — Using GPT-6](https://developers.openai.com/api/docs/guides/latest-model), “Prompting best practices” | Family starting-point prompts with an explicit Astra-observation caveat; initiative, instruction priority, pause explanations, delegation tuning, and proportionate checks. Does not establish identical model tendencies. |
| S2 | [Rethinking skills and prompts for GPT-6 Astra](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra), 2026-09-11 | Compact contextual guidance, preserved workflow constraints, and explicit completion. Model observations remain scoped to Astra. Its general instruction-audit workflow is deliberately outside this package. |
| S3 | [Prompting](https://learn.chatgpt.com/docs/prompting), “Describe the result you need,” “Add useful context,” and “Fix a bug” | Outcome-first requests, relevant sources and constraints, and focused reproduction/checks. Product workflow guidance, not a GPT-6 model comparison. |
| S4 | [Subagents](https://learn.chatgpt.com/docs/agent-configuration/subagents), “Availability,” “Triggering subagent workflows,” and “Approvals and sandbox controls” | Delegation depends on the surface and applicable instructions; independent work can benefit, while token cost and simultaneous writes require care. Actual tool and permission settings govern. |
| S5 | [Agent approvals & security](https://learn.chatgpt.com/docs/agent-approvals-security), “Sandbox and approvals” | Technical access and approval policy are separate controls. Execution prompts cannot override either. |
| S6 | [Long-running work](https://learn.chatgpt.com/docs/long-running-work), “Define what done means” | Explicit outcomes, constraints, and verification criteria; continuity for related work and caution around concurrent writes. |
| S7 | [Compaction](https://developers.openai.com/api/docs/guides/compaction), “Overview” and “Server-side compaction” | Runtime mechanisms reduce context while carrying state forward. The package's human-readable checkpoint is a heuristic, not an API requirement or replacement for opaque compaction items. |
| S8 | [Evaluation best practices](https://developers.openai.com/api/docs/guides/evaluation-best-practices), “Evals tips” and “Anti-patterns” | Task-specific evaluations, traces, explicit criteria, and human calibration. Used for methodology only; no dependency on the Evals platform or its availability. |

## Official guidance, heuristics, and empirical evidence

- **Official:** The scoped recommendations above. S1 invites trying its prompts across GPT-6; it does not report cross-model validation of this skill.
- **Package heuristics:** The core's operational synthesis, the clarification/approval decision table, checkpoint contents, ownership conventions, blocker taxonomy, retry/stopping rules, and evaluation scenarios. These preserve or extend v1.2 safeguards; they are not represented as verbatim OpenAI requirements.
- **Empirical:** Only recorded runs qualify. No controlled cross-model results or inferred Sol/Luna behavior claims are bundled. Release structure checks must not be reported as model-performance evidence.

## Refresh rule

For changing model behavior, tool availability, API compatibility, or platform policy, fetch the relevant current official page. Check the page's selected model and section: `latest-model` is mutable, and older model sections are not evidence about GPT-6.

Keep the smallest supported change. Record the date and scope of a model-specific claim. If official sources conflict, expose the conflict and avoid the disputed claim; do not silently generalize. If live documentation is unavailable, say what could not be verified rather than inventing current facts. Routine execution does not require rereading this entire source list.

## v1.2 continuity

The attached v1.2 archive is the editing baseline. Its source snapshot was dated 2026-09-18. S1 and S2 are retained and refreshed; the two skill-authoring repository links are removed from active guidance because instruction authoring/auditing no longer belongs to this skill. No historical v1.2 test results are assumed.

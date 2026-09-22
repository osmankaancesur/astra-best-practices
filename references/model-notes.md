# Model notes

Documentation checked: 2026-09-22. These are scoped source summaries, not comparative evaluation results.

## Official guidance and its scope

OpenAI's [Using GPT-6 guide](https://developers.openai.com/api/docs/guides/latest-model) presents its prompting examples as starting points for the GPT-6 family, while explicitly saying the underlying behavior observations concern Astra and require evaluation on the chosen model and workload.

For **GPT-6 Astra**, that guide documents possible clarification pauses, less delegation than a workflow wants, and excessive testing breadth on small coding tasks. The [Astra article](https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra) also describes tentative stopping after an initial implementation. These motivate explicit completion and calibrated verification, not blanket suppression of questions or tests.

The article's comparison to **GPT-5.6 Sol** is not evidence about **GPT-6 Sol**. It also cautions that instructions suitable for Sol or Luna may overconstrain Astra; it does not establish a task-independent recipe for those models.

## Application rule

Use the shared core first. Add a model-specific adjustment only when current official guidance or reproducible, workload-matched evidence supports it. Keep the model, date, environment, and evidence scope attached to the adjustment.

No Sol- or Luna-specific clarification, autonomy, delegation-frequency, or verification recipe is included in v1.3. This omission is not a claim that their behavior is identical or that no differences exist. Model rankings, prices, reasoning defaults, and API compatibility tables are outside this execution skill.

Distinguish platform behavior from model behavior: tools, approval policy, intelligence settings, and delegation permissions come from the actual environment. Do not infer them from a model name. Consult the current [subagent documentation](https://learn.chatgpt.com/docs/agent-configuration/subagents) when configuring those features.

## Empirical status

No controlled cross-model evaluation results are claimed for this release. The optional evaluation material provides a comparison protocol, not a leaderboard. A single successful run, especially under different harness instructions, cannot establish a family-wide behavior claim.

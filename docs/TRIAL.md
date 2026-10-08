# Compare workflow approaches

Human reference, not default agent input. Evaluate whether independent concept exploration, coherent synthesis, and resolved assignments improve useful detail at acceptable coordination cost. No quality or cost improvement has been measured in this template.

## Prepare comparable runs

Use separate clean destination repositories or checkouts from the same game starter. Choose one workflow as the control and another as the candidate; record their exact versions in the trial's own records. Keep generated project state, worker history, editor caches, and build outputs separate; do not carry one run's designs into the other. Leave this reusable template's `project/` uninitialized.

Use the same prompt when possible. Similar prompts are useful exploration but weaken attribution to the workflow. Keep engine/assets, tool access, coordinator model, worker bindings, time/token budget if available, and product constraints comparable. Record differences and unavailable measurements. Resolve necessary user questions consistently across runs; avoid tuning the candidate's prompt after seeing the control result.

Before starting, choose a short shared assessment rubric from the request: defining behaviors and interactions, expected feedback/content depth, scope, and the executable scenarios or play observations needed. Apply it to both outputs; retain additional worthwhile discoveries as separate observations. Give both runs the same user-visible finish condition. If a run cannot complete within the allotted effort, assess the actual deliverable and remaining work.

An example prompt to adapt identically for both runs:

> Build a small action RPG using the supplied starter and assets. Include readable enemy attacks, loot pickup, inspectable equipment with meaningful tradeoffs, and enemies that require different responses. Define one playable fight–reward–equip loop and build it within the stated budget. Report implemented detail, simplifications, unverified claims, and remaining scope. Follow the repository workflow.

## Assess quality and overhead separately

| Dimension | What to record for each run |
| --- | --- |
| Exploration depth | Materially different concepts, concrete player sequences, discriminating questions, and evidence behind pruning; idea count alone proves nothing |
| Synthesis quality | Source-traced contributions, rejected incompatibilities, resolved contracts, and full-feature behavior/failure scenarios before readiness |
| Requested detail | Rubric outcomes present, omitted, simplified, or unverified; concrete examples |
| Combined behavior | Results of the same scenarios, integration defects, and recovery/failure cases |
| Experience | Observed readability, responsiveness, meaningful choices, and variety; identify evaluator/build/input |
| Scope honesty | Reported completion versus actual requested coverage and evidence |
| Coordination | Time to first playable result, total effort, models/tokens/cost if observable, worker attempts/escalations |
| Process burden | Records actually read or used, duplication, repeated questions, blocked work, and avoidable handoffs |

Evaluate runnable outputs with the same scenarios and setup. Inspect docs only to explain behavior or process; more specifications or checked boxes do not establish a better game. Unknown feel remains unknown without observed play. Blind labels or a second evaluator can reduce preference bias when practical.

One comparison supplies feedback, not a general reliability claim. If results matter, repeat with another comparable prompt/run, including a clear local fix to check whether the candidate adds unnecessary ceremony. Keep model/runtime differences visible.

## Capture actionable feedback

Store trial records with the actual trial project or outside this template. For each issue, capture the run/build, observed result, relevant workflow step or assignment, concrete evidence, suspected cause, and one proposed change. Mark causation as a hypothesis until checked.

Ask whether independent concepts exposed a meaningful alternative, deeper branches resolved decisions, synthesis preserved coherent interactions, packets contained enough context, and any record lacked a consumer. Check whether siblings saw favored solutions too early or work limits concealed incomplete design. Compare useful detail with effort before retaining the process. Narrow activation or remove duplicated fields when overhead adds no demonstrated value. Keep unresolved product work visible while simplifying coordination.

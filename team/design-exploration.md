# Branching feature exploration

Audience: coordinator or designer managing/synthesizing exploration. Other branch workers receive scoped packets and [the branch form](templates/design-branch.md); they need not load this full guide. Activate before choosing a design for a new, nontrivial feature, when an accepted design loses its assumptions, or when the user requests exploration. A clear change within an accepted contract skips this flow. Pair it with [decomposition](design-decomposition.md): explore plausible approaches, then specify the complete agreed feature and sequence implementation.

Branches are Markdown proposals under one task. Use existing designer, scout, partner, and reviewer roles; no permanent role or Git branch per idea. During template maintenance, keep all generated records outside the repository.

## 1. Establish a neutral root brief

Record desired player outcomes and coverage IDs, scope, hard constraints, known evidence, assumptions, open questions, and success/failure examples. Describe the problem before naming a mechanism. A requested mechanism remains a constraint; explore meaningful choices within it rather than disregarding the user.

Choose comparison criteria before reading proposals: outcome coverage, meaningful player choices, clarity/accessibility, interaction risks, feasible production scope, and uncertainty as relevant. Distinguish required constraints from preferences. Give the brief a revision ID; freeze the common starting facts for the round.

Default budget: three concept assignments; shortlist at most two concepts; at most two focused children per survivor, one expansion layer; one independent synthesis challenge. That is at most eight design assignments and three concurrent workers, lowered to host limits. Use fewer when sufficient. Partner consultations, delegated synthesis, and reconciliation also consume this cap. Record exceptions and their expected decision value before dispatch. Budget limits bound exploration, not requested feature scope or acceptance.

## 2. Explore concepts independently

Give each fresh designer the same root brief, criteria, evidence, and return contract. Withhold coordinator preferences, sibling proposals, and prior solution conversations. Assign contrasting questions or design lenses, not prescribed answers; include a simple/existing-behavior alternative where credible. Differences must change player choices, rules, incentives, or meaningful tradeoffs, not just names or presentation.

Each proposal uses [the branch form](templates/design-branch.md): a concrete player sequence, rules/state/feedback, failures and recovery, dependencies, production implications, assumptions, strongest objection, and a check that could disprove it. A slogan is not a completed concept. Initial branches may inspect packet-approved factual sources; they do not read sibling design records. A tool-free partner can question the neutral framing without replacing these developed proposals.

Persist returns before comparison. Do not promote the first response. Account for every assigned proposal: compare completed branches, replace a failed/missing one within the budget, or explicitly record reduced coverage and its consequences. Require at least two genuinely independent concepts when the runtime and problem permit. If concepts converge, check for an anchored brief or binding constraints; do not manufacture differences unsupported by the problem.

## 3. Compare, then deepen selected uncertainties

Use one compact matrix against the original criteria. Separate evidence, predictions, and unknowns. Reject hard-constraint failures; explain consequential tradeoffs and why each branch advances or stops. Neither votes, confident prose, nor document length establish quality. Do not reject an underexplored option as infeasible without evidence.

Keep up to two plausible parents provisional. Create a child only when its answer could change the concept, an interaction contract, or a consequential risk. Label it **competing variant** (alternatives to choose between) or **complementary facet** (details that must work together). Splitting one favored idea into departments does not replace independent concept exploration.

Give children only root intent, relevant parent contracts/revisions, the unresolved question, dependencies, criteria, and scope. Require concrete input/output semantics, state/timing ownership, feedback, boundary cases, and a discriminating scenario as applicable. Children propose parent changes explicitly; they cannot silently redefine sibling assumptions. Only the coordinator dispatches children. Parallelize independent questions; run dependent ones in order. Stop a branch when its question is answered, evidence rules it out, or a named dependency blocks it.

## 4. Exchange discoveries without erasing alternatives

After independent proposals are saved, share concise transferable findings: new constraints, useful mechanisms, contradictions, or falsifying checks. Send only relevant discoveries, with source IDs, to affected branches. Keep their original proposal identifiable and record revisions as deltas. A revised concept is informed by peers; do not describe that revision as independently generated.

A new root fact or parent-contract revision marks dependent branches and comparisons as needing recheck. Reconcile them before synthesis; independent siblings unaffected by the change retain their evidence. Reassignments get new attempt IDs, preserving the previous result. Reconciliation consumes remaining budget or requires a recorded budget adjustment.

## 5. Synthesize one coherent feature

The coordinator or an exclusively assigned synthesizer owns [the canonical design](templates/design.md). Select a primary concept using the comparison evidence. Adopt, adapt, or reject discoveries from other branches with source IDs and short reasons; retain unresolved disagreements. Combining is optional, not a requirement to keep something from every branch.

For every imported element, resolve compatibility of rules, resource costs, incentives, pacing, feedback, lifecycle, and shared interfaces. Walk a combined normal scenario plus relevant failure/recovery and cross-system cases. If the mixture changes the primary concept, update its contracts and comparison rather than presenting it as an unchanged winner.

Specify behavior and interactions across the **whole agreed feature**, including defining content variation, boundary cases, provisional tuning and units, dependency ownership, and acceptance scenarios. Broader project ideas outside that feature remain visible as later scope. Only code-level breakdown and executable assignments may be limited to the next delivery slice. More detail means resolved decisions, not longer descriptions.

## 6. Challenge and check readiness

A fresh reviewer receives root intent, criteria, the synthesized specification, scenario walkthroughs, and evidence before selection advocacy. Check missing outcomes, contradictory contracts, unhandled failures, and weakened player choices. Resolve findings or keep the affected design open; this challenge is part of the default budget. A walkthrough establishes design consistency, not observed game feel, performance, or implemented behavior.

Design is ready to implement when each agreed outcome has explicit rules and acceptance, interacting contracts agree, material objections are addressed, and the builder can proceed without inventing consequential product behavior. Remaining tuning hypotheses or implementation choices need boundaries and validation plans. Missing required product decisions or feasibility evidence prevents readiness; explicitly scoped experiments may proceed with their hypothesis and rollback.

At the budget limit, report unresolved choices, consequences, and the smallest next experiment or decision. Extend only for a named material question within existing authority; ask the user when a consequential requirement or scope decision needs their input. Never mark an incomplete design ready just because the budget expired. No-subagent work uses labeled sequential self-analysis; serial fresh agents can preserve independence when only parallelism is unavailable.

## Records and context

The canonical design holds the root brief, comparison/disposition links, synthesis, and open decisions. Each proposal lives at `project/tasks/<task-id>/design/<branch-id>.md` and **is its assignment handoff**; point the task's existing Handoff column there instead of creating a duplicate report. The task alone owns scheduling/status; branch `ready` means returned for evaluation, not selected or approved.

One writer per branch file; one for the synthesis. Workers load only their packet, role, relevant sources, and applicable parent excerpts. They return a short conclusion with artifact pointers; the synthesizer reads decision-relevant branch detail. On resume, check brief/contract revisions and unresolved assignments before relying on proposals. Archive branch artifacts with the task and repair synthesis links; builders normally receive only the accepted design excerpts and interfaces.

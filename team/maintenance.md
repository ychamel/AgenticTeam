# Context maintenance

Audience: coordinator and assigned curator. Maintenance is triggered by work, not a background service.

When maintaining the reusable template itself, follow [the baseline-editing rule](../AGENTS.md#editing-the-baseline). Leave project identity and runtime bindings uninitialized, indexes empty, and counters at zero. Keep that work's task/handoff records outside the template; do not ship local paths, session identities, or execution history. The project lifecycle below applies after adoption.

## Stable and changeable layers

`team/foundation.md` is immutable during ordinary tasks. Root routing and `team/` processes, roles, and templates are versioned baseline material. Put project facts, command choices, model bindings, and local conventions in `project/`. Do not solve local exceptions by quietly weakening a general rule.

An explicit request to revise this baseline authorizes foundation edits. Record the reason and compatibility impact, review the affected rules, increment its version, and update [design notes](../docs/DESIGN.md). Routine curators can propose such a revision but cannot make it incidental to cleanup. This is a workflow convention; filesystem enforcement or protected branches are optional host controls.

## Triggers and bounds

At task close, the coordinator performs a small pass on touched records. Perform a wider curator pass after five completed standard/consequential tasks, when an active index becomes hard to scan, when a source contradicts its context note, or on request. Increment the completion count in [WORK](../project/WORK.md) for each such task closed; after a wider pass finishes, record its date and reset the count. A long idle interval triggers freshness checks on resumed work, not an automatic whole-repo rewrite.

Starting size targets (soft limits, not correctness limits): root entry under 400 words; foundation under 500; role under 250; project brief under 350; area note under 500; task under 800; ordinary handoff under 350; design-branch artifact under 500. Feature specifications may exceed summary targets when necessary to resolve behavior and contracts. Keep indexes one row per item, aiming for at most 20 active rows. Group a larger legitimate workload by area with linked subindexes; never discard unresolved work to hit a limit. Move detail only when it has a clear consumer. Measure words/bytes as proxies; exact token counts depend on the model.

## Closeout pass

1. Compare claims in touched notes with source, checks, and current decisions. Repair contradictions or explicitly mark unknown; do not refresh dates without checking the claims.
2. Promote reusable constraints and verified facts to their canonical homes. Link to them from the task instead of keeping several copies. An accepted decision records why; an area note records the current contract and points to that decision.
3. Preserve unresolved issues with owner, evidence, and next action in WORK or an active task. If work is tracked externally, retain a pointer and enough local context to resume; avoid a second competing backlog.
4. Mark the task done or cancelled only with its outcome and evidence intact. Move its entire directory, including handoffs, to `project/archive/YYYY/<task-id>/`. Create that directory on demand, repair incoming and outgoing links, and remove its active row. Never move a task while any worker owns a live assignment.

For later work arising from an archived task, create a new active task linking back to it. Do not resume writes into the old task ID or recreate only its handoffs under the active tree.

## Wider pass

Search targeted records for broken links, duplicate rules, obsolete commands, accepted decisions missing from area context, stale ownership, unintegrated handoffs, and active items with no next step. Review only the implicated sources. Deduplicate by choosing a canonical home and replacing other copies with links. Keep the reason for constraints that prevent repeated mistakes.

For game projects, recheck affected engine/plugin versions, import/build recipes, renamed scene or asset references, save/network contracts, and profiling/playtest evidence after relevant changes. Keep design hypotheses visibly unverified until observed evidence supports them; do not preserve obsolete tuning conclusions as permanent rules.

When design coverage is active, check affected IDs, accepted deviations, later scope, and evidence links against current design and implementation. Invalidate changed outcomes rather than preserving a stale verified status. Preserve unresolved requested work; consolidate duplicate specifications and link canonical contracts. Do not create design records for projects that do not need them.

Keep exploration comparisons and source IDs compact in the canonical design. Archive proposals with their owning task only after synthesis or explicit rejection, transfer unresolved decisions to an active owner, and repair incoming links. Preserve decision-relevant alternatives and contradictions without copying branch narratives into active context. Changed root facts or parent contracts require rechecking dependent proposals and design readiness; unrelated branches need not be reread.

Archive superseded decisions while retaining their status and replacement pointer in [DECISIONS](../project/DECISIONS.md). Accepted decisions remain addressable for as long as they constrain work. Archives are searchable by task ID or topic on demand and excluded from default reads; do not maintain a second narrative archive index.

Delete disposable logs, abandoned scratch notes, and duplicate summaries only after confirming no needed evidence or unresolved obligation lives there. Do not silently delete historical decision records or task outcomes; storage is cheaper than rediscovery. Without recoverable version history, retain original records while pruning active summaries. Report what changed, what evidence was checked, and what remains uncertain in the current task handoff; do not create an unbounded maintenance journal.

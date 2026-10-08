# Design decomposition

Audience: coordinator and assigned game designer. Activate for broad game requests, interacting new systems, or missing detail that threatens the intended experience. Skip this guide and its record for clear local changes governed by existing contracts. This adds no required role or separate task per layer.

When a feature has no accepted design, use [branching exploration](design-exploration.md) before selecting an approach. Preserve requested coverage while comparing independent concepts; decomposing the first idea is not sufficient exploration. This guide turns the synthesis into complete feature specifications and bounded implementation work.

## Preserve coverage before narrowing delivery

Read the relevant request, BRIEF, contracts, and evidence. Identify defining player outcomes and the behaviors, feedback, content variety, and interactions that support them. Keep a short map of meaningful facets; detail the agreed feature and critical dependencies. Broader project ideas can remain coverage rows. Do not enumerate an entire reference game's content or invent requirements to fill categories.

Distinguish requested requirements, accepted decisions, provisional choices, and unknowns. A named reference game is a starting point for clarifying desired qualities, not a complete specification. Resolve critical ambiguity with the product owner; use authorized, reversible prototypes to explore other unknowns without claiming fidelity.

For standard/consequential work, create one bounded `project/design/<slug>.md` from [the design template](templates/design.md), or use an existing canonical design source with equivalent fields. Link it from the task and BRIEF or the relevant MAP entry; create no new index. The coordinator owns accepted coverage and scope. Designers return proposed specifications in their handoffs or receive exclusive writing ownership of the whole design file; coordinator writes pause during that assignment.

Assign stable IDs to outcomes worth tracking. Separate delivery scope (`current`, `later`, `excluded`) from evidence state (`unresolved`, `specified`, `implemented`, `verified`). Record simplifications with their effect on the requested quality and authority. Deferred work remains visible; committed follow-ups need an owner and next action. An intermediate slice does not complete the whole request. Reducing requested outcomes needs acceptance from the user or delegated product owner; routine choices within existing authority proceed normally.

## Specify the feature by decision layer

| Layer | Resolve for the agreed feature |
| --- | --- |
| Experience | Player outcomes and observable qualities; label subjective hypotheses |
| Behavior | Rules, state transitions, tuning assumptions, feedback, failure cases, and defining content differences |
| Shared contracts | Dependencies, state/timing ownership, interface semantics, identifiers, and relevant compatibility constraints |
| Implementation | Next-slice assignments with acceptance, permitted decisions, exclusive paths, and parent context |
| Evaluation | Functional checks plus relevant content, integrated scenario, and observed-play evidence |

Layers organize decisions; playable slices organize delivery. Specify behavior and interactions throughout the agreed feature before declaring its design ready, including later delivery slices. Select a small end-to-end implementation loop exercising important interactions, presentation, and content. Preserve broader project coverage without exhaustively specifying unrelated future systems. Revisit affected decisions after prototypes; do not freeze uncertain tuning as architecture.

If the request spans slices, retain an active owning task/WORK row with the next slice or concrete blocker until the requested outcome is complete, explicitly revised, or paused by the user. Reuse that task when practical. Closing a child slice must transfer outstanding requested work to an active owner; a later-scope row alone is not that handoff.

## Dispatch a resolved local problem

Use [dispatch](dispatch.md). Each packet carries relevant outcome IDs, accepted behavior or source excerpts, interface dependencies, success/failure examples, and decision boundaries. Include enough parent intent to judge a local choice without loading the whole design record.

FAST implementation assignments need objective acceptance and established behavior/contracts. Send unresolved mechanics or coupling to the coordinator/designer or a stronger tier first. Before dispatching builders, apply the [design readiness check](design-exploration.md#6-challenge-and-check-readiness). Split work at coherent behavior and ownership boundaries; avoid one task per function or excessive fragments. Workers flag missing decisions affecting experience or shared contracts rather than silently simplifying them. Ordinary implementation choices inside the packet remain theirs.

## Evaluate detail and integration

Local success establishes local behavior. Run the combined slice's relevant scenarios, checking interactions and defining feedback/content differences against the coverage IDs. A passing compile or many assets cannot establish encounter variety, feel, or fidelity. Separate executed evidence from predictions and unavailable checks.

Update the affected rows after integration. `implemented` needs inspected integrated changes; `verified` needs the row's agreed evidence. Missing required evidence keeps a row open. Simplified behavior can satisfy only its explicitly accepted scope. Invalidate affected evidence when a design, dependency, or implementation changes.

At slice closeout, report satisfied outcomes, omissions/simplifications, remaining scope, and unknown experience claims. Link reusable contracts to area notes and accepted rationale to decisions without duplicating specifications. Merge or split records only when a clear consumer or ownership boundary justifies it. Maintain coverage on consequential changes, not every minor edit.

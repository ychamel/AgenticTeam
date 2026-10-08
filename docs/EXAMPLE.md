# Worked feature exploration

Everything below is fictional: project, assignments, decisions, values, and scenarios. No engine, prototype, player session, or profiler was run. The illustrated records belong in an adopted project, not this uninitialized template.

## Small tuning bypass

An agreed cooldown adjustment follows the existing contract and focused validation; it needs no concept roster or design record. Required feel acceptance still needs observed play. Unexpected shared-system consequences promote the work before broader edits.

## One neutral brief

Request: “Let players reposition under danger with meaningful risk and reward.” No mechanic is preferred.

The coordinator establishes coverage IDs: D-01 deliberate position changes; D-02 readable commitment and consequences; D-03 predictable movement, damage, pause, and lifecycle interactions. Constraints are one existing ability button, grounded combat, no added attack damage, and existing collision authority. Success requires specified combined behavior, executable acceptance checks, and observed player understanding; fun and balance remain hypotheses.

Before dispatch, comparison criteria are fixed: tactical choices, readable risk, failure predictability, input accessibility, and integration cost. Each concept must describe a complete loop, weakest case, contracts, and falsifying experiment. All receive the same brief and factual sources, without suggested solutions or sibling outputs.

## Independent proposals first

Three independent designers return proposals. These are predictions, not measured rankings:

| Branch | Proposed loop and risk | Shared criteria comparison |
| --- | --- | --- |
| C-A: steerable burst | Choose direction, steer through a short burst, recover exposed; spend one charge. | Immediate tactical freedom; readable endpoint; corners complicate failure; simple input; moderate collision integration. |
| C-B: planted return anchor | Mark retreat position, lure danger elsewhere, return along the path; placement and transit remain vulnerable. | Rewards preparation; visible commitment; changing paths threaten predictability; two presses; greater lifecycle integration. |
| C-C: reactive pivot | During an enemy windup, reposition around that enemy; mistiming leaves the player nearby and exposed. | Rewards threat reading; timing cue is central; target-loss ambiguity; precision limits accessibility; requires enemy targeting contracts. |

Each proposes a falsifier: C-A fails if steering removes meaningful commitment; C-B fails if players ignore placement and habitually return without evaluating danger; C-C fails if readable windups still produce frequent unintended pivots. These experiments remain unrun.

The coordinator waits for all returns, reconciles unsupported assumptions, and only then shares discoveries. C-C's threat-direction cue is useful; enemy lock and precision timing add unwanted dependencies. C-A and C-B survive deeper comparison. They are competing mechanics, not ingredients to stack together.

## Bounded deeper work

C-B receives two complementary children, not two more complete mechanics:

- **C-B.detail1:** charge, expiry, interruption, pause, death, and reset.
- **C-B.detail2:** anchor surfaces, path obstruction, feedback, and encounter implications.

Both inherit parent assumptions: fixed ground, one stored position, vulnerable transit, no damage reward, existing collision authority. Changing these returns to the coordinator. They receive relevant discoveries from the saved concepts and identify reusable insights and incompatibilities; unrelated branch detail stays out of their packets.

The coordinator controls budgets: three initial concepts, at most two survivors, at most two children per survivor, one expansion layer, eight design assignments including final challenge. This example spends six: three concepts, two children, one challenge. At most three run concurrently, reduced to the host limit. Children cannot recursively expand or raise budgets.

## Synthesize one feature

The coordinator provisionally selects C-B: placement, vulnerable transit, and a fixed return point make its risk/reward choices inspectable, accepting greater lifecycle complexity within scope. This is a testable design judgment, not evidence that it outperforms C-A. C-A's attractive steering during transit would erase anchor commitment and undermine path prediction, so it is rejected. C-C contributes a compatible directional danger cue without target lock or timing window.

The canonical record is `project/design/repositioning.md`. Its illustrative proposal links are:

```markdown
[C-A](../tasks/T-feature/design/C-A.md)
[C-B](../tasks/T-feature/design/C-B.md)
[C-C](../tasks/T-feature/design/C-C.md)
[Resource/lifecycle](../tasks/T-feature/design/C-B.detail1.md)
[Spatial/feedback](../tasks/T-feature/design/C-B.detail2.md)
[Final challenge](../tasks/T-feature/design/Q-1.md)
```

Each branch file is its assignment's proposal and handoff, owned by one writer. Accepted behavior lives in the synthesis; task status stays in the task. No duplicate status log is added.

### Integrated behavior excerpt

Values are provisional tuning, not validated balance:

- **Idle → Placing:** a fresh press while grounded starts 0.25 seconds of stationary, vulnerable placement. Invalid ground, stun, or unavailable charge rejects activation with distinct shape/audio feedback. Releasing before completion or being stunned cancels to Idle without cost.
- **Placing → Armed:** completion spends the single charge and creates a fixed marker. Movement resumes. The marker lasts four simulation seconds; expiry or moving beyond six metres consumes it, returns to Idle, and starts a 2.5-second cooldown.
- **Armed → Returning:** another press requests the marker. A blocked path offering less than 0.5 metres rejects the request, retains the anchor until expiry, and shows obstruction feedback. Otherwise consume the marker, start cooldown, and sweep toward it at 20 metres/second. No steering, attacks, or invulnerability apply.
- **Returning → Recovery → Idle:** arrival, new obstruction, or stun stops travel at the current valid position. Recovery lasts 0.3 seconds; longer stun still controls movement. Damage applies throughout. Cooldown continues during recovery; its expiry restores the charge. Presses during stun or recovery are rejected, never queued.
- **Lifecycle/ownership:** ability owns state, charge, and marker; movement owns position, collision owns sweeps, damage owns stun/death. Resolve sweeps before damage; death overrides recovery. Pause freezes simulation timers and drops activation input. Death or scene exit destroys marker and pending travel; respawn initializes Idle with one charge. Held input cannot reactivate it.
- **Feedback:** marker/path show availability and obstruction through shape plus sound; the borrowed cue reports threat direction, never promises destination safety.

## Challenge the combination

A fresh reviewer receives the integrated design, neutral brief, criteria, and unrun-evidence labels before authors' rationale. Its challenge exposes a destination becoming dangerous during transit; the coordinator clarifies the feedback promise above and resolves affected acceptance before design-ready.

The combined walkthrough covers:

- **Normal:** plant behind cover, move outward, lure a windup, return; vulnerable placement, travel, recovery, and charge depletion form one decision.
- **Failure:** a gate closes during return; the sweep stops short. A simultaneous hit stuns there without refunding charge or restarting cooldown.
- **Interaction:** pause during recovery, resume, then change scenes; timers freeze and no old marker or held input survives reset.

This establishes proposed consistency, not successful play or performance. At design-ready, D-01–D-03 are current/specified, not implemented/verified. Design-ready requires the full agreed feature and interactions, not merely its first coding slice. Allowing moving platforms changes a root constraint: affected parent assumptions, child conclusions, synthesis, and gates reopen.

## Implement and finish honestly

Only coding assignments narrow to the next playable slice. Builders receive resolved contracts and exclusive paths, including content/import ownership. Functional, import, target-build, and observed-play evidence remains unrun here; performance claims require comparable captures. Missing required evidence cannot pass acceptance.

At interruption, confirm the prior writer stopped and inspect files before resuming. Changed dependencies invalidate affected evidence. Deferred requested behavior keeps an active owner and next action; closing a slice is intermediate. Close the task after acceptance and review resolution, then archive records and repair links.

Without independent agents, explore sequentially and label later variants dependent, with self-review identified honestly. Do not invent independent agreement.

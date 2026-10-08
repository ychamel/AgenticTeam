# Workflow

Audience: coordinator. Workers follow their packet and role; the coordinator carries this process.

This lifecycle applies to actual projects. For explicit maintenance of the reusable template itself, follow [the baseline-editing rule](../AGENTS.md#editing-the-baseline) and keep starter project state pristine.

For game tasks, read [the game profile](game-development.md) and pass applicable constraints to each assignment. Keep subjective design hypotheses separate from functional, content, performance, and observed-play evidence.

## 1. Frame before exploring

State the desired behavior, constraints, unknowns, and a success check in at most five bullets. For an unfamiliar problem, first choose an investigation strategy: what evidence would distinguish likely causes or approaches? Do this before broad searches. A tiny task needs one sentence, not a planning document.

Choose the lightest path based on uncertainty and impact, not line count:

| Path | When | Records and participants |
| --- | --- | --- |
| Small | Clear, reversible, local; no meaningful unresolved design | Coordinator can implement and check directly. Final response is the handoff; update existing project facts only if they changed. |
| Standard | Multiple steps, delegation, uncertainty, or likely resumption | One task record; only needed process roles; persisted handoffs. |
| Consequential | Architecture, public contracts, security boundaries, migrations, or difficult rollback | Standard path plus context-isolated partner, independent review, and explicit failure/rollback checks. |

In games, consequential scope can include save formats, shared simulation timing, networking authority, or wide scene/content migrations. A small tuning change is not automatically consequential; judge its effect on the actual game contract.

Promote a small task to standard before delegating, suspending with unfinished changes, or discovering significant uncertainty. If the runtime lacks independent agents, use the documented fallback and state the review limitation.

For small work, proceed directly from framing to the edit, proportionate verification, updates to any changed canonical facts, and final reporting. The task-record, assignment, checkpoint-file, and archival steps below apply to standard/consequential work only.

## 2. Establish resumable state

Read the relevant row of [WORK](../project/WORK.md); reuse its task rather than creating a competing record. For new work, create `project/tasks/YYYY-MM-DD-short-slug/task.md` from [the task template](templates/task.md), checking for name collisions. Create directories only when needed. Register one row in WORK with owner, status, and next action.

Task states: `active`, `blocked`, `ready`, `done`, `cancelled`. `ready` means implementation awaits integration or verification, not completion. `blocked` requires a named missing dependency and resumption condition. Reopen an unarchived `ready` or `done` task as `active` when needed. For an archived task, create a new linked follow-up task and WORK row; preserve the archived record and never split one task across active and archive directories. Checkpoints may occur in any unfinished state.

One coordinator owns the task and shared indexes. Record each assignment's owner, write paths, handoff path, and state **before** starting it. Assignment states are `queued`, `active`, `blocked`, `ready`, `integrated`, or `cancelled`; only the coordinator marks a result integrated after checking it. Use [dispatch](dispatch.md) for model selection and packets. If multiple human sessions coordinate the same repository, agree a single owner or use isolated worktrees; a Markdown table is not an atomic lock.

## 3. Discover and decide

Have a scout locate relevant code, constraints, and checks when that saves main-context work. Ask a partner to challenge the neutral framing before committing to a consequential direction. Consult area notes and accepted decisions only for the affected scope. Confirm decision-critical summaries against sources.

Record a short decision brief: evidence, plausible alternatives, chosen approach and reason, main risk, and what would change the choice. Update it when evidence changes. Keep this in the task; promote it to a decision record only if future work must obey or understand it. Do not persist hidden reasoning, debate transcripts, or every discarded idea.

## 4. Build, verify, review

Assign disjoint file ownership or serialize overlapping changes. Builders update their handoffs at meaningful milestones. Verify behavior against acceptance criteria, including relevant failure paths. Tests or builds that mutate shared outputs must run serially or in isolated directories.

For a playable slice, verify its relevant code and content together. Select scene/import checks, gameplay scenarios, target-build smoke tests, performance measurements, or playtests according to acceptance. Record unavailable engine/device/human-play access explicitly and keep dependent criteria open. Save/import operations must respect related-file ownership.

Use an independent reviewer for consequential changes and for standard changes when it adds confidence. Give them acceptance criteria, the diff, and evidence before the builder's rationale. Resolve findings against evidence, then rerun only affected checks. The coordinator inspects the combined change and verifies interfaces across assignments; worker success does not prove integration.

Check evidence identifies the actual relevant inputs: revision plus content fingerprints of relevant dirty/untracked files, or dated relevant-file fingerprints without version control. Include changed configuration affecting the check. Filenames alone cannot identify tested content. If the checkpoint no longer matches or cannot be identified, mark validity unknown and recheck before relying on it.

## 5. Persist and close

Before any yield, known compaction, ownership transfer, blocked return, or completion:

1. Each worker replaces its assigned handoff with current state using [handoff](templates/handoff.md); it retains unresolved risks and links to useful prior evidence. Preserve the last complete content until its replacement is saved, using temporary-file replacement when supported. A reassigned attempt gets a new ID and handoff, preserving its predecessor.
2. Read-only workers return the same fields; the coordinator saves them before relying on the result or dispatching a dependent task.
3. The coordinator updates task state and WORK: integrated results, current ownership, exact next action, and unresolved work. Save worker records before marking their assignments integrated.

At completion, promote lasting facts to BRIEF, MAP, relevant area notes, or accepted decisions. Keep unfinished issues in WORK with an owner and next action. Run the small closeout pass in [maintenance](maintenance.md), remove the completed row from the active list, and archive the task. Report result, verification, and material limits. No new permission step is needed for ordinary authorized record updates.

## Resume after interruption

Read AGENTS, foundation, the task, and relevant latest handoffs. Confirm ownership and inspect actual files and repository status before acting. Look for unindexed task/attempt files if the index update may have been interrupted. If a worker may still be writing, contact or stop it and confirm it has stopped before reassignment; if that cannot be established, isolate the new workspace. Missing handoffs mean unknown progress, not an untouched tree. Reconstruct evidence from files and checks; revalidate stale claims, then write a fresh checkpoint. Never replay an action solely because an old plan lists it.

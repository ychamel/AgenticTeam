# Dispatch and model routing

Audience: coordinator, before delegating. Resolve model aliases and capabilities from [RUNTIME](../project/RUNTIME.md). These instructions request behavior; Markdown cannot create tools, enforce permissions, or schedule agents.

## Select a process and capability

| Process | Default tier | Bounded outcome |
| --- | --- | --- |
| [Scout](roles/scout.md) | FAST | Evidence, locations, relevant checks, unknowns |
| [Builder](roles/builder.md), mechanical change | FAST | Narrow edit with objective acceptance |
| [Builder](roles/builder.md), ordinary implementation | STANDARD | Coherent implementation and local checks |
| [Verifier](roles/verifier.md), known commands | FAST | Reproducible outcomes and failure summary |
| Verifier, diagnosis or test design | STANDARD; STRONG if subtle | Behavior-focused validation |
| [Reviewer](roles/reviewer.md) | STANDARD; STRONG for consequential work | Prioritized, supported findings |
| [Partner](roles/partner.md) | STRONG | Independent questions, options, falsifying checks |
| [Coordinator](roles/coordinator.md) | STRONG for difficult decisions | Scope, decisions, integration, acceptance |
| [Curator](roles/curator.md) | FAST for links; STANDARD for synthesis | Verified context repairs and pruning |

FAST means a smaller, faster model available in this runtime, not a weaker quality contract. Never send ambiguous architecture, security judgments, or risky migrations to FAST solely to save tokens. Alias bindings belong in one project file, not every role. Record the requested tier and actual selection if visible; say unknown when unavailable.

If one bounded attempt lacks evidence, contradicts sources, or discovers deeper coupling, narrow the task or escalate a tier with a short summary. Do not repeat the same cheap attempt indefinitely. Model output is checked to the same acceptance standard at every tier.

## Assignment packet

Give a fresh agent only:

- Task/assignment ID, process role, goal, acceptance criteria, and relevant non-negotiable constraints.
- Initial sources or source excerpts; facts already verified and remaining questions. Include cross-cutting constraints even if they live outside the requested files.
- Exact writable files or directories, read scope, owner, and whether tools may mutate outputs.
- Requested tier, expected output length, and a stopping condition.
- Assigned handoff path and the next consumer. Include the handoff fields inline if the worker cannot read its template.

Default to no inherited conversation history. Ordinary workers read root instructions, foundation, their own role, the packet, and relevant sources. Discover additional context when needed for correctness; the read list is a starting point, not a ban on finding dependencies. Expand write scope only through the coordinator. Workers do not spawn more agents by default.

Use up to three simultaneous workers as a starting ceiling, lowered to runtime limits. Spawn only independent work with a useful expected return. Prefer one scout with a bounded search to many overlapping scouts. A task already cheaper to do than explain stays local. Keep returns around 250 words plus essential evidence pointers; budget exceptions preserve important risks.

## Context-isolated pair programming

The coordinator acts as the driver; a fresh STRONG partner acts as a temporary navigator. Send the problem, constraints, and success criteria, omitting the current favored solution and project history. Supply the foundation and partner role directly; grant no repository-reading or writing work. Request up to three pointed questions, two alternatives, and an observation that could disprove each option.

Answer with the minimum neutral facts necessary, for at most two exchanges by default. Then choose using project evidence and save only the useful conclusion in the task. Restart fresh for a materially different dilemma; do not turn the partner into a second coordinator. This reduces inherited context bias; it does not guarantee an unbiased opinion.

Use a fresh context option and tool restrictions only if supported. If the host automatically injects project context, record partial isolation. If it cannot isolate conversations, use a deliberate alternative-analysis pass and label it a self-check, not independent review.

## Shared workspace and fallbacks

One writer per source file, task file, index, and handoff. Read-only tools may still create caches; make those outputs explicit. Serialize shared lockfiles, generated files, migrations, and build outputs, or isolate them in worktrees. Hand off ownership only after the previous writer has stopped; check the diff before integration.

No model selection: use the available model and keep tasks small; claim no cost savings. No subagents: perform needed roles sequentially with the same records. No worker filesystem: coordinator persists returned handoffs. No true read-only enforcement: scopes are an instruction contract, not a sandbox. No persistent write access at all: return the checkpoint to the user and clearly identify that persistence is unavailable.

# Agent entry point

This game-development branch uses a layered Markdown workflow. Read selectively; links are routes, not a request to load everything.

## Start

1. Read [the foundation](team/foundation.md) once per fresh context. It contains the baseline quality and collaboration contract.
2. If delegated, read only your assigned [role](team/roles/), assignment packet, and relevant sources. The packet may replace reading the full task. Request missing context when it could change correctness. A context-isolated partner receives the contract and role in its prompt and reads no repository files.
3. If coordinating, read [coordinator](team/roles/coordinator.md), [project brief](project/BRIEF.md), and [active work](project/WORK.md). If uninitialized, follow [setup](docs/SETUP.md). Otherwise select the task and use [workflow](team/workflow.md).
4. Before edits, inspect applicable directory instructions and the current files. Use [the map](project/MAP.md) to locate relevant area notes and commands. Expand to callers, dependencies, or cross-cutting constraints when needed.

## Routes

| Need | Read |
| --- | --- |
| Frame or validate game work | [Game-development profile](team/game-development.md); workers receive relevant constraints in their packets |
| Delegate, select models, isolate a partner | [Dispatch](team/dispatch.md); coordinator also reads [runtime bindings](project/RUNTIME.md) |
| Resume, plan, implement, finish | [Workflow](team/workflow.md) and the assigned task |
| Prune stale context or revise the baseline | [Maintenance](team/maintenance.md) |
| Create a record | Only the matching [template](team/templates/) |
| Understand this template's design | [Design](docs/DESIGN.md), on request |

## Always

- Frame the goal, constraints, and success check before detailed exploration. Record concise decisions and evidence, not private reasoning transcripts.
- Use focused subagents when they add value; keep the main context centered on decisions and integration. Prefer a smaller, faster model for bounded exploration and mechanical work when the runtime permits.
- Before yielding, ending, or an anticipated context reset, update your owned handoff with verified state, uncertainty, and the next action. Read-only workers return that content for the coordinator to save.
- One writer per file. The coordinator owns shared task state and indexes unless ownership is explicitly transferred.
- Do not load archives, unrelated tasks, all roles, or all decisions by default. Do not weaken the foundation during ordinary project work.

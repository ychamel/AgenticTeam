# AgenticTeam

A Markdown baseline for repositories worked on by coding agents. It keeps quality rules stable, sends focused work to the right agent, and preserves enough context for the next session without loading the whole project's history.

Start with [setup](docs/SETUP.md). Agents start at [AGENTS.md](AGENTS.md).

## What gets loaded

```text
AGENTS.md                    Small entry point and routing
  └─ team/foundation.md      Shared engineering and collaboration contract
      ├─ one process role   Only the responsibility assigned now
      └─ assignment packet  Goal, constraints, sources, permissions, return
          └─ relevant project context and source files

Coordinator additionally reads BRIEF + WORK and the required process guides.
Archives, other roles, and unrelated decisions stay out of default context.
```

## Layout

| Location | Purpose | Change policy |
| --- | --- | --- |
| [AGENTS.md](AGENTS.md) | Entry point and reading routes | Baseline revision |
| [team/foundation.md](team/foundation.md) | Quality, evidence, collaboration, completion | Stable during ordinary work |
| `team/` process guides and [roles](team/roles/) | Workflow, dispatch, maintenance, focused responsibilities | Deliberate baseline updates |
| [team/templates/](team/templates/) | Small task, handoff, decision, and area forms | Copy only when needed |
| [project/BRIEF.md](project/BRIEF.md), [MAP.md](project/MAP.md) | Project purpose, boundaries, locations, commands | Verified project facts |
| [project/WORK.md](project/WORK.md), [DECISIONS.md](project/DECISIONS.md) | Compact routing indexes | Coordinator-owned updates |
| [project/RUNTIME.md](project/RUNTIME.md) | Model aliases and observed host capabilities | Per environment |
| `project/tasks/`, `areas/`, `decisions/`, `archive/` | Work and durable knowledge | Created on demand |
| [docs/](docs/) | Setup, design rationale, worked example | Human/reference material; not default agent input |

## How work flows

The coordinator frames the problem before exploration. A fast scout gathers evidence; a fresh, strong partner challenges consequential design choices without inheriting project history. Builders own narrow edit scopes, verifiers run relevant checks, and reviewers inspect the outcome independently. The coordinator integrates results and a curator repairs stale context when triggered. These are seven available responsibilities, not seven mandatory agents.

Minor fixes use a short path. Resumable or delegated work gets one task directory with separate, exclusively owned handoffs. Consequential choices become decision records; completed work leaves the active index. [The worked example](docs/EXAMPLE.md) shows delegation, a design challenge, interruption recovery, and closeout.

“Automatic” means the instructions require agents to update records at milestones and before yielding. Markdown does not run a scheduler, choose a model by itself, enforce access controls, or guarantee a write after a crash. Multi-agent execution, cheaper models, and context isolation depend on host support; the framework defines explicit fallbacks. Codex-specific setup follows [official instruction-loading](https://learn.chatgpt.com/docs/agent-configuration/agents-md) and [subagent guidance](https://learn.chatgpt.com/docs/agent-configuration/subagents).

No package manager, database, orchestration service, or required scripts. Copy the baseline into a new repo and populate the five project files from evidence. Keep code in the structure appropriate to that project.

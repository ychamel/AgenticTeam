# Adopt the baseline

Read during initial setup or migration, not at every task start. The starter's five `project/*.md` files are intentionally uninitialized. They describe the destination project, not AgenticTeam's construction history.

## New repository

1. Copy `AGENTS.md`, `team/`, and `project/` into the destination root. Also copy `docs/SETUP.md`, `docs/DESIGN.md`, and `docs/EXAMPLE.md` so reference links resolve. Keep the destination's product README; this template's README is optional.
2. Ask the agent to initialize the project context using the prompt below. It should inspect only relevant manifests, entry points, CI, and existing documentation, or use your stated requirements for an empty project.
3. Fill BRIEF with purpose and constraints, MAP with real locations and commands, and RUNTIME with observed capabilities. WORK and DECISIONS start empty. Unknown facts remain explicitly unknown; ask only for missing choices that block meaningful work.
4. Run a small real task. Verify that the agent reads the intended route, saves a handoff when delegated, and reports actual checks. A tiny local fix should not create a team of agents or a task directory.

Example bootstrap request:

> Read AGENTS.md and initialize this baseline for the current repository. Infer facts from code and maintained configuration, record sources and unknowns, and bind FAST, STANDARD, and STRONG to available models when supported. Keep active work empty unless the request includes implementation. Then explain the files initialized and any runtime limitations.

For a truly new project, include its purpose, users, constraints, and preferred stack in the same request. The agent can begin reversible scaffolding within that scope while clarifying consequential unknowns.

## Existing repository

Merge the small router into existing root instructions. Preserve valid project conventions and resolve conflicts deliberately; do not overwrite an existing AGENTS file or context directory blindly. If `team/`, `project/`, or `docs/` names collide, choose an unused prefix and update links, literal read/write paths, template destinations, example packets, and entry-point routing together. Search for the old paths and verify that every operational reference targets the adopted location.

Existing docs, issues, and architecture decisions can remain canonical. MAP and DECISIONS should link to them rather than duplicate them. Preserve existing nested AGENTS files where they express real directory-specific instructions; role guides should remain ordinary Markdown files, avoiding accidental automatic loading of every role.

Commit the adopted files using the repository's normal workflow when authorized. Do not copy the source repository's `.git`, account configuration, credentials, unrelated task history, or generated logs.

## Codex binding

Codex discovers `AGENTS.md` through its instruction chain, with directory-specific overrides and a size cap. A linked role or project document still needs to be read when routed to; this baseline intentionally keeps the root small. Verify the instructions actually loaded in your session, especially when starting below the repository root. See [official AGENTS.md guidance](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

Codex supports subagents and model configuration in supported clients; exact controls depend on the host. Inspect the available spawn tool and model list before binding aliases. Set FAST to an available smaller model, STANDARD to a capable coding model, and STRONG to an available model appropriate for difficult reasoning. Configure or explicitly select the model at dispatch; a Markdown alias alone does not select it. See [official subagent guidance](https://learn.chatgpt.com/docs/agent-configuration/subagents).

For a host exposing the same collaboration controls as the environment used to build this baseline, the mapping is:

| Intent | Tool parameter / action |
| --- | --- |
| Fresh worker or partner | `spawn_agent` with `fork_turns: "none"` and a self-contained packet |
| Smaller-model scout | Set the available `model` explicitly, e.g. `gpt-6-luna`, with supported effort |
| Strong partner | Select the bound STRONG model, or inherit only its model setting while passing no conversation history |
| Transfer ownership | Request stop, confirm stopped, inspect files, then issue a new assignment ID |

These parameter names and the example model are specific to that host, not portable API promises. In other clients use their documented equivalents. Fresh conversation history can still include system or repository instructions; record the actual isolation limit. Read/write restrictions in Markdown are behavioral instructions unless the host enforces them. No runtime configuration is installed by this template.

## Other hosts and single-agent mode

Point the host's native instruction entry point at AGENTS.md or include its small router once. Avoid mirrored copies of the whole framework. If delegation, model choice, or fresh contexts are unavailable, record that in RUNTIME and use [the sequential fallbacks](../team/dispatch.md). Do not describe a single agent's self-review as independent review.

## Baseline updates

Compare the adopted foundation version with the version you want to adopt. Review changes to AGENTS and `team/`; retain project context and runtime bindings. Apply compatible updates as a deliberate change, inspect local instruction conflicts, and try one representative task. Do not overwrite `project/` with empty starter files during an upgrade. See [maintenance](../team/maintenance.md).

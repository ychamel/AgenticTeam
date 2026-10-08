# Adopt the game-development baseline

Read during initial setup or migration, not at every task start. The five `project/*.md` files describe the destination game; its identity, facts, and model bindings are intentionally uninitialized. Task and decision indexes are empty, maintenance counters start at zero, and no project history is included.

## New repository

1. Copy `AGENTS.md`, `team/`, and the five top-level `project/*.md` files into the destination root. Also copy `docs/SETUP.md`, `docs/DESIGN.md`, and `docs/EXAMPLE.md` so reference links resolve. Keep the destination's product README; this template's README is optional.
2. Ask the agent to initialize the project context using the prompt below. It should inspect only relevant manifests, entry points, CI, and existing documentation, or use your stated requirements for an empty project.
3. Fill BRIEF with game pillars, core loop, engine/toolchain, target platforms/input, and agreed budgets. Fill MAP with real code, scene/asset, import, test, and build entry points. RUNTIME holds agent capabilities and models. WORK and DECISIONS start empty. Unknown facts stay explicit; do not invent a frame-rate target or multiplayer requirement.
4. Run a small real task. Verify that the agent reads the intended route, saves a handoff when delegated, and reports actual checks. A tiny local fix should not create a team of agents or a task directory.

Example bootstrap request:

> Read AGENTS.md and the game-development profile, then initialize this baseline for the current game repository. Infer facts from code, scenes, and maintained configuration; record engine/platform/input, known budgets, asset/import boundaries, sources, and unknowns. Bind FAST, STANDARD, and STRONG when supported. Keep active work empty unless the request includes implementation. Explain initialized files and unavailable editor, build, device, or playtest capabilities.

For a truly new game, include the player experience, core loop, intended platforms, constraints, and preferred engine if known. The agent can begin a small authorized prototype while clarifying consequential unknowns. Keep uncertain mechanics as hypotheses and request real play observations when acceptance needs them.

## Existing repository

Merge the small router into existing root instructions. Preserve valid project conventions and resolve conflicts deliberately; do not overwrite an existing AGENTS file or context directory blindly. If `team/`, `project/`, or `docs/` names collide, choose an unused prefix and update links, literal read/write paths, template destinations, example packets, and entry-point routing together. Search for the old paths and verify that every operational reference targets the adopted location.

Existing docs, issues, and architecture decisions can remain canonical. MAP and DECISIONS should link to them rather than duplicate them. Preserve existing nested AGENTS files where they express real directory-specific instructions; role guides should remain ordinary Markdown files, avoiding accidental automatic loading of every role.

Commit the adopted files using the repository's normal workflow when authorized. Do not copy the source repository's `.git`, account configuration, credentials, unrelated task history, or generated logs.

## Codex binding

Codex discovers `AGENTS.md` through its instruction chain, with directory-specific overrides and a size cap. A linked role or project document still needs to be read when routed to; this baseline intentionally keeps the root small. Verify the instructions actually loaded in your session, especially when starting below the repository root. See [official AGENTS.md guidance](https://learn.chatgpt.com/docs/agent-configuration/agents-md).

Codex supports subagents and model configuration in supported clients; exact controls depend on the host. Inspect the available spawn tool and model list before binding aliases. Set FAST to an available smaller model, STANDARD to a capable coding model, and STRONG to an available model appropriate for difficult reasoning. Configure or explicitly select the model at dispatch; a Markdown alias alone does not select it. See [official subagent guidance](https://learn.chatgpt.com/docs/agent-configuration/subagents).

For hosts exposing these collaboration parameters, the mapping is:

| Intent | Tool parameter / action |
| --- | --- |
| Fresh worker or partner | `spawn_agent` with `fork_turns: "none"` and a self-contained packet |
| Smaller-model scout | Set `model` to the locally bound FAST model, with supported effort |
| Strong partner | Select the bound STRONG model, or inherit only its model setting while passing no conversation history |
| Transfer ownership | Request stop, confirm stopped, inspect files, then issue a new assignment ID |

These parameter names are host-specific, not portable API promises. In other clients use their documented equivalents. Fresh conversation history can still include system or repository instructions; record the actual isolation limit. Read/write restrictions in Markdown are behavioral instructions unless the host enforces them. No runtime configuration is installed by this template.

## Other hosts and single-agent mode

Point the host's native instruction entry point at AGENTS.md or include its small router once. Avoid mirrored copies of the whole framework. If delegation, model choice, or fresh contexts are unavailable, record that in RUNTIME and use [the sequential fallbacks](../team/dispatch.md). Do not describe a single agent's self-review as independent review.

## Baseline updates

Compare the adopted foundation and game-profile versions with the versions you want to adopt. Review changes to AGENTS and `team/`; retain project context and runtime bindings. The game profile layers on foundation 1.0.0 without changing its contract. Apply compatible updates as a deliberate change, inspect local instruction conflicts, and try one representative playable-slice task. Do not overwrite `project/` with empty starter files during an upgrade. See [maintenance](../team/maintenance.md).

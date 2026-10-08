# Runtime bindings

Status: uninitialized. Coordinator reads this when dispatching; workers receive only the resolved settings in their packets. These are documented choices, not executable configuration.

## Model aliases

| Alias | Intended capability | Actual available model / effort |
| --- | --- | --- |
| FAST | Smaller, faster model for bounded exploration, mechanical edits, and known checks | Unbound; resolve from exposed runtime options |
| STANDARD | Reliable everyday implementation and review | Unbound; resolve from exposed runtime options |
| STRONG | Difficult decisions, subtle risks, context-isolated partner | Unbound; resolve from exposed runtime options |

Model availability and price vary. Pick from the actual environment, honor user preferences, and verify capabilities before dispatch. If bindings cannot be set, use the available model and report that limitation. Do not claim model switching or savings based on this table alone. Revisit bindings when the runtime changes or an assignment repeatedly needs escalation.

## Capabilities

| Capability | Observed support / binding |
| --- | --- |
| Spawn and message subagents | Unknown |
| Choose a model per subagent | Unknown |
| Fresh context without inherited conversation | Unknown |
| Automatic project-instruction injection into fresh agents | Unknown |
| Tool/read/write restrictions per worker | Unknown; instructions alone are not enforcement |
| Persistent shared files or isolated worktrees | Unknown |
| Safe concurrent workers | Start with at most 3; lower to available limit |

- Host and version, if visible: unknown.
- Last verified and evidence: not initialized.
- Project-specific adaptations: none.

Use [dispatch fallbacks](../team/dispatch.md) for missing capabilities. Recheck capabilities per session if the host can vary; never put credentials in this file. Setup guidance includes an optional [Codex binding](../docs/SETUP.md#codex-binding).

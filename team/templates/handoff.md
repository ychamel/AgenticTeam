# Handoff: <assignment-id>

<!-- Copy to project/tasks/<task-id>/handoffs/<assignment-id>.md on demand. Placeholders are not facts. Remove unused optional sections and rebase copied/moved links. One writer per handoff. Reassignment needs a new ID (scout-01 → scout-02). Overwrite owned record; no competing state logs. Read-only workers return identical fields; coordinator persists before integration. -->

- **Task / assignment:** <task-id / unique assignment-id>
- **Role / owner:** <role / writer>
- **Requested tier / actual selection:** <alias / visible actual model or unknown>
- **Status:** <active | blocked | ready | cancelled>
- **Updated:** <timestamp with timezone>
- **Source checkpoint:** <revision plus relevant dirty/untracked content fingerprints; without VCS, dated relevant-file fingerprints>

## Objective and acceptance

<Outcome, scope, acceptance criteria.>

## Facts and assumptions

- **Verified:** <finding, source pointer, supporting observation>
- **Assumed or unknown:** <claim and required evidence>

## Changed paths

| Path | State: planned / applied / verified | Evidence |
| --- | --- | --- |
| <path or explicitly none> | <state> | <behavior and evidence pointer> |

## Checks

| Exact command | CWD | Scope | Exit / result | Timestamp | Checked checkpoint | Current validity |
| --- | --- | --- | --- | --- | --- | --- |
| <command or not run> | <directory> | <criteria/files> | <exit status and observation> | <time> | <revision + relevant content fingerprints> | <valid / stale / unknown, reason> |

<!-- Claim only executed results. Later edits invalidate affected checks. Link evidence, not logs. -->

## Next step

- **Uncertainty / scope gaps:** <remaining limits>
- **Blocker / resumption condition:** <dependency and required remedy; optional>
- **Next action / consumer:** <concrete step and recipient>

<!-- Refresh before yielding, blocking, milestones, compaction, ownership transfer, or completion. Retain unresolved risks and evidence links. -->

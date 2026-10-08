# Worked example and acceptance walkthrough

All projects, paths, outcomes, and commands in this example are fictional. No application tests below were executed in this template repository. The example demonstrates how to use the protocol; do not copy it into active project state.

## A tiny edit

Request: correct a misleading help message, without changing behavior.

The coordinator reads the root, foundation, project brief, and active work, then the relevant file. It frames the task in one sentence, edits the message, and checks the output or diff. It uses the small path: no spawned agents, decision record, or task directory. Its final response contains the change and validation. If it discovers the message reflects incorrect behavior, it promotes the work before proceeding.

## A consequential change

Request: make an existing CSV export handle large datasets while preserving its public behavior.

The coordinator selects the consequential path because data integrity, resource use, and a public output contract matter. It creates `project/tasks/2026-10-08-bounded-export/task.md`, registers it in WORK, and writes this framing before detailed searches:

- Desired behavior: export completes for the agreed large dataset.
- Constraints: preserve row order, escaping, authorization, and error behavior.
- Unknowns: where memory grows and whether the framework supports incremental output.
- Investigation: trace data access and output buffering; inspect tests and resource limits.
- Success: compatible output, bounded working memory, and correct cancellation behavior.

### Delegate evidence gathering

Illustrative scout packet:

```text
Task: 2026-10-08-bounded-export / scout-01
Role: scout; requested tier FAST; actual model resolved from RUNTIME
Goal: locate buffering and existing export contracts, not choose the architecture
Acceptance: source-backed answer, test entry points, remaining unknowns
Read first: AGENTS, foundation, scout role; relevant MAP excerpt below
Constraints: preserve authorization, CSV escaping, row order, failure behavior
Start sources: src/export.py and its callers; expand to relevant dependencies
Write only: project/tasks/2026-10-08-bounded-export/handoffs/scout-01.md
Stop: answer established, evidence conflicts, or two targeted search passes exhausted
Return: <=250 words plus source pointers; current handoff fields
Consumer: coordinator deciding the implementation boundary
```

The scout identifies an eager row list and a second full output buffer. It points to the symbols and existing tests, labels the resource-limit assumption as unknown, saves its handoff, and returns a short summary. The coordinator checks the decisive source locations. It does not ingest the scout's whole search transcript.

### Consult a fresh partner

The coordinator independently sends a STRONG partner the foundation and partner role inline, with this neutral problem:

> A service produces ordered tabular downloads. Input volume is growing; the output contract and access checks must remain compatible. What should we establish before selecting an approach to memory usage? Offer questions, at most two options, and checks that could rule them out. Do not read the repository or use tools.

The partner asks when response headers become irrevocable, whether data access is itself bounded, and how cancellation releases resources. It compares incremental output with background materialization. These are hypotheses, not code findings. The coordinator answers only the relevant neutral facts and concludes the exchange within two rounds.

The coordinator first persists the partner's read-only return. The task's decision brief then chooses incremental output based on source evidence, identifies partial-response failure as the main tradeoff, and states a revisit trigger if the storage layer cannot read incrementally. If this becomes a lasting public contract, a separate accepted decision records it.

### Build and integrate

Builder `builder-01` receives exclusive ownership of the affected implementation and test files. Once it stops editing and saves a `ready` handoff, a FAST verifier runs known commands, such as `python -m pytest tests/test_export.py`, from the project root. It records the actual exit result, timestamp, checked revision plus relevant dirty/untracked content fingerprints, and scope gaps. Memory characterization may need a separate measured check; passing compatibility tests alone proves no memory bound.

A STRONG reviewer receives acceptance criteria, the diff, and check evidence before the builder's rationale. It inspects resource release and partial-response handling. The coordinator resolves supported findings and checks the integrated result; any intervening edit invalidates affected earlier checks. Only the coordinator marks assignments `integrated`.

## An interrupted builder

Suppose the builder's handoff describes planned work, but its source edit landed before the session stopped. On resume, the coordinator checks the working tree and existing files before replaying anything. It confirms the previous writer stopped, records the partial change as applied but unverified, and assigns `builder-02` a different handoff. The original record remains available. If the old writer's state is unknown, work resumes in isolation instead of racing the writer.

If the completed scout handoff exists but its index update is missing, recovery finds it through the task directory and reconciles it. A missing index row or missing handoff never proves the source tree is clean.

## Closeout and drift

After acceptance and integration, the coordinator updates the export area's contract and its accepted decision link. It transfers any unresolved unrelated issue to WORK with a next action, then archives the whole closed task directory and repairs links. Active indexes contain no running narrative of completed work.

If a later change makes the documented command obsolete, the next affected task repairs it from manifest or CI evidence. After five standard/consequential completions, a curator checks the implicated context and resets the maintenance counter. It does not rewrite the foundation as part of pruning.

## Missing host features

With no model selection, the same packets use the available model and claim no savings. With no subagents, the coordinator runs the needed responsibilities sequentially. With no fresh conversation, the partner step becomes an explicitly labeled alternative-analysis self-check. With no worker write access, the coordinator saves its return. If no persistent writes are possible at all, the final response carries the checkpoint and discloses the missing persistence.

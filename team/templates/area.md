# Area: <name>

<!-- Copy on demand to the project's area-note location. Placeholders are not facts. Remove unused optional sections. Rebase relative links when copying or moving. Summarize current contracts and link sources; do not copy code or duplicate decision narratives. -->

- **Scope:** <responsibilities, boundaries, and excluded behavior>
- **Owner:** <responsible maintainer>
- **Last verified:** <timestamp with timezone>
- **Verified against:** <source paths and revision plus relevant dirty/untracked content fingerprints, or dated relevant-file fingerprints without VCS>

## Entrypoints

| Source or interface | Purpose |
| --- | --- |
| <relative link> | <where relevant behavior starts> |

## Contracts and invariants

<Inputs, outputs, interfaces, important error behavior, data/security boundaries, and compatibility requirements. Link authoritative source or accepted requirements for each material claim. Distinguish intended behavior from verified current behavior.>

## Dependencies and consumers

<Relevant upstream/downstream areas and external systems; link their contracts. Include cross-cutting constraints needed for safe changes.>

<For game areas, include relevant scene/asset identifiers, import/source relationships, simulation/lifecycle ownership, save or network schema, and target resource budgets. Omit absent systems.>

## Relevant commands

| Purpose | Exact command | CWD / prerequisites | Evidence of last verification |
| --- | --- | --- | --- |
| <focused check or operation> | <command> | <directory and requirements> | <timestamp/checkpoint, result, or explicitly unverified> |

## Decisions

<Links to accepted decisions explaining current constraints; mark proposed alternatives separately.>

## Unknowns and freshness

<Unverified claims, source contradictions, known limits, and conditions requiring revalidation. Link owned work for unresolved issues. Do not refresh verification dates without checking affected sources.>

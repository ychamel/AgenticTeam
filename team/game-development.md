# Game-development profile

Profile version: 1.2.0, on foundation 1.0.0. Read for game work; the coordinator passes only applicable constraints to workers. The foundation remains the shared quality contract.

## Frame the playable outcome

Define the player action, visible/audible feedback, success and failure states, and a small playable slice before choosing systems. Separate a design hypothesis ("this should feel responsive") from a measurable technical condition. Resolve uncertain feel with a bounded prototype or observed playtest; do not label an unplayed mechanic fun or balanced.

BRIEF holds game pillars, audience, core loop, target platforms/input, accessibility goals, engine/toolchain versions, and agreed budgets. MAP routes to code, scenes/levels, source assets, import settings, tests, and build recipes. Detailed systems and content contracts live in relevant area notes. Do not assume a genre, engine, multiplayer, determinism, or a target frame rate.

For a new nontrivial feature without an accepted design, use [branching exploration](design-exploration.md): independent concepts, targeted deeper branches, discovery exchange, coherent synthesis, and readiness review. Use [decomposition](design-decomposition.md) to preserve coverage and specify the whole agreed feature's behavior and contracts before sequencing implementation slices. Workers receive only relevant decisions. A slice is an intermediate milestone until the requested scope is satisfied or explicitly revised. Clear local fixes retain the small path.

## Engineering and content boundaries

- Make ownership of game state, simulation timing, presentation, and persistence explicit. Check lifecycle events such as spawn, despawn, pause, scene transitions, and device changes when affected.
- Keep tuning data and content references inspectable. Preserve identifiers, serialized schemas, and save compatibility unless the task authorizes a migration. Multiplayer, replay, and authority constraints apply only when the project uses them.
- Treat an editor save/import as a possible multi-file change. Assign related scenes, prefabs/resources, source assets, metadata, and generated output paths together. Inspect actual changes before accepting them; avoid concurrent writers to a shared scene or import/build output.
- Use existing engine/editor tooling for formats that cannot be safely edited as text. Never fabricate binary edits, import success, or engine execution. Missing editor access is a concrete limitation, not a passing check.
- Preserve source assets and provenance; record required license/attribution and import settings for new assets. Avoid committing disposable caches or build artifacts unless the project explicitly tracks them.

## Evidence and acceptance

Choose only checks affected by the change: code/data contracts, scene/import integrity, repeatable gameplay scenarios, target-build smoke tests, resource measurements, or observed player experience. Record build/revision, engine/toolchain, platform/hardware, scenario/scene, input method, seed when relevant, and relevant content/settings fingerprints. Omit irrelevant fields rather than expanding every handoff.

Editor success does not establish packaged-build compatibility. Code inspection does not establish player feel. An automated input run establishes only what it actually observes. For performance work, compare before/after under equivalent conditions and report frame-time distribution or spikes, resource usage, loading, and measurement limits as applicable; do not claim gains from intuition or a single unqualified FPS figure.

A hypothesis may remain pending while an implementation task closes only if its agreed acceptance does not require that evidence and the follow-up has an owner. Missing required playtesting, target hardware, or compatibility checks leaves acceptance incomplete.

## Activate only useful processes

Use [dispatch](dispatch.md) to select responsibilities. A tuning fix may need only a builder and a focused check. A new playable slice may benefit from a designer and playtester. Import failures route to content integration; unexplained stalls route to performance analysis. Keep automated verification, independent review, and player observations distinct; avoid a mandatory eleven-agent pipeline.

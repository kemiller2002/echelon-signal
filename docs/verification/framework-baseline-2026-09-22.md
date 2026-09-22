# Echelon Signal Framework Baseline Verification — 2026-09-22

This record captures the current-framework finalization performed from the then-current
`main` branch, preserving concurrent repository work rather than replaying an older
migration snapshot.

## Verified baseline

- Repository Operating System (ROS): 3.1.4
- State-Directed Engineering / Ordo execution package: 1.3.0
- Limen: 0.6.2

## Verification

- ROS 3.1.3 -> 3.1.4 lifecycle upgrade planned and applied through `ros upgrade`.
- ROS strict installation verification passed.
- SDE 1.3.0 strict verification passed.
- Limen 0.6.1 -> 0.6.2 lifecycle upgrade planned and applied through `limen upgrade`.
- Limen strict verification passed with explicit Signal engine/browser boundaries.
- ROS registries were rebuilt and checked.
- ROS unified repository validation passed.
- Repository diff whitespace checks passed except for pre-existing tool-owned SDE payload
  EOF whitespace, whose managed bytes are intentionally preserved.

## Boundary decisions

`src/Echelon.Signal.Engine` is the F#/.NET WebAssembly application-authority boundary.
It owns domain state, legal transitions, scoring, validation, privacy rules, capabilities,
obligations, effects-as-data, and view projection.

`src/Echelon.Signal.Browser` is the thin browser-facing boundary. Browser mechanisms are
provided through Limen; Signal domain decisions must not be re-derived there.

`tools/ros_cli.mjs` is excluded only from SDE structural-size review because it is retained
ROS compatibility tooling rather than Signal product code. Structural review remains strict
for supported Signal source paths.

## Trial observations

The finalization was deliberately rebased conceptually onto current `main` after detecting
substantial concurrent repository activity. This avoided overwriting newer requirements and
capability work with an older migration snapshot. That concurrency event is part of the ROS /
Ordo trial evidence for safe repository evolution.

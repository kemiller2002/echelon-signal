# Framework Baseline Verification — 2026-09-22

Echelon Signal framework lifecycle migration executed through GitHub Actions.

## Installed baseline

- Repository Operating System (ROS): 3.1.4
- State Directed Engineering / Ordo execution package: 1.3.0
- Limen: 0.6.2

## Verification performed

- ROS legacy configuration 0 -> 1 adoption completed through the supported ROS migration path.
- ROS strict installation verification passed after migration.
- SDE installation completed and strict verification passed.
- Limen installation completed and strict verification passed.
- ROS registries were rebuilt and checked.
- ROS repository validation passed.
- Repository whitespace validation passed.

## Structural review scope decision

`tools/ros_cli.mjs` is excluded from SDE-STRUCT-001 through repository-owned
`sde.config.json`. The file is retained as ROS legacy compatibility tooling and is
not Echelon Signal product code. All other supported source paths remain subject to
SDE structural review defaults.

## Framework-trial findings

- ROS 3.1.4 successfully adopted the real legacy installation without force or manual file deletion.
- ROS 3.1.0 had reported ten legacy files as blocking unmanaged conflicts; the 3.1.2+ legacy-adoption path eliminated those false conflicts by using the recorded legacy hashes.
- The current ROS 3.1.4 executable requires `work backlog-transition --action ready --id ID --occurred-at TIMESTAMP` for backlog mutation, while the current upstream `docs/work-backlog-guide.md` still demonstrates `work ready ID`. The executable contract was followed and the documentation mismatch is retained as ROS trial evidence.
- SDE strict structural review initially flagged `tools/ros_cli.mjs` (1,085 lines). That file is retained as ROS legacy compatibility tooling and is narrowly excluded from Signal product-code structural review rather than deleting it or disabling structural review globally.
- Limen's generated default boundary names `src/engine` and `src/kernel`, which did not yet exist. Signal replaces those placeholders with explicit `src/Echelon.Signal.Engine` and `src/Echelon.Signal.Browser` boundaries rather than weakening strict verification or reshaping the application around Limen's defaults.
- Four tool-owned SDE 1.3.0 payload Markdown files contain a trailing blank line that `git diff --cached --check` reports as whitespace. SDE strict verification requires those bytes to remain unchanged, so the migration staging guard permits whitespace findings only under `.sde/` and still rejects any repository-owned whitespace finding.

## Evidence authority

The GitHub Actions migration run is operational evidence. This document is the durable
repository summary; the installed manifests under `.echelon/` are the machine-readable
authority for exact installed versions and managed artifacts.

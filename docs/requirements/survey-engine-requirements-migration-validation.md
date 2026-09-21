# Survey engine requirements migration validation

Validated: 2026-08-31  
Work item: WI-0001  
Authoritative corpus: `input-documents/`

## Acceptance checks

| Check | Observed result | Status |
|---|---|---|
| Complete source inventory | 12 files discovered under `input-documents/`; 12 reviewed and included; 0 excluded | pass |
| Source completion markers | 12/12 files contain `Requirements-definition status: COMPLETED` | pass |
| Original source preservation | Source diffs contain appended migration blocks only; original line references remain pre-append locations | pass |
| Requirement-group parity | 72 unique group IDs in the central ledger, 72 in source appendices, and 72 in reciprocal work-item details | pass |
| Missing/extra group IDs | Set comparison between ledger, sources, and work-item details returned no differences | pass |
| Work-item coverage | WI-0002 through WI-0010 exist as captured ROS backlog records and each has a readable detail file | pass |
| Patch whitespace | `git diff --check` returned no findings | pass |

## Commands used

```bash
rg --files input-documents | sort
rg -l "Requirements-definition status: COMPLETED" input-documents | sort
rg -o '(AST|ACR|ARP|CAN|LURL|RPT|ANS|ALG|AUT|URLC|ID|VER)-[0-9]{3}' <target> | sort -u
comm -3 <ledger-groups> <source-groups>
comm -3 <ledger-groups> <work-item-detail-groups>
./ros work show WI-0010
./ros work list
git diff --check
```

## Interpretation

These checks establish migration accounting and reciprocal traceability. They do not establish implementation correctness for WI-0002 through WI-0010; those items remain captured and require their own evidence before completion.


## Extension review — 2026-09-21

A thirteenth authoritative requirement source was added:

`input-documents/survey-engine-advanced-ros-ordo-limen-stress-requirements.txt`

It contributes ARX-001 through ARX-012 and raises the accounted corpus from 72 to 84 requirement groups.

### Repository-API checks completed

| Check | Observed result | Status |
|---|---|---|
| Advanced source present | 1 new source containing ARX-001 through ARX-012 | pass |
| Central ledger mapping | All 12 ARX groups recorded in `docs/requirements/survey-engine-requirements-migration.md` | pass |
| Reciprocal work-item mapping | Advanced references appended to each affected WI-0002 through WI-0010 detail record | pass |
| No-PII boundary | New source explicitly forbids Echelon Signal from collecting, processing, persisting, logging, or exporting PII | pass |
| Framework baseline discovery | Legacy ROS install identified; current ROS, Ordo/SDE, and Limen release baselines recorded as trial inputs | pass |
| ROS live/projection consistency | `.ros/context/current.json` reports WI-0001 complete while `.ros/work/queue.md` reports active and `.ros/work/queue.json` retains ready | finding |

### Validation still required in a runnable checkout

The cloud GitHub connector can inspect and update repository files but cannot execute the repository's local lifecycle commands. Therefore the following are **not claimed as completed** by this extension review:

```bash
./ros registry build
./ros validate
./ros verify
git diff --check
```

ARX-001 intentionally requires upgrading the repository to the current ROS lifecycle before relying on legacy generated projections. After that upgrade, the stale WI-0001 projection observed above should be used as a concrete migration/repair test.

A skipped local command is unavailable evidence, not a pass.

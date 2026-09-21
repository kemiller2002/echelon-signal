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

It now contributes ARX-001 through ARX-014 and raises the accounted corpus from 72 to 86 requirement groups.

### Repository-API checks completed

| Check | Observed result | Status |
|---|---|---|
| Advanced source present | 1 new source containing ARX-001 through ARX-014 | pass |
| Central ledger mapping | All 14 ARX groups recorded in `docs/requirements/survey-engine-requirements-migration.md` | pass |
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


### ARX-013 extension check — 2026-09-21

The advanced source now also defines timer, pagination/progression, and banking requirements.

| Check | Observed result | Status |
|---|---|---|
| ItemsPerPage | Existing survey/per-section capability retained and strengthened to compose with banking and locking boundaries | pass |
| Question revisit policy | Independent forward-only question locking defined | pass |
| Section revisit policy | Independent forward-only section locking defined | pass |
| Timer | Survey/section/page/question scopes, explicit Clock evidence, resume policy, expiry transitions, and non-tamper-resistant browser limitation defined | pass |
| Question banking | Deterministic selection, constraints, seed/manifest reconstruction, authoring, scoring, and encoding behavior defined | pass |
| Section banking | Deterministic section selection and dependency validation defined | pass |
| Reciprocal traceability | ARX-013 mapped into WI-0002, WI-0003, WI-0004, WI-0006, WI-0007, and WI-0010 | pass |


### ARX-014 extension check — 2026-09-21

The advanced source now explicitly requires live incremental scoring and typed custom scoring expressions.

| Check | Observed result | Status |
|---|---|---|
| Incremental calculation | Authoritative F# score updates after every accepted answer and must equal full reference recomputation | pass |
| Incremental display option | ScoreDisplayPolicy includes AfterEachResponse plus hidden/page/section/final policies | pass |
| Partial score semantics | Provisional/final/unavailable status and explicit partial-response ScoreBasis defined | pass |
| Browser authority | Limen/TypeScript may render but may not calculate or independently cache scoring meaning | pass |
| Custom expression trees | Versioned serializable typed scoring AST required; arbitrary executable code and unrestricted System.Linq.Expressions payloads prohibited | pass |
| Publication validation | Type, reference, phase, cycle, deterministic-operator, and resource checks required before publication | pass |
| Incremental dependency graph | Custom expressions mechanically expose dependencies and participate in optimized invalidation | pass |
| Expression versioning | Published template binds to ScoringExpressionLanguageVersion and result lineage records it | pass |
| Differential verification | Reference, optimized, incremental, and serialized F# WASM scoring required to agree | pass |
| Reciprocal traceability | ARX-014 mapped into WI-0002, WI-0003, WI-0004, WI-0006, WI-0007, and WI-0010 | pass |

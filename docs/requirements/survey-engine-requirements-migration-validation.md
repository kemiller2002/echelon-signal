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


## Scoring and selector completeness review — 2026-09-22

A fifteenth authoritative requirement source was added:

`input-documents/survey-engine-scoring-selector-completeness-requirements.txt`

It contributes SCS-001 through SCS-019 and raises the accounted corpus to 183 requirement groups across 15 authoritative sources.

### Completeness checks

| Check | Observed result | Status |
|---|---|---|
| SCS group sequence | 19 unique groups, exactly SCS-001 through SCS-019, contiguous with no duplicates | pass |
| Central ledger mapping | Every SCS group appears in the central migration ledger | pass |
| Reciprocal work-item mapping | SCS requirements mapped into affected WI-0002, WI-0003, WI-0004, WI-0007, and WI-0010 detail records | pass |
| Basic scoring catalog | Direct/map/progress, sum/count, mean/weighted/median/min/max, percentage/normalization, reverse/bounds, threshold/pass-fail, section/domain/profile/composite included | pass |
| Moderate scoring catalog | Robust aggregates, difference/ratio/index/target, bonus/penalty/negative marking, top/bottom/favorable/net favorable, NPS, ranking/allocation/pairwise/best-worst, benchmark standardization included | pass |
| Assessment scoring | Correct/incorrect, blank policy, exact set, any/all/none, option weights, partial credit and penalty modes included | pass |
| Special-state semantics | Unanswered, N/A, Don't Know, Prefer Not to Answer/Declined and flow exclusion remain distinct | pass |
| Selector primitives | Existing primitives retained; finite BoundedDecimal and BoundedRange added without proliferating visual selector types into domain primitives | pass |
| Common selector families | Binary/tri-state, generic Likert, semantic differential, numeric/NPS/star/icon/slider, single/multi choice variants included | pass |
| Structured selectors | Matrix/grid, ranking, constant-sum allocation, pairwise, best-worst, hierarchical single/multi included | pass |
| Multi-choice constraints | exact/at-least/at-most/between and mutually exclusive/none/N-A options included | pass |
| Matrix variants | single, dropdown, multi, Likert, semantic differential, numeric rating and side-by-side included | pass |
| Accessibility contract | no drag-only, no visual-only semantics, explicit keyboard/screen-reader/touch/zoom/reflow/reduced-motion requirements | pass |
| UI/domain boundary | Web components emit typed events and render projected state; F# retains scoring/answer/applicability/completion authority | pass |
| Encoding | finite cardinality, deterministic encoding and worst-case URL-budget checks required for every new selector | pass |
| No-PII boundary | No free-text/contact/signature/upload/geolocation/identity primitive added | pass |
| Advanced-boundary clarity | IRT/Rasch, Bayesian/ML, advanced preference estimation, NLP and other advanced scoring explicitly remain separate requirements | pass |

### Automated repository-content assertions

The repository API validation used the new source and ledger to assert:

- exactly 19 SCS group headings,
- first group SCS-001,
- last group SCS-019,
- contiguous numbering,
- all 19 groups present in the central ledger,
- central ledger source count = 15,
- central ledger requirement-group count = 183,
- required completeness terms present for correctness/partial-credit, weighted top-box, NPS, percentile/Z/T, semantic differential, star/icon/slider, matrix/dropdown/side-by-side, hierarchical single/multi, selection cardinality, best-worst, Prefer Not to Answer, BoundedDecimal, and BoundedRange.

No assertion failed.

### External taxonomy cross-check

The completeness pass was cross-checked against current mainstream survey-platform question/scoring taxonomies for:

- multiple/single choice and dropdowns,
- checkbox/multiple response,
- matrix/rating scales and bipolar matrices,
- star/icon ratings and sliders,
- ranking,
- best-worst choice,
- constant-sum allocation,
- generic Likert scales,
- NPS,
- top-box/top-two-box and related favorable metrics.

Those products are comparison inputs only. Signal's deterministic F# semantics, immutable templates, no-PII policy, URL-state model, accessibility constraints, Ordo/Limen boundaries, and publication validation remain authoritative.

### Interpretation

This review establishes requirement-catalog completeness for basic and moderate scoring and closed-ended selector/question styles. It does not claim implementation exists. The mapped delivery work items remain responsible for implementation and acceptance evidence.


### ROS 3.1.4 attribution-policy migration finding

During completion of `SIGNAL-SCORING-SELECTORS-2026-09-22`, the first post-completion validation reported the work item's own finalized telemetry execution as an unattributed meaningful change.

Investigation confirmed that the current ROS 3.1.4 greenfield `ros.json` template excludes machine-owned:

- `.ros/telemetry/**`,
- `.ros/locks/**`,
- `.echelon/**`

from work-attribution checks, while Echelon Signal's older shared `ros.json` still excluded only context/events/work/registries.

Signal's attribution exclusions were aligned to the current ROS 3.1.4 policy. This does not exempt product, requirement, test, or application files from attribution; it prevents ROS machine-generated lifecycle metadata from recursively requiring its own work attribution.

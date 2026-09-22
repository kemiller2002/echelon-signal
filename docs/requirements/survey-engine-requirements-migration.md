# Survey engine requirements migration ledger

Status: requirements-definition migration completed through 2026-09-22 administrator extension  
Original migration completed: 2026-08-31  
Latest reconciliation completed: 2026-09-22  
Authoritative corpus: `input-documents/`  
Migration work item: WI-0001

## Meaning of completion

“Requirements-definition completed” means every actionable requirement in each source file has been assigned to at least one ROS work item. It does not mean the requirement is implemented, accepted as repository architecture, or verified in running software. All created delivery items remain in the local ROS backlog for prioritization.

Original source content is preserved. Each source received only an appended migration appendix; the line references below are the original pre-append line numbers.

## Complete corpus coverage

No file under `input-documents/` is excluded. The original 12-file corpus was reviewed completely on 2026-08-31; the advanced ROS/Ordo/Limen stress-trial extension was added and reviewed on 2026-09-21; the administrator console/storage/analytics/visualization extension was added and reviewed on 2026-09-22, bringing the authoritative corpus to 14 files. All 14 authoritative sources are migrated to ROS work items.

| Authoritative source | Migration status | Requirement groups | ROS work items |
|---|---|---|---|
| `input-documents/echelon-survey-scoring-expression-tree-approach.txt` | requirements-definition completed | AST-001, AST-002, AST-003, AST-004, AST-005, AST-006 | WI-0002, WI-0003, WI-0007, WI-0010 |
| `input-documents/survey-engine-additional-core-requirements.txt` | requirements-definition completed | ACR-001, ACR-002, ACR-003, ACR-004, ACR-005, ACR-006, ACR-007, ACR-008, ACR-009 | WI-0002, WI-0003, WI-0004, WI-0005, WI-0006, WI-0007, WI-0008, WI-0010 |
| `input-documents/survey-engine-admin-result-persistence-model.txt` | requirements-definition completed | ARP-001, ARP-002, ARP-003, ARP-004, ARP-005, ARP-006 | WI-0002, WI-0004, WI-0005, WI-0007, WI-0008, WI-0009, WI-0010 |
| `input-documents/survey-engine-canonical-architecture.txt` | requirements-definition completed | CAN-001, CAN-002, CAN-003, CAN-004, CAN-005, CAN-006, CAN-007, CAN-008 | WI-0002, WI-0003, WI-0004, WI-0005, WI-0006, WI-0007, WI-0008, WI-0009, WI-0010 |
| `input-documents/survey-engine-live-url-state-lifecycle.txt` | requirements-definition completed | LURL-001, LURL-002, LURL-003, LURL-004, LURL-005 | WI-0002, WI-0004, WI-0005, WI-0008, WI-0009, WI-0010 |
| `input-documents/survey-engine-reporting-requirements-data-contract.txt` | requirements-definition completed | RPT-001, RPT-002, RPT-003, RPT-004, RPT-005, RPT-006 | WI-0002, WI-0005, WI-0008, WI-0009, WI-0010 |
| `input-documents/survey-engine-requirements.txt` | requirements-definition completed | ANS-001, ANS-002, ANS-003, ANS-004, ANS-005 | WI-0002, WI-0004, WI-0007 |
| `input-documents/survey-engine-scoring-algorithms.txt` | requirements-definition completed | ALG-001, ALG-002, ALG-003, ALG-004 | WI-0003, WI-0007, WI-0010 |
| `input-documents/survey-engine-template-authoring-publication-workflow.txt` | requirements-definition completed | AUT-001, AUT-002, AUT-003, AUT-004, AUT-005, AUT-006, AUT-007 | WI-0003, WI-0004, WI-0006, WI-0007, WI-0009, WI-0010 |
| `input-documents/survey-engine-url-submission-requirement-changes.txt` | requirements-definition completed | URLC-001, URLC-002, URLC-003, URLC-004, URLC-005 | WI-0002, WI-0003, WI-0004, WI-0005, WI-0006, WI-0007, WI-0008, WI-0010 |
| `input-documents/survey-group-identity-anonymous-submissions.txt` | requirements-definition completed | ID-001, ID-002, ID-003, ID-004 | WI-0004, WI-0005, WI-0008, WI-0009, WI-0010 |
| `input-documents/survey-instance-template-versioning-requirements.txt` | requirements-definition completed | VER-001, VER-002, VER-003, VER-004, VER-005, VER-006, VER-007 | WI-0002, WI-0003, WI-0004, WI-0005, WI-0006, WI-0007 |
| `input-documents/survey-engine-advanced-ros-ordo-limen-stress-requirements.txt` | requirements-definition completed | ARX-001 through ARX-014 | WI-0002, WI-0003, WI-0004, WI-0005, WI-0006, WI-0007, WI-0008, WI-0009, WI-0010 |
| `input-documents/survey-engine-administrator-console-storage-analytics-visualization-requirements.txt` | requirements-definition completed | ADM-001 through ADM-076 | WI-0011 through WI-0020 |

## Work-item decomposition

| Work item | Delivery scope |
|---|---|
| WI-0002 | Canonical survey domain contracts and F# module boundaries |
| WI-0003 | Template authoring, publication, versioning, and compatibility |
| WI-0004 | Answer model, URL encoding, and live respondent lifecycle |
| WI-0005 | Identity, anonymity, roles, and group semantics |
| WI-0006 | Deterministic rules, validation, flow, completion, and recommendations |
| WI-0007 | Scoring engine, result semantics, and explainability |
| WI-0008 | Administrator import, aggregation, and report-state persistence |
| WI-0009 | Reporting contract, privacy, comparisons, and renderers |
| WI-0010 | Cross-cutting test, performance, security, migration, and acceptance program |
| WI-0011 | Administrator application state, group management, and Limen UX |
| WI-0012 | Storage provider contract and GitHub repository provider |
| WI-0013 | Administrator import, concurrency, durable aggregation, and indexes |
| WI-0014 | Administrator analytics, comparisons, lineage, and dependency invalidation |
| WI-0015 | Typed visualization grammar, dashboards, and accessibility |
| WI-0016 | Report builder, snapshots, exports, configuration packages, and policy packs |
| WI-0017 | Administrator privacy, security, audit, retention, and deletion lifecycle |
| WI-0018 | Storage migration, backup, schema evolution, and operational recovery |
| WI-0019 | Administrator sandbox, synthetic data, advanced analytics extensions, and phase boundary |
| WI-0020 | Administrator cross-cutting verification, performance, and acceptance program |

## Requirement accounting rule

Each row below is a requirement group. The mapping applies to every actionable/normative statement, listed invariant, required field, validation rule, test obligation, and explicit “must/should” behavior in the cited section and original line range. Examples and rationale are retained as design context for the same work item. A row assigned to multiple work items is a cross-cutting requirement; no single item may claim it is satisfied until its own acceptance criteria cover its portion.

| Requirement group | Exact source file | Exact source section/requirement | Original lines | Accounted requirement | ROS work items |
|---|---|---|---:|---|---|
| AST-001 | `input-documents/echelon-survey-scoring-expression-tree-approach.txt` | §§1–5, Purpose through Why Not Use System.Linq.Expressions Directly | 9–175 | Hybrid standard/parameterized/custom scoring architecture; persisted format excludes executable and CLR-coupled representations. | WI-0007, WI-0010 |
| AST-002 | `input-documents/echelon-survey-scoring-expression-tree-approach.txt` | §§6–11, Typed Expression Model through Complexity Limits | 177–331 | Typed, constrained, pure scoring AST; validation and resource limits. | WI-0007, WI-0010 |
| AST-003 | `input-documents/echelon-survey-scoring-expression-tree-approach.txt` | §§12–17, Standard Scorer Registry through Separate Answer Selectors From Scoring | 333–490 | Stable/versioned scorer registry, explicit missing-answer policy, multi-level results, and separation of scoring, interpretation, and selectors. | WI-0007 |
| AST-004 | `input-documents/echelon-survey-scoring-expression-tree-approach.txt` | §§18–21, Custom Rule Example through Testing Strategy | 492–585 | AST-first design, existing-survey characterization migration, unit/table/property tests. | WI-0007, WI-0010 |
| AST-005 | `input-documents/echelon-survey-scoring-expression-tree-approach.txt` | §§22–28, Diagnostics and Explainability through What Not to Build | 587–726 | Single-path diagnostics, authoring support, WASM performance, trust boundary, explicit errors, and standard/custom boundary. | WI-0003, WI-0007, WI-0010 |
| AST-006 | `input-documents/echelon-survey-scoring-expression-tree-approach.txt` | §§29–32, Proposed Architecture through Summary Decision | 728–862 | End-to-end scoring architecture, phased implementation, unresolved characterization questions, and summary decision. | WI-0002, WI-0007, WI-0010 |
| ACR-001 | `input-documents/survey-engine-additional-core-requirements.txt` | §§1–4, Survey Flow and Branching through Completion Rules | 23–331 | Declarative deterministic flow, derived facts, answer/cross-question validation, and explicit completion. | WI-0006 |
| ACR-002 | `input-documents/survey-engine-additional-core-requirements.txt` | §§5–6, Respondent/Subject/Role Semantics and Survey Group Semantics | 333–449 | Optional respondent/subject/role semantics and expressive group dependencies. | WI-0005 |
| ACR-003 | `input-documents/survey-engine-additional-core-requirements.txt` | §§7–11, Template Provenance through Self-Contained Published Templates | 451–653 | Template lineage, schema/engine compatibility, capabilities, and immutable dependency resolution. | WI-0003 |
| ACR-004 | `input-documents/survey-engine-additional-core-requirements.txt` | §§12–13, URL Response Integrity and URL Payload Version | 655–742 | Corruption/authenticity separation, survey-specific integrity policy, and response encoding version. | WI-0004, WI-0010 |
| ACR-005 | `input-documents/survey-engine-additional-core-requirements.txt` | §§14–15, Submission and Replay Policy and Response Revision Semantics | 744–789 | Earlier respondent-side replay/revision model, migrated with the explicit modifications in URLC-001/URLC-002. | WI-0008 |
| ACR-006 | `input-documents/survey-engine-additional-core-requirements.txt` | §§16–18, Randomization through Accessibility | 791–905 | V1 randomization constraints, immutable localization semantics, and accessible presentation contract. | WI-0003, WI-0010 |
| ACR-007 | `input-documents/survey-engine-additional-core-requirements.txt` | §§19–21, Recommendation/Action Rules through Rule Dependency Validation | 907–1034 | Engine-owned recommendations/actions, deterministic evaluation order, and cycle rejection. | WI-0006 |
| ACR-008 | `input-documents/survey-engine-additional-core-requirements.txt` | §§22–25, Publication Validation and recommended template/instance/group fields | 1036–1200 | Comprehensive publication gates and candidate canonical fields. | WI-0002, WI-0003, WI-0005 |
| ACR-009 | `input-documents/survey-engine-additional-core-requirements.txt` | §26, priorities, and Overall Architectural Principle | 1202–1295 | Cross-cutting invariants, ordered pre-reporting priorities, and deterministic immutable-input rule. | WI-0002, WI-0003, WI-0004, WI-0005, WI-0006, WI-0007, WI-0008, WI-0010 |
| ARP-001 | `input-documents/survey-engine-admin-result-persistence-model.txt` | §§1–16, Core Administrator Pipeline through SurveyGroupResult | 21–295 | Import pipeline and SurveyResult/SurveyGroupResult contracts, acceptance, validation, result shapes, facts, and recommendations. | WI-0002, WI-0007, WI-0008 |
| ARP-002 | `input-documents/survey-engine-admin-result-persistence-model.txt` | §§17–31, ExpectedSurveyCount through Result Version | 296–486 | Counts, identity modes, completion, deduplication, aggregates, coverage/confidence, template summary, and result schema version. | WI-0005, WI-0007, WI-0008 |
| ARP-003 | `input-documents/survey-engine-admin-result-persistence-model.txt` | §§32–40, AdminReportState through Submission Retention Policy | 487–609 | Report-state projection/source-of-truth layers, reproducibility, and privacy/audit retention policy. | WI-0008, WI-0009, WI-0010 |
| ARP-004 | `input-documents/survey-engine-admin-result-persistence-model.txt` | §§41–57, Report Persistence Strategy through Compact Identity Fingerprints | 610–800 | Embedded/external persistence parity, size-based escalation, store abstraction, resume, and accepted identity state. | WI-0004, WI-0008, WI-0010 |
| ARP-005 | `input-documents/survey-engine-admin-result-persistence-model.txt` | §§58–69, Import Errors through Core Invariants | 801–988 | Explicit import errors, group enforcement, minimal state, reporting boundaries, F# types, and administrator invariants. | WI-0005, WI-0008, WI-0009 |
| ARP-006 | `input-documents/survey-engine-admin-result-persistence-model.txt` | §70, Guiding Principle | 989–1003 | Raw respondent submission to deterministic results and persistence-transparent reporting. | WI-0008 |
| CAN-001 | `input-documents/survey-engine-canonical-architecture.txt` | §§1–7, Architectural Model through Selectors | 7–248 | Canonical domain/template/section/question/answer/selector contracts and compatibility metadata. | WI-0002, WI-0003, WI-0004 |
| CAN-002 | `input-documents/survey-engine-canonical-architecture.txt` | §§8–14, Scoring through Evaluation Order | 250–511 | Scoring catalog, derived facts, flow, validation, recommendations, typed shared AST, and deterministic evaluation order. | WI-0006, WI-0007 |
| CAN-003 | `input-documents/survey-engine-canonical-architecture.txt` | §§15–19, Survey Instance through Template Reference in URL | 513–609 | Instance/group identity and submission/template-reference contracts. | WI-0002, WI-0004, WI-0005 |
| CAN-004 | `input-documents/survey-engine-canonical-architecture.txt` | §§20–27, Answer Encoding through Submission Hash and Import | 611–769 | Bit packing, special/advanced answers, URL-safe serialization, versioning, integrity, URL budgets, and import hash. | WI-0004, WI-0008, WI-0010 |
| CAN-005 | `input-documents/survey-engine-canonical-architecture.txt` | §§28–29, Publication Validation and Canonicalization/Publishing | 771–891 | Complete validation gates and deterministic immutable publishing sequence. | WI-0003, WI-0010 |
| CAN-006 | `input-documents/survey-engine-canonical-architecture.txt` | §§30–38, Canonical Survey Result through Reporting Boundary | 893–1144 | Canonical results, shapes, coverage/confidence, explainability/errors, F# modules, and reporting responsibility boundary. | WI-0002, WI-0007, WI-0008, WI-0009 |
| CAN-007 | `input-documents/survey-engine-canonical-architecture.txt` | §§39–40, Recommended Implementation Order and Required Tests | 1145–1200 | Ordered delivery, representative fixtures, contract/property tests, and reproducibility checks. | WI-0010 |
| CAN-008 | `input-documents/survey-engine-canonical-architecture.txt` | §§41–42, Core Invariants and Canonical Architectural Principle | 1201–1258 | Twenty-five cross-cutting invariants and deterministic-interpreter architecture. | WI-0002, WI-0003, WI-0004, WI-0005, WI-0006, WI-0007, WI-0008, WI-0009, WI-0010 |
| LURL-001 | `input-documents/survey-engine-live-url-state-lifecycle.txt` | §§1–12, Core Principle through Stronger Canonical Statement | 9–201 | Continuously synchronized canonical respondent URL, resume/load flow, replace-history behavior, minimal state, and derived completion. | WI-0004 |
| LURL-002 | `input-documents/survey-engine-live-url-state-lifecycle.txt` | §§13–20, Anonymous Survey Behavior through Anonymous Finalization | 202–345 | Anonymous live URL versus finalized unlinkable submission and identified/anonymous finalization shapes. | WI-0004, WI-0005 |
| LURL-003 | `input-documents/survey-engine-live-url-state-lifecycle.txt` | §§21–28, Administrator Import Pipeline through Anonymous Duplicate Limitation | 346–489 | Import/results pipeline, derived administrator state, persistence escalation, source-of-truth boundary, and deduplication tradeoffs. | WI-0005, WI-0008 |
| LURL-004 | `input-documents/survey-engine-live-url-state-lifecycle.txt` | §§29–33, URL Encoding Infrastructure through Round-Trip Invariant | 491–560 | Deterministic compact versioned performant encoding, incremental evaluation, URL reconstruction, and round-trip properties. | WI-0004, WI-0010 |
| LURL-005 | `input-documents/survey-engine-live-url-state-lifecycle.txt` | §§34–36, Final Architecture through Guiding Principle | 561–640 | End-to-end respondent/admin architecture and 22 lifecycle core requirements. | WI-0002, WI-0004, WI-0005, WI-0008, WI-0009 |
| RPT-001 | `input-documents/survey-engine-reporting-requirements-data-contract.txt` | §§1–10, Reporting Boundary through Core Report Blocks | 9–188 | Reporting responsibility boundary, result inputs, audiences, and composable report blocks. | WI-0002, WI-0009 |
| RPT-002 | `input-documents/survey-engine-reporting-requirements-data-contract.txt` | §§11–20, ReportHeader through Coverage and Confidence | 190–355 | Core block field contracts, meaningful aggregates, semantic strengths/weaknesses/recommendations, and confidence separation. | WI-0009 |
| RPT-003 | `input-documents/survey-engine-reporting-requirements-data-contract.txt` | §§21–35, Comparisons through Audit Metadata Block | 357–582 | Comparison/benchmark compatibility, anonymous suppression, identity joins, methodology, and audit metadata. | WI-0005, WI-0009 |
| RPT-004 | `input-documents/survey-engine-reporting-requirements-data-contract.txt` | §§36–47, Report Definition through No Hidden Recalculation | 584–742 | Declarative/versioned report definitions, visibility/detail/localization/exports, rendering contract, and comparison-provider boundary. | WI-0009 |
| RPT-005 | `input-documents/survey-engine-reporting-requirements-data-contract.txt` | §§48–61, Rounding Rules through Report Extensibility | 743–934 | Explicit missing/sample/warning/status semantics, partial/final reports, snapshots, privacy classes, performance, caching, and extensibility. | WI-0009, WI-0010 |
| RPT-006 | `input-documents/survey-engine-reporting-requirements-data-contract.txt` | §§62–71, Initial V1 Report Types through Guiding Principle | 936–1097 | V1 reports, persistence parity, minimum report contract, 20 reporting invariants, and deterministic render flow. | WI-0005, WI-0008, WI-0009 |
| ANS-001 | `input-documents/survey-engine-requirements.txt` | Core Constraint through Special Answer States | 3–309 | URL-state/template-meaning separation, compact answer primitives, and distinct unanswered/N/A/Don't Know states. | WI-0004 |
| ANS-002 | `input-documents/survey-engine-requirements.txt` | Recommended Selector Presets | 311–659 | Selector presets over reusable answer primitives, including advanced ranking/allocation/pairwise forms. | WI-0004 |
| ANS-003 | `input-documents/survey-engine-requirements.txt` | Default Scoring Strategies | 661–806 | Standard unscored/direct/reverse/binary/weighted/mapped/multi-select/aggregate/normalized scoring. | WI-0007 |
| ANS-004 | `input-documents/survey-engine-requirements.txt` | Recommended Defaults through N/A and Missing-State Encoding | 808–933 | V1 defaults, prevention of selector-type proliferation, compact deterministic bit packing, cardinality, and special-state encoding. | WI-0004 |
| ANS-005 | `input-documents/survey-engine-requirements.txt` | Scoring Should Be Explicit through Guiding Principles | 935–997 | Explicit scoring declarations, architectural separation, decode/evaluate pipeline, and ten guiding principles. | WI-0002, WI-0004, WI-0007 |
| ALG-001 | `input-documents/survey-engine-scoring-algorithms.txt` | Purpose/Core Design and Recommended Built-In Algorithms for V1 | 3–320 | Separation of scoring concerns and twelve primary V1 algorithms/result patterns. | WI-0007 |
| ALG-002 | `input-documents/survey-engine-scoring-algorithms.txt` | Advanced Built-In Algorithms | 322–777 | Advanced reusable aggregation, weakest-link, maturity, rule, preference, rank/allocation, and confidence/completeness algorithms. | WI-0007 |
| ALG-003 | `input-documents/survey-engine-scoring-algorithms.txt` | Weakest-Link Scoring through Example Composition | 779–995 | Weakness-preserving semantics, result shapes/direction, composable primitives, and example compositions. | WI-0007 |
| ALG-004 | `input-documents/survey-engine-scoring-algorithms.txt` | Precompiled Algorithms through Guiding Principles | 997–1112 | Precompiled/declarative/custom boundary, authoring catalog, WASM-safe custom rules, and final scoring principles. | WI-0003, WI-0007, WI-0010 |
| AUT-001 | `input-documents/survey-engine-template-authoring-publication-workflow.txt` | §§1–9, Core Authoring Principle through Parent Lineage | 13–220 | Immutable compiled-artifact lifecycle, no-PII identity boundary, workspace, survey creation/versioning, and lineage. | WI-0003 |
| AUT-002 | `input-documents/survey-engine-template-authoring-publication-workflow.txt` | §§10–19, Section Authoring through Presentation Authoring | 222–412 | Authoring capabilities for sections/questions/selectors/scoring/rules/facts/recommendations/completion/presentation. | WI-0003, WI-0004, WI-0006, WI-0007, WI-0009 |
| AUT-003 | `input-documents/survey-engine-template-authoring-publication-workflow.txt` | §§20–31, Preview Mode through PII-Like Prompt Warning | 414–597 | Preview/test isolation, score/rule traces, simulation fixtures/assertions, URL capacity, no free text, and PII safeguards. | WI-0003, WI-0007, WI-0010 |
| AUT-004 | `input-documents/survey-engine-template-authoring-publication-workflow.txt` | §§32–43, Structural Validation through Canonicalization Preview | 599–726 | Full structural/semantic/compatibility/encoding/privacy validation and deterministic hash/layout preview. | WI-0003, WI-0010 |
| AUT-005 | `input-documents/survey-engine-template-authoring-publication-workflow.txt` | §§44–55, Template Diff through Publication Confirmation | 728–919 | Semantic/scoring/encoding/presentation diffs, comparability, validation report, blockers/warnings, and publication transaction. | WI-0003, WI-0010 |
| AUT-006 | `input-documents/survey-engine-template-authoring-publication-workflow.txt` | §§56–70, Superseding through Deterministic Publication | 920–1101 | Immutable supersession/rollback/deletion rules, test-mode isolation, cross-device checks, permissions/review, reports, fixtures, and deterministic publication. | WI-0003, WI-0009, WI-0010 |
| AUT-007 | `input-documents/survey-engine-template-authoring-publication-workflow.txt` | §§71–73, Core Authoring Invariants through Guiding Principle | 1103–1165 | Twenty-eight authoring invariants, V1 workflow, and quality-before-publication principle. | WI-0003, WI-0010 |
| URLC-001 | `input-documents/survey-engine-url-submission-requirement-changes.txt` | Core Submission Model and Requirements to Delete | 15–130 | URL transport model; removes required server-side response persistence, in-progress state, submission count, completion lock, and resume state. | WI-0004, WI-0008 |
| URLC-002 | `input-documents/survey-engine-url-submission-requirement-changes.txt` | Requirements to Alter §§1–10 | 134–367 | Logical response/portable submission distinction; derived status/completion; import-side replay/revision/integrity/template/group semantics. | WI-0004, WI-0008 |
| URLC-003 | `input-documents/survey-engine-url-submission-requirement-changes.txt` | New Requirements §§1–15 | 371–633 | Self-contained versioned portable URL envelope, explicit decode/integrity/authenticity, portability/resume/import/deduplication, and optional admin persistence. | WI-0004, WI-0008, WI-0010 |
| URLC-004 | `input-documents/survey-engine-url-submission-requirement-changes.txt` | Revised Domain/Data Ownership/Interpretation and Requirements That Remain Unchanged | 635–740 | Revised canonical entities and deterministic ownership equation while preserving immutable template/rule/scoring requirements. | WI-0002, WI-0003, WI-0004, WI-0005, WI-0006, WI-0007 |
| URLC-005 | `input-documents/survey-engine-url-submission-requirement-changes.txt` | Most Important Architectural Changes and Core Invariant | 743–781 | URL artifact, no server respondent state, submission domain, integrity/template resolution, admin persistence boundary, and foundational invariant. | WI-0002, WI-0004, WI-0008 |
| ID-001 | `input-documents/survey-group-identity-anonymous-submissions.txt` | §§1–5, Core Principle through Identified Survey Flow | 9–67 | Instance-not-person identity, group/instance fields, external administrator mapping, and identified submission. | WI-0005 |
| ID-002 | `input-documents/survey-group-identity-anonymous-submissions.txt` | §§6–13, Anonymous Requirement through URL Exclusions | 68–190 | Unlinkable anonymous final submission, random anonymous identity, identity modes/shapes, and PII exclusions. | WI-0004, WI-0005 |
| ID-003 | `input-documents/survey-group-identity-anonymous-submissions.txt` | §§14–22, Group Counts through Reporting Implication | 191–313 | Counts, import-side deduplication, privacy boundary/configuration, anonymous conversion/randomness tests, and anonymous report limits. | WI-0005, WI-0008, WI-0009, WI-0010 |
| ID-004 | `input-documents/survey-group-identity-anonymous-submissions.txt` | §§23–25, Core Requirements through Guiding Principle | 314–363 | Fifteen identity requirements, canonical identified/anonymous model, and engine identity principle. | WI-0005 |
| VER-001 | `input-documents/survey-instance-template-versioning-requirements.txt` | Core Entities | 28–163 | Template and instance identities, stable SurveyIdentifier, exact TemplateVersion, and deterministic TemplateHash. | WI-0002 |
| VER-002 | `input-documents/survey-instance-template-versioning-requirements.txt` | Published Immutability through Compact Hash Reference | 165–364 | Immutable lifecycle/version creation, canonical hashing, exact-template interpretation, and compact verifiable references. | WI-0003 |
| VER-003 | `input-documents/survey-instance-template-versioning-requirements.txt` | Survey Instance Runtime Information | 366–479 | Earlier candidate runtime/status/resume/edit/result fields, constrained by URLC-001/URLC-002 and LURL-001. | WI-0002, WI-0003 |
| VER-004 | `input-documents/survey-instance-template-versioning-requirements.txt` | Survey Template Information and Pagination | 481–604 | Complete interpretive template contents and presentation-only pagination/navigation/randomization behavior. | WI-0002, WI-0003 |
| VER-005 | `input-documents/survey-instance-template-versioning-requirements.txt` | Sections and Section/Survey-Level Scoring | 606–859 | First-class sections, applicability, explicit section scoring policies, and survey-level hierarchy. | WI-0002, WI-0007 |
| VER-006 | `input-documents/survey-instance-template-versioning-requirements.txt` | Survey Group through Result Shapes | 861–1052 | Group ordering/requirements/completion/scoring, explicit completion/validation, and scalar/categorical/profile/composite results. | WI-0005, WI-0006, WI-0007 |
| VER-007 | `input-documents/survey-instance-template-versioning-requirements.txt` | Survey Response through Guiding Principle | 1054–1134 | Minimal response/model and fifteen invariants, with physical persistence and anonymous identity refined by URLC/LURL/ID groups. | WI-0002, WI-0004 |


## 2026-09-21 advanced ROS / Ordo / Limen extension

The thirteenth authoritative source was added after the original migration specifically to turn Echelon Signal into an engineering-system stress trial. These requirements are additive and have reciprocal references in the existing WI-0002 through WI-0010 detail records.

| Requirement group | Exact source section | Accounted requirement | ROS work items |
|---|---|---|---|
| ARX-001 | Engineering-System Trial Baseline | Current verified ROS/Ordo/Limen lifecycle baseline, CI verification, and durable framework-friction evidence. | WI-0010 |
| ARX-002 | Ordo State, Capability, Obligation, and Knowledge Model | Explicit legal state/transitions, derived capabilities, obligations, unknown effects, and scoped negative knowledge. | WI-0002, WI-0006, WI-0010 |
| ARX-003 | Limen as the Only Browser Authority Boundary | F# application authority, serialized F# WASM boundary, no TypeScript domain fallback, and full used-capability conformance. | WI-0002, WI-0004, WI-0010 |
| ARX-004 | Required New Browser Capabilities | Generic focus, cryptographic entropy, and explicit clock evidence when time-based policy is activated. | WI-0004, WI-0005, WI-0010 |
| ARX-005 | Publication-Time Execution Plan and Incremental Evaluation | Reproducible execution plan, reference/optimized equivalence, dependency invalidation, and full/incremental equivalence. | WI-0003, WI-0006, WI-0007, WI-0010 |
| ARX-006 | Deterministic Numeric, Canonicalization, and Hash Semantics | Exact numeric/byte semantics, golden canonical vectors, and layered semantic/encoding/presentation/report/execution hashes. | WI-0003, WI-0007, WI-0010 |
| ARX-007 | URL Confidentiality, Browser History, and Concurrent Sessions | Fragment-first answer state, leakage controls, history semantics, multi-tab divergence, and stale-effect rejection. | WI-0004, WI-0005, WI-0010 |
| ARX-008 | Transactional Import, Idempotency, and Unknown External Effects | Explicit import acceptance state machine, idempotency, optimistic concurrency, and OutcomeUnknown reconciliation. | WI-0008, WI-0010 |
| ARX-009 | No-PII Privacy Hardening and Anonymous Inference Protection | System-wide no-PII enforcement, differencing-aware anonymity, and answer-free telemetry. | WI-0005, WI-0008, WI-0009, WI-0010 |
| ARX-010 | Static Analysis of Survey Programs | Reachability, contradictions, dead rules, score bounds, impossible categories, phase legality, and branch coverage. | WI-0003, WI-0006, WI-0007, WI-0010 |
| ARX-011 | Adversarial, Differential, Model-Based, and Resource Testing | Differential/model/property/malformed/resource/real-browser verification with explicit unavailable evidence. | WI-0010 |
| ARX-012 | Derivation Lineage, Reproducibility, and Trial Evidence | Hash/version derivation chain, same-path explanations, reason codes, engineering telemetry, and retrospective outcomes. | WI-0002, WI-0007, WI-0008, WI-0009, WI-0010 |
| ARX-013 | Timers, Forward-Only Progression, Pagination, and Content Banking | Timer scopes and authority, strengthened ItemsPerPage semantics, independent question/section revisit locks, deterministic question/section banking, selection seeds/manifests, bank-aware encoding/scoring, and combined stress fixtures. | WI-0002, WI-0003, WI-0004, WI-0006, WI-0007, WI-0010 |
| ARX-014 | Live Incremental Scoring and Typed Custom Scoring Expressions | Per-response authoritative scoring, configurable live score visibility, provisional/final semantics, typed serializable scoring AST, publication-time type/dependency/resource validation, expression-language versioning, and built-in/custom differential equivalence. | WI-0002, WI-0003, WI-0004, WI-0006, WI-0007, WI-0010 |
| ARX-015 | Required Aegis Operational-Fault Integration | Repository-wide required Aegis package/use at external operational boundaries, explicit boundary declarations, typed-domain separation, Ordo-authorized recovery, unknown-effect preservation, redaction, and integration verification. | WI-0002, WI-0004, WI-0008, WI-0010 |

### No-PII scope clarification

The extension strengthens the existing privacy language: Echelon Signal itself does not process external person-to-instance mappings. Opaque instance/group/submission identifiers remain permitted, but any personal identity mapping is outside this repository and outside the trial.

### Framework-baseline observation

At extension review time, the repository's installed ROS configuration identifies 1.2.1-main.16.1, while the current ROS source package is 3.1.0; the current Ordo/SDE distribution is 1.3.0 and the current Limen package is 0.6.1. The upgrade/install activity is therefore an explicit trial obligation under ARX-001 rather than an assumed prerequisite.


## 2026-09-22 administrator console / storage / analytics / visualization extension

The fourteenth authoritative source, `input-documents/survey-engine-administrator-console-storage-analytics-visualization-requirements.txt`, defines ADM-001 through ADM-077.

It extends the existing administrator persistence and reporting contracts with:

- a first-class administrator product/state system,
- capability-oriented storage providers,
- GitHub repository storage as the phase-1 durable provider,
- an explicit future installable service provider option without requiring that service in phase 1,
- concurrency, compare-and-swap, idempotency, and unknown-effect reconciliation,
- immutable accepted contributions plus rebuildable aggregate/index projections,
- incremental aggregation with full-recompute equivalence,
- deterministic query and analysis contracts,
- advanced statistical/measurement analysis with typed prerequisites,
- semantic cross-group/version comparison,
- a typed declarative visualization grammar,
- visualization suitability checks and anti-misleading rules,
- accessibility for low vision, color-vision deficiency, dyslexia, keyboard and screen-reader use,
- saved dashboards and interactive drill-down,
- report lineage, report builders, immutable snapshots, and exports,
- privacy-preserving small-cell/differencing controls,
- storage integrity, rate-limit behavior, scale modes, materialized-view repair,
- provider migration, backup/restore, and no-PII audit,
- read-only/degraded operation,
- explicit schema evolution,
- Limen/F# authority boundaries for the administrator application,
- adversarial/property/model-based testing and explicit resource limits,
- change-impact preview and obligation planning,
- sandbox/simulation mode and deterministic synthetic/adversarial data generation,
- a shared storage-provider conformance suite,
- explicit retention/archive/deletion lifecycle semantics,
- treating durable repository content as untrusted input,
- portable configuration packages and versioned policy packs,
- template-upgrade impact analysis,
- report/visual regression verification,
- semantic definition/state diffing,
- transition-based undo, bookmarkable safe analysis views, and capability explanations,
- operational/storage health diagnostics and localization preview,
- an end-to-end derived-state invalidation graph from accepted submission through visualization and snapshot eligibility,
- exact template registry/resolution management,
- credential lifecycle and multiple storage profiles,
- GitHub repository growth/rollover/compaction and operation-budget estimation,
- resumable per-item batch import semantics and quarantine,
- conflict-resolution workflows,
- formal dependency pinning,
- reproducibility-versus-deletion conflict semantics,
- optional dataset sealing and a formal close/finalization ceremony,
- non-PII import provenance,
- explicit clock/time-zone/period semantics,
- internationalization including RTL/bidirectional layout,
- offline/interrupted-session semantics,
- browser secret-storage policy and cross-tab credential coherence,
- protected-branch/PR-mode detection,
- operational repair previews,
- an invariant-health dashboard,
- proof-carrying derived artifacts through deterministic derivation certificates,
- required Aegis integration at architectural operational-fault boundaries, with Ordo/Limen separation and test evidence that Aegis is actually exercised.

ROS work-item reconciliation is complete. ADM-001 through ADM-077 are decomposed across WI-0011 through WI-0020, with reciprocal references in each work-item detail record. WI-0008, WI-0009, and WI-0010 remain the earlier administrator/reporting/cross-cutting baseline and are dependencies rather than duplicate implementations.



### Administrator extension requirement accounting

| Requirement group | Exact source section | ROS work item(s) |
|---|---|---|
| ADM-001 | Administrator Product Boundary and No-PII Contract | WI-0011 |
| ADM-002 | Administrator State System | WI-0011 |
| ADM-003 | Storage Provider Abstraction | WI-0012 |
| ADM-004 | Phase 1 GitHub Repository Storage Provider | WI-0012 |
| ADM-005 | Canonical Storage Manifest | WI-0012 |
| ADM-006 | Future Installable Service Storage Option | WI-0012, WI-0018 |
| ADM-007 | Group Administration | WI-0011 |
| ADM-008 | Submission Intake and Import Queue | WI-0013 |
| ADM-009 | Import Idempotency, Concurrency, and Unknown Effects | WI-0013 |
| ADM-010 | Durable Result and Aggregate Storage Model | WI-0013 |
| ADM-011 | Incremental Aggregation Engine | WI-0013 |
| ADM-012 | Query and Analysis Model | WI-0014 |
| ADM-013 | Statistical and Measurement Analysis | WI-0014 |
| ADM-014 | Cross-Group, Historical, and Version Comparison | WI-0014 |
| ADM-015 | Signal Visualization Grammar | WI-0015 |
| ADM-016 | Visualization Suitability and Anti-Misleading Rules | WI-0015 |
| ADM-017 | Visualization Accessibility | WI-0015 |
| ADM-018 | Dashboard System | WI-0015 |
| ADM-019 | Interactive Exploration and Drill-Down | WI-0014 |
| ADM-020 | Data-Lineage Explorer | WI-0014, WI-0016 |
| ADM-021 | Report Builder | WI-0016 |
| ADM-022 | Report Snapshots and Reproducibility | WI-0016 |
| ADM-023 | Exports | WI-0016 |
| ADM-024 | Privacy-Preserving Aggregation and Disclosure Controls | WI-0017 |
| ADM-025 | Storage Security and Integrity | WI-0012, WI-0017 |
| ADM-026 | GitHub Rate Limits, Scale, and Performance | WI-0012 |
| ADM-027 | Rebuildable Indexes and Materialized Views | WI-0013 |
| ADM-028 | Storage Migration and Provider Portability | WI-0018 |
| ADM-029 | Backup, Restore, and Disaster Recovery | WI-0018 |
| ADM-030 | Audit Without PII | WI-0017 |
| ADM-031 | Administrator UX Information Architecture | WI-0011 |
| ADM-032 | Search, Filtering, and Saved Analysis | WI-0011 |
| ADM-033 | Read-Only and Degraded Modes | WI-0011, WI-0018 |
| ADM-034 | Schema Evolution and Compatibility | WI-0018 |
| ADM-035 | Limen Boundary for Administrator UI | WI-0011 |
| ADM-036 | Advanced Stress and Adversarial Test Program | WI-0013, WI-0020 |
| ADM-037 | Property and Model-Based Tests | WI-0013, WI-0020 |
| ADM-038 | Performance and Resource Limits | WI-0020 |
| ADM-039 | Optional Advanced Analytics Extensions | WI-0019 |
| ADM-040 | Phase Boundaries | WI-0019 |
| ADM-041 | Change-Impact Preview and Obligation Planning | WI-0014 |
| ADM-042 | Administrator Sandbox and Simulation Mode | WI-0019 |
| ADM-043 | Synthetic and Adversarial Survey Data Generator | WI-0019 |
| ADM-044 | Storage Provider Conformance Suite | WI-0012, WI-0020 |
| ADM-045 | Data Lifecycle, Retention, Archival, and Deletion Semantics | WI-0017, WI-0018 |
| ADM-046 | Durable Store as Untrusted Input | WI-0012 |
| ADM-047 | Portable Configuration Packages | WI-0016 |
| ADM-048 | Versioned Policy Packs | WI-0016, WI-0017 |
| ADM-049 | Template Upgrade and Successor-Group Impact Analysis | WI-0014 |
| ADM-050 | Report and Visualization Regression Verification | WI-0015, WI-0020 |
| ADM-051 | Definition and State Diffing | WI-0014 |
| ADM-052 | Reversible Administration, Saved Views, and Capability Explanation | WI-0011, WI-0017 |
| ADM-053 | Operational Diagnostics and Localization Preview | WI-0011, WI-0018 |
| ADM-054 | End-to-End Derived-State Invalidation and Dependency Graph | WI-0014, WI-0020 |
| ADM-055 | Template Registry and Exact Template Resolution | WI-0012, WI-0014 |
| ADM-056 | Credential Lifecycle and Capability Revalidation | WI-0011, WI-0012, WI-0017 |
| ADM-057 | Multiple Storage Profiles | WI-0011, WI-0012, WI-0018 |
| ADM-058 | GitHub Repository Growth, Rollover, and Compaction Strategy | WI-0012, WI-0018, WI-0020 |
| ADM-059 | Storage Cost and Operation Budget Estimation | WI-0012, WI-0020 |
| ADM-060 | Batch Import Transaction and Resume Semantics | WI-0013, WI-0020 |
| ADM-061 | Quarantine Boundary for Untrusted Artifacts | WI-0013, WI-0017, WI-0020 |
| ADM-062 | Conflict Resolution Workspace | WI-0011, WI-0014 |
| ADM-063 | Explicit Dependency Pinning for Reports, Dashboards, and Snapshots | WI-0014, WI-0016 |
| ADM-064 | Reproducibility Versus Deletion Policy Conflict | WI-0016, WI-0017, WI-0018 |
| ADM-065 | Dataset Sealing | WI-0011, WI-0017 |
| ADM-066 | Group Close and Formal Finalization Ceremony | WI-0011, WI-0016, WI-0017 |
| ADM-067 | Import Provenance Without Person Identity | WI-0013, WI-0017 |
| ADM-068 | Clock, Calendar, Time Zone, and Period Semantics | WI-0011, WI-0014, WI-0016, WI-0020 |
| ADM-069 | Internationalization and Bidirectional Layout Semantics | WI-0015, WI-0016, WI-0020 |
| ADM-070 | Offline and Interrupted Administrator Session Behavior | WI-0011, WI-0012, WI-0020 |
| ADM-071 | Browser Secret Storage Policy | WI-0011, WI-0017 |
| ADM-072 | Cross-Tab Credential and Capability Coherence | WI-0011, WI-0012, WI-0020 |
| ADM-073 | GitHub Branch Protection and Pull Request Storage Mode | WI-0012, WI-0020 |
| ADM-074 | Operational Repair Preview and Plan | WI-0014, WI-0018, WI-0020 |
| ADM-075 | Invariant Health Dashboard | WI-0011, WI-0014, WI-0018 |
| ADM-076 | Proof-Carrying Derived Artifacts | WI-0013, WI-0014, WI-0016, WI-0018, WI-0020 |
| ADM-077 | Required Aegis Integration and Operational Fault Boundaries | WI-0011, WI-0012, WI-0013, WI-0017, WI-0018, WI-0020 |



## Modifying, superseding, and constraining relationships

- `URLC-001` and `URLC-002` explicitly modify the earlier server-oriented runtime, replay, revision, completion-lock, and response-persistence proposals in `ACR-005`, `VER-003`, and `VER-007`. The work items implement the URL-based/import-side semantics and retain the earlier text only as provenance.
- `LURL-001` strengthens “URL as final submission” into “URL as continuously updated respondent state,” with the completed URL becoming the submission.
- `ID-002`, `ID-004`, and `LURL-002` narrow the general requirement that `SurveyInstanceId` travel in the URL: it may remain in identified submissions and anonymous live/resume URLs, but it must be removed during anonymous finalization and replaced by a new unlinkable `AnonymousSubmissionId`.
- `CAN-001`–`CAN-008` consolidate the pre-reporting architecture. The later specialized administrator, reporting, authoring, lifecycle, and identity documents refine those contracts without replacing their shared deterministic invariants.
- Repository governance constrains implementation with explicit security/privacy review, accessibility as an acceptance property, immutable canonical history, and evidence-backed decisions. The repository currently states that no product architecture has been accepted; therefore this migration creates captured work obligations and traceability, not silent architectural acceptance.
- The project charter is still draft and the product baseline is not established. WI-0010 must establish measurable baselines and acceptance evidence before implementation items can be completed.

## Coverage verification

- Relevant source files discovered: 14
- Relevant source files reviewed completely: 14
- Relevant source files excluded: 0
- Requirement groups recorded: 164
- New delivery work items: 19
- Source appendices added: 12
- Sources fully migrated to ROS work items: 14
- Authoritative sources pending ROS work-item reconciliation: 0


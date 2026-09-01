# Survey engine requirements migration ledger

Status: requirements-definition completed  
Completed: 2026-08-31  
Authoritative corpus: `input-documents/`  
Migration work item: WI-0001

## Meaning of completion

“Requirements-definition completed” means every actionable requirement in each source file has been assigned to at least one ROS work item. It does not mean the requirement is implemented, accepted as repository architecture, or verified in running software. All created delivery items remain in the local ROS backlog for prioritization.

Original source content is preserved. Each source received only an appended migration appendix; the line references below are the original pre-append line numbers.

## Complete corpus coverage

No file under `input-documents/` was excluded. All 12 files were relevant and reviewed completely.

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

## Modifying, superseding, and constraining relationships

- `URLC-001` and `URLC-002` explicitly modify the earlier server-oriented runtime, replay, revision, completion-lock, and response-persistence proposals in `ACR-005`, `VER-003`, and `VER-007`. The work items implement the URL-based/import-side semantics and retain the earlier text only as provenance.
- `LURL-001` strengthens “URL as final submission” into “URL as continuously updated respondent state,” with the completed URL becoming the submission.
- `ID-002`, `ID-004`, and `LURL-002` narrow the general requirement that `SurveyInstanceId` travel in the URL: it may remain in identified submissions and anonymous live/resume URLs, but it must be removed during anonymous finalization and replaced by a new unlinkable `AnonymousSubmissionId`.
- `CAN-001`–`CAN-008` consolidate the pre-reporting architecture. The later specialized administrator, reporting, authoring, lifecycle, and identity documents refine those contracts without replacing their shared deterministic invariants.
- Repository governance constrains implementation with explicit security/privacy review, accessibility as an acceptance property, immutable canonical history, and evidence-backed decisions. The repository currently states that no product architecture has been accepted; therefore this migration creates captured work obligations and traceability, not silent architectural acceptance.
- The project charter is still draft and the product baseline is not established. WI-0010 must establish measurable baselines and acceptance evidence before implementation items can be completed.

## Coverage verification

- Relevant source files discovered: 12
- Relevant source files reviewed completely: 12
- Relevant source files excluded: 0
- Requirement groups recorded: 72
- New delivery work items: 9
- Source appendices added: 12


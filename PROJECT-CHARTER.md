---
id: PROJECT-CHARTER-echelon-signal
title: Echelon Signal Project Charter
status: draft
version: 0.2.0
created: 2026-08-31
updated: 2026-09-21
---

# Echelon Signal project charter

## Purpose

Build a deterministic, URL-first survey and assessment engine in F#/.NET WebAssembly while using the application as a demanding integration trial for Repository Operating System (ROS), Ordo / State-Directed Engineering, and Limen.

The product goal and the engineering-experiment goal are both first-class:

1. Deliver a useful survey engine whose published templates define immutable meaning and whose live respondent URL carries portable answer state.
2. Produce evidence about where ROS, Ordo, and Limen improve correctness, traceability, context locality, effect handling, and handoff quality, and where they create friction or leave gaps.

## Intended users

Primary product roles:

- Survey authors who create, validate, test, and publish immutable survey templates.
- Respondents who complete surveys without server-side respondent session state.
- Administrators who import completed survey artifacts, aggregate results, and render reports.
- Technical/audit users who need deterministic lineage and reproducibility.

Echelon Signal itself does not process personal identity information. Human identity mapping, if another system ever requires it, is outside this repository and outside this trial.

## First bounded outcome

Deliver one non-trivial end-to-end vertical slice that proves the architecture rather than a toy counter:

1. Author and publish an immutable survey template with branching, validation, scoring, derived facts, recommendations, and test fixtures.
2. Load that template into an F# WebAssembly engine behind Limen.
3. Complete a respondent survey while the URL continuously represents the authoritative answer state.
4. Finalize an anonymous submission using unlinkable cryptographic entropy and no PII.
5. Copy the completed submission through the Limen clipboard capability.
6. Import the submission in the administrator flow.
7. Produce deterministic SurveyResult, SurveyGroupResult, and report state.
8. Exercise at least one external effect whose outcome becomes unknown and requires explicit reconciliation.
9. Demonstrate reference/full evaluation equivalence with optimized/incremental evaluation.
10. Record ROS/Ordo/Limen evidence and a retrospective.

## Included

- Canonical survey domain model and immutable template lifecycle.
- Typed answers, selectors, validation, flow, completion, scoring, recommendations, and reporting.
- Live URL state and portable completed submissions.
- Identified opaque-instance mechanics where required by the domain, but no person mapping or PII.
- Strong anonymous finalization and aggregate reporting.
- F#/.NET WebAssembly application authority.
- Limen browser boundary and real serialized capability round trips.
- Explicit state, legal transitions, capabilities, obligations, unknown effects, and scoped negative knowledge using Ordo principles.
- ROS-governed work, traceability, telemetry, handoffs, validation, and retrospective evidence.
- Reference and optimized/incremental evaluation paths with differential tests.
- Static survey-program analysis, malformed/adversarial fixtures, resource limits, and real-browser acceptance tests.
- Accessibility as an acceptance property.
- Evidence-backed framework feedback and reusable upstream improvements when the trial exposes a genuine generic gap.

## Excluded

- Collection, storage, transmission, display, joining, logging, or processing of PII.
- Names, email addresses, phone numbers, employee identifiers, account identifiers, government identifiers, street addresses, or equivalent identifying data.
- Free-form survey answer fields during this trial.
- Server-side respondent session persistence as a requirement.
- Arbitrary executable scripts, F#, C#, JavaScript, CLR method calls, or general-purpose expression trees embedded in survey templates.
- Browser/application logic duplicated outside the F# engine.
- Hidden retry of non-idempotent effects after an unknown outcome.
- Claims that ROS, Ordo, or Limen improve development outcomes without measured evidence.
- Production-grade external identity management.
- Speculative framework capabilities that no Echelon Signal requirement exercises.

## Success criteria

- A non-trivial survey completes end to end through the F# WASM/Limen boundary.
- The same immutable template and submission always produce the same canonical result.
- Every valid response state round-trips through URL encoding.
- Reference/full and optimized/incremental evaluators are observationally equivalent for the accepted corpus.
- Published templates pass structural, semantic, compatibility, privacy, encoding, static-analysis, and fixture gates.
- Anonymous final submissions contain no invitation-linking identifier and use cryptographically secure unlinkable entropy.
- Echelon Signal processes no PII in product, diagnostics, tests, examples, telemetry, or reports.
- External unknown outcomes enter explicit reconciliation states rather than being mislabeled as failures.
- Browser navigation, clipboard, focus, and other used capabilities cross the actual F# serialization boundary and have real-browser evidence.
- Every formal result/report has reproducible derivation lineage.
- Requirement groups remain reciprocally traceable to ROS work and evidence.
- The repository can be continued by a successor from durable artifacts without relying on chat history.
- The trial produces explicit semantic and operational retrospective outcomes, including framework weaknesses and recommended upstream changes.
- Missing telemetry is reported as unknown/unavailable rather than fabricated.

## Constraints and assumptions

- F# is the application/domain implementation language.
- Limen owns browser mechanism; application meaning remains in the F# engine.
- HTML owns structure and CSS owns presentation.
- Published templates are immutable.
- The live respondent URL is the canonical serialized respondent state.
- No PII is permitted in Echelon Signal.
- Runtime and framework dependencies should remain minimal and must be justified.
- Determinism, explicit failure, and reproducibility take priority over minor byte or implementation savings.
- Unsupported versions/capabilities fail explicitly rather than silently degrading.
- A framework gap discovered by a real requirement may justify extending the reusable framework; speculative surface without a demonstrated need does not.
- The current framework stack is itself under evaluation and must not be treated as validated merely because this repository uses it.

## Owners and decision authority

Repository owner retains product and architecture decision authority.

Agents and contributors must follow the installed ROS work protocol, Ordo/SDE execution guidance, repository decision records, and the explicit acceptance/evidence requirements for the active work item.

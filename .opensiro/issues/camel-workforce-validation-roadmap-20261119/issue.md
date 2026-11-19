# CAMEL Workforce — native result validation vs an independent S3* constructor (OpenSiro plan-only)

**OpenSiro pilot · PLAN_ONLY / NO_USEFUL_CHANGE · DRAFT — NOT PUBLISHED.**
**Final operator decision: NO_GO — do not implement a new independent S3* constructor now.**
**Two-level case:** this human decision issue + [AI/developer evidence and acceptance contract](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/constructor-sufficiency.md).
**Working fork:** [opensiro-contributions/camel](https://github.com/opensiro-contributions/camel) · [case folder](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/README.md). This document is **not** a published GitHub Issue.

## 1. Why OpenSiro and central accepted VSM assessment

OpenSiro tests whether reusable VSM-informed organizational specifications can standardize AI-agent harness development and reduce total implementation, integration, and maintenance effort. This is an unmeasured hypothesis, not a mandate for CAMEL maintainers to adopt VSM. Here the test is whether another independently composable audit mechanism would outperform CAMEL's narrower native parallel-result validation and recovery proposals.

> **STARTING POINT — ACCEPTED HISTORICAL INDEX, NOT THE TARGET:** `S1=A · S2=C · S3=A · S3*=— · S4=— · S5=—`.
> [Accepted assessment](https://github.com/opensiro/vsm-harness-index/blob/34e11ec4dd52e1ba3ee0111d8bca73f13918f54f/assessments/ca/camel-workforce.md), blob `1d8e2198e02ddceb978d9bb3a5094bc7a40d0d16`, reviewed **2026-09-17**, reviewed CAMEL ref [`8c791b7b9cf7deab56cb5a92818c34499af9097f`](https://github.com/camel-ai/camel/commit/8c791b7b9cf7deab56cb5a92818c34499af9097f), Profile **0.2.1** / Skills assessment procedure **0.3.1**. These states are historical; no current HEAD or planned change has received a new Index grade.

| Function | Accepted state | Consequence at reviewed Workforce boundary |
| --- | --- | --- |
| S1 · Operations | **A** | Worker agents execute assigned operational tasks; no mandatory additional C target. |
| S2 · Coordination | **C** | Runtime-owned dependency gates and task ordering; already constructor-owned. |
| S3 · Current management | **A** | Coordinator selects assignments and capacity responses; no forced A→C conversion. |
| S3* · Independent complementary review | **—** | Ordinary quality/failure analysis was not independently protected review; this is a *research hypothesis*, not evidence of demand. |
| S4 · Future intelligence | **—** | Task-failure replanning did not establish a future/external adaptation loop; no proposed S4 work. |
| S5 · Ultimate policy | **—** | Human stop/pause and supplied task objectives were not S5 closure; retain legitimate parent/operator authority. |

**Pins / boundary:** original Workforce at [`c619d1fe5aa2182395d02aadddc71b818c1b6c9f`](https://github.com/camel-ai/camel/commit/c619d1fe5aa2182395d02aadddc71b818c1b6c9f), observed **2026-11-19**; accepted Index at `34e11ec4dd52e1ba3ee0111d8bca73f13918f54f`; the September review is **63 days old**, so an Index-owned source-pinned re-assessment is recommended before confident new ownership claims (advisory, not blocker). System-in-focus: first-party `camel.societies.workforce.Workforce` in supported AUTO_DECOMPOSE/PIPELINE task execution, its workers/coordinator/task agent, callback/quality/failure loop; not external applications, third-party observability systems, CAMEL maintainer governance or an imagined installed reviewer. Fork parent is `camel-ai/camel`, but its independent `opensiro/meta` is initialized as **PAUSE/DORMANT** (no inferred ALLOW). Original root license: **Apache-2.0**. [Contribution policy](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/CONTRIBUTING.md) requires prior accepted discussion for PRs, human-reviewed AI drafts, and tested submissions. CLA/DCO formalities for any future external submission remain **UNVERIFIED**.

## 2. User need and final decision

**P0 research candidate — independent S3* review of parallel Workforce outcomes: REJECTED NOW.** An operator seeking five *unique* papers across concurrent workers needs duplicate detection and targeted completion; [original issue #3332](https://github.com/camel-ai/camel/issues/3332) articulates that exact need. But it does **not** establish demand for a protected, separately developer-composed auditor outside the coordinator/task-agent recovery path.

**Simplest original-native answer:** pursue the [already-open PR #3395](https://github.com/camel-ai/camel/pull/3395) against #3332 (aggregation validation, deduplication and iterative refinement). It is **OPEN_PR, NOT SHIPPED** and its acceptance/testing still belongs to CAMEL maintainers. This addresses the stated operator counterfactual without introducing another VSM control surface.

**Separate P2: NONE.** S4/S5 labels do not justify unrelated controllers or policy grants.

## 3. Actual original work and remaining difference

| Capability | Verified current source or proposal | Residual user benefit of a new S3* constructor |
| --- | --- | --- |
| Execute parallel task graph | [Current `process_task_async`](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py#L2669-L2707) concatenates subtask results, runs coordinator and existing queues | Unique-result guarantee is not evident in this path, but native #3332 / PR #3395 addresses it |
| Quality/failure analysis | [Current `_analyze_task`](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py#L1645-L1726) assesses result quality in ordinary Workforce control | Not independently protected complementary audit; no verified separate operator request |
| Validation and refinement | [Issue #3332](https://github.com/camel-ai/camel/issues/3332) **OPEN ISSUE**; [PR #3395](https://github.com/camel-ai/camel/pull/3395) **OPEN, unmerged**; PR adds a validation prompt, `ValidationResult`, refinement strategy, example and tests | No proven incremental outcome beyond this native alternative |
| Plan/edit/run and event state | [Issue #3980](https://github.com/camel-ai/camel/issues/3980) + [PR #3979](https://github.com/camel-ai/camel/pull/3979) both **OPEN**, proposed public plan API/event metadata and tests | Enables observability/editing if merged, not independently an S3* decision owner |
| Streaming / callback changes | [#3379](https://github.com/camel-ai/camel/issues/3379), [PR #3403](https://github.com/camel-ai/camel/pull/3403), [#3352](https://github.com/camel-ai/camel/issues/3352), [PR #3363](https://github.com/camel-ai/camel/pull/3363) all **OPEN** | Reuse work where appropriate; event/transport changes do not themselves qualify as audit |

## 4. P0/P1/P2 and minimum sufficient result

| Priority | Outcome | Disposition |
| --- | --- | --- |
| **P0 — S3* proposed independent auditor** | Distinct independently composed auditor checks an immutable/restricted result and sends protected corrective feedback into subsequent task execution | **NO_GO**: independence, authority, independent first-party port, operator necessity and measurable delta are not demonstrated |
| **P1 — native alternative** | Five requested unique papers yield five unique papers or an explicit unsuccessful result after bounded refinement | **Reference #3332 and open PR #3395, do not duplicate their implementation**; tests for it remain proposal-native |
| **P2 — optional independent mode** | No independently evidenced second operator need | **NONE** |

**C sufficiency:** **NOT ESTABLISHED**, not merely missing code. The current callback/quality analysis is not a protected independent decision port; a C construction would require separately evidenced reviewer actor, authorization, immutable input visibility, select/hold/reject result, enforced corrective feedback to later operations, supported API and native positive/negative tests. No qualified proposal merits adding these today. Full conditional sufficiency/falsification reasoning is in the [AI companion](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/constructor-sufficiency.md).

## 5. Acceptance and stop

**Native baseline (hypothetical test, NOT EXECUTED):** concurrent workers return duplicate papers; compare current released behavior and the *unmerged* PR #3395 using identical inputs, count distinct identifiers and controlled corrective subtasks. Track duplicate rate, false rejection and cost/latency; no test results are claimed.

**Any later S3* escalation:** require evidence that the native validator cannot provide an essential **independently protected** audit judgment and that the reviewer can lawfully reject/hold/report and alter subsequent operation. Negative cases must reject unauthorized reviewer action, missing input, stale result, and feedback that never reaches the next task. If simpler native validation produces the same useful result, stop without new C.

**Stop now:** do not implement a speculative S3* constructor, merge PRs, change grades, publish external material or claim operational savings.

## 6. Independent choices

1. **Original-native:** follow #3332/#3395 rather than duplicate them; CAMEL maintainers decide whether to merge; no unsolicited AI-generated PR.
2. **Profile / Skills:** no proven normative defect from this specific case; only open a separate change if a real semantic ambiguity arises.
3. **Optional experimental fork:** lawful only with a new, evidenced independently protected reviewer task; no automatic implementation or adoption expectation.

## 7. Cost experiment

Compare the *same* five-unique-paper user task under (A) a minimal native validation/refinement implementation and (B) a hypothetical VSM-informed separately composable independent auditor. Predeclare output correctness/unique count, implementation and integration person-hours, review/tests, per-run latency/tokens, false positives and regression maintenance. **Cost status: NOT_MEASURED**; PR claims are not measurements.

## 8. Decision / handoff

**Result: NO_USEFUL_CHANGE. Final operator decision: NO_GO.** The evidence supports a native operator need, but not a *new independent S3* constructor* beyond original #3332 / PR #3395. The decision does not say the current original feature is solved: #3395 is still open.

**Action:** no new S3*/S4/S5 feature; retain source links and consider another assessment/research only on a future original-native request establishing independent review benefit. **Fork control: PAUSE/DORMANT.** The [AI contract](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/constructor-sufficiency.md) and [receipt](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/roadmap.md) share this conclusion.

**Publication:** **READY_FOR_FORK_ISSUE_APPROVAL — NOT PUBLISHED** in `opensiro-contributions/camel`, title `CAMEL Workforce — native result validation vs an independent S3* constructor (OpenSiro plan-only)`. No original maintainer Issue needed (already #3332). No fork Issue, original Issue/PR/comment, product change, new Index classification, CLA attestation or measured saving has been created by this roadmap. Exact current-conversation owner approval of this full title/body is required before any fork Issue publication.

**AI disclosure:** Drafted with AI assistance. Original source and competing issue/PR metadata were examined; no independent human source validation, executed native tests or established cost savings claimed.

# CAMEL Workforce — S3* independent-review constructor sufficiency and native overlap

**Level 2 AI/developer contract · PLAN_ONLY / NO_USEFUL_CHANGE · DRAFT — NOT PUBLISHED.**
[Human decision issue](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/issue.md) · [receipt](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/roadmap.md).
**Final operator decision: NO_GO.** No new S3* constructor now. This document is analysis, not an implementation spec approved for coding.

## Functional scope and starting accepted baseline

**Accepted historical Index**: `S1=A · S2=C · S3=A · S3*=— · S4=— · S5=—`.
[Immutable Index assessment](https://github.com/opensiro/vsm-harness-index/blob/34e11ec4dd52e1ba3ee0111d8bca73f13918f54f/assessments/ca/camel-workforce.md), blob `1d8e2198e02ddceb978d9bb3a5094bc7a40d0d16`, reviewed **2026-09-17**, source review [`8c791b7b9cf7deab56cb5a92818c34499af9097f`](https://github.com/camel-ai/camel/commit/8c791b7b9cf7deab56cb5a92818c34499af9097f), Profile **0.2.1**, Skills assessment procedure **0.3.1**. Current observed original [`c619d1fe5aa2182395d02aadddc71b818c1b6c9f`](https://github.com/camel-ai/camel/commit/c619d1fe5aa2182395d02aadddc71b818c1b6c9f) on **2026-11-19**, different from the accepted review; no current Index regrade. Freshness: **63 days**, recommended independent Index reassessment if confident new ownership claims are needed.

| Function | Historical baseline and authority | Target/exclusion |
| --- | --- | --- |
| S1 | A: workers make task-level choices | Existing; no mandatory constructor |
| S2 | C: runtime dependency coordination | Existing; retain ordering semantics |
| S3 | A: coordinator currently allocates work/capacity | Existing; a native validator remains in same operational control path |
| S3* | —: no protected independent complementary audit witnessed | **P0 rejected now**: independent user need, construction port and protected feedback not established |
| S4 | —: current-task replan not future/external adaptation | No S4 objective; no relabel of failure recovery |
| S5 | —: operator stop/pause not ultimate-policy closure | Preserve human and original authority; no S5 construction |

**Boundary:** supported first-party `camel.societies.workforce.Workforce` (AUTO_DECOMPOSE/PIPELINE), workers, coordinator/task agent, task graph, callbacks and local quality/recovery; exclude CAMEL maintainer governance, third-party tools/apps, uninstalled extensions and parent organizations. **Rights:** original Apache-2.0; [CONTRIBUTING AI policy](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/CONTRIBUTING.md) requires previously accepted discussion, human review of AI drafts and verified tests for PRs; CLA/DCO for a new external PR unverified. Verified fork `opensiro-contributions/camel` parent `camel-ai/camel`; **PAUSE/DORMANT** metadata bootstrap only, no ongoing engineering grant.

## 1. Actor, user counterfactual and actual disturbance

**Concrete task:** researcher requests five **unique** papers; several workers return overlapping papers. A simple concat may emit fewer than five unique entries. Current [`process_task_async`](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py#L2669-L2707) shows aggregation by joining subtask results, not a purpose-built uniqueness gate. [Issue #3332](https://github.com/camel-ai/camel/issues/3332) states this exact need.

**Developer counterfactual:** if a separate proposed audit agent is removed but the native dedup/refinement in [PR #3395](https://github.com/camel-ai/camel/pull/3395) remains, there is no demonstrated user outcome that becomes impossible. An extra LLM critic in the same TaskAgent control path would not satisfy complementary independent S3* merely by checking results.

**P0 / S3***: investigate protected independent auditor constructor; **NO_GO** now.
**P1**: reuse #3332/#3395 for native validation/refinement; do not duplicate or merge automatically.
**P2**: NONE.
**Sufficiency status:** NOT ESTABLISHED; no constructive C target endorsed.

## 2. SHIPPED vs OPEN_PR vs ISSUE_ONLY

| First-party path | Current original source | Existing competing work | Significance |
| --- | --- | --- | --- |
| Task control | [`workforce.py`](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py#L2669-L2707) task decomposition and subtask-result concat | [#3980](https://github.com/camel-ai/camel/issues/3980) issue / [PR #3979](https://github.com/camel-ai/camel/pull/3979) **OPEN** plan/edit/run API, event metadata and subtask sync | Current execution behavior is **SHIPPED**; plan/edit API is **OPEN_PR, not shipped** |
| Quality/recovery | [`_analyze_task`](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py#L1645-L1726) quality and failure analysis by existing control path | [#3332](https://github.com/camel-ai/camel/issues/3332) **OPEN** / [PR #3395](https://github.com/camel-ai/camel/pull/3395) **OPEN** | Not protected independent S3*; native dedup/refinement intended but **not merged** |
| Event transport | [`events.py`](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/events.py) and [callbacks](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce_callback.py) expose lifecycle events | [#3379](https://github.com/camel-ai/camel/issues/3379) / [PR #3403](https://github.com/camel-ai/camel/pull/3403) **OPEN**; [#3352](https://github.com/camel-ai/camel/issues/3352) / [PR #3363](https://github.com/camel-ai/camel/pull/3363) **OPEN** | Callback/stream transport is not autonomous audit ownership |
| Parallel duplicate handling | No verified built-in end-to-end uniqueness/corrective-refinement guarantee in inspected concat path | [PR #3395](https://github.com/camel-ai/camel/pull/3395) adds `VALIDATION_PROMPT`, `ValidationResult`, `REFINE`, example and test file | Exact operator need already has a source-native candidate; tests are **PR-added, NOT EXECUTED BY OPENSIRO** |

Observed PR heads (source readback 2026-11-19): **#3395** `f09c4390c8befc8b2cf46335f662a47846b1b881`; **#3979** `a7430416ef1d00105db400d833679fff7cd7cb66`; **#3403** `55fb89420f14451c63b7cd91236eb8498add1452`; **#3363** `4ff3882d101f6d2d6a22d11407d63a3995776bd0`. Live states read as OPEN/unmerged. Future merge/status requires fresh verification. No result is promoted to shipped.

## 3. What a *future*, genuinely qualified S3*=C constructor would need

**Do not implement these speculative ports from this NO_GO case.** They are a falsifiable sufficiency boundary if independent user demand appears:
1. **Independent evidence intake:** authorized reviewer sees stable task inputs, outputs and lineage, not solely the mutable coordinator summary. Distinguish integrity/provenance from a log callback.
2. **Developer-composed decisive actor:** public supported API registers a separately supplied autonomous reviewer with independent read/evaluate/hold/return right; the coordinator cannot silently impersonate its verdict.
3. **Choice and lifecycle:** reviewer selects pass / reject-and-correct / hold with recorded reason and bounded attempts; stale and duplicate reviews cannot apply twice.
4. **Lawful enforcement:** gate final result acceptance or corrective task dispatch at the actual first-party boundary; maintain owner permissions, task dependencies, pause/stop and resource limits.
5. **Closed feedback:** reviewer disposition is observed and changes real later task/finalization behavior. Failure to complete, missing reviewer or rejected authorization must be visible; generic telemetry alone is insufficient.
6. **Supported reachability:** shipped package API and tests work on first-party AUTO_DECOMPOSE/PIPELINE where claimed, without relying on a one-off external plugin.

**Counterfactual / falsification:** disable the custom reviewer, leave deterministic transport and native #3395 validator; if the same organizational decision and useful task outcome remain, the proposed independent C owner is not established. A separate agent name is not sufficient.

## 4. Dependency order and priority

- **P0: REJECTED — no new S3* construction** until a maintainer/operator identifies a *distinct* protected review task that the native quality/validation path cannot solve.
- **P1: REUSE NATIVE #3332 / #3395**, with potential overlap from #3980/#3979 for plan/event APIs if those PRs are accepted. Open PRs are not committed dependencies, and there is no authorization to modify/merge them.
- **P2: NONE**; already-A S3 does not require a C clone, and S4/S5 have no qualified additional need.

**No minimum complete C implementation set exists from current evidence.** Adding ports would solve a hypothetical objective rather than the evidenced five-unique-paper task. A later GO would need a new materiality/authority proof, reviewed ports and supported native tests; only Index owns an eventual grade.

## 5. Optional other constructor

**NONE.** S4 external/future intelligence and S5 ultimate-policy work lack original-native demand and protected decision-loop evidence in this case. Do not transform task failure replan into S4 or human stop into S5.

## 6. Native acceptance / negatives (proposed, NOT RUN)

1. **Native P1 positive:** five unique requested research items, four workers returning overlapping IDs; current baseline vs PR #3395 implementation should show dedup and bounded corrective task dispatch, or explicit incomplete result.
2. **Native P1 negative:** ambiguous/near-duplicate titles must not be dropped as exact duplicates; invalid/repeated identifiers and exhausted retries must not become a fabricated success.
3. **Control compatibility:** pause/stop, dependency order and configured retry limits remain enforceable; async callback/event ordering is not silently changed by another reviewer.
4. **Potential independent audit positive (conditional only):** reviewer with distinct authority rejects or holds a demonstrably untrustworthy result that the original TaskAgent path would finalize; an enforced downstream decision and later feedback is recorded.
5. **Independent audit negative (conditional only):** absent reviewer, stale output revision, unauthorized actor, skipped audit feedback or mutated coordinator-only summary must not claim independent closure.
6. **Materiality test:** compare incremental correctness, operator rights and total effort against smallest source-native alternative. If difference is none, reject the independent component.

Suggested native test location for a hypothetical future PR: `test/workforce/`; existing proposed [PR #3395 tests](https://github.com/camel-ai/camel/pull/3395/files) and [PR #3979 tests](https://github.com/camel-ai/camel/pull/3979/files) should be reviewed rather than cloned. **No tests have been executed in this PLAN_ONLY case.**

## 7. Evidence owners, falsification and costs

Original maintainers own source behavior, #3332/#3395 resolution and AI/PR requirements; user/operator owns any new separately protected reviewer need and legitimate rights; OpenSiro Index/Skills own formal grade and re-assessment. Recommend Index re-review because historical assessment is 63 days old; do not block current plan-only negative decision or relabel grades.

Matched trial: same five-unique-paper task, same workload, compare a minimal native implementation to a hypothetical independent-auditor implementation. Measure verified unique count, correction precision, rejected unauthorized decisions, implementation/review/test effort, run latency, maintenance and regressions. **Cost: NOT_MEASURED**.

**Decision: NO_GO.** Reuse original native issue/PR; no speculative S3* actor, S4/S5 controller, product change, new contribution record or external publication. Human [issue.md](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/issue.md) and [roadmap.md](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/roadmap.md) repeat the decision. **Public fork Issue: NOT PUBLISHED; exact owner approval required.**

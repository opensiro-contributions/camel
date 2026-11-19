# CAMEL Workforce — Capability Roadmap Receipt

- Original repository: camel-ai/camel
- Original HEAD: c619d1fe5aa2182395d02aadddc71b818c1b6c9f
- Observed at: 2026-11-19
- Accepted Index assessment: https://github.com/opensiro/vsm-harness-index/blob/34e11ec4dd52e1ba3ee0111d8bca73f13918f54f/assessments/ca/camel-workforce.md
- Accepted assessment blob SHA: 1d8e2198e02ddceb978d9bb3a5094bc7a40d0d16
- Accepted review ref: 8c791b7b9cf7deab56cb5a92818c34499af9097f
- Accepted reviewed at: 2026-09-17
- Accepted Index commit: 34e11ec4dd52e1ba3ee0111d8bca73f13918f54f
- Accepted vector: S1=A · S2=C · S3=A · S3*=— · S4=— · S5=—
- Profile version at accepted review: 0.2.1
- Skills procedure at accepted review: 0.3.1
- Latest canonical successful semantic review: 2026-09-17 (63 calendar days before this receipt)
- System in focus: First-party CAMEL Workforce supported AUTO_DECOMPOSE/PIPELINE tasks, coordinator, workers, task agent and built-in callbacks/recovery; exclude original maintainer governance and external plugins
- Result: NO_USEFUL_CHANGE
- Final operator decision: NO_GO
- External issue: DRAFT — NOT PUBLISHED
- Fork GitHub Issue: READY_FOR_FORK_ISSUE_APPROVAL — NOT PUBLISHED
- Cost status: NOT_MEASURED
- Research artifacts: [Human issue](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/issue.md) · [AI contract](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/constructor-sufficiency.md)
- Working fork: https://github.com/opensiro-contributions/camel
- Fork product branch base: 0366b64bf3609c76f50e396715aab73ba58a930c
- Fork metadata control: PAUSE/DORMANT after initial authorized bootstrap; no owner ALLOW inferred

## Identity and pins

Original [HEAD](https://github.com/camel-ai/camel/commit/c619d1fe5aa2182395d02aadddc71b818c1b6c9f) was separately observed from accepted [review source](https://github.com/camel-ai/camel/commit/8c791b7b9cf7deab56cb5a92818c34499af9097f); accepted Index is pinned at [34e11ec4dd52e1ba3ee0111d8bca73f13918f54f](https://github.com/opensiro/vsm-harness-index/commit/34e11ec4dd52e1ba3ee0111d8bca73f13918f54f) and its assessment blob is `1d8e2198e02ddceb978d9bb3a5094bc7a40d0d16` (historical review 2026-09-17). Historical vector `A C A — — —` is not a present-day regrade. The most recent supported semantic review is 63 days old; recommend a distinct Index-owned source-pinned reassessment if a confident updated vector is needed. No actual pending reassessment is asserted.

## Rights and authority

Verified original license: [Apache-2.0](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/LICENSE); [CONTRIBUTING](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/CONTRIBUTING.md) requires prior accepted discussion for PRs, human-vetted AI drafts and testing. Additional CLA/DCO evidence for future third-party submission: UNVERIFIED. Matching fork `opensiro-contributions/camel` verified `fork=true`, parent `camel-ai/camel`, writable by connected owner; dedicated `opensiro/meta` only. Initial state is `PAUSE/DORMANT`, not an ALLOW or permission for follow-on publication. This plan records no code improvement or contribution ID.

## Existing work / overlap

Current [`process_task_async`](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py#L2669-L2707) joins subtask results; ordinary [`_analyze_task`](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py#L1645-L1726) performs quality/failure analysis in existing control path. [Original #3332](https://github.com/camel-ai/camel/issues/3332) asks for dedup of parallel results and targeted retries; [PR #3395](https://github.com/camel-ai/camel/pull/3395) OPEN/unmerged supplies proposed validation/refinement, tests and example. [#3980](https://github.com/camel-ai/camel/issues/3980)/[PR #3979](https://github.com/camel-ai/camel/pull/3979) OPEN/unmerged proposes plan/edit/run API and better events. [#3379](https://github.com/camel-ai/camel/issues/3379)/[PR #3403](https://github.com/camel-ai/camel/pull/3403) and [#3352](https://github.com/camel-ai/camel/issues/3352)/[PR #3363](https://github.com/camel-ai/camel/pull/3363) address callback surfaces; these do not prove an independent reviewer. No PR is treated as shipped.

## Function ownership

Accepted historical S1=A (workers), S2=C (dependency gates), S3=A (coordinator), S3*=— (quality eval not independent audit), S4=— (no demonstrated future/external adaptation), S5=— (operator stop/pause not ultimate policy closure). At current inspected HEAD, operational native quality checks remain in existing Workforce control, while relevant separate validation/streaming proposals are open. No independent first-party S3* decision/feedback right was established by this research; no regrade is made.

## Capability priority

**P0: REJECTED new S3*=C constructor.** Evidenced operator need is five *unique* papers from parallel subtask results, not a protected independent audit owner. Current shipped concat may duplicate; native #3332 / open #3395 is narrower and directly aligned. **P1:** reuse original-native validation/refinement path and review its own tests, no independent OpenSiro PR. **P2:** NONE. Already-A S3 and already-C S2 need no mandatory C engineering; S4/S5 are not justified solely by missing historical states. Proposed protected reviewer ports and positive/negative conditional acceptance are detailed in the linked AI contract, **not qualified to implement**. C sufficiency: NOT ESTABLISHED.

## Implementation options

**Decision now: NO_GO** for a separate S3* constructor. Do not code, duplicate #3395, publish issue/PR, promote grades, or claim the need has already been solved. CAMEL may independently review #3395 and its native tests; if a future user proves an additional independent audit benefit, start a new source-pinned hypothesis and separate Upgrade permission. No native tests executed in this research-only pass.

## Specification and domain alternatives

No demonstrated Profile semantic bug or Skills method defect; retain their independent authority. A domain-specific fork experiment is optional only after distinct user need, lawful rights and a measurable comparison; it is not automatic follow-on work. An original maintainer issue would duplicate #3332, so no new original issue is proposed.

## Cost experiment

Predeclare the same five-unique-paper task under (A) minimal native validation/refinement and (B) an independent VSM-inspired auditor: compare correctness, exact distinct IDs, retries, review effort, implementation, integration, test, model cost and subsequent maintenance/regressions. **Cost status: NOT_MEASURED.** No claims of savings, adoption or independent native test execution.

## Delivery and publication

Human-first [issue.md](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/issue.md) and separate cross-linked [constructor-sufficiency.md](https://github.com/opensiro-contributions/camel/blob/opensiro/meta/.opensiro/issues/camel-workforce-validation-roadmap-20261119/constructor-sufficiency.md) both state **NO_GO** and the same accepted vector/P0/P1/P2. Full fork-publication proposed title: `CAMEL Workforce — native result validation vs an independent S3* constructor (OpenSiro plan-only)`; full proposed body is `issue.md`. **Fork Issue: READY_FOR_FORK_ISSUE_APPROVAL — NOT PUBLISHED**, requiring separate exact current-conversation owner consent. **External issue: DRAFT — NOT PUBLISHED** (not needed because #3332 already covers native operator task). No native implementation, fork PR, external original post, Index re-assessment, mandate or outcome KPI.

**Final decision: NO_GO; research closed for now.** The fork-local case preserves the source-backed negative decision but does not establish new S3* capability. Fork attention PAUSE/DORMANT; new effects need an attributable owner change and any separate exact publication approvals.

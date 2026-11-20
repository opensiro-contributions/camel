# CAMEL Workforce — v0.18.1 native-specific follow-up roadmap receipt

- Receipt contract: proposal-gate
- Original repository: camel-ai/camel
- Original HEAD: c619d1fe5aa2182395d02aadddc71b818c1b6c9f
- Observed at: 2026-11-20
- Accepted Index assessment: https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/ca/camel-workforce.md
- Accepted assessment blob SHA: 1d8e2198e02ddceb978d9bb3a5094bc7a40d0d16
- Accepted review ref: 8c791b7b9cf7deab56cb5a92818c34499af9097f
- Accepted reviewed at: 2026-09-17
- Accepted Index commit: c2e43bf4750841277b3e58d8ba80314121734764
- Accepted Profile version: 0.2.1
- Accepted Skills methodology version: 0.3.1
- Accepted VSM vector: S1=A · S2=C · S3=A · S3*=— · S4=— · S5=—
- System in focus: First-party CAMEL Workforce in AUTO_DECOMPOSE and PIPELINE with worker tasks, task-agent quality/recovery, coordinator, dependency release and callbacks; excludes application-side governance, arbitrary CAMEL agents and third-party integrations outside supported Workforce
- Matching working fork: opensiro-contributions/camel
- Fork owner control: ACTIVE/ALLOW on opensiro/meta, rechecked 2026-11-20
- Repository-wide source map: camel/societies/workforce/workforce.py; camel/societies/workforce/workforce_callback.py; camel/societies/workforce/events.py; camel/societies/workforce/prompts.py; camel/societies/workforce/task_channel.py; test/workforce/test_workforce_callbacks.py; test/workforce/test_workforce_pipeline.py; docs/key_modules/workforce.md; CONTRIBUTING.md; native Issues and PRs
- Evaluation object: HYPOTHETICAL opt-in independent raw-artifact task-result audit with lawful downstream hold/rework before dependent work starts in CAMEL Workforce; distinct from ordinary TaskAgent quality or five-paper deduplication
- Existing-work overlap: SHIPPED TaskAgent _analyze_task quality/recovery and observer-only WorkforceCallback, merged PR #4041 stream telemetry, OPEN PR #3979 plan and event enrichment, OPEN PR #4275 turn-level debt/ledger, OPEN PR #3395 TaskAgent deduplication; none verified as the full independent evidence plus pre-release hold/return chain
- Our on-top contribution: Optional developer-composed independent auditor and raw evidence provider, exposed via a pre-completion Workforce audit decision seam; attributed PASS/CHALLENGE/INCONCLUSIVE gates downstream completion, bounded authorized correction and re-audit across supported modes
- Incremental benefit: Hypothetical distinction between accepted worker result and independently substantiated raw evidence before releasing dependent tasks; unproven value and maintenance cost
- Decision scope: One source-native S3* C-construction hypothesis under v0.18.1 neutrality; no product decision, implementation, Index regrade or forced maintainer adoption
- Priority rationale: S1/S2/S3 already have supported ownership or gate; S4 lacks a proven specific prospective stimulus; S5 belongs to parent/application; S3* can reuse the actual Workforce quality-to-completion seam and dependency release to implement a separately owned corrective audit
- Target transition: S3*=— -> S3*=C
- P1 dependencies: Verify parent-approved auditor raw-artifact rights, exact pre-completion hook semantics in both AUTO_DECOMPOSE and PIPELINE, actual task-state interlock, retry-limit behavior, independent readback and targeted native test design; tests NOT_RUN
- P2 optional: NONE
- Proposed C construction: Optional first-party pre-completion audit adapter after worker result and in-path quality handling but before _handle_completed_task/dependency release, invoking a separately configured autonomous auditor with immutable artifact evidence and owner-scoped options PASS/CHALLENGE/INCONCLUSIVE; CHALLENGE requires hold plus lawful rework/re-audit, missing owner/evidence is not silently PASS
- C sufficiency falsifier: Equivalent shipped independent raw-evidence audit with authority to prevent downstream release and close feedback already exists; proposed interface can only read summaries or cannot prevent dependent execution; no lawful separate reviewer rights; or callback/log transport is mistaken for a decision owner
- Scenario basis: HYPOTHETICAL
- Proposal-stage decision: GO
- Research disposition: NEEDS_EVIDENCE
- Proposed validation: With a real raw source artifact, compare a truthful and fabricated worker citation at same input; assert reviewer PASS vs CHALLENGE, downstream hold and later independent re-audit, plus missing/revoked owner, stale evidence, parent pause and retry exhaustion in AUTO_DECOMPOSE and PIPELINE; NOT_RUN
- Validation state: NOT_RUN
- Proposal falsifier: If current first-party quality/observer path or a current merged original PR gives the same independently owned evidence decision, hold, correction and returned effect without new constructor, or if legitimate interception is unsupported
- Result: NEEDS_EVIDENCE
- External issue: DRAFT — NOT PUBLISHED
- Public fork Issue: DRAFT — NOT PUBLISHED
- Cost status: NOT_MEASURED
- S1 disposition: S1=A workers act on scoped tasks through model/tool outputs; no new C target
- S2 disposition: S2=C dependency graph and pending/completed gating in _post_ready_tasks coordinate worker execution; no duplicate C
- S3 disposition: S3=A Coordinator assigns current work and native recovery/replanning under configured limits; no new C
- S3* disposition: S3*=— historically; quality scorer and callbacks share normal control/logging, while independent raw-evidence auditor decision and held downstream release are not evidenced as a complete current first-party path; P0 HYPOTHETICAL
- S4 disposition: S4=— historically; memories and current-task replanning alone do not demonstrate separate external prospective choice-to-later-operation ownership, DEFER with intent UNVERIFIED
- S5 disposition: S5=— historically; user/application supplies objective, tool rights and pause/stop, parent policy stays parent-governed; NO_TARGET

## Identity and pins

Historical accepted https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/ca/camel-workforce.md, blob `1d8e2198e02ddceb978d9bb3a5094bc7a40d0d16`, matching catalog review-ref `8c791b7b9cf7deab56cb5a92818c34499af9097f`, reviewed 2026-09-17 (Profile 0.2.1 / Skills 0.3.1). Current original [HEAD](https://github.com/camel-ai/camel/commit/c619d1fe5aa2182395d02aadddc71b818c1b6c9f) is separately observed and not a new Index grade. First-pass independent source-only [checkpoint](https://github.com/opensiro/upstream/issues/58#issuecomment-7045477719) was published **before** historical case files were read. Earlier Wave v0.18 case [commit e4c7830](https://github.com/opensiro-contributions/camel/commit/e4c78300c6cf44ad1044c7ef35b683d217be42c9) is historical provenance; the v0.18.1 same-case finding confirms GO/NEEDS_EVIDENCE and **narrows its implementation seam** rather than inventing another case.

## Rights and authority

Verified fork `opensiro-contributions/camel@opensiro/meta` owner state ACTIVE / ALLOW. Original [CONTRIBUTING.md](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/CONTRIBUTING.md) requires an accepted prior discussion for code PRs, meaningful human review and test proof for AI-assisted code. Application/parent defines audit rights, original product owners control adoption. Internal fork metadata updates only; no third-party or public fork issue/comment/PR, code, autonomous S5 grant or Index update.

## Existing work / overlap

[camel/societies/workforce/workforce.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py) uses `_analyze_task(..., for_failure=False)` around line 1645 and quality handling around lines 5429–5713, including a low-quality retry exhaustion path that can still call `_handle_completed_task`. `_handle_completed_task` around line 4941 adds to `_completed_tasks`; `_post_ready_tasks` around line 4397 checks completed dependencies before posting work. [camel/societies/workforce/workforce_callback.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce_callback.py) exposes observer `log_task_completed` and stream methods returning None; [camel/societies/workforce/events.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/events.py) sends result summary/status, not independent raw evidence. [test/workforce/test_workforce_callbacks.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/test/workforce/test_workforce_callbacks.py) checks recording, not audit veto. SHIPPED [merged PR #4041](https://github.com/camel-ai/camel/pull/4041) adds stream events; [open PR #3979](https://github.com/camel-ai/camel/pull/3979) proposes plan/run/state metadata; [open PR #3395](https://github.com/camel-ai/camel/pull/3395) addresses [issue #3332](https://github.com/camel-ai/camel/issues/3332) five-paper dedup/TaskAgent post-aggregation validation; [open PR #4275](https://github.com/camel-ai/camel/pull/4275) introduces a separate turn-level debt check/ledger. [Issue #3072](https://github.com/camel-ai/camel/issues/3072) requests tracing/metrics. None has been verified to close the exact proposed S3* audit decision plus independent raw evidence plus downstream hold/re-audit.

## Function ownership

- **S1** historical **A** — scoped worker model/tool execution; already operating, no C target.
- **S2** historical **C** — Workforce dependency and pipeline gates; no duplicate constructor.
- **S3** historical **A** — Coordinator owns current assignment and bounded recovery; not confused with independent audit.
- **S3*** historical **—** — optional external independent artifact/auditor decision on a completed result before dependency release is a proposed C, not shipped.
- **S4** historical **—** — no established independently owned future external change feedback; DEFER, omission intent UNVERIFIED.
- **S5** historical **—** — ultimate policy, objectives, rights and approvals belong to parent/application; no invented local policy actor.

## Parallel contribution-on-top review

| S3* C-sufficiency link | Track A: original-native coverage | Track B: smallest missing native component | Falsifier |
| --- | --- | --- | --- |
| Independent artifact-based finding | In-path TaskAgent quality/recovery, observer callbacks, Task.result and stream events | Developer-configured autonomous reviewer with separate read-only raw evidence provider, pinned artifact criteria, PASS/CHALLENGE/INCONCLUSIVE receipt | Same worker summary or score used; no legitimate independent evidence |
| Lawful decision and enforcement | Existing pre-completion branch, recovery strategies, dependency release when completed | Opt-in audit decision before `_handle_completed_task` plus state interlock in `_post_ready_tasks`; CHALLENGE/INCONCLUSIVE holds affected dependency while rights are checked | Observational callback cannot stop later task; timeout silently passes |
| Returned feedback | Workforce recovery/retry/reassign, native Task state, parent pause/stop | Authorized correction and later independent re-audit tied to task/evidence version, not automatic policy override | No verified subsequent effect or parent right absent |

## Capability priority

**P0:** S3*=— -> S3*=C — optional source-native independently composed, rights-bound task-result audit before Workforce downstream acceptance. **P1:** verify actual hook and dependency interlock, independent raw evidence, parent approval, tests under both native modes, missing reviewer and retry limit. **P2:** NONE. Scope and uncertainty are qualitative only, no new score.

## Implementation options

Smallest design hypothesis: add **opt-in audit callback/adapter with decision semantics** at Workforce's actual returned-task-to-completed path; keep existing `WorkforceCallback` purely logging unless explicitly redesigned, so notification cannot masquerade as veto. Let the developer attach an independently configured read-only reviewer with source-artifact access, immutable evidence identifier and lawful PASS/CHALLENGE/INCONCLUSIVE choices. A CHALLENGE marks the result ineligible for dependency release until authorized retry/reassignment and re-audit; a missing reviewer or invalid/stale evidence must not silently become PASS. Parent pause/stop and max retry remain authoritative. Test that completion aggregation and both PIPELINE (can intentionally propagate failure) and AUTO_DECOMPOSE honor the **new distinct audited/unaudited state** without globally changing legacy defaults. Alternative: no new first-party C if existing application-only wrapper offers the same supported and legitimate closure; this must be demonstrated, not inferred from a similarly named PR. No product code is implemented here.

## Specification and domain alternatives

Before reading history, the v0.18.1 follow-up [first pass](https://github.com/opensiro/upstream/issues/58#issuecomment-7045477719) independently chose the same S3* function as the historical 2026-11-19 [v0.18 receipt](https://github.com/opensiro-contributions/camel/commit/e4c78300c6cf44ad1044c7ef35b683d217be42c9), but the new hypothesis specifies **the native task-completion and dependency-release boundary**, both supported modes and failure to release semantics. The older [five-paper duplicate handling issue #3332](https://github.com/camel-ai/camel/issues/3332) is a different S3/quality object and its old NO_GO is not reversed. Source does not justify labeling S4/S5 omissions deliberate; no Profile/Skills change is proposed. Original maintainer priorities for this S3* feature: NOT_STATED.

## Cost experiment

Future matched Workforce trial: identical research worker jobs with one substantiated citation and one fabricated citation. Compare shipped TaskAgent quality/recovery vs proposed independently evidenced audit on actual false-pass prevention and lawful rework, along with integration/review, latency, tokens, tests and maintenance. **NOT_RUN; NOT_MEASURED.** The proposition is architectural feasibility, not proven cost saving or maintainer preference.

## Delivery and publication

[Human issue draft](issue.md), [AI constructor contract](constructor-sufficiency.md), and this proposal-gate receipt remain in the **same fork-local case**. `GO / NEEDS_EVIDENCE` means plan-only, no shipped C and no Index regrade. Native tests NOT_RUN; external original/public fork interactions NOT PUBLISHED. Historic status-only Upstream PRs remain Supplementary only under merged [reporting hygiene PR #89](https://github.com/opensiro/upstream/pull/89). Terminal status only in [Upstream #58](https://github.com/opensiro/upstream/issues/58).

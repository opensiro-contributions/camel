# camel-ai/camel — Upstream #58 independent v0.18 receipt

- Receipt contract: proposal-gate
- Original repository: camel-ai/camel
- Original HEAD: c619d1fe5aa2182395d02aadddc71b818c1b6c9f
- Observed at: 2026-11-19
- Accepted Index assessment: https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/ca/camel-workforce.md
- Accepted assessment blob SHA: 1d8e2198e02ddceb978d9bb3a5094bc7a40d0d16
- Accepted review ref: 8c791b7b9cf7deab56cb5a92818c34499af9097f
- Accepted reviewed at: 2026-09-17
- Accepted Index commit: c2e43bf4750841277b3e58d8ba80314121734764
- Accepted Profile version: 0.2.1
- Accepted Skills methodology version: 0.3.1
- Accepted VSM vector: S1=A · S2=C · S3=A · S3*=— · S4=— · S5=—
- System in focus: Supported first-party CAMEL Workforce AUTO_DECOMPOSE and PIPELINE worker/coordinator task execution, result aggregation, quality and callback surfaces; excludes host governance and third-party deployments
- Matching working fork: opensiro-contributions/camel
- Fork owner control: ACTIVE/ALLOW per .opensiro/state.json
- Repository-wide source map: camel/societies/workforce/workforce.py; camel/societies/workforce/workforce_callback.py; docs/key_modules/workforce.md; original README, docs, tests, license, contributing, original Issues/PRs
- Evaluation object: Hypothetical external-source citation integrity review requiring audit separate from ordinary TaskAgent validation; no observed maintainer demand or measured benefit
- Existing-work overlap: TaskAgent aggregation/quality and failure recovery are in the coordinator control path; callbacks observe lifecycle but do not veto acceptance; open PR #3395 adds duplicate/refinement checks and is NOT shipped
- Our on-top contribution: Opt-in independent evaluator_agent injected at the Workforce boundary, reading stable citations/worker evidence rather than a mutable coordinator summary, able to accept/hold/request bounded rework before accepted completion, with a durable disposition and parent-checked authority
- Incremental benefit: hypothetical independent auditable correctness decision unavailable from same-owner quality checks; not measured
- Decision scope: one source-pinned proposed C capability, not whole-project or Index regrade
- Priority rationale: S3* has defensible distinct external-evidence actor, opt-in port and feedback; other functions have owner or no qualified scenario
- Target transition: S3*=— -> S3*=C
- P1 dependencies: Verify existence of an authorized pre-terminal interception; contrast TaskAgent/#3395 and separate evidence access; confirm that proposed reviewer returns a later-work correction
- P2 optional: NONE
- Proposed C construction: Opt-in independent evaluator_agent injected at the Workforce boundary, reading stable citations/worker evidence rather than a mutable coordinator summary, able to accept/hold/request bounded rework before accepted completion, with a durable disposition and parent-checked authority
- C sufficiency falsifier: If TaskAgent/PR #3395 or a user supplied callback already provides independently sourced pre-finalization veto and corrective feedback with the same parent rights, or lawful terminal interception is unavailable, the proposed new C is unnecessary
- Scenario basis: HYPOTHETICAL
- Proposal-stage decision: GO
- Research disposition: NEEDS_EVIDENCE
- Proposed validation: Same two Workforce research tasks with supported and fabricated cited outputs; compare TaskAgent baseline, independent accept/hold/rework, missing reviewer, stale review, parent pause and retry exhaustion; NOT_RUN
- Validation state: NOT_RUN
- Proposal falsifier: If TaskAgent/PR #3395 or a user supplied callback already provides independently sourced pre-finalization veto and corrective feedback with the same parent rights, or lawful terminal interception is unavailable, the proposed new C is unnecessary
- Result: NEEDS_EVIDENCE
- External issue: DRAFT — NOT PUBLISHED
- Public fork Issue: DRAFT — NOT PUBLISHED
- Cost status: NOT_MEASURED
- S1 disposition: first-party autonomous operational tasks under native tool feedback
- S2 disposition: dependency scheduling prevents premature concurrent tasks
- S3 disposition: Coordinator chooses worker assignment and current-task recovery
- S3* disposition: quality evaluator is within current control; callbacks are observer-only, proposed separate evidence audit is unshipped
- S4 disposition: current failure replanning is not independent prospective external intelligence
- S5 disposition: operator, deployment and user retain ultimate constraints

## Identity and pins

Pinned [Index assessment](https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/ca/camel-workforce.md), review [8c791b7b9cf7deab56cb5a92818c34499af9097f](https://github.com/camel-ai/camel/commit/8c791b7b9cf7deab56cb5a92818c34499af9097f), indexed 2026-09-17, blob 1d8e2198e02ddceb978d9bb3a5094bc7a40d0d16, Profile 0.2.1, Skills 0.3.1. Original [current HEAD](https://github.com/camel-ai/camel/commit/c619d1fe5aa2182395d02aadddc71b818c1b6c9f) is distinct; no new Index grades. Source-first research preceded old case comparison.

## Rights and authority

Matching writable fork parent checked and owner-controlled `opensiro/meta` state ACTIVE/ALLOW read back. License/contributing assessed; CAMEL AI policy demands accepted discussion, human review and tests; Cline needs approved feature issue first. No public fork Issue, original Issue/comment/PR or product code authorized. Parent policy remains authoritative.

## Existing work / overlap

Source [camel/societies/workforce/workforce.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py); [camel/societies/workforce/workforce_callback.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce_callback.py); [docs/key_modules/workforce.md](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/docs/key_modules/workforce.md). Native work [issues / 3332](https://github.com/camel-ai/camel/issues/3332); [pull / 3395](https://github.com/camel-ai/camel/pull/3395); [pull / 3979](https://github.com/camel-ai/camel/pull/3979). TaskAgent aggregation/quality and failure recovery are in the coordinator control path; callbacks observe lifecycle but do not veto acceptance; open PR #3395 adds duplicate/refinement checks and is NOT shipped. A new agent name alone is neither a source-grounded C nor permission for a product change.

## Function ownership

- **S1** historical **A**: first-party autonomous operational tasks under native tool feedback. NO_TARGET or DEFER.
- **S2** historical **C**: dependency scheduling prevents premature concurrent tasks. NO_TARGET or DEFER.
- **S3** historical **A**: Coordinator chooses worker assignment and current-task recovery. NO_TARGET or DEFER.
- **S3*** historical **—**: quality evaluator is within current control; callbacks are observer-only, proposed separate evidence audit is unshipped. P0 candidate.
- **S4** historical **—**: current failure replanning is not independent prospective external intelligence. NO_TARGET or DEFER.
- **S5** historical **—**: operator, deployment and user retain ultimate constraints. NO_TARGET or DEFER.

## Parallel contribution-on-top review

| Necessary function-specific outcome | Track A: shipped/Issue/PR | Track B: independent minimum addition or NONE | Falsifier |
| --- | --- | --- | --- |
| Hypothetical external-source citation integrity review requiring audit separate from ordinary TaskAgent validation; no observed maintainer demand or measured benefit | TaskAgent aggregation/quality and failure recovery are in the coordinator control path; callbacks observe lifecycle but do not veto acceptance; open PR #3395 adds duplicate/refinement checks and is NOT shipped | Opt-in independent evaluator_agent injected at the Workforce boundary, reading stable citations/worker evidence rather than a mutable coordinator summary, able to accept/hold/request bounded rework before accepted completion, with a durable disposition and parent-checked authority | If TaskAgent/PR #3395 or a user supplied callback already provides independently sourced pre-finalization veto and corrective feedback with the same parent rights, or lawful terminal interception is unavailable, the proposed new C is unnecessary |
| Later operational closure and parent rights | Real native task/host feedback, license and parent authority | Before-terminal receipt must authorize accept/hold/correct and feed a later Workforce retry | Same result without distinct owner or without lawful enforcement |

## Capability priority

P0: S3*=— -> S3*=C. P1: Verify existence of an authorized pre-terminal interception; contrast TaskAgent/#3395 and separate evidence access; confirm that proposed reviewer returns a later-work correction. P2: NONE. Research **GO/NEEDS_EVIDENCE**. The historical states are not a defect checklist.

## Implementation options

Opt-in independent evaluator_agent injected at the Workforce boundary, reading stable citations/worker evidence rather than a mutable coordinator summary, able to accept/hold/request bounded rework before accepted completion, with a durable disposition and parent-checked authority. Compare simpler alternative TaskAgent aggregation/quality and failure recovery are in the coordinator control path; callbacks observe lifecycle but do not veto acceptance; open PR #3395 adds duplicate/refinement checks and is NOT shipped. Proposed C requires eligible inputs, decisive actor, lawful enforcement, actual later operation and returned feedback; these are a source-mapped design, not a shipped or tested constructor. Falsifier: If TaskAgent/PR #3395 or a user supplied callback already provides independently sourced pre-finalization veto and corrective feedback with the same parent rights, or lawful terminal interception is unavailable, the proposed new C is unnecessary.

## Specification and domain alternatives

Previous same-HEAD NO_GO case concerns five-paper deduplication. This GO does not overturn that finding: it addresses distinct independent external-evidence audit ownership.. Original authors own implementation; historical different case did not determine this first-pass outcome. Missing S4/S5 code does not imply a deliberate omission; intention UNVERIFIED. No Profile/Skills changes implied.

## Cost experiment

Matched native comparator: Same two Workforce research tasks with supported and fabricated cited outputs; compare TaskAgent baseline, independent accept/hold/rework, missing reviewer, stale review, parent pause and retry exhaustion; NOT_RUN. Measure correct decisions, reviewer/regression effort, latency, tokens, human approval and maintenance cost. NOT_RUN; NOT_MEASURED.

## Delivery and publication

[Human](issue.md) and [AI](constructor-sufficiency.md) derive this **GO/NEEDS_EVIDENCE**. Internal OpenSiro fork metadata only; external issue DRAFT — NOT PUBLISHED. Current Index and original product untouched. No native tests, CI or cost measurements asserted.

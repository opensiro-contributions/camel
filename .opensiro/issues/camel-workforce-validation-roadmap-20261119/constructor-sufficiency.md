# camel-ai/camel — Upstream #58 AI constructor and acceptance contract

**Target transition:** S3*=— -> S3*=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

[issue.md](issue.md) · canonical [roadmap.md](roadmap.md). Internal PLAN_ONLY; no current assessment vector reasserted here.

## Boundary and decision right

Supported first-party CAMEL Workforce AUTO_DECOMPOSE and PIPELINE worker/coordinator task execution, result aggregation, quality and callback surfaces; excludes host governance and third-party deployments. Hypothetical external-source citation integrity review requiring audit separate from ordinary TaskAgent validation; no observed maintainer demand or measured benefit. Existing source: [camel/societies/workforce/workforce.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py); [camel/societies/workforce/workforce_callback.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce_callback.py); [docs/key_modules/workforce.md](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/docs/key_modules/workforce.md). Independent decisive owner must choose more than transport/relabeling; parent action approval/denial is respected.

## Parallel native A versus constructor B

| Logical requirement | Native Track A | Minimal Track B | Falsifier |
| --- | --- | --- | --- |
| Evidence and eligible decision options | TaskAgent aggregation/quality and failure recovery are in the coordinator control path; callbacks observe lifecycle but do not veto acceptance; open PR #3395 adds duplicate/refinement checks and is NOT shipped | Opt-in independent evaluator_agent injected at the Workforce boundary, reading stable citations/worker evidence rather than a mutable coordinator summary, able to accept/hold/request bounded rework before accepted completion, with a durable disposition and parent-checked authority | If TaskAgent/PR #3395 or a user supplied callback already provides independently sourced pre-finalization veto and corrective feedback with the same parent rights, or lawful terminal interception is unavailable, the proposed new C is unnecessary |
| Applied action and feedback | Existing worker run/status or host/catalog update; current owner retains policy | Opt-in reviewer returns immutable accept/hold/rework receipt; before-terminal gate, bounded rework and later task feedback | Same task outcome possible without candidate reviewer |

## C sufficiency and priority

The independent reviewer would read worker provenance/citations, form its own evaluation, gate terminal acceptance before the coordinator concludes, and send bounded corrective work into the native scheduler, reporting terminal outcome. Neither passive callback nor #3395 ordinary TaskAgent dedup grants that protected independent decision right; C remains hypothetical until a supported port and tests exist. P1: Verify existence of an authorized pre-terminal interception; contrast TaskAgent/#3395 and separate evidence access; confirm that proposed reviewer returns a later-work correction. P2: NONE; no second C target invented.

## Proposed native validation — NOT_RUN

Same two Workforce research tasks with supported and fabricated cited outputs; compare TaskAgent baseline, independent accept/hold/rework, missing reviewer, stale review, parent pause and retry exhaustion; NOT_RUN. Compare identical native behavior with and without the proposed owner; check parent permission, stale decisions, compatibility and missing actor. Falsifier: If TaskAgent/PR #3395 or a user supplied callback already provides independently sourced pre-finalization veto and corrective feedback with the same parent rights, or lawful terminal interception is unavailable, the proposed new C is unnecessary. 

## Research and publication

Previous same-HEAD NO_GO case concerns five-paper deduplication. This GO does not overturn that finding: it addresses distinct independent external-evidence audit ownership.. Current GO / NEEDS_EVIDENCE; cost NOT_MEASURED. No original/fork public Issue or third-party PR, no product implementation, no index regrade or executed source tests. AI-assisted research, human approval required for future public communication.

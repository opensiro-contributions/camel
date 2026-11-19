# camel-ai/camel — Upstream #58 independent Human roadmap

**Target transition:** S3*=— -> S3*=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

Canonical [roadmap.md](roadmap.md) · AI/developer [constructor-sufficiency.md](constructor-sufficiency.md). PLAN_ONLY, NOT PUBLISHED.

The accepted [Index assessment](https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/ca/camel-workforce.md) is historical (2026-09-17, Profile 0.2.1 / Skills 0.3.1, blob 1d8e2198e02ddceb978d9bb3a5094bc7a40d0d16); independently reviewed original [HEAD](https://github.com/camel-ai/camel/commit/c619d1fe5aa2182395d02aadddc71b818c1b6c9f) is current source, not current Index grade.

| Function / role | Historical Index | Current owner and source | Priority / candidate |
| --- | --- | --- | --- |
| **S1 · Operations** | A | first-party autonomous operational tasks under native tool feedback | NO_TARGET / DEFER |
| **S2 · Coordination** | C | dependency scheduling prevents premature concurrent tasks | NO_TARGET / DEFER |
| **S3 · Current regulation** | A | Coordinator chooses worker assignment and current-task recovery | NO_TARGET / DEFER |
| **S3* · Independent audit** | — | quality evaluator is within current control; callbacks are observer-only, proposed separate evidence audit is unshipped | P0 proposed |
| **S4 · Prospective environment** | — | current failure replanning is not independent prospective external intelligence | NO_TARGET / DEFER |
| **S5 · Ultimate identity/policy** | — | operator, deployment and user retain ultimate constraints | NO_TARGET / DEFER |

## Operator decision

**Question:** Hypothetical external-source citation integrity review requiring audit separate from ordinary TaskAgent validation; no observed maintainer demand or measured benefit. **Track A:** TaskAgent aggregation/quality and failure recovery are in the coordinator control path; callbacks observe lifecycle but do not veto acceptance; open PR #3395 adds duplicate/refinement checks and is NOT shipped. **Track B:** Opt-in independent evaluator_agent injected at the Workforce boundary, reading stable citations/worker evidence rather than a mutable coordinator summary, able to accept/hold/request bounded rework before accepted completion, with a durable disposition and parent-checked authority. **Rationale:** If TaskAgent/PR #3395 or a user supplied callback already provides independently sourced pre-finalization veto and corrective feedback with the same parent rights, or lawful terminal interception is unavailable, the proposed new C is unnecessary. Only a falsifiable proposal GO, validation NEEDS_EVIDENCE.

## Sources, next step and rights

Original code [camel/societies/workforce/workforce.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py); [camel/societies/workforce/workforce_callback.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce_callback.py); [docs/key_modules/workforce.md](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/docs/key_modules/workforce.md). Issues/PRs [issues / 3332](https://github.com/camel-ai/camel/issues/3332); [pull / 3395](https://github.com/camel-ai/camel/pull/3395); [pull / 3979](https://github.com/camel-ai/camel/pull/3979). P1: Verify existence of an authorized pre-terminal interception; contrast TaskAgent/#3395 and separate evidence access; confirm that proposed reviewer returns a later-work correction. Previous same-HEAD NO_GO case concerns five-paper deduplication. This GO does not overturn that finding: it addresses distinct independent external-evidence audit ownership.. Native tests NOT_RUN, cost NOT_MEASURED. Fork owner control ACTIVE/ALLOW does not authorize an original maintainer message or a public fork Issue; both remain NOT PUBLISHED. AI-assisted draft.

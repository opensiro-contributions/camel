# CAMEL Workforce — optional pre-completion independent artifact audit

**Target transition:** S3*=— -> S3*=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

[roadmap.md](roadmap.md) (canonical case receipt) · [constructor-sufficiency.md](constructor-sufficiency.md) (developer contract). PLAN_ONLY / HYPOTHETICAL; DRAFT — NOT PUBLISHED.

## 1. What changes for the developer?

A developer could opt in to a **separately authorized, evidence-reading reviewer** for selected CAMEL Workforce results, so dependent tasks are not released solely on a worker's self-report or the built-in TaskAgent quality score. The reviewer chooses **PASS, CHALLENGE or INCONCLUSIVE** after checking a pinned underlying artifact (for example, real paper titles and URLs), and an approved CHALLENGE causes bounded rework followed by re-audit.

The proposed new ability is a function-specific S3* audit path — **not** a new generic controller or mandatory safety gate. It is not present as a verified supported feature today, and no maintainer demand or benefits have been established.

## 2. Why S3*? Accepted evidence and whole six-function screen

Accepted historical https://github.com/opensiro/vsm-harness-index/blob/c2e43bf4750841277b3e58d8ba80314121734764/assessments/ca/camel-workforce.md: reviewed 2026-09-17, blob `1d8e2198e02ddceb978d9bb3a5094bc7a40d0d16`, source review ref `8c791b7b9cf7deab56cb5a92818c34499af9097f`, Profile 0.2.1 / Skills 0.3.1. Current original [HEAD](https://github.com/camel-ai/camel/commit/c619d1fe5aa2182395d02aadddc71b818c1b6c9f) examined separately. Historical states are **not current grades or quality scores**.

| Function / plain meaning | Historical Index | Current source and decision owner | C candidate / priority |
| --- | --- | --- | --- |
| **S1 · Operations** | A | [camel/societies/workforce/worker.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/worker.py): worker agent model/tool execution | NO_TARGET — already operational |
| **S2 · Coordination** | C | [camel/societies/workforce/workforce.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py): dependency graph and `_post_ready_tasks` | NO_TARGET — C exists |
| **S3 · Current management** | A | [camel/societies/workforce/workforce.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py): Coordinator assignment and recovery | NO_TARGET — A exists |
| **S3* · Independent audit** | — | [camel/societies/workforce/prompts.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/prompts.py): TaskAgent in-path quality; [camel/societies/workforce/workforce_callback.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce_callback.py) logs, does not close separate audit | **P0** — proposed independent raw-artifact pre-completion review |
| **S4 · Future adaptation** | — | [camel/societies/workforce/workflow_memory_manager.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workflow_memory_manager.py): workflow memory and learning from current runs, not a demonstrated independent prospective external loop | DEFER — intention UNVERIFIED |
| **S5 · Identity/policy** | — | [docs/key_modules/workforce.md](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/docs/key_modules/workforce.md): application supplies objectives, workers and human pause/stop | NO_TARGET — parent retains ultimate rights |

The Index notation is ownership, not a score: `A` autonomous decision owner; `C` supported developer-composed ownership; `P` parent-governed S3/S4/S5; `A(P)/C(P)` independent supported parent path; `—` bounded absent path at the reviewed revision; `?` unresolved evidence. Adding a local S4/S5 or replacing A with C is **not** a general requirement.

**Priority rationale:** S3* has a concrete, currently observable *worker-result acceptance → dependency release* seam. Other functions are currently owned, or their prospective operating demand and authority remain unproven.

## 3. Native baseline and smallest proposed delta

**Shipped Track A:** `_analyze_task` quality scores and recovery are the ordinary TaskAgent/Workforce decision path; `_handle_completed_task` archives accepted work and `_post_ready_tasks` releases dependents. The `WorkforceCallback` methods are observer-only. [Merged #4041](https://github.com/camel-ai/camel/pull/4041) exposes stream telemetry. [Open #3979](https://github.com/camel-ai/camel/pull/3979) proposes plan/edit/run and event metadata, [open #3395](https://github.com/camel-ai/camel/pull/3395) addresses five-paper deduplication, and [open #4275](https://github.com/camel-ai/camel/pull/4275) proposes turn-level production-debt metrics. None is evidenced to close the same independently sourced task-level hold/re-audit chain.

**Proposed Track B:** Add an **optional pre-completion audit decision interface** in the native result handling path, with externally configured read-only auditor and raw evidence provider. Audit outcome is recorded, not just logged; `CHALLENGE / INCONCLUSIVE` must hold dependent work until an application/parent-authorized recovery or escalation resolves the finding and a later independent check returns. The simpler alternative is retaining the built-in TaskAgent score/retry or a supported external application wrapper if sufficient; OpenSiro cannot decide whether CAMEL should adopt this.

## 4. Minimal proposed operational result

**P0:** `S3*=— -> S3*=C` with true independent raw-artifact audit, opt-in pre-completion decision and bounded later-work closure.

**P1:** Check actual injected reviewer rights, Task state interlock in AUTO_DECOMPOSE and PIPELINE, timeout/retry handling and native tests. **P2:** NONE.

**Expected benefit:** hypothetical prevention of an unsupported worker claim from being silently treated as a verified dependency. **Falsifier:** reviewer only sees worker summaries; callbacks cannot hold dependent execution; there is already an equivalent lawful first-party independent audit; or parent permission prohibits enforcement. All are open empirical questions, not reasons to guess maintainer intent.

## 5. Proposed validation, not executed

Use an otherwise-identical Workforce task with a true cited paper and a fabricated paper. Verify that a separately configured reviewer with source access allows the first result and challenges the second; ensure held dependencies stay held until permitted correction and actual re-audit. Check missing reviewer, stale source, denied parent action, retry exhaustion, both Workforce modes and unchanged default behavior. Native tests **NOT_RUN**; cost **NOT_MEASURED**; published current S3* C **NOT_CLAIMED**.

## 6. History, decisions and limits

The previous [v0.18 CAMEL case](https://github.com/opensiro-contributions/camel/commit/e4c78300c6cf44ad1044c7ef35b683d217be42c9) also reached S3* GO/NEEDS_EVIDENCE for a separate citation checker. The new post-v0.18.1 review [sealed before reading history](https://github.com/opensiro/upstream/issues/58#issuecomment-7045477719) independently confirms function choice and narrows the **actual** native completion/dependency release seam. The older five-paper deduplication NO_GO concerns a different evaluation object and remains untouched.

## 7. Independent choices and publication rights

A CAMEL-native, maintainer-reviewed discussion/patch (subject to [CONTRIBUTING.md](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/CONTRIBUTING.md) AI policy); a separately justified OpenSiro Profile/Skills methodology review; or a lawful experimental domain fork. None is automatically required. Public fork Issue and external original Issue/PR/comment **NOT PUBLISHED** — each needs explicit destination, content and current-conversation owner approval. No product-code change or Index regrade.

## 8. Decision and handoff

**Proposal-stage GO / research NEEDS_EVIDENCE.** This is an assessment-neutral **architectural hypothesis**, not a finding of product deficiency or maintainer adoption. Case receipts and evidence: [roadmap.md](roadmap.md), [constructor-sufficiency.md](constructor-sufficiency.md). Prepared with AI assistance, without human sign-off or native test execution.

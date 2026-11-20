# CAMEL Workforce — S3* source-native constructor and verification contract

**Target transition:** S3*=— -> S3*=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

[issue.md](issue.md) · canonical [roadmap.md](roadmap.md). Internal PLAN_ONLY; draft NOT PUBLISHED. Only the canonical receipt owns the historical six-function vector and verdict.

## 1. Function-specific construction boundary and methodology checks

**Boundary:** CAMEL first-party `Workforce` in `AUTO_DECOMPOSE` and `PIPELINE`; configured workers and `task_agent`, coordinator, task channel, lifecycle events, recovery and dependent tasks. Excludes outside CAMEL apps, original repository CI/maintainer reviews and parent operator governance. Current source [c619d1fe5aa2](https://github.com/camel-ai/camel/commit/c619d1fe5aa2182395d02aadddc71b818c1b6c9f). Historical Index pinned in [roadmap.md](roadmap.md), not regraded.

**Function witness:** Worker completes task with potentially false citation; S3 TaskAgent can assess self-reported quality, but S3* requires a different developer-composed auditor with independent source access, a lawful PASS/CHALLENGE/INCONCLUSIVE decision, an actual hold/correction before a downstream task uses that result and returned re-audit feedback. The developer/parent supplies bounded audit scope and tool rights; the auditor cannot grant them to itself.

**Counterfactual:** Without an independently evidence-reading auditor, default TaskAgent can still score/retry/reassign, while callbacks log results. The proposed separate *raw-evidence-based discretionary decision* disappears, even if existing transport and logging remain. Parent may legitimately keep this function external; no S5 promotion or mandatory six-function completeness. Maintainer interest: NOT_STATED.

## 2. Source-pinned baseline and parallel native Track A / on-top Track B

**Native execution:** [camel/societies/workforce/workforce.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce.py) `_analyze_task` (~1645) scores task quality, `_post_ready_tasks` (~4397) posts eligible dependents, `_handle_completed_task` (~4941) completes/archives; `_run` quality branch (~5429–5713) sometimes completes after exhausted recovery. [camel/societies/workforce/workforce_callback.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/workforce_callback.py) callbacks `log_task_completed` and `log_stream_chunk` return `None`: observer events alone cannot act as a pre-completion veto. [camel/societies/workforce/events.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/camel/societies/workforce/events.py) sends result_summary, not independent raw evidence. [test/workforce/test_workforce_callbacks.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/test/workforce/test_workforce_callbacks.py) tests recording, not independent auditing.

**Original alternatives:** SHIPPED [PR #4041](https://github.com/camel-ai/camel/pull/4041) stream events, native quality/recovery. OPEN [PR #3979](https://github.com/camel-ai/camel/pull/3979) richer plan and event metadata, OPEN [PR #3395](https://github.com/camel-ai/camel/pull/3395) five-paper de-dup validator for [Issue #3332](https://github.com/camel-ai/camel/issues/3332), OPEN [PR #4275](https://github.com/camel-ai/camel/pull/4275) turn debt ledger. ISSUE_ONLY [#3072](https://github.com/camel-ai/camel/issues/3072) asks for I/O tracing. None has been verified to provide independent source evidence, lawful task-level hold and later reviewer feedback as a complete supported S3* C constructor.

| S3* necessary C link | Shipped/PR native Track A | Minimum on-top Track B | Stop/falsifier |
| --- | --- | --- | --- |
| Separate decisive auditor with raw proof | TaskAgent quality scoring of `Task.result`; stream and complete observers | Opt-in independent read-only auditor + source-artifact provider, evidence ref/version and PASS/CHALLENGE/INCONCLUSIVE | Auditor just repeats summary or source unavailable |
| Pre-completion effect | `_handle_completed_task` marks done; downstream `_post_ready_tasks` consumes `_completed_tasks` | Insert configured audit decision BEFORE eligible completion and protect dependency release against challenged/inconclusive state | No actual hold or existing fully equivalent native owner |
| Later corrective closure | Native retry/reassign/replan and parent pause/stop | On authorized CHALLENGE, bounded rework/escalate, new evidence pin and subsequent independent re-audit receipt | Parent veto bypassed, stale result auto-passed or no later task change |

## 3. Minimal complete S3* first-party C construction

**Hypothetical native contract:** `Workforce(..., result_audit=<developer-supplied authorized audit adapter>)` or equivalent opt-in setter. This is a **proposed API, not a shipped signature**. The adapter receives a bounded `Task` identifier, immutable result/version and a separate *read-only evidence capability*, not all worker credentials. A distinct autonomous reviewer returns a versioned `PASS / CHALLENGE / INCONCLUSIVE` finding with evidence origin and approved action scope. The Workforce orchestrator enforces the finding before calling `_handle_completed_task` and before `_post_ready_tasks` can release dependents. On CHALLENGE, reuse bounded native failure-recovery choices under parent policy; later revised output is re-audited, with an attributed final receipt. On missing reviewer or evidence, preserve a **HOLD/ESCALATE** state under configured policy rather than inventing approval; leave default non-opt-in operation unchanged.

The smallest required edits are an optional decision seam in the returned-task result/quality branch, minimal eligible-completion/dependency interlock in `_handle_completed_task`/`_post_ready_tasks`, and a scoped evidence/verdict model. This must be reconciled with existing `PIPELINE` failed-dependency propagation and retry exhaustion (the native code currently may complete low-quality tasks after limit). A generic callback that only observes `TaskCompletedEvent` is **too late** for this requirement. Do not rewrite the existing TaskAgent, scheduler or tools unnecessarily.

**Logical precedence:** P1 evidence/authority test → P0 optional constructor and interlock → native positive/negative tests; P2 NONE. No auto rollback, external publication, unauthorized tool mutation, generic S4 updater, new S5 policy owner or Index reclassification. If a supported external native wrapper already closes the loop with equal rights, prefer no new C surface.

## 4. Priorities, optional alternative and stopping rules

**P0:** Proposed `S3*=— -> S3*=C` decision/hold/re-audit closure at exact Workforce result acceptance. **P1:** Confirm actual injectability and legal evidence access; compatibility under both modes and native failure semantics; parent approval. **P2:** NONE. Alternative is shipped TaskAgent quality and an application-owned reviewer when no first-party constructor is needed. Stop if equivalent first-party C is proven, separate reviewer authority impossible, reviewer has no independent evidence, result cannot be held, or parent forbids requested effect. Product desirability is maintainer-owned and not an architectural veto.

## 5. Future source-native acceptance — NOT_RUN

Use existing [test/workforce/test_workforce.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/test/workforce/test_workforce.py) and [test/workforce/test_workforce_pipeline.py](https://github.com/camel-ai/camel/blob/c619d1fe5aa2182395d02aadddc71b818c1b6c9f/test/workforce/test_workforce_pipeline.py) as test surfaces; `pytest test/workforce/test_workforce.py test/workforce/test_workforce_pipeline.py test/workforce/test_workforce_callbacks.py` is a **proposed command**, NOT_RUN. Do not assume all optional model dependencies are provisioned. Test with a deterministic isolated fake worker and reviewer plus raw artifact references; no network inference needed.

| Proposed case | Native setup | Expected later operation/feedback | Falsifier |
| --- | --- | --- | --- |
| Valid evidence | Worker says paper A; separately readable source confirms A | Auditor PASS with pinned receipt; dependent task may start | Only quality score consulted |
| False claim | Worker says B; raw source contradicts B | CHALLENGE prevents dependent dispatch; authorized new task/retry and re-audit eventually returns PASS/ESCALATE | Downstream dispatches before audit completes |
| Missing or revoked reviewer | Opt-in reviewer absent/denied or source ref stale | No fake PASS; hold/escalation according to parent, bounded timeout | Fail-open silently |
| Native mode/limit | Same artifact test in AUTO_DECOMPOSE + PIPELINE, quality retry exhaustion and parent pause | No unauthorized dependent release, no default-mode regression | Different mode bypasses interlock |

**Validation:** NOT_RUN; no native tests, CI results or independent cost data claimed. Required future result: demonstrable *reviewer decision → effect on real subsequent task → returned re-audit finding*, not a receipt-only metric.

## 6. Proposal verdict, falsification, evidence ownership and handoff

**Proposal-stage GO / research NEEDS_EVIDENCE**, PLAN_ONLY / HYPOTHETICAL. This supports a coherent proposed constructor only, not shipped S3*=C, validated utility, human review or automatic publication. Primary falsifier: proven equivalent first-party independent raw-artifact audit+downstream hold already shipped, no lawful separate owner, or no actual later-work effect.

Profile owns VSM semantics, Skills assessment procedure, Index historical accepted vector, original CAMEL maintainers product design, and [roadmap.md](roadmap.md) this case's decisions. Historic same-case [v0.18 commit](https://github.com/opensiro-contributions/camel/commit/e4c78300c6cf44ad1044c7ef35b683d217be42c9) preserved; v0.18.1 [source-first checkpoint](https://github.com/opensiro/upstream/issues/58#issuecomment-7045477719) precedes old-case comparison. Next lawful work is targeted tests *only after* separate approval and implementation authorization; third-party/public fork communication requires exact current-conversation approval. Cost NOT_MEASURED. AI assistance disclosed, no presumptive acceptance.

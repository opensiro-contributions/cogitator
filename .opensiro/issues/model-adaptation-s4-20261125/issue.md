# Cogitator — S4 prospective model migration (Opensiro roadmap)
**PLAN_ONLY · GO · NEEDS_EVIDENCE · DRAFT — NOT PUBLISHED**
**One-sentence proposal:** Opt-in prospective model migration for a named Agent binding: external future notice, autonomous bounded choice, matched evaluation, versioned activation for later runs and feedback.
**Canonical decision receipt:** [roadmap.md](roadmap.md)
**Technical companion:** [constructor-sufficiency.md](constructor-sufficiency.md)
**Working fork:** opensiro-contributions/cogitator
**Case:** .opensiro/issues/model-adaptation-s4-20261125/

## 1. Why Opensiro and central accepted VSM assessment
Opensiro studies reusable organizational specifications, not a mandatory architecture or proven savings.
> ACCEPTED HISTORICAL INDEX
> S1=A · S2=A · S3=A · S3*=C · S4=— · S5=—
> [Accepted Index](https://github.com/opensiro/vsm-harness-index/blob/7abafd36dd9216d94e795dac9e6030bc0e8e56a6/assessments/co/cogitator.md), blob 6fff685981c5ad914c14ade826b8d2d24473654c, reviewed 2026-11-20; ref 67b4fde644f648bc1df02a1ab38b211cf2171fbd; Profile 0.2.4 / Methodology 0.3.8.
**Repository-wide audit:** [packages/core/src/agent.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/agent.ts), [packages/core/src/cogitator.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/cogitator.ts), [packages/core/src/cogitator/tool-executor.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/cogitator/tool-executor.ts), [packages/swarms/src/strategies/team.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/swarms/src/strategies/team.ts), [packages/swarms/src/team/board.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/swarms/src/team/board.ts), [examples/swarms/05-agent-team.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/examples/swarms/05-agent-team.ts), [packages/models/src/registry.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/models/src/registry.ts), [packages/core/src/cost-routing/model-selector.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/cost-routing/model-selector.ts), [packages/core/src/llm/model-fallback.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/llm/model-fallback.ts), [packages/evals/src/eval-comparison.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/evals/src/eval-comparison.ts), [packages/workflows/README.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/workflows/README.md), [packages/self-modifying/src/self-modifying-agent.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/self-modifying/src/self-modifying-agent.ts), [docs/SECURITY.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/docs/SECURITY.md), [docs/ARCHITECTURE.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/docs/ARCHITECTURE.md), [.github/workflows/ci.yml](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/.github/workflows/ci.yml); single runtime, source HEAD equals review ref.
| Function | Historical | Current owner/closure | Priority |
| --- | --- | --- | --- |
| **S1 · Operations** | A | Model/tool loop | NO_TARGET |
| **S2 · Coordination** | A | Team lead/board | NO_TARGET |
| **S3 · Current management** | A | Lead revises commitments | NO_TARGET |
| **S3* · Independent review** | C | Checker task and return | NO_TARGET |
| **S4 · Future adaptation** | — | Registry/eval/clone not complete future choice | P0 |
| **S5 · Identity/policy** | — | External app owner | NO_TARGET |
A = autonomous closed owner; C = developer-composable first-party function path; P = parent-governed S3/S4/S5; A(P)/C(P) = additional parent mode; — bounded absence; ? unresolved. These are ownership categories, not quality ranks.
**Priority rationale:** S4 native reuse and prospective scenario; no duplicate A/C work.
**Deliberate exclusions / methodology challenge:** S5 authority external; intention UNVERIFIED; revisit if separate legitimate policy delegation emerges.

## 2. Selected construction hypothesis and operator outcome
**Target transition:** S4=— -> S4=C
**Function-specific disturbance:** HYPOTHETICAL external retirement/release notice.
**Proposed C capability (P0):** Opt-in prospective model migration for a named Agent binding: external future notice, autonomous bounded choice, matched evaluation, versioned activation for later runs and feedback.
**Best native operator alternative:** Registry refreshes structured catalogues; ModelSelector scores current tasks; fallback reacts to failed turns; Agent.clone changes model; EvalComparison compares targets; workflows schedule reviews. Custom app glue could migrate manually, but no integrated prospective discretionary binding/return path was identified.
**Expected user benefit:** HYPOTHETICAL proactive migration before failure; no measured improvement.
**Architectural sufficiency argument:** Developer supplies a migration Agent, approved external notice reader, target binding, candidate allowlist, eval budget and quality floor. Agent interprets a future provider retirement/release notice, chooses keep/evaluate/activate/rollback, consumes matched EvalComparison results and decides within its grant. Proposed first-party service validates authority, freshness and thresholds; compare-and-swap activates a versioned binding and Agent.clone applies model at the next Cogitator.run boundary. Actual modelUsed, binding version and outcome return to the decision owner. No active run mutation or credential/identity changes.

## 3. Existing native work versus missing construction
**Track A — native coverage:** SHIPPED: [packages/models/src/registry.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/models/src/registry.ts), [packages/core/src/cost-routing/model-selector.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/cost-routing/model-selector.ts), [packages/core/src/agent.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/agent.ts), [packages/core/src/llm/model-fallback.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/llm/model-fallback.ts), [packages/evals/src/eval-comparison.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/evals/src/eval-comparison.ts), [packages/workflows/README.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/workflows/README.md). [PR #210](https://github.com/cogitator-ai/Cogitator-AI/pull/210) merged 2026-10-20, head 6040b39f65e17833318fbe79dfef71d6f492c6c4, turn fallback not prospective migration. [PR #304](https://github.com/cogitator-ai/Cogitator-AI/pull/304) merged 2026-10-28, provider configuration. Nine open dependency PRs, no non-PR open issues; model search no exact proposal; Discussion coverage not verified. Maintainer demand NOT_STATED.
**Track B — independent on-top C construction:** Typed notice, scoped migration decision, gated versioned binding and outcome; not refresh/fallback.
**Distinctness and falsifier:** Equivalent complete first-party prospective decision/activation/return already exists, owner cannot choose different lawful outcomes, or later runs do not consume committed binding and return outcome.

## 4. Priorities and minimum sufficient result
- **P0:** Opt-in prospective model migration for a named Agent binding: external future notice, autonomous bounded choice, matched evaluation, versioned activation for later runs and feedback.
- **P1:** Typed evidence and decision contract, allowlist, expiry, eval gate, compare-and-swap binding store and next-run tests.
- **P2:** NONE
**Proposed C-sufficiency verdict:** PROPOSED_C_SUFFICIENT, not shipped or tested.

## 5. Proposed acceptance and stop gates
**Future positive test:** Same mocked future retirement notice and paired eval, authorized owner chooses activation; later run uses candidate, returns actual model/version/outcome. Same inputs with owner choosing keep retain incumbent.
**Future negative test:** Absent/revoked owner, stale evidence/version, failed eval or forbidden model cannot update binding. Active runs and opt-out unchanged; return explicit failure; rollback affects subsequent runs only.
**Proposed falsifier:** Equivalent complete first-party prospective decision/activation/return already exists, owner cannot choose different lawful outcomes, or later runs do not consume committed binding and return outcome.
**Validation state:** NOT_RUN

## 6. Independent paths
**Original-native contribution:** Only after separate approval, reuse native primitives.
**Profile / Skills:** No concrete counterexample established.
**Domain fork:** Optional matched experiment, if authorized.

## 7. Cost hypothesis
NOT_MEASURED. Compare same notice, candidates and eval dataset using app glue vs constructor, count engineering/integration/review/testing/maintenance and operational latency/cost.

## 8. Decision / handoff
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE
**Decision reason / next permitted step:** Architectural hypothesis complete, empirical validation pending. Fork Issues disabled; owner RESUME recorded 2026-11-26; prepare exact original Issue, gated consent pending.
**Agent/developer handoff:** [constructor-sufficiency.md](constructor-sufficiency.md) and [roadmap.md](roadmap.md).
**Rights and publication:** MIT [LICENSE](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/LICENSE); [CONTRIBUTING.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/CONTRIBUTING.md) permits feature requests/Discussions, assignment before PR when picking up an issue. [AGENTS.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/AGENTS.md) supports coding agents, no generated-by footers or AI co-author trailers. No CLA/DCO requirement found in inspected files, not a guarantee. Matching fork verified, Issues disabled; initial DORMANT/PAUSE outside verified #58 queue, superseded by owner RESUME on 2026-11-26 (ACTIVE/ALLOW). No product code or public Issue/PR authorized.
**AI disclosure:** AI-assisted draft; no native test or independent human review presumed.
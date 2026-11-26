# Cogitator prospective model migration
## Identity and pins
- Receipt contract: proposal-gate
- Original repository: cogitator-ai/Cogitator-AI
- Original HEAD: 67b4fde644f648bc1df02a1ab38b211cf2171fbd
- Observed at: 2026-11-25
- Accepted Index assessment: https://github.com/opensiro/vsm-harness-index/blob/7abafd36dd9216d94e795dac9e6030bc0e8e56a6/assessments/co/cogitator.md
- Accepted assessment blob SHA: 6fff685981c5ad914c14ade826b8d2d24473654c
- Accepted review ref: 67b4fde644f648bc1df02a1ab38b211cf2171fbd
- Accepted reviewed at: 2026-11-20
- Accepted VSM vector: S1=A · S2=A · S3=A · S3*=C · S4=— · S5=—
- System in focus: One configured self-hosted SDK runtime, optional first-party packages, future runs of named Agent binding; exclude host company and OSS governance.
- Target transition: S4=— -> S4=C
- Proposed C construction: Developer supplies a migration Agent, approved external notice reader, target binding, candidate allowlist, eval budget and quality floor. Agent interprets a future provider retirement/release notice, chooses keep/evaluate/activate/rollback, consumes matched EvalComparison results and decides within its grant. Proposed first-party service validates authority, freshness and thresholds; compare-and-swap activates a versioned binding and Agent.clone applies model at the next Cogitator.run boundary. Actual modelUsed, binding version and outcome return to the decision owner. No active run mutation or credential/identity changes.
- C sufficiency falsifier: Equivalent complete first-party prospective decision/activation/return already exists, owner cannot choose different lawful outcomes, or later runs do not consume committed binding and return outcome.
- Repository-wide source map: [packages/core/src/agent.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/agent.ts), [packages/core/src/cogitator.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/cogitator.ts), [packages/core/src/cogitator/tool-executor.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/cogitator/tool-executor.ts), [packages/swarms/src/strategies/team.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/swarms/src/strategies/team.ts), [packages/swarms/src/team/board.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/swarms/src/team/board.ts), [examples/swarms/05-agent-team.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/examples/swarms/05-agent-team.ts), [packages/models/src/registry.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/models/src/registry.ts), [packages/core/src/cost-routing/model-selector.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/cost-routing/model-selector.ts), [packages/core/src/llm/model-fallback.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/llm/model-fallback.ts), [packages/evals/src/eval-comparison.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/evals/src/eval-comparison.ts), [packages/workflows/README.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/workflows/README.md), [packages/self-modifying/src/self-modifying-agent.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/self-modifying/src/self-modifying-agent.ts), [docs/SECURITY.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/docs/SECURITY.md), [docs/ARCHITECTURE.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/docs/ARCHITECTURE.md), [.github/workflows/ci.yml](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/.github/workflows/ci.yml); evals measurement primitive, dashboard and gauntlet adjacent.
- Priority rationale: S1/S2/S3 already A, S3* already C; S4 native reuse and plausible future change; S5 retained by external application owner.
- Profile / Methodology: 0.2.4 / 0.3.8, accepted historical review five days old, current HEAD matches review ref.
## Rights and authority
MIT [LICENSE](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/LICENSE); [CONTRIBUTING.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/CONTRIBUTING.md) permits feature requests/Discussions, assignment before PR when picking up an issue. [AGENTS.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/AGENTS.md) supports coding agents, no generated-by footers or AI co-author trailers. No CLA/DCO requirement found in inspected files, not a guarantee. Matching fork verified, Issues disabled; initial DORMANT/PAUSE outside verified #58 queue, superseded by owner RESUME on 2026-11-26 (ACTIVE/ALLOW). No product code or public Issue/PR authorized.
## Existing work / overlap
SHIPPED: [packages/models/src/registry.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/models/src/registry.ts), [packages/core/src/cost-routing/model-selector.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/cost-routing/model-selector.ts), [packages/core/src/agent.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/agent.ts), [packages/core/src/llm/model-fallback.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/llm/model-fallback.ts), [packages/evals/src/eval-comparison.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/evals/src/eval-comparison.ts), [packages/workflows/README.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/workflows/README.md). [PR #210](https://github.com/cogitator-ai/Cogitator-AI/pull/210) merged 2026-10-20, head 6040b39f65e17833318fbe79dfef71d6f492c6c4, turn fallback not prospective migration. [PR #304](https://github.com/cogitator-ai/Cogitator-AI/pull/304) merged 2026-10-28, provider configuration. Nine open dependency PRs, no non-PR open issues; model search no exact proposal; Discussion coverage not verified. Maintainer demand NOT_STATED.
## Function ownership
- S1 disposition: ALREADY_A, model/tool execution.
- S2 disposition: ALREADY_A, team lead, board and arbitration.
- S3 disposition: ALREADY_A, lead revises current commitments.
- S3* disposition: ALREADY_C, separate checker and returned task result.
- S4 disposition: C_CANDIDATE, P0, medium design confidence.
- S5 disposition: NO_TARGET at this recursion, app owner retains authority, intentional omission UNVERIFIED; revisit if separate legitimate policy delegation exists.
## Parallel contribution-on-top review
- Evaluation object: Named binding and prospective migration before external provider change.
- Existing-work overlap: Registry refreshes structured catalogues; ModelSelector scores current tasks; fallback reacts to failed turns; Agent.clone changes model; EvalComparison compares targets; workflows schedule reviews. Custom app glue could migrate manually, but no integrated prospective discretionary binding/return path was identified.
- Our on-top contribution: Opt-in prospective model migration for a named Agent binding: external future notice, autonomous bounded choice, matched evaluation, versioned activation for later runs and feedback.
- Incremental benefit: HYPOTHETICAL reduced manual migration and future retirement exposure with quality gate.
- Decision scope: S4 constructor only, no adoption, no implementation or grade.
## Capability priority
- P0: Opt-in prospective model migration for a named Agent binding: external future notice, autonomous bounded choice, matched evaluation, versioned activation for later runs and feedback.
- P1 dependencies: Typed evidence and decision contract, allowlist, expiry, eval gate, compare-and-swap binding store and next-run tests.
- P2 optional: NONE
- Scenario basis: HYPOTHETICAL
- Proposal-stage decision: GO
- Research disposition: NEEDS_EVIDENCE
- Proposed validation: Same mocked future retirement notice and paired eval, authorized owner chooses activation; later run uses candidate, returns actual model/version/outcome. Same inputs with owner choosing keep retain incumbent. Absent/revoked owner, stale evidence/version, failed eval or forbidden model cannot update binding. Active runs and opt-out unchanged; return explicit failure; rollback affects subsequent runs only.
- Validation state: NOT_RUN
- Proposal falsifier: Equivalent complete first-party prospective decision/activation/return already exists, owner cannot choose different lawful outcomes, or later runs do not consume committed binding and return outcome.
## Implementation options
Reuse Agent.clone and EvalComparison; add prospective binding at new-run boundary rather than auto-refresh or error fallback. Scheduler transport only. NOT_RUN; observed SSH runner lacks Node/pnpm. Future native pnpm --filter @cogitator-ai/core test, pnpm --filter @cogitator-ai/evals test, pnpm --filter @cogitator-ai/models test, pnpm typecheck and pnpm lint; mock backend and external notice, no live provider.
## Specification and domain alternatives
Native integration after separate approval; no concrete Profile/Skills counterexample; optional domain-fork matched experiment.
## Cost experiment
- Cost status: NOT_MEASURED
NOT_MEASURED. Compare same notice, candidates and eval dataset using app glue vs constructor, count engineering/integration/review/testing/maintenance and operational latency/cost.
## Delivery and publication
- Result: PLAN_ONLY
- External issue: DRAFT — NOT PUBLISHED
FORK_ISSUES_DISABLED / NOT_PUBLISHED; initial DORMANT/PAUSE bootstrap superseded by explicit owner RESUME on 2026-11-26, ACTIVE/ALLOW for preparation only.

## Publication review — 2026-11-26
- Publication review source HEAD: 67b4fde644f648bc1df02a1ab38b211cf2171fbd
- Publication review action: original_issue
- Publication review destination: https://github.com/cogitator-ai/Cogitator-AI
- Publication review title SHA256: b01426944d22fdc373a735fa96879342ce1b0036cc94f5898b8d2617d970a9e1
- Publication review history SHA256: adc704b39b6bbec83f4874e6dffc72650258477e7d8a690753ffb2129a75bb17
- Publication review resolution: NEW_DISTINCT_OUTCOME
- Publication review rationale: Current source unchanged; current Index catalog row 1300 and assessment blob unchanged. Bounded original Issue/PR/Discussion and archive discovery returned no matching publication or search errors; not exhaustive novelty proof. Open Issues are dependency PRs. [PR #210](https://github.com/cogitator-ai/Cogitator-AI/pull/210) handles failed turns, even skipping failed models with circuit breakers, but each turn starts from the configured primary; [ModelSelector](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/cost-routing/model-selector.ts) ranks present task requirements. [EvalComparison](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/evals/src/eval-comparison.ts) and Agent.clone enable manual orchestration. The distinct hypothetical outcome is a developer-composed agent choosing and activating an authorized versioned future binding after external notice and paired evaluation, then receiving actual run feedback. Maintainer demand unknown; no demonstrated utility. Recommend new Feature Request for design feedback, owner reserves promotion.

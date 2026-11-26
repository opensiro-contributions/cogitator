# Cogitator — source-native C-construction technical contract
[issue.md](issue.md) · [roadmap.md](roadmap.md)
PLAN_ONLY. **DRAFT — NOT PUBLISHED**.

## 1. Function-specific construction boundary and methodology checks
**Source and mode boundary:** HEAD 67b4fde644f648bc1df02a1ab38b211cf2171fbd; one configured SDK runtime, not company governance. See receipt.
**Target transition:** S4=— -> S4=C
**Six-function dependencies (S1/S2/S3/S3*/S4/S5):** S1 future runs consume binding, existing S2/S3 unchanged, S3* optional existing checker, S5 parent fixes rights; see receipt.
**Function witness:** Developer supplies a migration Agent, approved external notice reader, target binding, candidate allowlist, eval budget and quality floor. Agent interprets a future provider retirement/release notice, chooses keep/evaluate/activate/rollback, consumes matched EvalComparison results and decides within its grant. Proposed first-party service validates authority, freshness and thresholds; compare-and-swap activates a versioned binding and Agent.clone applies model at the next Cogitator.run boundary. Actual modelUsed, binding version and outcome return to the decision owner. No active run mutation or credential/identity changes.
**Counterfactual owner test:** No migration Agent means unchanged binding despite registry/eval; two lawful decisions yield different future bindings.
**Possible methodological negative control:** Fixed model and stable environment need no local S4; omission intent unverified; no S5 delegation.
**Contributor / maintainer priorities:** NOT_STATED

## 2. Source-pinned baseline and parallel native Track A / on-top Track B
**Original native workflow:** Registry refreshes structured catalogues; ModelSelector scores current tasks; fallback reacts to failed turns; Agent.clone changes model; EvalComparison compares targets; workflows schedule reviews. Custom app glue could migrate manually, but no integrated prospective discretionary binding/return path was identified.
**Closest existing solution:** Application glue schedules a notice reader, compares targets and explicitly clones Agent.
**Relevant original Issues/PRs:** SHIPPED: [packages/models/src/registry.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/models/src/registry.ts), [packages/core/src/cost-routing/model-selector.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/cost-routing/model-selector.ts), [packages/core/src/agent.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/agent.ts), [packages/core/src/llm/model-fallback.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/llm/model-fallback.ts), [packages/evals/src/eval-comparison.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/evals/src/eval-comparison.ts), [packages/workflows/README.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/workflows/README.md). [PR #210](https://github.com/cogitator-ai/Cogitator-AI/pull/210) merged 2026-10-20, head 6040b39f65e17833318fbe79dfef71d6f492c6c4, turn fallback not prospective migration. [PR #304](https://github.com/cogitator-ai/Cogitator-AI/pull/304) merged 2026-10-28, provider configuration. Nine open dependency PRs, no non-PR open issues; model search no exact proposal; Discussion coverage not verified. Maintainer demand NOT_STATED.
**On-top distinctness:** Prospective external evidence -> discretionary choice -> durable future binding -> actual feedback; not task ranking or error fallback.
**Source ambiguity / rights blockers:** MIT [LICENSE](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/LICENSE); [CONTRIBUTING.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/CONTRIBUTING.md) permits feature requests/Discussions, assignment before PR when picking up an issue. [AGENTS.md](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/AGENTS.md) supports coding agents, no generated-by footers or AI co-author trailers. No CLA/DCO requirement found in inspected files, not a guarantee. Matching fork verified, Issues disabled; initial DORMANT/PAUSE outside verified #58 queue, superseded by owner RESUME on 2026-11-26 (ACTIVE/ALLOW). No product code or public Issue/PR authorized. Bounded publication history scan on 2026-11-26 found no matching original Issue/PR/Discussion or archive action; no native tests.

## 3. Minimal complete S4 first-party C construction
**Required property:** First-party function-specific developer-composable decision owner, lawful effect and return.
| Native seam | Existing source | Proposed integration | Return |
| --- | --- | --- | --- |
| Signal/options | [packages/models/src/registry.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/models/src/registry.ts) | typed future notice, expiry, allowlist, migration Agent | selected option |
| Compare | [packages/evals/src/eval-comparison.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/evals/src/eval-comparison.ts) | matched evidence and threshold/budget guard | eval outcome |
| Binding | [packages/core/src/agent.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/agent.ts), [packages/core/src/cogitator.ts](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/cogitator.ts) | versioned CAS, opt-in next-run clone and receipt | modelUsed/version/outcome |
**Architectural C-sufficiency argument:** Developer supplies a migration Agent, approved external notice reader, target binding, candidate allowlist, eval budget and quality floor. Agent interprets a future provider retirement/release notice, chooses keep/evaluate/activate/rollback, consumes matched EvalComparison results and decides within its grant. Proposed first-party service validates authority, freshness and thresholds; compare-and-swap activates a versioned binding and Agent.clone applies model at the next Cogitator.run boundary. Actual modelUsed, binding version and outcome return to the decision owner. No active run mutation or credential/identity changes. Catalogue-only updates lack owner; current-run fallback responds to present failure; user glue is baseline.
**Explicit non-goals:** No active run mutation, credentials or policy expansion, generic supervisor, grade change.
**Implementation dependency graph:** P1 scoped contracts/eval/CAS -> P0 closure -> native tests.

## 4. Priorities, optional alternative and stopping rules
**P0 and P1:** Opt-in prospective model migration for a named Agent binding: external future notice, autonomous bounded choice, matched evaluation, versioned activation for later runs and feedback. Typed evidence and decision contract, allowlist, expiry, eval gate, compare-and-swap binding store and next-run tests.
**P2:** NONE
**Alternative path:** Manual clone/eval/scheduled workflow if owner prefers fixed decision.
**Stop:** Equivalent complete first-party prospective decision/activation/return already exists, owner cannot choose different lawful outcomes, or later runs do not consume committed binding and return outcome.

## 5. Future source-native acceptance — derive tests, do not copy a matrix
**Native test commands and entry points:** NOT_RUN; observed SSH runner lacks Node/pnpm. Future native pnpm --filter @cogitator-ai/core test, pnpm --filter @cogitator-ai/evals test, pnpm --filter @cogitator-ai/models test, pnpm typecheck and pnpm lint; mock backend and external notice, no live provider.
**Positive functional closure:** Same mocked future retirement notice and paired eval, authorized owner chooses activation; later run uses candidate, returns actual model/version/outcome. Same inputs with owner choosing keep retain incumbent.
**Independent alternative (where applicable):** Keep instead of activate under identical allowed evidence; rollback prior version only for future runs.
**Negative authority and compatibility (where applicable):** Absent/revoked owner, stale evidence/version, failed eval or forbidden model cannot update binding. Active runs and opt-out unchanged; return explicit failure; rollback affects subsequent runs only.
**Matched native alternative:** Custom glue with same fixture and eval cases, explicit clone update; compare all-in cost.

## 6. Proposal verdict, falsification, evidence ownership and handoff
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE
**Primary falsifier:** Equivalent complete first-party prospective decision/activation/return already exists, owner cannot choose different lawful outcomes, or later runs do not consume committed binding and return outcome.
**Validation state:** NOT_RUN
**Ownership of truth:** Profile semantics, Skills method, Index grade, original implementation/adoption, roadmap.md case decision.
**Cost status:** NOT_MEASURED. Compare same notice, candidates and eval dataset using app glue vs constructor, count engineering/integration/review/testing/maintenance and operational latency/cost.
**Next permitted action:** Prepare and validate same-case original Issue; separate exact public consent.
**Human backlink:** [issue.md](issue.md)
**case receipt:** [roadmap.md](roadmap.md)
**AI disclosure:** AI-assisted; no tests or independent review presumed.
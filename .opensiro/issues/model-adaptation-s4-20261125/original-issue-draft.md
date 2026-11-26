# Opt-in evaluation-gated model migration for future agent runs

## Proposal in the project's own terms

### Problem Statement
When a provider announces a model retirement or a promising replacement, developers may need to evaluate alternatives before existing runs fail. Cogitator already has useful building blocks; a prospective migration process appears to require application-specific orchestration.

### Proposed Solution
Offer an opt-in constructor for a developer-composed migration agent that can evaluate and update a named agent's model binding for subsequent runs, within explicitly granted limits.

**What exists today:** [ModelRegistry](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/models/src/registry.ts), task-aware ModelSelector, runtime fallback, Agent.clone and EvalComparison.
**What may be missing:** A first-party decision, versioned activation and feedback path for prospective migration.
**Closest existing project-native solution:** Schedule a review, run paired evaluations and clone the agent with application-managed configuration.
**Existing discussion:** [PR #210](https://github.com/cogitator-ai/Cogitator-AI/pull/210) implements turn fallback and circuit breakers, not a prospective binding change. No matching proposal found in the bounded Issue/PR/Discussion search on 2026-11-26; not exhaustive.

### Alternatives Considered
Use existing workflow scheduling and manual cloning, or a deterministic evaluation threshold rather than an autonomous migration agent.

### Related Package
@cogitator-ai/core

## How we reached this proposal — Opensiro VSM assessment

OpenSiro uses the Viable System Model to examine organizational functions and decision ownership, not product quality or maturity.

**Historical assessment:** [Accepted Index assessment](https://github.com/opensiro/vsm-harness-index/blob/7abafd36dd9216d94e795dac9e6030bc0e8e56a6/assessments/co/cogitator.md); Index commit 7abafd36dd9216d94e795dac9e6030bc0e8e56a6; assessment blob 6fff685981c5ad914c14ade826b8d2d24473654c; reviewed 2026-11-20; review_ref 67b4fde644f648bc1df02a1ab38b211cf2171fbd; Profile 0.2.4; Methodology 0.3.8.
**Boundary:** One configured self-hosted SDK runtime with optional first-party packages; excludes application-owner and OSS governance.
**Current original HEAD:** [67b4fde644f648bc1df02a1ab38b211cf2171fbd](https://github.com/cogitator-ai/Cogitator-AI/commit/67b4fde644f648bc1df02a1ab38b211cf2171fbd), checked 2026-11-26 separately from the historical assessment.

| Function | Meaning | Historical state | Evidence or limitation |
| --- | --- | --- | --- |
| **S1 · Operations** | Execute work | A | Model/tool execution |
| **S2 · Coordination** | Resolve operational interference | A | Team lead and board |
| **S3 · Current management** | Manage current commitments | A | Lead revision and reassignment |
| **S3* · Independent audit** | Independent checks and feedback | C | Separate checker task |
| **S4 · Future adaptation** | Adapt to external/future change | — | No complete first-party path evidenced |
| **S5 · Identity and policy** | Ultimate policy and authority | — | Application owner outside boundary |

**State notation:** `A` means an autonomous agent closes the function-specific decision and feedback loop in a supported first-party mode; `C` means a first-party constructor is available but the developer composes the actor, authority or closure; `P` means supported parent governance without established local A/C (S3/S4/S5 only); `A(P)` / `C(P)` mean a separately evidenced parent-governed mode alongside A/C; `—` means no material first-party path evidenced within the boundary, not a defect; `?` means insufficient evidence. These are ownership states, not rankings.

## Why this particular construction?

**Whole-repository prioritization:** S1/S2/S3 already have A and S3* has C in the accepted historical assessment. S4 has relevant native building blocks; S5 remains with the application owner. Maintainer priorities are not established.
**Construction hypothesis:** S4=— → S4=C, a future constructor, not a shipped capability or regrade.
**Native building blocks:** [ModelSelector](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/cost-routing/model-selector.ts), [EvalComparison](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/evals/src/eval-comparison.ts), [Agent.clone](https://github.com/cogitator-ai/Cogitator-AI/blob/67b4fde644f648bc1df02a1ab38b211cf2171fbd/packages/core/src/agent.ts).
**Minimal proposed addition:** A typed external notice and candidate interface, a bounded migration decision, and a versioned model binding with evaluation-gated activation and next-run feedback.
**Scope exclusions:** No active-run mutation, credential changes, policy expansion or mandatory S5 delegation.

## Proposed approach and validation

1. The developer configures a migration agent, approved notice reader, candidate allowlist, evaluation budget, and quality floor.
2. The agent considers an upcoming provider retirement or release, compares alternatives on matched cases, and chooses keep, evaluate, activate or roll back. A first-party service validates authority, evidence freshness and thresholds; compare-and-swap updates the named binding, consumed via Agent.clone at the next Cogitator.run boundary.
3. Return actual modelUsed, binding version and outcome. Test that keep and activate yield different authorized outcomes; absent or revoked authority, stale evidence or version, forbidden models and failed evaluations cannot change the binding. Active runs and opt-out applications remain unaffected.

**Hypothesized benefit:** Less custom migration orchestration and fewer surprises from future provider changes.
**How to falsify:** Existing native composition already provides an equivalent complete decision/feedback path, or the proposed constructor cannot preserve lawful choice and actual subsequent-run feedback. Compare against deterministic scheduling and application-managed migration.
**Cost status:** NOT_MEASURED. No runtime tests executed; benefits remain hypothetical.

## Feedback requested

Would this fit Cogitator's architecture, or would a documented composition of existing primitives be preferable? Is the assessment inaccurate or the adaptation deliberately out of scope? Maintainers decide product fit and adoption.

## Three independent ways to participate

- Improve the harness through a small native integration if desired.
- Challenge the VSM mapping or improve the open Profile/Skills methodology.
- Explore a permitted domain-specific fork experiment without requiring original-project adoption.

## Research attribution and AI disclosure

[Opensiro Upstream](https://github.com/opensiro/upstream) · [VSM Profile](https://github.com/opensiro/vsm-harness-profile) · [VSM Skills](https://github.com/opensiro/vsm-harness-skills) · [VSM Index](https://github.com/opensiro/vsm-harness-index).

**AI involvement:** This architectural hypothesis was prepared with AI assistance. No maintainer endorsement, independent human validation, implemented C constructor, new Index grade or measured benefit is claimed.

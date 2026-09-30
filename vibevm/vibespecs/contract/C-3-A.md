# C.3.A - Typed Guard Macros for Kinds + USM (Annex) {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **One-line summary.** These guard macros combine C.3 declaration compatibility, the exact C.3.2 candidate judgment when an actual candidate is current, RoleMask and KindBridge declarations/relations, and A.2.6 Scope without collapsing them. A claim quantified over a kind can be checked at declaration level; applying that claim or a capability to one candidate additionally requires an admissibility check and, for an admissible request, `J(candidate, kind, signatureEdition, slice)`. `true`, `false`, and `unknown` remain classification values, while allow/refuse remains a separate guard disposition. KindAT never appears in a guard.

**Status.** Normative for macro obligations, evaluation order, three-valued/fail-closed discipline, and the conformance checklist; informative for decision trees, examples, and implementation-like skeletons.

**Placement.** Part C (Kinds), identifier **C.3.A**. Audience: engineering managers, editors, reviewers, assurance leads, and authors of regulatory, evidence, ESG, and Method–Work checks.

**Depends on.**

- **A.2.6 USM:** exact `U.ContextSlice`, Claim/Work scope, `Gamma_time`, scope bridges, and SpanUnion.
- **C.3/C.3.1:** exact local kinds and obtaining `U.SubkindOf` relations.
- **C.3.2:** `KindSignature` declaration epistemes, candidate/slice admissibility, `J(candidate, kind, signatureEdition, slice)`, `true`/`false`/`unknown`, and optional extension representations.
- **C.3.3:** obtaining `KindBridge` relations and separate bridge-assertion epistemes carrying `CL^k`, loss, evidence, definedness, and admitted use.
- **C.3.4:** `RoleMask` and `MaskAdapter` declaration epistemes and `J_mask(candidate, kind, kindSignatureEdition, roleMaskEdition, slice)`.
- **C.3.5:** KindAT as an editorial facet forbidden in guards.
- **C.2.2/C.2.3 and Part B:** F–G–R, formality on the owning episteme, bridge consequences, and scope congruence.
- **A.15/A.15.1:** the separation of capability, plan, exact actual Work occurrence, and every episteme about it.

## C.3.A:2 - Problem {#problem}

Older guard shorthand used one two-valued “membership defined” question for several different jobs. That erased the exact candidate and signature edition, collapsed unavailable support into known failure, made a refusal look like a classification result, and allowed a record or bridge assertion to manufacture target truth. Method–Work use added another collapse when a JobSlice, capability row, plan, or log was read as the performed Work occurrence.

C.3.A restores two levels:

- **declaration level:** which exact local kind and `KindSignature` edition a claim quantifies over, and whether that kind is compatible with the receiver's expected kind under C.3.1 order or an obtaining KindBridge; and
- **candidate-use level:** whether one exact target-side candidate satisfies the receiver's exact declaration in that exact slice, with the claim-kind consequence supplied only by the already established C.3.1 order or obtaining KindBridge.

## C.3.A:6 - Conformance checklist (normative) {#conformance-checklist-normative}

| ID | Requirement |
| --- | --- |
| **GC-01** | A universally quantified claim pins both claim-kind and receiving-kind declaration editions; the non-bridged restriction requires the receiving kind to be identical to or a subkind of the claim kind, while producer/output positions use their own direction. No candidate is invented. |
| **GC-02** | Every claim-to-candidate use pins candidate, claim kind, receiving kind, both needed signature editions, and slice; it checks admissibility before evaluating the target receiving judgment and consuming `true`/`false`/`unknown`. An inadmissible request retains `not-applicable` without a judgment. |
| **GC-03** | `not-applicable`, `unknown`, and known `false` remain distinct from each other and from guard refusal. |
| **GC-04** | RoleMask use recovers the declaration episteme and exact masked judgment; any MaskAdapter remains a separate declaration. |
| **GC-05** | Cross-context use compares kind identity and recovers each bridge channel required by its own applicability, the exact target declaration, and a fresh target judgment when a candidate is current; penalties route to R only. |
| **GC-06** | Scope, `Gamma_time`, freshness, type compatibility, admissibility, classification, and disposition remain separate. |
| **GC-07** | SpanUnion preserves one typed claim and line independence; candidate-specific evidence names exact candidates and judgments. |
| **GC-08** | KindAT appears in no guard, and no plan, row, card, log, or slice substitutes for an actual candidate or Work occurrence. |

### C.3.A:6.1 - Proven-equivalent aliases {#proven-equivalent-aliases}

A context-specific guard alias is equivalent only when all required objects, inputs, classification values, bridge distinctions, and disposition boundaries can be recovered. Similar wording or the same final allow/refuse bit is insufficient.

### C.3.A:6.2 - Bridge consequences {#bridge-consequences}

`Phi(CL_scope)` and `Psi(CL_kind)` are monotone non-increasing consequences on the receiving R path under the governing bridge patterns. This Annex prescribes no numeric form. It never performs arithmetic on F or G.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-3#root, C.3.1-C.3.5, spec://ai.lev/fpf-spec/contract/A-2-6#root, spec://ai.lev/fpf-spec/contract/C-2-2#root, spec://ai.lev/fpf-spec/contract/C-2-3#root, spec://ai.lev/fpf-spec/contract/A-15#root, spec://ai.lev/fpf-spec/contract/A-15-1#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-3-4#root, spec://ai.lev/fpf-spec/contract/C-3-5#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-3-A

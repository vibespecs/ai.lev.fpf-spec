# C.27.TA - Temporal Aspect: Time Windows, Rhythm, Cadence, and Currentness: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.27.TA:5 - Archetypal Grounding {#archetypal-grounding}

### C.27.TA:5.1 - Release Cadence {#release-cadence}

`CheckoutSystem-1 had a weekly release cadence during release train R14.`

This is a complete first result: exact bearer, cadence predicate, release-train reference, and R14 window. It does not by itself say that the cadence is good, that quality improved, that particular Work occurred, or that a promised service level was met. Add further fields only when the next use depends on them.

### C.27.TA:5.2 - Source Freshness {#source-freshness}

A benchmark comparison uses a model report from April and a competitor report from June.

C.27.TA names the source-currentness and validity windows. `G.9`, source-use, evidence, and benchmark patterns carry comparator parity, provenance, and evidence use.

### C.27.TA:5.3 - Architecture Recovery Timing {#architecture-recovery-timing}

An architecture move is expected to reduce an interlevel conflict after two release cycles.

C.27.TA states the expected recovery timing for the exact selected structure discussed by the C.30 architecture claim, under the release-cycle reference and window. Use A.22 and the applicable architecture pattern to identify that structure independently; the claim episteme is not its proxy. Use A.3.4 for the proposed structure transformation and evidence/result patterns for any observed effect.

```text
TemporalAspectStatementClaimContent:
  entityOfConcernRef: the exact independently identified selected structure discussed by the C.30 interlevel-conflict claim.
  entityRulePatternCitation: A.22 plus the applicable C.30 architecture-structure pattern.
  sourceOrUseBoundaryRef?: the exact C.30 architecture claim supplying this expected recovery-timing assertion.
  claimOrWorkScopeRef?: exact A.2.6 claim scope for the pump-station operations-service architecture concern during release train R14-R15.
  aspectPredicate: recoveryTiming.
  temporalReference: release train cycle.
  windowOrInterval: two release cycles after the accepted architecture move starts.
  measuredReadingRef?: measurement result for the operations-service conflict indicator, if C.16 measurement is being made.
  directRelationDeclarationRef?: A.3.4 transformation declaration, if that relation is current.
  obtainingRelationOccurrenceRef?: omitted here; the expected reduction is not an obtaining transformation occurrence.
  receivingUseRulePatternCitation: A.3.4 for bounded transformation, C.30 for selected architecture structure, and the evidence/result pattern for an observed effect.
  validityOrCurrentnessCondition?: valid only while the same selected structure, release train, and conflict indicator remain in force.
  refreshOrReopenCondition?: reopen if the conflict indicator worsens, the release train changes, or the selected structure changes before R15 close.
  blockedLocalOverread: this recovery-timing claim does not prove that the architecture move reduced the conflict.
```

### C.27.TA:5.4 - Work Rhythm {#work-rhythm}

A review practice depends on a two-day response rhythm across several review positions and participants. Keep a responsibility claim separate when the temporal account relies on it.

Name a local system-role kind or a separate System-classification judgement only when the receiving claim uses that distinction. If it relies on an assignment, cite the directly declared relation species and its obtaining occurrence with the actual participant values, holder, applicability, and extent under `A.2.1`. An assignment may be current in a plan or availability statement before any response Work occurs; it neither classifies a System nor implies completed Work. Only when the claim says that a System performed dated response Work should the reader first recover that exact performer through A.13 and independently admit the Work under A.15.1. Add F.6 only if the temporal account also consumes precise assignment-bound attribution through the same obtaining A.13 assignment; missing or failed F.6 leaves the Work intact.

C.27.TA names the exact EntityOfConcern, rhythm or cadence predicate, temporal reference, and window. When cross-bearer coordination matters, cite the direct coupling-relation declaration and an obtaining occurrence only after its predicate passes; keep the PatternID as a separate rule citation.

## C.27.TA:6 - Bias-Annotation {#bias-annotation}

Lenses: **Onto**, **Prag**, **Epist**, **Arch**, **Gov**.

Distortions to watch for:

- **rhythm-as-vibe:** rhythm or cadence appears without bearer, timing reference, and window;
- **freshness-as-permission:** currentness is treated as permission, evidence, or gate passage;
- **time-as-transformation:** timing language is treated as the transformation relation;
- **dynamics theft:** a temporal aspect is treated as a state-space or transition-law episteme;
- **measurement theft:** a temporal aspect is treated as a completed measurement construction.

## C.27.TA:8 - Common Anti-Patterns {#common-anti-patterns}

| Anti-pattern | Symptom | Repair |
| --- | --- | --- |
| Cadence without bearer | "Weekly cadence" appears without saying what has the cadence. | Name the exact EntityOfConcern, cadence predicate, temporal reference, and interval; add other fields only when the receiving use needs them. |
| Freshness without window | A source is called current without reference time or validity window. | Name the exact source, current or fresh predicate, reference time or edition, and validity window; add a refresh condition only when the next use depends on it. |
| Recovery without an adequate temporal claim | A claim says "recovery improved" without an exact bearer, temporal reference, or interval. | State the four-part minimum; add a disturbance, measure, rule citation, or relation only when the receiving use depends on it. |
| Rhythm as value | A rhythm is treated as good by default. | Use the direct value, assurance, quality, or proxy pattern for those separate claims. |
| Timing as transformation | A time window is treated as if it specified the change. | Use `A.3.4` for the transformation relation and C.27.TA for the temporal aspect. |

## C.27.TA:9 - SoTA-Echoing {#sota-echoing}

| Source family | Current lesson for C.27.TA | FPF decision |
| --- | --- | --- |
| Control and model-predictive practice | Horizons, constraints, update intervals, and feedback timing are distinct from the controlled object and the control law. | Express temporal aspects as predicates or qualifiers in claim content; use `A.3.3`, evidence, and control-related patterns for models and control claims. |
| David Deutsch and Chiara Marletto, "Constructor theory of time" (`arXiv:2505.08692v3`), version-specific source posture. | A task or transformation specification need not itself specify duration or the internal course of performance; duration and dynamics can be recovered through timer and clock relations among attributes. Reopen this row if a later version changes the task/duration/timer/clock separation used here. | Require C.27.TA temporal aspects to name bearer and temporal reference. Use `A.3.4` for the transformation, `A.3.3` for dynamics episteme, and C.27 only when an authored temporal claim uses the aspect for a practical use. |
| Dynamic treatment regimes and policy evaluation | Intervention timing, follow-up interval, policy window, and outcome window must be separated before causal or policy claims are made. | Use C.27.TA for temporal windows; use `C.28` and evidence patterns for causal-use and policy claims. |
| Object-centric process and event-log practice | A scalar throughput or latency can hide multiple bearers, event types, and interaction windows. | Name the exact EntityOfConcern, temporal predicate, and temporal reference before using a rate, cadence, or trajectory across objects. |
| Rhythm and synchronization research | Rhythm needs a bearer, timing reference, and window; phase or interval structure and coupling matter only when the receiving use relies on them. | Keep rhythm and cadence as predicates or qualifiers in temporal claim content; state a separate temporal-adequacy or other subject assertion only for its current use, and resolve the defining or constraining `ClaimGraph` through C.27 or the relevant pattern locator. |


## C.27.TA:End {#end}

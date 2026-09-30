# C.30.LCA - Control Structure View Adequacy (LCA): depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.30.LCA:5 - Archetypal Grounding {#archetypal-grounding}

| Archetype | Without C.30.LCA | With C.30.LCA |
|---|---|---|
| System | A plant, controller, or supervisor diagram is treated as if the drawing itself established the controlled system's behavior. | The controlled system, controller, observer, planner, supervisor, boundaries, rate bands, actual control relations, and selected control structure remain separately recoverable. |
| Episteme | A control-description publication is read as structure, `U.View`, or proof because it uses familiar control labels. | The exact description episteme has one selected-structure EntityOfConcern; it is a view only through exact E.17.0 conformance. Representation, publication, and proof-like claims stay separate. |

## C.30.LCA:6 - Bias-Annotation {#bias-annotation}

* **Diagram authority bias.** A neat feedback diagram can look more persuasive than the structure, source-to-use path, work-reliance relation, or claim it actually supports. Repair by naming each object or relation and the pattern used to state or test the claim.
* **Stratification-label bias.** A `layer`, `level`, `tier`, or `stack` label can hide whether it names a control relation, rate band, aggregation, scale, organization, Work scope, evidence scope, deployment, or publication section. Repair with `C.30.STRAT`; C.30.LCA applies only to the recovered control-specific case.
* **Supervisor anthropomorphism.** A supervisor label can make an episteme, policy, assignment, or dashboard sound agentive. Repair by recovering the supervision relation first. If action is claimed, recover the exact performer System through A.13 and admit the dated Work and enacted Method independently through A.15.1. Add assignment and F.6 only for an expressly consumed precise assignment-bound attribution; recover authority, responsibility, gate, safety, and evidence separately.
* **Transformation-flow and LCA conflation.** A transformation-flow graph expression and a control description or view can inform each other, but neither replaces the other. Repair by naming the EntityOfConcern, structure kind, and direct relations for each.

This checklist verifies the preceding guidance after the practitioner has chosen the selected repair action; it is not a required project control form and not a substitute for the note, description episteme, conformance occurrence, direct control relation, or repair guidance above.

## C.30.LCA:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
|---|---|---|
| LCA-as-proof | The text says the control stack proves safety, stability, or gate readiness. | Keep the control view and use the relevant dynamics, evidence, assurance, gate, or safety pattern for each proof or claim named by value. |
| Control-layer-as-generic-level | `Layer`, `level`, `tier`, or `stack` is used without a direct control relation, inter-layer relation, rate band, or `B.2.5` supervisor-subholon relation. | Apply `C.30.STRAT`; use C.30.LCA only after a control-specific relation is recovered. |
| Agentive episteme, kind, or assignment | A policy, model, dashboard, local system-role kind, assignment, or architecture note is said to watch, decide, plan, or adapt. | Recover the direct control relation and participant meanings. For actual action, recover the exact performer through A.13 and admit the `U.Work` occurrence independently through A.15.1. Add assignment and F.6 only when precise assignment-bound attribution is expressly consumed; keep publication, source-to-use, work-reliance, authority, responsibility, gate, safety, and evidence relations separate. |
| Transformation-flow and LCA substitution | A transformation-flow graph expression is treated as control architecture, or an LCA diagram is treated as the transformation-flow graph expression. | Recover both exact selected structures and description epistemes separately; use E.17.0 only for actual viewpoint conformance. |
| Hidden rate claim | Multi-rate control is named, but rate adequacy is not checked. | Add `rateSeparationClaimRefs?`; use `C.27.TA` for temporal-aspect or rate-band claims and `C.27` for authored temporal-claim adequacy. |

## C.30.LCA:10 - Rationale {#rationale}

Control architecture is too important to leave to diagram authority and too useful to remove from architecture language. The FPF move is to keep the practice cue and recover control-structure content first: selected structure, controlled holon, actual architecture relation when current, direct control relations and participant meanings, recovered rate or control-layer labels, observation and actuation boundaries, externality boundaries, and next admissible move. Systems, classifications, assignments, Methods, Work, and F.6 attribution are added independently; use their own patterns for authority, responsibility, gate, safety, stability, and evidence. The full record is one description episteme and, only through E.17.0 conformance, the same episteme as `U.View`. It can cite `C.30.STRAT`, `B.2.5`, E.18 transformation-flow structure, dynamics, `C.27.TA`, `C.27`, `C.28`, evidence, assurance, gates, and C.29, but does not absorb their claim kinds.

This protects subject, structure, episteme, View, representation, and publication boundaries. Several descriptions may have the same selected control structure as EntityOfConcern, and one description may be published repeatedly without changing identity, creating the structure, granting view membership, or making direct relations obtain.

## C.30.LCA:11 - SoTA-Echoing {#sota-echoing}

| SoTA and practice source | What it contributes | FPF adoption stance | Practitioner implication |
| --- | --- | --- | --- |
| Anderson, Doyle, Low, and Matni, "System Level Synthesis" (Annual Reviews in Control, 2019). | Structured controller-synthesis practice treats closed-loop responses, constraints, locality, and distributed implementation as explicit synthesis variables and implementation relations rather than as a box-and-arrow guarantee. | Adopt and adapt: use SLS as current control-structure pressure for explicit control-participant meanings, direct relations, locality, rate, and implementation boundaries; do not import SLS proof claims into C.30.LCA. | A distributed-control diagram can start a control-structure description; for stability or robust-performance claims, use the relevant dynamics or control-proof pattern. |
| Ames, Coogan, Egerstedt, Notomista, Sreenath, and Tabuada, "Control Barrier Functions: Theory and Applications" (ECC, 2019). | Safety-critical control separates a controller structure from a safety property and the mathematical certificate or enforcement method used for that property. | Adopt and adapt: keep safety wording visible as a neighboring safety or proof claim, not as control-view adequacy. | When a sentence says the supervisor or controller makes the plant safe, keep the control description and use the relevant safety, dynamics, evidence, or assurance pattern to state and test that claim. |
| Rawlings, Mayne, and Diehl, *Model Predictive Control: Theory, Computation, and Design*, 2nd ed. (2017). | Planner and regulator distinctions, receding horizon, constraint, update period, and model-boundary distinctions are current MPC structure cues. | Adopt as control vocabulary: recover direct control relations and participant meanings, rates, model boundaries, and constraints; add Systems, classifications, assignments, Methods, and Work only when independently current. Handle temporal or rate claims under `C.27.TA`, authored temporal adequacy under `C.27`, and dynamics under `A.3.3`. | A multi-rate or MPC-style note names relation participants, rate bands, and model boundaries before claiming adequacy. |
| Leveson and Thomas, *STPA Handbook* (2018), as systems-theoretic safety-control practice. | Safety analysis treats unsafe control actions, feedback, process models, constraints, and losses as control-structure-relevant distinctions. | Adopt and adapt: allow safety-loss control-structure notes, while keeping safety-case verdicts and evidence sufficiency outside C.30.LCA. | A loss-control diagram can organize the description; it does not close the safety case. |
| FPF `C.2.1`, `A.22`, `C.30`, `C.30.AD`, `E.17.0`, and `C.30.ASV`. | These patterns separate selected control structure, architecture relation, architecture claim, description episteme, viewpoint episteme, conformance occurrence, described holon, and controlled holon. | Bind `ControlStructureView` to one selected `U.Structure` and viewpoint conformance; recover every control relation through the pattern that defines it. | A control view can coordinate several relations without becoming the architecture, relation occurrence, or proof. |


## C.30.LCA:End {#end}

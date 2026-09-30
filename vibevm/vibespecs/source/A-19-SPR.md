# A.19.SPR - Repair State and Status Wording: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.19.SPR:5 - Worked examples {#worked-examples}

Each example starts with the smallest useful final wording. The second paragraph adds detail only for a machine-readable, replayed, or high-consequence use.

### A.19.SPR:5.1 - Physical-system state {#physical-system-state}

**Before:** “Pump 37 is in a good operating state.”

**After:** “Pump 37 satisfies `InspectionOperatingCondition`: its coolant temperature is 72 °C, within the 60–80 °C band, and its discharge pressure is 315 kPa, above the 300 kPa minimum.”

For a relied-on inspection decision, also name the reading time, measurement basis, condition edition, and the event that requires another check. Do not add those fields to a casual status sentence that no decision consumes.

### A.19.SPR:5.2 - Work-entry readiness is not gate passage {#work-entry-readiness-is-not-gate-passage}

**Before:** “Release 12 is ready.”

**After:** “At 10:00, the A.15.5 check found that `PlanItem-Deploy-12` satisfied its release-entry criterion and was ready for work entry until 10:30; recheck if a required input changes. No A.21 gate decision has yet been made.”

When another use must replay the check, add the exact WorkPlan, criterion, checking Work, input facts, result episteme, and reliance window. Add an A.21 sentence only if a distinct `OperationalGate(profile)` actually consumes declared checks and publishes its own decision.

### A.19.SPR:5.3 - Source currentness {#source-currentness}

**Before:** “The source posture is good.”

**After:** “This review uses edition E7 as the accepted decision source. Recheck that use if the edition or the reviewed question changes.”

For automation or consequential reliance, also name the exact source-use relation, currentness result, use window, and the claim that must be reconsidered. The short sentence does not turn the source into evidence, assurance, gate passage, or FPF doctrine.

### A.19.SPR:5.4 - Other direct repairs {#other-direct-repairs}

- **Evidence.** Replace “evidence status incomplete” with “The current evidence path does not yet support reliance on claim C; obtain the missing calibration record and check again.” Add exact evidence and currentness references only when the receiving decision needs them.
- **Publication.** Replace “publication posture allows decision input” with “This publication exposes candidate input X for the decision; the decision rule still evaluates X.” Publication does not decide or assure by itself.
- **Mathematical lens.** Keep `LensUseBoundaryValue` in C.29 when its possible values and intended lens use are defined. State the practical result in ordinary words; the field does not establish evidence, assurance, release, or source authority.
- **Temporal claim.** Keep `dynClaimPosture` in C.27 when its values and temporal use are defined. Say which temporal claim is usable and for what purpose; the field does not upgrade its evidence or authority.
- **Project-side state.** Put review, dispatch, release, admission, or source-control status in the project record that carries it. A pattern may mention only the user-facing boundary needed for its own subject.

## A.19.SPR:7 - Common mistakes {#common-mistakes}

| Mistake | Symptom | Repair |
| --- | --- | --- |
| **Status word as cover** | `posture` or `status` hides a source relation, evidence result, assurance result, gate decision, or release claim. | Say what item has which value or relation under the direct rule. |
| **One broad word replaces another** | `support` becomes `support posture`, `basis posture`, or `source posture`. | Recover the actual source, evidence, assurance, relation, characteristic, or reader-help claim before choosing words. |
| **Technical field without meaning** | A `...Status` or `...Posture` field has no object, possible values, or rule. | Complete those three facts or replace the field with an ordinary sentence. |
| **Project status in pattern prose** | Review, dispatch, landing, release, or source-control state appears as user guidance. | Move it to the project record and keep only the practical boundary the pattern user needs. |
| **Everything becomes a source-language case** | Evidence, assurance, gate, Work, temporal, or lens-use claims are all sent to source or publication repair. | Use the direct pattern for the actual claim. |

## A.19.SPR:9 - Rationale {#rationale}

The problem is not the word `state`. The problem is a sentence that hides what has changed, what is being judged, or which rule makes the judgment meaningful. Recovering those facts first lets FPF keep short engineering language without creating a general status ontology.

Local fields such as `LensUseBoundaryValue` and `dynClaimPosture` remain useful when their object, possible values, and rule are clear. Broad phrases such as `source posture`, `evidence posture`, or `release posture` should instead become the direct sentence or project record the reader actually needs.


## A.19.SPR:End {#end}

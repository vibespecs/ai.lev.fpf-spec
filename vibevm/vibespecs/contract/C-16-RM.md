# C.16.RM - Repair a Measurement Model or Arrangement {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative

## C.16.RM:1 - Problem frame {#problem-frame}

Use this pattern when a measurement disagrees with an expected result or cannot distinguish the cases needed for the work. A detector combines a beam with background light. A voltmeter changes the voltage it measures. A program turns correctly recorded counts and times into an incorrect rate. Each situation offers a different place to repair.

**First useful move.** Put the wanted quantity beside the indication and recover the relation used to connect them. Mark the contribution that prevents the wanted answer. If a detector responds to beam plus background, repeating that reading leaves their separate contributions unknown; a reading with the beam removed can make their difference usable.

The Method selects and carries through a change to a measurement model, its computation or the actual arrangement. The useful result is a corrected interpretation, an adequate changed measurement, a conditional design result or a remaining limitation with its effect on the work. C.16 supplies the measurement, model, performed work and obtained-result meanings.

The examples assume elementary algebra, bounds and units. The subject law, calibration and operating conditions come from the relevant physical or other domain practice. Apply a suitable established correction or repair procedure directly when the fault and applicable remedy are already known. Use the present Method when the choice of what to change remains consequential.

## C.16.RM:2 - Problem {#problem}

A disagreement can arise from the measured subject, its description, the instrument, the instrument model or the calculation. Improving the wrong contribution consumes effort while leaving the wanted answer unavailable. Repeated observations can reduce some random effects and preserve a loading error, background contribution or computational mistake.

A change can also alter the quantity being measured. Cooling a specimen to stabilize an instrument may change the specimen property whose value was wanted at the original temperature. Better agreement in the changed situation therefore needs a relation back to the intended use.

The problem is to locate a useful repair, carry it through the affected relations and establish what the revised result supports. Explaining the historical cause of a fault and obtaining an adequate measurement can require different amounts of work.

## C.16.RM:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Better model and simpler conditions | Describing an influence can be costly; controlling it can change the subject or require new equipment. |
| Fault diagnosis and sufficient repair | Several causes may remain possible while an available change already restores the needed result. |
| Repeated data and structural ambiguity | More readings help only through the distinctions or error reduction their relation supports. |
| Changed arrangement and original target | A more convenient experiment may answer a different question. |
| Numerical correctness and measurement adequacy | Correct calculation can implement an inadequate model; a suitable model can be computed incorrectly. |
| Full restoration and useful completion | A conditional result or adequate bound may settle the work before every uncertainty is removed. |

## C.16.RM:4 - Solution {#solution}

Follow the disagreement from the wanted result through the indication-producing relations. Compare changes at the contribution that matters, choose a sufficient available repair, and use the revised relation to obtain the result needed by the work.

**Align the question and observations → locate the consequential contribution → compare a model, computation or arrangement change → carry through the selected repair → determine what the revised result supports.**

The starting point can be a known fault, an unexplained discrepancy or a proved inability to distinguish the needed cases.

### C.16.RM:4.1 - Align the comparison and target {#align-the-comparison-and-target}

State the quantity or distinction sought, its subject and operating conditions. Put the expected result and obtained indication on a comparable basis: same quantity, time interval, units and relevant preparation. If the expectation concerns an unconnected source but the reading concerns a loaded source, retain that difference in the relation.

Recover how the indication was produced and interpreted. Separate an observed disagreement from an assumed explanation. A temperature-dependent response may come from the subject, sensor or their interaction; the correlation alone leaves those contributions to be distinguished.

Use C.16.MR when the measurement relation itself is missing. Use C.16.IR to find which alternatives fit an available relation and which distinction remains unresolved. A sufficient bound may already answer the question and end the repair attempt.

### C.16.RM:4.2 - Locate the contribution that could change the answer {#locate-the-contribution-that-could-change-the-answer}

Follow the target-to-indication relation far enough to identify the consequential influence or incompatible operation. Ask what each candidate explanation would require changing and what present information bears on it.

| Possible repair location | What to inspect | A useful change |
| --- | --- | --- |
| Subject model | Which interaction, boundary or varying condition is omitted from the predicted quantity? | Include a background contribution or the dependence on the actual preparation. |
| Instrument model | How does the instrument respond in the range and conditions used? | Include loading, offset, saturation or a calibrated nonlinear response. |
| Computation | Does the implemented operation evaluate the intended relation with its units, domains and required accuracy? | Correct a unit conversion, retained branch, numerical approximation or aggregation interval. |
| Subject arrangement | Can a relevant condition be controlled while retaining the target or a usable relation to it? | Shield an unwanted input or hold a consequential condition stable. |
| Measuring arrangement | Can a different interaction or indication distinguish the needed alternatives? | Change the input resistance, operating range, observation timing or reference measurement. |

The table locates choices; the domain Method supplies the physical law or diagnosis that makes one choice appropriate. A common influence can cross several rows. For example, a change in illumination can alter both the subject response and the detector response.

For a suspected computational fault, run a supplied or constructed input whose answer follows from the intended relation. Compare intermediate values, units and branch choices until the divergence is located. A successful calculation on that input checks implementation of the relation. Compare the relation with the actual subject separately when its adequacy is in question.

### C.16.RM:4.3 - Compare changes by their predicted contribution {#compare-changes-by-their-predicted-contribution}

For each serious available repair, change the corresponding part of the relation and determine what would become knowable. An added parameter can represent a missing effect while introducing an unknown that one reading cannot determine. A physical change can remove the effect or make its influence small enough to bound.

A difference measurement is useful when the target changes between two observations in a known way while the influences being cancelled remain sufficiently stable. A larger input resistance is useful when the loading relation shows how much it reduces the consequential error. Repeating an unchanged observation needs its own error or dynamics account to support a narrower conclusion.

Prefer an already available comparison or a small reversible change when it can settle the repair choice. If several explanations predict the same result of a proposed test, that test cannot select among them. Use C.11.DUA to compare the gain from an attainable further observation with its effort and delay.

The needed conclusion sets the reach of diagnosis. Replacing a defective assembly and obtaining the required response may restore the measurement without identifying which internal component failed. Retain the unresolved cause if later reliability, maintenance or causal explanation depends on it. Use C.28 when the required result is a causal attribution.

### C.16.RM:4.4 - Carry the selected repair through the measurement {#carry-the-selected-repair-through-the-measurement}

Keep the target and receiving question fixed while revising the selected contribution. If an alternative target or operating condition is acceptable, make that change part of the receiving decision and derive the relation for the new use.

For a model repair, include the consequential influence and obtain its value, range or relation from available information. An added correction term earns its use through that basis. Carry any remaining uncertainty into the sought result.

For a computation repair, correct the operation and recalculate the affected results from retained inputs. Reuse observations whose meaning and conditions still fit. Identify outputs that depended on the incorrect operation so that subsequent comparisons use the repaired result.

For an arrangement change, derive how preparation, interaction, indication and calibration are affected. An attenuator can move a detector out of saturation while introducing an attenuation factor and its uncertainty. A shield can remove ambient light while changing alignment. Retain the conditions that make the new relation appropriate.

A planned change supports a conditional result. Once performed, use the resulting observations and conditions to interpret that measurement. Older observations can still answer their original question or be reinterpreted through a supported revised relation; changing a model now does not supply a new past observation.

### C.16.RM:4.5 - Test the repaired contribution at the needed scope {#test-the-repaired-contribution-at-the-needed-scope}

Choose a comparison capable of exposing the defect the repair addresses. For computation, compare with an independently obtained result for the same mathematical input. For an omitted influence, use a relevant reference condition, intervention or already available contrast. For a claimed operating range, include the range boundary or change of behavior on which the claim depends.

Read the result through the repaired measurement relation. Propagate the uncertainty that could change the receiving answer, and use C.16.IR when compatible alternatives or an outer bound require interpretation. A closer numerical match can still leave a consequential ambiguity.

When the comparison leaves the needed answer unresolved, return to the remaining contribution. A further repair may be justified, or the useful result may be a narrower claim, a changed use or a stop. Do not expand a successful local comparison into a wider range claim without the corresponding basis.

### C.16.RM:4.6 - Return the usable result {#return-the-usable-result}

Give the corrected value or comparison, the conditions under which it applies and the consequence for the receiving work. Keep the reason for a changed interpretation where another user could otherwise continue using the old one.

Stop when the result is adequate for that use. Further investigation may have value for another question, such as broader operating conditions or the origin of the fault; it is a separate continuation whose gain should be clear.

## C.16.RM:7 - Conformance Checklist {#conformance-checklist}

- @fact:CC-C16-RM-1 **CC-C16.RM-1 - Comparable question.** The wanted quantity, actual indication, expectation and relevant conditions support the comparison being made. @status:spec/work
- @fact:CC-C16-RM-2 **CC-C16.RM-2 - Repair location.** The proposed change acts on a contribution capable of altering the unresolved answer. @status:spec/work
- @fact:CC-C16-RM-3 **CC-C16.RM-3 - Choice basis.** Available comparisons, domain relations or proportionate further inquiry support the selected repair. @status:spec/work
- @fact:CC-C16-RM-4 **CC-C16.RM-4 - Target continuity.** The revised arrangement retains the intended target or a stated relation to the accepted changed use. @status:spec/work
- @fact:CC-C16-RM-5 **CC-C16.RM-5 - Dependent results.** Changed models, computations, calibration and observations are carried through the affected interpretation. @status:spec/work
- @fact:CC-C16-RM-6 **CC-C16.RM-6 - Adequate test.** The comparison can expose the addressed defect and supports the range or result actually claimed. @status:spec/work
- @fact:CC-C16-RM-7 **CC-C16.RM-7 - Useful completion.** The returned result and remaining uncertainty answer the receiving question or state the consequential limitation. @status:spec/work

## C.16.RM:9 - Consequences {#consequences}

The practitioner can change the contribution responsible for an inadequate measurement and recover a usable result. Available observations may suffice; an equipment change can simplify the inference; a computational repair can restore results without a new physical experiment.

A targeted repair also limits what is established. A successful local result may leave the fault's cause, a wider operating regime or the uncertainty of a different quantity open. Those limits direct further work when its receiving question becomes current.

## C.16.RM:12 - Relations {#relations}

- **C.16** supplies measurement, model, work, result and uncertainty meanings.
- **C.16.MR** constructs or revises the measurement relation needed to interpret an indication.
- **C.16.IR** obtains compatible values and determines what the relation and readings resolve.
- **B.5.MPC.R** coordinates repair across the wider physical, mathematical and computational connection.
- **B.5.RR** carries a changed premise through affected reasoning.
- **C.29.2** constructs or repairs a needed computational formulation and its accuracy conditions.
- **C.28** supplies a causal account when identifying the cause is the required result.
- **C.11.DUA** compares further inquiry and its attainable contribution to the receiving use.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/C-16-MR#root, spec://ai.lev/fpf-spec/contract/C-16-IR#root, spec://ai.lev/fpf-spec/contract/B-5-MPC-R#root, spec://ai.lev/fpf-spec/contract/B-5-RR#root, spec://ai.lev/fpf-spec/contract/C-29-2#root, spec://ai.lev/fpf-spec/contract/C-28#root and spec://ai.lev/fpf-spec/contract/C-11-DUA#root. @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-16-RM

# B.5.MPC.R - Repair a Physical-Mathematical-Computational Connection {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative unless marked informative

## B.5.MPC.R:1 - Problem frame {#problem-frame}

Use this pattern when a physical question has an attempted answer, but the physical account, mathematical reasoning, computation or observed execution no longer fit together. A requested result may have changed, a command may produce an unexpected motion, or an observation may fail to distinguish the physical possibilities that the answer assumes.

**First useful move:** state the difference that now matters and compare the two contributions at the point where their meanings or results disagree. For a delayed robot stop, compare the duration used in the distance calculation with the duration for which the motor remained active.

The useful result is a repaired connection and its consequence for the physical question, or a located incompatibility that directs the next contribution. The method specializes B.5's reasoning revision for the joint work described by B.5.MPC. B.5.RR supplies the general treatment of affected reasoning, shared prerequisites and sufficient alternatives.

The practitioner needs the subject knowledge required to interpret the contributions, or access to that help. Use a known adequate correction directly when its conditions fit. Use B.5.MPC when the joint account has yet to be constructed. A fault already located within one discipline can proceed through that discipline's diagnostic or repair method.

## B.5.MPC.R:2 - Problem {#problem}

Local success can survive a failed joint answer. Algebra can produce a command beyond the device's range. A frequency calculation can correctly analyze samples while those samples are compatible with several physical frequencies. A voltage measurement can be accurate for the connected circuit while the question concerns the circuit before the meter was connected.

Trying harder within the successful contribution can leave the failure unchanged. More arithmetic precision does not make an unavailable command executable. More samples taken under the same ambiguous sampling relation may preserve the ambiguity.

The difficulty is to locate which connection fails and change the contribution that can repair it. Several accounts may explain the same discrepancy, so an observed disagreement must not be assigned to a particular component before the available reasoning distinguishes those possibilities.

## B.5.MPC.R:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Local correctness and joint usefulness | A valid result can answer a question different from the receiving physical question. |
| Stable relations and changed unknowns | The same physical relation can serve several questions, but each may require a different computation. |
| Observation and intervention | Obtaining an indication can change the state or conditions whose behavior is being inferred. |
| Economical repair and unresolved alternatives | A short correction can suffice; an ambiguous discrepancy may need a discriminating observation or a conditional result. |
| Useful abstraction and realizable operation | Mathematical possibilities can exceed the preparation, timing or range of the available apparatus. |

## B.5.MPC.R:4 - Solution {#solution}

Keep the receiving physical question in view while tracing the failed connection:

**State the changed result or disagreement → recover the contributing relations → locate the incompatible use → construct a sufficient repair → carry it through the affected contributions → use the revised physical consequence.**

These are dependencies of the repair. A known physical change, a failed calculation or a surprising observation can each be the starting point.

### B.5.MPC.R:4.1 - Compare results for the same physical question {#compare-results-for-the-same-physical-question}

Name the physical difference that the answer must resolve and the conditions under which it is wanted. Put the attempted result beside the changed request or observation. Recover the participants, units, times and operating regime needed to compare them.

For instance, a predicted displacement during eight seconds of motor operation and a measured displacement during eleven seconds concern different durations. Aligning the comparison may already explain the discrepancy.

If the question changed, say which quantities are now supplied and which must be determined. Keep the physical relation available while choosing its new use. A velocity-to-duration calculation can become a duration-to-command calculation.

If the comparison concerns a performance claim, recover the observation and its measurement relation. An acknowledgement can supply information about command reception while leaving physical completion unobserved.

### B.5.MPC.R:4.2 - Recover what each contribution supplies to the next {#recover-what-each-contribution-supplies-to-the-next}

Start at the mismatch and follow the needed relations in both directions. Ask what the receiving operation takes as input, what the supplied result actually represents and which condition permits that use.

The following questions distinguish common repair locations. Use the ones that can explain the disagreement.

| Connection to inspect | Question that can locate a repair |
| --- | --- |
| Physical account to mathematical formulation | Which interaction, boundary or operating assumption licenses this equation or constraint? |
| Mathematical formulation to computation | Does the procedure obtain the quantity or property now requested, with the required constraints and approximation? |
| Representation to another representation | Which distinction or operation must survive, and does the correspondence preserve it? |
| Computation to executing arrangement | Can the arrangement prepare the input, perform the operation and finish with the state or result being used? |
| Observation to physical inference | Which physical possibilities can produce this indication under this measurement procedure? |

Explain an unresolved connection in the working notation. Use B.5.RA to recover a needed argument and B.5.RC to recover a construction. C.29.1 compares mathematical transfers; C.29.2 constructs a computation; C.29.3 compares a computation with its realization. Their results answer the corresponding rows, while the physical question determines which row matters.

Keep a common premise visible across different contributions. An analytical calculation and a simulation that both assume no slip leave the same question open when slipping is suspected. A different algorithm is a sufficient alternative only if its premises and output interpretation fit the receiving use.

### B.5.MPC.R:4.3 - Locate the incompatibility without guessing its cause {#locate-the-incompatibility-without-guessing-its-cause}

Work a small instance or derive a consequence that distinguishes the competing accounts. If a command is outside the admitted range, its value and range already establish that incompatibility. If two physical inputs produce the same represented data but require different answers, exhibit those two inputs and their common representation.

When several explanations remain, compare what each would require you to change. A motion discrepancy might come from calibration, a retained command or an incorrectly interpreted position. Recover an available observation that distinguishes those accounts, or choose a worthwhile further observation through C.11.DUA. An investigation is unnecessary when a sufficient bound or conditional answer already settles the present decision.

Account for what the observation does. Identify which processes continue during measurement or debugging, which input remains applied and which state is changed by the probe. Use A.3.3 for the state and C.16 for the measurement relation when that construction is unresolved.

A mathematical account may support several physical interpretations. Compare their additional physical assumptions and the observations or interventions that distinguish them. Retain an unresolved difference when the available observations do not decide it; use the consequences shared by those interpretations when they suffice.

### B.5.MPC.R:4.4 - Construct the repair that the receiving use needs {#construct-the-repair-that-the-receiving-use-needs}

Choose the contribution that can remove the located incompatibility. The choice follows its cause and the wanted result.

- If the requested unknown changed, retain the interpreted relations, release the former fixed value where appropriate and derive the new computational direction.
- If a representation merged cases that the question must distinguish, retain the missing information, obtain a different observation or use a result that the merged representation still supports.
- If the procedure uses the wrong operation, constraint or approximation, replace that part and establish the property the receiving use needs.
- If the physical or measurement account omits a consequential interaction, model that interaction or change the arrangement so that the retained account applies.
- If execution differs in preparation, range, state or completion, revise that part of the realization or choose an available realization that supplies the required behavior.

An expression of an equation states a relation; an assignment or solver performs a chosen operation. Keep the equation's meanings when generating or editing that operation. A modelling environment can help transform the equation system, but the physical interpretation and the requested result still guide the choice.

Compare the repair with a sufficient alternative. Changing a deadline may be cheaper than replacing an actuator. A useful ambiguity result may suffice before changing measurement equipment. Present a changed requirement as a choice for the receiving work.

### B.5.MPC.R:4.5 - Carry the repair through its dependents {#carry-the-repair-through-its-dependents}

Use B.5.RR to derive the affected consequences. Reuse contributions whose conditions and meanings still fit; revise each needed use of a changed shared premise.

Compare the repaired contributions on the same input or physical case. For a mathematical change, derive the needed property. For numerical work, carry the error relevant to the physical question. For an execution claim, compare the prepared state, operation and interpreted observation with the intended result.

Keep the comparison at the claim's scope. A conditional calculation can establish what a proposed arrangement would do under its assumptions. Actual performance requires the observations and inference appropriate to that use.

If the comparison still fails, follow the remaining disagreement. Do not repeat a test that leaves the live alternatives indistinguishable. Change the question or obtain the missing contribution when the present means cannot settle it.

### B.5.MPC.R:4.6 - Return the physical consequence and the next useful action {#return-the-physical-consequence-and-the-next-useful-action}

State what can now be understood, constructed or changed. Return a usable command, corrected interpretation, realizability bound or a remaining ambiguity with its effect on the receiving decision.

When work is divided, give the next contributor the quantities and conditions at the unresolved connection, the result needed and how it will be used. The receiver must be able to reconnect the supplied contribution to the physical question. A.15.9 helps obtain that contribution.

The repaired reasoning may reveal another worthwhile problem: extending an operating regime, constructing a more informative measurement or developing an operation for a changed class of questions. Carry that possibility into B.5's next inquiry when pursuing it would enable further work.

## B.5.MPC.R:7 - Conformance Checklist {#conformance-checklist}

- The attempted and wanted results concern a stated physical question and comparable conditions.
- The contribution supplied at the disagreement has an interpretable meaning and receiving operation.
- The repair distinguishes a located incompatibility from an unresolved diagnosis.
- Shared premises remain visible across calculations, simulations and observations.
- The repair changes the responsible relation, procedure, realization or requested result.
- Its dependent consequences are reworked and returned at the supported scope.
- The receiver can perform the next action or identify the contribution still needed.

## B.5.MPC.R:9 - Consequences {#consequences}

The method makes a failed joint answer useful: the disagreement can reveal a range limit, a lost distinction, an omitted interaction or a missing construction. It also supports division of work by the contribution needed at the failed connection.

The cost is reconstruction across disciplinary boundaries. A sufficient conditional result or a known correction can keep that effort small. Where several causes remain compatible with the evidence, the result can remain a bounded diagnostic question.

## B.5.MPC.R:12 - Relations {#relations}

- **B.5.MPC** constructs the joint physical, mathematical and computational answer; this method repairs an attempted connection.
- **B.5.RR** revises affected reasoning. **B.5.RA** and **B.5.RC** recover an argument or construction needed for that revision.
- **C.29.1, C.29.2 and C.29.3** supply mathematical transfer, computational formulation and realization.
- **A.3.3** constructs the relevant state and continuation account. **C.16** constructs and qualifies the measurement relation.
- **A.6.3.RT** helps express the changed relation or operation. **A.15.9** helps obtain another practice's contribution.
- **C.11.DUA** compares further effort with its effect on the receiving decision. **B.3 and B.3.3** supply claim-specific assurance when required.


## Dependencies {#dependencies}

- @fact:SPECIALIZES Specializes: the revision work in spec://ai.lev/fpf-spec/contract/B-5#root and spec://ai.lev/fpf-spec/contract/B-5-MPC#root. @status:spec/done
- @fact:USES Uses: spec://ai.lev/fpf-spec/contract/B-5-RR#root, spec://ai.lev/fpf-spec/contract/C-29-1#root, spec://ai.lev/fpf-spec/contract/C-29-2#root, spec://ai.lev/fpf-spec/contract/C-29-3#root, spec://ai.lev/fpf-spec/contract/A-3-3#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT#root and spec://ai.lev/fpf-spec/contract/A-15-9#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-3-3-PI#root, spec://ai.lev/fpf-spec/contract/A-3-3-TR#root, spec://ai.lev/fpf-spec/contract/B-5-FM#root, spec://ai.lev/fpf-spec/contract/B-5-RR#root, spec://ai.lev/fpf-spec/contract/C-16-IR#root, spec://ai.lev/fpf-spec/contract/C-16-MR#root, spec://ai.lev/fpf-spec/contract/C-16-RM#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/B-5-MPC-R

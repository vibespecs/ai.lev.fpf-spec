# C.16.MR - Construct a Measurement Relation {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative

## C.16.MR:1 - Problem frame {#problem-frame}

Use this pattern when you have an indication or a proposed measurement procedure, but the relation between that indication and the property you want to determine is missing or unsuitable. A connected voltmeter can change the voltage. A test response can depend on both capability and the assistance offered. A counter can report the remainder after a wrap rather than the total number of events.

**First useful move.** Follow one indication back through the procedure that produces it. Name the sought property, the conditions under which it is sought, and one interaction or transformation that can make the indication differ from it. Express the relation supplied by that interaction. For an ideal source with open-circuit voltage E and series resistance Rs, a voltmeter of resistance Rm reads V=E*Rm/(Rs+Rm). This already shows why the indication alone need not determine E.

The Method constructs a measurement relation: how sought values, the measuring arrangement and relevant influences produce an indication, or how those contributions jointly constrain the sought value. The relation may use laws, an applicable calibration, an empirical response model or their combination. It can be used to plan a measurement or interpret an obtained indication.

The worked constructions concern quantities and event counts; they require elementary algebra and, in the assessment case, conditional probabilities. Subject Methods supply the physical laws, instrument response, assessment meaning or computational operations. C.16 supplies the Characteristic, Scale and performed-measurement account. This construction can return a conditional relation before any measurement is performed.

When a usable relation already supplies the needed answer under the current procedure and conditions, use it. If the relation is available but several sought values fit the indication, the next work is to determine what that indication can resolve. If an existing measurement disagrees with a prediction, compare possible changes to the models and arrangements.

## C.16.MR:2 - Problem {#problem}

An instrument display, test outcome or log value is produced by a procedure. Its meaning depends on that procedure and on the conditions in which the property is sought. Substituting the display for the sought value can therefore answer a different question.

A correction copied from another arrangement can also fail. Its sign, magnitude and uncertainty depend on the relation that produced it. Unknown influences can leave multiple compatible values even when the displayed number is stable.

The working difficulty is to construct enough of that relation to interpret the indication for the intended use, without modeling every possible influence or assuming that a familiar formula applies unchanged.

## C.16.MR:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Sought property and observed response | A procedure can transform or disturb what it observes. |
| Available relation and changed conditions | A calibration can save construction work while depending on its arrangement and range. |
| More detail and useful interpretation | Adding an influence costs information and computation; omitting a consequential one changes the answer. |
| Physical and statistical accounts | A deterministic response and a distribution of responses support different inversions. |
| Direct calculation and joint constraints | Some relations give the sought value directly; others require solving several relations together. |
| Planning and obtained measurement | A conditional model can guide an experiment before the data and conditions of an actual measurement exist. |

## C.16.MR:4 - Solution {#solution}

Fix the property and conditions of interest. Follow the production of the indication, combine the relations that connect it to the sought value, and retain the influences that can change its interpretation. Obtain a first conditional result or expose the missing relation.

### C.16.MR:4.1 - Fix what the measurement is meant to determine {#fix-what-the-measurement-is-meant-to-determine}

Specify the subject, Characteristic, Scale and conditions needed to distinguish the sought value. Include timing, location, population or averaging interval where they change the question. Use C.16:5.1-:5.2 for that specification.

Distinguish values that can differ across stages of the procedure. The open-circuit voltage before connecting a meter and the terminal voltage during measurement are different sought quantities. Either can be a legitimate target; choosing one determines the required relation.

Name the receiving question. Estimating a value, deciding whether it exceeds a limit and detecting a change can tolerate different remaining uncertainty. This choice helps decide which influences are consequential.

### C.16.MR:4.2 - Follow the production of the indication {#follow-the-production-of-the-indication}

Trace the procedure from the subject through the interactions, transformations and sampling that produce the indication. For each consequential stage, identify the relation supplied by the physical principle, known operation, applicable calibration or response model.

Start with relations already available for the actual or proposed arrangement. A supplied conversion can be enough. When it is missing, derive it from the subject account or identify the empirical relation that must be learned. B.5.RC helps recover a construction from an unfamiliar description; B.5.FM helps formulate the first model.

Retain an intermediate value when another relation uses it or when it exposes a consequential interaction. In the voltmeter example, current connects the source equation to the meter indication. Eliminate that current only after the relations use the same current and conditions.

For a statistical procedure, describe how response probabilities depend on the sought property and relevant conditions. The expected response and one realized sample are separate inputs to inference. Learning or transporting the response model requires the subject's estimation and applicability work.

### C.16.MR:4.3 - Include the influences needed by the question {#include-the-influences-needed-by-the-question}

Ask which features of the arrangement can change the interpretation at the intended range or decision boundary. Relevant candidates include loading the subject, offsets, limited resolution, sampling, timing, saturation and dependence on environmental or operating conditions. Follow the procedure to choose among them.

Describe a consequential effect where it enters the relation. An offset at an instrument's input can propagate differently from an offset added to its displayed output. A known correction follows from that relation; an uncertain effect retains its uncertainty. Several effects can be modeled together when their combined contribution is sufficient for the use.

Retain an unknown influential value as unknown. Available bounds or a justified probability model can support a useful conditional answer. Do not assign zero solely because the influence has not been measured.

Compare omission with inclusion at the needed result. A simple limiting case or a bound can show that an influence is negligible for this question. Keep the condition under which that conclusion holds, so a tighter requirement can reopen it.

### C.16.MR:4.4 - Compose the relation and obtain a first result {#compose-the-relation-and-obtain-a-first-result}

Combine relations only after their shared quantities, units, stages and conditions agree. Use substitution, a joint equation system, a conditional response calculation or another operation appropriate to the supplied model. C.29.2 helps construct the computation when obtaining the consequence is itself difficult.

A direct formula for the sought value is convenient but not required. Keep an implicit relation when solving it needs additional information or when several sought values remain compatible. A computational procedure can express the relation when its steps and interpretation are available.

Work one small case. Supply the known values, retain unknowns, derive a sought value or compatible set, and substitute back where that tests the construction. Inspect an informative limit: a meter with negligible loading, identical assessment response rates, or an interval too long for a wrapping counter.

Carry uncertainty that can change the conclusion. C.16:5.4 gives its interpretation requirements; the mathematical propagation Method depends on the relation. Algebraic solvability alone does not determine whether a near-threshold decision is resolved.

### C.16.MR:4.5 - Return the relation and its next useful use {#return-the-relation-and-its-next-useful-use}

Return the relation with the meanings of its inputs and sought value, the conditions that make it applicable, and the first result it supports. Preserve this information in the calculation, model or explanation being used; a new record is needed only when the receiving work requires one.

If the relation leaves a consequential ambiguity, name the indistinguishable values or the missing contribution. The next measurement should be selected for how it can resolve that distinction. C.11.DUA helps compare the value and cost of obtaining it.

When a discrepancy calls for repair, keep open the distinct possibilities of changing the subject model, the measurement model, the subject arrangement or the measuring arrangement. Additional mathematical detail is one option. Removing an unwanted interaction or restoring the specified procedure can be simpler.

Reopen the affected part when the target conditions, measuring procedure, calibration range or consequential influence changes. Use B.5.MPC.R when that change also affects connected physical, mathematical and computational work.

## C.16.MR:7 - Conformance Checklist {#conformance-checklist}

- @fact:CC-C16-MR-1 **CC-C16.MR-1 - Sought property.** Subject, Characteristic and target conditions identify what is to be determined. @status:spec/work
- @fact:CC-C16-MR-2 **CC-C16.MR-2 - Indication production.** The procedure's consequential interactions and transformations have relations with recoverable meanings. @status:spec/work
- @fact:CC-C16-MR-3 **CC-C16.MR-3 - Shared values.** Composed relations agree on units, stages and shared quantities. @status:spec/work
- @fact:CC-C16-MR-4 **CC-C16.MR-4 - Influences.** Consequential effects enter where they act; unknown effects retain their relevant uncertainty. @status:spec/work
- @fact:CC-C16-MR-5 **CC-C16.MR-5 - First result.** A case supplies a sought value, compatible set, conditional result or missing contribution. @status:spec/work
- @fact:CC-C16-MR-6 **CC-C16.MR-6 - Interpretation.** A statistical expectation, sample estimate and obtained measurement retain the qualifications needed by the use. @status:spec/work
- @fact:CC-C16-MR-7 **CC-C16.MR-7 - Useful return.** Further work addresses a distinction that can change the receiving result. @status:spec/work
- @fact:CC-C16-MR-8 **CC-C16.MR-8 - Changed conditions.** The construction identifies which relation must be reconsidered when the procedure, range or target changes. @status:spec/work

## C.16.MR:9 - Consequences {#consequences}

The reader obtains a relation usable for interpreting or planning a measurement. Intermediate interactions, response assumptions and unknown influences become parts of a calculation whose result can be inspected and revised. A missing contribution becomes a specific next task.

The cost is recovering the procedure and the subject relations it uses. A complete metrological or statistical investigation can be much larger than the first construction. The Method permits a useful conditional result or interval before that larger work.

## C.16.MR:12 - Relations {#relations}

- **C.16** identifies measurement, Characteristic, Scale, indication, model and obtained result.
- **B.5.RC** recovers a needed construction from its description; **B.5.FM** develops a first model.
- **A.3.3.CC** constructs compatible variables and constraints; **A.3.3.TR** constructs a rule for change where a dynamic measurement requires one.
- **A.3.3.PI** retains information for a future prediction; a measurement relation supplies its observation contribution.
- **C.29.2** constructs the computation needed to obtain a modeled result.
- **B.5.MPC.R** revises connected physical, mathematical and computational contributions.
- **C.11.DUA** decides whether reducing a remaining ambiguity is worth the work.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/A-3-3#root, spec://ai.lev/fpf-spec/contract/B-5-RC#root, spec://ai.lev/fpf-spec/contract/B-5-FM#root, spec://ai.lev/fpf-spec/contract/B-5-MPC-R#root, spec://ai.lev/fpf-spec/contract/C-29-2#root and spec://ai.lev/fpf-spec/contract/C-11-DUA#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-RI#root, spec://ai.lev/fpf-spec/contract/C-16-IR#root, spec://ai.lev/fpf-spec/contract/C-16-RM#root, spec://ai.lev/fpf-spec/contract/C-40-CU#root, spec://ai.lev/fpf-think-phy/contract/PHY-9#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-16-MR

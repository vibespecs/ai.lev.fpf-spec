# C.16.MR - Construct a Measurement Relation: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.16.MR:5 - Archetypal Grounding {#archetypal-grounding}

### C.16.MR:5.1 - Recover an open-circuit voltage from a loaded indication {#recover-an-open-circuit-voltage-from-a-loaded-indication}

The sought value is a source's open-circuit voltage E. The supplied ideal circuit represents the source by E in series with resistance Rs. Connecting a voltmeter of input resistance Rm completes the circuit. Assume positive resistances, a stable source and a meter whose indication equals its terminal voltage.

The common current I satisfies

    E = I*Rs + I*Rm
    V = I*Rm

Eliminating I gives

    V = E*Rm/(Rs+Rm)
    E = V*(1+Rs/Rm)

For Rs=Rm=1 megohm and V=5 volts, the inferred open-circuit voltage is 10 volts. Substitution returns I=5 microamperes and the original 5-volt indication. The two voltage drops explain both the sign and magnitude of the correction.

If the desired quantity were instead the connected terminal voltage, V would already be the value in this ideal model. The measurement question determines which result is needed.

As Rm becomes large relative to Rs, loading becomes small and V approaches E. For a use that needs only a bound on this effect, E-V=V*Rs/Rm supplies it. If Rs/Rm is at most 0.001 and V is 5 volts, the loading correction is at most 0.005 volts. Whether that is negligible depends on the receiving question and the other uncertainties.

If Rs is unknown, the same relation can expose an unresolved contribution. With V=5 volts, Rm=1 megohm and Rs between 0.8 and 1.2 megohms, E lies between 9 and 11 volts under the ideal assumptions. The interval may be enough. A performed measurement additionally accounts for indication and resistance uncertainty and relevant model inadequacy.

### C.16.MR:5.2 - Build the relation for an assessment of independent performance {#build-the-relation-for-an-assessment-of-independent-performance}

The sought quantity p is the fraction of a stated population able to perform a specified action independently under specified conditions. An applicable assessment account supplies s, the probability of a positive response when that capability is present, and f, the probability when it is absent.

Partition the population by the capability. The probability of a positive response is

    q = s*p + f*(1-p)
      = f + (s-f)*p

For s=0.9 and f=0.1, q=0.1+0.8*p. A sample positive fraction of 0.7 gives the estimate p=0.75 obtained by substituting the sample fraction. Its use also depends on sampling uncertainty, uncertainty in s and f and whether those rates apply to this population and procedure. The formula describes the expected response; the sample proportion estimates it.

If s=f, q is independent of p and the test does not distinguish the two conditions through this response. The failure is visible in the constructed relation. Further estimates of that same marginal positive rate cannot identify p through this relation.

Now change the procedure by offering hints. The earlier rates may cease to apply. Recover rates for the changed procedure or restore independent performance if that remains the target. The subject's capability and assessment Methods establish those conditions; the general construction shows where they enter the inference.

This population estimate does not identify which particular people or agents have the capability. That different question requires an individual assessment account.

### C.16.MR:5.3 - Interpret a wrapping event counter {#interpret-a-wrapping-event-counter}

A modeled counter increments once for each event and retains a value from 0 to 15, returning to 0 after 15. Readings immediately before and after an interval are r0 and r1. The sought quantity is the number N of intervening events. Assume no reset, no missed increment and readings taken at the stated interval boundaries.

The counter operation gives

    r1 = (r0+N) mod 16
    N = d + 16*k

Here d is the least nonnegative remainder of r1-r0 modulo 16, and k is a nonnegative integer. With r0=14 and r1=3, d=5: the compatible counts are 5,21,37 and so on.

If the interval is known to contain fewer than 16 events, N=5. Without that bound, subtracting the displayed numbers or returning the modular difference loses possible complete wraps. A wider counter, a recorded wrap count or shorter observation intervals can supply the missing information for a later measurement.

To infer elapsed time, another relation is needed: the counter must count timing ticks with an applicable tick-duration account. A counter of arbitrary work events alone measures no duration. This identifies a missing relation rather than inventing one from the numerical display.

## C.16.MR:6 - Bias-Annotation {#bias-annotation}

The examples have small, supplied subject models. Real instruments can require dynamic response, correlated influences or numerical inversion. Assessment rates can depend on population and conditions. A familiar model should therefore be reused with its applicable range and interpretation.

The construction can be shared across human, organizational and machine measurement practices. Its concrete laws and response models remain those of the subject. The general steps do not establish that a statistical assessment measures an individual's capability.

## C.16.MR:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Effect on use | Repair |
| --- | --- | --- |
| Read the display as the sought value after the procedure changes the subject | The answer can concern the measured arrangement instead of the target conditions. | Model the interaction and state which quantity is sought. |
| Copy a correction without its measurement relation | Its direction, magnitude or range can be wrong for the current arrangement. | Recover where the effect enters and derive its contribution. |
| Fill an unknown influence with zero | A numerical answer hides unresolved alternatives. | Keep the influence unknown and use available bounds or a justified distribution. |
| Treat expected response as an error-free observed proportion | The inferred population property loses sampling uncertainty. | Keep the response model and sampling inference distinct. |
| Repeat measurements to remove structural ambiguity | The same indication can still fit different sought values. | Change the relation or observation that distinguishes those values. |
| Model every conceivable influence before answering | The work expands without changing the result. | Test the consequence of the influence for the intended use and stop with an adequate result. |

## C.16.MR:10 - Architectural Rationale {#architectural-rationale}

The result is a relationship for interpreting an indication with respect to a specified property. A model of the subject can predict its behavior while leaving the measuring procedure undescribed. Connecting that procedure to the target property is an independently useful construction.

Construction, resolving ambiguity and repairing an inadequate arrangement cooperate but can start from different inputs and return different results. A measurement relation can be available before its data are obtained. It can also reveal that a particular indication leaves the target unresolved.

Physical interaction, mathematical expression and computational readout participate together. Their roles explain why revising a measuring instrument can require revising an equation or interpretation, and why a new display format alone may leave the underlying ambiguity unchanged.

## C.16.MR:11 - SoTA-Echoing {#sota-echoing}

The working question is to connect an indication to the property needed by the task. The selected construction follows the indication-producing procedure and includes its consequential interactions and transformations. A serious alternative is to reuse a supplied direct calibration or conversion. That alternative saves derivation when it already applies to the current arrangement and range. The present Method is needed when a changed interaction, procedure or target leaves that relation incomplete.

The voltmeter case exhibits the trade-off. Reading V directly is sufficient for the connected terminal voltage in the ideal model. Recovering the open-circuit value adds the source resistance and loading relation; it changes the answer from 5 to 10 volts in the worked case. At a sufficiently small resistance ratio, an available loading bound can justify the simpler use. More detail is valuable through that changed interpretation.

[GUM-6:2020, §§7, 9-10](https://www.bipm.org/documents/20126/2071204/JCGM_GUM_6_2020.pdf) develops measurement models from a principle, empirical information and effects of implementation. **Adapt:** :4.2-:4.4 combine those contributions, locate an influence where it acts, and retain unknown effects when no useful correction is available. The guide concerns quantity measurement; the assessment and counter constructions here use their separately stated response and operation models.

[Dounas-Frazer and Lewandowski (2018), §2](https://arxiv.org/pdf/1805.10334), distinguishes the investigated phenomenon, measuring equipment and their models. **Adapt:** :4.1-:4.2 recover the measurement contribution, while :4.5 preserves the separate model and arrangement repairs. The source studies experimental physics education; this cross-practice construction does not claim that its educational findings establish transfer to all agents or domains.

The common procedure and worked cases are a conceptual synthesis. Reopen the construction choice when a supplied calibration achieves the same interpretation with less work, or when a newly consequential interaction or response condition defeats the existing relation. Detailed uncertainty propagation, calibration design and model identification remain substantial specialized Methods.


## C.16.MR:End {#end}

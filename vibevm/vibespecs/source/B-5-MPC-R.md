# B.5.MPC.R - Repair a Physical-Mathematical-Computational Connection: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## B.5.MPC.R:5 - Archetypal Grounding {#archetypal-grounding}

These are constructed cases under stated models. They demonstrate different repair locations and the contributions that follow from them.

### B.5.MPC.R:5.1 - A robot receives a new deadline, then keeps moving during a pause {#a-robot-receives-a-new-deadline-then-keeps-moving-during-a-pause}

A robot must travel d=1 m along a straight guide. In the stipulated regime, constant speed obeys v=k*u, where u is a dimensionless command and k=0.2 m/s. The model initially idealizes starting and stopping as immediate. The available command range is 0<u<=0.8.

With u=0.5, the relation d=v*T gives T=d/(k*u)=10 s. The question then changes: find the command for T=5 s. Keep the relations but choose u as the unknown:

u=d/(k*T)=1/(0.2*5)=1.

The algebra supplies a value outside the available range. The corresponding lower bound on duration is T>=1/(0.2*0.8)=6.25 s. This answers the feasibility question before another controller is written. Changing the deadline or the available motion capability is now a meaningful choice.

Suppose the requester chooses T=8 s. The required command is u=0.625, giving v=0.125 m/s. A controller applies that command, counts eight seconds of active program execution and then issues stop.

During a diagnostic run, a debugger freezes the program and its timer for three seconds. In this example the output retains u=0.625 and the motor continues to run. The stop is therefore issued after eleven seconds of physical operation, giving d=0.125*11=1.375 m under the model.

The disagreement concerns execution timing. The equation and chosen command remain appropriate to eight seconds of motion. If the question concerns an uninterrupted run, observe that run under its intended timing. If such pauses can occur in the required operation, provide a stopping mechanism whose elapsed-time behavior survives the pause, or revise the control arrangement accordingly. Test its physical completion at the condition the use needs.

For example, suppose an independent timer can remove the motor command and continues to run while the controller is paused. Start it with the command and set it to remove the command after eight physical seconds. Under the example's immediate-start/stop model, motion then lasts eight seconds and covers 0.125*8=1 m, including a run with the three-second program pause. Compare the timer's actual behavior with those conditions before relying on that performance. If no such mechanism is available, the next contribution is a way to stop motion with that timing or a revised operating requirement.

A real stopping delay or speed transient would be another changed premise. Incorporate it when predicting final displacement; acknowledging stop does not measure that displacement. The example's next useful result is a duration bound or a repaired timing design with an identified performance question.

### B.5.MPC.R:5.2 - A correct spectrum calculation answers an ambiguous physical question {#a-correct-spectrum-calculation-answers-an-ambiguous-physical}

A measurement uses uniformly spaced samples at f_s=100 samples/s. The earlier physical account admits a single sinusoidal signal with frequency below 50 Hz. A spectrum calculation returns a 10 Hz component, interpreted under that restriction.

The apparatus is changed and the admitted frequency range becomes 0 to 120 Hz. The same interpretation is now in question. For ideal samples of a unit-amplitude cosine at times n/100 seconds:

cos(2π*90*n/100)=cos(2π*10*n/100)

for every integer n. This follows because 90/100=1−10/100 and cosine is periodic and even. A 110 Hz cosine gives the same samples as well.

Consequently, the sampled sequence fits physical frequencies 10, 90 and 110 Hz in the new range. The spectrum calculation can remain correct for its input. Increasing its arithmetic precision or merely collecting more samples at the same times leaves this ambiguity.

To determine which frequency is present, change a contribution that distinguishes those cases. For the stipulated single-tone model, sampling at 300 samples/s places the whole admitted range below half the sampling rate. A three-second record of a 90 Hz signal then contains 270 cycles; the spectrum can return 90 Hz under the stated ideal timing and signal assumptions.

For a physical measurement, obtain the needed sampling and input-conditioning behavior from the instrument account. Frequencies outside the admitted band, timing error and an unsuitable analog input path can reopen the interpretation. A filter that removes the signal of interest changes the measurement question rather than recovering its frequency.

The repair is a changed acquisition and interpretation, with a recomputation on the new data. The receiving user can now distinguish a physical-frequency estimate from an unresolved alias. If the old record is all that is available, return the remaining alternatives instead of selecting one without further grounds.

### B.5.MPC.R:5.3 - The voltmeter changes the circuit being inferred {#the-voltmeter-changes-the-circuit-being-inferred}

An ideal 10 V source drives two 1 MΩ resistors in series. The wanted quantity is the midpoint voltage before a meter is connected. The divider relation gives 5 V.

A voltmeter with 1 MΩ input resistance is connected between the midpoint and the lower terminal. In the connected circuit it lies in parallel with the lower resistor, whose combined resistance becomes 0.5 MΩ. The same divider construction now gives:

V_mid=10*0.5/(1+0.5)=10/3 V.

The indicated value can agree with the connected-circuit model. Comparing it directly with the unloaded prediction had omitted the meter's interaction.

One repair is inferential: with these resistor, source and meter models, recover the unloaded value from the model, keeping its conditional status. Another is experimental: choose a measurement arrangement whose loading is small enough for the wanted use and account for its remaining effect. Repeating the same connection alone preserves the load.

The result tells the practitioner which voltage was observed and how the wanted voltage can be obtained. A different observed value may require revisiting the assumed source, resistor or instrument behavior through their subject methods.

### B.5.MPC.R:5.4 - A motion command changes its unit and starting point {#a-motion-command-changes-its-unit-and-starting-point}

In C.29.3's robot case, the effective wheel radius is 0.05 m, ten motor revolutions turn the wheel once, and the interface counts 1,000 increments per motor revolution. A two-metre displacement requires a total of 63,662 motor increments after rounding. C.29.3 handles sending that total through the available command field.

Now change the radius to 0.06 m and the interface to an absolute wheel-position target. It counts 1,000 units per wheel revolution, currently reads 3,000 and admits targets from 0 to 65,535. The requested forward displacement remains 2 m. Assume rolling without slip and completion at the commanded count.

Recover the count's new meaning before reusing the calculation. If q is the target, the wheel travels (q−3,000)/1,000 revolutions, so the model gives:

d=(q−3,000)/1,000 * 2π * 0.06 m.

The new scale already counts wheel revolutions; use that scale to obtain the needed increment:

Δq=2/(2π*0.06) * 1,000 ≈ 5,305.16477.

Round to 5,305 and add the initial count, giving target q=8,305. This target is admitted. Its modeled displacement is approximately 1.99993788 m. Nearest-integer rounding contributes at most half a count, corresponding to π*0.06/1,000 m ≈ 0.00018850 m; compare that contribution with the receiving accuracy requirement.

Reusing the former total 63,662 as the absolute target would pass the new range check but give approximately 22.8690 m under this model. The value has changed from a relative motor increment to an absolute wheel position. The repair therefore changes the physical parameter, the count-to-motion correspondence and the computational use of initial state together.

The useful return is the new command with its displacement and rounding consequence. A changed starting count requires recomputing the target; a changed radius or count scale reopens their correspondence. A slip or incomplete motion requires the relevant physical or execution repair. C.29.3's preparation and completion comparison can then use this revised command.

## B.5.MPC.R:6 - Bias-Annotation {#bias-annotation}

The cases use elementary models so the connection can be worked explicitly. Nonlinear dynamics, statistical observations or coupled physical computations can require more demanding subject contributions. Preserve their interaction and uncertainty conditions when applying the same repair method.

A visible software failure can attract attention even when the computation is correct and its physical interpretation is wrong. Compare the meaning of the input and output before choosing a programming repair.

## B.5.MPC.R:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Consequence | Repair |
| --- | --- | --- |
| Solve for the former unknown | A correct formula answers the old question. | Retain the relation and select the givens and unknowns again. |
| Refine the computation of ambiguous data | The physical alternatives remain indistinguishable. | Change acquisition or return the supported ambiguity. |
| Treat debugger time as physical time | A retained actuator command can continue to act during the pause. | Recover the actual timer and actuator behavior. |
| Treat a probe as passive despite its coupling | The observed system differs from the modelled unobserved arrangement. | Include the probe interaction or change the measurement. |
| Switch algorithms while retaining the disputed physical premise | The alternative preserves the same failure. | Compare its complete application conditions. |

## B.5.MPC.R:10 - Architectural Rationale {#architectural-rationale}

The common revision method B.5.RR follows affected reasoning. This specialization adds the recurring correspondences that a physical application consumes: a physical account expressed mathematically, an interpreted computation and a realized or measured operation. It lets the practitioner choose the repair that can change the physical answer.

Working from the disagreement can settle the question with a bound or identify the observation that must change.

The physical and mathematical accounts need each other without becoming the same account. A mathematical equality can expose why two frequencies have identical samples. The physical sampling arrangement determines whether those are the relevant possible inputs. Computational analysis then operates on the resulting data. The useful knowledge comes from keeping those relations together; applying it can change the measurement method itself.

## B.5.MPC.R:11 - SoTA-Echoing {#sota-echoing}

**How can an expression help locate a failed connection?** Adapt Sussman and Wisdom's [*Structure and Interpretation of Classical Mechanics*, second-edition preface (2015)](https://mitp-content-server.mit.edu/books/content/sectbyfn/books_pres_0/9579/sicm_edition_2.zip/preface001.html): expressing mathematics as executable procedures exposes operations that informal notation can leave implicit. Sections 4.2 and 4.4 use that feedback where available. Compared with polishing a symbolic answer alone, it can locate an unusable operation; its extra formalization is worthwhile only for the receiving question.

**What survives a changed computational direction?** Adapt the separation of equation models and generated computations in [ModelingToolkit's version-10 documentation](https://docs.sciml.ai/ModelingToolkit/v10.4/), alongside Ma et al.'s [2021 account](https://arxiv.org/abs/2103.05244). Section 4.4 retains relations while changing givens, unknowns or the obtaining procedure. This supports acausal modelling rather than making one assignment direction part of a physical law. An adequate explicit formula remains cheaper for the robot's small calculation; no modelling platform is required.

**When must observation be treated as an operation?** Adapt Khrennikov's [Contextual Measurement Model (2024), §§2.1–2.2](https://doi.org/10.1098/rsos.231953): the measurement procedure can change the context used by subsequent inferences. Section 4.3 therefore recovers that operation when it matters. The passive-observation account remains useful where its approximation is adequate. The voltmeter case supplies an elementary circuit construction of an interacting probe; broader physical interpretations need their own assumptions and observable consequences.

**Which sampling repair changes the physical inference?** Use NI's [sampling and aliasing account, “Sample Rate” and “Aliasing”](https://www.ni.com/en/shop/data-acquisition/measurement-fundamentals/analog-fundamentals/acquiring-an-analog-signal--bandwidth--nyquist-sampling-theorem-.html) for the acquisition constraint and input conditioning. Section 5.2 derives its alias equality explicitly and states f_s and the admitted signal band. Compared with increasing numerical precision, changing acquisition can distinguish the physical cases. The instrument's bandwidth, filtering and timing remain part of that repair.

Reopen the source choices when a physical theory, representation, computational method or executing technology supplies a better way to resolve the same disagreement. Compare the actual operation, consequence and conditions that let the receiving work use it.


## B.5.MPC.R:End {#end}

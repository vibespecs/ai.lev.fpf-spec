# B.5.FM - Construct a First Model for the Working Question: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## B.5.FM:5 - Archetypal Grounding {#archetypal-grounding}

These constructed cases expose different model choices. Their calculations establish conditional consequences; no apparatus test is reported.

### B.5.FM:5.1 - Choose the heat path before commissioning a calculation {#choose-the-heat-path-before-commissioning-a-calculation}

An engineer asks whether a stronger external fan can bring an overheating component below 65 °C. Inspection finds the component attached to a metal case through a pad; the fan blows over the outside of the case.

Trace the proposed path from component to case and then to the surrounding air. Keep the component, the case at its attachment and the air distinguishable: their temperatures can differ, and the fan acts on one part of that path.

Try a steady account with constant component heating, all generated heat passing through the pad, and an unchanged linear conductance between component and case. Carrying the same heat per second then requires the same temperature difference across that path. Treat outward case-to-air transfer as driven by temperature difference. A steady case receiving positive heat must remain warmer than the air.

Use supplied steady readings of 80 °C at the component, 25 °C at the case attachment and 20 °C in the air. The component-to-case difference is 55 °C. Even ideal external cooling of the case to the air temperature leaves the component at 75 °C under these assumptions. The fan-only proposal cannot reach 65 °C in this model.

The result directs work toward the component-to-case contact, another heat path or reduced heating. Direct airflow onto the component would change the assumed path; temperature-dependent heating or conductance would change the fixed-difference argument. Measurement uncertainty matters to the real-device conclusion.

A useful next request is: “Can this component stay below 65 °C after changing its contact to the case, and which observations distinguish the relevant heat paths?” The model supplies that request before a detailed equation set is commissioned.

### B.5.FM:5.2 - Include the air when modeling liquid discharge {#include-the-air-when-modeling-liquid-discharge}

Consider a rigid vessel with a liquid outlet near its bottom and trapped air above the liquid. The question is whether enlarging the outlet will allow most of the liquid to drain. A model based only on liquid height can miss what changes when liquid leaves.

For a first conditional account, assume that no air enters and the liquid is incompressible. Treat the trapped air as an ideal gas at constant temperature and fixed amount. Consider slow flow whose inertia is negligible and whose motion is dissipated by resistance at the outlet. Include the gas volume and absolute pressure, the liquid height above the outlet and the outside pressure. Liquid leaving increases gas volume and lowers gas pressure.

At the no-flow equilibrium, the internal pressure at the outlet equals the outside pressure. For the following rough calculation take liquid density as 1,000 kg/m³ and gravitational acceleration as 10 m/s². Initial liquid height is 20 cm, trapped gas volume is 100 cm³, vessel cross-section is 100 cm² and initial gas and outside pressures are both 100 kPa.

Let q be the discharged volume in cm³. The gas occupies 100+q cm³; liquid height is 20−q/100 cm. The isothermal gas relation and hydrostatic head give the equilibrium equation:

```text
10000/(100+q) + 0.1*(20−q/100) = 100   [kPa]
```

The positive solution is about 2.039 cm³, with gas pressure about 98.002 kPa and liquid height about 19.980 cm. In this slow-flow account, the discharge approaches a stop after a very small volume. Changing outlet size changes resistance and the approach to equilibrium; this same equilibrium balance applies while air entry and inertial effects remain negligible.

Allowing ambient air to reach the gas space changes the model: gas pressure can remain near outside pressure as liquid leaves. Air entering through the outlet, gas-temperature change, vessel deformation or appreciable capillary pressure requires another account. The immediate useful result is the distinction between an outlet-flow restriction and a gas-replacement restriction. Investigate the air path before treating outlet enlargement as the answer.

### B.5.FM:5.3 - Construct classes that permit a counting inference {#construct-classes-that-permit-a-counting-inference}

We need counts of binary strings at several lengths under a rule that forbids consecutive 1s. Use length four as a small case. The question supplies symbols and a restriction, but no recurrence.

Start with short valid prefixes and examine their allowed next symbols. A prefix ending in 1 may receive only 0. A prefix ending in 0 may receive either symbol; the empty prefix has the same two permissions. Group prefixes by those extension permissions.

Let r_n count valid length-n prefixes that are empty or end in 0; let b_n count those ending in 1. Every valid prefix can receive 0, while only the r_n prefixes can receive 1:

```text
r_0 = 1, b_0 = 0
r_(n+1) = r_n + b_n
b_(n+1) = r_n
```

The pairs for lengths 1 through 4 are (1,1), (2,1), (3,2), (5,3). There are eight valid strings of length four.

The inference works because each extension produces a distinct string, deleting its final symbol recovers its unique predecessor, and the two resulting classes exhaust the permitted cases. The total alone does not tell how many prefixes permit appending 1; keeping the two classes makes that operation possible.

If the restriction changes to “no three consecutive 1s”, the same grouping loses a needed distinction. Separate prefixes with zero, one or two trailing 1s and reconstruct the permitted transitions. This change identifies what the state must retain; the subsequent recurrence or program is a further computational contribution.

### B.5.FM:5.4 - Find the limiting relation in a workshop plan {#find-the-limiting-relation-in-a-workshop-plan}

Twelve people have accepted a 60-minute workshop. There are twelve seats and one instructor. The proposed arrangement gives each person a four-minute attempt observed by that instructor, then two minutes of the instructor's feedback before the next attempt begins. The initial plan lists attendance and materials.

Use the relation between attempted action, observation and feedback to ask whether the intended practice can occur in the session. The sequential arrangement requires `12 * (4 + 2) = 72` minutes before any introduction. The next question is which arrangement can supply the intended practice and feedback within the available time. Reducing attendance, increasing duration or changing the learning arrangement have different consequences. Merely pairing learners supplies the required feedback only if they can provide that contribution.

Now suppose twelve independent stations already provide the required task-specific feedback and can be used concurrently. The serial calculation no longer describes the work. Use the concurrent duration and the remaining session activities to decide whether the arrangement fits; this reasoning does not require another instructor. If the intended event is instead a demonstration with no individual practice, the individual-feedback relation does not impose that practice on it. Clarify the event's purpose before treating this scheme as applicable.

The same question-forming move can use a measurement scheme: a shared column label, such as temperature, leaves the relevant quantity, observing conditions and aggregation to be recovered before combining records. If the existing documentation already establishes their suitability, use that answer. The scheme supplies a question, not a compulsory new measurement.

## B.5.FM:6 - Bias-Annotation {#bias-annotation}

The examples use small explicit accounts so that the reader can inspect the construction. Complex systems can require learned representations, instruments and multiple specialist contributions. Their suitability depends on the inference and available means.

Source studies of human scientific work motivate some construction moves. Their transfer to AI agents concerns the work to perform and the result to supply; it does not assert identical cognitive mechanisms or learning requirements.

## B.5.FM:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Recognizable failure | Repair |
| --- | --- |
| Fit a model whose variables cannot express the proposed intervention. | Recover the participants and relations through which the intervention could change the result. |
| Copy a familiar analogy while its operation has a different meaning in the present case. | Construct the needed correspondence and test the transferred consequence. |
| Aggregate cases before performing an operation whose permissions differ between them. | Keep the permission-changing distinction until that operation is complete. |
| Increase simulation detail while an omitted interaction determines the answer. | Obtain a limiting or contrasting case that exposes that interaction. |
| Give a specialist a broad modeling request that leaves the needed result unclear. | Supply the provisional account and ask for the contribution that would change the next decision. |

## B.5.FM:10 - Architectural Rationale {#architectural-rationale}

Model construction and model use often develop together. Trying an operation reveals which distinctions are missing, while the revised distinctions permit another inference. The method therefore keeps selection, relation construction, expression and consequence in one connected reasoning move.

The heat case depends on separating temperatures and locating an intervention along a path. The vessel case requires coupling two interacting media. The counting case creates classes from permitted operations. Their shared method is the construction of an inferentially useful account; their subject premises remain different.

B.5 coordinates the overall inquiry. This method develops its model-building contribution. B.5.4 gives a narrower entry when an available concept needs a situational interpretation. C.29 supplies mathematical representation choice. A.3.3, C.16 and A.6.3.RT supply state, measurement and expression construction when those questions occur within model building.

## B.5.FM:11 - SoTA-Echoing {#sota-echoing}

**Construction as a reasoning contribution.** Adapt Nersessian's [2025 account, §3](https://onlinelibrary.wiley.com/doi/10.1111/tops.12777): a useful analogy may have to be built, with its correspondence revised during use. The present method applies that contribution in :4.2–:4.4: select distinctions through a needed consequence, build compatible relations and use a small case to revise the correspondence. Reusing a calibrated domain model is cheaper when it already expresses the proposed change. Constructing another account becomes worthwhile when the available model cannot express a consequential interaction or operation; the vessel and prefix cases show those failures.

**Qualitative consequences and application.** The [ISLE explanation by Etkina and Brookes](https://www.islephysics.net/why-isle.html) connects observation, proposed explanation, predicted consequence, testing and application, first qualitatively and then quantitatively. Use that progression in :4.4–:4.6 when a physical prediction needs examination and application. A formal construction can instead proceed from its formation rules and a derivation, as in :5.3.

**Finding a question through a scheme.** Compare two practical starting points: follow a provisional question into a small model (:4.1–:4.5), or use an understood scheme to expose a question (:4.2.1). Give both routes the same workshop facts, knowledge of the attempt/feedback relation and a hand calculation. The first can begin with “Can this plan provide the intended practice?”, select the instructor's time, derive 72 minutes and revise the arrangement. With independent stations it changes the model and withdraws the serial restriction. Both routes can obtain these results.

Use the scheme-based entry when an apparently adequate account, such as a seating plan, leaves the relevant question unclear. Its applicability table distinguishes an unknown relation from one that is inapplicable, inexpressible or in conflict with the case. In :5.4 the demonstration-only variant drops the individual-practice question instead of treating it as a missing provision. Recovering and trying a scheme has a cost: use the direct construction when the distinction and question are already clear. This comparison supports a choice between instructions under the stated conditions; it establishes neither faster learning nor better field performance.

Gentner and Hoyos, [Analogy and Abstraction](https://doi.org/10.1111/tops.12278), 2017, §§1.2–2, provide a historical structural-alignment account. Adapt relational rather than name matching in :4.2.1; the reviewed transfer effects depend on their task and comparison conditions. Keet and Khan, [Discerning and Characterising Types of Competency Questions for Ontologies](https://arxiv.org/html/2412.13688v1), 2024, §§3–4, contribute purpose-sensitive questions and limits of a scheme's expressiveness. Adapt those distinctions in the applicability table without imposing their ontology-specific taxonomy. Vagnino and Walker, [Schema drift](https://doi.org/10.1016/j.cognition.2025.106418), 2026, supplies a limitation: repeated comparison can change relational judgments, with rival explanations unresolved. This motivates the explicit return to a changed relation; it does not establish this repair's efficacy.

Reconsider the scheme-based entry when it repeatedly produces irrelevant questions or when the direct construction already supplies the needed distinction. Repair the correspondence or continue from the adequate question before broadening the inquiry.

**Subject premises of the physical cases.** [OpenStax, University Physics 2, §1.6](https://openstax.org/books/university-physics-volume-2/pages/1-6-mechanisms-of-heat-transfer) supplies the conducting-layer and convection relations. [Volume 2, §2.1](https://openstax.org/books/university-physics-volume-2/pages/2-1-molecular-model-of-an-ideal-gas) supplies the isothermal fixed-amount gas relation; [Volume 1, §14.1](https://openstax.org/books/university-physics-volume-1/pages/14-1-fluids-density-and-pressure) supplies the hydrostatic pressure relation. The chosen arrangements, simplifications and receiving questions are the present constructions.

Reopen the method when another construction approach supplies a more useful model at comparable effort, or when a recurring difficulty calls for a model-building move absent from this account.


## B.5.FM:End {#end}

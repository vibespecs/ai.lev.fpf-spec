# C.28.CM - Construct and Challenge a Causal Model: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.28.CM:5 - Archetypal Grounding {#archetypal-grounding}

The following constructed cases demonstrate reasoning under stated premises. They do not report field effects.

### C.28.CM:5.1 - Separate an omission, its record and the incident sample {#separate-an-omission-its-record-and-the-incident-sample}

Four incident tickets mention missing order identifiers after a reporting-template change. A planner asks whether supplying the identifier before import would remove manual matching. All four tickets came from problematic reports; the frequency among all reports is unknown.

Choose M for an actually missing identifier and Y for manual matching after import. X denotes template use and L high process load. One account proposes X → M → Y, with load affecting template deployment and identifier omission. A second account proposes that load produces both missing identifiers and an additional wrong join key K; K causes matching work even after the identifier is supplied. The second account has L → M and L → K → Y without an M → Y mechanism.

These accounts make different conditional predictions. If missing identifiers are the operative joining failure and supplying one changes no other input, supplying it removes that modeled obstacle. If K remains wrong, the same correction leaves the K-related work. A report with its identifier restored but the same failed join can challenge the first account's claim of sufficiency. It does not establish the second account merely by eliminating one rival.

Now recover the observing process. Let R be a log saying the identifier is missing. A logging defect can make R=1 while M=0. Inspecting the submitted report and the importer’s actual inputs can therefore resolve a recording question before further causal research is useful.

Let S=1 mean a report entered the incident sample, either because R=1 or because matching work was severe. The structure R → S ← Y means that analyzing only S=1 conditions on a collider. The four tickets cannot by themselves establish the population association or the effect of correcting identifiers. Obtain the needed comparison cases if they could change the decision; retaining a qualified unresolved answer is also possible.

The first return is specific: determine which joining inputs were actually missing or wrong, then distinguish the two modeled failure mechanisms. If all retained accounts support a cheap temporary manual check under the decision's own conditions, using it does not establish which account caused the incident.

**Onset, persistence and amplification.** Suppose a queue began during a specialist's absence. After their return, ten new items and capacity for ten items arrive each day. Under the simplified balance B(t+1)=max(0, B(t)+A(t)+R(t)−C(t)), with backlog B(0)=12, A=10, R=0 and C=10, the backlog remains 12. Two daily rework items, R=2, increase it by two per day. The absence explains the initial loss of service; the present flow balance explains persistence; rework explains growth under these premises. Restoring attendance alone need not clear the backlog. A different arrival pattern, capacity or feedback from delay to rework reopens the corresponding part of the model.

### C.28.CM:5.2 - Construct the measurement and device mechanisms separately {#construct-the-measurement-and-device-mechanisms-separately}

An idealized regulated supply has command C=12 volts and a fixed 6-ohm resistive load. Its display reads D=14 volts. The practical question is whether correcting the display can reduce the load current.

Construct separate variables for delivered voltage V, display D and current I. Use the load relation I=V/6. Two accounts fit the displayed value:

| Account | Proposed mechanisms | Current implied by the account |
| --- | --- | --- |
| Display bias | V=C; D=V+2. | V=12 and I=2 amperes. |
| Supply offset | V=C+2; D=V. | V=14 and I=7/3 amperes. |

Setting the displayed number to 12 replaces the display mechanism in either model. It leaves V and I unchanged. Changing C to 6 instead gives V=6, I=1 in the first model and V=8, I=4/3 in the second, if the stated offsets and load relation remain valid. The observation D=14 alone does not choose between the accounts.

A separately qualified voltage or current observation can discriminate these idealized models. The need is a measurement of the physical quantity with a suitable independent basis, not another copy of the same display.

Change the situation: the displayed value is fed into an automatic controller for the next command. The earlier absence of a display-to-device path no longer applies over that horizon. Add D(t) → C(t+1) → V(t+1) and obtain the controller law before predicting the later current. The current instant and later controlled behavior are different questions. C.28.MR then performs the chosen replacement in the model actually constructed.

### C.28.CM:5.3 - Separate AI assistance from assignment and selection {#separate-ai-assistance-from-assignment-and-selection}

A team reports that AI-assisted tasks had a higher success rate. The question is the effect of actually using assistance A on success Y for the same eligible task population. Let D denote pre-existing task difficulty and H the worker's prior skill.

One model contains A → Y, D → A, D → Y, H → A and H → Y. The rival keeps the assignment and difficulty/skill relations but omits A → Y: the observed difference could arise through who used assistance and on which tasks. Success rates alone do not settle that difference.

The models permit different intervention consequences even when they fit the same aggregate report. Under the explicit assumption that D and H suffice to block common-cause paths, with comparable treatment versions and adequate overlap, adjustment might identify the chosen effect. Those conditions are additional premises, not results of drawing D and H. If workers choose assistance using an unmeasured expectation of difficulty, preserve that possible influence and return the identification gap.

Suppose inclusion in the showcase S depends on both use of assistance and success. A → S ← Y adds a selection path; conditioning on showcased tasks opens it. Reconstruct the eligible set and inclusion process before using the selected comparison for the population question.

Now randomize an offer Z while leaving actual use A voluntary. The offer's effect is a different estimand from the effect of A. If the offer also teaches a technique used without the AI, Z has a route to Y outside A. Using the offer as an instrument to learn the effect of actual use would require it to affect success only through use, among other assumptions. The additional route violates that requirement. The model returns the exact identification question and keeps observed performance descriptive until the required result is available.

The useful return can be a revised comparison population, a retained unmeasured cause, or a direct-effect route that invalidates a proposed design. A larger benchmark or more detailed simulation does not resolve those missing premises by itself.

## C.28.CM:6 - Bias-Annotation {#bias-annotation}

The scope is construction for a bounded causal question. Epistemic discipline separates a mechanism proposal from its evidence; pragmatic discipline stops at a useful conditional result; ontological discipline separates variables, their values, observations and the subject being changed.

Narrative closure favors the first fluent explanation. Diagram authority favors a tidy graph. Observed-variable bias omits causes that were not measured. Remedy these tendencies by constructing a material rival, explaining consequential omissions, and checking how observations and case selection were produced. Retaining every imaginable model can also prevent useful work; narrow the family by subject grounds and the receiving question.

## C.28.CM:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Misuse | Repair |
| --- | --- |
| “We drew the intermediate cause, so the mechanism is established.” | Recover what supports the intermediate relation and what the rival predicts. |
| “The common cause explains everything, so there is no direct effect.” | Inspect the proposed direct path separately; both mechanisms may operate. |
| “This variable is always a confounder.” | Name the question and path before deciding its role or adjustment use. |
| “All reports in our incident set show the effect.” | Recover registration and selection, then the comparison needed for the target cases. |
| “The graph fits, so it is the true graph.” | Name the implication actually tested and retain indistinguishable alternatives. |
| “Remove the original cause and the ongoing problem ends.” | Reconstruct the present persistence mechanism and horizon. |
| “A better model must precede any response.” | Compare the value of further discrimination with an independently justified available response. |

## C.28.CM:10 - Rationale {#rationale}

Constructing a causal account and judging its support answer different questions. A coherent hypothetical model can expose a decisive experiment or invalidate an inference without establishing that the model describes the subject. Preserving both the constructive and evidential questions makes that intermediate result usable.

A model family preserves a live disagreement when the available grounds do not select one account. Explicit measurement and selection processes prevent uncertainty about observing from disappearing into a confident story about the subject. Time distinctions make the same discipline usable when an initiating event and an ongoing mechanism differ.

## C.28.CM:11 - SoTA-Echoing {#sota-echoing}

The comparison concerns usable construction and criticism for a bounded causal question. It does not rank causal-discovery algorithms or claim a universally best empirical workflow.

| Practice question and selected move | Alternative, trade-off and concrete use | Source role, limits and reopening |
| --- | --- | --- |
| How can a working account become explicit causal assumptions? **Adapt** extraction, translation and critical integration of subject claims. | Directly drawing the preferred story is cheaper but can hide missing or conflicting premises. :4.2–4.3 recover meanings and alternatives; a full evidence synthesis is reserved for questions that need it. | [Ferguson et al., 2020, Table 1 and Discussion](https://pdfs.semanticscholar.org/cb52/45fd90f7942f734911ebd1492c3d3e5a4e24.pdf) supplies a developed construction comparator. Its integration heuristics do not establish causal truth. Reopen when this extraction loses a subject mechanism or a simpler adequate construction is available. |
| Which conditioning changes the causal question or opens a misleading path? **Adopt** whole-graph path inspection; **reject** deciding from a variable's name or one three-node picture. | Classifying a few familiar motifs is quicker but can miss another open path or conditioning through selection. :4.4 works the entire small graph and :5.3 preserves assignment and selection. | [Geiger, Verma and Pearl, 1990](https://ftp.cs.ucla.edu/pub/stat_ser/r116.pdf) gives the formal separation basis; [Cinelli, Forney and Pearl, 2022](https://ftp.cs.ucla.edu/pub/stat_ser/r493-reprint.pdf) supplies the current practice comparison for controls. These are conditional graphical results, not tests of omitted subject premises. Change the rule when the graph class or estimand changes. |
| What if the graph itself is uncertain? **Adapt** comparison of the causal query over admissible structures. | Selecting one convenient graph simplifies calculation but can suppress a result-changing rival. :4.5 retains the remaining family and states its shared or differing consequences. | [Padh et al., 2025, §§2 and 6](https://arxiv.org/html/2502.17030v2) supplies a computational line with explicit structural uncertainty; its procedure assumes no hidden confounding and has optimization limitations. [Peters et al., 2014](https://jmlr.org/papers/volume15/peters14a/peters14a.pdf) shows how additional model assumptions can identify structure. Neither licenses assumption-free discovery. Reopen when a qualified result excludes a live rival or reveals another. |
| How should feedback affect construction? **Adopt** temporal distinction where it answers the query; otherwise request a suitable cyclic model. | Forcing an equilibrium loop into a DAG can delete the operative mechanism. :4.4 and :5.2 retain the horizon and the controller dependency. | [Bongers et al., 2021](https://staff.fnwi.uva.nl/j.m.mooij/articles/21-AOS2064.pdf) supplies existence and interpretation conditions for cyclic structural models. Its theory makes a cyclic alternative available under conditions, not automatically solvable. Reopen when the chosen temporal resolution or equilibrium premise changes. |
| Is specialized construction needed at all? **Retain** direct use of sufficient general modeling or a supplied mechanism model. | B.5.FM can construct the thermal limiting argument without a causal-model family; C.28.MR can transform supplied equations directly. This pattern adds work only when the causal account or a material alternative is missing. | These internal alternatives determine :1 and :4.7. In :5.2 the additional work distinguishes supply, display and feedback before choosing a transformation. The examples establish conditional reasoning, not superior field performance. Prefer the simpler route when it supplies that distinction already. |


## C.28.CM:End {#end}

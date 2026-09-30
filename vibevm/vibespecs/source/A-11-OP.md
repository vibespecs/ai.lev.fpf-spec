# A.11.OP - Decision-Relevant Least Action and Operational Parsimony: Test a Proposed Requirement: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.11.OP:5 - Archetypal Grounding {#archetypal-grounding}

### A.11.OP:5.1 - Duplicate status update and deterministic publication build {#duplicate-status-update-and-deterministic-publication-build}

A publication repair route asks for a second status update immediately before the repair decision. The update has the same possible values as the first one. None changes `repair`, `stop`, or `publish`, no receiver cites it, and removing it changes no assurance or recovery condition. The second update passes no branch, so the route removes it or leaves it as an optional convenience.

The same route runs a deterministic build after the sources and publication form have been selected. The build has no decision-changing outcome by design, but it assembles the selected sources into the required publication. It passes selected realization and remains. Any claim about the assembled publication or its release still needs its direct owner.

### A.11.OP:5.2 - Exploration whose value appears in a later decision {#exploration-whose-value-appears-in-a-later-decision}

A maintenance team must choose next week between Method A and Method B for a recurring seal failure. A bounded probe performed today can return one of three observations: evidence favoring A, evidence favoring B, or an unresolved result that triggers a hold. Today's immediate action is unchanged, but every possible probe result has a named effect on the later Method-selection decision.

The probe passes the contribution screen. Its horizon ends at that named selection and window. The team still has to decide whether to obtain it.

For a constructed comparison, suppose A, B and holding are all available within the applicable operating constraints. The team minimizes expected hours of later rework or deferral over the same maintenance horizon. Its current model gives three conditions with weights 0.4, 0.4 and 0.2:

| Selected continuation | Condition favoring A | Condition favoring B | Unresolved condition |
| --- | --- | --- | --- |
| Method A | 0 hours | 10 hours | 5 hours |
| Method B | 10 hours | 0 hours | 5 hours |
| Hold | 4 hours | 4 hours | 4 hours |

These are illustrative planning inputs. On this basis, A and B each cost five expected hours; holding costs four. Suppose the probe distinguishes the three conditions in time. Choosing A, B or holding after its result costs 0.8 expected hours before probe effort. At one hour for the whole probe, the total is 1.8 hours, so the team selects the probe and the stated conditional continuation. At five hours for the same probe, still available before selection, the total is 5.8 hours: the completed advice is to hold on the current basis. If the probe cannot return before selection, its information does not serve this horizon. The operating constraints and uncertainty remain visible in each answer.

If instead the team establishes that every materially plausible observation leads to Method A and no other reliance changes, the probe fails even the contribution screen for that use. The team can choose A directly, without inventing a study and then recording why it was omitted.

### A.11.OP:5.3 - Assurance evidence with an unchanged operating decision {#assurance-evidence-with-an-unchanged-operating-decision}

A pressure-system release check is expected to confirm the current operating decision. The release authority nevertheless relies on its evidence, and omission changes the accepted exposure for release. The check passes assurance preservation even when its most likely result leaves the operating branch unchanged.

`B.3`, the applicable evidence pattern, and the release authority set the assurance floor and disposition. A.11.OP returns only that the check is non-ceremonial for this named release reliance. A candidate check qualifies here only when the relying condition, exposure change, and direct owner are known.

Now consider a local rule requiring a copy of the same accepted check record. In this constructed case, every relying reader already has the original, and retyping adds no independent verification. It consumes the technician's only hour available for correcting an identified defect. The local rule owner can amend this copying requirement today while retaining the required check and its accessible evidence. The useful amendment is to use the original record and recover that hour for correction. The protected people and pressure-system condition, the lost correction opportunity and the feasible authority to amend supply the comparison. If the amendment cannot be obtained in time, the technician follows the applicable requirement or authorized hold route; a favorable merits comparison alone does not authorize omission.

### A.11.OP:5.4 - Recovery cue and discriminating language {#recovery-cue-and-discriminating-language}

After an interrupted multi-part analysis, a small progress marker identifies the last closed item and the next item. Removing it can cause the practitioner to repeat completed work or resume from the wrong branch. The marker passes recovery preservation while that continuation use relies on it. If the task is short and the next item is already unambiguous, the marker becomes optional.

In another case, a sentence must distinguish a reusable Method from dated Work that enacted it. The distinction changes whether the practitioner repairs a description claim or a performance claim. The requirement to preserve that distinction passes the decision-changing-result branch for this use. Other terminology remains informative unless a named interpretation or action depends on it.

### A.11.OP:5.5 - Speculative compliance without a receiver {#speculative-compliance-without-a-receiver}

A team proposes generating a compliance packet for possible future reuse. No applicable authority or named receiving use has been established for the packet, so it passes no branch and is not mandatory.

If an applicable duty or relying receiver is later established, reopen the disposition under that direct authority. The earlier speculative possibility was not evidence that the duty already existed.

## A.11.OP:6 - Bias-Annotation {#bias-annotation}

Scope: **Universal** for the cross-domain admission question governed by this pattern.

| Lens | Likely bias | Countermove |
| --- | --- | --- |
| **Gov** | Parsimony language is used to bypass an instituted duty, safety rule, or assurance floor. | Return authority and applicability to the direct law, duty, Guard-Rail, evidence, gate, or assurance owner. |
| **Arch** | Every special case receives another owner, or this pattern absorbs Method, choice, Work, evidence, and assurance decisions. | Keep one three-branch admission screen and return every downstream claim to its direct pattern. |
| **Onto/Epist** | An author declares ordinary words such as *action*, *apparatus*, or *horizon* as new kinds, or treats information volume as decision relevance. | Keep the words ordinary and name the exact receiving decision, result, reliance, or recovery condition. |
| **Prag** | “Less is better” deletes exploration, deterministic realization, prevention, or recovery; “might help” preserves ceremony forever. | Compare keeping and removing at the nearest named substantive horizon through all three branches. |
| **Did** | The branch table becomes a mandatory form that costs more than the judgement it supports. | Keep ordinary use to one disposition sentence and introduce durable evidence only for a named relying use. |

## A.11.OP:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | What fails | Repair |
| --- | --- | --- |
| **Fewest steps wins** | Deterministic realization, exploration, assurance, or recovery is deleted because it adds work. | Apply all three branches and compare substantive consequences, not step count. |
| **Next-click horizon** | A probe is judged useless because it changes a later decision rather than the next administrative action. | End the horizon at the nearest named substantive receiver and state the dependency. |
| **Infinite downstream usefulness** | Any requirement survives because it might help an unnamed future user. | Require a named receiver, decision, reliance, or recovery use; otherwise remove or demote it. |
| **Administrative self-receiver** | A receipt is justified because it updates the route state that exists only to carry the receipt. | Name a subject decision or reliance outside the requirement's own administration. |
| **Fabricated alternatives for deterministic work** | A build or transformation step must invent outcome branches to look decision-relevant. | Retain it through selected realization when it performs the already selected result. |
| **Precaution label as assurance** | Calling a step “safety” or “compliance” creates an unsupported floor. | Name the direct authority, evidence, exposure, and relied-on condition; return their disposition to the direct owner. |
| **Possible contribution as sufficient reason to require work** | A probe is demanded because it could matter, despite unavailable means, excessive burden or a missed receiving window. | Establish contribution here; complete the live demand or choice question through C.11.DUA or C.11 and retain a useful current answer when acquisition is not selected. |
| **Mandatory parsimony record** | The screen creates the same ceremony it is meant to remove. | Use one ordinary disposition sentence unless a named later use needs a durable episteme. |
| **Free-energy or physics laundering** | Expected free energy, variational free energy, or Hamiltonian least action is presented as proof of a universal engineering rule. | Keep only the bounded epistemic, pragmatic, horizon, and risk distinctions; reject mathematical equivalence and mandated scalarization. |

## A.11.OP:10 - Rationale {#rationale}

Operational parsimony is about relevance, not abstract minimization. The fewest-step method can be wrong when one additional action realizes the chosen result, changes a later policy, or preserves a relied-on condition. The longest method can also be wrong when its extra actions have no substantive receiver. Comparing keeping and removing one proposed requirement makes that difference visible without inventing a global cost function.

The three branches distinguish contributions that a step-count screen would confuse. Decision-changing result recognizes exploration and discrimination. Selected realization recognizes deterministic work. Assurance or recoverability preservation recognizes a named relied-on condition. None alone establishes obtainability, net value or an obligation. Existing selection or reliance can settle the need; otherwise the direct choice or demand method completes it. This preserves useful work while allowing a probe that could matter to lose against an available continuation.

The horizon must be substantive and bounded. A next-event horizon hides delayed information value; an indefinite horizon lets hypothetical future usefulness justify everything. The nearest named receiver is the smallest horizon that can carry the reason and the smallest reopen boundary when the use changes.

The rule coordinates existing decisions, transformations, results, evidence, assurance, and recovery uses. Keeping these objects under their direct patterns preserves FPF layering while giving practitioners one discoverable admission question.

## A.11.OP:11 - SoTA-Echoing {#sota-echoing}

| Practice question | Best-known line and serious alternative | Defect overcome and pattern mutation | Source roles and limits | Reopen condition |
| --- | --- | --- | --- | --- |
| How should a process designer recognize information-seeking action whose value appears in a later decision rather than the immediate result? | Historical anchors distinguish epistemic from pragmatic value and evaluate present action across counterfactual future policies. The serious default is an immediate-result screen that calls a probe useless when the next action stays unchanged. | The default deletes useful exploration. **Adapt:** the decision-changing-result branch recognizes a probe's contribution when a materially plausible result changes a named later policy inside the substantive horizon; the receiving choice still decides whether obtaining it is worthwhile. | Friston et al., [“Active Inference: A Process Theory”](https://direct.mit.edu/neco/article/29/1/1/8207/Active-Inference-A-Process-Theory) (2017), supplies the epistemic/pragmatic distinction; Friston et al., [“Sophisticated Inference”](https://direct.mit.edu/neco/article-abstract/33/3/713/97487) (2021), supplies the counterfactual policy horizon. They supply historical discriminators, not evidence of a universal engineering threshold, FPF ontology, or effectiveness claim. At comparable use effort, naming the receiving decision preserves delayed value that the immediate-result default loses. | Reopen if stronger current evidence changes the epistemic/pragmatic distinction, defeats the receiving-decision test, or supplies a lower-effort discriminator that preserves the same exploration boundary. |
| When does relevant uncertainty justify another inquiry? | The current constructed-value-of-information line separates decision relevance from uncertainty magnitude and examines uncertainty in the prioritization itself. The serious alternative treats either large uncertainty or a possible decision change as a sufficient acquisition rule. | **Adapt:** contribution screens a demand; the receiving decision then compares attainable gain with the whole burden. Use a proportionate sensitivity comparison when plausible input changes could reverse that result. | Runge et al., [A Simplified Method for Value of Information Using Constructed Scales](https://pubsonline.informs.org/doi/10.1287/deca.2023.0474) (2023), supplies preliminary decision-relevance assessment. Davis et al., [Constructed value of information with iterative scoring and parametric uncertainty](https://pubmed.ncbi.nlm.nih.gov/41678595/) (2026), supplies a later research-priority comparison in which scoring uncertainty can change priorities. Their domain results motivate these distinctions; they do not establish a universal required score, authority or engineering threshold. `C.11` and `C.11.DUA` carry the local choice and advice methods. | Reopen when a relevant source or actual use changes how attainable information alters the receiving decision, or defeats the proportionality of the comparison. |
| Can expected free energy or physical least action serve as a universal scalar rule for admitting engineering actions? | The selected critical line shows that expected free energy is not obtained merely by projecting variational free energy forward, while least-action results in the free-energy principle depend on a particular random-dynamical and Bayesian construction. The serious alternative is to transplant EFE, VFE, or Hamiltonian “least action” as a general engineering objective. | The transplant launders model-dependent mathematics into authority and can hide the actual receiving use. **Reject:** no EFE/VFE/Hamiltonian equivalence or mandatory score enters the Solution. **Adapt:** judge information-seeking work by a named receiving decision and counterfactual horizon, with risk and ambiguity supplied by their direct owners. | Millidge, Tschantz, and Buckley, [“Whence the Expected Free Energy?”](https://direct.mit.edu/neco/article/33/2/447/95645/Whence-the-Expected-Free-Energy) (2021), supplies failure evidence against the simple VFE-forward account. Friston et al., [“The free energy principle made simpler but not too simple”](https://www.sciencedirect.com/science/article/pii/S037015732300203X) (2023), supplies the model-dependent least-action construction. Neither source establishes an engineering duty, assurance floor, scalar optimum, or universal process law. The selected qualitative rule is cheaper to apply and keeps direct authorities visible. | Reopen if a current primary result establishes a transferable engineering admission rule with explicit scope and lower decision error at comparable effort, or if a governed use requires a quantitative comparator under its own direct pattern. |


## A.11.OP:End {#end}

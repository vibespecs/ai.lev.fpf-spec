# C.28.CM - Construct and Challenge a Causal Model {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Stable
> **Normativity:** Normative unless marked informative

## C.28.CM:1 - Problem frame {#problem-frame}

Use this pattern when an explanation names a possible cause but leaves you unable to work out what follows, compare another mechanism, or say what observation could change the explanation. The difficulty can arise in a work process, a physical device or an AI-assisted task. A plausible story is available; the causal relations needed for the question still have to be constructed.

Begin with one outcome, the contrast that matters, and the relevant observations and subject knowledge. Express two materially different accounts when both remain plausible. Work out a consequence on which they differ, or identify the premise that prevents that comparison. An annotated sketch and a conditional explanation can be the first useful result.

The governed object is the causal model, or family of alternative causal models, being constructed for that question. This is the causal branch of broader modeling and explanation work. The model describes proposed mechanisms and the conditions of a consequence; it remains distinct from the situation, its observations and the evidence for those mechanisms.

Use a sufficient existing model directly. A calculation under known physical relations can finish in B.5.FM or C.28.MR. A disagreement about whose objective should govern needs that practical or normative decision; constructing more causal arrows will not supply it. If a subject relation cannot be recovered, ask for that relation or retain the missing premise. Neither a literature review nor a numerical model is a universal prerequisite.

## C.28.CM:2 - Problem {#problem}

“Missing information caused the delay” can conceal several accounts. The information may be needed to perform the work. Both the omission and the delay may arise from overload. The recorded omission may describe a logging failure rather than the information actually available. Studying only reported incidents can introduce a further difference.

These accounts can support different responses while fitting the same initial story. Filling a field, changing the generating process, improving registration and temporarily supplying another route are different actions. A model makes their assumptions and consequences inspectable before one narrative becomes the explanation.

A second difficulty arises when a diagram is mistaken for evidence. Drawing a mediator does not establish that the mechanism operated. Leaving out an arrow makes a substantive assumption. A model can be useful for exposing such a premise before it supports an empirical effect claim.

## C.28.CM:3 - Forces {#forces}

| Force | Consequence for construction |
| --- | --- |
| A useful first result may be qualitative. | Add equations or probability laws when the needed consequence requires them. |
| Subject knowledge constrains mechanisms, while the first account may be incomplete. | Keep the basis for a relation and a serious alternative recoverable. |
| More variables can expose a missed influence or make construction unaffordable. | Add a distinction when its omission can change the answer. |
| Different models can fit the available observations. | Preserve the resulting uncertainty instead of selecting a graph for its appearance. |
| An action can help before its complete explanation is known. | Return the supported conditional result and let the receiving decision judge whether further inquiry is worthwhile. |

## C.28.CM:4 - Solution {#solution}

Construct the account around the question, then challenge the relations on which its useful consequence depends. The following moves can return to one another. A discovered measurement error may change the outcome definition; a missing mechanism may change the question.

### C.28.CM:4.1 - Fix the contrast and the time that matter {#fix-the-contrast-and-the-time-that-matter}

State what needs explaining or changing. Name the outcome and the cases it concerns, the relevant time, and any proposed action or comparison. “Why did this queue start?”, “Why does it remain?” and “What will shorten it now?” can require different mechanisms.

Distinguish an observed comparison from an intervention query. Observing X=x supplies information about the mechanisms already operating; imposing X=x replaces a mechanism. When the question concerns the same past case under another action, preserve its factual observations and the underlying conditions they constrain. C.28.MR develops the corresponding model calculation; C.28 determines what supports that use.

Keep the question small enough for a useful contrast. If two retained accounts permit the same sufficient next action under its own grounds, C.11.DUA can settle whether distinguishing them is worth the effort.

### C.28.CM:4.2 - Turn the story into variables with subject meaning {#turn-the-story-into-variables-with-subject-meaning}

Choose quantities or distinctions that can vary across the relevant cases or times. Give each a meaning, possible values and observation time. A particular late delivery is a case; its lateness is a value of a selected variable. Whether a variable is binary, ordinal or continuous depends on the question and measurement.

Separate the subject quantity from its registration when that difference matters. For example, distinguish an identifier present in the submitted report, a log entry reporting its absence, and inclusion of that report in an incident sample. Recover how the observation is produced through C.16 when needed. A copied ticket is another report of the same event, not another occurrence of it.

Retain enough distinctions for the proposed contrast. Combining two stages is unsafe when the action can change one while leaving the other unchanged. Conversely, a single “ready for dispatch” variable may suffice until readiness failures require different responses.

### C.28.CM:4.3 - Propose mechanisms and serious alternatives {#propose-mechanisms-and-serious-alternatives}

For each consequential relation, explain how changing a proposed cause could change its effect under the relevant conditions. Use the process arrangement, physical law, subject theory, observations or qualified source that supports that proposal. Mark a conjecture as such. A chronological sequence can suggest a mechanism while leaving common causes unresolved.

Construct a material alternative: another cause, a common influence, a recording difference, or a model in which the proposed direct influence is absent. Causes may coexist. An account of overload need not remove an effect of missing information. Keep the outcome and horizon comparable, and specify the same intervention in each model when that is the question.

A directed arrow X → Y represents a proposed direct causal influence in the chosen model. “Direct” is relative to the variables retained. Explain a consequential omitted influence as carefully as an included one: excluding it may be what makes the answer follow.

For an equation-based model, write the relevant mechanisms in a form such as Y=f(X,U), where U represents inputs left outside that mechanism. Specify shared inputs or their dependence when needed. A graph supplies qualitative restrictions; it does not supply an omitted functional form, effect size or disturbance law. Ask for these only when the receiving calculation needs them.

### C.28.CM:4.4 - Inspect the whole relevant structure {#inspect-the-whole-relevant-structure}

Follow possible paths between the proposed cause and outcome. Look for common causes, intermediate mechanisms, measurement processes and selection of cases. A common cause can coexist with a causal path. The role of a node is relative to a path and question, not a permanent label attached to the variable.

For a **directed acyclic graph (DAG)**, the following path test makes that inspection precise. A path joins distinct nodes along edges, ignoring arrow direction when finding the path. At an internal node, two arrowheads meeting there make it a collider on that path; other internal nodes are noncolliders.

Given a conditioning set W disjoint from the endpoints, a path is open when every noncollider on it is outside W and every collider is itself in W or has a descendant in W. Otherwise it is blocked. If every path between two variable sets is blocked, the sets are d-separated by W. For a distribution satisfying the graph's Markov property, d-separation implies the corresponding conditional independence. An open path permits dependence; it does not guarantee it for every parameter choice. Inferring graph structure from observed independences needs further assumptions, often faithfulness (no extra independences beyond those entailed by the graph), as well as adequate data.

Apply this rule to all relevant paths, including those opened by the way the sample was selected. Conditioning on an incident being reported can matter even when “reported” is absent from the regression.

Consider the complete small graph:

~~~text
Z → X → M → Y
Z → Y
X → S ← Y
S → D
~~~

There are three simple X-to-Y paths. X → M → Y carries the proposed causal mechanism; X ← Z → Y carries a common cause; X → S ← Y is blocked at S before conditioning. Conditioning on Z blocks the common-cause path and retains the causal path. Conditioning on M blocks that causal path. Conditioning on S, or its descendant D, opens the collider path. Inspecting only the fork would miss that selection effect.

For a total effect in an appropriate causal DAG, the back-door criterion provides one sufficient adjustment rule: choose measured covariates that are not descendants of X and block every path entering X through an arrowhead. This leaves the directed causal paths available. The resulting identification still relies on the model's causal interpretation, suitable data and support for the required comparisons. Failure of this sufficient criterion is not proof that the effect is unidentified. Use C.28 for the identification question rather than inventing an adjustment from one recognizable three-node shape.

The ordinary d-separation rule above applies to DAGs. If feedback matters, distinguish times: an outcome at t may affect workload at t+1. A finite time-unfolded model still needs its initial conditions and omitted influences justified. An equilibrium with simultaneous causal feedback needs an appropriate cyclic model, its solution conditions and its separation rule. Do not erase feedback merely to obtain an acyclic picture.

### C.28.CM:4.5 - Derive a consequence that can distinguish the accounts {#derive-a-consequence-that-can-distinguish-the-accounts}

Work the same question through each retained model. Start with a direction, a possible or impossible outcome, a conditional independence, or an observation that one account can explain only by adding another premise. Show which relation makes the consequence follow.

Keep three operations distinct. Conditioning restricts attention using an observed value. Intervention replaces the specified mechanism. Omitting a variable from a report or marginalizing it out leaves its possible influence in the subject model. Treating all three as “fix the variable” can reverse the conclusion.

When the mechanisms are specified, C.28.MR derives an intervention consequence while retaining the relevant other mechanisms and underlying inputs. Use C.29 when expressing or computing the model requires further mathematical construction. If the needed function or input law is missing, return that precise gap along with any qualitative result that survives.

Two graphs may entail the same observed independences. Two mechanisms may produce the same measurements in the available range. Retain both when the present material does not distinguish them. A causal-discovery procedure can contribute within its declared model class and assumptions; its returned graph does not remove those conditions.

### C.28.CM:4.6 - Challenge the consequence with available evidence {#challenge-the-consequence-with-available-evidence}

Compare the consequence with an observation, contrasting case, subject argument or feasible intervention that bears on it. First check that the observation concerns the modeled variable, cases and time. A contradiction can arise from the mechanism, measurement, implementation of a proposed action, or a changed operating condition.

Distinguish a contradicted implication, an untested implication and compatibility with the inspected material. A graph with no relevant testable implication cannot acquire support merely from an absence of contradiction. Conversely, failure to reject an implied independence does not establish the graph. Deterministic constraints, measurement error, missing cases and sampling uncertainty can all change the interpretation.

Revise only as far as the finding warrants. Preserve a valid observation when its causal interpretation fails. Restore a rival when its rejected premise changes. If an additional study could change the answer, C.28:4.8 helps specify the evidence question and C.11.DUA helps choose whether to obtain it. A useful model may end with an unresolved distinction.

### C.28.CM:4.7 - Return the model with the use it can support {#return-the-model-with-the-use-it-can-support}

Give the recipient the question, the relevant mechanisms and alternatives, their source basis and assumptions, the derived consequence, and the uncertainty that changes its use. A short explanation can carry this result; no universal record form is required.

Recognition can stop at “these two accounts imply different responses”. Consequential reliance requires the corresponding subject and evidential grounds. C.28 qualifies causal support; a statistical estimate or bound requires its own identification and estimation result. A controlled direct effect is a different query from a total effect. A claim about the cause of one historical outcome or responsibility also needs its chosen concept and subject standard; a population effect does not settle it.

Return the next useful contribution by what it must establish: for example, whether a log reflects an actual omission, whether a controller reads a display, or whether an apparent AI effect survives comparable task selection. Temporary mitigation can remain available under its own evidence, costs and authority while the causal question is open.

## C.28.CM:7 - Conformance Checklist {#conformance-checklist}

- The outcome, cases, time and required contrast can be recovered.
- Each consequential variable and relation has a subject meaning; registration and selection are explicit when they change the answer.
- Important included and excluded influences have stated grounds or remain assumptions.
- Material alternatives receive comparable questions, including coexisting causes where relevant.
- The graph or equation class supports the rule used; DAG path inspection covers all relevant paths and conditioning, including selection.
- A consequence follows from named premises, or the missing premise is returned precisely.
- Compatibility, contradiction and absent discrimination retain different meanings.
- The returned use distinguishes recognition, model consequence, evidential support and action choice.

## C.28.CM:9 - Consequences {#consequences}

The practitioner obtains explicit alternatives, a usable conditional consequence and a concrete return when a premise is missing. This can prevent spending effort on an intervention that changes only a record or on a study that cannot distinguish the live accounts.

The cost is recovering mechanisms, meaningful variables and competing assumptions. Limit that cost to distinctions that can change the question's answer or a consequential use. Some questions remain unidentified or underdetermined; a clearer statement of that limit is a useful result.

## C.28.CM:12 - Relations {#relations}

- **B.5.FM** constructs a general first model; this method develops the missing causal relations and returns their conditional consequences.
- **B.5.2** generates and compares hypotheses. Causal-model construction can change their plausibility grounds or expose an unresolved rival.
- **C.16** qualifies measurement and registration; **C.27** qualifies temporal claims when those questions are needed.
- **C.28** governs causal-use support, identification and evidence questions; **C.28.MR** derives a consequence of changing specified mechanisms.
- **C.29** supplies needed mathematical representation and computation.
- **C.11.DUA** compares worthwhile inquiry with available action; **A.15.9** obtains a missing contribution from another practice.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/B-5-FM#root, spec://ai.lev/fpf-spec/contract/B-5-2#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/C-27#root, spec://ai.lev/fpf-spec/contract/C-28#root, spec://ai.lev/fpf-spec/contract/C-28-MR#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/C-11-DUA#root and spec://ai.lev/fpf-spec/contract/A-15-9#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-40-CU#root, spec://ai.lev/fpf-eng-mkt/contract/MKT-10#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-28-CM

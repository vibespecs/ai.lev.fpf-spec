# E.10.INT - Recovering What Interest or Curiosity Means Here {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** lexical and ontological precision restoration (E)
>
> **Status:** Draft

## E.10.INT:1 - Problem frame {#problem-frame}

**Use this when** a claim that something is *interesting*, *in someone's interest* or *driven by curiosity* is being used to choose work, but leaves you unsure what to do. You may need to select an experiment, retain a promising construction, design an agent's exploration policy or understand why participants want different outcomes.

Begin by saying whose interest is involved and what the sentence proposes. “This experiment is interesting” might mean that its result would distinguish two models, that a participant wants to try it, or that the resulting technique could support further experiments. Each meaning can guide useful work.

The first result is a clearer sentence and a next action that follows from its meaning. Keep ordinary wording when its meaning is already sufficient. A musician expressing delight and a contract stating an interest rate can continue their respective work without this recovery.

## E.10.INT:2 - Problem {#problem}

The same word connects several different questions. An informative observation changes beliefs; a learning-progress signal compares what a learner can do; a promising stepping stone offers further possibilities; an affected participant has something to gain or lose. In a joint project these relations often coexist.

Their differences matter when a phrase becomes an instruction. Asking an agent to maximize “surprise” may reward unpredictable observations instead of observations that help it distinguish its hypotheses. Requiring a promising idea to demonstrate progress toward a distant goal may discard the very construction from which another goal could emerge. Selecting an “interesting rhythm” leaves the choice unresolved until the listener, performer or musical use is known.

## E.10.INT:3 - Forces {#forces}

| Force | Working tension |
|---|---|
| Shared vocabulary | A short familiar word helps discussion, but can hide which participant or consequence guides a choice. |
| Several useful explanations | Motivation, information gain and future possibilities may contribute together, while their measures answer different questions. |
| Open exploration | A present clue can justify trying a continuation before its eventual uses can be predicted. |
| Proportionate precision | A consequential choice needs its meaning restored; an ordinary expression often needs no further work. |

## E.10.INT:4 - Solution {#solution}

Recover the relied-on meaning, then continue the work that gives it value.

1. **Locate the claim that matters.** Take the sentence together with the decision or activity it is meant to guide. Ask what would change if the object were judged interesting. If nothing depends on that judgement, keep the expression as it stands.
2. **Name the participant and relation.** Identify who is engaged, affected, learning or choosing. Identify what draws attention, what might change, or what the participant stands to gain or lose. Use the distinctions in §4.1 only where they resolve the sentence.
3. **Preserve combined meanings.** If a participant enjoys an experiment and the experiment could distinguish two models, say both. Let the corresponding motivation and inquiry methods supply their different contributions.
4. **Restore a needed comparison.** When a score or optimization rule is proposed, name what it compares and under which model, experience or resources. Use §4.2 to resolve ambiguous appeals to surprise, progress or a Goldilocks region.
5. **Return to the action.** Rewrite the claim so its recipient can choose, inquire, practise, retain a result or explain a concern. Continue once that meaning is sufficient. A shared decision can keep the clarification in its existing account; an ordinary sentence needs no additional form.

### E.10.INT:4.1 - Recover the contribution being claimed {#recover-the-contribution-being-claimed}

These are recurring uses of the wording. Select the ones needed for the sentence; several can apply together.

| What the wording is doing | What to recover | Example of the resulting claim |
|---|---|---|
| Expressing a participant's stake | The participant, affected outcome and consequence | “The maintenance team wants the inspection window because it can then replace the worn coupling.” |
| Expressing attraction or engagement | The person or group, activity and response | “These listeners want to keep moving to this rhythm.” |
| Selecting information-seeking action | The agent's uncertainty, available observation and use of the resulting information | “The controller samples input 1 to distinguish the two candidate relations before choosing its command.” |
| Describing learning progress | The learner or model, what changes and the comparison | “After training, the compressor describes the same material in fewer bits.” |
| Explaining active-inference policy selection | The generative model, candidate actions, information expected from them and preferences over outcomes | “The agent first observes the cue to learn which action is likely to produce its preferred outcome.” |
| Recognizing a promising continuation | The present clue, available variation or combination, and what is worth trying or retaining | “This construction permits a new family of transformations; keep it available for exploration.” |

An information-seeking policy can be attributed to a human, an AI agent or a collective whose members obtain and use the information. For a claim about a person's experience, preserve that experiencer. A policy description alone leaves the question of subjective experience open.

A prospective continuation can be supported by a hunch, a newly available operation or a promising variation. State that basis at its actual strength. Where its future destination is unknown, the next action can be to explore or retain the construction. C.18 supplies retention in an exploration archive; C.19 helps choose which directions in an active search pool to continue, retain or stop; C.40 helps develop problems and ways together.

### E.10.INT:4.2 - Recover the model behind the comparison {#recover-the-model-behind-the-comparison}

For **surprise**, first recover the quantity being used. The surprisal of an observation, `-log p(observation)`, concerns its probability under a selected model. Bayesian surprise concerns the change from prior to posterior beliefs about chosen variables. Expected information gain evaluates a possible observation before it is obtained. A learning-progress signal compares successive predictive or constructive performance under a learning procedure. Those comparisons can disagree, as §5.1 shows.

In **active inference**, distinguish updating beliefs from selecting actions. Predictive coding uses prediction errors to update beliefs about hidden states and, in learning formulations, model parameters. Policy selection also depends on the information and outcomes expected from action. Recover the prior preferences when a source explains avoiding an outcome through its expected surprise. The source's account may couple epistemic and pragmatic value. Preserve that coupling together with the quantities and assumptions that give it meaning.

For a **Goldilocks region**, recover what varies, for which agent and use, and over which range. It might concern an attainable learning challenge, a listener's response to syncopation or a combination of rhythmic properties. Use the applicable account of the relation between those characteristics and the desired result. The useful region can move as the agent learns or as the task changes. In a search algorithm, a difficulty screen can select candidates for learning while novelty and transfer still govern which possibilities are retained.

When a quantitative answer is needed, C.16 supplies measurement and C.17 separates novelty, usefulness and sample surprise. Keep an adequate qualitative comparison when it already settles the action.

### E.10.INT:4.3 - Combine contributions in a development project {#combine-contributions-in-a-development-project}

A project can use information-seeking to distinguish alternatives, learning progress to choose a promising practice opportunity, and novelty or diversity to retain further possibilities. State the contribution of each rule to that project.

For example, a group can test the controller in §5.1 during a maintenance window. The researcher calls input 1 interesting because its response distinguishes two candidate relations. A colleague sees the query construction as material for other unknown interfaces. The maintenance team needs the controller returned to service before the window ends. Recover their claims as three instructions: “Query input 1 to choose the command”; “Keep this construction available for exploration of other interfaces”; and “Schedule controller work within the available window.” If the relation is supplied, the query becomes unnecessary. The potential use of the construction remains, and the window still constrains any remaining controller work.

C.11 compares formed options when a choice is needed. C.19 helps decide which directions in an active search pool to continue, retain or stop. A single agent's information-seeking policy uses the applicable subject method; choosing among formed queries can use C.11. C.40 supports the development of problems and ways. The field's methods supply the experiment, training activity or construction itself.

## E.10.INT:7 - Conformance Checklist {#conformance-checklist}

- The repaired sentence identifies the participant and the contribution that matters to the work.
- Combined meanings remain recoverable when both affect the action.
- A proposed score retains its model, comparison and receiving use.
- An exploratory continuation can proceed from its present basis while its eventual destination remains unknown.
- The reader can resume the relevant activity, or identify the particular unresolved meaning that prevents it.
- The recovery stops when ordinary wording is sufficient; further measurement or inquiry follows the needs of the activity.

## E.10.INT:9 - Consequences {#consequences}

A clarified interest claim can guide an experiment, an exploration policy, a practice choice or a discussion of stakes. A project can combine these contributions while preserving what each one explains.

Recovery sometimes reveals that the needed information is absent. Keep that uncertainty attached to the claim. Obtain more information only when its possible contribution warrants the work, using C.11.DUA when the advice or demand itself needs examination.

## E.10.INT:12 - Relations {#relations}

- **E.10 and E.10.ARCH** locate this recovery when interest-family wording hides the relation needed for work. F.19 handles the surrounding prose.
- **E.10.LRN** recovers a remaining ambiguity about what learned or changed. E.10.DEV handles a remaining development or evolution claim.
- **C.16 and C.17** supply measurement and the distinctions among novelty, usefulness and sample surprise.
- **C.11** compares formed options; **C.19** governs directions in an active search pool; **C.18** supplies retention in an exploration archive. **C.40** develops problems and ways together.
- **D.1 and D.3** supply ethical-value and conflict analysis when affected interests raise those questions.
- **E.23.CDI** offers candidate capability-development guidance that separates a described acquisition method, its execution and an asserted capability change. It can govern an FPF claim only after its own admission; the applicable admitted field pattern supplies the acquisition or intervention method.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-10#root and spec://ai.lev/fpf-spec/contract/E-10-ARCH#root. @status:spec/done
- @fact:USES Uses: spec://ai.lev/fpf-spec/contract/E-10-LRN#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/C-17#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/C-18#root, spec://ai.lev/fpf-spec/contract/C-19#root and spec://ai.lev/fpf-spec/contract/C-40#root for the recovered question. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/B-5-QD#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-10-INT

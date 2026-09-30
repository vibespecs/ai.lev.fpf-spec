# First Principles Framework (FPF) Readme {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Readme section of the publication. See LICENSE.md for the list of changes.

> First Principles Framework (FPF) is a standards-style pattern language for turning difficult engineering, research, management, and mixed human and AI work into explicit, reviewable, improvable reasoning.

FPF helps when a project has outgrown one clever conversation. It is useful when meanings, claims, options, evidence, architecture, work decisions, publication forms, and improvement criteria need to stay coherent across people, teams, tools, time, or AI agents.

## Start here {#start-here}

Before selecting framework guidance, read and apply [Using FPF and its DPF Suites](spec://ai.lev/fpf-common/pub/USING-FPF#root). This instruction applies to project work, framework development, review and coordination. It explains how to find and read relevant content in the publications available to you, including when an interface cannot retrieve a large file.

When an AI agent assists you, put this requirement and the instruction's location in your project's `AGENTS.md` or equivalent instructions. If a reading test explicitly limits its reader to an isolated excerpt, use only the materials supplied for that test; do not add USING-FPF.md unless the test includes it.

Use FPF as a reference model and pattern language, not as a linear textbook. Start from the working question you bring from your project. Bring in internal FPF terms only after they help you keep the work precise.

You can ask an assisting agent to explain an answer or give feedback in ordinary language, without FPF terminology. For example: “Explain this and comment on my proposal without FPF jargon; use the language of my work.” The patterns can guide the reasoning while the answer uses familiar words.

This readme is a thin public practical-use rendering of FPF for engineers, researchers, managers, reviewers, and AI-assisted project workers deciding what FPF can help them do now. It foregrounds the project questions most likely to pay off and deliberately coarsens, omits, or defers the full pattern language, source publications, source-use history, and relation structure. When a claim becomes important, use the Preface and Table of Contents as locators, then inspect the exact definition, constraint, test, method, evidence rule, or assurance rule needed for that claim in the cited pattern body; do not treat this readme as the specification.

Begin with the project object at stake and the current question about it. In FPF, a holon is an object whose actual construction supports treatment as a whole with parts and as a possible part of a larger whole. Examples, when they meet the conditions in `A.1`, include a machine, product, organization-as-system, body of knowledge, publication system, work occurrence, discipline, AI-agent arrangement, method, or local framework.

Bare claim-bearing *role* has no single FPF referent. Start with `E.10.ROLE`, then continue through the object or relation it recovers. If the recovered wording is a claim-bearing function use, apply `A.6.F` and its selected subject pattern. Do not choose a branch from the trigger word alone. Once the object and question are named, ask which structure, claim, decision, evidence, description, Work, or improvement relation is current.

## Practical entries {#practical-entries}

The entries below illustrate questions that FPF can help answer; they do not exhaust its uses. Bring the actual difficulty from your project and use the search guidance in USING-FPF.md to find an individual method or a connected application. Search the Table of Contents for relevant entries, or ask an assisting agent to compare plausible candidates.

The ordinary examples start with one direct pattern and retain any conditions for a later use. They can stop at the first useful result without a mantra. The Practical-Use Cards show another use: a difficult question whose answer normally draws on several pattern contributions. Their mantras show in compact form how that answer unfolds through those contributions, without turning the unfolding into a fixed workflow.

### LIVE-WORK-STEERING — Choose the next action while Work is changing {#live-work-steering-choose-the-next-action-while-work-is-changing}

- **Situation:** Ongoing Work has an applicable domain Method, but a current fact can change what should happen next.
- **Question:** What should the deciding System choose now, who will perform it, and when must they stop or look again?
- **First useful result or blocker:** One bounded decision, intended performer, and feedback condition—or a named blocker due to missing or outdated action-guiding information, authority, capability, safety, applicability, or no current Work.
- **Start with:** `A.15.7`.
- **Stop or return:** Stop when the action, performer, and nearest return condition are clear. If ongoing Work is blocked by a missing or unsupported performer, support, or continuation-state relation rather than by candidate choice, use `A.15.8` to repair that configuration or stop, then return. If Work has not begun, use `A.15.2` for intended-work content, `A.15.5` for work-entry readiness, or `C.11` only when a known chooser must compare an already formed `OptionSet`.

### METHOD-RECOVERY — Explain what reusable way several performances may show {#method-recovery-explain-what-reusable-way-several-performances}

- **Situation:** Several observations or records suggest a reusable way, but no Method has been established.
- **Question:** What candidate explanation is supported, which real rivals remain, and which uncertainty can change the intended use?
- **First useful result or blocker:** One source-traceable provisional account per candidate with real rivals and relevant gaps—or an honest record-only result. Include a useful distinguishing question when it changes recovery or receiving use; designing or undertaking a study is a separate choice.
- **Start with:** `A.3.1.MR`.
- **Stop or return:** Stop at the strongest honest account or lowering result. Continue to `A.3.1` or specialist `ME.18` only when that later use is current.

### PROFESSIONAL-RESULT — Use one result from another practice without transferring the decision {#professional-result-use-one-result-from-another-practice}

- **Situation:** A decision needs a legal, safety, tax, privacy, engineering, scientific, or other outside-practice result, but the available source or request names only a title, department, document, approval, provider, or tool.
- **Question:** What does the available result support for this decision, and would an obtainable additional contribution warrant its whole acquisition burden?
- **First useful result or blocker:** The supported answer with its necessary use limit, a worthwhile bounded result request, or the exact source, Method, capability, authority, access, evidence, or applicability blocker.
- **Start with:** `A.15.9`.
- **Stop or return:** Finish at the useful answer and its material limit; a remaining gap does not itself require a request or an explanation for omitting one. Select acquisition through A.15.9 when its contribution is worth obtaining. The supplier keeps its Method and professional authority; the receiver keeps the receiving decision. A title, document, delivery, provider label, or tool output transfers neither.

### NAMING — Give one identified thing a usable name {#naming-give-one-identified-thing-a-usable-name}

- **Situation:** One already identified thing needs understandable wording; later use may also require a stable, reusable name.
- **Question:** Does ordinary wording suffice, or which durable name preserves the thing and avoids misleading alternatives?
- **First useful result or blocker:** Sufficient ordinary wording; only when reuse needs a durable settlement, one local `NameCard`; otherwise the exact missing thing, use, reader group, scheme, sense, or candidate evidence.
- **Start with:** `F.18` when the name must become durable. For one-off wording, keep the ordinary phrase and use the thing's direct pattern only if its meaning is unclear.
- **Stop or return:** Stop without a card when ordinary wording answers the need; otherwise stop at the local naming settlement. Return when the thing, use, readers, scheme, or likely misunderstanding changes.

### SYSTEM-RECOGNITION — Test systemhood only when it changes the decision {#system-recognition-test-systemhood-only-when-it-changes-the}

- **Situation:** A decision may change if one exact entity is a System, while the same noun may instead name Work, a Method, capability, episteme, structure, or another subject.
- **Question:** What decision depends on treating that entity as a System?
- **First useful result or blocker:** Return to the direct non-system claim; recognize or reject the System reading; or name the missing construction fact or test.
- **Start with:** `A.1.SCR`.
- **Stop or return:** Stop at that direct result or exact blocker. A noun, assignment, capability, plan, or project label does not establish systemhood.

### TIME — Decide what a timing claim lets you do {#time-decide-what-a-timing-claim-lets-you-do}

- **Situation:** A trend, deadline, cadence, or stale result is being used to decide what to do next.
- **Question:** Which moment, rate, rhythm, or freshness relation matters, and does it support continuing, refreshing, waiting, synchronizing, or changing rhythm?
- **First useful result or blocker:** A bounded temporal claim and supported continuation, or the exact missing window, evidence, effort, resistance, or currentness basis.
- **Start with:** `C.27`; use `G.11` only when an affected result may need scoped refresh because its basis is stale.
- **Stop or return:** Stop at a state or rate reading when it supports no stronger claim. Return when the window, evidence, currentness, or intended use changes.

### CAUSAL-USE — Keep a causal-looking result within its support {#causal-use-keep-a-causal-looking-result-within-its-support}

- **Situation:** A correlation, estimate, simulation, or comparison is being used to say that an action will cause an outcome.
- **Question:** What causal statement may the evidence support, and what stronger statement must not guide intervention or investigation?
- **First useful result or blocker:** A supported statement and its limit, or the missing alternative, intervention, comparator, evidence path, identification result, or transport basis.
- **Start with:** `C.28`.
- **Stop or return:** Stop, narrow the claim, or abstain when support is insufficient. The causal-use result does not choose, deploy, publish, or certify by itself.

### MEASUREMENT — Make a number interpretable before relying on it {#measurement-make-a-number-interpretable-before-relying-on-it}

- **Situation:** A reading, score, rating, sensor value, or dashboard number is being compared or used in a decision.
- **Question:** What exact subject and characteristic were measured, on what scale and unit, by what method, and under what calibration and time stance?
- **First useful result or blocker:** An interpretable attributed value with uncertainty and a use boundary, or the missing subject, scale, method, calibration, evidence, or validity window.
- **Start with:** `C.16`.
- **Stop or return:** Stop when the value supports the present comparison. Return when the subject, method, calibration, time stance, uncertainty, or use changes.

### MATHEMATICAL-MODELING — Obtain a useful consequence from a representation {#mathematical-modeling-obtain-a-useful-consequence-from-a}

- **Situation:** A working question needs a mathematical construction, or a proposed representation may omit something that changes the answer.
- **Question:** Which object and correspondence make the question answerable, and which conditions permit using its result?
- **First useful result or blocker:** A calculation, bound, construction, obstruction or distinguishing observation, with its interpretation; alternatively, the missing relation or operation.
- **Start with:** `C.29:4.1`. Use an adequate local equation or algorithm directly when no representation question remains.
- **Stop or return:** Stop when the consequence answers the present use. Return when a changed assumption, lost distinction or execution condition changes that consequence. Validate correspondence to a phenomenon when the intended reliance requires it under `C.29:4.5a`.

When the direct pattern is already known, open it rather than forcing the question into an example: `E.11.PFP` for framework publication, `E.11.DSG` for the DPF Suite Reference when a question spans several DPFs, `A.15.6` when *project*, *process*, or *case* hides the subject, `A.1.1` for model-use organization, `C.22.PFR` for an actual-problem claim, and `A.6.REL` for an obtaining relation. These are locators, not more selectable examples.

### WORK-OPPORTUNITY — Find a useful continuation before proposing change {#work-opportunity-find-a-useful-continuation-before-proposing}

- **Situation:** Work meets its present requirements, or you have useful material but no settled question about what to change.
- **Question:** What result could matter here, and is finding or proposing another way worth the work it creates?
- **First useful result or blocker:** A supported local possibility, a question worth resolving, an exact missing contribution, or continuation of the present work.
- **Start with:** Use [C.40](spec://ai.lev/fpf-spec/contract/C-40#root) for material whose useful result is still open; [C.39](spec://ai.lev/fpf-spec/contract/C-39#root) when the result is known but its obtaining way is missing; [C.11.DUA](spec://ai.lev/fpf-spec/contract/C-11-DUA#root) when a proposed change needs a value-and-burden judgement. Use adequate domain reasoning directly.
- **Stop or return:** Stop at that first result, including no worthwhile advice. Reopen only the conclusion whose conditions change; existing obligations remain in force.

Start with a bounded piece of available work: for example, replay an order queue using its durations and delivery conditions, or compare how two recipients use the same result. Try a supported variation of an operation, order, contribution or use; say which consequence it could change. A different word or an unusual observation is a lead, not a diagnosis. If the needed way is absent, construct and explain a local operation or identify its exact missing basis.

Before proposing that variation, distinguish the larger work performed through the action from later work that uses its result. Use [B.1.5.EW](spec://ai.lev/fpf-spec/contract/B-1-5-EW#root) to recover unclear connections between the action, its constituents and the larger work, and [B.1.5.RS](spec://ai.lev/fpf-spec/contract/B-1-5-RS#root) when replacing the action can affect another use. Follow a later result handover separately when it can change the proposal. Stop following the connections when further detail cannot change this continuation on the available basis.

Compare with continuing as at present. Thinking, obtaining evidence, explaining the advice, deciding and making the change can burden different people and resources. Include already committed work and other proposed changes in the same interval: two worthwhile changes can exceed shared capacity together. DUA supplies this comparison and returns to [C.11.CRC](spec://ai.lev/fpf-spec/contract/C-11-CRC#root) when a finite comparison is missing. Offer only the result whose contribution warrants that burden; explain its decisive conditions in the recipient's working language. A useful local answer can end the inquiry without a pattern recommendation or a record of refusal.

### COMMUNICATION-FOR-USE — Make communication useful, then learn from what happens {#communication-for-use-make-communication-useful-then-learn-from}

- **Situation:** A report, model, message, or answer seems clear, but its intended use and evidence are unclear, including whether its producer can use it later.
- **Question:** Who should understand or do what with it, what evidence is enough, and what should change if that use is not achieved?
- **First useful result or blocker:** A supported decision to keep or repair it, change prerequisites or a future use, or stop, with evidence, causation, and permission limits.
- **Start with:** Use `A.2.9` to judge the communication against what its recipient should understand or do. Distinguish the act from its wording and medium, and interpretation from response, later action, world change and causal contribution. For the repair question that arises, use `A.6.3.CR` for wording, `A.6.3.RT` for representation, or `A.6.3.NAR`/`E.17.EFP`/`E.24.PUB` for narrative, explanation or publication. Use `A.10` for evidence, `C.28` for causation and `C.11` to compare repair options only when needed. A repair may change prerequisites, medium, interaction or future use. Check authority, consent and admissibility separately.
- **Stop or return:** Stop when the named use has enough support or a blocker is explicit. Preserve the earlier intended use when interpreting the response; revise a future use when warranted. Response or silence alone proves neither meaning, success, causation, authority, consent, nor permission.

### RESULT-TO-NEXT-MOVE — Route an obtained result to the next probe or option {#result-to-next-move-route-an-obtained-result-to-the-next-probe}

- **Situation:** A DPF or project calls something information gain, learning progress, or novelty, or has articulated a result from an earlier cue, and wants to use it to choose the next probe or option.
- **Question:** What result actually exists, and which downstream question, if any, is current?
- **First useful result or blocker:** The direct result plus the first needed reliance disposition, characterization, possibility-space claim, configuration-relative comparison, `ChoiceResult`, or missing basis.
- **Start with:** Name the obtained result and use its direct pattern. Use `E.10.LRN` when *learning* hides the result; separate ambiguous claims and return each to its direct pattern. Continue to `A.10` only for actual reliance, `C.17`/`C.18` only for characterization or space change, `C.11.CRC` only for a missing finite realizable-configuration comparison, and `C.11` only for a live choice.
- **Stop or return:** Stop when the present question is answered and before every non-current question. Observations, objectives, and characterizations retain their identities. Route the result articulated from a cue through its direct pattern; if its `A.16.1` cue pack remains current as a source or provenance, retain it separately.

### ACTUAL-TEMPORAL-STRUCTURE — Recover what actually obtains before testing coordination {#actual-temporal-structure-recover-what-actually-obtains-before}

- **Situation:** A cycle, onset list, trace, notation, or geometry is called rhythm, but may be a prescription, representation, Method unfolding, or account rather than what obtains.
- **Question:** Which subjects and relations support the selected structure, what grounds it, and is a coordination trial useful now?
- **First useful result or blocker:** A.22-selected structure and grounded C.2.1 account—or missing bearer, relation, observation, or grounding. Keep future specifications and representations separate. For a selected coordination trial, add direct relations, conditions, observations, and next decision or stop.
- **Start with:** Begin with actual changing subjects and their use. Recover changes, Work parts or a continuous carrier, plus obtaining relations; use A.3.4/A.15.1 for change or Work and C.27.TA for the temporal claim. Use A.22 to select one structure and C.2.1 to ground its account. Distinguish structure, account, future specification, representation, Method unfolding and Work; periodicity, onsets, notation or geometry alone establish no structure. For coordination, name bearers and direct relations. Only when a trial can change the decision and warrants its burden, compare feasible interventions, try one within bounds, observe, then decide or stop. Open specification, representation, decision, causal, trial or domain patterns as their questions arise.
- **Stop or return:** Stop when answered. Return when bearer, relation, constraint, grounding, intervention, or use changes; domain Methods stay in DPF.

### CONSEQUENCE-BEARERS — Find omitted Systems before closing a decision {#consequence-bearers-find-omitted-systems-before-closing-a}

- **Situation:** A consequence account for a decision or investigation may omit physical or operational wholes beyond its candidate bearer.
- **Question:** Which other Systems may undergo a relevant change, through what supported relation or still-modal path, and what next step follows for the decision or investigation?
- **First useful result or blocker:** A bounded consequence account with its focus, bearers or intended referents, obtaining or modal paths, changed characteristics, support, uncertainty, and material limit. A useful constraint, alternative, or explicit unknown can complete the answer; further discovery needs a worthwhile obtainable contribution.
- **Start with:** Use `A.1.CSD` for the focus and receiving decision or investigation. Trace obtaining relations separately from modal paths, challenge the boundary and recover the relevant wholes; use `A.1.SCR` only when a candidate's systemhood is load-bearing. Qualify each change and keep each bearer's changes and conditions distinct. Leave through the direct evidence, causality, comparison, domain or value pattern only when that stronger question is current. Select further inquiry by individual and combined contribution and burden.
- **Stop or return:** Return the smallest useful account with its material limit; it may change or hold open the named decision or investigation. Reopen when the focus, configuration, horizon, whole, relation support, bearer, observation, or receiving use changes.

### Practical-Use Cards {#practical-use-cards}

These cards offer a non-exhaustive set of optional routes for extended work with a pattern language, each selectable by its situation and intended result and composable only from contributions current in the actual case.

The keys only help navigation. Compare cards by the situation and intended result, then open the direct patterns needed in the actual case. Skip a contribution whose question is not current, and stop at the first useful result or blocker.

#### UNFAMILIAR-THEORY - Make an unfamiliar theory usable {#unfamiliar-theory-make-an-unfamiliar-theory-usable}

- **Situation:** A theory offers a useful construction or result, but you cannot yet assemble and interpret its application to your question.
- **Question:** How can you obtain the needed consequence and use it?
- **First useful result or blocker:** A worked application with an interpreted answer, or the missing operation, premise or correspondence that directs the next contribution.
- **Mantra:** Recover the question the theory helps answer. Connect its objects and rules to one case. Obtain the construction and reconstruct the decisive argument. Compare the corresponding operations when using another representation. Apply the consequence; use what suffices or identify the remaining question.
- **Start with:** `B.5.TU` for application construction. `B.5.RC` and `B.5.RA` supply construction and argument recovery, `A.6.3.RT` an operative expression, and `C.29.1` result transfer. Use `C.39` for a missing way.
- **Stop or return:** An adequate supplied result can enter where needed. Stop when its interpreted consequence answers the question. If a premise changes, follow its effect instead of repeating unaffected work.

#### PHYSICAL-RESULT - Connect physics, mathematics and computation {#physical-result-connect-physics-mathematics-and-computation}

- **Situation:** A team has physical, mathematical and programming knowledge, but cannot connect the contributions needed to produce a physical result.
- **Question:** Which missing contribution prevents the next engineering move?
- **First useful result or blocker:** An interpreted calculation, proposed realization or located failure in the physical account, computation or execution.
- **Mantra:** State the physical change sought. Construct the state and continuation needed to reason about it. Formulate the mathematical question and interpret its variables and operations. Obtain a result or computational procedure. Connect input preparation, system actions and output reading. Return to the physical question and repair the failed contribution.
- **Start with:** `B.5.MPC` to connect available contributions and select the missing one. `C.29` constructs mathematical correspondence; `C.29.1` tests result transfer; `C.29.2` constructs computation; `C.29.3` connects it to an executing system. Subject engineering supplies physical laws and mechanisms.
- **Stop or return:** Reuse ready contributions. Stop when the result suffices for the present decision. Reopen the contribution whose changed condition invalidates its use.

##### Expansion for PHYSICAL-RESULT {#expansion-for-physical-result}

**Divide the work.** Give the next participant the result, what it denotes and the assumptions needed to use it. For the robot in `B.5.MPC:5.1`, the physical contribution supplies the motion model; the mathematical contribution relates distance to motor increments; the computational contribution produces an integer command and its rounding bound; the realization contribution checks what that command makes the controller do. People and AI agents can take these contributions according to their capabilities.

Use `A.3.3` to construct a missing state account and `C.16` for a needed measurement relation. These are dependencies between results. A ready model or computation can be reused at its point of need. Slip can reopen the motion model, overflow the command representation, and changed timing the execution arrangement. A calculated displacement remains conditional on the model until actual motion is established.


#### ARCHITECTURE — Carry an outside need through structure and feedback {#architecture-carry-an-outside-need-through-structure-and}

- **Situation:** A system or another architecture subject must produce an outside result, but its pressure, options, decision, or realized feedback is unclear.
- **Question:** What missing architecture result prevents the next useful decision or action?
- **First useful result or blocker:** One clear architecture question, candidate comparison, decision, or exact missing fact or constraint.
- **Mantra:** Start with the outside change and who relies on it. Name the subject and pressure; separate facts from intended constraints; compare plausible structures; choose what the current decision needs; check what the realized structure produces; reopen when use, evidence, or structure changes.
- **Start with:** `C.32.P2S`, then the pattern for the current question in `C.30`, `C.32`, `C.32.PAD`, or `C.30.AD`.
- **Stop or return:** Stop when the first result makes the architecture work reviewable. The card is not a compulsory lifecycle.

#### PRACTICE-ARCHITECTURE — Develop a practice without collapsing its structures {#practice-architecture-develop-a-practice-without-collapsing-its}

- **Situation:** Methods, Work, capabilities, providers, descriptions, tools, and cultural change do not align one-for-one in a practice.
- **Question:** Which relations must be reconciled for the practice to become usable or improve in representative Work?
- **First useful result or blocker:** One readable synthesis, one bounded development action, or the exact missing Work case, relation, or transfer evidence.
- **Mantra:** Start from representative Work and its needed result. Keep Methods, Work, capabilities, providers, descriptions, tools, and cultural processes distinct; compare the structures that conflict; develop the limiting capability; test transfer in real Work; return when practice, provider, evidence, or style changes.
- **Start with:** `C.32.MWA`; use `E.23.CDI`, `E.23`, or `C.36` only for the question actually opened.
- **Stop or return:** Stop when the synthesis or transfer result answers the decision. A practice description is not the practice or performed Work.

#### WORKING-DOCUMENTS — Make a document answer one use {#working-documents-make-a-document-answer-one-use}

- **Situation:** A document is requested, but its label does not reveal the use it must support.
- **Question:** Do you need to check one view, reuse related views, show the same subject differently, see enough structure, compare named sources, or use an architecture description in a decision?
- **First useful result or blocker:** A checked view, a reusable viewing approach, another presentation of the subject, an account of sufficient or missing structure, a source comparison, the architecture-description result needed now, or the exact blocker.
- **Mantra:** Name who will use the document and what it must support. Check one view; prepare recurring views; show the subject another way; expose enough structure; compare sources; or use a description in architecture work. Keep document, subject, decision, and performed Work distinct. Stop when the needed result exists; return when its use or content changes.
- **Start with:** `E.17.0` for one viewpoint; `E.17.1`/`E.17.2` for recurring use; `A.6.3.RT` for representation change; `C.33` for structural information; `E.17.ID.CR` for source comparison; `C.30.AD` for architecture-description use; otherwise use the direct pattern for the document result.
- **Stop or return:** Stop when that result answers the use. One file may carry several results without merging them.


#### OPTION-COMPARISON — Keep unlike option results distinct {#option-comparison-keep-unlike-option-results-distinct}

- **Situation:** Labels such as *build*, *buy*, *reuse*, *provider*, *internal*, *outsource* or *AI* need comparison; uncertainty blocks costly commitment; or advice demands costly or infeasible work.
- **Question:** Form complete ways, compare or retain candidates, govern a pool, prepare options for another chooser, choose now, or repair an evidence demand?
- **First useful result or blocker:** A complete-enough same-result way set, comparison or retained set, pool rule, prepared `OptionSet`, `ChoiceResult`, usable advice, answer to the blocking question or exact gap.
- **Mantra:** Name one result, use, situation, horizon, and acceptance basis. Turn labels into complete ways on one parity basis, keeping supported, proposed, and unknown premises visible. Compare or choose only when current; preserve worthwhile variants and gaps. For costly action, resolve only the uncertainty blocking commitment. Return when the result, basis, evidence, or use changes.
- **Start with:** `C.11.DUA` for a demand's contribution or feasibility; `C.38` for incomplete ways; otherwise `A.19.ECS`, `C.18`, `C.19`, `G.5` or `C.11` for the current question. For costly commitment, select the current check in `A.10`, `B.3`, `A.20`, `A.21`, `C.28`, `C.11` or `A.15.5`.
- **Stop or return:** Stop at the present question's result. Option descriptions establish neither choice nor capability, authority, Work, provision, delivery, acceptance or use.




#### PROBLEM-SHAPING — Stop at the earliest honest problem-side result {#problem-shaping-stop-at-the-earliest-honest-problem-side-result}

- **Situation:** Something matters, but the team may have only signals worth preserving, a direction for inquiry, a question about competing explanations, or enough clarity to accept a problem statement.
- **Question:** What can you honestly produce now: preserved signals, a routed direction for inquiry, an explicit question that contrasts possible explanations, or a problem statement ready for acceptance?
- **First useful result or blocker:** A preserved set of signals, a clear inquiry route, a question about plausible explanations, an accepted problem statement, or the exact missing anchor, route, subject, constraint, or acceptance basis.
- **Mantra:** Keep what was noticed before declaring a problem. Route the inquiry only when the signal has a stable anchor. Ask about explanations only when the open question and contrast are clear. Accept a problem statement only when the subject, constraints, unresolved relations, important distinctions, and basis can be stated. Stop at the earliest useful truth; return when its basis changes.
- **Start with:** `A.16.1` for a cue pack, `B.4.1` for routed cues, `B.5.2.0` for an abductive prompt, and `C.22.2` for an accepted `ProblemCard`.
- **Stop or return:** Do not force a cue into a problem. Open `C.22.PFR` only when whether the adverse relation obtains changes the next use.

#### IMPROVEMENT — Define better before repeating change {#improvement-define-better-before-repeating-change}

- **Situation:** A team wants to improve something but has not agreed what better means or how the changed version will be checked.
- **Question:** Which evaluation question, characteristics, scales, changes, and comparison make improvement reviewable?
- **First useful result or blocker:** One evaluation question, current assessment, bounded change, before-after comparison, or exact missing use, evidence, scale, or trade-off.
- **Mantra:** Name the entity, current state, and use that better must serve. Frame the question before choosing metrics; select characteristics, scales, and protected trade-offs; assess the current state; compare candidate changes; make only the supported change; evaluate it on the same basis; continue, stop, or change direction from that result.
- **Start with:** `E.22`, `A.19.ECS`, `C.16`, and `E.23` as their questions become current.
- **Stop or return:** Stop at the first missing prerequisite or useful comparison. Reopen when the entity, use, evidence, or scale changes.

#### WORDING — Repair language without replacing the project question {#wording-repair-language-without-replacing-the-project-question}

- **Situation:** A load-bearing sentence hides the subject, relation, kind, use, or nearby false inference.
- **Question:** What should the reader understand and do, and which distinctions matter for that use?
- **First useful result or blocker:** One plain repaired sentence, direct clarification, local naming result, or exact missing subject, sense, test, or reader use.
- **Mantra:** Recover the ordinary project sentence first. Name what it is about, what it claims, and who must use it; add ontological distinctions only where they change truth, understanding, or action; choose a durable name only when later use needs one; rewrite in plain technical language; check that a reader without private context can recover the intended claim and action; retain a guard only under F.19's full grounded-contribution test; return to the domain task.
- **Start with:** `F.19`; use `E.10` for unresolved FPF wording, and `F.18`, `F.0.1`, `F.9`, or the subject's direct pattern only when needed.
- **Stop or return:** Stop when the reader can understand the claim and carry out its intended use. Do not continue ontology work after the language problem is solved.

#### SOTA-PORTFOLIO — Move from a plural field to the cheapest useful result {#sota-portfolio-move-from-a-plural-field-to-the-cheapest-useful}

- **Situation:** A project needs the modern field of approaches rather than one popular answer and may later need maintained domain guidance.
- **Question:** What plural view is adequate now, and does the remaining problem call for reuse, a contribution, another product, a DPF or LPF, or no maintained result?
- **First useful result or blocker:** One source-linked SoTA view, live option set, reuse route, framework decision, or exact missing scope or maintenance basis.
- **Mantra:** Name the practical question, scope, freshness need, and rival traditions. Build a source-linked plural view; preserve disagreement, source-use limits and constructions; compare useful approaches; try cheaper reuse or contribution first; open a framework decision only for a recurring unmet problem; author and test the needed patterns; refresh when the field or use changes.
- **Start with:** `G.2`; add `C.18`, `C.19`, or `G.5` for the set and the E.4/E.9 authoring route only if a framework is selected.
- **Stop or return:** Stop at the first adequate maintained or one-off result. If allocation to familiar patterns loses a source’s construction, use `FPF.Preface:16.5` to identify the missing result, obtain it through the appropriate subject method and return to the original use. A source pack or proposal is not a framework by appearance.

#### SYSTEM-DELIMITATION — Separate parts, selected boundary, and crossings {#system-delimitation-separate-parts-selected-boundary-and}

- **Situation:** One System is recognized, but a decision mixes its parts and assembly with a chosen boundary, external participants, and relations that cross it.
- **Question:** Which facts, use-relative choice, crossings, and selected structure answer the decision?
- **First useful result or blocker:** One exact part or assembly fact, boundary choice, crossing relation, selected structure, or missing participant, predicate, constraint, or use.
- **Mantra:** Start with the recognized System and decision. Recover parts and assembly as facts; keep external participants outside the part list; choose a boundary only when alternatives matter; name every crossing by its own relation; select a joint structure only when organization changes the decision; reopen when identity, facts, use, crossings, or constraints change.
- **Start with:** `B.1.2`, `A.14`, and `C.13`; use `C.11`, `C.32.PAD`, the direct relation pattern, or `A.22` only when needed.
- **Stop or return:** Stop at the smallest result answering the decision. If system recognition is unresolved, return to `A.1.SCR`.


## Decide Whether FPF Fits {#decide-whether-fpf-fits}

Use FPF when ordinary discussion is no longer enough to keep work coherent. Typical signs:

- several teams, experts, tools, or AI agents share reasoning about the same work;
- the real-world test is slow, expensive, noisy, risky, or politically hard to repeat;
- different readers need different reports, dashboards, explanations, or decisions about the same underlying work;
- names, roles, responsibilities, options, evidence, or quality criteria are starting to blur;
- the team needs a current view of possible approaches, not just one recommendation;
- a decision is small enough to make now but important enough to leave a durable reason.

FPF is probably too heavy when the task is small, feedback is fast and cheap, the vocabulary is already stable, the decision will not be reused or audited, and a quick answer is enough.

FPF is mainly useful for people who have to keep difficult work understandable across boundaries:

- engineers and systems engineers working with complex products or operations;
- researchers building claims for inspection or reuse by others;
- platform and AI teams coordinating humans, models, tools, and approvals;
- safety, assurance, compliance, and regulatory leads who need visible evidence and responsibility boundaries;
- managers and product leaders comparing options, budgets, risks, and delivery promises without hiding trade-offs.

There are three common ways to use FPF:

1. Human-only: use it as a writing and review discipline for meetings, notes, decisions, and technical documents.
2. Mixed team: use it to keep specialists, managers, safety leads, and AI assistants aligned around the same work.
3. AI-assisted: attach or index the specification, ask for plain-language project help first, and use pattern names only when they make the answer easier to check.

FPF can help with the evidence and decision questions that remain as AI becomes more capable. AI can generate fluent options quickly, but projects still need to decide what counts as evidence, which option is being compared, who may rely on an answer, when a claim is stale, what remains only a guess, and what work is actually authorized. FPF helps make those boundaries explicit before a confident answer becomes an expensive mistake.

Core ideas in plain language:

- first name the project object under concern; FPF calls it a holon when its actual construction supports treatment as a whole with parts and as a possible part of a larger whole; use `A.1` to check a particular candidate;
- local teams may use local meanings; boundary-crossing work makes the translation relation explicit;
- the project object itself, its description, a dashboard about it, a decision about it, and the work done to change it are not the same;
- architecture is structure of that holon or project object in a context, not the diagram, document, approval, or plan about it;
- serious architecture work can move from problem pressure to candidate structures, selected structures, decisions, method and work, actual structures, and feedback;
- when the current question is which reusable way of doing changes, produces, derives, selects, controls, or preserves the project object under stated conditions, inspect `A.3.1 U.Method`; a strategy name, procedure text, program, plan, dated run, mechanism, or evidence record does not answer that method question by its label or form;
- to decide whether setting up and applying a selected apparatus, such as a model, is worth the cost for one use, inspect `C.19.2`; it tests the bounded application against the required result and guarantee. Use `C.39` when a missing obtaining explanation must be developed, or `C.40` when usable material needs variation and examination. Use `C.18` for archive or front claims, and `C.11` when two or more eligible alternatives make a local choice current;
- when a clear engineering claim produces a wrong action, identity, dependence, obtaining, responsibility, or projection consequence, inspect `A.7.1`; when current FPF uses produce incompatible consequences for the same receiving claim and scope, inspect `A.7.2`. In either case, keep the method episteme, admitted performer, dated work, the claim-specific result returned by the applicable pattern, and one result episteme distinct: the local disposition is a value in that result, not its kind, and `A.7.2` need not converge;
- when an accepted C.22.2 `ProblemCard` episteme must remain usable while the project selects a method, prepares or performs work, interprets a result, branches, stops, or returns after a changed assumption, inspect `E.18.1 P2W Problem-to-Work Carry-Through`; it carries the accepted problem-side distinctions into one next value or relation returned by the pattern that answers the current question rather than prescribing one universal workflow;
- when route-like positions, relations, or constraints change which continuation remains possible, inspect `E.18.3`: begin with the concrete thing being transformed, two recognizable places or states, the proposed connection or guard, and the current continuation question. An ordinary provisional explanation may answer it or stop with the exact missing predicate or occurrence rule, missing case fact, or unavailable information. Recover exact A.22/E.18 qualification and a separate demonstrative-slice claim only when qualification, comparison, publication, or stronger reliance is current; if no branch, connection, or constraint changes the continuation question, keep an ordinary route description;
- keep several options alive until the comparison is clear enough to choose;
- say what "better" means before optimizing or scoring;
- make trust depend on evidence, freshness, scope, and intended use;
- publish different views for different readers without changing the underlying claim;
- when explanation, reader-facing ordering, or narrative rendering of selected source structure is current, state what structure is preserved, deliberately coarsened, abstracted, omitted, or lost; name the source-return condition and any stronger neighboring claim together with the concrete definition, constraint, test, method, evidence rule, or assurance rule it uses;
- use mathematics or formal models when they clarify what structure is preserved, what is lost, and what can be checked;
- build domain or local FPF-grounded frameworks as dependents of FPF Core, not as silent rewrites of the Core.

## When Several Transformation Flows Form One Network {#when-several-transformation-flows-form-one-network}

Inspect `E.18.NET` when the current question joins independently identified transformation-flow structures through exact direct relation occurrences. Several stages, several paths, or several valuations of one flow do not make a network.

- **Build the builder.** A compiler-source-change flow, a bootstrap-compiler build flow, an application build flow, and a deployment-and-operation flow keep their own changes, work, positions, and local state. Recover the project's exact relation that says which executable compiler is used for the application build and its exact delivery relation to deployment. A selected tool-build network can itself be a member of a selected release network; follow a finite member path rather than inventing “level 2” and “level 3” kinds. Inspect `E.18.NET`; if the case is only one flow with several stages or valuations, stay in `E.18`.
- **Change a product and its production system.** Product-development Work changes and verifies the product definition; production-system-change Work redesigns, retools, and qualifies equipment; production Work makes units; operation supplies observations that may inform later product-development Work. Treat their transformation-flow structures as separately identified selected structures: the structures organize positions and exact relations but do not perform the Work. Keep the product and production system distinct, and recover the exact release, readiness, production, and observation relations needed by the current case. A selected product-development network and a selected production-system-change network can be members of a larger selected network without becoming one giant flow. Inspect `E.18.NET`; if only one architecture correspondence is current, use its direct architecture pattern instead.

When the immediate question is whether dated Work actually occurred or whether an entity was actually produced, leave the network overview and apply the tests in a finite order. First A.13 recovers every actual performer System's core: exact admitted System, local agential kind and criterion, classification, obtaining assignment for the scope, working situation, and window, and adequate core evidence; add a characteristic profile only when conditionally consumed. Next `A.15.1` independently admits one `U.Work` occurrence from the exact performance history, at least one Method actually followed, temporal extent, and at least one obtaining locally declared containing-System relation. That admission neither assumes nor requires F.6. Only afterward, when the receiving use needs precise assignment-bound performer attribution, F.6 tests `performedUnderAssignment` through the same obtaining A.13 assignment, direct case fact, holder equality, declared species and participants, and coverage. If that relation is unresolved, retain the admitted Work and lower only the attribution. A compact attribution sentence may omit an assignment identifier that its receiving use does not need; the omission changes only the sentence, not those facts. A log, ticket, or record creates neither Work nor attribution. After that Work and the required participant facts are exact, `A.15.PROD` separately tests the Work's participation in producing the entity, the start of that entity's identity, and production completion. Missing agency basis, Work granularity, production-participation predicate, identity-specification or inception basis, completion criterion or applicability, boundary or composition facts, or required substrate is a branch-local blocker. Actual change, output or result, identifier allocation, evidence, delivery, and acceptance remain separate claims and none proves those three production claims by itself.

## Perform several levels of work through one action {#perform-several-levels-of-work-through-one-action}

While adding an amount to a customer's running total, an agent can be calculating that total and preparing the report that contains it. These are related descriptions of the work being performed through the action. The report can still be unfinished. Earlier data collection supplies an input; it need not be taking place during the addition.

Use `B.1.5.EW` when you cannot explain this vertical: recover the constituent operations, the encompassing work and the conditions that connect them. Stop expanding where the practitioner can perform the needed contribution or obtain it from another agent. Check that the necessary capabilities and shared resources fit together. Knowing the final procedure does not supply an unlearned operation in the middle.

If the report must now identify the first chronological crossing of a limit, preserving the final total is insufficient. Use `B.1.5.RS` to compare a proposed replacement with the requirements of each receiving use; restoring order or changing the procedure may be necessary. `A.22.CGUS` helps distinguish a continuation that can be performed now from one whose constituent capability or resource conditions are missing. A feasible practice or preparation step may remain available while the whole performance is not.

## Recover a lost path from outside use to recursive builders {#recover-a-lost-path-from-outside-use-to-recursive-builders}

Use this guide when the team has recovered or is explicitly proposing one project system-of-interest but can no longer show how a local result supports the expected outside change, release or runtime use, architecture, Work and change of that system, creator systems, and recursive build-the-builder branches. Open `A.1.STM` to locate the first unsupported result, select the particular pattern contribution that answers that claim, and state one next question or action or an exact stop.

Trace the dependencies backward from the release, runtime use, or outside change that matters now, stopping at the first unsupported answer. If the actual versus intended project system-of-interest or its project designation is unclear, apply `A.15.6` first to distinguish actual project Work, intended material, and project designation. Apply `A.1.SCR` to the recovered exact entity only when recognition under `U.System` remains load-bearing for the named decision.

## One-Minute Example {#one-minute-example}

A platform team asks:

> Should we buy, fine-tune, or build an agent stack for our product?

Without FPF, the conversation often mixes architecture, vendor comparison, safety, evidence, budget responsibility, user value, and implementation planning. The loudest option can win before the team knows what is being compared.

With FPF, the first pass can become a small set of explicit project objects:

- holons in play: the product, the agent stack, and the team or toolchain that will change it are not the same holon;
- architecture flow: what problem pressure should become which candidate, selected, expected, and actual structures;
- comparison frame: which alternatives are in the candidate set;
- evaluation characteristics: cost, latency, controllability, safety, maintainability, time to first use, and other project-specific characteristics;
- evidence gaps: which test result makes commitment admissible;
- current decision state: whether the team is choosing now, keeping a selected set, making a project architecture decision, or doing more discovery;
- work and feedback: which method, readiness, and performed-work records establish that the selected structures were actually realized;
- reader reliance: what engineering, management, and assurance readers may responsibly rely on.

That same shape can be used for a factory modernization, laboratory protocol, construction design change, supply-chain decision, safety case, or research program. The point is not the AI topic; the point is one body of reasoning that can be reviewed, improved, and published without changing meaning on the way.

## What FPF Is {#what-fpf-is}

FPF is a pattern language for disciplined thinking in projects where ordinary prose, local expert judgment, or one-off AI output is not enough.

It helps teams:

- keep meanings stable when work crosses teams, tools, documents, and time;
- separate the project object being discussed from diagrams, dashboards, explanations, promises, decisions, and actual work;
- state what a claim can responsibly be used for before people rely on it;
- compare options without collapsing too early to one favorite;
- define quality criteria before improvement starts;
- keep evidence, assurance, decisions, and implementation work visible as different questions;
- carry architecture work from problem pressure to real structures and feedback instead of stopping at diagrams or decision prose;
- grow domain or local frameworks from FPF Core without silently changing Core meaning;
- repair confusing wording by first asking what the wording is doing in the project, not by swapping synonyms;
- leave each pass with one useful next result: a clearer question, a better name, a comparison note, an evidence gap, a safer document, or a reason to inspect a specific pattern.

## What FPF Is Not {#what-fpf-is-not}

FPF is not:

- a shrink-wrapped project methodology;
- a checklist bureaucracy;
- a quick-answer cheat sheet;
- a replacement for domain expertise;
- a demand to study the whole specification before useful work begins;
- a promise that every project needs every pattern.

FPF is most useful when the cost of semantic drift, premature convergence, hidden evidence gaps, weak architecture, vague quality, or unreviewable work is higher than the cost of using a disciplined pattern language.

## How to Use This Repository {#how-to-use-this-repository}

Start with one of the ordinary examples or one of the cross-pattern cards when it recognizes the current project question. A direct example is enough when one pattern can return the needed result. A card helps when the answer must retain several pattern contributions, checks, and returns. If no example fits, use the Table of Contents or ask an assisting agent to compare a small plausible set of direct patterns. The examples are not a list of all questions FPF can help with.

Use the `Preface` for the cross-cutting ideas. Its **Big FPF Storylines** section follows a report-review question through measurement, assurance, a shared-capacity condition and further inquiry. The Architectural Rationale there explains the choice of direct patterns, combinations and profiles, with shared source contributions and their limits. Use the selected pattern body for its `Solution`. Once one pattern is current, use `E.11.PUA` to follow that `Solution` to the smallest useful result or an honest missing-basis stop. Name a receiving use only when an actual continuation or later reliance is current. Use `E.11.PUR` when applicability, recommendation, coordination, or ordering among candidate pattern uses is the current question, or when an earlier result may already answer it. Keep an ordinary reversible judgement conversational; make it addressable only when a named later use needs that support.

If you use an AI assistant, attach or index `FPF-Spec.md` and ask for plain-language project help first. Let internal pattern names enter only when they make the answer more precise.

A good first prompt is:

```text
You have the FPF specification as a file.
Help me with this current project question:
[short project description and question]

Use plain language for engineer-managers. The Readme examples are clues,
not a list of the questions FPF allows. If one direct pattern can answer
the difficulty, start there. If the answer needs several pattern
contributions, give me a short attention map and open only the
contributions whose questions are current.

First give one useful result for the situation, or an honest blocker.
Then name the project question that result answers and any missing fact,
rule, evidence, or authority needed before a truthful answer is possible.
Add PatternIDs after the plain explanation so I can inspect the direct
Solutions and checks. Stop when the current question is answered; do not
turn the example or card into a whole-project plan.
```

## License and reuse {#license-and-reuse}

The original FPF and DPF content by Anatoly Levenchuk, including the Engineering DPF Suite and Narrativization DPF, is available under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/): you may share and adapt it, including commercially, with attribution, a license link and an indication of changes. See the [licensing scope](https://github.com/ailev/FPF/blob/main/LICENSING.md) for the full notice and third-party and software boundaries.

You choose the license for your own original DPF or LPF. Using FPF methods or its publication form does not impose CC BY on your work. When sharing licensed FPF or DPF text under CC BY 4.0, preserve its attribution and comply with the license. Where your use needs no copyright permission, including under an applicable exception, these conditions do not apply. The license has no ShareAlike requirement.

## Citation {#citation}


If you use FPF, please cite:

```text
Levenchuk, Anatoly. First Principles Framework (FPF).
GitHub repository: https://github.com/ailev/FPF
```

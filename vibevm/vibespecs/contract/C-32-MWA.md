# C.32.MWA - Practice Architecture Synthesis from Several Structures {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Tech-name:** `PracticeArchitectureSynthesisFromSeveralStructures`
> **Plain-name:** build one usable practice architecture from several structures that do not line up one-for-one
> **Type:** Method-description pattern under `C.32`
> **Status:** Candidate
> **Normativity:** Normative unless marked informative

## C.32.MWA:1 - Problem frame {#problem-frame}

Use this pattern when several accounts describe one professional practice through different structures—for example Methods, performed or planned Work, subjects, descriptions or models, capabilities or providers, and cultural change—and those structures do not line up one-for-one. Use it only when a current decision needs one coherent practice-architecture answer across them.

The primary working reader is an architect, methodologist, practice designer, or domain-framework author who has already found useful source material but cannot safely copy its table, stack, lifecycle, or diagram as the practice architecture.

**First useful move.** Say whether the practice is obtaining or possible-future. In plain terms: is representative Work actually being performed, or is the practice still being designed? Then write the architecture question in one sentence and list only the structures that can change its answer.

**What goes wrong if missed.** A source layout is mistaken for the practice. A list becomes levels, a procedure becomes a hierarchy, simultaneous contributions become a sequence, a model becomes the thing modeled, or a future design acquires fictitious performed Work. A local repair may also look successful only because its unresolved burden moved to another structure or scope.

**What this buys in practice.** The reader gets a short, usable account of the practice, the selected structures and relations, their correspondences, the main conflict or moved burden, and the alternative that changes the current decision. The account can remain ordinary prose; a table or symbolic form is optional assurance.

**Not this pattern when.**

- Use the direct Method, Work, subject, description, capability, provider, or cultural-change pattern when only one such claim is unclear.
- Use base `C.32` when the need is a palette of architecture candidates for one already grounded architecture question, rather than one coherent practice-architecture answer from several non-isomorphic structures.
- Use `C.30.ILC` and `C.32.MLAO` when an already recovered cross-scope conflict or residual is the main subject.
- Do not use this pattern for one clear Method decomposition, one procedure order, a carrier index, a universal level stack, a mandatory record schema, domain filling, product-roster generation, or lifecycle design.
- A practitioner can use this Method to prepare evidence for a framework or project decision. Making that decision, establishing a product, publishing a description, or realizing a future practice remains separate work.

For the smaller question of what encompassing work is being done through one current action, start with **B.1.5.EW**. It can expose a missing constituent or a changed condition without requiring this full synthesis. Use **B.1.5.RS** when the difficulty is preserving encompassing uses while replacing one constituent. Return here when the answer depends on several structures that do not correspond one-for-one.

The result is a **practice-architecture synthesis** for the named use. That phrase names an ordinary working description, not a new root kind. The practice, its Methods and Work, participating Systems, and its description remain different things.

## C.32.MWA:2 - Problem {#problem}

Professional-practice sources commonly mix several useful accounts. One may show Method order, another Work participation, another organizational or technical subjects, another capabilities and providers, another descriptions or models, and another cultural generation or retention. Their rows can look aligned while referring to different wholes and relations.

Three failures follow.

1. **Layout substitution.** The source's visible order or nesting is copied before the practitioner knows whether it means Method composition, Work order or overlap, subject composition, model grouping, provider dependency, cultural scale, or only chapter order.
2. **Present/future substitution.** A possible-future practice is described as though a representative Work occurrence had already happened, so the architecture gains evidence it does not have.
3. **Local-success substitution.** A candidate resolves one visible conflict but hides the residual or burden it moves elsewhere. The account reports the gain and loses the trade-off.

A fourth failure appears only in some uses: a live product-boundary question is reduced to one favored publication arrangement, or a product comparison is forced into an architecture question that does not concern product identity. Both errors confuse a conditional comparison with a universal step.

## C.32.MWA:3 - Forces {#forces}

| Force | Tension to hold |
| --- | --- |
| **One answer vs several structures** | The decision needs a coherent account, while the useful structures may remain non-isomorphic. |
| **Actual practice vs prospective design** | Obtaining Work offers dated evidence; a possible-future practice needs a truthful realization and later-test account instead. |
| **Precision vs readable entry** | Exact kinds and relations prevent false claims; notation-first prose can make the Method unusable to the practitioner who needs it. |
| **Candidate breadth vs proportional effort** | The first source layout is rarely enough; an unlimited candidate search can delay the decision without changing it. |
| **Local gain vs moved burden** | One structure can improve while another inherits cost, delay, evidence burden, loss of control, or unresolved residual. |
| **Project choice vs cultural change** | A project can deliberately choose or change an arrangement; distributed generation, transmission, selection, retention, and loss are different claims. |
| **Reusable Method vs domain filling** | The action sequence transfers across domains; actual domain Methods, institutions, evidence, constraints, and cases remain with the receiving domain. |

## C.32.MWA:4 - Solution {#solution}

Build one readable synthesis from the relations supported by the current case. Keep the following eight actions in order as an attention aid, not as a claim that the practice itself is one eight-stage process.

### C.32.MWA:4.1 - Eight actions {#eight-actions}

1. **Choose a truthful entry.** For an obtaining practice, anchor one independently admitted representative performed Work occurrence and the useful result at stake. For a possible-future practice, anchor an intended-use case, `WorkPlan`, or another correctly typed prospective account; state what would realize it and how later representative Work would test it. Do not invent performed Work.
2. **Name the subject and participants.** State the subject under discussion (`EntityOfConcern`) and the actual kinds of the participants before classifying rows or positions. A source word such as *practice*, *layer*, *role*, *model*, or *provider* does not settle those kinds.
3. **Generate genuinely different organizations.** Prepare alternatives that differ in a way that can change use or fail on different cases. When NQD is the current generation test, retain NQD-distinct candidates: their novelty is not a relabeling, their use-value preserves the declared constraints, and their diversity exposes different failure modes. Do not accept the source's first layout as the option set, and do not turn NQD into one scalar score.
4. **Recover each relation actually used.** In ordinary words first, state whether the source claim concerns Method composition or order, Work parthood or overlap, a subject relation, description or model use, a capability or provider dependency, cultural dynamics, or another admitted relation. Use the pattern that defines or constrains that relation when the claim matters to the answer.
5. **Separate practice from description.** Keep obtaining practice wholes and relations distinct from descriptions, models, views, and coarse-grained accounts. State their correspondence and the distinctions each description preserves or loses.
6. **Reidentify a whole when needed.** Use `B.2` when the previously identified Method, Work, System, or Discipline whole cannot carry the current claim. Reidentify a selected structure under `A.22`'s four identity discriminators when the current claim requires a different selected structure. Do not keep the old identity merely to preserve a neat stack.
7. **Compare conflict and moved burden.** Expose conflicts between candidate structures. For every apparent local repair, ask what residual, constraint, cost, evidence burden, delay, or loss moved to another structure or scope. Compare the alternatives against the named architecture question, not against visual tidiness.
8. **Keep deliberate and distributed change distinct.** Separate a project's architecture choice or intervention from cultural generation, transmission, recognition, selection, rejection, retention, and loss. A project can influence those processes without controlling or proving them.

### C.32.MWA:4.2 - Short working result {#short-working-result}

Write the first result as a short account that another practitioner can use without decoding a private ontology. This outline is a writing aid, not a mandatory schema:

```text
Current architecture question:
Entry: obtaining practice / possible-future practice
Representative occurrence or prospective anchor:
Useful result at stake:
Selected structures and the relations used:
Practice-description correspondences and losses:
Genuinely different alternatives:
Main conflict and any moved residual or burden:
Alternative that changes the current decision:
Source-return or later-test condition:
```

A compact table can support this account. Symbolic predicates are optional assurance and belong after the readable explanation. The result stops at architecture evidence; comparison, selection, decision, publication, evidence, assurance, or gate claims use their own patterns when those claims become current.

### C.32.MWA:4.3 - Conditional product-boundary comparison {#conditional-product-boundary-comparison}

Only when product identity is the current architecture question, compare these four genuinely different arrangements:

1. one domain DPF;
2. independently maintained sibling DPFs;
3. direct use of FPF plus exact domain sources; and
4. a proposed common applied DPF.

For each arrangement, state the recurring practitioner problem, first useful result, independently useful boundary, sources and maintenance burden, and what another arrangement would leave hidden or duplicate. These four are comparison forms, not a selected product roster. When product identity is not the question, do not force this comparison into the Method.

### C.32.MWA:4.4 - Stop, lower, and reopen {#stop-lower-and-reopen}

Stop when the short synthesis identifies the truthful entry, selected structures and relations, important correspondences and losses, at least one genuinely different alternative, the main conflict or moved burden, and the next use. Do not keep adding views that cannot change the decision.

Lower the claim when the subject, representative occurrence or prospective anchor, relation, evidence boundary, or alternative is not recoverable. Preserve the useful source cue and return to the direct pattern or source instead of completing the architecture by guesswork.

Reopen when representative Work contradicts the synthesis, a future practice becomes obtaining, a new structure changes the decision, a moved burden becomes material, a direct source changes, or the product-boundary question enters or leaves scope.

## C.32.MWA:7 - Conformance Checklist {#conformance-checklist}

| Check | Passing observation |
| --- | --- |
| **CC-MWA-1 — Recognizable use** | @fact:CC-MWA-1 The opening names a current decision that needs one answer across several structures, plus an ordinary non-use boundary. @status:spec/work |
| **CC-MWA-2 — Truthful entry** | @fact:CC-MWA-2 The synthesis explicitly chooses obtaining or possible-future practice. An obtaining entry has representative performed Work; a prospective entry has an intended-use or plan anchor, realization condition, and later-test condition without fictitious Work. @status:spec/work |
| **CC-MWA-3 — Subject before layout** | @fact:CC-MWA-3 The subject and participant kinds are recoverable before source rows, levels, or positions are interpreted. @status:spec/work |
| **CC-MWA-4 — Candidate difference** | @fact:CC-MWA-4 Alternatives differ by decision use or unlike-case failure, not merely wording or picture layout; when NQD is current, novelty, use-value, and diversity remain distinct. @status:spec/work |
| **CC-MWA-5 — Relation recovery** | @fact:CC-MWA-5 Every relation used in the answer is stated by value and supported through its defining or constraining pattern when material. Order is not overlap; overlap is not parthood; co-use is not Method composition. @status:spec/work |
| **CC-MWA-6 — Practice-description separation** | @fact:CC-MWA-6 Practice wholes and relations remain distinct from descriptions, models, views, and coarse-graining; important preserved and lost distinctions are stated. @status:spec/work |
| **CC-MWA-7 — Whole reidentification** | @fact:CC-MWA-7 A Method, Work, System, or Discipline whole is reidentified when the old whole cannot carry the claim; a selected structure is reidentified under A.22 when the claim requires a different selected structure. @status:spec/work |
| **CC-MWA-8 — Conflict and moved burden** | @fact:CC-MWA-8 The main conflict is named and every claimed local improvement states any material residual or burden moved elsewhere. @status:spec/work |
| **CC-MWA-9 — Conditional product branch** | @fact:CC-MWA-9 The four product arrangements are compared when product identity is current and omitted when it is not; the comparison itself selects no product. @status:spec/work |
| **CC-MWA-10 — Deliberate/distributed distinction** | @fact:CC-MWA-10 Project choice and intervention remain distinct from cultural generation, transmission, recognition, selection, retention, and loss. @status:spec/work |
| **CC-MWA-11 — Usable result** | @fact:CC-MWA-11 A cold reader can recover the short synthesis, the decision-changing alternative, the next use, and the stop or reopen condition without reading symbolic assurance first. @status:spec/work |
| **CC-MWA-12 — Unlike grounding** | @fact:CC-MWA-12 At least two unlike cases test the Method, and a prospective case is used whenever the candidate claims it can synthesize possible-future practice. @status:spec/work |

## C.32.MWA:9 - Consequences {#consequences}

The Method preserves useful differences among Method, Work, subject, description, capability/provider, and cultural structures while producing one decision-ready account. It prevents source tables, lifecycle diagrams, and models from silently becoming practice ontology. It also makes future-practice claims and moved burdens inspectable.

The cost is a small amount of relation recovery and alternative construction before a clean diagram can be accepted. Some attractive source organizations will remain unresolved or will be retained only as descriptions. That cost is proportional: the first result is short, structures that cannot change the decision are omitted, and formal assurance is optional.

Receiving domains still supply their own Methods, institutions, evidence, constraints, providers, cases, and maintenance conditions. Reuse of this Method does not move those fillings into FPF.

## C.32.MWA:12 - Relations {#relations}

- **Builds on:** `A.3.1` for Method identity, `B.1.5` for Method order/composition and Work enactment distinctions, `A.15.1` and `F.6` for actual performed Work and attribution when claimed, `A.22` for selected-structure identity, `B.2` for whole reidentification, `C.30` and `C.30.AD` for architecture and architecture-description distinctions, and `C.36` for cultural-change relations.
- **Coordinates with:** base `C.32` for general architecture candidate synthesis; `C.17` and `C.18` only when NQD generation, novelty/diversity, archive, or front claims are current; `C.30.STRAT` before accepting level, layer, tier, stack, or similar source wording; and `C.30.ILC` plus `C.32.MLAO` when a conflict, residual, or moved burden needs its own treatment.
- **Provides a result to:** `E.4.PFAD` when several practice structures change a framework-architecture answer; `E.4.DPF` when those structures change DPF identity, scope, pattern organization, first use, or use of named results; `E.4.DPF.DA` when package adequacy needs the resulting two-way sequence-versus-simultaneity evidence; and `E.23.CDI` only when target-practice architecture must be recovered or compared before capability development.
- **Does not replace:** the direct domain sources and Methods, `E.4` product-family decisions, explicit comparison or selection, project architecture decision, `E.24.PUB` publication occurrence and availability, evidence or assurance, or the currentness and refresh patterns.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/A-3-1#root, spec://ai.lev/fpf-spec/contract/B-1-5#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, spec://ai.lev/fpf-spec/contract/A-22#root, spec://ai.lev/fpf-spec/contract/C-30-AD#root, spec://ai.lev/fpf-spec/contract/C-36#root. @status:spec/done
- @fact:USED-BY Used by: spec://ai.lev/fpf-spec/contract/E-4-DPF#root, spec://ai.lev/fpf-spec/contract/E-4-PFAD#root, spec://ai.lev/fpf-spec/contract/E-23-CDI#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-3-1-MR#root, spec://ai.lev/fpf-eng-adm/contract/ADM-1#root, spec://ai.lev/fpf-spec/contract/B-1-5-EW#root, spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-eng-dtm/contract/DTM-8#root, spec://ai.lev/fpf-spec/contract/E-23-CDI#root, spec://ai.lev/fpf-spec/contract/E-4-PFAD#root, spec://ai.lev/fpf-eng-eam/contract/EAM-9#root, spec://ai.lev/fpf-eng-fin/contract/FIN-19#root, spec://ai.lev/fpf-eng-hcd/contract/HCD-4#root, spec://ai.lev/fpf-eng-mdpe/contract/MDPE-14#root, spec://ai.lev/fpf-eng-mdpe/contract/MDPE-21#root, spec://ai.lev/fpf-eng-mdpe/contract/MDPE-8#root, spec://ai.lev/fpf-eng-me/contract/ME-6#root, spec://ai.lev/fpf-eng-mnt/contract/MNT-15#root, spec://ai.lev/fpf-eng-oce/contract/OCE-16#root, spec://ai.lev/fpf-eng-ops/contract/OPS-19#root, spec://ai.lev/fpf-eng-psd/contract/PSD-16#root, spec://ai.lev/fpf-eng-str/contract/STR-14#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-32-MWA

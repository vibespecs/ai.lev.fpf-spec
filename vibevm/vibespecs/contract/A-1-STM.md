# A.1.STM - Find the First Unsupported Project Dependency (System-Thinking Long Mantra) {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Part A practitioner application pattern
> **Status:** Stable
> **Normativity:** Normative unless marked informative

**Plain name.** Use the system-thinking long mantra.

*Long mantra* and *attention map* are Plain names for a repeatable reminder and its readable dependency display.

## A.1.STM:1 - Problem {#problem}

A project can get every nearby statement locally right and still lose the long dependency. One team improves a component, another produces a builder, and another measures operation, yet nobody can show which supported relation carries those results toward use of the project system-of-interest. The gap is often hidden by a diagram arrow, the word *creates*, or a calendar sequence.

The opposite failure is to turn the reminder into a universal route. Then project Work becomes a network, a case becomes a slice type, a planned system is treated as already existing, and every arrow appears to be the same relation. A.1.STM keeps the long question visible while every local truth stays with its subject pattern.

## A.1.STM:2 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Whole-project coherence | A distant use must stay visible without making one pattern id or ClaimGraph stand for all intermediate subject assertions. |
| Outside before inside | Architecture is justified by a revisable external-use hypothesis, yet discovery and feedback may reopen that hypothesis. |
| Backward justification | Reading from value toward missing support is useful, but it is not temporal order or transformation direction. |
| Forward actuality | Work and changes must be traced through facts that obtain, not through planned arrows or shared names. |
| Local contribution | A team needs to know how its result matters without inventing a universal contribution relation. |
| Recursive builders | Build-the-builder reasoning must recur without a creator kind, fixed levels, or a generic `creates` edge. |
| Evidence and return | A supported answer may later become stale or fail; reopening should be local rather than restarting the whole map. |

## A.1.STM:4 - Solution {#solution}

1. **Choose by the final result.** Name the release, runtime use, or specific change expected outside the project system-of-interest. If a local result is current, say exactly what it is about and ask which supported fact connects it next to production or change, release, runtime use, or that outside change. If another long mantra better matches the final result, leave A.1.STM.
2. **Place supported answers and the current scope.** Put only answers supported by named facts, observations, decisions, or results in the matching regions. At project level, name the admitted E.18.NET selection and its exact use question; before admission, keep a Plain provisional map and name the missing member, relation occurrence, or endpoint binding. In neither case call the network project Work. For one current case, state only four things in ordinary language: the exact subject or claim; the bounded references and direct claims needed to answer this closure question; the separately governed closure basis; and one named downstream receiving use that remains outside the closed case. Use A.15.6 to choose any technical reference form the case actually needs; do not copy those forms here. Keep plans, descriptions, Methods, Work, systems, changes, relations, evidence, and assurance distinct; do not turn this placement into a dossier or record schema.
3. **Find the first unsupported dependency.** Read backward from the final result and choose the earliest missing, stale, disputed, or unsupported answer that blocks the next dependency. *First* means logical firstness, not calendar firstness.
4. **Use one subject pattern.** Perform the working move described by the pattern whose `Use this when` accepts the missing question, and retain the resulting assertion or named stop. Do not copy its `Solution` into this pattern.
5. **Return only what the next use needs.** Put the answer back in the map. Select an E.18.NET network only when its members, relations, constraints, use frame, and endpoint bindings are grounded. Usually return the individual answers. Select another A.22 structure only when one named later task must reuse their organization as one thing and all four identity discriminators pass. Otherwise keep the direct plurality or Plain provisional map.
6. **Trace forward and test.** Follow actual Work, production and identity facts, later changes, participation in use, and environment-side changes through their subject patterns. Repeat for each relevant builder branch. Bind evidence to the claim it supports; stop at the first unsupported direct link and reopen only the smallest affected earlier answer.

Four orders remain separate throughout: the order used to teach the map; the logical dependency read backward; planned or actual Work order; and the subject relations that obtain. One ordering establishes none of the others.

## A.1.STM:8 - Conformance checklist {#conformance-checklist}

| ID | Check |
| --- | --- |
| `CC-A1-STM-1` | @fact:CC-A1-STM-1 The intended final result and the first unsupported logical dependency are readable without decoding a technical record. @status:spec/done |
| `CC-A1-STM-2` | @fact:CC-A1-STM-2 Expected outside use and the project-system boundary are stated before internal architecture is justified; the actual runtime transformation of an exact environment or input referent and any system participation remain separately governed, and feedback may reopen the earlier hypotheses. @status:spec/done |
| `CC-A1-STM-3` | @fact:CC-A1-STM-3 Project system-of-interest identity, project designation, system-role-kind interpretation, and system-role assignment remain separate. @status:spec/done |
| `CC-A1-STM-4` | @fact:CC-A1-STM-4 Project Work, an admitted project-level network selection or Plain provisional map, and one minimal case placement retain their own identities. @status:spec/done |
| `CC-A1-STM-5` | @fact:CC-A1-STM-5 Backward attention, forward actuality, didactic order, Work order, and direct subject relations are not substituted for one another. @status:spec/done |
| `CC-A1-STM-6` | @fact:CC-A1-STM-6 Every local answer is one exact assertion under its subject predicate, with the pattern retained only as a locator, or a truthful stop. @status:spec/done |
| `CC-A1-STM-7` | @fact:CC-A1-STM-7 A case states four things in ordinary language: the exact subject or claim; the bounded references and direct claims needed to answer this closure question; the separately governed closure basis; and one named downstream receiving use that remains outside the closed case. @status:spec/done |
| `CC-A1-STM-8` | @fact:CC-A1-STM-8 An admitted network has independently identified members, exact obtaining cross-member relations, applied constraints, a use frame, and complete endpoint bindings; otherwise the map stays provisional. @status:spec/done |
| `CC-A1-STM-9` | @fact:CC-A1-STM-9 Expected environmental effect, actual runtime transformation and system participation, production, identity inception, completion, later change, and use are separately grounded; required behaviour is not actuality, and no not-yet-existing system is transformed. @status:spec/done |
| `CC-A1-STM-10` | @fact:CC-A1-STM-10 Evidence is bound to its claim, assurance is limited to a named reliance use, and changed grounds reopen only the smallest affected answer. @status:spec/done |

## A.1.STM:10 - Consequences {#consequences}

**Benefits.** Teams can locate a missing long-range dependency. Local results remain usable, builder recursion remains visible, and a missing relation stays an explicit stop rather than becoming a convenient arrow.

**Costs.** Practitioners must name the final result, keep several kinds of order apart, and return to subject patterns for local truth. A provisional map may remain incomplete for a long time.

**Limits.** This pattern does not identify a system, designate a project system-of-interest, select architecture, admit Work or transformation, close a case, identify a TFS network, or establish evidence or assurance. It only governs how a practitioner uses the long attention map to find and return the next result.

## A.1.STM:13 - Relations {#relations}

- **Builds on:** the Plain long/local boundary in Preface; `A.1` and `A.1.SCR` for exact system recognition; and `A.15.6` for project system-of-interest designation, actual project Work, and subject- or claim-centred case recovery.
- **Coordinates with:** `C.32.P2S` and the C.30 family for outside-use-to-architecture reasoning; `A.3.4` and the patterns for exact dynamics, interaction, causality, participation, assignment, Method, and Work claims in runtime change and system participation; `A.2` and `A.2.1` for system-role-kind interpretation and assignment; `A.3.1`, `A.12`, the A.15 family, `A.15.PROD`, `A.15.5`, and `A.21` for Method, Work, production, identity, readiness, and gates; `E.18` and `E.18.NET` for TFS and project-level network selection; `A.15.6` for the minimal case recovery and closure boundary; `A.10` and `B.3` for evidence and assurance; `A.1.CSD` when the missing answer is which other Systems may undergo relevant changes; and `C.28` only for actual causal-use claims.
- **Optional demonstration:** `A.22.CGUS` may govern a separately admitted demonstrative unfolding slice. Ordinary use of this long mantra requires no CGUS, F.17 row, durable card, or registration.
- **Does not replace:** any direct pattern named above. A.1.STM returns that pattern's result or stop to the attention map and defines no world-side predicate.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: Preface, spec://ai.lev/fpf-spec/contract/A-1#root, spec://ai.lev/fpf-spec/contract/A-1-SCR#root, spec://ai.lev/fpf-spec/contract/A-15-6#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-32-P2S#root, spec://ai.lev/fpf-spec/contract/C-30#root family, spec://ai.lev/fpf-spec/contract/A-2#root/spec://ai.lev/fpf-spec/contract/A-2-1#root, spec://ai.lev/fpf-spec/contract/A-3#root/spec://ai.lev/fpf-spec/contract/A-15#root families, spec://ai.lev/fpf-spec/contract/E-18#root/spec://ai.lev/fpf-spec/contract/E-18-NET#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/C-28#root, spec://ai.lev/fpf-spec/contract/A-22-CGUS#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-SCR#root, spec://ai.lev/fpf-spec/contract/A-15-6#root, spec://ai.lev/fpf-spec/contract/A-6-P#root, spec://ai.lev/fpf-spec/contract/C-32-P2S#root, spec://ai.lev/fpf-spec/contract/E-18-NET#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-1-STM

# C.32.FAIL - Architecture Failure Recognition and Repair {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural subpattern under C.32
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

## C.32.FAIL:1 - Problem frame {#problem-frame}

Use this pattern when a practitioner sees a recurring architecture-synthesis failure and needs to turn that warning into the smallest repair action over a named architecture object before evidence, assurance, selection, or decision claims are current.

Primary working reader: an architect or architecture-responsible practitioner who sees a warning sign during synthesis and needs the first architecture repair action, not a larger risk catalogue.

Typical entry cues:

```text
"This looks modular, but changes still cross hidden dependencies."
"The model is called a module, but the interface is weak."
"The platform promise hides exception growth."
"The search picked a winner, but the alternatives and losses disappeared."
"The graph looks convincing, but we cannot say which architecture object it repairs."
```

**First-minute use slice.** A team calls an ML model a module in a safety-relevant product architecture. Using C.32.FAIL, the practitioner names the architecture object under stress: a candidate module-interface relation for the described product holon. The blocked overread is: model file equals stable module. The first repair action is to recover interface behavior, admissible-use conditions, change policy, and evidence-decay boundary before using the model as a module. If a safety assurance claim is current, the case escalates only after that architecture repair is named.

The primary `EntityOfConcern` is one repair cue for one architecture object under stress. The cue is a working repair aid, not a risk register, assurance case, selection result, release argument, or decision object.

What goes wrong if C.32.FAIL is missed: failure language degenerates into a warning bank. The team can say what looks suspicious, but it cannot say which architecture object must be repaired or which pattern defines or constrains the next claim.

What C.32.FAIL buys in practice: a practitioner can convert a vague failure signal into one typed repair action, keep the repair near the selected structure, and stop before nearby decision, release, or governance claims expand the case.

Ordinary working move: convert the symptom into four fields: architecture object under stress, blocked overread, first repair action, and stop or escalation condition.

Adoption test: after using C.32.FAIL, a reader can see four things in the cue: the architecture object under stress, the blocked overread, the first repair action, and the pattern for the next question or stop condition.

Use another pattern when the current work is only lexical cleanup, evidence sufficiency, release, architecture description, MVPK publication face, comparison, selection, archive, front, selected-set result declaration, actual publication, local choice, or final architecture decision. Use C.32.FAIL only when the failure cue changes the first architecture repair action.

Common exits by claim kind:

- `C.30.P`, `A.6.F`, `A.6.M`, `C.31`, `C.32`, `C.32.MLAO`, and `C.32.CONWAY` for architecture or selected-structure repair.
- `A.19.CPM` for explicit comparison and `A.19.SelectorMechanism` for set-returning selection.
- `C.18` and `C.19` for archive, front, pool-treatment, or retained-stepping-stone claims.
- `A.10` for evidence, `B.3` for assurance, `A.20` for internal-constraint validity, and `A.21` for a named gate decision under an applicable profile, including a release gate when current. Release requirements remain with the patterns that define them.
- `C.30.AD` for architecture description, `E.17` for a source-backed publication face and source return, and `E.24.PUB` for the publication occurrence and audience availability.
- `G.5` for selected-set result declaration, `C.11` for local choice, and `C.32.PAD` for a project decision. For publication, keep the distinct E.17 and E.24.PUB uses just named.

The first useful output is `ArchitectureRepairCue@Project`. It is a working record for one repair action. It names the stressed architecture object and first repair; it is not a failure ontology, risk register, assurance case, release argument, selection result, or decision:

```text
ArchitectureRepairCue@Project:
  projectWorkOccurrenceRef?: U.EntityRef constrained to U.Work
  architectureRepairCueProjectUseRelationRef?: U.RelationRef defined by the exact repair-use or work-use pattern
  symptom:
  describedHolonRef:
  architectureClaimRef?:
  architectureConcern:
  intendedRepairUse:
  claimScopeRef?: U.ClaimScope
  qualificationWindowRef?:
  architectureObjectUnderStress:
  selectedStructureRef?:
  sourceCueRef?:
  failureEvidenceRefs:
  blockedOverread:
  firstPatternLocator:
  repairAction:
  sourceReturnCondition:
  stopCondition:
  escalationIfCurrent:
```

Here `@Project` is a compatibility and retrieval cue only. It establishes no project entity, composite-work identity, context, authority, viewpoint, or parthood. When the repair cue is genuinely used in one actual project, `projectWorkOccurrenceRef` identifies the exact composite `U.Work` and `architectureRepairCueProjectUseRelationRef` identifies the direct relation by which that exact project Work uses the cue. Any separately claimed repair Work and its own cue-use or work-to-change relation remain under their direct governors. The cue, the actual repair Work, the architecture object under stress, and the composite project Work remain distinct.

## C.32.FAIL:2 - Problem {#problem}

Architecture synthesis often fails before formal evidence or decision work starts. The defect is not only that a word is vague. The practical defect is that the architecture object under stress is missing or misread.

Most first-contact failures cluster into a few repair-entry families:

* a proposed bearer, module, platform, or universal substrate hides interface behavior, variation pressure, function bearing, evidence burden, or new coupling;
* a proxy result, generated artifact, architecture description, graph, dashboard, front member, or workshop favorite is used before the selected structures, losses, and pattern for the next question are named;
* one structure, function, system-role kind or assignment, responsibility, control relation, evidence relation, or Method step is improved while the synthesis frame loses the architecture characteristics and other structures that made the trade-off real;
* a current candidate is treated as a durable optimum, or ideality pressure deletes a bearer without naming the function still carried, the lost structure, and the new burden;
* an influence-source architecture and the transformed-side architecture content collapse into one claim instead of opening C.32.CONWAY and separating the changed referent, each obtaining C.30 architecture relation or modal `ArchitectureClaim`, any asserted direct influence occurrence, and any separately current actor, assignment, Work, or actual transformation facts.

These cues are useful only when each one is converted into a repair shape: symptom, architecture object under stress, first repair action, and stop or pattern for the next question.

```text
symptom -> architecture object under stress -> blocked overread -> first subject pattern -> repair action -> stop or escalation
```

Use C.32.FAIL for that conversion. It does not mint a local ontology of failure kinds.

## C.32.FAIL:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Fast recognition | Practitioners need short warning cues while the repair object is still unclear. |
| Object recovery | Source expressions and domain habits can hide the architecture object under stress. |
| Repair locality | The first useful repair action should change architecture handling, not open a broad audit. |
| Neighboring claim patterns | Evidence, assurance, gate, release, selection, and decision claims may be nearby but governed elsewhere. |
| Cue inflation | Warning rows can multiply without improving repair unless admission requires a concrete repair action. |

## C.32.FAIL:4 - Solution {#solution}

Convert the warning cue into an `ArchitectureRepairCue@Project`. Work in six steps:

1. State the symptom in ordinary practitioner language.
2. Name the described holon, architecture claim when one is current, concern, intended repair use, scope or qualification window when material, architecture object under stress, and failure evidence.
3. State the blocked overread that would lead the team astray.
4. Name the first subject pattern for the architecture object or lens relation.
5. Propose the smallest repair action that changes architecture handling.
6. State where to stop, or which neighboring pattern defines or constrains the next claim if another claim is already current.

Core repair families for a first repair-cue draft:

| Repair family | Symptom | Architecture object under stress | First repair action | Stop or pattern for the next question |
|---|---|---|---|---|
| Weak module-interface | A source-side bearer is called a module because it has a convenient boundary. | Candidate module-interface relation and selected structure boundary. | Recover interface behavior, admissible-use boundary, change policy, and interface-conformance witness. | Stop at repaired interface cue; module-interface structure claims belong to `A.6.M`, `C.30.ASV`, or `C.31` when current. |
| False platform | A reusable-structure promise hides variation pressure and local exceptions. | Variation structure, substitution policy, evidence scope, and exception boundary. | Recover variation slots, substitution rules, substitution-conformance checks, and exception-growth trigger. | Cross-scope residual work belongs to `C.32.MLAO` when current. |
| Hidden single winner | A comparison or generation result is treated as selected architecture. | Candidate palette and retained alternatives. | Rebuild the C.32 palette with candidate gain, loss, preserved structure, hidden structure, and source-return condition. | State explicit comparison under the A.19.CPM predicate, set-returning selection under A.19.SelectorMechanism, selected-set result declaration under G.5, local choice under C.11, and a project architecture decision under C.32.PAD. For publication, state the E.17 source-backed face and source return separately from the E.24.PUB occurrence and audience availability. |
| Proxy result or description as authority | A score, graph, residual vector, generated output, architecture-description artifact, or MVPK publication face is used to accept or prefer an architecture candidate before the selected structure and pattern for the next question are named. | Candidate architecture claim and selected-structure relation hidden behind the proxy, description, or visible result. | Recover the selected structure, source-side referent, view relation, or lens-output relation first. Use `C.29` for lens output, `C.30.ASV` or `C.30.AD` for view or description use, `A.19.CPM` for comparison, `C.11` for local choice, `A.19.SelectorMechanism` for set-returning selection, and `G.5` for selected-set result declaration. For publication, use `E.17` for a source-backed face and source return and `E.24.PUB` for the occurrence and audience availability. | Stop when the visible work product only orients repair; evidence claims belong to `A.10` and assurance claims belong to `B.3`. |
| Coordination cost displaced by responsibility change | A change in ordinary work organization or a responsibility relation improves local flow while pushing coordination into module interfaces, shared test, evidence, approval, or deployment structures. | Team or organization System and its relations; coordination relation; module-interface, evidence, deployment, Method or plan structure; and, only when current, local kind, separate System-classification judgment, assignment, enactor relation, and actual Work network. | Recover the shifted coordination cost and the structure under stress. If responsibility retargeting is claimed, name its direct predicate, old and proposed participants, and occurrence identity or return `missing-governor`; then decide whether the architecture repair belongs to `C.32.CONWAY`, `A.6.M`, or `C.32.MLAO`. | Route unresolved role wording through `E.10.ROLE`. Keep ordinary work organization, Method or plan structure, local kind, separate System-classification judgment, assignment, enactor relation, dated Work, and responsibility as separate branches under their subject patterns. |
| Temporal or control coupling | Named parts need brittle timing or control coordination. | Temporal relation, control relation, and affected work or evidence relation. | Recover the timing or control constraint and ask whether a candidate architecture change affects the selected structure. | Temporal adequacy claims belong to `C.27`, control or mechanism placement claims belong to the governing mechanism pattern, and flow-structure claims belong to `E.18` when current. |
| Evidence jump | The team asks for more evidence before naming the architecture repair. | Architecture object whose evidence relation may be stale, misplaced, or bearer-dependent. | Name the architecture repair first, then record the A.10 evidence relation, source-currentness relation, bearer, scope, and decision-use boundary. | Evidence relations belong to `A.10`, assurance to `B.3`, internal-constraint validity to `A.20`, and a named gate decision to `A.21` under an applicable profile. Release requirements remain with the patterns that define them. |
| Generated output as authority | A generated architecture-looking output is treated as carrying an authority relation for architecture adequacy. | Source cue, generated description, candidate selected structure, and evaluation boundary. | Treat the output as a source cue; recover source-side referent, selected structure, architecture-change kind, gain, loss, and human review boundary. | Use `C.32` for candidate generation and `C.30.AD` for generated-description use. For publication, use `E.17` for a source-backed face and source return and `E.24.PUB` for the occurrence and audience availability. |
| Single-structure synthesis | One selected structure is improved and called the architecture synthesis. | Synthesis structure map and architecture characteristic bundle. | Use C.32; name the other selected structures that must be coordinated and the architecture characteristics that make the trade-off real. | Stop at repaired C.32 palette, or open `C.32.MLAO` if the failure crosses scopes. |
| User function as architecture characteristic | A user-visible function is treated as the architecture quality being optimized. | Functional demand, architecture characteristic, and quality bundle boundary. | Recover the function through `A.6.F` or `C.30.ASV`; then name the architecture characteristic or `C.25` quality bundle separately. | Stop before comparison until function and characteristic occupy distinct fields. |
| Function with no feasible bearer | A function graph, workflow, use case, method step, or neural cell graph names a required function that no admitted bearer can perform under the current constraints. | Functional demand, candidate bearer set, module-interface relation, placement or deployment relation, resource access, control relation, and evidence burden. | Use `C.32`. Possible first repairs include adding or changing a bearer, splitting the function, changing placement or resource access, changing control responsibility, reducing demand, or rejecting the candidate. | Stop before comparison, G.5 selected-set result declaration, publication availability, assurance, or decision claims. |
| Static optimum | A front member or local winner is treated as durable optimum. | Evolution window, pattern for the next question result, front or archive relation, and reopen trigger. | Add evolution window, source-return condition, and pattern for the next question; keep C.18 and C.19 as retention or pool policy only. | Use `A.19.CPM` for comparison, `A.19.SelectorMechanism` for set-returning selection, `C.11` for local choice, `G.5` for selected-set result declaration, and `C.32.PAD` for an architecture decision. For publication, use `E.17` for a source-backed face and source return and `E.24.PUB` for the occurrence and audience availability. |
| Ideality shortcut | Having fewer bearers or fewer modules is treated as architecture improvement by itself. | Function-bearing allocation, selected structure count, and architecture characteristic bundle. | Recover the function-bearing transfer; name the removed or generalized bearer, the functions still carried, the new burden, and lost structure. | Use `C.32`; use `C.31`, `A.6.F`, `A.6.M`, and `C.19.1` when their claims are current. |
| Universal bearer as adequacy shortcut | A universal module or general substrate is treated as architecture adequacy or scale adequacy by itself. | Scale-amenability claim, module-interface relation, evidence burden, control burden, and safety or admissibility boundary. | Treat the proposed universal module or general substrate as a candidate bearer; require BLP scale window or waiver when scale advantage is claimed and record coupling, evidence, control, and source-return effects. | Stop before G.5 selected-set result declaration, actual publication, assurance, release, or decision claims unless patterns for the next questions are current. |
| Mismatch between architecture influence and transformed-side structure | An influence-source architecture is collapsed with transformed-side architecture content, a desired transformed-side structure is paired with no compatible influence-source arrangement, or an architecture or selected structure is treated as the changing actor. | The exact changed referent; each influence-source-side and transformed-side obtaining C.30 `ArchitectureRelation` or modal `ArchitectureClaim`; and the direct architecture-influence or correspondence occurrence only when independently governed and obtaining. | Open `C.32.CONWAY`; recover the two exact architecture sides, the direct influence kind and predicate or `missing-governor`, and then prepare influence-source-side, transformed-side, joint, or bounded-mismatch candidates. Add acting systems, assignments, Work, and actual transformation only through their subject patterns when those claims are current. | Use `A.6.M` only for module-interface repair, `C.29` only when structural similarity is claimed, and E.18.NET only for an independently selected network; a C.32.CONWAY frame or exact pair row is neither an actor, network, nor cross-flow occurrence. |

Admit a new repair family only when its row tells the practitioner what to repair first. A suspicious name alone is not enough; the row must name the architecture object under stress, the first repair action, and the stop or pattern for the next question.

**Stop condition.** Stop after the repair action, pattern for the next question, and source-return condition are named. Do not grow the cue into a risk register, evidence case, release argument, or final architecture choice.

**Lowering condition.** Keep the row as a C.32.FAIL repair cue only while the symptom, described holon, architecture object under stress, blocked overread, first subject pattern, repair action, stop condition, and escalation condition remain current. Lower the row to an observation when the architecture object is unknown, the repair action is missing, the first subject pattern is not named, or the symptom belongs only to evidence, assurance, release, description, publication, comparison, selection, choice, or decision work. Retire the cue when the repair action has been applied or the stressed architecture object is no longer current. Use `A.6.P` or `E.10` when the case is only source-expression recovery, `C.32` when candidate repair is current, `C.32.MLAO` or `C.32.CONWAY` when their residual or correspondence repair is current, and the named pattern for the next question when a stronger downstream claim is current.

## C.32.FAIL:7 - Conformance Checklist {#conformance-checklist}

| ID | Requirement | Purpose |
|---|---|---|
| `CC-C32.FAIL-1` | @fact:CC-C32-FAIL-1 The cue states a recognizable symptom in practitioner language. @status:spec/done | Keeps the pattern usable at first contact. |
| `CC-C32.FAIL-2` | @fact:CC-C32-FAIL-2 The described holon, architecture claim when current, architecture concern and intended repair use, architecture object under stress, failure evidence, and any material scope or qualification window are named. @status:spec/done | Prevents source wording or a generic context field from replacing object recovery. |
| `CC-C32.FAIL-3` | @fact:CC-C32-FAIL-3 The blocked overread is stated in one sentence. @status:spec/done | Makes the failure precise enough to repair. |
| `CC-C32.FAIL-4` | @fact:CC-C32-FAIL-4 The first subject pattern is named. @status:spec/done | Keeps architecture, lens, work, evidence, assurance, and decision claims distinct. |
| `CC-C32.FAIL-5` | @fact:CC-C32-FAIL-5 The repair action changes architecture handling. @status:spec/done | Prevents warning-only rows. |
| `CC-C32.FAIL-6` | @fact:CC-C32-FAIL-6 The stop condition or pattern for the next question is named. @status:spec/done | Keeps the cue lightweight and composable. |
| `CC-C32.FAIL-7` | @fact:CC-C32-FAIL-7 New cue rows name the architecture object, first repair action, and stop or pattern for the next question. @status:spec/done | Prevents warning-bank inflation. |

## C.32.FAIL:9 - Consequences {#consequences}

| Positive consequence | Cost or trade-off |
|---|---|
| Failure recognition produces repair action. | Many tempting warning rows are rejected. |
| Repair stays near the architecture object under stress. | The team may need to postpone evidence, assurance, or decision work. |
| Source expressions can be used as cues without carrying ontology. | Each cue must recover the described holon and selected structure. |
| C.32 candidate repair stays separate from final selection. | Selected-set result declaration, actual publication, or choice requires the pattern for the next question. |
| Generated or tool-derived architecture material can widen discovery. | Generated material must still recover source-side referent, selected structures, architecture-change kind, gain, loss, and human review boundary before candidate use. |

## C.32.FAIL:12 - Relations {#relations}

- **Builds on:** `C.32` for candidate palette repair; `C.32.CONWAY` for a synthesis frame or qualified pair connecting architecture influence with transformed-side architecture while keeping the changed referent, C.30 architecture relations or modal claims, direct influence occurrence, organization relations, local kinds, separate System-classification judgments, assignments, enactor relations, ordinary work or procedure organization, actual Work, direct responsibility relations, actual transformation, and any E.18.NET network distinct; `C.30` and `C.30.AD` for architecture relation, claim, and description boundaries; `C.30.ASV` for architecture structural views; `C.31` for module and interface architecture; `C.32.MLAO` for cross-scope residual repairs; `C.29` for mathematical-lens use; `E.17` and `E.24.PUB` for publication-face boundaries; and `A.6.P`, `E.10`, and `E.10.ROLE` for source-expression and role-word recovery.
- **Coordinates with:** `A.6.F` when function and architecture-characteristic wording is mixed; `A.6.M` for module-interface repair; `C.19.1` for a general scale-amenable bearer or Method; A.2/C.3 for a local system-role kind and any separate System-classification judgment; A.2.1 for an assignment species and occurrence; A.13 for every precise performer's core, A.15.1 for independent actual-Work admission, and F.6 only for current precise assignment-bound attribution; and the exact enactor, coordination, or responsibility predicate, or A.6.RCD `missing-governor`, when that direct route is absent. Use `E.10.ROLE` only for unresolved claim-bearing *role* wording. Ordinary work or procedure organization may remain ordinary. For other current claims, use the applicable exits in §1; `C.27` additionally governs temporal adequacy, `E.18` transformation-flow structure, and `C.32.P2S` reopened carry-through.
- **Patterns for the next questions after the repair cue:** Use the applicable next-question exits in §1 only after the architecture repair cue has named the object under stress and the repair action.
- **Boundary:** C.32.FAIL contains repair cues for architecture-synthesis failures. It does not decide final candidate selection, evidence sufficiency, assurance, gate passage, release, or an architecture decision.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-30-P#root, spec://ai.lev/fpf-spec/contract/A-6-F#root, spec://ai.lev/fpf-spec/contract/A-6-M#root, spec://ai.lev/fpf-spec/contract/C-31#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/E-10#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-32-MLAO#root, spec://ai.lev/fpf-spec/contract/C-32-CONWAY#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/A-19-CPM#root, spec://ai.lev/fpf-spec/contract/A-19-SelectorMechanism#root, spec://ai.lev/fpf-spec/contract/C-18#root, spec://ai.lev/fpf-spec/contract/C-19#root, spec://ai.lev/fpf-spec/contract/G-5#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/E-24-PUB#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/A-20#root, spec://ai.lev/fpf-spec/contract/A-21#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-30-P#root, spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-CONWAY#root, spec://ai.lev/fpf-spec/contract/C-32-MLAO#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-32-FAIL

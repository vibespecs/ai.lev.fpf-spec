# A.19.UNM - Normalize Coordinate Values under Declared Invariants (UNM) {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural (A)
> **Status:** Stable
> **Normativity:** Normative (unless explicitly marked informative)
> **Placement:** Part A / CN‑Spec cluster (A.19) / CHR mechanism-governing patterns
> **Boundary:** A.19.CN defines the CN-Spec fields that select normalization and comparability. This pattern defines the normalization operation and how it uses those fields.

**If someone says “we normalized”, ask (in this order):**
1) Which **`UNM_id`** (if applicable) and which **`NormalizationMethodInstanceId`** (and its validity window) was used?
2) Which **`NormalizationInvariant[*]`** were declared (i.e., *what is preserved*)?
3) Which **bearer, scope/window, reference or comparison basis, evidence, and intended comparison** were recorded, and does this use actually rely on an F.9 Bridge, kind relation, or plane relation?

**Mental model.** UNM applies a declared directed transformation from an input coordinate value (`CV`) to an output (`NCV`). State its domain, target and preserved or lost distinctions. An inverse, an equality-of-output class or an operation on those classes is a narrower result requiring its own conditions.

## A.19.UNM:1 - Problem frame {#problem-frame}

FPF needs a disciplined way to talk about **measurable slots** (coordinates/scales) such that engineers can reason about:
- **What it means** to compare values across charts, slices, bearers, or reference bases, and
- **Where the “meaning-preserving” transformations live**, so comparisons are lawful and explainable.

In practice, teams routinely face a mismatch between:
- values that look comparable (“they’re numbers”), and
- values that are not comparable without normalization—for example, because their units, scale types, reference planes, bearer or population assumptions, comparison bases, intended uses, or validity windows differ.

FPF’s CHR family explicitly separates stages (normalize → indicatorize → score → fold → compare → select). UNM is the *normalization* stage, and its job is to make “compare-on-invariants” explicit and auditable.

## A.19.UNM:2 - Problem {#problem}

Without an explicit UNM governing pattern:

1) **Normalization drifts into hidden places.** It gets embedded inside scoring, comparison, or selection, making admissibility and governance non-local.

2) **Comparability becomes rhetorical.** People say “we normalize” but cannot answer:
   *Which method? Which invariants? Which bearer, comparison basis, scope and window? Which evidence? Does the receiving comparison rely on an actual Bridge, kind relation, or plane relation?*

3) **Basis and relation changes become invisible.** Teams reuse normalizations for another bearer, comparison basis, source-local meaning, or reference plane without naming what changed or the relation on which the new use depends.

4) **Engineers cannot reconstruct the mechanism.** When UNM semantics are scattered, the pattern structure (problem/forces/solution) is lost, hurting didactic use by engineering managers.

## A.19.UNM:3 - Forces {#forces}

| Force | Tension |
|---|---|
| **Evolvability vs Usability** | Stable mechanism surface ↔ method families evolve; single place to read ↔ modular wiring. |
| **Semantic precision vs Cognitive load** | Formal invariants/quotients ↔ a mechanism description that engineers can act on. |
| **Governing-pattern discipline vs Cross-cutting reality** | UNM touches CN, CG, transport, and plane claims ↔ avoid “shadow specs” and duplicate centers of gravity. |
| **Trustworthiness vs Overreach** | “Normalization is legitimate” must be evidence-backed ↔ UNM must not pretend to define measurement meaning itself. |
| **Locality vs Reuse** | A normalized value is valid for a declared bearer, basis, scope, window, and use ↔ a later use may need a separately supported relation or a new normalization. |
| **Fail-closed safety vs Convenience** | Unknown/insufficient evidence must not coerce ↔ teams want “a number anyway”. |

## A.19.UNM:4 - Solution {#solution}

UNM declares directed normalization operations. For an admitted input in the selected transformation's domain, return its NCV and the preserved/lost distinctions needed by the receiving use. An undefined input has no normalization result. Use the additional branches below only when the receiver needs an inverse, classes, a class-level operation or a representative.

UNM is **not** a bag of algorithms. It is a **canonical semantic surface**:
- **Routing** lives in `CN_Spec.normalization` and `CN_Spec.comparability.mode`.
- **Evidence/calibration legitimacy** lives in `C.16 (MM‑CHR)`.
- **Method families** can be supplied by SoTA packs and wired via extensions, without mutating UNM’s surface.

### A.19.UNM:4.0 - Vocabulary (normative) {#vocabulary-normative}

**NormalizationMethodId.** A stable token naming a normalization method *kind*, used in `CN_Spec.normalization.methods`.

**NormalizationMethod.** The method *kind* (class) that defines:
1) its input/output domains, the directed transformation and the **invariants** it preserves (`NormalizationInvariant[*]`), with any distinctions it loses,
2) its **closure rules** (composition, and inverses where defined), and
3) its **validity rules** (admitted bearer, scope, qualification window, reference or comparison basis, and intended-use constraints).

**NormalizationMethodDescription.** An editioned epistemic description of a normalization method (bounds, validity region/window, scope constraints, and evidence links governed by `C.16`).
**NormalizationMethodDescriptionRef.** A ref to an editioned `NormalizationMethodDescription`, used in `CN_Spec.normalization.method_descriptions`.

**NormalizationMethodInstanceId.** A stable token naming a normalization method configured for specific coordinates in a base `U.CharacteristicSpace`, with a named validity window and (when required) evidence pins. One such configuration can be used by several distinct `apply` occurrences; this identifier does not identify a calculation invocation. Used in `CN_Spec.normalization.instances`.

**NormalizationMethodInstance.** That configured method, referenced by `NormalizationMethodInstanceId`. Its coordinate qualification and validity window are separate from the extent of a calculation that uses it.

**CV (CoordinateValue).** A raw coordinate value for a **named measurable slot** in a chart: conceptually `⟨slot_id, raw_value⟩` (plus any chart/slice scoping needed by the chart). UNM re‑parameterizes `CV → NCV` under declared invariants and validity constraints.

**NCV (NormalizedCharacteristicValue).** A normalized **value** for a coordinate (UNM does **not** “normalize characteristics”; it normalizes coordinate values under declared invariants).

**Directed transformation.** The selected method states its actual input domain D, target N and transformation rule. For a partial normalizer, D is the subset where a result is defined. An edge from x to its output does not supply a reverse edge. A relation-valued or uncertain output needs its declared result semantics; the function theorem below cannot be applied without a function and equality on its output values.

**`≡_UNM` (equality of normalization outputs).** For one fixed function `n:D→N`, define `x ≡_UNM y` iff `n(x)=n(y)`. Equality in N gives reflexivity, symmetry and transitivity on D. Thus the fibers form the set quotient `D/≡_UNM`. Inputs outside D have neither an n-value nor membership in this partition. This relation is distinct from the directed transformation graph.

**Operational quotient.** To inherit a total operation on classes, equivalent argument tuples must produce equivalent outputs. For a partial operation, its availability must also agree across equivalent tuples. Use the relevant equivalence on each input and output sort. A receiving query q is recoverable only when `x ≡_UNM y` implies `q(x)=q(y)`. Only after these tests may the equivalence be called a congruence for the named operations. A set quotient alone supplies no such result.

**Reversible chart change.** A declared inverse recovers the input on the transformation's stated image. A strictly monotone encoding on a totally ordered domain is injective and invertible on that image, even if the declared target contains other values. A merely monotone LUT may merge inputs. Repeated normalization or idempotence requires its own composable domain and law; it does not follow from the fibers.

**NormalizationInvariant.** A named invariant (e.g., unit alignment, polarity, reference plane) declared in `CN_Spec.normalization.invariants` and/or the selected `NormalizationMethodDescription`. Preserving the declared `NormalizationInvariant[*]` is the core admissibility claim for a normalization method instance.

**NormalizationFixSpec.** A declared policy selecting a representative of an already established `≡_UNM` class when the receiving use needs one. It does not recover which member was the actual input or restore a lost query answer. Bound via `CN_Spec.normalization.fix`; omit it when no class representative is needed.
**UNM_id.** An optional identifier in `CN_Spec.normalization.UNM_id?` selecting the UNM **mechanism instance** used by this CN‑frame. This is routing/governance; it is distinct from `NormalizationMethodInstanceId` (configured normalization method).
**ValidityWindow.** A named validity window attached to a `NormalizationMethodInstanceId`, bounding where/when the instance is admissible (no implicit “latest”).

**Relation and reuse boundary.** A normalized value remains tied to the exact normalization-method instance and edition, characteristic-space and CN-Spec editions, bearer, scope and window, reference or comparison basis, evidence, and intended comparison. Reusing it does not by itself establish a transfer relation. Cite an F.9 Bridge or a plane relation only when that relation actually obtains, and state the receiving use separately.
**Lexical discipline.** Name a UNM operation as normalization, re-parameterization or a coordinate mapping under its declared invariants. Use a specialized FPF `Map` designation only when its defining conditions apply; an ordinary mathematical mapping does not thereby assert that specialized kind or an F.9 Bridge.
Legacy κ‑notation for normalization is retired; do not re‑introduce it.

### A.19.UNM:4.1 - UNM operation declaration (normative) {#unm-operation-declaration-normative}

`UNM.IntensionRef` is the retained citation name for the exact A.6.1 declaration episteme presented here. It does not identify a generic family in place of that declaration. The CHR baseline selects its edition before use; the `normalize` stage resolves to the declaration-local `apply` operation below. Its four named input meanings, NCV result and eligibility guard come from that selected declaration.

A different realizer of the same declaration changes no suite member. A corrected layout or citation can preserve its C.2.1 identity. A changed argument, law or guard changes the declaration contract and must be selected explicitly in the suite and protocol. For example, replacing `pass|degrade` admission with `pass` only would change whether `apply` may produce an NCV for degraded evidence; that hypothetical revision cannot enter through the unqualified name UNM. Whether two declarations concern the same operation family is a separate claim requiring that subject's direct kind and identity rule; the UNM label supplies neither.

**Scope note.** This operation declaration uses the `U.Mechanism` content rules governed by `A.6.1`. It defines only UNM’s stable *semantic surface*. It does **not** bind project pins (editions/policy‑ids), which belong to the A.15.2 baseline and, only for independently declared positions, A.15.3 typed filling under A.19.CHR, and it does **not** emit `GateDecision`/`GateLog`. It may emit tri‑state `GuardDecision` and Audit pins.

**IntensionHeader**
- `IntensionId`: `UNM`
- `IntensionRef`: `UNM.IntensionRef`
- `Name`: Unified Normalization Mechanism
- `Status`: Stable
- `Version`: `v1.0`
- `SuiteRole`: CHR.normalize (when enabled by CN/CHR routing)

**Imports (cite, don’t duplicate)**
- `A.6.1` (shape: `U.Mechanism`, specialization discipline)
- `A.19.CHR:4.2` (CHR suite boundary / membership)
- `A.19.CHR:4.2.1` (CHR SlotKind Lexicon)
- `A.19.CHR:4.5` (suite protocols: ordering/optionality; suite closure)
- `A.19.CN` (CN-frame routing: `normalization`, `comparability.mode`)
- `G.0` (CG-frame admissibility gates where required downstream)
- `C.16` (evidence carriers; calibration/validity for normalization legitimacy)
- `A.17/A.18` (measurement meaning & scale lawfulness; not redefined here)

**SubjectBlock**
- `SubjectKind`: declared normalization methods, with their actual domains, output kinds and preserved/lost distinctions; functional methods may additionally supply `≡_UNM` over their admitted inputs
- `RangedValueKind`: coordinate values (`CV`) for named measurable slots in the exact `U.CharacteristicSpace` and CN-Spec editions; UNM normalizes **values**, not characteristics
- `BearerAndUseBoundary`: the exact bearer, scope and window, reference or comparison basis, evidence, and intended comparison declared for those values
- Input qualification: coordinate values admitted by the selected CN-Spec for this bearer and use, within the configured method's declared validity window. This is not an operation-application extent or an A.6.1 slice-membership `ExtentRule`.
- `ResultKinds`:
  - `NormalizedCharacteristicValue (NCV)`
  - optional function-kernel equivalence (`≡_UNM`) and its set of classes; a congruence claim only for separately checked operations
  - optional quotient objects and/or `Normalization-fixed` representatives (via `NormalizationFixSpec`)
**Operation-local argument and result declarations**

The names below are declaration-local designators. `ByValue` carries the stated value; each named Ref resolves to one exact value and edition under this declaration's effective reference scheme. Cardinality is per application. The first four arguments are shared declarations instantiated separately for `apply` and `UNM_Eligibility`.

| Operation and direction | Local designator | Meaning and ValueKind | Designation; cardinality |
| --- | --- | --- | --- |
| apply / UNM_Eligibility argument | NormalizationMethodInstanceSlot | Configured normalization method selected for the value; NormalizationMethodInstanceId | ByValue; 1 for apply, 0..1 for eligibility |
| apply / UNM_Eligibility argument | CoordinateValueSlot | Coordinate value to transform or assess; CV in the named chart | ByValue; 1 for apply, 0..1 for eligibility |
| apply / UNM_Eligibility / compose argument | CharacteristicSpaceSlot | Space that supplies the coordinate meanings and Scales; U.CharacteristicSpace | U.CharacteristicSpaceRef; 1, or 0..1 for eligibility |
| apply / UNM_Eligibility / compose argument | CNSpecSlot | CN-Spec used for the bearer, scope/slices, qualification window, basis, evidence requirements and intended comparison | CNSpecRef; 1, or 0..1 for eligibility |
| apply result | NCVSlot | Transformed value returned under the selected method's domain and preservation/loss basis; NCV | ByValue; 1 on successful return, 0 without a defined/admitted result |
| UNM_Eligibility result | GuardDecision | Eligibility judgment under the predicates below; pass, degrade or abstain | ByValue; 1 on completed evaluation |
| compose argument | NormalizationMethodInstancePairSlot | Ordered pair of configured methods, first inner and second outer; NormalizationMethodInstanceId[2] | ByValue; 1 pair |
| compose result | NormalizationMethodInstanceSlot | Configured composed method, with its declared validity window and evidence basis; NormalizationMethodInstanceId | ByValue; 1 on successful construction |
| quotient argument | domain | Actual admitted domain D of the selected normalization function, with coordinate meanings recoverable; set of CV values | ByValue or one exact governed chart-domain reference; 1 |
| quotient argument | NormalizationMethodInstanceSlot | Configured functional method used to form equality-of-output classes; NormalizationMethodInstanceId | ByValue; 1 |
| quotient result | UNMEquivalenceSlot | Relation on D defined by equality of that function's outputs | ByValue; 1 on successful construction |
| quotient result | classes | Set D/≡_UNM of all classes of that relation | ByValue; 1 on successful construction |

For each argument row, its **bindingPredicate** obtains exactly when that application uses the resolved value for the row's stated purpose: as the transformation operand, selected method, governing space/CN-Spec, ordered composition pair or quotient domain. A supplied but unused value is not bound. `UNM_Eligibility` may assess an incomplete proposal; an absent argument has no binding and the corresponding missing-input condition gives `abstain`. This does not relax `apply`'s inputs.

For each result row, its **bindingPredicate** obtains exactly when that application returns the resolved value as the row's declared result, subject to the result laws below. A returned NCV binds the transformation value; `compose` binds the identifier of the method it constructed; `quotient` binds the relation and class set it constructed; the guard binds the judgment it evaluated. Each binding has the A.6.1 identity and maximal continuous extent within its application; a result binds at return, not before. Equal values returned by different applications have distinct bindings because their applications differ.

**SlotIndex (derived projection).** Project the designators, ValueKinds, designation rules and cardinalities from these operation-local declarations; the index adds no meanings. The historical `Slot` suffix permits CHR lookup. A.6.5 relation SlotSpecs are not the source of these operation meanings. Method descriptions, invariants and any `NormalizationFixSpec` are resolved from the selected configured method and CN-Spec. They qualify the method or a separately chosen representative use; they are not additional arguments of every operation.

**Relation note (not a SlotKind).** A Bridge, kind relation, or plane relation is cited only when the use relies on that obtaining relation. Its declaration and receiving use remain separate from the UNM SlotIndex.

**OperationAlgebra**
1) `apply`
   - Preconditions: `UNM_Eligibility(…) ∈ {pass, degrade}` (fail‑closed; `abstain` ⇒ no NCV output).
   - Inputs: `NormalizationMethodInstanceSlot`, `CoordinateValueSlot`, `CharacteristicSpaceSlot`, `CNSpecSlot`; the selected CN-Spec supplies the exact bearer, scope/window, basis, evidence requirements, and intended comparison.
   - Outputs: `NCVSlot` for an input in the selected transformation's actual domain, with the declared preservation/loss basis. Undefined inputs produce no NCV; an eligibility result cannot create a transformation value. The optional class/operation results follow their separate conditions below.

2) `compose`
   - Purpose: build a composed method when the inner outputs lie in the outer operation's actual domain and the claimed preservation laws compose. Losses and receiving-use restrictions remain explicit.
   - Inputs: `NormalizationMethodInstancePairSlot` (roles = {inner, outer}), `CharacteristicSpaceSlot`, `CNSpecSlot`; both instances must be admitted for the same declared bearer, scope/window, basis, and intended use.
   - Output: `NormalizationMethodInstanceSlot` (new composed `NormalizationMethodInstanceId`), with an explicit validity window and evidence pins.

3) `quotient(≡_UNM)` (optional)
   - Preconditions: one fixed functional normalization on its actual domain, with an explicit output equality. Recover that domain and the exact method/use basis.
   - Inputs: `domain`, resolved from the characteristic-space declaration or a declared chart domain, and `NormalizationMethodInstanceSlot`.
   - Outputs: `UNMEquivalenceSlot` and its `classes` set. Inherited operations additionally require equivalent-output and representative-independent-availability proofs; a class query additionally requires constancy on each class.
   - Use the declared `NormalizationFixSpec` only when a representative is needed. It selects a member of a class rather than proving that member was the original input.

**Particular applications of these operations**

The **ApplicationPredicate** differs by operation:

- `apply`: a calculation actually applies the selected configured method to the bound CV under the bound space and CN-Spec. Its defined, admitted return is the NCV required above. An `abstain` decision prevents this application from starting; passing eligibility alone does not start it.
- `compose`: a construction actually resolves the bound inner/outer methods, checks the domain and preservation conditions and constructs their composite for the bound space and CN-Spec. A failed condition yields no composed-method result.
- `quotient`: a mathematical construction actually uses the bound functional method and domain to determine equality of outputs and form its classes. A symbolic construction is sufficient; enumeration of an infinite domain is not required. Stronger inherited-operation and query claims retain their separate proofs.
- `UNM_Eligibility`: an evaluation actually assesses the bound proposal under the eligibility predicates below and returns the corresponding GuardDecision. Its result is separate from any subsequent normalization.

For each operation, the **ApplicationIdentityRule** identifies one invocation at its calculation or construction locus, from taking up those operands for that operation until return or termination. References to the same uninterrupted invocation reidentify one application. A second invocation, including a nested or later one with the same operands, method, qualification window and result, is another application. Changing an operand after beginning a fresh calculation starts another invocation; a continuation of an interrupted calculation counts as the same application only when continuity of that same invocation is established.

The **ApplicationExtentRule** takes that invocation's actual interval: first use of its arguments through its return or termination. For the guard it is the eligibility evaluation; for compose it is the composite construction; for quotient it is the class construction; for apply it is the value calculation. An unfinished invocation has an open extent and no unreturned result binding. The data's qualification window and the method's validity window do not date these invocations. A trace may designate an invocation; a copied record, matching value or valid method identifier does not establish it. Ordinary function and projection guidance remains usable without an assertion of dated U.Work.

For example, with fixed method `n(x)=x/10`, domain [0,100] and the same CN-Spec, two separate calculations of `n(20)` both return 2. The first operand-to-return episode and the second are two `apply` occurrences; each binds 20 and its own return of 2. A third record containing 2, with no corresponding calculation, supplies no third result binding. Two constructions of `g∘n`, or of the same quotient, are likewise distinct when performed in separate construction episodes; their equal constructed mathematical values do not merge those episodes. Conversely, a second description of the first episode adds no application.

**LawSet (UNM laws; identifiers are stable)**
- **UNM‑L0 (Values, not characteristics).** UNM produces `NCV` as a **value** under declared invariants; it does not redefine the underlying characteristic meaning (measurement meaning remains governed by A.17/A.18 and evidence by C.16).
- **UNM‑L1 (Declared method class gate).** A normalization method instance is admissible only if its method is declared in the allowed method class set: `{ratio:scale, interval:affine, ordinal:monotone, nominal:categorical, tabular:LUT(+uncertainty)}`.
- **UNM‑L1a (Method semantics are governed by the method).** `NormalizationMethod` defines invariants, closure (composition / inverses where defined), and validity rules. UNM consumes these declarations; it does not invent extra admissibility.
- **UNM-L2 (Directed result before narrower claims).** Return the defined transformed value with its domain and preserved/lost distinctions. Functional equality of outputs forms equivalence classes on that domain. A receiving operation descends only after compatibility and, for a partial operation, representative-independent availability hold. A query descends only when constant on the classes; otherwise retain/refine the input or return the missing distinction.
- **UNM-L2a (Declared-basis locality).** Every transformed value, function-kernel equivalence and stronger operation/query claim retains the selected method, actual domain, characteristic-space and CN-Spec editions, bearer, scope/window and comparison basis. Reusing an unchanged equivalence for a new query does not make that query recoverable; assess its own constancy/compatibility and the receiving-use conditions.
- **UNM‑L3 (Fail‑closed).** If admissibility/evidence is insufficient (or required inputs are missing/stale), UNM does not silently coerce; it yields `abstain` or `degrade` (tri‑state guard discipline) and may surface an explicit freshness/work request (see A.19.UNM:4.5).
  *Didactic reading:* `abstain` ⇒ no lawful NCV/comparability for this slice; `degrade` ⇒ NCV may be produced but must be treated as policy‑gated and auditable (never “quietly good enough”).
- **UNM‑L4 (No implicit indicatorization).** `NCV` does not imply “indicator”; indicator status is a separate policy step (UINDM).
- **UNM-L5 (Relation before reuse).** When a receiving comparison depends on an F.9 Bridge, kind relation, or plane relation, cite the exact obtaining relation, its direction, what it preserves or loses, and the receiving use. A change of bearer, scope, corpus, scale, method, or window is not by itself such a relation. Supported penalties route to the **R-lane only** (never to F/G; if scalarized, into `R_eff`).
- **UNM‑L6 (Time explicitness).** Validity windows are named; no implicit “latest”.
- **UNM‑L7 (Auditability).** The applied method and CN-Spec editions, normalized values, bearer, scope and window, comparison basis, evidence pins, intended comparison, and any actually relied-on Bridge, kind relation, or plane relation must be auditable as refs or pins.
- **UNM-L8 (No shadow writers).** Downstream patterns cite the exact method, CN-Spec, basis, and evidence editions they use; they do not re-author those anchors or make a registry substitute for them.
- **UNM‑L9 (No publish/telemetry ops).** UNM defines no publish/telemetry step. Any publication/telemetry is out of suite closure and does not mutate UNM semantics (`NCV`, `≡_UNM`, quotient/fix); only Audit pins are produced here.

**AdmissibilityConditions**
Definition (UNM‑Eligibility):
`UNM_Eligibility(NormalizationMethodInstanceSlot, CoordinateValueSlot, CharacteristicSpaceSlot, CNSpecSlot) → GuardDecision`
where `GuardDecision ∈ {pass | degrade | abstain}` and follows this predicate semantics:
- **pass** iff all of the following hold:
  - (**CN-Spec binding**) the selected `NormalizationMethodInstanceId` is declared in `CN_Spec.normalization.instances` (or an equivalent declared surface), its method kind is included in `CN_Spec.normalization.methods`, and (if present) it satisfies `normalization.admissible_reparameterizations`; the exact characteristic-space and CN-Spec editions, bearer, claim scope and selected slices, qualification window, reference or comparison basis, and intended comparison are recoverable;
  - (**Target coordinate binding**) the input `CV`’s `slot_id` belongs to the method instance’s declared bound coordinate set;
  - (**Scale‑regime compatibility**) the method kind is compatible with the coordinate’s regime (`ratio:scale | interval:affine | ordinal:monotone | nominal:categorical | tabular:LUT(+uncertainty)`) and preserves the declared `NormalizationInvariant[*]` (from `CN_Spec.normalization.invariants` and/or the method description);
  - (**Validity window**) the method instance’s validity window covers the active slice/time policy (no implicit “latest”);
  - (**Evidence sufficiency when routed into governance**) when `comparability.mode = normalization-based` (or downstream uses `NCV` in gated decisions), the method instance’s evidence pins satisfy `CN_Spec.comparability.minimal_evidence` (structure typically gated by `G.0`; evidence semantics governed by `C.16`).
- **degrade** iff all non‑evidence conditions above hold, but the evidence check does not pass and the declared failure behavior permits producing a policy‑gated degraded `NCV` rather than abstaining.
- **abstain** otherwise (including missing binding, coordinate mismatch, out‑of‑window validity, or evidence failure when the declared failure behavior is abstain).

**Applicability**
UNM is applicable when:
- `CN_Spec.comparability.mode = normalization-based`, or
- a declared downstream step requires “compare-on-invariants” and thus requires explicit normalization.
UNM is typically skipped when `comparability.mode = coordinatewise` (unless an explicit downstream step requires a declared quotient/fix anyway).

**Relation and reuse boundary**
- A normalized value remains local to the exact method instance and edition, characteristic-space and CN-Spec editions, bearer, scope and window, reference or comparison basis, evidence, and intended comparison recorded for it.
- If a receiving use depends on a relation between distinct source-local meanings, cite the exact F.9 Bridge, its direction, what it preserves or loses, and that receiving use. If reference planes differ and the comparison depends on their relation, cite the exact plane relation as a separate claim.
- A changed bearer, scope, corpus, scale, method, or window does not by itself establish either relation. If the bearer kind also changes, state the separate kind relation rather than hiding it inside a Bridge. Any loss penalty remains on the R-lane and is used only when the corresponding relation claim supports it.
**Γ_timePolicy**
- Default: `point` (no implicit “latest”).
- If normalization relies on time windows, the validity window is part of the method instance and must be declared.

**PlaneRegime**
- A normalized value keeps the reference plane declared for its input and intended comparison; normalization creates no implicit plane crossing.
- When a comparison actually relies on a relation between different planes, cite that exact relation, its direction and loss, and keep its use separate from the normalization result.
**Audit**
Audit records MUST include:
- `CNSpecRef.edition` + `comparability.mode`, the exact `U.CharacteristicSpace` edition, and the evaluated bearer
- (when present) `CN_Spec.normalization.UNM_id` (the selected UNM mechanism instance id for this CN-Spec)
- chosen `NormalizationMethodInstanceId`, its validity window, and any `NormalizationMethodDescriptionRef.edition`
- declared `NormalizationInvariant[*]` and `NormalizationFixSpec` (if used)
- any declared admissible re-parameterizations (if present in `CN_Spec.normalization`)
- claim scope and selected slices, reference or comparison basis, intended comparison, and all evidence pins used by the instance
- an exact F.9 Bridge, kind relation, or plane relation only when the recorded result or receiving use actually relies on it, including direction, preserved or lost meaning, and the receiving use
- any emitted `FreshnessRequest` / work request identifiers (when applicable; see A.19.UNM:4.5)

### A.19.UNM:4.2 - CN-frame wiring: `normalization` and comparability routing (normative-by-reference) {#cn-frame-wiring-normalization-and-comparability-routing}

**Tell.** CN-frame does not “do normalization”; it **routes** normalization.
- `comparability.mode ∈ {coordinatewise, normalization-based}` governs whether comparisons are done directly or “normalize-then-compare”.
- `normalization.UNM_id?` selects the UNM mechanism instance used by this CN-frame.
- `normalization.methods / instances / method_descriptions / invariants / fix` provide the declared surface that UNM consumes.
(If present) `normalization.admissible_reparameterizations` constrain which re‑parameterizations count as “admissible” under the declared invariants.
(See CN-frame definition in `A.19.CN`; `A.19.CN` remains the governing pattern of the CN-frame surface. This section only states the UNM consumption/interpretation constraints and does not introduce a shadow spec.)

### A.19.UNM:4.3 - Evidence and calibration are governed by MM‑CHR (normative-by-reference) {#evidence-and-calibration-are-governed-by-mm-chr-normative-by}

UNM does not claim “this normalization is legitimate” by decree.
Instead, the legitimacy claim is supported by evidence carriers, calibration records, and validity records governed by `C.16 (MM‑CHR)` and referenced from the chosen `NormalizationMethodInstance`.

### A.19.UNM:4.4 - Select the result needed by the receiver {#select-the-result-needed-by-the-receiver}

For a value comparison, first use the transformed values and their declared preservation/loss basis. Ask whether that basis retains every distinction the comparison requires. Keep original values, refine the normalization, or return the exact missing distinction when it does not.

Form classes only when their set-level result is useful. For an operation on classes, check output compatibility and partial-operation availability. For a query, check class constancy. Name a `NormalizationFix` only when an already justified class use needs a representative. A representative-selection policy and additional evidence cannot repair a false compatibility theorem.

### A.19.UNM:4.5 - P2W and transformation-flow integration note (normative-by-reference) {#p2w-and-transformation-flow-integration-note-normative-by}

When UNM is used inside transformation-flow structures/graphs (e.g., `E.18`):
- UNM occurs **before** selection/decision steps.
- If required measurements are **missing or stale**, apply the declared `abstain` or `degrade` rule and state the gap. The receiving practitioner first checks whether an adequate current basis is already available and whether obtaining new evidence is worth doing. Any chosen acquisition is separately planned and performed under its applicable method; UNM itself neither obtains measurements nor mandates new Work.
- A receiving step cites the exact normalized values, method and CN-Spec editions, bearer, scope/window, comparison basis, evidence and intended use. It cites a Bridge, kind relation or plane relation only when its conclusion actually relies on that obtaining relation and keeps any supported loss on the R-lane.
- Downstream consumers cite editioned method, basis and evidence anchors as refs and do not re-author them.

## A.19.UNM:7 - Conformance Checklist {#conformance-checklist}

- [ ] **Normalization identity:** cite the selected method and configured instance, its description, invariants and any representative-fixing rule. Resolve legacy identifiers through F.18 when used. An ordinary coordinate mapping does not assert a specialized `Map` kind or a Bridge; apply the lexical distinction in §4.0.
- [ ] **CN routing:** uses `CN_Spec.comparability.mode` and the `CN_Spec.normalization` surface; does not embed “shadow CN-spec”.
- [ ] **Fail-closed:** eligibility is tri-state and never coerces unknown to pass.
- [ ] **Lawfulness classes declared:** method class is one of `{ratio:scale, interval:affine, ordinal:monotone, nominal:categorical, tabular:LUT(+uncertainty)}` and the instance's validity window is named.
- [ ] **No indicator conflation:** does not treat NCV as automatically implying indicator status.
- [ ] **Relation and reuse discipline:** every NCV names the method and CN-Spec editions, bearer, scope/window, reference or comparison basis, evidence and intended comparison; cite a Bridge, kind relation, or plane relation only when the use actually relies on it, with any supported loss on `R`/`R_eff`.
- [ ] **Result branch:** the actual domain, directed output and preserved/lost distinctions are explicit. An inverse is claimed only on its stated image. A set quotient uses equality of function outputs on that domain; an inherited operation also passes compatibility and partial-availability checks, and a recovered query is constant on each class. A required representative has a declared fix and is not treated as the lost original input.
- [ ] **Auditability:** method and CN-Spec editions, bearer, scope/window, basis, evidence, intended comparison, and any actually used relation are recorded as refs or pins.
- [ ] **No shadow writers:** downstream consumers cite the exact method, basis, and evidence editions and do not re-author them or replace them with a generic registry.
- [ ] **Missing or stale inputs:** apply the declared abstain/degrade rule and name the gap. An undefined transformation input has no NCV. Reuse an adequate existing basis or plan a justified acquisition under its own method; normalization alone mandates no new Work.
- [ ] **SlotKind discipline:** SlotKind tokens reuse the CHR SlotKind lexicon where applicable; UNM‑specific SlotKinds are docked into the suite lexicon before use (no ad‑hoc drift).
- [ ] **No proxy registry:** no registry key stands in for the exact normalized values, method, CN-Spec, bearer, scope/window, basis, evidence, intended comparison, or actually obtaining relation.

## A.19.UNM:9 - Consequences {#consequences}

**Benefits**
- Makes “normalize-then-compare” a first-class governance choice.
- Centralizes governing-pattern assignment, improving usability and reducing drift.
- Supports evolvability: method families can evolve via packs/extensions without mutating the mechanism surface.
- Prevents silent inadmissibility (unit, scale, and plane errors) by fail-closed guards.

**Costs**
- Requires explicit declarations (method instance, invariants, validity window, evidence pins).
- Class-level use requires compatibility/query arguments; ordinary transformed-value use need not construct a quotient or fix.

## A.19.UNM:12 - Relations {#relations}

**Builds on / cites**
- `E.8` (pattern template)
- `E.20` (governing-pattern discipline for mechanism‑intension content)
- `A.15.2` for the edition/reference baseline; `A.15.3` only for typed planned filling of an independently declared position
- `F.18` (alias docking / token continuity, when renaming or retiring legacy UNM tokens)
- `A.6.1` (U.Mechanism shape; specialization discipline)
- `A.19.CHR` (CHR suite boundary; slot lexicon; suite protocols)
- `A.19.CN` (CN_Spec normalization + comparability routing)
- `C.16` (MM‑CHR evidence/calibration carriers)
- `G.0` (CG-frame admissibility gates used downstream)
- `G.2` (SoTA synthesis packs as the method‑family ingress; wiring‑only integration)
- `E.18` (when UNM is used in transformation-flow structures/graphs; P2W freshness/work routing)
- `C.29` for the mathematical account of the chosen function, equivalence or quotient; `B.3` only for an actual named assurance claim

**Used by**
- CHR suite protocols (normalize stage), when `comparability.mode` requires normalization-based comparability.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-19-CN#root, spec://ai.lev/fpf-spec/contract/A-6-1#root, spec://ai.lev/fpf-spec/contract/A-6-5#root, spec://ai.lev/fpf-spec/contract/A-19-CHR#root, spec://ai.lev/fpf-spec/contract/A-17#root–spec://ai.lev/fpf-spec/contract/A-18#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/G-0#root, spec://ai.lev/fpf-spec/contract/E-18#root, spec://ai.lev/fpf-spec/contract/E-20#root, spec://ai.lev/fpf-spec/contract/F-18#root. @status:spec/done
- @fact:USED-BY Used by: spec://ai.lev/fpf-spec/contract/A-19-CHR#root, spec://ai.lev/fpf-spec/contract/A-19-USCM#root, spec://ai.lev/fpf-spec/contract/A-19-CPM#root, spec://ai.lev/fpf-spec/contract/A-19-SelectorMechanism#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/G-2#root, spec://ai.lev/fpf-spec/contract/B-3#root. @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-19-UNM

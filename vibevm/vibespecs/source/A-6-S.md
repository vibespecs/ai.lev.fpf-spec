# A.6.S - TargetSignature and optional ConstructorSignature - demand-driven signature engineering: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.6.S:0 - PCP-TERM/LEX token guards (local-first) {#pcp-term-lex-token-guards-local-first}

This pattern reserves the following tokens in Tech (normative) register:

* **TargetSignature** — the engineered signature episteme (and its editions) under construction and stabilisation (**not** the EntityOfConcern, and **not** the target source or cell of an F.9 relation).
* **ConstructorSignature** — the enabling signature that describes constructor operations for TargetSignature evolution (do **not** mint a second Tech token such as `EnablingSignature`).

Rename-guards (common collisions):

* **enabling** — Plain adjective meaning “producing/maintaining the TargetSignature”; it is not a `U.*` token.
* **constructor** — MUST distinguish `ConstructorSignature` (episteme), a constructor-operation description, the A.6.2 arrow used to state its effect-free episteme relation, and the admitted System that applies the described constructor operation and performs any separately admitted construction Work. State any local system-role classification and obtaining assignment separately. If the physics term is intended, spell **Constructor Theory** explicitly.
* **target** — avoid bare “target” in Tech clauses; use `TargetSignature` or qualify the target (for example, “F.9 target cell” or “target holon”).
* **contract** — if source wording uses this Plain shorthand, recover whether it means `TargetSignature`, Contract Bundle, promise content, commitment, or work/evidence. In this pattern the intended recovered value is usually `TargetSignature`; promises, duties, and gates are classified under `A.6.B` and `A.6.C`.

## A.6.S:5 - Worked cases {#worked-cases}

**Ordinary cheap stop.** An editor adds the law `Refund does not increase net balance` to `PaymentBoundarySignature` and issues edition 4. The changed ClaimGraph identifies a new signature episteme; the edition or continuity relation and the editor's Work are stated only when the receiving claim uses them. If nobody needs reusable constructor vocabulary, stop. No ConstructorSignature or pair object is created.

### A.6.S:5.1 - Repeated engineering of a service boundary {#repeated-engineering-of-a-service-boundary}

**Working situation.** Several client teams and two authoring Systems will revise and republish the same payments boundary over multiple editions. They need one reusable account of the allowed authoring operations.

**TargetSignature:** `PaymentBoundarySignature` declares operations such as `Authorize`, `Charge`, and `Refund`; the participant meanings and ref modes reused in any actual relation declaration; laws such as idempotent charging; and the external-API applicability boundary. Keep operation arguments and results under A.6.1; A.6.5 governs participant positions only in an exact RelationSignature.

**ConstructorSignature:** `PaymentSignatureEngineering` is justified because the named authoring and review uses reuse the same operation vocabulary and laws. It may declare:

* a by-value law revision and a reference-retargeting operation when those distinctions are reused; apply A.6.5 only if the move concerns a SlotSpec in an exact RelationSignature, keeping ordinary law-content revision under its declaration rule and operation arguments/results under A.6.1;
* a direct calibration, provenance, or other relation assertion under its own pattern, with an A.6.6 declaration-change label only when a receiver tracks its represented history; and
* an E.17 publication operation for the repeated Plain, Tech, and interoperability publications, with a reusable view-producing operation only when needed and any A.6.3 construction identified separately.

`PaymentSignatureEngineeringPipeline`, if admitted as a System, may apply the described operations. Any claimed dated authoring or publication Work requires its complete A.13 performer core and independent A.15.1 admission as in §4.0. The ConstructorSignature does not act. Add the separate F.6 Work-assignment relation only for precise attribution through that same obtaining assignment; state an application binding, carrier, evidence relation, or additional classification or assignment only when its own claim is current.

The sentence `Charges are recorded in Ledger L for the external API` must first name and test its actual direct relation. Do not replace it with `declareBase`, a generic `baseRelation`, or a witness package. If later comparison needs a stable representation of that assertion and its scope, A.6.6 may add the optional declaration history.

The publication faces are faithful forms over the exact TargetSignature edition for their bounded readers and uses. Any claim that the selected episteme is a `U.View` requires its own E.17.0 conformance under §4.4. `Guarantees idempotency` is unpacked into the actual law, any separate mechanism admission condition, deontic commitment, and evidence-use claim; the word *contract* creates none of them.

### A.6.S:5.2 - Repeated engineering of a model-correspondence signature {#repeated-engineering-of-a-model-correspondence-signature}

**Working situation.** A research group maintains a correspondence signature across several model editions and publishes mathematical and engineering views. A second group must reproduce the same revisions.

`ModelCorrespondenceSignature` is the TargetSignature. Its vocabulary, laws, and applicability state the exact correspondence claim and the schemes in which it is interpreted. An actual F.9 Bridge is cited only when a relation between two exact F.17 cells obtains and a separate bounded-use claim is current.

`CorrespondenceSignatureEngineering` is an optional ConstructorSignature because the second group reuses its declared revision and view-production vocabulary. A reference-retargeting operation may identify a new model edition. An A.6.2 arrow may compare exact source and receiving signature epistemes and any named neighboring facts; it changes none of those facts. The actual application, authoring System, Work, resulting episteme, and publications remain separate.

If the project only changes one reference dataset window once, state that direct revision and any needed Work or successor edition, then stop. Do not create the ConstructorSignature merely to host `retime`.

## A.6.S:6 - Bias-Annotation {#bias-annotation}

Scope: signature-engineering uses that meet the entry condition; ordinary one-off revisions remain outside the two-signature branch.

* **Architecture bias (Arch):** a reusable ConstructorSignature can improve repeated work but can also turn one edit into a framework.
  *Mitigation:* require a named receiver for the reusable vocabulary and laws; otherwise use the direct move and stop.
* **Onto/Epist bias (Onto/Epist):** treating “editing the signature” as harmless can hide semantic change.
  *Mitigation:* distinguish a direct edit or new same-EntityOfConcern edition from an A.6.4 retargeting. A changed C.2.1 discriminator identifies another episteme; A.6.4 opens only when the exact EntityOfConcern changes.

* **Pragmatic bias (Prag):** repeatable operation declarations cost authoring effort.
  *Mitigation:* introduce them only when a named receiver would otherwise reconstruct the same vocabulary or law.

## A.6.S:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Why it fails | Repair |
| --- | --- | --- | --- |
| **Pair object by juxtaposition** | Two signatures are named and called `U.SignatureEngineeringPair`. | No admitted kind, predicate, applicability, or occurrence identity exists. | Retire the pair token; state the exact dependency or use that actually obtains, or merely name both signatures. |
| **ConstructorSignature for every edit** | A one-line revision acquires two operation lexicons, arrow metadata, assignment, evidence, and publication records. | Reusable declaration work has replaced the actual task. | State the direct revision and stop; add a ConstructorSignature only for a named reuse of its vocabulary and laws. |
| **One publication mixes declaration and work record** | Target laws, constructor notes, review history, gates, and Work evidence share one undifferentiated artifact. | Signature, operation description, application, Work, and carrier cannot be distinguished. | Separate only the objects current for the receiving use; do not create a ConstructorSignature merely to hold notes. |
| **Silent semantic edit** | A law or applicability changes while consumers still cite the old episteme. | A new C.2.1 discriminator triple is presented as the same episteme. | Identify the successor episteme and the exact edition, continuity, or reference change actually used. |
| **Arrow as performed operation** | An A.6.2 arrow is said to author, validate, or publish a signature. | Mathematical relation, application, and Work collapse. | Let the arrow compare exact epistemes; identify any application, System, and Work separately. |
| **View as another truth** | Plain and Tech faces add different commitments. | Publication gained semantics. | Keep each face a faithful E.17 publication form over the exact source episteme and state any new claim separately; use §4.4 for view membership and boundary claim-set integrity. |
| **Episteme as actor** | The ConstructorSignature builds or publishes the TargetSignature. | Hides the acting System and gives agency to a description. | Say what the signature describes; name the System and Work only when the receiving claim needs them. |

## A.6.S:10 - Rationale {#rationale}

Stable boundaries sometimes benefit from a reusable description of how they are revised. That is the useful two-signature technique: one `U.Signature` is the current target declaration, and another `U.Signature` declares constructor operations for a named reuse. It is not a universal architecture for editing and does not require a third pair object.

A.6.5, A.6.6, A.6.2-A.6.4, and E.17 supply distinct optional moves. Treating all of them as mandatory constructor primitives would recreate the ambiguity and overhead those patterns are meant to remove. The direct move comes first; the reusable ConstructorSignature packages only the operation language that has an actual receiver.

The result keeps viewing, declaration edits, episteme succession, reference retargeting, EntityOfConcern Retargeting: Judge a Bounded Use Across Different Entities, application, and Work distinct. A.6.B likewise keeps laws, gates, duties, and evidence-use claims from competing in one “contract” paragraph.

**SoTA source note (informative).** Modern effect systems support the separation between an operation declaration and effectful realization; categorical optics inform explicit preservation claims; and architecture-description practice informs accountable views. A.6.S adopts those limited separations without importing a tool ontology or making a ConstructorSignature mandatory.

## A.6.S:11 - SoTA-Echoing {#sota-echoing}

* **Adopt: algebraic effects and effect systems separate operation signatures from handler semantics.**
  Contemporary effect systems emphasise that an operation signature can be described independently of how effects are handled. A.6.S adopts that separation here: the TargetSignature remains the boundary declaration, while any operation application, construction Work, and operational enforcement remain separately identified. This echoes row-typed algebraic effects and modern handler formulations (Leijen 2017; Hillerström & Lindley 2018).

* **Adapt: categorical optics treat “focus” and “round‑trip laws” as a disciplined interface for bidirectional structure.**
  Optics offer a compact mathematical language for “what is preserved” under a transformation and when updates are coherent. A.6.S adapts this mindset to boundary evolution: viewing corresponds to projection, and retargeting corresponds to an explicit transition with stated preservation claims. Profunctor optics provide a post‑2015 reference point for this style of interface reasoning (Pickering, Gibbons & Wu 2017).

* **Adapt: architecture-description practice relates views to viewpoints and stakeholder concerns.**
  ISO/IEC/IEEE 42010:2022 contributes that discipline. FPF's local adaptation identifies the exact `U.Viewpoint` episteme and tests the selected episteme's `U.View` membership through E.17.0 conformance; a publication face remains the separate form over its source for a bounded reader/use, with membership and A.6.3 construction conditional under §4.4. Any separate `responsibility` or `view-accountability` claim needs its actual participants and governing predicate. A ConstructorSignature is added only when a named receiver reuses the view-producing operation declaration; it is not required to explain how every view was produced.

* **Adopt in spirit: behavioural protocol disciplines treat boundaries as typed interaction protocols with safety commitments.**
  Session and behavioural type practice treats boundaries as protocols with progress and safety properties, which matches the A.6 split between signature laws and mechanism entry gates. A.6.S does not import tooling or typechecking, but it adopts the practice of making boundary interactions explicit and law‑governed (e.g., modern MPST practice as cited in A.6.1).


## A.6.S:End {#end}

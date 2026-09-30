# A.6.B — Boundary Norm Square (Laws / Admissibility / Deontics / Work‑Effects) {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural (A)
> **Status:** Stable
> **Normativity:** Normative (unless explicitly marked informative)
> **Placement:** Part A → A.6.B (matrix module; referenced by A.6 cluster overview)
> **Builds on:** E.8 (authoring template), A.6.0 (`U.Signature`), A.6.1 (`U.Mechanism`), A.6.3 (`U.EpistemicViewing`), E.17.0/E.17 (MVPK + “no new semantics” faces), A.7 (EntityOfConcern and Description-episteme boundary; specification-use and publication-carrier distinction), A.2.3 (promise content when contract language is current), A.2.8 (`U.Commitment`), A.2.8.PER (subject pattern selected by the permission-word branch), A.2.9 (`U.SpeechAct`), E.10.D2 (EntityOfConcern and Description-episteme boundary; specification-use and refinement discipline), E.10 publication face, form, unit, and carrier discipline
> **Purpose (one line):** Provide a canonical 2×2 norm square that classifies boundary statements (L/A/D/E), constrains how each quadrant is written, and defines explicit cross‑quadrant reference rules to support later boundary evolution and audit.

**Use this when.** Use `A.6.B` when boundary wording mixes definitions, runtime entry conditions, generic prescriptions, individual duties or grants, actual work or evaluation results, and evidence.

**First useful move.** Split the live passage into atomic claims, classify each claim by modality and adjudication position, and replace any consequential paraphrase dependency with an ID or canonical-location reference.

**What changes in practice.** Laws, gates, governance, and work-and-evidence claims can change without silently changing one another; publication faces reuse the canonical claims instead of restating them.

**Ordinary non-use boundary.** A one-off local sentence with one recoverable logical job still needs the correct quadrant, but it does not need a Claim Register or a separate publication form. Add those only when reuse, decision, audit, or cross-face citation needs them; §6.1 still requires any material dependency to name the claim by ID or canonical location.

## A.6.B:1 — Problem frame {#problem-frame}

Boundary descriptions routinely collapse four distinct claim families into “contract soup”: definitions are written as obligations, runtime gates are hidden inside laws, governance talk is assigned to “the interface”, and operational-result “guarantees” are asserted without the actual Work, evaluation, or observation needed to settle them. The resulting boundary is brittle: substitution becomes unclear, and auditability becomes performative rather than adjudicable.

FPF already separates the necessary strata (Signature vs Mechanism, EntityOfConcern, Description episteme, and carrier, views under viewpoints). What is still needed is a **single, reusable classification primitive** that any boundary text can apply consistently and that other patterns can cite as a stable authoring module.

## A.6.B:2 — Problem {#problem}

When authors cannot reliably answer two questions—

1. “Is this a truth‑conditional statement or a governance statement?”
2. “Is it adjudicated by reading the description or by observing work?”

—then boundary statements drift across layers, faces fork semantics, and “compliance” becomes a matter of interpretation rather than a property that can be checked.

A boundary needs a minimal, stable classification that:

* classifies every **atomic** statement into a unique quadrant, and
* forces any cross‑quadrant dependencies to be **explicitly referenced**, not smuggled by paraphrase.

## A.6.B:3 — Forces {#forces}

| Force                              | Tension                                                                                        |
| ---------------------------------- | ---------------------------------------------------------------------------------------------- |
| **Precision vs readability**       | Predicate‑style constraints reduce ambiguity; narrative helps adoption.                        |
| **Evolvability vs enforceability** | Stable laws should not embed volatile runtime gates; governance still needs enforcement hooks. |
| **Auditability vs simplicity**     | Evidence makes claims adjudicable; evidence also introduces operational design obligations.    |
| **Local meaning vs reuse**         | Boundaries must be local; reuse must be explicit via IDs and references, not duplicated prose. |

## A.6.B:4 - Solution — the Boundary Norm Square {#solution-the-boundary-norm-square}

### A.6.B:4.1 - Two independent distinctions {#two-independent-distinctions}

The **Boundary Norm Square** is the cross product of two independent distinctions:

1. **Modality family:** Truth‑conditional vs Governance
2. **Adjudication position:** In-description vs in-work

The square yields four quadrants that are *mutually exclusive for atomic claims*.

### A.6.B:4.2 — The square {#the-square}

|                                | **Truth‑conditional** (definitions & invariants) | **Governance** (governance conditions & obligations) |
| ------------------------------ | ------------------------------------------------ | ------------------------------------------ |
| **In-description or in-theory** | **L — Laws & Definitions**                       | **D — Deontics & Commitments**             |
| **In-work or in-execution**     | **E — Work‑Effects & Evidence**                  | **A — Admissibility & Gates**              |

**Clarification (classify the claim by its job, not by its subject pattern).**

* Classify the exact atomic claim by what its sentence states and by the conditions that let a reader decide it.
* The exact ClaimGraph located through the subject pattern supplies the referenced object's predicate and obtaining conditions; it does not choose the claim's quadrant.
* When permission wording is present, use the single permission-word branch in §8.4.1. It separates the possible jobs of that wording without inventing a common “permission result” kind.

**Normative rule (single quadrant).** Each **atomic** claim **MUST** be classifiable under exactly one quadrant **L/A/D/E**.

**Normative rule (no mixed sentences).** A conforming boundary text **SHALL** decompose any sentence that bundles multiple quadrants (typical form: “MUST … if … then … and it is logged …”) into multiple atomic claims before those claims are treated as normative.

### A.6.B:4.3 — Canonical placements in the Signature Stack {#canonical-placements-in-the-signature-stack}

The quadrants have canonical placements in the boundary stack:

* **L → Signature layer:** `U.Signature.Laws` (and mechanism‑local semantic laws if present).
* **A → Mechanism layer:** `U.Mechanism.AdmissibilityConditions` (entry gates / runtime admissibility predicates).
* **D → Deontics & Commitments layer:** atomic claims about a generic prescription or about one separately obtaining individual duty, recommendation-as-duty, prohibition, or commitment. When permission wording is live, §8.4.1 decides whether its claim also belongs here.
* **E → Work-Effects & Evidence layer:** truth-conditional claims whose satisfaction requires actual work, evaluation, observation, or produced carriers.

A publication face **MUST NOT** introduce new semantic claims outside this L/A/D/E-classified claim set. **E.17 (MVPK)** enforces this rule for publication faces and their selected profiles.

## A.6.B:10 — Conformance Checklist {#conformance-checklist}

| ID                                       | Requirement                                                                                                                                                                                                      | Purpose                                                  |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| **CC‑A.6.B.1 (Atomicity).**              | A conforming boundary text **SHALL** decompose mixed sentences into **atomic claims** such that each atomic claim belongs to exactly one quadrant **L/A/D/E**.                                                    | Makes L/A/D/E classification unambiguous; prevents contract soup.       |
| **CC‑A.6.B.2 (Quadrant classification).** | Each atomic claim **MUST** be classified by its own modality and adjudication position, not by its subject-pattern family. When permission wording is present, the single branch in §8.4.1 **MUST** select the claim's job before assigning L/A/D/E. | Prevents one pattern catalogue from replacing the square's decision. |
| **CC‑A.6.B.3 (Form and obtaining constraints).** | `L-*` and `A-*` claims **MUST NOT** use RFC deontic keywords as operators. A generic-prescription `D-*` claim **MUST** name its exact normative source and applicable rule content without inventing an individual occurrence; an individual-duty `D-*` claim **MUST** name its actual bearer and exact separately obtaining `U.Commitment`; a grant `D-*` claim **MUST** satisfy §8.4.1. No claim text makes its relation obtain. Responsibility uses its direct predicate or exact missing governor. An `E-*` claim **MUST** name the work, evaluation, or observation that settles it and any evidence used for reliance. | Keeps normative content, individual institution, responsibility, and evaluated results distinct. |
| **CC‑A.6.B.4 (Explicit references).**    | Where a claim depends on another L/A/D/E-classified claim, that dependency **MUST** be expressed by explicit ID or canonical-location reference rather than restating the other claim in new words.                                                | Prevents paraphrase drift across layers and faces.           |
| **CC‑A.6.B.5 (E‑claim adjudicability).** | Each `E-*` claim names its exact predicate and object plus the actual work, evaluation, or observation, scope/window, comparison frame, and other conditions required to settle that predicate. It adds an evidence/source-use relation, carrier/schema, viewpoint, and consumer only when the receiving reliance decision depends on that support. | Makes work-effects adjudicable without forcing unrelated carrier apparatus into every result claim. |
| **CC‑A.6.B.6 (No gate smuggling).**      | Operational admissibility predicates **MUST NOT** appear as `L-*` laws in the signature layer; they **MUST** be `A-*` claims in the mechanism layer.                                                             | Preserves substitution and signature stability.          |
| **CC‑A.6.B.7 (No upward dependencies).** | `L-*` claims **MUST NOT** reference `A-*`, `D-*`, or `E-*`, except for purely informative notes explicitly marked informative; `A-*` claims **MUST NOT** reference `D-*`. An `E-*` reference to `D-*` **MUST** meet §6.4's evidence-target or evaluation-input rule and **MUST NOT** treat the D claim alone as an E result. | Keeps laws and gates independent while permitting evidence about normative claims. |

## A.6.B:12 — Consequences {#consequences}

| Benefits                                                                                                     | Trade‑offs / mitigations                                                                         |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| **Stable modular boundaries.** Laws don’t accidentally become gates; governance doesn’t masquerade as truth. | Requires writers to split sentences; mitigated by the triangle decomposition pattern.            |
| **Explicit adjudication links.** Commitments can be linked to adjudicable evidence carriers.                | Requires evidence to be designed; mitigated by keeping evidence conceptual and carrier-referenced. |
| **Reduced semantic drift across faces.** IDs + explicit references reduce drift caused by restatement.            | More cross‑references; mitigated by a Claim Register (optional but recommended).                 |

## A.6.B:15 — Relations {#relations}

* **Used by A.6 and A.6.C:** supplies the canonical matrix and cross-quadrant link discipline. Both consumers classify each exact atomic claim by predicate and adjudication, keep the claim episteme separate from its EntityOfConcern, and use the §8.4.1 branch only when permission wording is live.
* **Constrains A.6.0 (`U.Signature`):** enforces that `L-*` laws are truth‑conditional and do not include admissibility predicates.
* **Constrains A.6.1 (`U.Mechanism`):** enforces that admissibility lives in `AdmissibilityConditions` (`A-*`) and that evidence semantics are classified as `E-*` with carrier references.
* **Requires A.7:** identifies each claim's EntityOfConcern separately from the
  episteme carrying it. The concern may itself be a Description episteme or
  publication carrier.
* **Interacts with MVPK/E.17:** faces are projections that cite L/A/D/E-classified claims and mint no new semantics. When the permission-word branch is selected, its row names the subject pattern and obtaining or failure test; A.6.B only classifies the statement, and neither wording nor a carrier makes the referenced object obtain.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-8#root, spec://ai.lev/fpf-spec/contract/A-6-0#root, spec://ai.lev/fpf-spec/contract/A-6-1#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/A-7#root, spec://ai.lev/fpf-spec/contract/A-2-8#root, spec://ai.lev/fpf-spec/contract/A-2-8-PER#root, spec://ai.lev/fpf-spec/contract/A-2-9#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-6#root, spec://ai.lev/fpf-spec/contract/A-6-C#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-2-8#root, spec://ai.lev/fpf-spec/contract/A-2-8-PER#root, spec://ai.lev/fpf-spec/contract/A-6#root, spec://ai.lev/fpf-spec/contract/A-6-C#root, spec://ai.lev/fpf-spec/contract/A-6-F#root, spec://ai.lev/fpf-spec/contract/A-6-M#root, spec://ai.lev/fpf-spec/contract/A-6-P#root, spec://ai.lev/fpf-spec/contract/A-6-S#root, spec://ai.lev/fpf-spec/contract/C-26-1#root, spec://ai.lev/fpf-spec/contract/E-17-EFP#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-6-B

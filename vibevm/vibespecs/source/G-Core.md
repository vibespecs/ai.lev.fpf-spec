# G.Core - Discipline SoTA Kit Invariants, Defaults and Refresh Triggers (Part G): depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## G.Core:5 - Archetypal grounding {#archetypal-grounding}

**Tell.**
In Part G authoring, `G.Core` is the hub that allows each `G.x` to become structurally predictable: (a) a short, normative “Core linkage” slice, and (b) pattern‑scoped `Extensions`. Universal obligations cite canonical governing definitions such as `A.6.7`, `A.15.3`, `A.19`, `G.0`, and `A.19.CHR`, while RSCR trigger kinds and `DefaultGoverningDefinitionRef` references become typed and cite named definitions.

**Show 1: Refresh triggers without semantic drift.**
`G.11` already uses trigger tokens `T0…T7`. `G.Core` keeps them as aliases and maps them to canonical trigger kinds (e.g., `TelemetryDelta`, `EditionPinChange`, `CrossingBundleEdit`). This makes RSCR reason codes consistent across patterns and avoids re-explaining trigger semantics in every pattern.

**Show 2: Resolving competing defaults.**
If multiple patterns imply a default for `PortfolioMode`, the Default Governing Definition Index points to one governing definition (currently `CC‑G5.23`). Other patterns (e.g., bundles/log patterns) must cite that governing definition or delegate to it, rather than restating the default with slightly different wording. This preserves intent while preventing drift and ambiguity.

## G.Core:6 - Bias-annotation (informative) {#bias-annotation-informative}

* **Centralization bias:** One governing hub can become too thick. Mitigation: delegation-first citation; keep only true Part‑G invariants and typed indices here.
* **Over-typing bias:** A trigger catalogue can become overly granular. Mitigation: granularity discipline + scope notes; only add new kinds when planning/selection needs it.
* **Refactor rigidity bias:** Preserving IDs can feel cumbersome. Mitigation: delegation items preserve IDs while enabling deduplication.
* **Default absolutism bias:** Defaults may require conditional rules. Mitigation: Default Governing Definition Index allows conditional default rules with explicit applicability conditions.
* **Single-writer bias:** prefers single‑writer *authoring* for catalogs and explicit governing-definition tables.
  *Mitigation:* delegation-first citation; keep catalogs minimal; avoid “second specs”.
* **Architectural bias:** centralizes invariants to prevent accidental coupling across `G.x`.
  *Mitigation:* keep core thin; force `Extensions` to remain pattern‑scoped.
* **Ontological/epistemic bias:** enforces strict distinction between governing spec refs, kits, mechanisms, and orchestration.
  *Mitigation:* allow didactic scope notes while keeping normative surface id‑based.
* **Pragmatic bias:** adds authoring overhead (linkage sections, alias maps).
  *Mitigation:* one small mandatory bridge CC item per pattern (`CC‑Gx‑CoreRef`) and short linkage slices only.
* **Didactic bias:** risks “glossy hub prose” that hides missing CC coverage.
  *Mitigation:* enforce CC/Solution coherence (E.19) and keep invariants checkable via `CC‑GCORE‑…`.

## G.Core:8 - Common anti-patterns and how to avoid them {#common-anti-patterns-and-how-to-avoid-them}

* **Anti-pattern:** Restating CN‑Spec/CG‑Spec rules inside a `G.x` “for convenience”.
  **Avoid:** cite `A.19.CN` and `G.0` through `CC‑GCORE‑CN‑CG‑1`.

* **Anti-pattern:** Adding a fourth guard status (“unknown”, “maybe”, “probe-only”) as a separate decision value.
  **Avoid:** keep guard domain tri‑state; express “probe-only” as policy/branching and record via pins/audit.

* **Anti-pattern:** Treating mandatory invariants as “defaults” to centralize them.
  **Avoid:** keep invariants as invariants (CC‑GCORE‑* cited through canonical governing definitions); restrict the Default Governing Definition Index to true defaults (constants or conditional default-rules).

* **Anti-pattern:** Turning partial orders into scalar ranks silently.
  **Avoid:** keep set‑valued semantics unless a total order is explicitly declared by a comparator/policy.

* **Anti-pattern:** Competing defaults scattered across multiple patterns.
  **Avoid:** Default Governing Definition Index; delegate duplicate statements to the one governing definition.

* **Anti-pattern:** Local trigger tokens without canonical mapping.
  **Avoid:** provide/cite a `TriggerAliasMap` with namespace‑qualified aliases.

* **Anti-pattern:** Breaking public CC ids during dedup.
  **Avoid:** convert to delegation items; preserve IDs.

## G.Core:10 - Rationale {#rationale}

Universalization of Part G requires a stable "gravity center" for invariants, otherwise each pattern becomes a competing governing source. Delegation-first citation prevents duplication and makes governing-definition assignment explicit, while typed trigger kinds and the Default Governing Definition Index turn historically prose-driven drift into checkable, id-based structure.

## G.Core:11 - SoTA alignment (informative) {#sota-alignment-informative}

Although FPF is conceptual (not a data governance framework), `G.Core` aligns Part‑G authoring with modern best practice patterns seen across post‑2015 work:

* **Selective prediction / abstention** informs tri‑state guard discipline: abstaining or degrading is a first-class outcome, not an error coerced into a scalar.
* **Set-valued / conformal methods** motivate set-return semantics: when comparability is partial or uncertainty is structural, returning sets/regions is often the SoTA-friendly representation.
* **Multiobjective optimization and quality-diversity** reinforce declared set-result and `Archive` semantics instead of forced “best single scalar”.
* **Monotone constrained modelling** (where used) supports “legality-first” scoring/aggregation: constraints and admissibility precede optimization, mirroring CG‑Spec gate discipline.
* **Schema evolution and contract testing** motivate id-stable conformance points and typed trigger catalogues: stable identifiers + regression hooks are the practical mechanism for safe refactoring.


## G.Core:End {#end}

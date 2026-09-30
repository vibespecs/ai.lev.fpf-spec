# C.31.ASAP - Which Architecture Is Preferable Under Scale? (Scale Amenability): depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.31.ASAP:5 - Archetypal Grounding {#archetypal-grounding}

| Archetype | Without C.31.ASAP | With C.31.ASAP |
| --- | --- | --- |
| Product-line platform | Platform name is treated as scale-preference evidence. | Variability slots, extension rules, exception curve, and refactor triggers are declared before preference use. |
| Neural architecture block library | Reusing blocks is treated as reusable architecture by itself. | The alternative set names scale variable, interface grammar variants, exception growth, and source-return condition. |
| Safety or certification reuse | Reusable evidence package is counted without validation boundary. | Evidence reuse remains tied to source-return. An evidence-validity or safety claim is tested under its applicable domain rule. Use `A.10` for source recovery and bounded reliance, `G.6` for addressable provenance, and `B.3` when a named assurance claim is current. |
| Cross-scope residual | A frustration or complexity label is treated as scale mathematics. | C.31.ASAP names the scale window and residual slope; C.29 records the lens-use fields if the mathematical-lens use is being claimed. |

### C.31.ASAP:5.1 - Filled triage slice {#filled-triage-slice}

```text
ScaleClaimTriage:
  architectureAlternativeSetRef: product-line platform alternative vs bespoke customer-specific variants
  describedHolonRef: the regulated deployment platform and its site-specific variants
  claimScopeRef: preference claim for 5 to 40 named regulated deployment sites inside the current qualification boundary
  selectedContextSliceRefs: the named site, jurisdiction, and qualification-window slices admitted by that claim scope
  modelUseStructureRef?: absent; no independently selected bounded-model-use structure changes this use
  scaleVariableRef: N_sites
  scaleWindowRef: 5 to 40 regulated deployment sites inside the current qualification window
  claimedPreferenceUnderScale: platform alternative is preferred if interface variants and approval exceptions grow slower than bespoke variants
  slopeEvidenceRef, scaleProbeEvidenceRef, or noProbeReason: scale-probe evidence from six deployments; no universal scale law claimed
  expectedStableOrImprovingStructure: interface grammar, reusable test package, deployment work template
  exceptionGrowthRisk: jurisdiction-specific clauses and side-channel integrations may grow faster than sites
  sourceReturnCondition: return to exception register, interface variant log, and deployment evidence before publication, selected-set, assurance, or decision use
  relatedClaimGovernanceIfClaimed: C.31 for the characteristic; C.31.RSA for reusable-structure share; C.16 for measurement; A.19.CPM for comparison; G.5 for selected-set declaration; G.9 for parity; C.11 for local decision; A.10 for source recovery and bounded reliance; G.6 for addressable provenance; B.3 for a named assurance claim
  stopCondition: stop at local scale-preference guidance unless comparator admission, evidence validity, and decision or selected-set governance are present
```

Admissible move: prefer the platform alternative as a local scale-preference guide and start interface-grammar repair before deployment spread increases. Stop at local guidance; open the direct selected-set, evidence-sufficiency, assurance, gate, or decision pattern only when that downstream claim is current.

### C.31.ASAP:5.2 - Near-miss lowering slice {#near-miss-lowering-slice}

Near-miss: a team says the platform architecture should win because it has an 82 percent reusable-structure share, an RG-like coarse description, and "less bespoke debt" than the local variant.

Lowering replay:

- The platform label is a source cue, not scale-preference evidence; recover variability slots, extension rules, exception curve, and source-return condition first.
- The 82 percent reusable-structure share stays report-only under C.31.RSA until the scale variable, scale window, accounting basis, comparator admission, and admissible comparison relation are declared.
- The RG-like phrase stays with C.29 unless the mathematical-lens fields, preserved structure, lost structure, payoff, admissible use, and stop condition are recoverable.
- The "bespoke debt" label is lowered to waiver review when safety, law-domain, mission, assurance, or scale-probe overturn reasons may justify the local variant.

Stop C.31.ASAP use when the scale window, probe evidence or no-probe reason, comparator admission, or source-return condition is absent. Reopen it only after those fields are recoverable and the platform-label, share, lens, and waiver claims have their governing patterns.

## C.31.ASAP:6 - Bias-Annotation {#bias-annotation}

| Bias risk | C.31.ASAP correction |
| --- | --- |
| **Platform label bias** | Platform or product-line wording names a possible source context, not scale-preference evidence. Recover variability slots, extension rules, exception curve, refactor triggers, and source-return condition. |
| **Modularity-means-scalability bias** | A module count, interface count, or reusable-structure share is not a scale preference. Use C.31 and C.31.RSA first, then C.31.ASAP only when scale variable and scale window are named. |
| **Debt inflation bias** | A locally hand-engineered solution is called debt without checking deontic, safety, law-domain, mission, assurance, or scale-probe waiver reasons. |
| **RG proof bias** | RG, coarse-graining, fixed-point, or universality wording is treated as scale-preference proof. Use C.29 for lens recovery and keep scale preference in C.31.ASAP. |
| **Selection laundering** | The scale-preference claim is used as if it selected the architecture. Use `G.5` for selected-set declaration and `C.11` for local choice; use `G.9` when parity is current. |

## C.31.ASAP:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
| --- | --- | --- |
| `ModularThereforeScalable` | The text says modular or platform architecture scales without scale variable, window, slope evidence, or exception curve. | Add `ScaleClaimTriage` or downgrade to C.31 characteristic cue. |
| `GenericScaleAudit` | Audit fields appear with no architecture alternative set or preference use. | Return to `ScaleClaimTriage`; remove audit apparatus until preference use is being made. |
| `AllExceptionsAreDebt` | Any non-scale-amenable choice becomes debt. | Test waiver reasons and keep justified bounded exceptions out of `ArchitectureHeuristicDebt`. |
| `RGAsScaleProof` | Coarse-graining or RG wording is used as a scale-preference claim. | Apply C.29 for lens use and C.31.ASAP for preference claim; require source-return condition. |
| `ShareAsScalePreferenceEvidence` | `ReusableStructureShare` or `BespokeResidueShare` is used to prefer one alternative. | Keep the share report-only in C.31.RSA until scale variable, window, and admissible comparison are declared. |

## C.31.ASAP:10 - Rationale {#rationale}

`C.31` and `C.31.RSA` can expose scale-sensitive characteristics and reusable-structure residue, but they should not themselves decide which architecture alternative is preferable under scale. C.31.ASAP governs this architecture scale-preference claim family; it is narrower than general BLP and broader than one measurement card.

The pattern adapts BLP-style scale-amenability to architecture: prefer the alternative that preserves or improves reusable structure over a declared scale window when safety, law-domain, and assurance boundaries are comparable. Treat modularity, reuse, platform practice, and mathematical coarse-graining as candidate cues. Base the preference on the named scale variable and window, expected stable or improving structure, exception-growth risk, and available slope or scale-probe evidence or no-probe reason.

## C.31.ASAP:11 - SoTA-Echoing {#sota-echoing}

| Source family | Source-use relation | C.31.ASAP contribution | Practitioner use |
| --- | --- | --- | --- |
| Software product-line and variability-management practice (`https://www.sei.cmu.edu/library/variability-in-software-product-lines/`; `https://arxiv.org/abs/2605.21353`) | Mature variability lineage plus current SPLE-review cues. | Adopt variability slots, product-line reuse, exception inventory, and refactor triggers as architecture scale-preference fields. | Treat a product-line label, shared code base, feature model, or platform name as a cue. Before preferring the product-line alternative, name the scale window, variability slots, exception curve, and source-return condition. |
| Product-platform and modular product-architecture practice (`https://link.springer.com/article/10.1007/s00163-023-00427-1`; `https://arxiv.org/abs/2510.11089`) | Current engineering-design source line for modular product architecture, assembly orientation, product-family reuse, and manufacturing-aware modularity. | Adopt the product-family commonality and variety trade-off as an architecture scale-preference pressure: reusable structure needs declared variation points, interface rules, assembly or realization constraints, exception curve, and source-return condition. | Treat a product-platform name, common-module count, or modular-product label as a cue; establish any module-interface or manufacturing claim separately. Before preferring a product-platform alternative, state which product-family variation is scaled, which structure remains stable, and which assembly, safety, law-domain, or mission exception is allowed. |
| Platform-engineering maturity practice (`https://tag-app-delivery.cncf.io/fr/whitepapers/platform-eng-maturity-model/`) | Current platform-practice source for platform service set, extension-rule, substitution-policy, and maturity-pressure claims. | Adapt platform practice into extension-rule, substitution-policy, conformance-expectation, and exception-growth checks. | Treat platform maturity as a source cue until the architecture scale variable and exception behavior are declared. Establish any architecture selection or reusable-structure claim through its own pattern. |
| C.19.1 BLP in FPF | FPF-local preference discipline for general scale-amenable methods. | Specialize the preference idea to architecture alternatives, selected structures, scale variables, and architecture slope vector. | Use C.19.1 for method-family policy and C.31.ASAP for architecture scale preference; selector policy and decision records remain with their governing patterns. |
| C.29 RG and coarse-graining lens use in FPF | FPF-local mathematical-lens discipline. | Require scale window, coarse-graining rule, preserved structure, lost structure, and source-return condition when RG-like architecture scale reasoning is being claimed. | Use `MLU.Description@RGArchitecture` or `MLU.Description@MultilevelLearningFrustration` only when the lens changes the next admissible use. Establish any physical-RG, scale-proof, causal-proof, assurance, or selected-architecture claim through its own source basis and governing pattern. |


## C.31.ASAP:End {#end}

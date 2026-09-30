# C.31.RSA - Reusable Structure Accounting: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.31.RSA:5 - Archetypal Grounding {#archetypal-grounding}

**Tell.** Account for structure at declared loci under a declared accounting basis.

**Show.** In one architecture, reusable structure may be located in a template and interface grammar. In another, it may be located in a test package, regulatory argument, work method, or flow pattern. In a third, the reusable part may be small, but the bounded exception is exactly what preserves safety or local fit.

**Show.** A share can be useful as a local report. It becomes misleading when it hides which structure was counted, which structure was not counted, and when the reader must return to source records.

Holon and episteme: the structures being accounted over are selected architecture-relevant structures in context. The RSA description describes those structures; it records the local accounting slots, report-only share values, and any source-return condition.

### C.31.RSA:5.1 - Worked case: reusable evidence package, bespoke delivery work {#worked-case-reusable-evidence-package-bespoke-delivery-work}

Situation:

```text
A regulated product line has reusable component templates and a reusable test package.
Each customer delivery still repeats approval work and bespoke integration exceptions.
```

`ReusableStructureTriage`:

```text
describedHolonRef: product-line delivery system
reuseQuestion: which selected structures are reused and where does bespoke residue grow?
deploymentBoundary: regulated customer deployments
intendedAccountingUse: decide the next reusable-structure repair
claimScopeRef: reusable-structure accounting for regulated delivery
qualificationWindowRef: 2026Q3 regulated-delivery review window
architectureClaimRef: C.30 architecture claim for the product-line delivery system and its selected delivery structures
structureRefs:
  component template structure
  interface grammar structure
  evidence package structure
  delivery work structure
accountingRelationRefs:
  reuse, exception, and bespoke-residue relations for the named deployments
evidenceRefs:
  deployment, approval, integration-exception, and reusable-test-package records
whereReusableStructureCurrentlyLives:
  component template structure
  reusable test package
  interface grammar for standard variants
whereBespokeResidueCurrentlyGrows:
  customer-specific approval work
  integration exceptions outside interface grammar
  local evidence witnesses not covered by reusable package
residueRefactoredInto:
  workStructure + evidencePackage + interfaceSpecification
residueAcceptedAsBoundedException:
  customer-specific regulatory clause with declared non-admissible reuse
sourceReturnCondition:
  return to deployment evidence and regulatory exception record before assurance or gate use
relatedClaimPatternsIfClaimed:
  `A.10` for the evidence-validity claim's source-to-use basis; `G.6` when a citable provenance path is needed; `B.3` for assurance reliance; `A.6.M` for interface grammar when a module-interface claim is made; `C.16` for the measurement account; `A.19.CPM` for comparison under a declared comparator
stopCondition:
  report-only accounting unless comparator admission, evidence validity, and assurance validity are declared
```

Admissible move: publish the local report-only RSA note and refactor the repeated organization of delivery approval work into reusable work structure and reusable evidence structure. Non-admissible move: claim that the reusable evidence package proves every deployment or that a high reusable share makes the architecture better.

### C.31.RSA:5.2 - Anti-case: high share hides a bad architecture move {#anti-case-high-share-hides-a-bad-architecture-move}

Situation:

```text
A team reports that 85 percent of its architecture is reusable because most screens use one shared template.
The template makes many local exceptions necessary for product teams and side-channel integrations.
```

This is not a successful RSA result. The accounting basis counts template instances but hides interface relation cost, lost variation, hidden bespoke work, and evidence decay. The repair is to mark the share as report-only, add the missing bespoke-residue slots, and apply A.6.M, C.31, or a characteristic pattern governing the claim to the interface relation cost before any comparison or decision use.

Lowering replay: the team tries to use the 85 percent share to rank this template architecture above another product-line variant and approve the template program. The use is lowered to local report-only accounting because the comparator set, accounting-basis alignment, interface-cost measure, source-return condition, and decision record are absent. Before comparison or decision use, the interface grammar must be repaired under its direct pattern, using A.6.M when a module-interface claim is current, C.16 must govern the interface-cost measurement, A.19.CPM must govern comparison of the admitted profiles, A.19 must govern any CharacteristicSpace or reusable space predicate used, and C.11 must govern the local decision claim.

Stop condition: do not use the 85 percent share for outside-RSA ranking, gate, assurance, or decision. Reopen the RSA note when the interface grammar, exception register, or comparator set changes.

### C.31.RSA:5.3 - Transfer case: neural-network block replacement {#transfer-case-neural-network-block-replacement}

Situation:

```text
A model architecture replaces a repeated attention block with a hybrid SSM-attention block.
The benchmark improves, but cache placement, memory access, and ablation evidence change.
```

RSA can transfer from product-line architecture to neural-network architecture only after `C.30.STRAT` has treated `block`, `cache`, and related terms as source labels unless the reusable locus is already recovered. Then RSA names the declared structures and accounting basis:

- reusable structure may be located in recovered repeated-block topology, dataflow pattern, cache-placement rule, or evaluation harness;
- bespoke residue may be located in model-specific tuning, data distribution dependence, memory-layout exception, or ablation gap;
- benchmark gain is not reusable-structure accounting by itself;
- for evidence claims, use `A.10` for source recovery and bounded reliance, and `G.6` when a citable provenance path is needed; use `C.28` for causal claims and `C.29` for mathematical-lens or compression claims.

Admissible move: record which recovered structural locus was reused, what changed, what source distinctions must remain reachable, and which pattern defines or tests each benchmark, evidence, causal-use, or mathematical-lens claim. Non-admissible move: treat "block replacement improved the architecture" as RSA proof.

## C.31.RSA:6 - Bias-Annotation {#bias-annotation}

| Bias risk | C.31.RSA repair |
| --- | --- |
| Reuse-good bias | Do not treat more reusable structure as automatically better. Ask what repair, cost, or source-return condition follows. |
| Share-proof bias | Do not let `ReusableStructureShare` prove modularity, quality, or any outside-RSA use named in the claim-use boundary. |
| Hidden-unit bias | Do not sum templates, interface variants, work items, and evidence packages without a declared accounting basis. |
| Residue-bad bias | Do not treat every bespoke exception as waste. Some residue is a bounded exception that preserves local fit or safety. |
| Evidence-reuse bias | Do not count evidence reuse without validity context and source-return condition. |
| Compression bias | Do not let accounting hide distinctions needed for action, assurance, causal use, law-domain review, regulatory review, or subsequent decision reopening. |

## C.31.RSA:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
| --- | --- | --- |
| `ArchitectureAmount` | A reusable share is treated as an amount of architecture. | Restate as report-only share under one declared accounting basis. |
| `ResidueIsWaste` | All bespoke residue is marked bad. | Split repairable residue from bounded exception. |
| `HeterogeneousPseudoSum` | Templates, interface variants, work items, evidence packages, and exceptions are summed as if they shared one unit. | Declare accounting basis or keep the decomposition qualitative. |
| `EvidenceReuseAsAssurance` | Evidence reuse share is treated as assurance. | Recover the evidence-validity claim's source-to-use basis through A.10; use G.6 for a citable provenance path when needed and B.3 for assurance reliance. |
| `RSAAsC31Duplicate` | RSA repeats every modularity characteristic. | Keep RSA to reusable loci, bespoke residue, residual uncertainty, report-only shares, and source-return conditions. |
| `NoSourceReturn` | Accounting hides source distinctions used by downstream action. | Add `sourceReturnCondition` or narrow admissible use. |

## C.31.RSA:10 - Rationale {#rationale}

C.31.RSA is separate from C.31 because accounting over reusable structure answers a different question from choosing modularity characteristics. C.31 asks which characteristic changes action. C.31.RSA asks where reusable structure and bespoke residue are located under a declared accounting basis.

C.30 distinguishes an architecture relation from its selected structure. RSA does not define `StructureAmount`. A useful accounting description can still report shares, but only under declared structure refs, structural aspects, and an accounting basis.

The pattern also keeps residue ethically and practically neutral until interpreted. Bespoke residue can be a defect, a local necessity, a safety boundary, a regulatory constraint, or a deliberately accepted exception. The repair is to name which one.

## C.31.RSA:11 - SoTA-Echoing {#sota-echoing}

| Source or practice | Currentness or lineage use | Adopt and adapt for C.31.RSA | Rejected overread | Governing-pattern use and action consequence |
| --- | --- | --- | --- | --- |
| C.25 Q-Bundle discipline inside FPF | FPF-local discipline for decomposing quality-family claims. | Adopt separation of scope, measures, mechanisms, windows, evidence, and admissible use. In C.31.RSA this changes `ReusableStructureShare`: the share is report-only accounting under declared `accountingBasisRef` until the relevant outside-RSA use meets the conditions defined by its applicable pattern. | A reusable-structure share does not replace the underlying Q-Bundle, description, evidence relation, or decision record. | Apply `C.25` for quality-family decomposition and `C.16` for a measurement account; the practitioner may report a share locally but must not use it as proof without the governing pattern for that use. |
| ISO/IEC/IEEE 42010:2022 architecture-description, viewpoint, model-kind, and correspondence discipline (`https://www.iso.org/standard/74393.html`; `https://www.iso-architecture.org/ieee-1471/cm/`) | Current international standard and conceptual-model source for architecture-description and view discipline for this source-use decision. | Adopt explicit architecture description, source view, viewpoint, model-kind, correspondence, and conformance pressure. In C.31.RSA this changes source-return use: reusable-structure accounting names the structure refs, source view or architecture-description refs, correspondence refs, and source-return condition before any cross-view share is used. | A view, diagram, model kind, or correspondence label is not the reusable structure itself and does not make a share comparable, admissible for decision use, or assurance-bearing. | Apply `C.30` for architecture claims, `C.30.AD` for architecture-description use, `C.30.ASV` for structural-view use, and `E.17.0` for viewpoint conformance; RSA may count only after the selected structure refs and accounting basis are recoverable. |
| Modular Open Systems Approach (MOSA) and open-system acquisition or engineering practice (`https://www.cto.mil/sea/mosa/`; `https://www.cto.mil/wp-content/uploads/2025/03/MOSA-Implementation-Guidebook-27Feb2025-Cleared.pdf`) | Current engineering and acquisition practice family for modular interfaces, conformance, replacement, and supplier-diversity pressure. | Adopt the pressure to make reusable interface, conformance, substitution, and supplier-diversity structure explicit. In C.31.RSA this changes interface reuse: reusable interface accounting remains report-only until A.6.M has repaired the module-interface claim and its interface grammar, substitution policy, and version or change policy, and the conformance work and source or evidence relation are established through their direct patterns. The supplier-diversity relation likewise needs its direct predicate when that relation is being claimed. | Open interface label, API label, platform label, or supplier-diversity goal is not reusable structure, procurement suitability, assurance, gate passage, or decision authority by itself. | Apply A.6.M to the module-interface claim, including interface grammar, substitution policy, version or change policy, and conformance expectations; keep source or evidence relations and any claimed supplier-diversity relation under their direct patterns before RSA comparison or decision use. Use `G.5` for supplier-set result declaration or `C.11` for a procurement decision when that use is being made. |
| DSM, dependency, and product-architecture practice, including Eppinger and Browning DSM lineage | Mature architecture-analysis lineage still used for dependency and product-architecture reasoning; lineage, not a complete current standard. | Adopt typed dependency structures as possible source for reusable loci and bespoke-residue diagnosis. In C.31.RSA this changes dependency use: dependency counts, partitions, and clusters become candidate source fields only when declared `structureRefs`, structural aspects, and accounting basis are present. | Dependency count, cluster count, or DSM modularity score is not architecture amount, quality proof, or decision verdict. | Apply `C.31` to select modularity characteristics, `C.16` when the count or other result must be interpreted as a measurement, and `A.18` for scale-operation legality; apply `C.29` when graph, partition, compression, or C.29 lens-use result changes action. |
| Goodhart and Campbell proxy-pressure laws | General proxy-risk lineage for report-only shares, reuse scores, and benchmark-like accounting. | Adopt proxy-risk discipline for reusable-share use. In C.31.RSA this changes share use: a reusable-structure share remains report-only until the relevant outside-RSA use meets the conditions defined by its applicable pattern. | Reusable-share improvement, coverage improvement, or benchmark improvement is not value, assurance, evidence sufficiency, gate passage, or architecture decision by itself. | Before a reuse number guides selection or reliance, apply the corresponding measurement, quality-family, set-result, decision, evidence, or assurance pattern identified in section 12. |
| System-evolution, information-hiding, and effective-interface lineage | General holon-architecture lineage for reusable structure that changes over time and hides variation-prone structure. | Adopt evolution and hidden-change discipline. In C.31.RSA this changes residue interpretation: reusable loci, bespoke residue, hidden interface behavior, source-return conditions, and bounded exceptions are reopened when the structure edition, accounting rule, implicit interface, or reliance relation changes. | One-time reusable-share accounting is not sustainable fitness; a stable-looking interface or template does not prove future substitutability. | Reopen or lower the RSA result when hidden variation, implicit dependency, source distinction, or continuing adaptation changes the accounting meaning. |
| Software product-line engineering and variability-management practice, including Pohl, Boeckle, and van der Linden lineage plus current product-line and variability work (`https://www.sei.cmu.edu/library/variability-in-software-product-lines/`; `https://arxiv.org/abs/2605.21353`) | Mature product-line variability lineage plus current SPLE-review cues for variability slots, product-line reuse, platform extension rules, and reuse-rule discipline. | Adopt variability-slot and reuse-rule pressure. In C.31.RSA this changes product-line use: reusable structure may be located in template, interface, work, evidence, and exception loci, and bespoke residue must name repair direction, bounded exception, or source-return condition instead of being averaged into one share. | Product-line label, shared code base, feature model, or platform name is not enough to infer reusable structure or architecture scale-preference evidence. | Apply A.6.M when platform or interface wording carries a module-interface claim, C.31.ASAP for architecture scale preference, C.11 for choice, or G.5 for selected-set result declaration. |
| GSN Community Standard v3 and assurance-case reuse and safety-case reuse practice (`https://scsc.uk/gsn`; `https://arxiv.org/abs/2506.11023`) | Current assurance-case standard family plus current formalization work for this source-use decision; assurance validity remains context-sensitive. | Adopt the distinction between reusable assurance argument structure, reusable evidence structure, and context-specific validity witnesses. In C.31.RSA this changes evidence and assurance reuse: reuse remains accounting until evidence validity, safety-case use, or assurance reliance is governed by its own pattern. | Evidence reuse share or assurance-argument template reuse does not infer assurance, safety-case success, gate passage, or release permission. | Use `A.10` for the evidence-validity claim's source-to-use basis, `G.6` for a citable provenance path when needed, and `B.3` for an assurance claim, including one about safety-case support; add source-return condition and validity-window check before reliance. |
| Architecture-operation language, with neural-network and software-system discussions as source examples, including the GonzoML architecture-operation intake | Current practitioner-language source for structural substitution, gating, memory placement, cache placement, routing, ablation, pruning, distillation, and architecture search; not used as a current standard by itself. | Adopt the recognition that replacement and search expose reusable and bespoke structural loci. In C.31.RSA this changes architecture-operation use: source labels such as block, layer, expert, cache, router, gate, or pruning mask remain source labels until `C.30.STRAT` and the governing pattern for the claim being made recover `structureRefs`, aspect refs, accounting basis, repair actions, and source-return conditions. | Block, layer, expert, cache, router, gate, benchmark, ablation, pruning mask, or distillation success is not RSA slot ontology, architecture decision, evidence sufficiency, gate passage, assurance, or architecture adequacy by itself. | Apply `C.30.STRAT` first where source-label recovery is needed, then `C.30` or `C.30.ASV` for architecture claim and structural view, `C.30.TFS-REL` for flow changes, `C.29` for mathematical-lens or compression claims, `A.10` or `G.6` for the evidence-provenance account of a benchmark or evidence claim, and `C.28` for causal claims. |

**Source-currentness front.** Use the table's `Currentness or lineage use` cell as the source-use boundary. Rows named current, such as ISO/IEC/IEEE 42010:2022, MOSA guidance, current product-line or variability work, GSN Community Standard v3, current safety-case reuse work, and the architecture-operation corpus material used as current practitioner language, require source refresh before outside-RSA use when the named standard, guide, practice family, or corpus use changes. Rows named lineage, such as DSM or product-architecture lineage, Eppinger and Browning lineage, Goodhart and Campbell proxy-pressure lineage, system-evolution and information-hiding lineage, and Pohl, Boeckle, and van der Linden lineage, stay lineage unless a current source relation is explicitly recovered.

Refresh or lower the RSA result when a source-use change alters the reusable locus, bespoke-residue locus, accounting basis, source-return condition, comparator admission, evidence-validity relation, assurance or safety-case reliance, architecture scale-preference relation, or any outside-RSA use. A source row may explain why an accounting distinction matters, but it does not make an RSA share current for comparison, decision, assurance, gate, or publication without the applicable pattern for that outside-RSA use.

Older or local sources may serve as lineage or worked examples only when the row says so. They do not stand in for current competitive source, and they do not make an RSA share admissible for outside-RSA use without the governing pattern for that use.


## C.31.RSA:End {#end}

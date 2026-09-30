# A.1.CSD - Discovering Systems That May Bear Consequences: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.1.CSD:0 - Practitioner Entry {#practitioner-entry}

**Use this when.** Use this pattern when proposed or observed Work, realization, operation, use, maintenance, misuse, failure, recovery, retirement, policy, or change may alter Systems omitted from the current decision or investigation, and finding one of them could change a probe, constraint, alternative, monitoring condition, explanation, or reopen decision.

Ask: **Which other Systems may undergo a relevant change, through what supported relation or still-modal path, and what should the receiver do next?**

**First useful move.** Name the exact focus and receiver. Generate a small set of concrete change-producing possibilities, trace outward through supported direct relations or explicitly modal path claims, and challenge the current boundary for a missing bearer.

**First useful result.** Return the smallest bounded consequence account useful to the named decision or investigation. A qualified claim, retained constraint or alternative, modal path, or explicit unknown can finish the answer with its material limit. Further discovery is selected only when its obtainable contribution warrants the whole burden.

**Cheap stop.** Stop if the current bearer set and consequence claims already support the receiver at the declared configuration, scope, horizon, and evidence window. Also stop the affected claim branch when an exact non-System finding or missing relation blocks its next claim; return that finding to its direct owner instead of inventing a System.

**What goes wrong if missed.** A familiar participant list becomes the boundary of inquiry, a possible path is reported as an obtaining relation, a scale label stands in for a constructed whole, or unlike changes disappear inside one aggregate. The receiver closes while a cheap observation or alternative could still have changed it.

**What this buys.** The practitioner gets a reviewable set of possible bearers, relation-status claims, changed characteristics, evidence limits, and a useful receiving result without importing a full domain impact, risk, due-diligence, or assessment procedure.

**Not this pattern when.**

- If one proposed entity must first be tested as a `U.System`, use `A.1.SCR`.
- If the current question is an already named direct relation, use its A.6 governor.
- If the receiver relies on a causal effect, intervention, or counterfactual claim, use `C.28` for that claim.
- If the current question is comparison or choice among configurations, use `C.11.CRC` and `C.11` after the needed bearer claims exist.
- If the domain already has a qualified discovery Method with its own quantities, thresholds, evidence rules, and authority, use that Method; use A.1.CSD only for the shared early discovery result.

## A.1.CSD:0.1 - Precision Restoration {#precision-restoration}

| Expression | Working meaning here |
| --- | --- |
| consequence-bearing System | An actual `U.System` whose state or characteristic may change under the stated conditions. This is a plain description, not a kind, role, assignment, or status. |
| intended System referent | A designator for a System whose intended existence is stated in a modal claim. It does not assert current systemhood or existence. An unidentified bearer remains an explicit unknown with the claim's modality preserved. |
| supported obtaining direct-relation occurrence | One exact world-side relation occurrence whose participants, predicate, and obtaining conditions are supported under its direct governor. |
| modal path claim | A claim that a path may obtain, naming the proposed relation kind, candidate participants, conditions, support, and uncertainty. |
| consequence claim | A claim about a possible or observed changed state or characteristic, its bearer, conditions, time, support, uncertainty, and causal status. The claim is not the world-side change. |
| affected-System consequence account | One ordinary `C.2.1` episteme identified by one exact `<ClaimGraph, EntityOfConcern, effective ReferenceScheme>` triple. It is not a new result kind or the bearer Systems themselves. |
| receiver | The exact decision or investigation that can use the account. It is a neighboring use, not part of the account's identity triple. |

Affectedness creates no `AffectedSystem`, `ConsequenceBearingSystem`, `AffectedSystemRole`, `ImpactRelation`, `U.Level`, priority, aggregate, or decision. Use each stronger claim only under its direct owner.

## A.1.CSD:5 - Four First-Screen Situations {#four-first-screen-situations}

| Working situation | First action | First useful result or stop |
| --- | --- | --- |
| A flood-pump modernization may shift load, maintenance demand, downstream flow, and failure exposure. | Name the configuration decision, trace the finite change through supported plant relations and modal operating paths, and challenge the selected boundary. | Return an additional pump, maintenance, downstream, or containing-System claim when it changes a design constraint or monitoring condition. Finish if the current account already supports the configuration decision. If a missing relation blocks the next needed claim, stop that branch and name the exact missing relation. |
| An on-call and platform arrangement is being reorganized. | Trace the proposed Work and assignment changes to employee, provider, service, customer, and neighboring organization Systems without treating those names as a level ladder. | Keep workload, capability, service, and organization consequences separate; return the missing bearer or relation to the organization-change Method. |
| A public appointment service is being redesigned through facilitated inquiry. | Trace service and policy alternatives to applicant, staff, provider, transport, and other material Systems; use participation as a discovery source, not proof of systemhood or authority. | Return descriptive bearer claims to the facilitated inquiry; route participation, concern, and authority questions to their direct practice. |
| A nutrient pulse in a bioreactor may change living and engineered Systems. | Trace supported feed and effluent relations separately from modal biological and operating paths, and recover actual whole/part facts. | Return the separate consequence claims and current limit; select spatial sampling, pressure observation, or effluent measurement only when their individual and combined contribution warrants the programme. |

The same discovery action changes all four situations. Their domain Methods, quantities, evidence rules, and decisions remain different.

### A.1.CSD:5.1 - Minimally Viable Worked Case: Nutrient Pulse {#minimally-viable-worked-case-nutrient-pulse}

In this constructed case, `FeedPulsePlan-FP4` proposes a larger nutrient pulse for `BioreactorOperatingSystem-BR7`. The receiving investigation is `ProbeDecision-PD4`: decide whether and which further observations are worthwhile before changing the feed setting for the next 48 hours. The plan is the account's one exact focus EntityOfConcern; the ClaimGraph examines the possible feed-operation occurrence it specifies rather than treating the plan as a physical cause. The probe decision is the account's neighboring use.

Baseline instrumentation supports one obtaining substrate-transfer occurrence from `FeedLine-F2` into the reactor medium and one obtaining effluent-flow occurrence from `BR7` to `TreatmentTrain-TT2`. Microscopy and persistence observations support the constructive recognition of individual bacterial Systems and `BiofilmPatch-BP3`: matrix-linked constituents, persistent assembly, whole-level nutrient-processing and shear-resistance characteristics, and actual participation in nutrient transformation establish the patch as a distinct System. The exact constituent relations used for the patch are recorded under their part-whole governors. No generic impact edge is added.

The proposed larger pulse has not occurred. The account therefore keeps four paths modal:

| Candidate bearer | Modal path and possible changed characteristic | Support and uncertainty | Receiver connection |
| --- | --- | --- | --- |
| sampled individual bacterial Systems near the inlet | Larger pulse -> higher local substrate concentration -> changed individual metabolic states and sample-level viability distribution. | Baseline gradient observations support plausibility; the proposed concentration field is unmeasured. | Retain the local-exposure limit; spatial sampling could distinguish inlet and bulk responses in a selected bounded trial. |
| `BiofilmPatch-BP3` | Larger pulse -> changed growth and matrix production -> changed patch coverage and shear resistance. | Current patch identity and coverage obtain; the proposed growth response remains model-supported and uncertain. | Preserve the current pulse alternative; short-window images may leave the growth response unresolved. |
| `BioreactorOperatingSystem-BR7` | Changed patch coverage and local transfer -> changed transfer efficiency and pressure drop. | Baseline pressure and transfer measurements obtain; the coupling under the larger pulse remains modal. | Preserve the pressure/transfer constraint; a trace during a selected trial could test the proposed coupling. |
| `TreatmentTrain-TT2` | Changed reactor effluent composition -> changed incoming load and treatment performance. | The effluent connection obtains; the proposed composition and downstream response are unmeasured. | Keep the downstream-load limit visible; an effluent observation could change whether a tested pulse may continue. |

The account keeps bacterial, biofilm, reactor, and treatment-train characteristics separate. It does not average them into one score. Its discovery residual names an observed unattached aggregate outside `BiofilmPatch-BP3`. Current evidence supports treating the observed members as a collection; whether that collection also forms a whole/System remains `unknown` because assembly, persistence, and the kind-specific A.1 facts are unsupported. The aggregate's whole identity does not alter this receiving decision in the case, so it remains an explicit unknown. If later reliance needs that identity, the relevant A.1/C.13 evidence would concern stable assembly, persistence, and whole-level behavior across observations; acquiring it still needs a worthwhile receiving contribution. Recover those facts before classifying it; only supported failure of a required A.1 component or condition warrants a negative System result.

The current pulse remains available while the larger pulse's consequences are modal. For the inquiry choice, suppose the domain investigation supplies these attainable contributions and full efforts, including preparation, any required trial operation, observation, and individual interpretation: spatial sampling can distinguish local exposure within 48 hours for one staff-hour; a pressure trace can qualify the transfer constraint for one hour; and an effluent observation can address downstream load for one and a half hours. Those answers could change the admissible pulse comparison. A two-hour imaging series would not discriminate the growth response in this window. These are illustrative planning premises, not biological thresholds or observed effects.

The programme has four available staff-hours after existing duties and adds half an hour of shared coordination and joint interpretation. All four proposed observations would take six hours and exceed that capacity. Spatial sampling, pressure observation, and effluent measurement together take four hours, finish in the receiving window, and supply the worthwhile discriminating contribution. The inquiry selects that programme while retaining the current pulse alternative and the unresolved biofilm-growth and aggregate-identity claims. If access, interpretation capacity, protection, or trial authority cannot support it, the available result is the qualified account with the current setting retained.

The domain practice governs whether any trial or subsequent feed change is admissible. Selecting observations neither performs them nor establishes their outcomes, causal effects, or permission. Reopen when a new whole becomes material, the feed configuration changes, an observation reverses a path claim, or the programme's contribution or feasibility changes.

## A.1.CSD:6 - Bias Annotation {#bias-annotation}

| Bias risk | Failure | Repair |
| --- | --- | --- |
| Visible-system closure | Only Systems already named by the current project or investigation are considered. | Trace outward from concrete possibilities and challenge the current boundary. |
| High-agency bias | Systems unable to speak, decide, or participate are omitted. | Apply A.1 systemhood and consequence relevance; neither voice nor agency is required. |
| Relation promotion | A plausible arrow becomes an obtaining world-side relation. | Keep the modal path claim distinct; add a separate actuality claim only when its direct predicate and case conditions are supported. |
| Level ladder | Familiar scale words are treated as Systems in a fixed hierarchy. | Recover exact holons, scopes, construction, crossings, and any real whole-reidentification question. |
| Aggregate closure | A total hides changed characteristics, evidence, or receivers on one side. | Preserve the original coordinates and make any aggregate an additional domain result. |
| Causal overread | Sequence, association, or model output is treated as an effect of intervention. | Keep the narrower claim and use `C.28` when the receiver relies on causality. |
| Completeness theatre | A long list is presented as exhaustive. | Use a receiver-relative stop and retain the material residual; select additional discovery by its attainable contribution and complete burden. |

## A.1.CSD:8 - Common Failures and Repairs {#common-failures-and-repairs}

| Failure | Symptom | Repair |
| --- | --- | --- |
| Actor-list substitution | The search repeats owners, users, operators, or interface participants. | Begin from possible changes and trace beyond the current list. |
| Mention inflation | Every nearby entity is called affected. | Require a possible or observed changed state or characteristic and a receiver connection. |
| Affectedness as kind or role | A bearer is assigned a new universal category or duty. | Keep affectedness in qualified claim content; use existing kinds and direct relations. |
| Diagram proof | An arrow or model edge is treated as an obtaining relation. | State its status, participants, conditions, support, and uncertainty. |
| Collection-to-System jump | A population, fleet, community, or aggregate is treated as one acting whole. | Apply A.1/C.13 to the exact candidate whole or retain the collection. |
| Scale trump card | One constituent or larger whole receives automatic priority. | Preserve each consequence coordinate; route any comparison or priority claim to its owner. |
| Universal assessment form | Every case must fill a domain-sized template. | Return the thin account that changes the receiver and name the residual. |
| Negative catalogue | The result mainly lists what was not found. | Return usable bearer claims, probes, direct-owner exits, and the honest blocker. |

## A.1.CSD:10 - Conditional Consumer Boundary {#conditional-consumer-boundary}

The core account ends before stronger neighboring claims. Continue only when the next question is current:

| Next question | Continue through |
| --- | --- |
| Does evidence support a retained claim, and may it be relied on now? | `A.10`, with `C.27` for temporal adequacy and `B.3` for assurance. |
| Does a claimed effect, intervention, or counterfactual have adequate causal support? | `C.28`. |
| Does a mathematical scale, aggregation, optimization, or representation lens preserve what the receiver needs? | `C.29`; use `C.30.ILC` only for a current cross-scope architecture residual. |
| Would a particular further inquiry warrant its full attainable burden? | `C.11.DUA`; `A.15.9` for a selected outside-practice contribution. |
| How does a finite configuration change compare, and what is chosen? | `C.11.CRC`, then `C.11`. |
| Does a later question concern value, benefit, harm, responsibility, admissible sacrifice, or an actual interlevel conflict? | Enter through `D.1`; use `D.2` for multilevel entry, `D.3` for an actual conflict description, `D.4` for mediation or decision use, and `D.5` for its bounded audits. |

For the last branch, one admissible D.1 value-frame edition is multilevel holonic consequentialism: inspect consequences for every constructively identified affected holon without automatic priority for a person, collection, or larger whole. That frame is conditional and plural under D.1. It adds no field to the A.1.CSD account. Establish any conflict, priority, or decision claim under its direct pattern.

## A.1.CSD:11 - Rationale {#rationale}

A.1.SCR answers whether one proposed entity is a System. A.1.CSD begins after a focus is current and asks which other Systems may undergo relevant changes. Merging the two would burden every systemhood check with an open-ended consequence search and would confuse candidate generation with recognition.

A.1.STM locates one unsupported answer across a long dependency; C.28 qualifies one causal-use claim; C.11.CRC constructs a finite comparison. None generates the bounded bearer/path/change account at comparable effort. A.1.CSD therefore stays a thin sibling in the A.1 family and returns each stronger claim to its direct owner.

The result remains an ordinary C.2.1 episteme because the recurring need is a reusable set of qualified claims, not a new world-side kind or relation. One focus fixes the account's EntityOfConcern within its C.2.1 identity triple; claims about several bearers give it content.

## A.1.CSD:12 - SoTA Echoing and Source Use {#sota-echoing-and-source-use}

Each row distinguishes a descriptive result, constructive Method, normative premise, or institutional preference; it retains only the action supported for this use.

| Source line | Claim and practical action retained | Adoption status and boundary |
| --- | --- | --- |
| Ulrich and Reynolds, [Critical Systems Heuristics: The Idea and Practice of Boundary Critique](https://doi.org/10.1007/978-1-4471-7472-1_6), 2020 | Boundary critique is an argued reflective and discursive Method. It changes practice here by adding an outside-in challenge after forward tracing. | **Adapt.** Retain the boundary challenge; do not import its complete normative programme, twelve-question form, System recognition, completeness claim, or scale priority. |
| OECD, [Guidelines for Multinational Enterprises on Responsible Business Conduct](https://doi.org/10.1787/81f92357-en), 2023, and [Due Diligence Guidance](https://doi.org/10.1787/15f5f4b3-en), 2018 | The guidance supplies an operational mapping and reassessment Method for actual and potential consequences across operations and remote relationships. It changes practice by widening path generation and reopening after conditions change. | **Adapt.** Enterprise duties, rightsholders, severity priorities, remedy, and authority remain domain results; publication status is not evidence of effectiveness. |
| European Commission, [Better Regulation Toolbox 2023](https://commission.europa.eu/system/files/2023-09/BR%20toolbox%20-%20Jul%202023%20-%20FINAL.pdf), Tool 18 and Chapter 2 | The institutional procedure distinguishes direct/indirect, intended/unintended, positive/negative, and one-off/recurrent consequences and asks for proportionate depth. | **Adapt.** Retain path and horizon prompts; reject its affected-group list, territorial ladder, reporting categories, monetization preference, and form as universal ontology or work order. |
| NIST, [AI Risk Management Framework 1.0](https://doi.org/10.6028/NIST.AI.100-1) and [Map playbook](https://airc.nist.gov/airmf-resources/playbook/map/), checked 2026-08-26 | The framework and playbook add misuse, repurposing, downstream factors, external feedback, later conditions, and continuing remapping as prompts. | **Adapt.** Reject AI actor classes, ready scale lists, risk taxonomy, governance apparatus, and aggregate score as general FPF results. |
| ISO/IEC/IEEE [24748-7000:2022](https://www.iso.org/standard/84893.html), IEEE [7000-2021](https://standards.ieee.org/ieee/7000/6781/), and ISO/IEC/IEEE [15288:2023](https://www.iso.org/standard/81702.html) | These normative engineering standards provide implementable traceability and iterative/lifecycle attention. They change practice by keeping selected concerns linked to concepts, requirements, design choices, and later observation. | **Adapt conditionally.** Conformance and involvement do not prove bearer completeness, discovery effectiveness, System construction, representation, or authority. The full processes stay in engineering practice. |
| Friedman and Hendry, [Value Sensitive Design, 2nd ed.](https://mitpress.mit.edu/9780262553254/value-sensitive-design/), 2026, and the authors' [current Method account](https://vsdesign.org/vsd/) | Current VSD retains direct/indirect stakeholder and value-scenario prompts and multi-lifespan attention. Value scenarios can widen social/design path generation. | **Adapt conditionally.** Human-value orientation is a normative premise, not the A.1.CSD admission test. Route Diverse Voices and tech-policy participation to the direct domain practice. |
| U.S. EPA, [Conducting an Ecological Risk Assessment](https://www.epa.gov/risk/conducting-ecological-risk-assessment) and [EcoBox analysis material](https://www.epa.gov/ecobox/phases-era-analysis), checked 2026-08-26 | Laboratory, field, monitoring, and modeled practices support stressor-to-receptor tracing, exposure/effect separation, time, recovery, uncertainty, and evidence-producing questions. They provide the neutral living-System stress test. | **Adapt.** Organism, population, community, and ecosystem are prompts, not a ready FPF holarchy. Regulatory endpoints, adversity judgments, risk estimates, and the complete ecological procedure remain domain results. |

These sources converge on path tracing, boundary challenge, proportional inquiry, qualified uncertainty, and reopening. Their taxonomies, normative ends, calculations, evidence thresholds, and authority do not converge and are not imported.


## A.1.CSD:End {#end}

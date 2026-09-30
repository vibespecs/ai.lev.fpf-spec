# E.23.CDI - Developing Capability for a Named Work Family {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Tech-name:** `WorkFamilyCapabilityDevelopmentMethod`
> **Plain-name:** develop a System's capability for named work and check it in representative work
> **Type:** Method-description pattern for a separate capability-development Method; coordinated with `E.23`
> **Status:** Candidate
> **Normativity:** Normative unless marked informative

## E.23.CDI:1 - Problem frame {#problem-frame}

Use this pattern when one named System must become more capable of performing a named Work family and transfer must later be checked in representative Work. The holder can be, for example, a person, team, organization, pair, ensemble, engineering arrangement, operating arrangement, or another collective. In every case, that whole must be independently admitted as the System whose capability is at stake.

**First useful move.** Keep the opening ordinary. Write two short sentences. `Current:` name the holder, named Work family, operating envelope, current measures and evidence, the contribution that currently limits performance, and how long that account remains current. `Target:` name the desired measures or success predicate, representative Work that will test them, intervention and any provider, and trade-offs that must remain protected. Use only values that can change the development decision. If the holder or Work family cannot be named, stop before choosing training, tooling, or another intervention.

**What goes wrong if missed.** Attendance, an exercise score, a certificate, a published description, or successful provider Work can be mistaken for changed capability. A development programme can then optimize visible activity while the holder still cannot perform the target Work under its real conditions.

**What this buys in practice.** The project develops the capability that matters for named Work, directs effort at a real limitation, protects important conditions, and tests transfer where the capability will be used. It can stay small: use the two-sentence entry.

**Not this pattern when.**

- Use `A.2.2` when only a holder's identity, qualified ability, measures, support or current reliance is current.
- Use `E.23.CAE` first when previous performance or failed transfer leaves it unclear whether the live issue is envelope, configuration, applicability selection, access or activation, context-dependent expression, adaptation, enactment, or actual capability change. Its disposition is a premise, not selection of development Work.
- Use `E.22` when one evaluation question is current and no development Method is needed.
- Use base `E.23` for repeated improvement of an arbitrary object version.
- Use `C.32.MWA` first only when the target-practice architecture must itself be recovered or compared.
- Use a population assessment for a distribution or statistic over member capabilities, and `C.36` for cultural generation, transmission, recognition, selection, retention, or loss.

## E.23.CDI:2 - Problem {#problem}

Capability development is often organized around available courses, tools, exercises, providers, or credentials. Those can contribute to an intervention, but none tells the project which System must become capable, which Work family matters, which contribution is limiting, or whether the change transfers.

The opposite mistake is to demand one universal decomposition or balanced scorecard. Human, technical, organizational, artistic, and hybrid holders can require different capability characteristics and different development Methods. The reusable part is the problem-solving move, not one curriculum, provider architecture, or scale.

## E.23.CDI:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Target-Work relevance | Exercises can be cheap and controlled, while the capability must hold in representative Work. |
| Holder precision | A group label is convenient, while capability belongs to the exact admitted System whose ability is claimed. |
| Shared Method versus domain filling | The development move recurs across domains, while Methods, measures, evidence, and constraints remain domain-specific. |
| Provider leverage | Coaching, tooling, infrastructure, or another provider contribution may matter, while provider success is not holder capability. |
| Focus versus protected conditions | One limiting contribution needs attention, while safety, autonomy, continuity, service, cost, or another protected condition must not be sacrificed. |
| Evidence versus proxy | Exercises and descriptions support learning, while transfer requires evidence from representative Work. |

## E.23.CDI:4 - Solution {#solution}

### E.23.CDI:4.1 - Name the holder and target Work {#name-the-holder-and-target-work}

Keep the holder System, its capability, the target Work family, development intervention, provider Systems, development Work, transfer Work, and evidence separate. A familiar group name does not by itself identify the capability holder.

| Candidate holder wording | Boundary for this use |
| --- | --- |
| a person or equipped person | Use the person or equipped whole only when that System is the bearer of the bounded capability claim. |
| a team or organization | Use the team or organization only when the whole is admitted as one System for the target Work; member capabilities do not aggregate automatically. |
| a pair or ensemble | Use the pair or ensemble when joint performance is the capability at stake; do not distribute that claim to every member. |
| an engineering or operating arrangement | Use the whole arrangement only when its boundary and relevant conditions are recoverable; tools, people, and providers remain separately identifiable participants. |
| a population | Treat the population as holder only when that whole independently satisfies the System boundary for this claim. Otherwise keep member capabilities separate, assess their distribution separately, and use `C.36` for cultural propagation. |

### E.23.CDI:4.2 - Apply the Method {#apply-the-method}

1. Start from an evidence-backed account of the domain Methods needed for the named Work and how their contributions relate.
2. Name the operating envelope and the qualification window or currentness condition that can change whether the Work succeeds.
3. State the current capability baseline and desired result before choosing an intervention: the decision-bearing current measures and evidence, the desired measures or success predicate, and the trade-offs that must remain protected. The desired result is a target for later evaluation, not an established current ability or an actual change.
4. Find the contribution that is missing, limiting, or poorly coordinated.
5. Choose an intervention directed at that limitation, and name any provider System on which the intervention relies. The intervention may use, for example, practice, coaching, adaptation, tooling, changed support, or a changed Method; the receiving domain supplies the actual choice.
6. Carry the protected conditions into the chosen intervention. Keep the selected intervention or plan separate from any development Work that is later performed.
7. Declare a transfer check that tests the stated target in representative Work under the relevant operating conditions. When that check is performed, keep the transfer Work, its evidence and result, and the resulting capability statement or currentness assessment separate. An exercise, description, publication, attendance record, or provider delivery is not that transfer check.
8. Reopen the Method account, holder boundary, baseline, target, intervention, protected conditions, or currentness claim when the transfer evidence shows that the earlier account was wrong, incomplete, or no longer current.

### E.23.CDI:4.3 - Return the first useful result {#return-the-first-useful-result}

The first useful result names the admitted holder System, target Work family, current capability baseline, operating envelope, decision-bearing measures and evidence, qualification window or currentness condition, desired measures or success predicate, current limiting contribution, selected intervention and any provider dependency, protected conditions, representative transfer check, and reopen condition. If member distributions or cultural propagation are also current, return their separate assessment or C.36 result. A population can be the capability holder only when that whole is independently admitted as the System.

The exact holder, its qualified `A.2.2` ability claim and the basis for relying on the current baseline must be recoverable. The practitioner-facing result can still remain the two short sentences above plus the evidence used for the baseline and transfer result. Expose record identifiers, a separate `E.22` evaluation frame, or detailed provider and service relations only when a receiving use needs them.

Keep the selected intervention or plan, performed development Work, performed transfer Work, transfer evidence and result, pre- and post-intervention capability statements, a comparison claiming capability change, and any actual Transformation claim separate. A plan remains prospective. For performed Work, recover each exact actual performer through A.13 and let A.15.1 independently admit the occurrence; add F.6 only when the record or receiving use expressly consumes precise assignment-bound attribution. A capability-change comparison needs commensurable measures, envelopes, windows, and current support; it does not by itself say that the development Work caused a world-side change. A causal Transformation claim additionally needs an independently identified `A.3.4` Transformation and a named obtaining Work-to-change predicate or a supported local claim under `A.6.RCD`. Completion of development or transfer Work alone establishes none of these later claims. If the direct relation is missing, retain the Work, evidence, capability statements, and comparison and return that exact blocker.

## E.23.CDI:7 - Conformance Checklist {#conformance-checklist}

| Check | Passing condition |
| --- | --- |
| `CC-E23CDI-1` | @fact:CC-E23CDI-1 One admitted holder System and one named Work family are explicit. @status:spec/work |
| `CC-E23CDI-2` | @fact:CC-E23CDI-2 Before intervention selection, the current capability baseline names its operating envelope, decision-bearing measures and evidence, qualification window or currentness condition, and limiting contribution. @status:spec/work |
| `CC-E23CDI-3` | @fact:CC-E23CDI-3 Before intervention selection, the desired measures or success predicate and protected conditions are explicit; the desired result is not presented as an established current ability or actual change. @status:spec/work |
| `CC-E23CDI-4` | @fact:CC-E23CDI-4 The intervention addresses the limitation; any provider System and provider contribution remain distinct from the holder's capability, and a selected plan remains distinct from performed development Work. @status:spec/work |
| `CC-E23CDI-5` | @fact:CC-E23CDI-5 Transfer tests the declared target in representative Work under the relevant envelope and window; attendance, exercise completion, description, publication, or provider delivery is not substituted. @status:spec/work |
| `CC-E23CDI-6` | @fact:CC-E23CDI-6 The plan, performed development Work, performed transfer Work, evidence and result, pre- and post-intervention capability statements, capability-change comparison, and any actual Transformation claim remain separate. The comparison uses commensurable measures, envelopes, windows, and current support. A causal Transformation claim cites an independently identified Transformation and an obtaining direct Work-to-change predicate or supported local claim; otherwise the exact missing-governor blocker remains. @status:spec/work |
| `CC-E23CDI-7` | @fact:CC-E23CDI-7 A population is not treated as capable by aggregation. Member distributions and cultural propagation have separate results unless the population whole is independently admitted as the holder System. @status:spec/work |
| `CC-E23CDI-8` | @fact:CC-E23CDI-8 The result states what evidence, expired qualification window, changed operating condition, or failed transfer result reopens the baseline, target, Method account, holder boundary, intervention, protected conditions, or currentness claim. @status:spec/work |

## E.23.CDI:9 - Consequences {#consequences}

The same Method can guide human, organizational, artistic, engineering, operating, technical, or hybrid capability development without copying one domain's curriculum or measures into FPF. Receiving DPFs still supply the actual domain Methods, characteristics, interventions, providers, evidence, protected conditions, representative Work, and transfer limits.

The added cost is that a project must identify the holder and target Work before buying or designing an intervention, and it must test transfer rather than closing on activity. That cost prevents training, tooling, publication, or provider delivery from becoming a proxy for capability.

## E.23.CDI:12 - Relations {#relations}

| Pattern | Relation |
| --- | --- |
| `A.1`, `A.2.2` | Admit the holder System and govern qualified ability claims, their work conditions and attained bounds, support, qualification and fit. |
| `A.3.1`, `A.3.2` | Govern the domain Methods and their descriptions used by the development account. |
| `A.13`, `A.15.1`, `A.2.1`, `F.6` | Govern exact actual-performer recovery and independent admission of performed development and transfer Work. Assignment and F.6 enter only for an expressly consumed precise assignment-bound attribution. Completion of either Work occurrence does not establish a post-intervention capability or actual capability change. |
| `A.3.4`, `A.6.RCD` | Govern an independently identified actual Transformation and the obtaining direct Work-to-change predicate or supported local claim needed when development Work is said to have caused that change. When neither route is available, keep Work and Transformation separate and return the exact missing-governor blocker. |
| `A.19`, `C.2.1`, `A.10`, `B.3` | Govern comparison of declared measures, capability statements, and the evidence, ordinary reliance, or assurance relations that support their use. These epistemes and relations are not the holder's actual ability, an actual Transformation, or a causal Work-to-change claim. |
| `E.22` | Frames the capability or transfer evaluation when that question needs an explicit evaluation use. |
| `E.23` | Supplies the general improvement boundary and routes here when capability development for named Work is the live question. |
| `E.23.CAE` | Supplies an observation-qualified differential and candidate routes when apparent loss or failed transfer remains ambiguous. Capability development enters this pattern only after a separate applicable steering or choice result selects it. |
| `C.32.MWA` | Supplies a practice-architecture result only when the target-practice Method architecture must first be recovered or compared. |
| `C.36` | Governs distributed cultural generation, transmission, recognition, selection, retention, and loss; use `A.2.2` for a capability claim about an independently admitted population holder System. |
| `E.13` | Tests proxy-to-value alignment when attendance, scores, credentials, or another visible measure begins to replace the intended capability and transfer result. |


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/A-2-2#root, spec://ai.lev/fpf-spec/contract/A-3-1#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, spec://ai.lev/fpf-spec/contract/E-22#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-23-CAE#root, spec://ai.lev/fpf-spec/contract/C-32-MWA#root, spec://ai.lev/fpf-spec/contract/C-36#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-15-11#root, spec://ai.lev/fpf-spec/contract/A-2-2#root, spec://ai.lev/fpf-spec/contract/C-32-MWA#root, spec://ai.lev/fpf-spec/contract/C-36-RP#root, spec://ai.lev/fpf-spec/contract/E-23-CAE#root, spec://ai.lev/fpf-eng-hcd/contract/HCD-1#root, spec://ai.lev/fpf-eng-hcd/contract/HCD-15#root, spec://ai.lev/fpf-eng-mdpe/contract/MDPE-10#root, spec://ai.lev/fpf-eng-mdpe/contract/MDPE-23#root, spec://ai.lev/fpf-eng-oce/contract/OCE-8#root, spec://ai.lev/fpf-eng-syse/contract/SYSE-45#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-23-CDI

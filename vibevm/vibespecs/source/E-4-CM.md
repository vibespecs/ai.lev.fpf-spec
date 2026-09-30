# E.4.CM - Develop Composite Methods as Framework Contributions: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## E.4.CM:5 - Archetypal Grounding {#archetypal-grounding}

### E.4.CM:5.1 - Assemble a comparison that another reader can use {#assemble-a-comparison-that-another-reader-can-use}

A team has two public operations: grouping records and comparing paired observations. Its receiving question requires each error/non-error pair to share both setup and temperature. The existing grouping uses only setup.

The available data are T1=(error, S1, warm), T2=(acceptable, S1, cool), T3=(error, S2, warm), T4=(acceptable, S2, warm). Grouping by setup offers T1–T2 and T3–T4. Only the latter satisfies the comparison's precondition.

The author locates a composition difficulty: the producer's grouping key is weaker than the receiver's eligibility rule. The repair groups by setup and temperature, returns T3–T4 as eligible and makes the missing S1 comparison explicit. Comparison then uses the eligible pair; it cannot claim a result for S1. A request for another record is warranted only if that unresolved use matters.

This is already developed in C.40.CD:5.1. E.4.CM therefore selects reuse of that explanation rather than another pattern for these same operations. If a proposed card merely lists grouping and comparison, it should point to the available construction instead of asking the reader to invent the missing key.

Now change the receiving rule to require a shared instrument revision too. Temperature matching alone no longer answers eligibility. If revisions are present, extend the key; if absent, return the unavailable comparison rather than treating omission as a match. This change illustrates what the public explanation must teach: derive the joining rule from the receiving condition and preserve partial results. It does not establish causality from one matched pair.

### E.4.CM:5.2 - A larger contribution survives subtraction {#a-larger-contribution-survives-subtraction}

Suppose an author has explanations for probing an unfamiliar device, comparing architecture alternatives and retaining a shared way of working. A practitioner still needs to turn an unexpected response into a repeatable delivery use.

The necessary connection is not “do all three.” A response supports only a bounded claim; the intended use determines whether that claim is sufficient. If it is insufficient, the next probe must distinguish the relevant alternatives. A chosen use then determines which preparation and environmental support to preserve, and a receiving participant's attempt can reopen the arrangement rather than the original causal question.

C.40.CU develops this whole. Its suppliers remain useful, but subtracting their individually supplied operations leaves the selection and return relations above. A normal FPF pattern is appropriate because those relations recur across constructs and uses.

The whole has both dimensions. Horizontally, a supported fixed-task response can permit use while an unfamiliar-task claim remains unknown and calls for another probe; these are conditioned continuations, not a compulsory inquiry sequence. Vertically, guide inspection and loading are constituent actions of delivery, and the delivery deadline constrains their combined performance. Ontologically, the tested configuration's success remains distinct from the controller's independently held capability. Each distinction changes the construction.

A short entry can say “take the response, bound the claim, construct a useful arrangement, and reproduce it under the receiving conditions.” That sentence is a reminder, not the complete explanation.

### E.4.CM:5.3 - Integrate overlapping checks without losing either use {#integrate-overlapping-checks-without-losing-either-use}

An intake Method accepts a reading when its unit is °C and its value lies from 0 through 100. A calibration-use Method repeats that same check and also requires a current calibration. The two Methods consume the same immutable reading version and use the same meanings of unit, endpoints and rejection. Under those conditions the common check can be performed once and its result supplied to both uses.

For the readings R1=(42, °C, current), R2=(42, °F, current), R3=(120, °C, current), R4=(60, °C, expired) and R5=(60, °C, current), the common check accepts R1, R4 and R5. Intake retains all three. Calibration use additionally tests calibration currentness, retaining R1 and R5. Sharing the check does not permit removing that additional condition or imposing it on intake.

Now the calibration use changes its upper limit to 50 °C. Use B.1.5.RS to follow the replacement through both receiving uses. Retain the shared 0–100 check for intake and add the narrower condition on the calibration branch; that branch now retains only R1. Changing the common threshold to 50 would incorrectly remove R4 and R5 from intake. Alternatively, keep separate checks when different observation versions, meanings or required failure responses prevent sharing their result.

The constructive choice is to identify the identical predicate and input, preserve each distinct obligation, and reconnect their results to the two receivers. It integrates the overlap without flattening the Methods into one stronger admission rule. No additional pattern is needed merely to give these checks a second name.

## E.4.CM:6 - Bias-Annotation {#bias-annotation}

An expert author can forget how much synthesis they supplied between references. Compare the actual public inputs with the reasoning used in the worked case. Conversely, enthusiasm for a source can create a named umbrella with no added contribution. The same-situation comparison tests both errors.

## E.4.CM:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| “All parts exist, so nothing remains to publish” | Compare the whole's connections and the reader's required reconstruction. |
| One new pattern for every row or action | Select independently recognizable recurring difficulties; combine inseparable contributions. |
| A mandatory tour through all suppliers | State branch conditions and stop when the useful result is supplied. |
| A card as the only explanation | Develop the reusable Method in a normal public owner, then derive the card. |
| A successful expert trial silently completes the text | Identify the rule the expert added and either supply it or delimit the required preparation. |
| A source summary placed directly in a pattern | Reconstruct practitioner actions, conditions and results; retain provenance and theoretical limits. |

## E.4.CM:10 - Rationale {#rationale}

Pattern authoring and scientific Method development often perform conceptual synthesis. Composition is productive work because successful local contributions do not determine their joint conditions, suitable selection or response to change. These relations can themselves have recurring problems and reusable solutions. A new primitive operation is therefore neither necessary nor sufficient for a useful framework contribution.

Normal patterns can describe these solutions at the scale where practitioners need them. Publication length is a separate choice. Keeping a short first entry and a developed body avoids both a compulsory long first read and an unexplained whole.

## E.4.CM:11 - SoTA-Echoing {#sota-echoing}

| Source and role | Contribution used here | Boundary of adoption |
| --- | --- | --- |
| Ralyté and Rolland, “An Assembly Process Model for Method Engineering” (2001), §§2–4; historical method-engineering basis. [Primary paper](https://cui.unige.ch/~ralyte/publications/CAISE01(Ralyte-Rolland).pdf) | Distinguishes associating complementary chunks from integrating overlapping ones; constructs methods from situational requirements with returns when requirements change. | Its information-systems method models are not a universal FPF ontology or a requirement to store every method as a chunk record. |
| “Towards a process selection method for embedded analytics” (2024), §3.2; a more recent domain application. [Primary study](https://link.springer.com/article/10.1007/s10257-024-00675-1) | Uses requirements, fragment selection and assembly as constructive work, showing continued practical use of assembly-based method engineering. | A domain study does not establish effectiveness for all FPF compositions or validate this pattern. |
| B.1.5, B.1.5.EW/RS, C.39.RO and E.11.PFP | Supply Method composition, vertical enactment, replacement, reusable construction and explanation at selected scales. | Reuse is by the actual supplied action; these foundations do not make every particular whole already explained. |

**When does a composition require developed guidance beyond its constituents?** The selected line constructs the missing relation from the receiving problem and then compares the resulting whole with the available public explanation. A serious alternative is a direct reading route to existing constituent descriptions. In 5.1 that route is sufficient because C.40.CD already explains the join; 4.4 therefore selects reuse. In 5.2 the route leaves application selection and reproduction returns to expert invention, while 5.3 exposes an integration choice that a sequence of both Methods would hide. Sections 4.2–4.3 supply those constructive moves, 4.5 selects their public owner, and 4.6 develops the full knowledge account at that scale. The historical assembly line supports distinguishing association from overlap integration; the 2024 application shows a current domain use of requirements, selection and assembly, not universal effectiveness. The extra cost is developing and maintaining the consequential connections and their cases, with exact suppliers retaining their reusable detail. Reopen this choice when a directly usable public whole is found, a constituent or receiving condition changes the connection, or an actual use exposes missing construction. A demonstrated lower-burden explanation with the same useful reach would replace the current one.


## E.4.CM:End {#end}

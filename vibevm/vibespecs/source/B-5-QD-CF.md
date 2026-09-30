# B.5.QD.CF - Reformulate a Problem by Examining Its Conflicting Assumptions: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## B.5.QD.CF:5 - Archetypal Grounding {#archetypal-grounding}

The following constructed cases supply the conditions needed for their reasoning. They demonstrate different reformulations and a case in which the original demand remains impossible.

### B.5.QD.CF:5.1 - Distinguish operating conditions without inventing a machine {#distinguish-operating-conditions-without-inventing-a-machine}

A proposed device has one fixed setting p. The task requires p to be at least 6 during work and at most 2 during quiet operation. In the proposed design, both requirements constrain the same fixed value; no such value exists.

Recover the extra premise: the setting is fixed across those operating conditions. Let p_work and p_quiet describe the two values. The account is:

- p_work ≥ 6;
- p_quiet ≤ 2;
- p_work = p_quiet.

Keeping the two requirements and reconsidering the equality produces a construction question: **Can the device select different settings in the two distinguishable conditions?** The values (6,2) satisfy the revised inequalities. They identify what a switching construction would have to supply.

That answer is conditional. The device must be able to recognize the condition and reach the required setting in time, using the resources permitted by the task. If a transition takes three seconds while the retained requirement allows one second, this proposed transition fails. A faster operation, another construction or an authorized requirement change is still needed.

If instead both inequalities concern the same operation at the same time, separating their names would misrepresent the task. The inequality 6 ≤ p ≤ 2 remains impossible. The useful result then identifies the requirements that cannot both be retained.

### B.5.QD.CF:5.2 - Replace an assumed means while retaining two outcomes {#replace-an-assumed-means-while-retaining-two-outcomes}

A team must reproduce an earlier calculation and use new prices for new calculations. A current file stores the quantity 3 and the price 10, so the earlier result is 30. Tomorrow the price becomes 12 and the new result must be 36.

The proposed practice keeps only one mutable price value. Reproducing the earlier result is taken to require keeping that value at 10; obtaining the new result requires changing it to 12. The conflict depends on that proposed means of recovering the earlier input.

Ask instead: **What information and operation reproduce the earlier calculation without freezing the current price?** For this case, the calculation is quantity times price. Retaining the input pair (3,10), the multiplication rule and the identity of the earlier calculation supplies its result 30. The current pair (3,12) supplies 36. A versioned input or a retained calculation record can therefore replace the supposed need for one unchanged current value.

The scope matters. This construction suffices for the supplied arithmetic question. If the earlier result used a rounding rule, exchange rate or other input, that contribution must also remain recoverable. A claim about who approved the transaction asks another question and is not established by recomputing 30.

Now change the retained requirements: every copy of the earlier price must be destroyed, and no equivalent information may remain, but the system must later recover that price uniquely. The retained-input proposal violates the deletion requirement. The conflict has not been repaired under these new conditions. The next case isolates why this stronger combination can be impossible.

### B.5.QD.CF:5.3 - Return an impossibility instead of hiding retained information {#return-an-impossibility-instead-of-hiding-retained-information}

A device receives one bit x, either 0 or 1. Complete erasure in this formal task means that, afterward, its entire accessible state is the same s for both inputs; there is no external record or later input revealing x. A deterministic operation g must then recover the original bit for either input.

For the input 0, recovery requires g(s)=0. For the input 1, it requires g(s)=1. The same operation on the same state cannot satisfy both. The required erasure and universal recovery are incompatible under the supplied model.

An external copy or a different final state would allow other constructions, but each changes the complete-erasure condition. Renaming an external copy as a pointer preserves information rather than meeting that condition. Returning a default value changes the recovery requirement. Neither is a solution to the original task.

The result can already end the construction search under these premises. If the work instead permits a retained distinction, develop that changed question explicitly. A later physical implementation also has a physical model and its own scope; the argument here establishes the finite information constraint stated above.

## B.5.QD.CF:6 - Bias-Annotation {#bias-annotation}

The familiar means can dominate the description of a need. Recovering the result it supplies helps make a replacement thinkable. Conversely, a wish for a harmonious answer can lead the practitioner to relax the very condition that mattered. Returning to all retained requirements exposes that loss.

The easiest premise to remove may be the one with the strongest physical or practical basis. Diagnose its role without treating mathematical removability as permission to discard it. People and AI agents can both produce a coherent reformulation that solves a different problem.

## B.5.QD.CF:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure invited by conflict repair | Better move |
| --- | --- |
| “This way has always worked, so the result requires it.” | Recover what the way supplies and ask whether another operation supplies that contribution. |
| A solver returns a solution after a hard requirement is removed. | State the changed requirement and return to the original need; the witness answers the relaxed problem. |
| Two names are introduced for one quantity in one condition. | Establish the actual distinction or retain the incompatibility, as in :5.1. |
| The small conflicting set is repaired while another affected requirement is ignored. | Reapply the retained requirements; inspect the transition time or lost information that the change can affect. |
| A consistent description is presented as an implemented repair. | State the operation and support still needed to obtain the result. |
| Every conflict is promised a solution that preserves every demand. | Return the supported limit or requirement-change question when no warranted repair exists. |

## B.5.QD.CF:10 - Architectural Rationale {#architectural-rationale}

An incompatibility is relational: it depends on statements used together. That is why inspecting one requirement in isolation often misses the constructive opening. Separating a needed outcome from an assumed necessary means exposes a question about how else the outcome could be obtained.

The return to the original need prevents successful reformulation from becoming accidental goal substitution. A conditional construction, an achieved result and an impossibility make different contributions to the encompassing work. Keeping those contributions distinct allows division of work between people and AI without requiring each contributor to solve the whole problem.

Conflict-driven reformulation is a constituent of question development with its own recurring difficulty and operation. B.5.QD supplies the broader development of a question from either failure or success. This pattern unfolds the move from conflicting premises to an alternative construction or a useful limit, leaving subject construction and validation with their own methods.

## B.5.QD.CF:11 - SoTA-Echoing {#sota-echoing}

For the question **“How can incompatible demands reveal an alternative means?”**, **adapt** the Theory of Constraints move from a required outcome to its assumed necessary means. Against choosing a side before examining that necessity, the selected method asks for a replacement that supplies the retained outcome. Sections :4.2–:4.4 and :5.2 carry this difference. Goldratt's [Letter #5](https://www.toc-goldratt.com/index.php?cont=787) gives the original method argument; the current [ProConCloud account](https://www.goldrattresearchlabs.com/proconcloud-method) includes conditional and alternative changes. They are method proposals, not independent evidence of this pattern's effectiveness. **Reject** a guarantee of preserving every demand and a mandatory experiment for every case. The selected return to retained requirements can cost more than simply choosing a side, but is warranted when another construction could change that choice. Reopen this comparison if a stronger method finds such constructions with less burden or reveals a missing class of consequential assumptions.

For **“What does a diagnosed formal conflict establish?”**, **adopt** the distinction between an inconsistent subset and a correction subset from Gamba, Bogaerts and Guns, [*Efficiently Explaining CSPs with Unsatisfiable Subset Optimization*](https://arxiv.org/html/2303.11712v2), Definitions 1–3. Against treating a returned correction as the practical repair, :4.2 and :4.4 preserve its narrower meaning: removing those constraints permits consistency in that formal problem. **Adapt** the distinction to optional diagnosis here; subset minimality and optimization are required only when their extra result matters. The source's algorithms concern constraint problems, and their performance does not transfer to arbitrary disagreements. Reopen when a different constraint semantics changes what the diagnostic result means or a cheaper explanation suffices.

For **“How should attempted construction change the problem?”**, **adapt** the problem–solution co-evolution account in Parsons and Shukla, [*Beyond Problem Solving: Framing and Problem–Solution Co-Evolution in Data Visualization Design*](https://arxiv.org/html/2508.07058v1), §§4–5 and 6.4. Against fixing the problem once and testing only proposed solutions, :4.3–:4.5 return a failed construction to the consequential premise and then to the original need. Their study of eleven selected experts supplies practice-specific observations, not a universal creative mechanism or a test of this method. The extra return is useful when the attempted construction changes the question; an adequate existing formulation needs no such work. Reopen when evidence or another practice reveals that the return loses a needed distinction or obstructs a better continuation.


## B.5.QD.CF:End {#end}

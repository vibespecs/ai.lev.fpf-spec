# A.6.P.RI - Recover Agent-Relative References for Action: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.6.P.RI:5 - Archetypal Grounding {#archetypal-grounding}

The following constructed cases show different things a transfer can preserve.

### A.6.P.RI:5.1 - Preserve a displacement across orientations {#preserve-a-displacement-across-orientations}

A faces north and asks B to displace a crate one metre in the direction A calls left. B faces south. The assignment is to preserve the external displacement, and both headings are known.

The source direction is west. For B, facing south, west is right. The receiving instruction is therefore to move the crate one metre to B's right. If B turns east before acting, west becomes backward. Copying “left” would now send the crate north.

Change the assignment to “move the crate one metre toward your own left”. With B facing east, the correct displacement is now north. The known headings did not settle the instruction; the preservation condition did.

If B's heading is unavailable, “one metre west” can still be a complete instruction for a performer who can act in that frame. Otherwise the body-relative instruction remains unresolved. The method asks for the information needed by the chosen means, not for every possible position description.

A mobile robot receiving the same external displacement needs a usable relation between the shared frame and its action representation. Obtaining that relation and the capability to perform the movement is a separate technical task. The example does not prescribe its learning or control architecture.

### A.6.P.RI:5.2 - Preserve the speaker when relaying a request {#preserve-the-speaker-when-relaying-a-request}

Dana writes to an assistant: “Put the comparison in my project folder.” The assistant sends the request to another worker. Replacing “my” with the new worker's own project folder would change the destination.

The receiving purpose preserves Dana's destination. The assistant identifies Dana's project folder through the available project information and relays: “Put the comparison in Dana's project folder,” with a usable reference to it. The worker uses its own authorized means of access; Dana's request does not grant access that the worker lacks.

If the next assignment is instead “each worker puts a copy in its own project folder”, the rule is applied relative to each worker. That is a changed distribution task, not another wording of the original destination.

Where the workspace contains several Dana projects and the intended one cannot be recovered, the useful result is a question selecting the project. Producing another fluent paraphrase leaves the same action unresolved.

### A.6.P.RI:5.3 - Relate a dancer's report to an observer's account {#relate-a-dancer-s-report-to-an-observer-s-account}

A dancer facing the teacher says, “I feel a pull along my left side when I turn in this figure.” The teacher sees movement on the teacher's right. Both accounts can concern the dancer's left side even though the spatial words differ.

The first receiving task is to understand the report. Recover the dancer as the experiencing participant, the dancer's orientation and the turn being described. The teacher can say, “You report a pull along your left side during that turn,” and ask the dancer to correct the expression if needed.

A second task is to decide how to change the movement. The report and external observation can inform that inquiry, but do not themselves identify the tissue, force, cause or suitable exercise. The relevant bodily practice must supply the further operation.

In this figure, maintaining balance during the turn contributes to performing the figure; regulating bodily effort helps enact that balance, while the steps keep their required rhythm. Changing whose account is used can make another question accessible; it does not by itself identify which constituent needs development. B.1.5.EW supplies that vertical inquiry, and B.5.EA helps articulate a distinction the dancer cannot yet express.

## A.6.P.RI:6 - Bias-Annotation {#bias-annotation}

A translator can assume that the recipient occupies the same position as the source. A shared diagram or vocabulary makes this especially easy. Test the particular changed condition on which the action depends.

An observer can also replace the performer's report with an interpretation that is easier to describe externally. Keep the report open to correction by its source and give the additional interpretation its own basis.

## A.6.P.RI:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

**Copying a relative direction.** The source and recipient face different ways, but both act on the same word. Recover the source direction and the intended receiving result before deriving the recipient's instruction.

**Replacing every “I” with the recipient.** A quotation or relayed instruction loses its original speaker. Preserve the source attribution unless the new task deliberately applies a rule to another participant.

**Treating shared facts as self-identification.** Several systems receive the same participant description, but none has been linked to its own entry. Obtain that link from the actual working configuration.

**Turning a felt report into a bodily cause.** “The dancer reports tension here” becomes “this tissue causes the failure”. Preserve the report and use the appropriate subject method to examine the causal claim.

## A.6.P.RI:10 - Architectural Rationale {#architectural-rationale}

Relational precision restoration recovers missing participants. Agent-relative use additionally requires a link between the receiving agent and the described participants, together with a decision about what the transfer preserves. Neither a complete participant list nor a change of notation supplies these by itself.

The construction therefore combines the source interpretation, receiving purpose and recipient's position. Representation change and EntityOfConcern retargeting retain their existing conditions. Domain operations compute the actual conversion or classification; this method exposes the premises they need and returns their result to the receiving action.

The method applies when the receiving performer can be identified in the account and the relevant reference conditions can be recovered. Human first-person experience remains available through the experiencing person's account and correction. An artificial agent uses the identification, representations and signals its configuration supplies.

## A.6.P.RI:11 - SoTA-Echoing {#sota-echoing}

The practice question is how an explicit shared account becomes usable by an agent whose position differs from its source. The method recovers the source reference, chooses what the receiving use preserves and connects the recipient to the account. Its serious alternative is to make all participants explicit and assume that this alone determines the receiving instruction.

**Adapt the distinction between common descriptions and agent-relative use.** [Partridge and colleagues, Ontology then Agentology (2018)](https://biblio.ugent.be/publication/8547739), §§2–4 and Figure 2, distinguish the reusable form of an account from its agent-dependent content and add a link identifying the system itself. This supports the self-identification required in §§4.2 and 4.5. It is a conceptual source, not evidence about human learning or current robot performance.

The crate case shows why this pattern also states the preservation condition in §4.3. Even correct source interpretation and self-identification leave two different possible tasks: preserve the displacement or repeat the relative movement. This is the pattern's methodological synthesis, rather than a result attributed to that paper.

**Reuse representation and retargeting methods under their own conditions.** A.6.3.RT is sufficient when the receiving use needs only a representation change under already available bindings. A.6.4 is needed when the independently identified EntitiesOfConcern differ.

Use the simpler direct clarification when it already settles the action. Reopen the construction when it cannot determine which reference changed, when the recipient cannot bind itself to the supplied account, or when the intended preservation condition fails under changed use. Technical conversion and learning methods require their own current subject evidence.


## A.6.P.RI:End {#end}

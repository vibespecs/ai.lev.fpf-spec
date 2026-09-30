# B.5.RC - Recover a Construction from Its Description: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## B.5.RC:5 - Archetypal Grounding {#archetypal-grounding}

### B.5.RC:5.1 - Recovering an equilateral-triangle construction {#recovering-an-equilateral-triangle-construction}

A reader has two distinct points A and B in the Euclidean plane and needs an equilateral triangle on side AB. The description says to draw two circles, each centred at an endpoint and passing through the other endpoint, and use an intersection as the third vertex.

The reader recovers three operations: draw a circle with the given centre and radius; select a common point of the two circles; join two given points by a segment. The third vertex requires both circles. The final triangle requires that vertex together with A and B. The two circles share the segment length AB as radius.

For a small case, place A at (0,0) and B at (2,0). The circles have equations x²+y²=4 and (x−2)²+y²=4. Subtracting gives x=1, and substitution gives y²=3. Thus the two common points are (1,√3) and (1,−√3). Selecting C=(1,√3) supplies the vertex above AB. Joining A to C and B to C completes the construction.

The property follows from how C was obtained: AC and BC are radii of circles of radius AB, so AC=BC=AB. The coordinate calculation also supplies the intersection in the Euclidean-plane account used for this case. A description formulated under a different set of construction rules must obtain that intersection under those rules.

The recovered dependency is reusable for another positive side length. The value of the coordinates changes, while the two equal-radius circles and the common-point construction retain their roles. If A and B coincide, the initial requirement of a nondegenerate triangle fails; that case needs distinct endpoints before this construction can begin.

The Euclidean account supplies the circle and segment operations and their justification.

### B.5.RC:5.2 - Recovering a display-stand assembly design {#recovering-a-display-stand-assembly-design}

A specification asks for a portable display. It supplies a base, an upright and a panel, together with these rules: the upright can be joined to the base when their fittings match; the panel can be attached to the mounted upright when their fittings match.

Working backward from an assembled display yields a mounted upright and a compatible panel. Recovering the mounted upright yields the base, upright and their fitting condition. Working forward gives the assembly order: join base and upright, then attach the panel.

Inspection of the supplied parts reveals that the panel fitting differs from the upright fitting. The method has localized the obstruction. Available continuations include obtaining a compatible panel, developing an adapter with usable connection rules, or choosing another assembly design. “Assemble the display” alone does not select among them.

Suppose a compatible panel is supplied. The recovered design now connects the three components in the required order. Portability is still assessed against the actual carrying requirement, and stability against the loading and support conditions. Those engineering questions can change the design, but they are distinct from the recovered answer about how its parts connect.

The first useful result is the assembly design or the fitting mismatch that prevents it. Physically assembling and testing the stand are subsequent work selected by the intended use.

## B.5.RC:6 - Bias-Annotation {#bias-annotation}

A fluent description can hide an unfamiliar operation behind a familiar verb. Keep attention on what the operation takes, permits and produces. Conversely, a highly formal description can make an existence claim look like an executable recipe; use the next task to decide whether a witness or construction procedure is needed.

Examples can also narrow the apparent method. The circles in :5.1 and fittings in :5.2 supply different subject operations. The common move is recovering and using their prerequisites, including the property needed for continuation.

## B.5.RC:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure in the working situation | Repair |
| --- | --- |
| Repeating “construct an object with property P” when the obtaining operation is missing | Recover the last producing operation and trace its prerequisites to available inputs. |
| Flattening a construction into a list that loses a shared object or a joint condition | Preserve those dependencies and perform each operation only when its inputs are available together. |
| Filling an omitted operation with a plausible guess and attributing it to the source | Name the addition and establish how it works, or return to the source for the missing operation. |
| Treating a successful small case as a result for all inputs | Recover which conditions carry the general argument and which belong only to the trial. |
| Continuing source reconstruction after the intended use is already possible | Use the recovered construction; reopen only for a further question that requires more. |

## B.5.RC:10 - Architectural Rationale {#architectural-rationale}

Backward recovery and forward construction answer complementary questions. The backward direction reveals what the desired result requires. The forward direction tests whether the available inputs and operations can supply it. Either direction alone can leave a gap: a plausible plan may lack an executable step, while available operations may produce objects irrelevant to the question.

The method follows the construction's dependency structure. One intermediate object can support several later steps, and several objects can be required jointly. Preserving these relations makes the construction intelligible and helps divide its execution among people and AI agents. The receiving operation determines what a collaborator needs to supply.

Construction and reasoning about properties remain connected. In the triangle case, the construction creates a common point and the circle properties establish equal sides. In the stand case, fitting conditions permit assembly, while load and carrying requirements can lead to design revision. This relation warrants cooperating methods for construction recovery and argument recovery.

B.5 coordinates these contributions within inquiry. C.39 develops a missing method, C.29.2 develops a computational formulation, and A.6.3.RT prepares an operative expression. Their results can supply a missing step here; the source-recovery question does not by itself select every neighbouring method.

## B.5.RC:11 - SoTA-Echoing {#sota-echoing}

**Constructive and propositional accounts.** Rodin's [One Mathematic(s) or Many? Foundations of Mathematics in Today's Mathematical Practice](https://arxiv.org/html/2301.08131v1), especially its discussion of Euclid's operations and problems, treats object-forming procedures and reasoning about their properties as connected contributions to mathematical practice. This pattern adopts that connection in :4.2–:4.5. It leaves the choice of mathematical foundations to the account being used. A propositional existence result remains sufficient when that is the required result; obtaining a particular instance calls for the corresponding construction.

**Problem reduction.** Rodin's [Kolmogorov's Calculus of Problems and Its Legacy](https://philomatica.org/wp-content/uploads/2023/07/kolmoeng.pdf), in the 2023 author manuscript's discussion of reductions among problems, supplies an earlier account of solving one problem through solutions to others. The present method uses that idea for prerequisite recovery, including joint and alternative contributions. It does not require the reader to adopt intuitionistic logic for every subject.

**Bounded method choice.** For a compressed construction whose result is needed now, compare a linear paraphrase of the source with backward prerequisite recovery followed by a small forward construction. The triangle case requires two circles together; the stand case exposes the unmatched fitting before a complete display exists. The second method is selected because it makes those dependencies actionable. If the source already provides an executable construction understood by the reader, direct use is cheaper. The recovered procedure and the stand example are the present synthesis; the source accounts do not establish an empirical learning gain for this generic method. Reconsider the backward-then-forward approach when, for the same unfamiliar construction and reader preparation, another recovery method supplies the missing operation more reliably at comparable effort.


## B.5.RC:End {#end}

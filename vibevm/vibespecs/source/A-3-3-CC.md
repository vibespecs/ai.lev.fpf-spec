# A.3.3.CC - Construct a Configuration Description under Constraints: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.3.3.CC:5 - Archetypal Grounding {#archetypal-grounding}

### A.3.3.CC:5.1 - A rigid link, then a variable length {#a-rigid-link-then-a-variable-length}

Consider a freely placed link in a plane, with distinguishable endpoints A and B and fixed length 2 metres. Use one Cartesian reference frame. The implicit description is

`q = (xA, yA, xB, yB)`, with `(xB - xA)^2 + (yB - yA)^2 = 4`.

The tuple (0, 0, 2, 0), in metres, satisfies the relation. The tuple (0, 0, 1, 0) fails it. Each endpoint separately has a valid position in the plane, but the second pair violates the modeled link.

For locating the endpoints, use parameters X, Y and orientation phi:

`A = (X, Y)`; `B = (X + 2 cos(phi), Y + 2 sin(phi))`.

Every pair of endpoints at distance 2 has such a representation. Orientations differing by a full turn describe the same configuration. Reversing the direction while keeping A fixed changes B, so identifying opposite orientations would lose a distinction of this labeled-endpoint model.

Now allow the link to extend or contract with length `0 < r <= 3`. Replace 2 by the variable r. The formerly rejected pair (0, 0, 1, 0) is admitted at r = 1. A later motion calculation needs a law for the changing length and whatever initial data that law requires. If the question concerns force carried by a rigid constraint, retaining its equation can help express the force calculation through a multiplier; eliminating the constraint from position coordinates has not answered that force question.

### A.3.3.CC:5.2 - Buffer counts, external arrivals and job order {#buffer-counts-external-arrivals-and-job-order}

Two buffers each hold at most two jobs. Exactly three jobs are distributed between them. The product of count ranges is `{0,1,2} x {0,1,2}`; the stock condition is `q1 + q2 = 3`.

Testing the nine pairs leaves `Q = {(1,2), (2,1)}`. Equivalently, choose q1 from {1,2} and reconstruct `q2 = 3 - q1`. The description now supplies both possible occupancy arrangements.

An external arrival can raise the total to four. Keeping `q2 = 3 - q1` would omit the possible arrangement (2,2). Retain both counts and use the total applicable to the new question, or include total N as a variable with `q1 + q2 = N`. Which arrival can occur, and when, comes from an arrival and transition account.

Suppose the next question asks which job a first-in-first-out buffer serves. The sequences [A,B] and [B,A] have the same count, yet they give different next jobs under that rule. Represent the ordered job identities in the relevant buffer. Counts remain recoverable as sequence lengths; the receiving operation gains the distinction it lacked.

### A.3.3.CC:5.3 - A body must fit, not just its reference point {#a-body-must-fit-not-just-its-reference-point}

A rigid body occupies the one-dimensional interval `[x-r, x+r]`; x is its centre and r its half-length. It must lie wholly inside `[0,L]`. Contact with the endpoints is permitted in this model.

Containment gives `x-r >= 0` and `x+r <= L`, hence `r <= x <= L-r`. For L = 3 and r = 1, the admissible centres are [1,2]. Centre x = 0.5 lies inside the container but places part of the body outside it, so a point-only test gives the wrong fitting answer.

If clearance is required, include the clearance in the inequalities. If L = 1.5 while r remains 1, the interval for x is empty. That conditional impossibility directs the next decision to the body size, container size or permitted deformation. It was obtained by connecting a physical extent, a mathematical inequality and a calculation; no motion simulation was needed.

### A.3.3.CC:5.4 - A velocity restriction leaves a configuration question open {#a-velocity-restriction-leaves-a-configuration-question-open}

For an ideal car rolling in a plane without lateral wheel slip, let (x,y) be the point halfway between the rear wheels and theta the chassis orientation. Let v be this point's velocity component along the chassis's forward direction. Then

`xdot = v cos(theta)`, `ydot = v sin(theta)`,

so `sin(theta) xdot - cos(theta) ydot = 0`. At theta = 0 the rear reference point has ydot = 0.

This equation constrains a velocity at a configuration. It does not impose a fixed y coordinate: a stationary car at another y satisfies the same velocity condition with v = 0. Whether a car can reach a selected parking position from its current one also depends on steering, obstacles and an allowed sequence of motions. Preserve those as a planning question instead of deleting the position from the configuration description.

## A.3.3.CC:6 - Bias-Annotation {#bias-annotation}

A familiar coordinate system can make its convenient operations look like properties of the subject. The centre-only containment test in :5.3 demonstrates the loss: the representation retained a point while the fitting question concerned an extended body. Recover the modeled participants and required distinctions before transferring the result.

Minimal-coordinate preference can also hide a useful relation. In the linkage, fewer coordinates simplify position reconstruction, while the retained constraint equation is useful for a constraint-force question. Choose with that operation in view.

Both biases can occur in a person's reasoning, an AI-generated model or a shared engineering calculation. Make the interpretation recoverable to the next participant, including when a computation is delegated.

## A.3.3.CC:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Observed or example-demonstrated failure | Repair |
| --- | --- |
| Choosing valid values for each endpoint but violating the link between them | Test the joint tuple against the distance constraint, or reconstruct both endpoints from parameters satisfying it. |
| Carrying a fixed-total reduction into a model with arrivals | Make the changed total explicit or retain the counts needed to express it. |
| Answering a job-order question from queue lengths alone | Retain the ordered identities used by the service rule. |
| Treating a small coordinate count as a global representation | Supply coverage and equivalence information; use multiple charts or implicit constraints where needed. |
| Rejecting a parking position because immediate sideways motion is forbidden | Keep the position and test a sequence of allowed motions under the relevant steering and obstacle conditions. |
| Treating a failed search as impossibility | Return the search limit, or obtain a complete argument or computation for the impossibility claim. |

## A.3.3.CC:10 - Architectural Rationale {#architectural-rationale}

Constraint-based construction connects the subject's arrangement to the mathematical and computational operations used on it. Separating value ranges from compatibility explains why independently valid coordinates can form an inadmissible combination. It also lets the same construction work with continuous positions, finite stocks and ordered data.

The result can be useful before a transition law exists. Keeping that stopping point allows division of work: one participant constructs the configuration description, another supplies interaction or operation rules, and another computes a receiving result. Their contributions remain connected through interpretable participant values and conditions.

Implicit descriptions, parametrizations and finite enumeration expose different operations. Treating one as universally preferable would make the Method fail on either constrained geometry or a small discrete problem. The representation can be refined at the scale its use needs. C.29.1 handles the more general transfer between accounts; here the construction specifically obtains compatible arrangements.

## A.3.3.CC:11 - SoTA-Echoing {#sota-echoing}

**How should constraints determine the representation?** Tong's [Classical Dynamics, section 2.3](https://www.damtp.cam.ac.uk/user/tong/dynamics/dynhtml/S2.html) develops generalized coordinates and the alternative of retaining constraints through multipliers. At comparable effort for the linkage, reduced coordinates make positions easy to reconstruct; the implicit relation keeps the connection available for a force calculation. Sections :4.2-:4.3 adopt this choice by the receiving question. Its mechanics supplies the physical interpretation of those constraints, not a law for every modeled subject.

Lynch and Park's [Modern Robotics, section 2.3.2](https://modernrobotics.northwestern.edu/nu-gm-book-resource/2-3-2-configuration-space-representation/) compares explicit and implicit configuration representations, including singular coordinate descriptions of a sphere. Section :4.3 adopts the coverage and representation question instead of equating fewer coordinates with a better account. Their [section 2.4](https://modernrobotics.northwestern.edu/nu-gm-book-resource/2-4-configuration-and-velocity-constraints/) distinguishes holonomic configuration constraints from nonholonomic velocity restrictions. Section :5.4 carries that distinction into a small motion question. These are durable construction Methods; the particular robot geometry and kinematic assumptions must still be supplied for a new robot.

**How does physical extent enter a computational configuration?** LaValle's [Planning Algorithms, chapter 4, introduction and sections 4.2-4.3](https://lavalle.pl/planning/ch4.pdf), constructs robot configurations, transformations and collision sets. Compared with checking a reference point alone, testing the transformed body's intersection with obstacles preserves the extent that the fitting question needs. Sections :4.1-:4.2 and :5.3 adopt that connection and the need to state contact conditions. The one-dimensional containment calculation is an authored reduced case. Path planning and collision algorithms retain their own assumptions and costs.

**When should a finite constraint set be solved by enumeration?** Poole and Mackworth's [Artificial Intelligence: Foundations of Computational Agents, third edition, section 4.1](https://artint.info/3e/html/ArtInt3e.Ch4.S1.html) makes variables, value domains, assignments and constraints explicit. Their [section 4.2](https://artint.info/3e/html/ArtInt3e.Ch4.S2.html) compares complete-assignment testing with search that rejects a partial assignment once a relevant constraint fails. Sections :4.2-:4.4 adopt those operational forms. For the two-buffer case, nine combinations make full enumeration inexpensive; a large product calls for a solving Method that exploits its constraints. Early rejection saves search without changing the satisfying set; it does not make arbitrary constraint problems cheap.

Together these sources supply complementary current answers to the construction question, with older sources serving as substantive methods rather than as claims of novelty. Reconsider the representation when the needed operation, configuration coverage, contact condition, participant distinctions or computational budget changes. A faster solver cannot recover a physical distinction omitted from its input.


## A.3.3.CC:End {#end}

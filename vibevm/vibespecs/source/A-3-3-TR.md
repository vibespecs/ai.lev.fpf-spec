# A.3.3.TR - Construct a Rule for State Change: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.3.3.TR:5 - Archetypal Grounding {#archetypal-grounding}

### A.3.3.TR:5.1 - Two correct local increments can lose a global increment {#two-correct-local-increments-can-lose-a-global-increment}

Participants A and B each read an integer counter and later write the saved value plus one. Individual reads and writes are atomic. Each participant reads before it writes. Initially x = 0.

Use the state x, positions pA and pB in the two local procedures, and saved values rA and rB after their reads. Positions 0, 1 and 2 mean before read, after read and finished. Initially pA = pB = 0 and rA = rB = 0; each participant overwrites its saved value before using it.

The four action rules are:

| Action | Enabled when | Changed values | Other values |
| --- | --- | --- | --- |
| ReadA | pA = 0 | rA' = x; pA' = 1 | x, pB and rB retain their values |
| WriteA | pA = 1 | x' = rA + 1; pA' = 2 | rA, pB and rB retain their values |
| ReadB | pB = 0 | rB' = x; pB' = 1 | x, pA and rA retain their values |
| WriteB | pB = 1 | x' = rB + 1; pB' = 2 | rB, pA and rA retain their values |

The next step is any one enabled action. From pA = pB = 0, six complete histories respect the local orders. ReadA, WriteA, ReadB, WriteB and its A/B reversal finish at x = 2. In the other four, both reads precede either write; both saved values are zero, so the final value is one.

The result identifies how interference defeats the intended total. Serializing the two read-and-write pairs or supplying an indivisible increment changes the transition rule and removes these lost-increment histories. If serialization introduces waiting, a claim of eventual completion still needs its scheduling conditions.

The ordering rules already suffice to exhibit failure. If a scheduler chooses uniformly among enabled actions at each step, the two serialized histories each have probability 1/4 and the other four each have probability 1/8; the lost-increment probability is 1/2. Uniform choice among the six complete histories instead gives 2/3. Choose and justify a scheduler model when a likelihood estimate is needed.

### A.3.3.TR:5.2 - A fixed connection and two force equations determine acceleration {#a-fixed-connection-and-two-force-equations-determine}

Two carts move on an ideal frictionless straight track. A massless rigid connector keeps their positions q1 and q2 at q2 - q1 = L. Their positive masses are m1 and m2. Signed external forces along the track are F1 and F2. The connector exerts equal and opposite signed forces, written -lambda on cart 1 and +lambda on cart 2.

The positional constraint alone permits many common motions. Differentiating the constant-separation condition gives v2 = v1 and a2 = a1 = a for compatible motion. Newton's equations for this ideal model give

    m1*a = F1 - lambda
    m2*a = F2 + lambda

Adding them obtains `a = (F1 + F2)/(m1 + m2)`. Substituting back gives `lambda = (m2*F1 - m1*F2)/(m1 + m2)`. The connection constraint and both interaction equations were needed to determine the common acceleration and exchanged force.

For m1 = 1 kg, m2 = 3 kg, F1 = 4 N and F2 = 0, the result is a = 1 m/s² and lambda = 3 N. Start with q1 = 0, q2 = L and both velocities zero. While the forces remain constant, q1(t) = t²/2 and q2(t) = L + t²/2 in metres when t is in seconds; both velocities are t metres/second.

These formulas provide a state-transition calculation for any chosen interval within those assumptions. If the forces vary, supply their time or state dependence before computing the motion. If the connector is elastic or has consequential mass, its constitutive and interaction account changes the rule. Choosing smaller numerical time steps cannot supply that missing physical relation.

The calculation combines the physical interaction account, mathematical constraints and an executable rule. It also shows why reducing to one position can simplify motion prediction while retaining the connector force lets a designer determine the load on the connection.

### A.3.3.TR:5.3 - Preserving a value and making progress require different arguments {#preserving-a-value-and-making-progress-require-different}

For nonnegative integers a and b with `a >= b > 0`, use integer division `a = k*b + r`, where k and r are integers and `0 <= r < b`. Take the transition `(a,b) -> (b,r)`. Every common divisor of a and b divides `r = a - k*b`; every common divisor of b and r divides `a = k*b + r`. The integer quotient makes both implications valid. The transition therefore preserves the common divisors and hence the greatest common divisor. At `b = 0`, stop and return a.

From (30,18), the successive states are (18,12), (12,6), (6,0). The terminal result is 6. The second component is a nonnegative integer and decreases at every nonterminal step, establishing termination.

By comparison, repeatedly swapping the two arguments also preserves their greatest common divisor but can alternate forever. Preservation alone did not establish progress. The Euclidean rule adds the remainder operation and a decreasing quantity.

This is a transition account for a mathematical construction. An implementation must supply integer operations with the assumed meanings; using a bounded machine representation introduces its own arithmetic conditions.

### A.3.3.TR:5.4 - A switch changes the law within the prediction interval {#a-switch-changes-the-law-within-the-prediction-interval}

Consider a stated temperature model with T in degrees Celsius and heater mode OFF or ON. While OFF, temperature falls at 1 degree/minute; while ON, it rises at 2 degrees/minute. OFF at T<=18 switches immediately to ON. ON at T>=20 switches immediately to OFF. A switch changes the mode and preserves T.

Start at T=19, OFF. The requested result is temperature and mode at 1.5 minutes. In OFF mode, flow is permitted while T>18. The trajectory T(t)=19-t reaches 18 at minute 1; the event then switches the mode to ON. The new law gives T(t)=18+2*(t-1) until T reaches 20. At 1.5 minutes the result is **19 degrees, ON**.

At minute 2, the upper-threshold event switches to OFF; the next segment uses T(t)=20-(t-2). This continuation follows from retaining the mode and restarting the evolution after each event.

Keeping the initial OFF law through the whole first interval would give 17.5 degrees. Checking the switch only at the interval's end describes a controller that samples at those times, with different behavior from the supplied immediate-event model. A real controller's sampling or delay therefore belongs in its modeled timing.

## A.3.3.TR:6 - Bias-Annotation {#bias-annotation}

The continuous example uses an ideal Newtonian model with supplied masses, forces and constraints. Its simplicity makes the common construction visible; another phenomenon needs its own interaction account. The concurrent example assumes atomic reads and writes and makes interleaving observable at that scale. Choose the granularity from the interactions and intermediate effects that can change the answer.

Finite examples can make complete exploration look inexpensive. Large state sets and continuous systems may require abstraction, symbolic reasoning, approximation or a less detailed conclusion. The Method permits a useful conditional result before that larger work.

## A.3.3.TR:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Why it changes the result | Repair |
| --- | --- | --- |
| Replace saved-value updates with updates of the current value | Interference between read and write disappears from the model. | Retain the saved value and instruction position, or justify an atomic operation. |
| Conjoin alternative actions | The model demands incompatible changes at once and can lose legitimate executions. | State the alternatives and the condition enabling each one. |
| Leave a local action's other state values free | A model can introduce changes no participant performs. | State the unchanged values or the joint action that changes them. |
| Filter away violations of the property being investigated | The model excludes the failure instead of explaining whether the implementation prevents it. | Model the behavior or derive the prevention rule, then test the property. |
| Infer progress from preservation | An invariant can hold in a cycle with no useful completion. | Supply a decreasing measure, scheduling condition or other relevant progress argument. |
| Repair a missing interaction law by changing a numerical setting | The computation still lacks the relation needed to determine the modeled change. | Repair the subject account and then select a computation for it. |

## A.3.3.TR:10 - Architectural Rationale {#architectural-rationale}

The independently useful result is a rule for modeled change. Configuration construction establishes compatible arrangements; prediction sufficiency asks whether retained information supports the needed future distinction. Neither contribution by itself connects the interactions and operations that produce allowed continuations.

A relational description keeps joint constraints and unresolved alternatives available before a computation chooses how to solve or explore them. This supports physical, mathematical and computational reasoning together. It also lets a reader alter the inputs or seek a different unknown without discarding the already useful relations.

Atomic actions, continuous equations, event resets and stochastic transitions have different semantics and can use different temporal scales. Their shared construction requires explicit participating quantities and effects; their specialized solution and validation Methods retain the substantive differences.

## A.3.3.TR:11 - SoTA-Echoing {#sota-echoing}

**Working question and selected answer.** How can a reader construct a rule when several local operations or physical interactions jointly determine the change? The selected best-known line keeps their state relations available, combines jointly applicable relations, and retains alternative actions until the question or model selects among them. A serious alternative is a directly executable update procedure with a fixed order. That procedure is cheaper to apply when its order and effects already describe the required behavior; :1 therefore permits direct use of a suitable existing rule.

For the interference question in :5.1, choosing one execution order loses the alternative histories that can defeat the total. Retaining saved values and local instruction positions costs additional description and exploration, but a single lost-increment history already answers whether failure is possible. For the load question in :5.2, retaining the connection force makes that result calculable; eliminating it is useful when only motion is needed. The selected trade-off is to keep the relations and alternatives that can change the requested answer, and to stop at a sufficient result. **Adapt:** :4.1–:4.3 construct those contributions, :4.4 derives the consequence, and :4.5–:4.6 limit stronger claims and additional work.

**Discrete operations and proof.** Lamport's [Specifying Systems](https://lamport.azurewebsites.net/tla/book-02-08-08.pdf), chapters 2–3 and §5.7, supplies before/after actions, unchanged values and the distinction between reachable invariance and an inductive assertion. **Adopt** these constructions in :4.2–:4.4 and :5.1. TLA's stuttering and fairness conventions serve their stated modeling purposes; choose progress assumptions for the use in :4.5.

**Constrained interaction.** Tong's [Classical Dynamics, §2.3](https://www.damtp.cam.ac.uk/user/tong/dynamics/dynhtml/S2.html) compares generalized coordinates and constraint-force treatment. **Adapt** the latter in :4.2 and :5.2 to retain the exchanged force when it is needed. Reduced coordinates offer a serious simpler alternative for motion alone. The cart derivation is an authored Newtonian case with its idealizations stated; another physical theory must supply its own relations.

**Coupled equations and events.** The [Modelica Language Specification 3.7, chapter 8](https://specification.modelica.org/maint/3.7/equations.html) supplies simultaneously satisfied equations, event semantics and consistent initialization. Its [DAE representation](https://specification.modelica.org/maint/3.7/modelica-dae-representation.html) separates continuous evolution and event processing: halt at a detected event, resolve its relations and restart integration. **Adapt:** :4.2–:4.3 keep joint relations distinct from evaluation order; :4.3.1 and :5.4 teach the continuous/event passage. Modelica supplies one explicit instantaneous-event convention; actual delays enter the model when consequential.

The joint Method is a conceptual synthesis whose comparison is supported by these constructions and their stated uses. Reopen the choice if a competing construction retains the same consequential continuations or interaction result at lower effort, or if an observed missing interaction, intermediate effect or event defeats the selected rule. Further Methods develop efficient exploration, proof, differential-equation solution and protocol design when the constructed rule requires that work.


## A.3.3.TR:End {#end}

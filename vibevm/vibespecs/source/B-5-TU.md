# B.5.TU - Construct a Working Use of an Unfamiliar Theory: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## B.5.TU:5 - Archetypal Grounding {#archetypal-grounding}

### B.5.TU:5.1 - Discover whether one input is enough {#discover-whether-one-input-is-enough}

A practitioner wants to use two available operations, `f: X -> Y` and `g: X -> Z`, on one input. The letters name distinct atomic types. The question is whether the chosen composition rules can produce both results from that input.

In a cartesian account, a copying operation `Delta_X: X -> X x X` supplies the pair of inputs. First copy, then apply the two operations: `(f x g) after Delta_X` sends `x` to `(f(x), g(x))`. The input of the parallel operation is now supplied.

Compare a resource-sensitive account generated only by `f`, `g`, identities, serial composition, tensoring and exchange of factors. Tensoring `f` with `g` takes `X tensor X` to `Y tensor Z`: it requires two inputs. Each given generator preserves the number of atomic factors, and serial composition, tensoring and exchange preserve that property. These rules therefore cannot construct `X -> Y tensor Z`. Supplying another input or adding an admissible copying operation changes what can be built. This is a result about the stated generated account.

Now apply the distinction. For a reusable data value interpreted through pure functions, both uses can receive that value. For a physical specimen consumed by an assay, obtain a physical way to supply what each assay needs. Dividing a specimen may supply those inputs if the assays admit the resulting portions. The word “copy” would leave that physical contribution unexplained.

The common method discovers the needed theory operation and returns its consequence to use. The cartesian construction and its contrast with tensor composition come from [Baez and Stay, §2.3](https://arxiv.org/html/0903.0340v3); the input-count argument makes the stated restricted case inspectable.

### B.5.TU:5.2 - Use variational mechanics to answer a motion question {#use-variational-mechanics-to-answer-a-motion-question}

An engineer wants to understand what a variational account predicts for an ideal carriage coasting along a straight horizontal track. Adopt a one-dimensional nonrelativistic free-particle model: positive mass `m`, negligible resistance and no applied driving force during the interval. Its Lagrangian is `L(q, v) = m*v*v/2`. For this case, the action is the time integral of that quantity along a proposed path. The physical model supplies this choice of Lagrangian.

The mechanical rule selects paths of stationary action: for every small path variation that leaves the endpoint positions fixed, the first-order change of action must vanish. The calculation below finds that path and shows that, for this free particle, it minimizes the action. Reproducing the calculation uses differentiation and definite integration; the displayed action identity can also be obtained as a supplied mathematical result.

Let the carriage pass `q=0` at time `0` and `q=d` at positive elapsed time `T`. Recover the operations hidden by “calculate the action”: choose a position function `q(t)`, differentiate it to obtain velocity, evaluate `L` on those values, then integrate over time. This is the constructive use developed in [SICM, §§1.3–1.4](https://mitp-content-server.mit.edu/books/content/sectbyfn/books_pres_0/9579/sicm_edition_2.zip/chapter001.html). The following one-dimensional case uses it.

Start with `q_0(t)=d*t/T`, and try paths
`q_a(t)=d*t/T + a*(t/T)*(1-t/T)`, where `a` is a length. Every path has the specified endpoint positions. Its velocity is `v_a(t)=(d+a*(1-2*t/T))/T`. Substitution and integration give
`S_a = m*(d*d+a*a/3)/(2*T)`.
For `m=1 kg`, `d=2 m` and `T=1 s`, the straight path has action `2 J s`; `a=1 m` gives `13/6 J s`.

This comparison favors the straight path within the chosen family. The general argument is also short. For any continuously differentiable added displacement `eta(t)` that is zero at both endpoints, the cross term integrates to `(m*d/T)*(eta(T)-eta(0))=0`. Thus the change in action is `(m/2)*integral(eta'(t)^2 dt)`, which is nonnegative. The straight path minimizes this action among those paths. For a nonzero `eta`, write this positive change as `K`. Along the paths `q_0+c*eta`, the action is `S[q_0]+c*c*K`, whose derivative at `c=1` is `2*K>0`. Thus a nonzero displacement from `q_0` cannot be stationary. The selected motion has constant velocity `d/T`.

The application now has an interpreted answer: under the adopted model, passing those endpoint positions in that time entails constant velocity. A computational implementation must evaluate the path derivative in the velocity argument before integrating. It can reproduce the numerical action comparison; the displayed argument supplies the wider conclusion.

Suppose the same two-metre trip must instead begin and end at rest. The constant-velocity answer fails that condition. The useful return is that the undriven free-particle account cannot supply this trip: the design needs acceleration and deceleration, and an account of the forces producing them. The next contribution is that driven-motion model. Increasing the resolution of the same free-particle calculation would retain the missing physical contribution.

### B.5.TU:5.3 - Keep a useful bound when the optimizer cannot be enacted {#keep-a-useful-bound-when-the-optimizer-cannot-be-enacted}

A planner learning optimization must select whole jobs for four available hours. At most one A-job is available, taking three hours for stipulated value 5; at most two B-jobs are available, each taking two hours for value 3. Durations and values add in this constructed problem.

A linear relaxation permits real counts `0 <= x <= 1`, `0 <= y <= 2` with `3*x+2*y <= 4`. It returns `x=1, y=0.5`, value `6.5`. Recover the argument: the time condition gives `y <= (4-3*x)/2`, so `5*x+3*y <= 6+0.5*x <= 6.5`; the returned pair attains that limit.

For the actual whole-job choice, enumerate the alternatives. With A selected, no B fits and value is 5. Without A, two B-jobs fit and value is 6. Select two B-jobs. The fractional optimizer has still supplied a useful bound: no whole-job arrangement can attain value 7 because every such arrangement is also admitted by the relaxation.

The use of the theory changes with the question. Selecting work needs an attainable arrangement; excluding a target can use a bound. The practitioner needs to recover that relation before deciding whether a further optimization step is useful. B.5:5.4 also works the changed five-hour case.

## B.5.TU:6 - Bias-Annotation {#bias-annotation}

The worked cases favor explicit mathematical accounts with small, inspectable operations. Other theories can use qualitative or interpretive inferences; their warranted application conditions and criticism must come from the relevant practice. A convenient numerical example should not decide which kind of explanation the question needs.

Familiar terminology can make a supplied interpretation look independently recovered. Attribute the actual contribution when assessing learning or capability. In ordinary assisted work, use the supplied result at the scope its interpretation supports.

## B.5.TU:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Observed difficulty in the method's cases | Repair |
| --- | --- |
| Reuse a composition while overlooking how many inputs it consumes. | Recover the permitted operations and supply their inputs; in :5.1, copying is the decisive additional operation. |
| Evaluate a familiar-looking expression before filling its arguments. | Construct the path, derivative and substitution required by the operation, as in :5.2. |
| Improve a computation whose formulation omits the receiving condition. | Recover that condition and change the model or question; finer calculation of undriven motion leaves departure at rest unresolved. |
| Discard an infeasible optimizer together with its valid bound. | Interpret each result separately; :5.3 retains the exclusion of value 7. |
| Require the same depth of study for using and altering a result. | Locate the contribution the work needs, then recover or obtain the reasoning that enables it. |

## B.5.TU:10 - Architectural Rationale {#architectural-rationale}

The method joins two directions of reasoning. Working backward from the question reveals the needed contribution. Working forward through the theory tests whether the available objects and operations actually supply it. Returning the consequence to use exposes conditions a correct internal calculation can leave unresolved.

B.5.RC and B.5.RA recover constructions and arguments. Here they contribute to assembling an application whose meaning and needed output may still be unsettled. C.29 constructs and tests mathematical correspondence; it can start before a mathematical object has been selected. This method adds recovery of how the unfamiliar theoretical account becomes usable at that point. A theory can also be used within its own mathematical setting, as in the composition case.

A complete explanation of the theory can be the appropriate learning project. For one urgent use, however, an adequate supplied application or bounded specialist result may settle the question sooner. The choice depends on the work the receiver must perform, including any need to criticize or change the method later.

A small successful application provides something to use and a basis for further inquiry. Broader generalization requires its own argument. If the application exposes a limitation in the theory, the resulting construction or counterexample can become material for developing its objects, rules or questions.

## B.5.TU:11 - SoTA-Echoing {#sota-echoing}

**How much theory must be reconstructed for a first use?** Adapt [van Oostrum, Langer and Ay (2025), Introduction and §§1–2, 4](https://arxiv.org/html/2406.07726v4): connect the operational question to stated model variables and inference, work an example, and recover deeper derivations when they are needed. The alternative is to use an interpreted supplied implementation. Retain that cheaper route when it suffices; reconstruct dependencies when adaptation or explanation requires them. Sections :4.1–:4.4 make that choice explicit. The source provides a discrete active-inference account and a minimal implementation, not evidence that one learning sequence suits every practice or agent.

**How can notation reveal what an application still lacks?** Adapt [SICM's Preface](https://mitp-content-server.mit.edu/books/content/sectbyfn/books_pres_0/9579/sicm_edition_2.zip/preface001.html): recover function arguments, substitutions and composition where implicit conventions obscure the operation. A familiar conventional expression is cheaper when the reader can already use it reliably. Sections :4.2–:4.4 therefore call for operative reconstruction at the unresolved step; :5.2 supplies a case. The selected contribution is explicit operation recovery. Its source's strong requirement of automatic interpretability is appropriate for computational exposition; ordinary use may be settled by a clear hand-worked construction.

**What does a theory's formal structure contribute to an application?** Adopt [Baez and Stay, §2.3](https://arxiv.org/html/0903.0340v3)'s constructive comparison of cartesian and monoidal operations. A familiar “parallel composition” description can leave input duplication unresolved. Section :5.1 obtains the required operation or the obstruction under stated rules, then asks whether the receiving practice can supply it. This pays the cost of recovering only the consequential structure. The broader cross-disciplinary correspondences in that paper do not establish the physical copying operation in our case.

The common method is a synthesis of these contributions. Reopen it when a better approach obtains a usable application with less reconstruction, when a recurring failure requires another connecting operation, or when changed tools alter the contribution the receiver must understand.


## B.5.TU:End {#end}

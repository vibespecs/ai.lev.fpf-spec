# A.1.RI - Reidentifying an Object across Observations: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.1.RI:5 - Archetypal Grounding {#archetypal-grounding}

### A.1.RI:5.1 - Associate two moving objects and retain an unresolved alternative {#associate-two-moving-objects-and-retain-an-unresolved}

Consider two persistent point objects with independent motion on one axis; their paths may cross. Each object is observed once at each end of a one-second interval. Positions are assumed known in one common frame. Initially A is at 0 cm and B at 10 cm. Later R is at 1 cm and S at 9 cm.

The motion account limits speed to 2 cm/s. Construct the complete associations:

| Association | Required displacement magnitudes | Result under the speed bound |
| --- | --- | --- |
| A to R; B to S | 1 cm each | Admissible; the two straight paths give a joint realization. |
| A to S; B to R | 9 cm each | Excluded; each exceeds the permitted displacement. |

Under these premises, R observes the continuing A and S the continuing B. A's displacement is +1 cm and B's is -1 cm.

Now allow speed up to 10 cm/s. Both associations have admissible straight paths. The observations leave A's displacement as either +1 or +9 cm; choosing the shorter path adds a preference absent from the speed-bound premise.

Suppose the next question is instead the mean position of these two objects. It was 5 cm and is still 5 cm under both associations. That calculation can proceed without another observation. If a following action must address A individually, look for a discriminator that matters to that action or use an explicitly permitted provisional association.

If the motion premise changes again to a bound below 1 cm/s, neither complete association fits. Reconsider the bound or the observation account before asserting an identification.

### A.1.RI:5.2 - Test associations together {#test-associations-together}

Keep the one-second, independent, persistent-point and complete-detection premises. Initially A is at 0 cm and B at 1 cm; later R is at 2 cm and S at 3 cm. Each displacement is at most 2 cm.

The admissible pairs are A-R, B-R and B-S. B's nearest detection is R. Assigning it first leaves A without a permitted observation. The joint association A-R with B-S satisfies every constraint and uses each later observation once. It is the only complete association under these premises.

The common Method contributes the joint comparison. The supplied motion bound and complete-detection rule determine which associations it tests. If missed or repeated detections become possible, revise those premises and reconstruct the affected alternatives.

### A.1.RI:5.3 - Separate a process run from a reused number {#separate-a-process-run-from-a-reused-number}

An operator wants to compare resource use in two reports carrying the same process number. The object of interest is one process run. Both reports concern the same machine boot and PID naming scope; their fields are assumed to describe the indicated process consistently.

The first report gives start time 1,000 ticks after boot; the second gives 2,400 ticks. Linux exposes such a start-time field in `/proc/pid/stat`. The changed start time excludes continuation of the earlier run, despite the repeated number. Keep the two runs' resource totals separate; subtracting the earlier total from the later one would not measure one run's interval use.

If the reports contain only the number and executable name, they can fit either continuation or termination followed by reuse. An available lifecycle event may distinguish them. For ongoing supervision, a retained process reference such as a Linux PID file descriptor can make a fresh number-based inference unnecessary.

This case resolves run continuity. A question about a service continuing through replacement processes uses the service's own continuation criterion.

## A.1.RI:6 - Bias-Annotation {#bias-annotation}

Under E.3's five Principle-Taxonomy lenses (Gov, Arch, Epist, Prag and Did), this Method concerns what observation and subject constraints support about an object's continuation. Its finite examples favor explicit alternatives and simple constraints. Many real tracking problems require distributions, approximate inference or decisions under unresolved identity.

The Method can be performed by people, computational agents or coordinated teams. Their observation access and ability to construct alternatives differ.

## A.1.RI:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure in these situations | Consequence | Repair |
| --- | --- | --- |
| Treat a reused label as uninterrupted object continuity | Resource totals or actions can be assigned to another run or object. | Apply the relevant lifecycle or continuity rule to the available observations. |
| Accept a plausible pair without its shared constraints | Another object loses its only possible observation. | Compare the complete associations that must hold together. |
| Report the best-ranked connection as the only possible one | A scoring preference becomes an unsupported identification. | Keep the ranking assumption and test alternatives when uniqueness matters. |
| Require identity resolution for an invariant aggregate | Additional observation delays a result already determined. | Evaluate the receiving quantity across the surviving associations. |
| Treat a failed model as evidence that one convenient association is true | Contradictory observations or rules remain hidden in later reasoning. | Locate the incompatible premise or observation and repair that contribution. |

## A.1.RI:10 - Architectural Rationale {#architectural-rationale}

Object continuity and observation identity answer different questions. Relating two observations to one object can be a substantive result of reasoning: a motion account connects positions, or lifecycle information distinguishes runs. The observations can retain different claims after that result is obtained.

The common construction couples three contributions: a criterion of continuation, constraints connecting observations, and a comparison of the connections relevant to use. Spatial motion supplies one realization. Lifecycle and other subject rules supply different realizations of the same Method.

A.1 supplies the general individuation question. This member develops observation-based reidentification without requiring the object to be recognized as a holon or system. C.2.1 retains the episteme questions, and C.16 supplies measurement interpretation. Their distinct results can participate in one investigation.

## A.1.RI:11 - SoTA-Echoing {#sota-echoing}

**Practice question and choice.** What may observations support about the continuation of an object? Use the domain criterion and observation account to construct and compare relevant associations; retain the distinctions that change the receiving use.

**A comparison at the same finite task.** In :5.1 with the 10 cm/s bound, selecting the association with the smaller total displacement gives A-R/B-S. Comparing all admissible associations retains that candidate and A-S/B-R. Both methods can use the same four distances and supplied constraints. The selected construction additionally keeps the second complete association and its consequences. This small cost answers whether the speed-bound observations resolve the identity. The minimum-displacement choice supplies a provisional association when the practice accepts that preference; it adds an assumption that the stated motion bound did not provide. The mean-position use needs neither choice nor more observations.

**Adapt** Andrei Rodin's [*Venus Homotopically*](https://philsci-archive.pitt.edu/12116/1/vh.pdf), §§2-8: observation and a theory-supported connecting construction contribute to identification. The distinction between possible and actual trajectories motivates :4.3-4.4. Its homotopy-type interpretation is one mathematical reconstruction, while the ordinary Method uses whichever subject construction supplies the connection.

**Adapt** the explicit association operation in Bewley et al., [*Simple Online and Realtime Tracking*](https://arxiv.org/abs/1602.00763), §3.3, as a historical computational comparator. It combines predicted states, an association cost and a globally solved assignment for online tracking. The present synthesis keeps subject constraints, ranked selection and the strength of an identifying conclusion separate. SORT's benchmark results do not establish the performance of this general Method, and the finite displacement comparison above is an authored case rather than its image-overlap algorithm.

**Adopt** the relevant lifecycle meanings from the current Linux manuals for [process start time](https://man7.org/linux/man-pages/man5/proc_pid_stat.5.html) and [PID file descriptors](https://man7.org/linux/man-pages/man2/pidfd_open.2.html) in :5.3. They supply a nonspatial continuation case and a direct-use alternative to reconstructing identity from repeated numbers.

Reopen the chosen construction when a changed subject or observation model admits a consequential omitted association, an available reference makes reconstruction unnecessary, or a cheaper procedure supplies the distinction needed for use. A new tracking algorithm's practical gains belong to its stated object, data and decision conditions.


## A.1.RI:End {#end}

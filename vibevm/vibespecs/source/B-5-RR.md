# B.5.RR - Revise Reasoning After a Premise or Question Changes: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## B.5.RR:5 - Archetypal Grounding {#archetypal-grounding}

### B.5.RR:5.1 - Changing the range of a sum {#changing-the-range-of-a-sum}

A reader has established S(n)=n² for the sum of the first n positive odd integers, with S(0)=0 and n a nonnegative integer. The argument uses the shared initial value and increment: S(n+1)−S(n)=2n+1, also the increment from n² to (n+1)².

The new question asks for n terms beginning at 3: 3+5+...+(2n+1). The change is the range of summation. Reuse the established result on the first n+1 terms and remove the initial 1:

T(n)=S(n+1)−1=(n+1)²−1=n²+2n.

For n=4, the new sum is 3+5+7+9=24. The old formula applied unchanged would return 16. The proof of S survives; the application of that proof changes.

This repair also exposes a reusable construction. For n terms starting at a and increasing by 2, term j, counted from j=0, is (2j+1)+(a−1). Summing the established odd-number terms and the n equal additions gives n²+n(a−1). Changing the increment would require another derivation. The worked extension makes the next question precise without assuming that the same correction covers every progression.

For the next use, retain four terms and the increment 2, but require their sum to be 28. The former starting value a=3 becomes the unknown: 16+4(a−1)=28 gives a=4. Checking 4+6+8+10=28 confirms the required sum. If there are zero terms and the required sum is positive, no starting value can supply it: the empty sum is zero for every a. The changed question then requires a different term count or total.

### B.5.RR:5.2 - Losing one way to recover a report {#losing-one-way-to-recover-a-report}

A team needs to read revision 17 of a report. Its established account has two ways to obtain that revision's bytes: decrypt the local backup using its available key and decryptor, or obtain an unencrypted remote copy. An available viewer then displays the report.

The key becomes unavailable. Following that change removes the local decryption route. The remote copy and viewer still supply the requested reading, so the team can proceed through them. The missing key need not be recovered for this use.

Now consider a different finding: the supposed remote alternative is encrypted with the same key. Both routes need that key, so neither supplied route obtains the bytes. The next contribution is the key, another usable copy or a different way to obtain the report. A second storage location had concealed a shared prerequisite.

If instead the viewer becomes unavailable, either route may still provide the bytes. Reading now needs a suitable viewer or format conversion. This repair preserves the obtained result and locates the different operation that the receiving use requires.

### B.5.RR:5.3 - A repeated conclusion loses its starting support {#a-repeated-conclusion-loses-its-starting-support}

An analysis establishes claim A from an observation O, derives B from A and uses B in a further argument for A. A corrected interpretation of O removes its support for A.

The second occurrence of A does not preserve that support: its offered reason B was itself obtained from A. Reopen both uses and look for an argument grounded in retained premises. The conclusion may be true, but this circular route no longer establishes it.

Contrast this with an induction argument whose base case remains established and whose step derives the next case from the preceding one. Its recurrence has a grounded way to obtain each finite case. The relevant inference, rather than the visual presence of a cycle or repeated letter, decides what can be retained.

## B.5.RR:6 - Bias-Annotation {#bias-annotation}

The examples favor explicit premises and recoverable derivations. In statistical or interpretive work, revising one observation can require reconsidering dependence, selection or meaning before the changed conclusion can be obtained. Use the practice's inference method; a list of supporting statements does not supply it.

The method can also overvalue salvage. When the earlier reasoning is poorly recoverable and an adequate new answer is cheap, obtain the new answer.

## B.5.RR:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Observed failure in revision | Why it matters | Repair |
| --- | --- | --- |
| Replace a number while retaining the old question | The calculation still solves for the former unknown. | Restate the givens and requested result before choosing the computation. |
| Treat the loss of one argument as a refutation | A different sufficient argument may remain. | Examine its premises and derive the conclusion or its negation separately. |
| Count two dependent arguments as independent | Both can fail with their shared prerequisite. | Follow the common premise through both uses. |
| Preserve a conclusion through circular repetition | The retained statements supply no starting support. | Recover a grounded argument or leave the conclusion unresolved. |
| Repair the whole report to answer a small change | Unaffected results are needlessly reproduced. | Compare affected repair with a fresh sufficient answer and choose the useful scope. |

## B.5.RR:10 - Architectural Rationale {#architectural-rationale}

An argument and an application can change separately. A theorem can remain established while its former substitution ceases to answer the question. An empirical premise can become doubtful while its conditional consequences remain worth investigating. Keeping those distinctions lets revision preserve knowledge without preserving an unsupported use.

The method therefore joins backward recovery of what the desired result needs with forward derivation from the premises now available. Alternative arguments preserve useful results; shared prerequisites explain where that preservation fails. Detailed deduction, statistical inference and physical-model revision remain contributions of their respective practices.

This is a method of obtaining and applying knowledge. Its result can also change the method repertoire: the revised sum reveals a parameterized construction, and an unresolved dependency can become the next research question. Those continuations are useful when they enable further work.

## B.5.RR:11 - SoTA-Echoing {#sota-echoing}

**Which part of an argument needs revision?** Adapt the assumption-sensitive reasoning of de Kleer's [*A General Labeling Algorithm for Assumption-Based Truth Maintenance* (1988), §2](https://cdn.aaai.org/AAAI/1988/AAAI88-034.pdf). Compared with discarding every conclusion that used a removed premise, §4.3 retains sufficient alternatives and their shared conditions. This historical computational method supplies a precise model of conditional support. The present method uses that insight without requiring an ATMS or exhaustive assumption labels for an ordinary inquiry.

**When is incremental repair cheaper than starting again?** Adapt the comparison in Hu, Motik and Horrocks, [*Optimised Maintenance of Datalog Materialisations* (2018), §§1–4](https://www.cs.ox.ac.uk/people/boris.motik/pubs/hmh18optimised-maintenance.pdf): eagerly finding alternative derivations can avoid unnecessary deletion, but that search can itself be costly; recursive support needs more than simple counting. Section 4.3 therefore compares recovery and repair with a fresh answer. These are results for Datalog maintenance; selecting subject premises and interpreting empirical change require further reasoning.

**What should repair preserve for its receiver?** Adapt Klowden and Tao's [*Mathematical methods and human thought in the age of AI* (2026), §§4.4–4.6](https://arxiv.org/html/2603.26524v1). An inspectable proof result can serve one use, while changing its assumptions or applying its idea needs recoverable reasoning. Sections 4.1–4.5 retain that receiving question. The trade-off is explanation and recovery effort when another use actually needs them; full exposition is unnecessary for an already adequate application.

**What does current automated proof repair contribute?** [Wang et al., *Learning to Repair Lean Proofs from Compiler Feedback* (2026), §§3–5](https://arxiv.org/html/2602.02990v1), studies repair from generated failures and compiler feedback. Adapt its use of a localized failing transition when such feedback is available. Its single-shot formal-repair result answers a narrower question than choosing changed premises or interpreting an application. Section 4.4 preserves those questions instead of using compiler success as their answer.

Reopen these choices when better dependency recovery, subject inference or repair support changes the attainable result or the cost of obtaining it.


## B.5.RR:End {#end}

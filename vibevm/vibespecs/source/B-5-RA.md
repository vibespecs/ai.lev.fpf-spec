# B.5.RA - Recover an Argument for Its Next Use: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## B.5.RA:5 - Archetypal Grounding {#archetypal-grounding}

### B.5.RA:5.1 - Understanding why the sum of odd numbers is a square {#understanding-why-the-sum-of-odd-numbers-is-a-square}

Consider this compressed argument: “The sum of the first n positive odd numbers is n²: the sum and the square start at zero, and both increase by 2n+1 when n increases by one.” The statement concerns every nonnegative integer n. A reader recognizes the formula but needs to explain the steps compressed in that reason.

Write S(0)=0 and S(n+1)=S(n)+(2n+1). The main reason is that both the sum and the square start at zero and grow by the same amount when n increases by one. The algebraic identity (n+1)²−n²=2n+1 supplies that connection.

Recover the general transition. Assuming S(n)=n² for an arbitrary nonnegative integer n gives:

S(n+1)=S(n)+2n+1=n²+2n+1=(n+1)².

The temporary assumption is the induction hypothesis. It supports the successor step. Together with S(0)=0, that step establishes the statement for every nonnegative integer by induction.

For n=3, the sum is 1+3+5=9. Adding the next odd number, 7, gives 16. This instance makes the equal-increment operation visible. The argument's reach comes from the arbitrary n, the base value and the induction rule.

A square drawing gives another way to follow the increment: grow an n-by-n square with a row of n cells and a column of n+1 cells. That adds 2n+1 cells. The drawing and algebra expose the same increment under the counting interpretation.

The reader can now explain the role of the initial value and successor step. If the next task instead asks for the sum of n odd terms beginning at 3, the changed range opens a revision: use the established sum through the (n+1)th odd number and remove the first term, giving S(n+1)−1=n²+2n. For four terms, 3+5+7+9=24. The reusable contribution is the recovered relation between range, initial value and increment.

If the original question asked only for 1+3+5, direct addition would already supply the result. Recovering the general argument earns its effort when explanation, general use or revision needs it.

### B.5.RA:5.2 - Understanding a drawing-recovery argument {#understanding-a-drawing-recovery-argument}

A team needs to open an archived engineering drawing for reuse. Someone argues that the drawing is recoverable because three backup copies exist.

Recover the method behind that conclusion. For the encrypted-backup route, the needed contributions are readable stored data, an available way to decrypt it and a decoder for the drawing format. Their joint use produces a readable drawing. Having more copies addresses loss of stored data, while all three may still share one decryption key.

Suppose the key is unavailable. The backup count leaves the decoding route incomplete. The next useful question is whether the key can be recovered or another usable copy obtained. The recovered argument identifies that missing prerequisite.

Now suppose a separate plaintext copy in a readable format is available. That gives a different route to the drawing and permits the team to continue without recovering the encryption key for this use. The original encrypted route remains conditional.

The result is a usable recovery choice or a focused request for a missing contribution. A later claim that the opened drawing describes the present equipment requires its own comparison; the file-opening argument answers the immediate recovery question.

## B.5.RA:6 - Bias-Annotation {#bias-annotation}

Familiar vocabulary and a correct-looking calculation can create confidence before the reasoning has been recovered. Conversely, checking every line can consume attention while leaving the role of a lemma unexplained. Use the local transition and the main reason together.

AI-generated formal proofs make the distinction consequential: a checked formal derivation supplies a result under its formal definitions, while the intended statement and the explanatory structure needed for reuse may still need recovery. The relevant comparison is the one that can change the contemplated use.

## B.5.RA:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure in the working situation | Repair |
| --- | --- |
| Paraphrasing successive claims while the inference remains missing | Apply the relevant definition, rule or earlier result to the transition's actual premises. |
| Checking local steps while failing to explain why a lemma or construction appears | Recover the difficulty that contribution resolves and connect it to the conclusion. |
| Treating several uses of one premise as several independent grounds | Keep the common prerequisite visible and examine its role in the needed branches. |
| Promoting a temporary assumption to an established premise | Recover the subargument and the conclusion obtained when that assumption is discharged. |
| Using one example to claim that the general statement has been proved | Recover the argument that covers the stated domain; retain the example as an illustration of it. |
| Demanding a complete reproof when the task only needs an established result under its stated conditions | Use that result at the needed level; open its internals when the new question requires them. |

## B.5.RA:10 - Architectural Rationale {#architectural-rationale}

A source orders its text for exposition; the argument relates premises, intermediate contributions and conclusions. Understanding therefore needs more than following the paragraph order. Backward dependency recovery identifies what the desired conclusion uses, while recovery of the main reason explains why those contributions were chosen.

Local and overall understanding constrain each other. In :5.1, the equal-increment idea explains the role of the recurrence, and the induction step establishes the general result. In :5.2, the recovery route explains why the key and format matter, and their availability determines which route can be used. A fluent summary that cannot support these transitions is insufficient for the intended use.

This common method concerns recovery of reasoning already offered for a result. B.5 coordinates the broader inquiry; B.5.RC recovers an auxiliary construction; a subject method supplies an unfamiliar inference. To explain the result to someone else, select the reasoning and representation that make their intended use possible. C.2.8 helps characterize what that recipient can extract under stated preparation and access.

Recovery also makes revision possible. The changed premise can be followed through the contributions that use it, while independent arguments remain available. Revision has its own task and result; recovering the original argument supplies the dependency information it needs.

## B.5.RA:11 - SoTA-Echoing {#sota-echoing}

**Local and overall proof comprehension.** Mejía-Ramos and colleagues distinguish understanding terms, logical status and justifications from understanding a proof's main idea, components, transfer and examples. Their [2017 account of developing and validating proof-comprehension tests](https://sites.math.rutgers.edu/~jpmejia/files/Mejia_TUES_method.pdf), §2.2, develops the earlier 2012 model and makes the dimensions operational for particular undergraduate proofs. This pattern adopts the combination of local transitions and overall method in :4.2–:4.4. The published assessment results concern those proof-reading settings, while the generic recovery procedure here is a synthesis.

**Self-explanation.** Hodds, Alcock and Inglis's work is accompanied by the [Loughborough guide for mathematics lecturers](https://www.lboro.ac.uk/media/media/schoolanddepartments/mathematics-education-centre/downloads/SE-booklet-guide.pdf). It explains why relating claims to prior knowledge and to other claims differs from confidence reports or paraphrase. This contribution informs :4.4. The evidence reported there concerns undergraduate mathematical proof comprehension; it does not establish the effectiveness of this whole method for every practice or AI agent.

**Later assessment work.** The [PRIUM framework](https://doi.org/10.1007/s11858-024-01628-1), Cooley and colleagues (2024), develops proof-comprehension assessment through questions about definitions, statements and their relationships, with revision informed by discrepancies between intended questions and student answers. That is an assessment contribution to consider when demonstrated comprehension is required. The present method supplies the recovery work; it does not require a departmental assessment programme for an ordinary use.

**AI-assisted reasoning.** Klowden and Tao's [Mathematical Methods and Human Thought in the Age of AI](https://arxiv.org/html/2603.26524v1), especially §4.4, distinguishes a verified formal statement from the intended statement and from the explanatory reasoning around a proof. This pattern adopts the intended-use comparison and the recovery of the method behind the result. The essay provides a contemporary conceptual argument, rather than an experiment validating this procedure.

**Recoverable methods beyond answer production.** The [Math and AI declaration](https://mathandai.org/) raises the risk that rapid answer production can outpace understanding and development of methods. It is a position statement. This pattern takes the resulting recovery question: which reasoning can the next practitioner actually use? Human or AI production does not settle that question; the returned argument and its use do.

**Bounded method choice.** Compare line-by-line paraphrase, full proof validation and use-directed recovery on the same short argument. Paraphrase can retain the odd-sum formula while missing the equal-increment reason. Full validation answers correctness, but may spend effort inside already usable lemmas. Recovering the main reason together with the needed transitions gives the explanation or changed-use basis sought here. Select it when that is the unresolved task; retain full validation when correctness of the complete argument is the required conclusion. The drawing-recovery case extends the dependency method to a practical inference without treating mathematical proof as the sole form of reasoning. Reconsider this recovery approach if prepared readers repeatedly cannot recover why the decisive inference works, while another explanation or reading method enables the same use with comparable effort.


## B.5.RA:End {#end}

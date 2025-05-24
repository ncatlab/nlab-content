

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

*QWIRE* &lbrack;[Paykin, Rand & Zdancewic (2017)](#PaykinRandZdancewic17)&rbrack; is a [[quantum programming language]] for [[quantum circuit]] [[certified programming|certification]] based on [[linear type theory]] combined with [[intuitionistic type theory]] via the [[exponential modality]]. More specifically, it is a [[domain specific programming language]] for [[quantum circuits]] meant to be [[domain specific embedded programming language|embedded]] into an [[intuitionistic type theory]]. As such it is similar to *[[Quipper]]*.

## Related

* [[QBricks]]

* [[Quipper]]

* [[CoqQ]]

* [[quantum programming languages]]

## References

The original article

* {#PaykinRandZdancewic17} [[Jennifer Paykin]], [[Robert Rand]], [[Steve Zdancewic]], *QWIRE: a core language for quantum circuits*, POPL 2017: Proceedings of the 44th ACM SIGPLAN Symposium on Principles of Programming Languages (2017) 846–858 &lbrack;[doi:10.1145/3009837.3009894](https://doi.org/10.1145/3009837.3009894)&rbrack;



Theoretical background:

* [[Robert Rand]], *Formally Verified Quantum Programming*, UPenn (2018) &lbrack;[ediss:3175](https://repository.upenn.edu/edissertations/3175)&rbrack;

  > emphasis on [[formal software verification]]:

  > &lbrack;p. iv:&rbrack; "We argue that [[quantum programs]] demand [[proof assistant|machine-checkable proofs]] of correctness. We justify this on the basis of the complexity of programs manipulating [[quantum states]], the expense of running [[quantum programs]], and the inapplicability of traditional debugging techniques to programs whose states cannot be examined."

  > &lbrack;p. 3:&rbrack; "Quantum programs are tremendously difficult to understand and implement, almost guaranteeing that they will have bugs. And traditional approaches to debugging will not help us: We cannot set breakpoints and look at our qubits without [[quantum state collapse|collapsing the quantum state]]. Even techniques like unit tests and random testing will be impossible to run on classical machines and too expensive to run on quantum computers – and failed tests are unlikely to be informative"

  > &lbrack;p. 4:&rbrack; "Thesis Statement: *[[quantum programming|Quantum programming]] is not only amenable to [[software verification|formal verification]]: it demands it.*"

  > "The overarching goal of this thesis is to write and verify quantum programs together. Towards that end, we introduce a quantum programming language called [[Qwire]] and embed it inside the [[Coq]] [[proof assistant]]. We give it a [[linear type system]] to ensure that it obeys the laws of [[quantum mechanics]] and a [[denotational semantics]] to prove that programs behave as desired."


* [[Jennifer Paykin]], *Linear/non-Linear Types For Embedded Domain-Specific Languages*, 2018 ([upenn:2752](https://repository.upenn.edu/edissertations/2752))


Application to [[verified programming]] after [[domain specific embedded programming language|embedding]] into [[Coq]]:

* {#RandPaykinZdancewic18} [[Robert Rand]], [[Jennifer Paykin]], [[Steve Zdancewic]], *QWIRE Practice: Formal Verification of Quantum Circuits in Coq*, EPTCS **266** (2018) 119-132 &lbrack;[arXiv:1803.00699](https://arxiv.org/abs/1803.00699)&rbrack;

* [[Robert Rand]], [[Jennifer Paykin]], Dong-Ho Lee, [[Steve Zdancewic]], *ReQWIRE: Reasoning about Reversible Quantum Circuits*, EPTCS **287** (2019) 299-312 &lbrack;[arXiv:1901.10118](https://arxiv.org/abs/1901.10118), [doi:10.4204/EPTCS.287.17](https://doi.org/10.4204/EPTCS.287.17)&rbrack;


Using [[domain specific embedded programming language|embedding]] into [[homotopy type theory]]:

* {#PaykinZdancewic19}[[Jennifer Paykin]], [[Steve Zdancewic]], *A HoTT Quantum Equational Theory*, [talk at QPL2019](http://qpl2019.org/a-hott-quantum-equational-theory/) &lbrack;[arXiv:1904.04371](https://arxiv.org/abs/1904.04371)&rbrack;

For development *EWIRE*:

* [[Mathys Rennela]], [[Sam Staton]], *Classical Control, Quantum Circuits and Linear Logic in Enriched Category Theory*, Logical Methods in Computer Science **16** (2020) lmcs:6192 &lbrack;[arXiv:1711.05159](https://arxiv.org/abs/1711.05159)<a href="https://doi.org/10.23638/LMCS-16(1:30)2020">doi:10.23638/LMCS-16(1:30)2020</a>&rbrack;


Fork development *SQIR*:

* [[Kesha Hietala]], [[Robert Rand]], [[Shih-Han Hung]], Xiaodi Wu, [[Michael Hicks]], *A verified optimizer for Quantum circuits*, Proceedings of the ACM on Programming Languages **5** Issue POPL 37 (2021) 1–29 &lbrack;[doi:10.1145/3434318](https://doi.org/10.1145/3434318)&rbrack;

* [[Kesha Hietala]], [[Robert Rand]], [[Shih-Han Hung]], Liyi Li, [[Michael Hicks]], *Proving Quantum Programs Correct*, in *12th International Conference on Interactive Theorem Proving (ITP 2021)*, Leibniz International Proceedings in Informatics (LIPIcs) **193** (2021) &lbrack;[arXiv:2010.01240](https://arxiv.org/abs/2010.01240)&rbrack;

* [[Kesha Hietala]], *A verified software toolchain for quantum programming* (2022) &lbrack;[pdf](https://khieta.github.io/files/drafts/khieta-dissertation.pdf), [blog](https://blog.sigplan.org/2021/06/02/verifying-a-quantum-compiler/)&rbrack;


category: people

[[!redirects Qwire]]

[[!redirects SQIR]]
[[!redirects EWIRE]]


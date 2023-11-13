
* [personal page](http://rand.cs.uchicago.edu/)


## Selected writings

Introducing *[[QWIRE]]*, a [[quantum programming language]] based on [[linear type theory]] connected with [[intuitionistic type theory]] via the [[exponential modality]]:

* {#PaykinRandZdancewic17} [[Jennifer Paykin]], [[Robert Rand]], [[Steve Zdancewic]], *QWIRE: a core language for quantum circuits*, POPL 2017: Proceedings of the 44th ACM SIGPLAN Symposium on Principles of Programming LanguagesJanuary 2017 Pages 846–858 ([doi:10.1145/3009837.3009894](https://doi.org/10.1145/3009837.3009894))

Application to [[verified programming]] after implementation in [[Coq]]:

* [[Robert Rand]], [[Jennifer Paykin]], [[Steve Zdancewic]], *QWIRE Practice: Formal Verification of Quantum Circuits in Coq*, EPTCS 266, 2018, pp. 119-132 ([arXiv:1803.00699](https://arxiv.org/abs/1803.00699))

* [[Robert Rand]], *Formally Verified Quantum Programming*, UPenn (2018) &lbrack;[ediss:3175](https://repository.upenn.edu/edissertations/3175)&rbrack;

  > &lbrack;p. iv:&rbrack; "We argue that [[quantum programs]] demand [[proof assistant|machine-checkable proofs]] of correctness. We justify this on the basis of the complexity of programs manipulating [[quantum states]], the expense of running [[quantum programs]], and the inapplicability of traditional debugging techniques to programs whose states cannot be examined."

  > &lbrack;p. 3:&rbrack; "Quantum programs are tremendously difficult to understand and implement, almost guaranteeing that they will have bugs. And traditional approaches to debugging will not help us: We cannot set breakpoints and look at our qubits without [[quantum state collapse|collapsing the quantum state]]. Even techniques like unit tests and random testing will be impossible to run on classical machines and too expensive to run on quantum computers – and failed tests are unlikely to be informative"

  > &lbrack;p. 4:&rbrack; "Thesis Statement: *[[quantum programming|Quantum programming]] is not only amenable to [[software verification|formal verification]]: it demands it.*"

  > "The overarching goal of this thesis is to write and verify quantum programs together. Towards that end, we introduce a quantum programming language called [[Qwire]] and embed it inside the [[Coq]] [[proof assistant]]. We give it a [[linear type system]] to ensure that it obeys the laws of [[quantum mechanics]] and a [[denotational semantics]] to prove that programs behave as desired." 



* [[Robert Rand]], [[Jennifer Paykin]], Dong-Ho Lee, [[Steve Zdancewic]], *ReQWIRE: Reasoning about Reversible Quantum Circuits*, EPTCS **287** (2019) 299-312 &lbrack;[arXiv:1901.10118](https://arxiv.org/abs/1901.10118), [doi:10.4204/EPTCS.287.17](https://doi.org/10.4204/EPTCS.287.17)&rbrack;


Further on [[quantum circuit]] [[certified programming|certification]] with the [[quantum programming language]] *[[SQIR]]*:

* [[Kesha Hietala]], [[Robert Rand]], [[Shih-Han Hung]], Xiaodi Wu, [[Michael Hicks]], *A verified optimizer for Quantum circuits*, Proceedings of the ACM on Programming Languages **5** Issue POPL 37 (2021) 1–29 &lbrack;[doi:10.1145/3434318](https://doi.org/10.1145/3434318)&rbrack;

* [[Kesha Hietala]], [[Robert Rand]], [[Shih-Han Hung]], Liyi Li, [[Michael Hicks]], *Proving Quantum Programs Correct*, in *12th International Conference on Interactive Theorem Proving (ITP 2021)*, Leibniz International Proceedings in Informatics (LIPIcs) **193** (2021) &lbrack;[arXiv:2010.01240](https://arxiv.org/abs/2010.01240)&rbrack;



category: people

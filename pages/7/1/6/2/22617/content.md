

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

* [[Quipper]]

* [[CoqQ]]

* [[quantum programming languages]]

## References

The original article

* {#PaykinRandZdancewic17} [[Jennifer Paykin]], [[Robert Rand]], [[Steve Zdancewic]], *QWIRE: a core language for quantum circuits*, POPL 2017: Proceedings of the 44th ACM SIGPLAN Symposium on Principles of Programming LanguagesJanuary 2017 Pages 846–858 ([doi:10.1145/3009837.3009894](https://doi.org/10.1145/3009837.3009894))



Theoretical background:

* [[Robert Rand]], *Formally Verified Quantum Programming*, UPenn (2018) &lbrack;[ediss:3175](https://repository.upenn.edu/edissertations/3175)&rbrack;

  > (emphasis on [[formal software verification]])


* [[Jennifer Paykin]], *Linear/non-Linear Types For Embedded Domain-Specific Languages*, 2018 ([upenn:2752](https://repository.upenn.edu/edissertations/2752))


Application to [[verified programming]] after [[domain specific embedded programming language|embedding]] into [[Coq]]:

* {#RandPaykinZdancewic18} [[Robert Rand]], [[Jennifer Paykin]], [[Steve Zdancewic]], *QWIRE Practice: Formal Verification of Quantum Circuits in Coq*, EPTCS **266** (2018) 119-132 &lbrack;[arXiv:1803.00699](https://arxiv.org/abs/1803.00699)&rbrack;

* [[Robert Rand]], [[Jennifer Paykin]], Dong-Ho Lee, [[Steve Zdancewic]], *ReQWIRE: Reasoning about Reversible Quantum Circuits*, EPTCS **287** (2019) 299-312 &lbrack;[arXiv:1901.10118](https://arxiv.org/abs/1901.10118), [doi:10.4204/EPTCS.287.17](https://doi.org/10.4204/EPTCS.287.17)&rbrack;


Using [[domain specific embedded programming language|embedding]] into [[homotopy type theory]]:

* {#PaykinZdancewic19}[[Jennifer Paykin]], [[Steve Zdancewic]], *A HoTT Quantum Equational Theory*, [talk at QPL2019](http://qpl2019.org/a-hott-quantum-equational-theory/) &lbrack;[arXiv:1904.04371](https://arxiv.org/abs/1904.04371)&rbrack;

Fork development *SQIR*:

* [[Kesha Hietala]], [[Robert Rand]], [[Shih-Han Hung]], Xiaodi Wu, [[Michael Hicks]], *A verified optimizer for Quantum circuits*, Proceedings of the ACM on Programming Languages **5** Issue POPL 37 (2021) 1–29 &lbrack;[doi:10.1145/3434318](https://doi.org/10.1145/3434318)&rbrack;

* [[Kesha Hietala]], [[Robert Rand]], [[Shih-Han Hung]], Liyi Li, [[Michael Hicks]], *Proving Quantum Programs Correct*, in *12th International Conference on Interactive Theorem Proving (ITP 2021)*, Leibniz International Proceedings in Informatics (LIPIcs) **193** (2021) &lbrack;[arXiv:2010.01240](https://arxiv.org/abs/2010.01240)&rbrack;

* [[Kesha Hietala]], *A verified software toolchain for quantum programming* (2022) &lbrack;[pdf](https://khieta.github.io/files/drafts/khieta-dissertation.pdf), [blog](https://blog.sigplan.org/2021/06/02/verifying-a-quantum-compiler/)&rbrack;


category: people

[[!redirects SQIR]]


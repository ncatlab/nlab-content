

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

*QWIRE* ([Paykin, Rand & Zdancewic 17](#PaykinRandZdancewic17)) is a [[quantum programming language]] based on [[linear type theory]] combined with [[intuitionistic type theory]] via the [[exponential modality]]. More specifically, it is a [[domain specific programming language]] for [[quantum circuits]] meant to be [[domain specific embedded programming language|embedded]] into an [[intuitionistic type theory]]. As such it is similar to *[[Quipper]]*.


## References

The original article

* {#PaykinRandZdancewic17} [[Jennifer Paykin]], [[Robert Rand]], [[Steve Zdancewic]], *QWIRE: a core language for quantum circuits*, POPL 2017: Proceedings of the 44th ACM SIGPLAN Symposium on Principles of Programming LanguagesJanuary 2017 Pages 846–858 ([doi:10.1145/3009837.3009894](https://doi.org/10.1145/3009837.3009894))

Theoretical background:

* [[Robert Rand]], *Formally Verified Quantum Programming*, UPenn (2018) &lbrack;[ediss:3175](https://repository.upenn.edu/edissertations/3175)&rbrack;

  > (emphasis on [[formal software verification]])




* [[Jennifer Paykin]], *Linear/non-Linear Types For Embedded Domain-Specific Languages*, 2018 ([upenn:2752](https://repository.upenn.edu/edissertations/2752))

Application to [[verified programming]] after [[domain specific embedded programming language|embedding]] into [[Coq]]:

* {#RandPaykinZdancewic18} [[Robert Rand]], [[Jennifer Paykin]], [[Steve Zdancewic]], *QWIRE Practice: Formal Verification of Quantum Circuits in Coq*, EPTCS **266** (2018) 119-132 &lbrack;[arXiv:1803.00699](https://arxiv.org/abs/1803.00699)&rbrack;

Using [[domain specific embedded programming language|embedding]] into [[homotopy type theory]]:

* {#PaykinZdancewic19}[[Jennifer Paykin]], [[Steve Zdancewic]], *A HoTT Quantum Equational Theory*, [talk at QPL2019](http://qpl2019.org/a-hott-quantum-equational-theory/) &lbrack;[arXiv:1904.04371](https://arxiv.org/abs/1904.04371)&rbrack;

category: people


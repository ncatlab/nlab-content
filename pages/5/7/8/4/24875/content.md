

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

* [github.com/coq-quantum/CoqQ](https://github.com/coq-quantum/CoqQ)

*CoqQ* &lbrack;[Zhou et al. (2022)](#ZhouEtAl22)&rbrack; is the name of a [[domain specific programming language|domain specific]] [[quantum programming language]] which is [[domain specific embedded programming language|embedded]] in the (classical) [[proof assistant]] *[[Coq]]* and used for studying [[software verification]] of quantum programs (such as [[quantum circuits]] but also more generally).

CoqQ uses an analytic formalization of ([[finite dimensional vector space|finite dimensional]]) [[Hilbert spaces]] (from [Mahboubi & Tassi (2021)](Coq#MahboubiTassi21)) in order to formalize [[quantum gates]] as actual [[linear maps]] between these.


## Related languages

* [[Quipper]]

* [[QWIRE]]

* [[QBricks]]

## References

* {#ZhouEtAl22} [[Li Zhou]], [[Gilles Barthe]], Pierre-Yves Strub, Junyi Liu, [[Mingsheng Ying]], *CoqQ: Foundational Verification of Quantum Programs* &lbrack;[arXiv:2207.11350](https://arxiv.org/abs/2207.11350)&rbrack;


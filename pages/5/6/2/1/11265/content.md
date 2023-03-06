
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Idea

_Exact real computer arithmetic_ refers to treatment of [[real number]] [[arithmetic]] on [[computation|computers]] to finite (necessarily) but arbitrary precision. This is in contrast with what is called [[floating-point arithmetic]] which uses just one fixed finite approximation of the real numbers by [[natural numbers]]. 

Exact real computer arithmetic essentially implements what in mathematical [[computability theory]] is known as the [[Type Two Theory of Effectivity|type-II theory]] (in contrast to the "type-I" theory of [[partial recursive functions]] acting just on [[natural numbers]]). The formal mathematical definition of [[computable function (analysis)]] is the core topic of [[constructive analysis]]/[[exact analysis]].


## Related concepts

* [[topological domain theory]]


## References


For more see the references at *[[real number]]* and at *[[constructive analysis]]*.

* [[Chee-Keng Yap]], [[Thomas Dubé]], *The exact computation paradigm*,  in: *Computing in Euclidean Geometry*, Lecture Notes Series on Computing, World Scientific (1995) 452-492  &lbrack;[doi:10.1142/9789812831699_0011](https://doi.org/10.1142/9789812831699_0011), [[YapDube-ExactComputationParadigm.pdf:file]]&rbrack;

* [[Jean Vuillemin]], *Exact real computer arithmetic with continued fractions*, in *LFP '88: Proceedings of the 1988 ACM conference on LISP and functional programming* (1988) 14–27 &lbrack;[doi:10.1145/62678.62681](https://doi.org/10.1145/62678.62681)&rbrack;

* Peter Potts, Abbas Edalat, *Exact real computer arithmetic* (1997) &lbrack;[pdf](http://www.doc.ic.ac.uk/research/technicalreports/1997/DTR97-9.pdf), [[PottsEdalat-ExactRealComputerArithmetic.pdf:file]]&rbrack;

* Dave Plume (supervised by [[Martín Escardó]], [[Alex Simpson]]): *A Calculator for Exact Real Number Computation*, University of Edinburgh  (1998) &lbrack;[web](https://www.dcs.ed.ac.uk/home/mhe/plume/)&rbrack;

A collection of further references is listed at

* [Exact computation](https://web.archive.org/web/20150512035451/http://wwwhomes.doc.ic.ac.uk/~ae/exact-computation/)

Discussion relating to [[computability theory]], [[Type Two Theory of Effectivity]] and [[constructive analysis]]/[[computable analysis]] includes

* [[Herman Geuvers]], [[Milad Niqui]], [[Bas Spitters]], [[Freek Wiedijk]], _Constructive analysis, types and exact real numbers_, Mathematical Structures in Computer Science **17** 01 (2007) 3-36 &lbrack;[doi:10.1017/S0960129506005834](https://doi.org/10.1017/S0960129506005834)&rbrack;

* The Haskell Wiki, _[Exact real arithmetic](http://www.haskell.org/haskellwiki/Exact_real_arithmetic)_

Efficient exact representations of [[pi]] and related [[irrational numbers]] ([[Bailey-Borwein-Plouffe algorithm]])

* [[David Bailey]], [[Peter Borwein]], [[Simon Plouffe]]: *On the Rapid Computation of Various Polylogarithmic Constants*, Math. Comp. **66** (1997) 903-913 &lbrack;[doi:1997-66-218/S0025-5718-97-00856-9](https://www.ams.org/journals/mcom/1997-66-218/S0025-5718-97-00856-9), [pdf](https://www.davidhbailey.com/dhbpapers/digits.pdf)&rbrack;

further discussed in:

* [[Jerzy Karczmarczuk]], *Infinite precision real fractions, and lazy carry propagation* or: *The Most Unreliable Technique in the World to Compute $\pi$*, A Braga School (1998) &lbrack;[pdf](https://karczmarczuk.users.greyc.fr/arpap/lazypi.pdf), [[Karczmarczuk-Pi.pdf:file]]&rbrack;

* [[Simon Plouffe]], *On the computation of the $n^{th}$ decimal digit of various transcendental numbers* &lbrack;[arXiv:0912.0303](https://arxiv.org/abs/0912.0303)&rbrack;

* MathWorld, *[BBP-Type formula](https://mathworld.wolfram.com/BBP-TypeFormula.html)*    

Implementation of [[Cauchy real numbers]] (in [[Errett Bishop|Bishop]]-style [[constructive analysis]]) in [[Agda]]:

* [[Martin Lundfall]], *Formalizing real numbers in Agda* (2015) &lbrack;<a href="https://wcl.cs.rpi.edu/pilots/library/papers/TAGGED/4211-Lundfall%20(2015)%20-%20Formalizing%20Real%20Numbers%20in%20Agda.pdf">pdf</a>, [[Lundfall-RealNumbersInAgda.pdf:file]], [github](https://github.com/MrChico/Reals-in-agda)&rbrack;

* [[Zachary Murray]], *Constructive Analysis in the Agda Proof Assistant* &lbrack;[arXiv:2205.08354](https://arxiv.org/abs/2205.08354), [github](https://github.com/z-murray/honours-project-constructive-analysis-in-agda)&rbrack;

Coding of something like the [[HoTT book real numbers]] in [[Coq]]:

* [[Gaëtan Gilbert]], *Formalising Real Numbers in Homotopy Type Theory*, in *CPP 2017: Proceedings of the 6th ACM SIGPLAN Conference on Certified Programs and Proofs*  (2017) 112–124 &lbrack;[arXiv:1610.05072](https://arxiv.org/abs/1610.05072), [doi:10.1145/3018610.3018614](https://doi.org/10.1145/3018610.3018614)&rbrack;



[[!redirects exact real computer arithmetic]]
[[!redirects exact real arithmetic]]
[[!redirects exact arithmetic]]

[[!redirects Bailey-Borwein-Plouffe algorithm]]
[[!redirects BBP algorithm]]


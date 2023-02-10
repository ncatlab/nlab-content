
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea ##


In [[type theory]], _induction-induction_ is a principle for mutually defining [[types]] of the form

$$
  A \colon Type\,,\;\;\; and \;\;\; B \colon A \to Type
  \,,
$$ 

where both $A$ and $B$ are [[inductive types|defined inductively]], such that the constructors for $A$ can refer to $B$ and vice versa. In addition, the constructor for $B$ can refer to the constructor for $A$. 

Such induction-induction occurs for instance when formalising [[dependent type theory]] in [[type theory]].

## Results ##

Inductive-inductive types are related to [[inductive-recursive types]]. Importantly, inductive-inductive types have an initial algebra semantics with respect to [[dialgebras]]. In [Forsberg's thesis](#ForsbergThesis) inductive-inductive types are reduced to [[indexed inductive types]] in the setting of extensional type theory. This reduction however only provides "simple" elimination rules (not to be confused with _simply typed_). Indexed inductive types in turn can be reduced to [[W-types]] in extensional type theory. See [[inductive families]].

The consistency of the framework used for the elimination (e.g. in the [[theorem prover]] [[Agda]]) is not so clear, as it allows the definition of a universe containing a code for itself. There is an axiomatisation of the new principle in such a way that the resulting type theory is consistent, as proved by constructing a set-theoretic model; see [Forsberg-Setzer 10](#ForsbergSetzer10).

[Hugunin](#Hugunin19) provides a reduction of an inductive-inductive type to an inductive type. This construction is conjectured to generalize to all inductive-inductive types. The construction is done in [[cubical type theory]] and hence is consistent with [[homotopy type theory]].

## Higher inductive inductive types ##

Experiments with higher inductive inductive types (elaborate versions of [[higher inductive types]]) are sections 11.3 "Cauchy reals" and section 11.6 "Conway surreals"  of the [HoTT book](#HoTTBook) (cf. the *[[HoTT book real numbers]]*). As they are at the set level, these are instances of [[quotient inductive type|quotient inductive-inductive types]]; see [QIIT](#QIIT). An experimental syntax for HIITs by [Kaposi and Kovacs](#KaposiKovacs).

Another example of a higher inductive-inductive type is a [[univalent Tarski universe]], where the where a type $U$ is defined inductively together with a [[type family]] $a:U \vdash T(a) \; \mathrm{type}$ and has constructors 

* an element $h(a, b, f):\mathrm{fiber}(\mathrm{transport}^T(a, b), f)$ for all $a:U$, $b:U$, $f:T(a) \simeq T(b)$
* an identity $\mathrm{ua}(a, b, f, c):c =_{\mathrm{fiber}(\mathrm{transport}^T(a, b), f} h(a, b, f)$ for all $a:U$, $b:U$, $f:T(a) \simeq T(b)$ and $c:\mathrm{fiber}(\mathrm{transport}^T(a, b), f)$

where $\mathrm{transport}^T(a, b):(a =_U b) \to (T(a) \simeq T(b))$ is the [[transport]] function for all $a:U$ and $b:U$ and 
$$\mathrm{fiber}(\mathrm{transport}^T(a, b), f) \coloneqq \sum_{p:a =_U b} \mathrm{transport}^T(a, b)(p) =_{T(a) \simeq T(b)} f$$

This means that $h(a, b, f)$ is the [[center of contraction]] of the fiber of transport across $T$ at the equivalence $f:T(a) \simeq T(b)$. 

## References 

### Plain inductive-inductive types

* [[Andrej Bauer]], _[What is induction-induction?](http://cs.stackexchange.com/q/64139)_

* [[Fredrik Nordvall Forsberg]], [[Anton Setzer]], _A finite axiomatisation of inductive-inductive definitions_ [PDF](http://cs.swan.ac.uk/~csfnf/papers/indind_finite.pdf)

* {#ForsbergSetzer10} [[Fredrik Nordvall Forsberg]], [[Anton Setzer]], _Inductive-Inductive Definitions_, Computer Science Logic, Lecture Notes in Computer Science Volume 6247, 2010, pp 454-468 [Paper](http://link.springer.com/chapter/10.1007%2F978-3-642-15205-4_35).

* {#ForsbergThesis}[[Fredrik Nordvall Forsberg]], _Inductive-inductive definitions_, PhD thesis
Swansea University, 2013.  [PDF](http://cs.swan.ac.uk/~csfnf/thesis/thesis.pdf)

* {#cat} [[Thorsten Altenkirch]], Peter Morris, [[Fredrik Nordvall Forsberg]], [[Anton Setzer]],  _A Categorical Semantics for Inductive-Inductive Definitions_, CALCO, 2011 [link](https://link.springer.com/chapter/10.1007%2F978-3-642-22944-2_6)

* {#QIIT}  [[Thorsten Altenkirch]], [[Paolo Capriotti]], [[Gabe Dijkstra]], [[Fredrik Nordvall Forsberg]], _Quotient inductive-inductive types_ &lbrack;[arXiv:1612.02346](https://arxiv.org/abs/1612.02346)&rbrack;

* [[Marcelo P. Fiore]], [[Andrew M. Pitts]], [[S. C. Steenkamp]], *Quotients, inductive types, and quotient inductive types*, Logical Methods in Computer Science **18** 2 (2022) lmcs:7076  &lbrack;[arXiv:2101.02994](https://arxiv.org/abs/2101.02994), <a href="https://doi.org/10.46298/lmcs-18(2:15)2022">doi:10.46298/lmcs-18(2:15)2022</a>&rbrack;


### Higher inductive-inductive types:

For the example of constructing the [[real numbers]] (cf. *[[HoTT book real number]]*)

* {#HoTTBook} [[Univalent Foundations Project]], section 11 of: _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_ (2013)

Approaches to a general definition:

* {#KaposiKovacs} [[Ambrus Kaposi]], [[András Kovács]], *A Syntax for Higher Inductive-Inductive Types*, at *3rd International Conference on Formal Structures for Computation and Deduction (FSCD 2018)* (2018) 20:1-20:18 &lbrack;[pdf](http://drops.dagstuhl.de/opus/volltexte/2018/9190/), [doi:10.4230/LIPIcs.FSCD.2018.20](https://doi.org/10.4230/LIPIcs.FSCD.2018.20)&rbrack;

* [[Ambrus Kaposi]], [[András Kovács]], *Signatures and Induction Principles for Higher Inductive-Inductive Types*, Logical Methods in Computer Science **16** 1 (2020) lmcs:6100 &lbrack;[arXiv:1902.00297](https://arxiv.org/abs/1902.00297), <a href="https://doi.org/10.23638/LMCS-16(1:10)2020">doi:10.23638/LMCS-16(1:10)2020</a>&rbrack;

Discussion of examples in [[cubical type theory]] ([[cubical Agda]]):

* {#Hugunin19} [[Jasper Hugunin]], _Constructing Inductive-Inductive Types in Cubical Type Theory_, in *Foundations of Software Science and Computation Structures. FoSSaCS 2019*, Lecture Notes in Computer Science **11425** (2019) &lbrack;[doi:10.1007/978-3-030-17127-8_17](https://link.springer.com/chapter/10.1007/978-3-030-17127-8_17)&rbrack;


[[!redirects Inductive Inductive Type]]
[[!redirects induction-induction]]
[[!redirects inductive-inductive types]]

[[!redirects higher inductive-inductive type]]
[[!redirects higher inductive-inductive types]]



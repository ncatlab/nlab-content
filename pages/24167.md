
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{: toc}

## Overview

This is a stub collecting information on the [[proof theory|proof theoretic]] strength of [[univalent type theory]] with [[higher inductive types]].

Setzer computes the strength of MLTT+W. Voevodsky reduces Coq's inductive types to W-types. Coquand et al reduces univalence and some HITs to an unspecified constructive framework.

There is an [MO-question](http://mathoverflow.net/questions/69229/proof-strength-of-calculus-of-inductive-constructions) on the proof theoretic strength of pCIC. Avigad provide a general overview of the proof theory of predicative constructive systems.

## The strength of type theories

This section collects some references that establish the strength various type theories, roughly in increasing order of strength.

Let $\mathrm{ML}_n$ denote MLTT without inductive types and $n$ universes closed under $\Pi$ and $\Sigma$. This has the strength of the first-order system of $n$ iterated fixed points (whether with intuitionistic or classical logic), and thus by Feferman 1982 has proof-theoretic ordinal $\xi_n$, where $\xi_0=\varepsilon_0$ and $\xi_{n+1} = \varphi(\xi_n,0)$. 

## References

* {#Avigad} Jeremy Avigad, _Proof Theory_, 2014 [PDF](https://www.andrew.cmu.edu/user/avigad/Papers/formal_epistemology.pdf)

* {#Coquand} Thierry Coquand et al, _Variation on Cubical sets_, 2014 [PDF](http://www.cse.chalmers.se/~coquand/comp.pdf).

* {#Feferman} Solomon Feferman, _Iterated inductive fixed-point theories: application to Hancock's conjecture_, Stud. Logic Foundations Math., 109, 1982.

* {#Setzer} Anton Setzer, _Proof theoretical strength of Martin-Lof Type Theory with W-type and one universe_ [PDF](http://cs-svr1.swan.ac.uk/~csetzer/articles/weor0.pdf).

* {#Setzer2004} Anton Setzer, _Proof theory of Martin-L&ouml;f type theory. An overview_ [PDF](http://www.cs.swan.ac.uk/~csetzer/articles/overviewProofTheoryTypeTheory2004.pdf)

* {#Voevodsky} Vladimir Voevodsky, _Notes on type systems_ 2011 [PDF](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/expressions_current.pdf).



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _affinoid algebra_ is a local model for [[analytic spaces]] in [[analytic geometry]] ([[rigid analytic geometry]]). 

## Definition

Let $K$ be a [[complete normed field|complete]] [[non-archimedean valued field]]. 

As a [[ring]], a __standard affinoid algebra__ (or __Tate algebra__) $T_{n,K}$ is the subring of the ring of [[formal power series]] in $K[ [x_1, \ldots, x_n] ]$ consisting of all strictly [[convergence|converging]] series $ c= \sum_I c_I x^I$, that is such that $|c_I|\to 0$ as $I\to \infty$. 

There is a [[Gauss norm]] on such series $\|\sum_I c_I x^I \| = max\{|c_I|\}_I$. This is indeed a [[norm]] making $T_{n,K}$ into a Banach $K$-algebra of countable type. 

An __affinoid algebra__ is any [[Banach algebra]] which can be represented in a form (Tate algebra)/(closed ideal). 

The [[category]] of **$k$-[[affinoid spaces]]** is the [[opposite category]] of the category of $k$-affinoid algebras and bounded [[homomorphisms]] between them.


## Properties

A version of the [[Weierstrass preparation theorem]] in this context implies a version of the 
[[Hilbert basis theorem]]: $T_{n,K}$ is a [[noetherian ring]]. Moreover $T_{n,K}$ is a [[unique factorization domain]] of [[Krull dimension]] $n$. 


## References

Affinoid algebras were introduced in 

* [[John Tate]], (1961)

A standard textbook account is

* {#BoschGuntzerRemmert84} S. Bosch, U. G&#252;ntzer, [[Reinhold Remmert]], part B of  _[[Non-Archimedean Analysis]] -- A systematic approach to rigid analytic geometry_, 1984 ([pdf](http://math.arizona.edu/~cais/scans/BGR-Non_Archimedean_Analysis.pdf))


See the references at _[[analytic geometry]]_ for more details.

Discussion of affinoid algebras as a [[site]] for a more [[topos]]-theoretic formulation of of [[analytic geometry]] is in 

* {#BenBassatKremnitzer13} [[Oren Ben-Bassat]], [[Kobi Kremnizer]], section 7 of _Non-Archimedean analytic geometry as relative algebraic geometry_ ([arXiv:1312.0338](http://arxiv.org/abs/1312.0338))

See also 

* {#Bambozzi14} [[Federico Bambozzi]], _On a generalization of affinoid varieties_ ([arXiv:1401.5702](http://arxiv.org/abs/1401.5702))

[[!redirects affinoid algebras]]
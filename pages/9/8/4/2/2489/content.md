<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>

#Contents#

* automatic TOC goes here
{:toc}


#Idea#

The notion of _differential crossed module_ (or crossed module of/in Lie algebras) is a way to encode the structure of a [[strict Lie 2-algebra]] in terms of two ordinary [[Lie algebra]]s.


This is the [[infinitesimal object|infinitesimal]] version of how a smooth [[crossed module]] encodes a smooth [[strict 2-group]].


#Definition#

A **differential crossed module** $\mathfrak{g}$ is 

* a pair of [[Lie algebra]]s $\mathfrak{g}_2$ and $\mathfrak{g}_1$

* equipped with two Lie algebra homomorphisms

  * $\partial : \mathfrak{g}_2 \to \mathfrak{g}_1$

  * $ \rho : \mathfrak{g}_1 \to Der(\mathfrak{g}_2)$

* such that for all $x \in \mathfrak{g}_1, b,b' \in \mathfrak{g}_2$ we have

  * $\partial  ( \rho(x)(b) ) = [x, \partial(b)]$

  * $\rho(\partial b)(b') = [b, b']$.

#Remarks#

* The Lie algebra structure on $\mathfrak{g}_2$ is already fixed by the rest of the data. So a differential crossed module may equivalently be thought of as extra structure on a Lie module of $\mathfrak{g}_1$.

* Crossed modules are equivalent to strict [[L-infinity-algebra|Lie 2-algebras]]: those for which the ternary bracket vanishes.


#References#

* [[John Baez]], [[Alissa Crans]], _Lie 2-algebras_ ([arXiv](http://arxiv.org/abs/math/0307263))

The [[crossed modules]] (in groups or Lie groups) and the differential crossed modules are examples of the [[internal crossed module]]s. A good theory of them is developed in [[semiabelian categories]]. 

* G. Janelidze, _Internal crossed modules_, Georgian Math. J. 10 (2003) 99114 ([journal](http://www.heldermann.de/GMJ/GMJ10/GMJ101/gmj1008.htm)).

[[!redirects differential crossed modules]]
[[!redirects crossed module in Lie algebras]]
[[!redirects Lie algebra crossed module]]
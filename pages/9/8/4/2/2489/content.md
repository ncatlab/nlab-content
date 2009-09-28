
#Contents#

* automatic TOC goes here
{:toc}


#Idea#

A _differential crossed module_ is to an ordinary [[Lie algebra]] as a strict Lie [[2-group]] is to an ordinary [[Lie group]].

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

* Crossed modules are equivalent to strict [[L-infinity-algebra|Lie 2-algebras]]: those for which the trinary bracket vanishes.


#References#

* [[John Baez]], [[Alissa Crans]], _Lie 2-algebras_ ([arXiv](http://arxiv.org/abs/math/0307263))
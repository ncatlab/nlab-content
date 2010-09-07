
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

# Simple Lie algebras
* table of contents
{: toc}


## Definition

A __simple Lie algebra__ is a [[Lie algebra]] $\mathfrak{g}$ such that:

*  $\mathfrak{g}$ is not [[abelian Lie algebra|abelian]], and
*  the only [[proper ideal]] of $\mathfrak{g}$ is the zero ideal.

Equivalently, a simple Lie algebra is a [[simple object]] of [[LieAlg]] that *also* is nonabelian.  Note that there are only two abelian Lie algebras whose only proper ideal is the zero ideal: the [[trivial Lie algebra]] (which is not a simple object in $Lie Alg$ either, since the zero ideal is not proper either) and the [[line]] (which is a simple object in $Lie Alg$ but is still not considered a simple Lie algebra).


## Classification

Simple Lie algebras over an [[algebraically closed field]] of [[characteristic]] [[zero]], like many other things in [[mathematics]], may be classified by [[Dynkin diagram]]s.  We have:

* $\mathfrak{a}_n = \mathfrak{sl}_{n+1}$, the [[special linear Lie algebra]] of rank $n$.  We count this only for $n \geq 1$, since $\mathfrak{a}_0$ is the [[trivial Lie algebra]] (which is not simple but is still [[semisimple Lie algebra|semisimple]]).

* $\mathfrak{b}_n = \mathfrak{so}_{2n+1}$, the odd-dimensional [[special orthogonal Lie algebra]] of rank $n$.  We count this only for $n \geq 2$, since $\mathfrak{b}_n = \mathfrak{a}_n$ for $n \lt 2$.

* $\mathfrak{c}_n = \mathfrak{sp}_n$, the [[symplectic Lie algebra]] of rank $n$.  We count this only for $n \geq 3$, since $\mathfrak{c}_n = \mathfrak{b}_n$ for $n \lt 3$.

* $\mathfrak{d}_n = \mathfrak{so}_{2n}$, the even-dimensional [[special orthogonal Lie algebra]] of rank $n$.  We count this only for $n \geq 4$, since $\mathfrak{d}_n = \mathfrak{a}_n$ for $n \lt 2$ and $n = 3$, while $\mathfrak{d}_2 = \mathfrak{a}_2 \oplus \mathfrak{a}_2$ (which is not simple but is still [[semisimple Lie algebra|semisimple]]).

* $\mathfrak{e}_n$, an [[exceptional Lie algebra]] that only exists for rank $n \lt 9$.  We count this only for $n \geq 6$ (thus for $n = 6, 7, 8$ in all), since $\mathfrak{e}_5 = \mathfrak{d}_5$, $\mathfrak{e}_4 = \mathfrak{a}_4$, $\mathfrak{e}_n = \mathfrak{a}_{n-1} \oplus \mathfrak{a}_1$ (which is not simple but is still [[semisimple Lie algebra|semisimple]]) for $2 \leq n \lt 4$, and $\mathfrak{e}_n = \mathfrak{a}_n$ for $n \lt 2$.

* the [[exceptional Lie algebra]]s $\mathfrak{f}_4$ and $\mathfrak{g}_2$, which exist only for those ranks.

If you want to classify simple objects in $Lie Alg$, then there is one other possibility: the [[line]] (which has no corresponding Dynkin diagram).

It is much more difficult to classify simple Lie algebras over non-closed fields, over fields with positive characteristic, and especially over non-fields.


## Semisimple Lie algebras

A __[[semisimple Lie algebra]]__ is a [[direct sum]] of simple Lie algebras.  In particular, every simple Lie algebra is semisimple, but there are many more.


## Simple Lie groups

A [[Lie group]] is a [[simple Lie group]] if the Lie algebra corresponding to it under [[Lie integration]] is simple.


[[!redirects simple Lie algebra]]
[[!redirects simple Lie algebras]]

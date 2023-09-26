
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


# Modifications
* table of contents
{: toc}

## Idea

A [[transfor]] between [[pseudonatural transformation|pseudo]]/[[lax natural transformations]] is sometimes called a _modification_. Hence modifications are the [[3-morphisms]] in a [[3-category]] [[2Cat]] of [[2-categories]] and [[2-functors]] between them.

Just as a [[natural transformation]] between [[functor]]s is a
collection of $1$-cells indexed by $0$-cells, a _modification_ between
transformations is an indexed collection of 2-cells.


## Definitions

To be most general, start with [[lax natural transformation|lax transformations]]
$\alpha, \beta : F \dot{\to} G : C \to D$. Given those, a modification
$m : \alpha \ddot{\to} \beta$ assigns to each $0$-cell $A\in
C$ a $2$-cell $m_A : \alpha_A \Rightarrow \beta_A$ in $D$
that commutes suitably with the $2$-cell components of
$\alpha$ and $\beta$ (see Leinster for details).

If $\alpha,\beta$ are strict transformations, then the
complicated-looking modification condition becomes simply
a naturality square with globs $m_A : \alpha_A \Rightarrow
\beta_A$ where the $1$-cells $\alpha_A$ would normally be.


## Generalisation

When you get tired of thinking individually about $n$-categories, functors, transformations, modifications, and so on, check out [[(n,k)-transformation]].

(Some discussion from here has also been moved to there.)

## Related concepts

* [[2-functor 2-category]]


## References

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], Section 4.4 of: *2-Dimensional Categories*, Oxford University Press 2021 &lbrack;[arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378)&rbrack;


* [[Tom Leinster]], _Basic bicategories_ &lbrack;[arXiv:math/9810017](http://arxiv.org/abs/math/9810017)&rbrack;


[[!redirects modification]]
[[!redirects modifications]]

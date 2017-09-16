Just as a [[natural transformation]] between [[functor]]s is a
collection of $1$-cells indexed by $0$-cells, a _modification_ between
transformations is an indexed collection of 2-cells.


## Definitions ##

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

When you get tired of thinking individually about $n$-categories, functors, transformations, modifications, and so on, check out [[(n,j)-transformation]].

(Some discussion from here has also been moved to there.)


## References ##

Leinster, _Basic bicategories_,
[arXiv](http://arxiv.org/abs/math/9810017).

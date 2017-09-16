Just as a natural transformation between functors is an
indexed collection of 1-cells, a modification between
transformations is an indexed collection of 2-cells.

## Definition ##

Given [[lax natural transformation|lax transformations]]
$\alpha, \beta : F \dot{\to} G : C \to D$, a modification
$m : \alpha \ddot{\to} \beta$ assigns to each object $A\in
C$ a 2-cell $m_A : \alpha_A \Rightarrow \beta_A$ in $D$
that commutes suitably with the 2-cell components of
$\alpha$ and $\beta$ (see Leinster).

If $\alpha,\beta$ are strict natural, then the
complicated-looking modification condition becomes simply
a naturality square with globs $m_A : \alpha_A \Rightarrow
\beta_A$ where the 1-cells $\alpha_A$ would normally be.


## Discussion ##

+-- {: .query}

[[Finn Lawler|Finn]]: There is a pattern here: functions
are indexed collections of objects, natural
transformations are i.c.s of 1-cells, modifications i.c.s
of 2-cells; and these are what make the collection of all
$n$-categories into an $n+1$-category, for $0 \leq n \leq
2$ anyway.  Any references for the pattern in higher
dimensions?

=--

## References ##

Leinster, _Basic bicategories_,
[arXiv](http://arxiv.org/abs/math/9810017).

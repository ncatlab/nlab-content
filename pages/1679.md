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


## Discussion ##

+-- {: .query}

[[Finn Lawler|Finn]]: There is a pattern here: functors
are indexed collections of objects, natural
transformations are i.c.s of 1-cells, modifications i.c.s
of 2-cells; and these are what make the collection of all
$n$-categories into an $n+1$-category, for $0 \leq n \leq
2$ anyway.  Any references for the pattern in higher
dimensions?

_Toby_:  Do you mean for the terminology or for the appropriate coherence laws? (the details that you\'ve been leaving out).  Not that I have either ...

Incidentally, I corrected 'function' to 'functor' in you question above; I hope that\'s OK.

=--

## References ##

Leinster, _Basic bicategories_,
[arXiv](http://arxiv.org/abs/math/9810017).

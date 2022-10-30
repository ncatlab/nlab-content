##Idea##

A [[subcategory]] $S$ of category $C$ is _dense_ if every object $c$ of $C$ is a [[colimit]] of a diagram of objects in $S$, in a canonical way. 

##Definition##

A functor $i:S\to C$ is __dense__ if it satisfies the following equivalent conditions.

1. every object $c$ of $C$ is the vertex of the following colimit over the [[comma category]] $(i/c)$:
   $$
   \mathrm{colim}((i/c)\stackrel{\mathrm{pr}_S}{\longrightarrow} S \stackrel{i}{\to} C)
   $$

1. every object $c$ of $C$ is the $C(i-,c)$-weighted colimit of $i$.  This version generalizes more readily to the [[enriched category|enriched]] context.

1. the corresponding [[nerve|nerve functor]] (or "restricted [[Yoneda embedding]]") $C \to [S^{op},Set]$ is [[full and faithful functor|fully faithful]]. 


##Terminology and History##
 
Dense functors were defined in [MR0175954](#MR0175954) under the name *left adequate* (the name was actually applied to the subcategory).  The dual notion of *right adequate* was also introduced and subcategories satisfying both were called *adequate*.  It was also shown that while the relation of being left (or right) adequate is not transitive, being adequate is transitive.


Also, in arXiv v4 of [[Higher Topos Theory|HTT]] this notion (for [[(∞,1)-categories]]) is referred to as *strongly generating*, but that term actually means [[strong generator|something different]].

## Examples

1. Let $V$ be a category of [[algebras]] and $n \in \mathbb{N}$ such that $V$ has a presentation with operations of at most arity $n$.  Let $v$ be the free $V$-algebra on $n$ generators.  Then the full subcategory with object $v$ is dense in $V$.

1. In $\Set$, a singleton space is dense.

##Warning##

There is a different notion of a dense subcategory, often used in [[shape theory]], which has a bit of the same spirit. A [[full subcategory]] $D\subset C$ is
__dense__ in this second sense, if every object in $C$ admits a $D$-expansion. 

A _$D$-expansion_ of an object $X$ in $C$ is a morphism
$X\to \mathbf{X}$ in $\mathrm{pro}C$ such that $\mathbf{X}$
is in $\mathrm{pro}D$ and $X$ is the rudimentary system (constant inverse system) corresponding to $X$; moreover one asks that the morphism is universal among all such morphisms $X\to\mathbf{Y}$. 

Given a dense subcategory $D\subset C$ one defines
an abstract shape category $\mathrm{Sh}(C,D)$ which has the same objects as $C$, but the morphisms are the equivalence classes of morphisms in $\mathrm{pro}D$ of $D$-expansions.


## References

* {: #MR0175954 } Isbell, J. R. (1960). Adequate subcategories. _Illinois J. Math._, _4_, 541&#8211;552. [MR0175954](http://www.ams.org/mathscinet-getitem?mr=0175954)

[[!redirects adequate subcategory]]
[[!redirects left adequate subcategory]]
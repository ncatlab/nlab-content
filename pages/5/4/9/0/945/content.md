##Idea##

A [[subcategory]] $S$ of category $C$ is _dense_ if every object $c$ of $C$ is a [[colimit]] of a diagram of objects in $S$, in a canonical way. 

##Definition##

A functor $i:S\to C$ is __dense__ if every object $C$ is the 
vertex of the following colimit over the [[comma category]] $(i/c)$:
$$
\mathrm{colim}((i/c)\stackrel{\mathrm{pr}_S}{\longrightarrow} S \stackrel{i}{\to} C)
$$
Equivalently, $i$ is dense if every object $C$ is the $C(i-,c)$-weighted colimit of $i$.  This version generalizes more readily to the [[enriched category|enriched]] context.


##Characterization##
 
A functor is dense iff it is (left) adequate in the sense of Isbell i.e. if the corresponding [[nerve|nerve functor]] $C \to [S^{op},Set]$ is [[full and faithful functor|fully faithful]]. 


##Warning##

There is a different notion of a dense subcategory, often used in [[shape theory]], which has a bit of the same spirit. A [[full subcategory]] $D\subset C$ is
__dense__ in this second sense, if every object in $C$ admits a $D$-expansion. 

A _$D$-expansion_ of an object $X$ in $C$ is a morphism
$X\to \mathbf{X}$ in $\mathrm{pro}C$ such that $\mathbf{X}$
is in $\mathrm{pro}D$ and $X$ is the rudimentary system (constant inverse system) corresponding to $X$; moreover one asks that the morphism is universal among all such morphisms $X\to\mathbf{Y}$. 

Given a dense subcategory $D\subset C$ one defines
an abstract shape category $\mathrm{Sh}(C,D)$ which has the same objects as $C$, but the morphisms are the equivalence classes of morphisms in $\mathrm{pro}D$ of $D$-expansions.

+--{: .query}
[[Mike Shulman|Mike]]: Would it be possible to have one page about dense subcategories in the canonical-colimit sense, and a different page about dense subcategories in the shape-theory sense, which only refer to each other briefly as a different meaning of the word?  If one never talks about a dense functor in shape theory, then maybe all the shape-theoretic stuff could be on the page [[dense subcategory]] and the canonical-colimit stuff on this page.  Or we could be like Wikipedia and have [[dense subcategory (shape theory)]] and, uh, the other one.

_Toby_:  What about [[adequate subcategory]]?  Or is that outdated?
=--

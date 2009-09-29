The _disjoint union_ is a [[coproduct]] in [[Set]], the category of [[sets]].


# Definition #

Given any family $(A_i)_{i:I}$ of sets, the (external) __disjoint union__ $\biguplus_i A_i$ (also written $\sum_i A_i$, $\coprod_i A_i$, etc) of the family is the set of all (ordered) pairs $(i,a)$ with $i$ in the index set $I$ and $a$ in $A_i$.

As stated, the second element of such a pair depends on the first element, which is natural in dependent type theory and certainly feasible in material set theory; but if you don't like this, then define $\biguplus_i A_i$ to be the set of those elements $x$ of the [[cartesian product]] $\prod_i \mathcal{P}A_i$ of the [[power sets]] such that there is exactly one index $j$ such that $x_j$ is [[inhabited set|inhabited]] and that $x_j$ is a [[singleton]].  If you\'re trying to be [[predicative mathematics|predicative]] too, consider adopting the existence of disjoint unions as an axiom in your [[foundations]].

There is a natural [[injection]] $A_j \to \biguplus_i A_i$ (mapping $a$ to $(j,a)$) for each index $j$, and its common to treat $A_j$ as a [[subset]] of $\biguplus_i A_i$.  So if no confusion can result (in particular, when the notation for an elements of $A_j$ always makes the ambient set clear), one often suppresses the index in the notation for an element of the disjoint union.


# Special cases #

Given sets $A$ and $B$, the disjoint union of the binary family $(A,B)$ is written $A \uplus B$ (also $A + B$, $A \amalg B$, etc); its elements may be written (if care is needed) as $(0,a)$ and $(1,b)$, $(1,a)$ and $(2,b)$, $\iota{a}$ and $\kappa{b}$, and in many other styles.

Given sets $A_1$ through $A_n$, the disjoint union of the $n$-ary family $(A_1,\ldots,A_n)$ is written $\biguplus_{i=1}^n A_i$ (or similarly); its elements may be written (if care is needed) as $(i,a)$ for $1 \leq i \leq n$ and $a \in A_i$.

Given sets $A_1$, $A_2$, etc, the disjoint union of the countably infinitary family $(A_1,A_2,\ldots)$ is written $\biguplus_{i=1}^\infty A_i$ (or similarly); its elements may be written (if care is needed) as $(i,a)$ for $i$ a natural number and $a \in A_i$.

Given a set $A$, the disjoint union of the unary family $(A)$ may be identified with $A$ itself; that is, we identify $(i,a)$ for the unique index $i$ with $a$.

The disjoint union of the empty family $()$ is [[empty set|empty]]; it has no elements.


# Internal version #

(This is internal in the sense of 'internal direct sum', not [[internalization]].  For that, just see [[coproduct]].)

If a family $(A_i)_{i: I}$ of [[subsets]] of a given set $X$ are all pairwise disjoint (that is, $A_i \cap A_j$ has an element only if $i = j$, for any indices $i$ and $j$), then the [[union]] $\bigcup_i A_i$ is [[natural isomorphism|naturally bijective]] with the (external) disjoint union defined above.  Conversely, given an external disjoint union $\biguplus_i A_i$, each $A_j$ may be identified with a subset of $\biguplus_i A_i$ (as explained above); these subsets are all pairwise disjoint, and their union is the entire disjoint union.

Accordingly, a union of pairwise disjoint subsets may be called an __internal disjoint union__.  (Compare the internal vs external notions of [[direct sum]].)


category: foundation axiom

[[!redirects disjoint unions]]
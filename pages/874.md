The _cartesian product_ is a [[product]] in [[Set]], the category of [[set]]s.

# Definition #

Given any family $(A_i)_{i:I}$ of sets, the __cartesian product__ $\prod_i A_i$ of the family is the set of all [[function]]s $f$ from the index set $I$ with $f_j$ in $A_j$ for each $j$ in $I$.

As stated, the [[target]] of such a function depends on the argument, which is natural in dependent type theory; but if you don't like this, then define $\prod_i A_i$ to be the set of those functions $f$ from $I$ to the [[disjoint union]] $\biguplus_i A_i$ such that $f_j \in A_j$ (treating $A_j$ as a [[subset]] of $\biguplus_i A_i$ as usual) for each $j$ in $I$.

In traditional forms of [[set theory]], one can also take the target of $f$ to be the [[union]] $\bigcup_i A_i$ or even the class of all objects (equivalently, leave it unspecified).

# Special cases #

Given sets $A$ and $B$, the cartesian product of the binary family $(A,B)$ is written $A \times B$; its elements $(a,b)$ are called __ordered pairs__.  (In [[set theory]], one often makes a special definition for this case, defining
$$ (a,b) = \{\{a\},\{a,b\}\} $$
rather than as a function so that ordered pairs can then be used in the definition of function.  From a structural perspective, however, this is unnecessary.)

Given sets $A_1$ through $A_n$, the cartesian product of the $n$-ary family $(A_1,\ldots,A_n)$ is written $\prod_{i=1}^n A_i$; its elements $(a_1,\ldots,a_n)$ are called __ordered $n$-tuples__.

Given sets $A_1$, $A_2$, etc, the cartesian product of the countably infinitary family $(A_1,A_2,\ldots)$ is written $\prod_{i=1}^\infty A_i$; its elements $(a_1,a_2,\ldots,)$ are called __infinite [[sequence]]s__.

Given a set $A$, the cartesian product of the unary family $(A)$ may be identified with $A$ itself; that is, we identify the __ordered singleton__ $(a)$ with $a$.

The cartesian product of the empty family $()$ is the [[point]], a set whose only element is the __empty tuple__ $()$; we often call this set $1$ (or $\pt$, when we\'re Urs) and write its element as $*$.
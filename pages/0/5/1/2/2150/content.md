Let $X$ be a [[paracompact space|paracompact]] [[Hausdorff space]]. A [[sheaf]] $F$ of [[groups]] over $X$ is __fine__ if for every two disjoint closed subsets $A,B\subset X$, $A\cap B = \emptyset$, there is an [[endomorphism]] of the sheaf of groups $F\to F$ which restricts to the identity in a neighborhood of $A$ and to the $0$ endomorphism in a neighborhood of $B$. Every fine sheaf is [[soft sheaf|soft]].

+-- {: .query}
Changed $A \cap B \neq \emptyset$ to $A \cap B = \emptyset$. Unless I am very confused, this is the right definition! David Speyer
=--

+-- {: .query}
David Speyer asks: Voisin, in _Hodge Theory and Complex Alegbraic Geometry I_, definition 4.35 makes a different definition of fine sheaf. I can see that they are related, but I can't see precisely what the relation is. 

According to Voisin:

:A fine sheaf $\mathcal{F}$ over $X$ is a sheaf of $\mathcal{A}$-modules, where $\mathcal{A}$ is a sheaf of rings such that, for every open cover $U_i$ of $X$, there is a partition of unity $1 = \sum f_i$ (where the sum is locally finite) subordinate to this covering.

A technical point: I infer from context that, for Voisin, being subordinate to $U_i$ means that, for each $U_i$, there is an open set $V_i$ such that $X = U_i \cup V_i$ and $f|_{V_i}=0$. This is slightly stronger than requiring that $f|_{X \setminus U_i} =0$. When working on a regular (T3) space, I believe that, if partitions of unity exist in the weaker sense, than they also exist in the stronger sense.
=--
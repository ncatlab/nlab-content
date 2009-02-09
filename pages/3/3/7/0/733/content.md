A **directed set** is a [[poset]] (or more generally [[preorder|proset]]) in which any (finite) set of elements has a common upper bound.

# Definitions

To be explicit, a **finitely directed set** (which is the default notion) is equipped with a [[preorder]] $\leq$ such that:
* there exists an element (so the set is [[inhabited set|inhabited]]); and
* given elements $x, y$, there exists an element $z$ such that $x \leq z$ and $y \leq z$.

It follows that, given any finite set $x_1, \dots, x_n$ of elements, there exists an element $z$ such that $x_i \leq z$ for all $i$. (For [[constructivism|constructive]] purposes, one should interpret 'finite set' above as a [[finite set|finitely indexed set]], as shown.)

More generally, if $\kappa$ is a [[cardinal number]], then a **$\kappa$-directed set** is equipped with a preorder $\leq$ such that, given any index set $A$ with $|A| \lt \kappa$ and function $i \mapsto x_i$ from $A$, there exists an element $z$ such that $x_i \leq z$ for all $i$. Then a finitely directed set is the same as an $\aleph_0$-directed set.  An **infinitely directed set** allows any index set $A$ whatsoever, but this reduces to the statement that the proset has a [[top]] element.

# Remarks

A preorder that makes a set into a directed set is called a **direction** on that set, especially when one considers many different directions on the same set.  Directions on the real line are quite interesting; there\'s a textbook that does ordinary calculus from scratch using directions, and there\'s a paper generalising interval arithmetic to arithmetic on directions.

As a proset is a special kind of [[category]], so a (finitely) directed set is a proset in which all finite diagrams admit a cocone.  If the proset actually has finite coproducts (equivalently, all finite colimits), then it is a [[join]]-semi[[lattice]].  (In particular, every join-semilattice is a directed set.)

Directed sets are heavily used in point-set topology and analysis, where they serve as index sets for [[net|nets]] (aka Moore&#8211;Smith sequences).  There it is important that $\le$ be allowed to be a preorder, not necessarily a partial order, since a net need not preserve $\leq$ in any way but by default is still assumed to preserve $=$.

Colimits over directed index sets also play an important role in the theory of [[locally presentable category|locally presentable]] and [[accessible category|accessible]] categories; see also [[filtered category]].

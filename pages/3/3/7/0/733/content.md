A **directed set** is a [[poset]] in which any (finite) set of elements has a common upper bound.

# Definitions

To be explicit, a **finitely directed set** (which is the default notion) is equipped with a partial order $\leq$ such that:
* there exists an element (so the set is [[inhabited set|inhabited]]); and
* given elements $x, y$, there exists an element $z$ such that $x \leq z$ and $y \leq z$.

It follows that, given any [[finite set]] $x_1, \dots, x_n$ of elements, there exists an element $z$ such that $x_i \leq z$ for all $i$. (For [[constructivism|constructive]] purposes, one should interpret 'finite set' above as a finitely indexed set.)

More generally, if $\kappa$ is a [[cardinal number]], then a **$\kappa$-directed set** is equipped with a partial order $\leq$ such that, given any index set $A$ with $|A| \lt \kappa$ and function $i \mapsto x_i$ from $A$, there exists an element $z$ such that $x_i \leq z$ for all $i$. Then a finitely directed set is the same as an $\aleph_0$-directed set.  An **infinitely directed set** allows any index set $A$ whatsoever.

# Remarks

As a poset is a special kind of [[category]], so a directed set is a poset which has all (finite) [[weak colimit|weak]] [[coproduct]]s (hence all finite weak [[colimit]]s).  If the poset actually has coproducts (not merely weak ones), then it is a [[join]]-semi[[lattice]].  (In particular, every join-semilattice is a directed set.)

Directed sets are heavily used in point-set topology and analysis, where they serve as index sets for nets (aka Moore&#8211;Smith sequences).

A partial order that makes a set into a directed set is called a **direction** on that set, especially when one considers many different directions on the same set.  Directions on the real line are quite interesting; there\'s a textbook that does ordinary calculus from scratch using directions, and there\'s a paper generalising interval arithmetic to arithmetic on directions.

# Discussion

To be honest, I\'ve never seen anything but finitely directed sets in the literature, but the general concept is quite natural, don\'t you think? &#8212;[[Toby Bartels|Toby]]
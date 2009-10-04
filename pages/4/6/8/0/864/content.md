A **quasiorder** on a set $S$ is a (binary) [[relation]] $\lt$ on $S$ that is both [[irreflexive relation|irreflexive]] and [[transitive relation|transitive]].  That is:
* $x \nless x$ always;
* If $x \lt y \lt z$, then $x \lt z$.

A **quasiordered set**, or **quoset**, is a [[set]] equipped with a quasiorder.

Unlike with other notions of [[order]], a set equipped with a quasiorder cannot be [[constructive mathematics|constructively]] understood as a kind of [[enriched category]] (at least, not as far as I know ...).  Using [[excluded middle]], however, a quasiorder is the same as a [[partial order]]; interpret $x \leq y$ literally to mean that $x \lt y$ or $x = y$, while $x \lt y$ conversely means that $x \leq y$ but $x \ne y$.

Accordingly, quasiorders in general should usually be replaced by partial orders when generalising mathematics to other categories.  However, if a quasiorder satisfies comparison (if $x \lt z$, then $x \lt y$ or $y \lt z$), then it is a [[linear order]] (at least on some [[quotient set]]), which is an important concept.


[[!redirects quasi-order]]
[[!redirects quasiordered set]]
[[!redirects quasi-ordered set]]
[[!redirects quoset]]
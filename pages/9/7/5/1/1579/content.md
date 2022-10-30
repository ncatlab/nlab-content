[[!redirects prometric]]

# Definition

A **prometric** on a set $X$ is a family $G$ of functions $d:X\times X\to [0,\infty)$ such that

1. $G$ is a $\ge$-[[filter]], i.e.

    1. there exists an element $d\in G$,
    1. if $d_1,d_2\in G$ there is a $d_3\in G$ with $d_3\ge d_1$ and $d_3\ge d_2$ pointwise, and
    1. if $d_1\in G$ and $d_2\le d_1$ pointwise, then $d_2\in G$.

1. For every $d\in G$ and $x\in X$, we have $d(x,x)=0$.

1. For any $d\in G$ there exists an $e\in G$ such that for all $x,y,z\in X$ we have
   $$d(x,z) \le e(x,y)+e(y,z).$$

1. For every $d\in G$, there is an $e\in G$ with $d(x,y)\le e(y,x)$ for all $x,y\in X$.

If we drop the final condition, we obtain a **quasi-prometric**.  We can also consider **extended** prometrics in which the $d$ can take the value $\infty$.

A **base** for a prometric is a collection satisfying all these axioms except $\le$-closure; the $\le$-closure of a prometric base is a prometric.  Any single [[pseudometric]], and in fact any [[gauge space|gauge]], constitutes a base for a prometric.

Of course a **prometric space** is a space equipped with a prometric, and likewise for a **quasi-prometric space**.


# Morphisms

A **short map** between prometric spaces $X$ and $Y$ is a function $f:X\to Y$ such that for every $d\in G_Y$, we have $d\circ (f\times f) \in G_X$.  We write $ProMet$ for the category of prometric spaces and short maps.

If the prometrics of $X$ and $Y$ are presented by bases, then this is equivalent to saying that for any basic $d$ on $Y$, there is a basic $e$ on $X$ such that $d(f(x),f(x'))\le e(x,x')$ for all $x,x'\in X$.  Thus, for metric spaces and gauge spaces considered as prometric spaces, this reduces to the usual notion of short map (i.e. distance-decreasing map).  Hence the category $Gau$ of gauge spaces and short maps is included as a full subcategory of $ProMet$.

+--{: .query}
_Toby asked at [[latest changes]]_: But do you have any good example of a nongaugeable prometric space?

[[Mike Shulman|Mike]]: No.
=--


# Categorical interpretation

As observed by Lawvere, an (extended quasi pseudo) metric space is a category enriched over $([0,\infty],\ge,+,0)$.  In other words, it is a monoid (or monad) in the [[bicategory]] $[0,\infty] Mat$ of matrices with values in this monoidal category.  Analogously, an (extended quasi) prometric space is a monoid in the bicategory $Pro [0,\infty] Mat$ whose hom-categories are the categories of [[pro-object]]s in the hom-categories of $[0,\infty] Mat$.

Note that if $Rel = \{0,1\} Mat$ denotes the bicategory of [[relation]]s in $Set$, then a monoid in $Rel$ is a [[preorder]], while a monoid in $ProSet$ is a (quasi) [[uniform space]].

In all these cases, in order to recover the correct notion of morphism abstractly, we must consider monoids in a [[double category]] or [[equipment]] rather than merely a bicategory.


# References

* Maria Manuel Clementino, Dirk Hofmann, and Walter Tholen.  "One Setting for All: Metric, Topology, Uniformity, Approach Structure."

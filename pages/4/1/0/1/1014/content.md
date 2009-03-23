A **pure set** is a collection of pure sets, nothing more.

This is a circular definition; if you interpret it [[recursion|recursively]], then you get **well-founded sets**; if you interpret it [[corecursion|corecursively]], then you allow for **non-well-founded sets**.  (But not that the corecursive interpretation includes the well-founded sets as well, an example of the [[red herring principle]].)

At first, the only well-founded set possible is the [[empty set]] $\empty = \{ \}$, the collection of no pure sets.  Once you have that, you can form $\star = \{\empty\}$, then $\{\star\}$ and $\{\empty,\star\}$, and so on.  These are the [[hereditarily finite set]]s; using an axiom of infinity, one can jump to a set of all hereditarily finite sets (one model for the set $\mathbf{N}$ of [[natural number]]s, although not the usual model) and continue from there.

For non-well-founded sets, there are additional possibilities, such as a set $\star$ such that $\star = \{\star\}$ (the [[point]]), or sets $A$ and $B$ such that $A = \{B\}$ and $B = \{A\}$.  These may be ruled out by an appropriate _axiom of foundation_.

# Formalisation

In membership-based [[set theory|set theories]] (such as the Zermelo axioms and variations), one usually assumes that everything is a pure set.  Fraenkel\'s axiom of foundation assures that only well-founded sets are included.
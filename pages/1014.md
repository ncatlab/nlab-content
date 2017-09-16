A **pure set** is a [[set]] of pure sets.

This is a circular definition; if you interpret it [[recursion|recursively]], then you get **well-founded sets**; if you interpret it [[corecursion|corecursively]], then you allow for **ill-founded sets**.  (But note that the corecursive interpretation includes the well-founded sets as well, an example of the [[red herring principle]].)

At first, the only well-founded set possible is the [[empty set]] $\empty = \{ \}$, the set of no pure sets.  Once you have that, you can form $\star = \{\empty\}$, then $\{\star\}$ and $\{\empty,\star\}$, and so on.  These are the [[hereditarily finite set]]s; using an axiom of infinity, you can jump to the set of all hereditarily finite sets (one model for the set $\mathbf{N}$ of [[natural number]]s, although not the usual model) and continue from there.

+--{.query}
Mike, why don\'t you accept the hereditarily finite sets as a model for $\mathbf{N}$?  There are countably infinitely many, so as a mathematical statement, it\'s certainly true.  And the hereditarily finite sets are rather nicely enumerated (beginning as above): set $i$ belongs to set $n$ iff the $i$th base-$2$ digit of $n$ is $1$.  ---Toby

[[Mike Shulman|Mike]]: Yes, it's certainly _true_, but it didn't seem particularly helpful to me to mention it here.  But if you want mention it, please include a description of that enumeration as well, so that no one is tempted to confuse $V_\omega$ with $\omega$.
=--

For ill-founded sets, there are additional possibilities, such as a set $\bullet$ such that $\bullet = \{\bullet\}$ (a suggestive model for the [[point]]), or sets $A$ and $B$ such that $A = \{B\}$ and $B = \{\empty, A\}$.  These may be ruled out by an appropriate _axiom of foundation_.

# Formalisation

In material [[set theory|set theories]] (such as ZFC and its variations), one usually assumes that everything is a pure set (although ur-elements are also sometimes used).  The late addition (1930) of Zermelo\'s axiom of foundation assures that only well-founded sets are included.

In a structural set theory like [[ETCS]], we model pure sets by their membership trees.
+--{.query}
If I learnt SVG, I could draw some pictures.  (Or I could draw them in XyPic and upload them.)  ---Toby
=--
The basic idea is that the set of well-founded sets is the [[initial algebra]] of the covariant [[power set]] functor, while the set of ill-founded sets is the [[final coalgebra]] of the same functor.  Of course, neither of these algebras exists (since this would violate [[Cantor's theorem]]), but we can still describe what their elements would be like (and in fact define them as [[discrete category|discrete]] [[large category|large categories]]).
The __specialisation order__ is a way of turning any [[topological space]] $X$ into a [[preorder]]ed set (with the same underlying set).

Let $x \leq y$ if and only if $x$ belongs to the closure of $\{y\}$.  One may also use the opposite convention.

# Properties

$X$ is $T_0$ if and only if its specialisation order is a [[partial order]].  $X$ is $T_1$ iff its specialisation order is [[equality]].  $X$ is $R_1$ (like $T_1$ but without $T_0$) iff its specialisation order is an [[equivalence relation]].

Given a continuous function $f: X \to Y$ between topological spaces, it is order-preserving relative to the specialisation order.  Thus, we have a [[faithful functor]] from teh category of $\Top$ of topological spaces to the category $\Pros$ of preordered sets.

If we restrict to a [[finite set|finite]] underlying set, then the categories $\Fin\Pros$ and $\Fin\Top$ of finite prosets and finite topological spaces are [[equivalence of categories|equivalent]] in this way.  The corresponding topology can be recovered from a finite proset through its [[specialization topology]].

+--{.query}
There\'s an adjunction here; I should think about which way it goes and whether it\'s a reflection or something.  ---Toby
=--
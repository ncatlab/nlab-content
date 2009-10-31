# Definition 

A **weak limit** for a diagram in a [[category]] is a [[cone]] over that diagram which satisfies the existence property of a [[limit]] but not necessarily the uniqueness.

# Examples

A **weak [[pullback]]** of a [[cospan]] $A\overset{f}{\to} C \overset{g}{\leftarrow} B$ consists of a commutative square
\[\array{ P & \overset{p}{\to} & A\\
  ^q \downarrow && \downarrow ^f\\
  B & \overset{g}{\to} & C}\]
such that for any commutative square
\[\array{ X & \overset{x}{\to} & A\\
  ^y \downarrow && \downarrow ^f\\
  B & \overset{g}{\to} & C}\]
there exists a morphism $h:X\to P$, not necessarily unique, such that $x = h p$ and $y = h q$.

Every [[inhabited set]] is a weak [[terminal object]] in [[Set]], since there always exists a [[function]] from any [[set]] to any inhabited set.  But only a [[singleton]] is a terminal object.

# Projective objects and exact completion #

In any category with finite limits and [[projective object|enough projectives]], the full subcategory of projective objects has weak finite limits.  For example, given a cospan $A\overset{f}{\to} C \overset{g}{\leftarrow} B$ of projective objects, let $P\to A\times_C B$ be a projective cover of the actual pullback; then any square
\[\array{ X & \overset{x}{\to} & A\\
  ^y \downarrow && \downarrow ^f\\
  B & \overset{g}{\to} & C}\]
with $X$ projective induces a morphism $X\to A\times_C B$, which lifts to a morphism $X\to P$ since $X$ is projective.

Conversely, from any category with weak finite limits one can construct an [[exact category|exact completion]] in which the original category sits as the projective objects, and the exact categories constructible in this way are precisely those having enough projectives.

# Weak limits and homotopy limits #

Unlike usages of 'weak' in terms like [[weak n-category]], a weak limit is not be like a [[homotopy limit]] or a [[2-limit]], which satisfy uniqueness (as well as existence) albeit only up to higher [[homotopy|homotopies]] or [[weak equivalence|equivalences]].

However, some homotopy limits induce the corresponding type of weak limit in the corresponding [[homotopy category]].  For example, suppose that
$$\array{ P & \overset{p}{\to} & A\\
  ^q \downarrow && \downarrow ^f\\
  B & \overset{g}{\to} & C}
$$
is a homotopy pullback in some category $M$ having a notion of [[homotopy]], such as a [[model category]].  In particular, this square commutes up to homotopy, and thus it commutes in the homotopy category $Ho(M)$.  Then any square
$$\array{ X & \overset{x}{\to} & A\\
  ^y \downarrow && \downarrow ^f\\
  B & \overset{g}{\to} & C}$$
that commutes in $Ho(M)$ commutes up to homotopy in $M$, and thus (by the ("local") universal property of homotopy pullbacks), there is a map $h:X\to P$ and homotopies $p h \simeq x$ and $q h\simeq y$; thus the given square is a weak pullback in $Ho(M)$.  While the universal property of a homotopy pullback means that $h$ is unique up to homotopy, this is only true for a given _choice_ of homotopy $f x \simeq g y$, and different such homotopies can induce inequivalent $h$'s.  Thus in $Ho(M)$, which remembers only the _existence_ of homotopies, we have only a weak pullback.

Note, though, that not _all_ homotopy limits produce weak limits in the homotopy category, because in general it will not be possible to lift a cone that commutes in $Ho(M)$ to a cone that commutes up to _coherent_ homotopy in $M$.  However, in "simple" cases such as pullbacks, products, equalizers, sequential inverse limits, and so on, this is always true (and it will be true whenever the diagram category is a [[quiver]]).  On the other hand, homotopy products in $M$ give actual (not weak) products in $Ho(M)$, since there are no homotopies necessary.

Weak limits in homotopy categories play an important role in the [[Brown representability theorem]].

[[!redirects weak pullback]]
[[!redirects weak finite limits]]
[[!redirects weak limits]]

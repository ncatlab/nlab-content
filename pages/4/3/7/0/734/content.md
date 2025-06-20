
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A **weak limit** for a [[diagram]] in a [[category]] is a [[cone]] over that diagram which satisfies the existence property of a [[limit]] but not necessarily the uniqueness. The dual concept is a [[weak colimit]].

Beware that "weak" here does **not** correspond to that in "[[weak n-category]]", in particular it does **not** refer to [[homotopy limits]]. Nevertheless, there is a relation, see [below](#RelationToHomotopyLimits). It is due to this relation that weak limits in [[homotopy categories]] play a key role in the [[Brown representability theorem]].


## Weak pullbacks

A **weak pullback** of a  [[cospan]] 

$$
  A\overset{f}{\to} C \overset{g}{\leftarrow} B
$$ 

(in some [[category]]) is a [[commutative diagram|commutative square]]

$$
  \array{ 
    P & \overset{p}{\to} & A
    \\
    {}^{\mathllap{q}} \downarrow && \downarrow^{\mathrlap{f}}
    \\
    B & \overset{g}{\to} & C
  }
$$

such that for every commuting square



\[\array{ X & \overset{x}{\to} & A\\
   {}^{\mathllap{y}} \downarrow && \downarrow^{\mathrlap{f}}\\
   B & \overset{g}{\to} & C}\]

there exists a morphism $h \colon X\to P$, not necessarily unique, such that $x = h p$ and $y = h q$;

If the actual [[pullback]] $A \underset{C}{\times}B$ exists, then this condition means equivalently that the universal morphism 

$$
  P \longrightarrow A \underset{C}{\times}B
$$

is a [[split epimorphism]].

## Weak terminal objects

Every [[inhabited set]] is a weak [[terminal object]] in [[Set]], since there always exists a [[function]] from any [[set]] to any inhabited set.  But only a [[singleton]] is a terminal object.

## Projective objects and exact completion 

In any category with finite limits and [[projective object|enough projectives]], the full [[subcategory]] of [[projective object]]s has weak finite limits.  For example, given a cospan $A\overset{f}{\to} C \overset{g}{\leftarrow} B$ of projective objects, let $P\to A\times_C B$ be a projective cover of the actual pullback; then any square
\[\array{ X & \overset{x}{\to} & A\\
  ^y \downarrow && \downarrow ^f\\
  B & \overset{g}{\to} & C}\]
with $X$ projective induces a morphism $X\to A\times_C B$, which lifts to a morphism $X\to P$ since $X$ is projective.

Conversely, from any category with weak finite limits one can construct an [[exact category|exact completion]] in which the original category sits as the projective objects, and the exact categories constructible in this way are precisely those having enough projectives.

## Relation to homotopy limits 
 {#RelationToHomotopyLimits}

Unlike usages of 'weak' in terms like [[weak n-category]], a weak limit is not like a [[homotopy limit]] or a [[2-limit]], which satisfy uniqueness (as well as existence) albeit only up to higher [[homotopy|homotopies]] or [[weak equivalence|equivalences]].

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

## Related concepts

* [[weak adjoint]]

* [[weak multilimit]]

## References

* [[Peter Freyd]], _Representations in abelian categories_ 1966 Proc. Conf. Categorical Algebra (La Jolla, Calif., 1965) pp. 95&#8211;120 Springer, New York

[[!redirects weak limits]]


[[!redirects weak pullback]]
[[!redirects weak pullbacks]]

[[!redirects weak pushout]]
[[!redirects weak pushouts]]

[[!redirects weak finite limit]]
[[!redirects weak finite limits]]

[[!redirects weak terminal object]]
[[!redirects weak terminal objects]]
[[!redirects weakly terminal]]




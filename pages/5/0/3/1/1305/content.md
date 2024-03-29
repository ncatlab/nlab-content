
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The modifier __'quasi-compact'__ (or simply __'quasicompact'__) is used to denote a compactness property in the relative setup (that is, for morphisms) and in the setups emphasising non-Hausdorff topology. For example, schemes over complex numbers have both the [[complex analytic topology]] and the [[Zariski topology]]; we use "quasicompact" for Zariski and "compact" for complex topology in that setup. 

For many topologists, analysts and so on, the word 'compact' means a [[compact Hausdorff space]]. Some topological schools distinguish a "[[compact space]]" (which is not necessarily [[Hausdorff space|Hausdorff]]) and a "[[compactum]]" (which is Hausdorff); and similarly a "[[paracompact space]]" and a "[[paracompactum]]". In [[algebraic geometry]], in contrast, one usually says __quasicompact space__ to denote a topological space which is compact but not necessarily Hausdorff. For example, the [[Zariski topology]] on an [[algebraic variety]] and the topology of an &#233;tal&#233; space of a [[sheaf]] (even over a Hausdorff topological space) are typically not Hausdorff.

## Definition

A [[scheme]] is quasicompact iff it has a Zariski cover by [[finite number|finitely many]] open affine subschemes. In particular, any affine scheme is quasicompact. 

Most important is the relative version of this concept. A morphism $f\colon X \to Y$ of schemes is a __quasicompact morphism__ if the inverse image of a quasicompact Zariski open subset of $Y$ is quasicompact (EGAI6.6.1). 

It is straightforward to show [EGAI6.6.4] that it is enough to require this for affine subsets of $Y$, or even to require the existence of a single covering $Y = \cup_i U_i$ of $Y$ by open affine subschemes $U_i$, such that the inverse image $U_i \times_Y X$ of $U_i$ in $X$ is quasicompact. A scheme $X$ over a base scheme $S$ is quasicompact if the canonical morphism $X \to S$ is quasicompact. This is consistent, because if $X$ is a usual scheme (over the spectrum of integers $S = \mathbb{Z}$) or, more generally, a relative scheme over an _affine_ scheme $S$, quasicompactness of the canonical morphism $X\to S$ is by the above criteria clearly equivalent to the usual quasicompactness of $X$.

## Properties

A composition of quasicompact morphisms is quasicompact, and the pullback of quasicompact morphisms is quasicompact. This enables the definition for [[algebraic stack]]s: a morphism of algebraic stacks is quasicompact if the pullback of that morphism to some atlas is quasicompact.

Algebraic geometers sometimes (but more rarely) also talk about __quasicompact objects__ in more general categories, meaning [[compact object]]s (object which corepresent covariant functors commuting with filtered colimits); with or without a modifier denoting a cardinal ($\kappa$-quasicompact objects).  

## Related concepts

* [[finitely presented morphism]]

## References

An old discussion on the terminological aspects (Mike, Zoran, Toby) is at $n$Forum [here](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=2680&Focus=22689#Comment_22689).

category: algebraic geometry
[[!redirects quasicompact]]
[[!redirects quasi-compact]]

[[!redirects quasicompact morphism]]
[[!redirects quasicompact morphisms]]
[[!redirects quasi-compact morphism]]
[[!redirects quasi-compact morphisms]]

[[!redirects quasicompact scheme]]
[[!redirects quasicompact schemes]]
[[!redirects quasi-compact scheme]]
[[!redirects quasi-compact schemes]]

[[!redirects quasicompact map]]
[[!redirects quasicompact maps]]
[[!redirects quasi-compact map]]
[[!redirects quasi-compact maps]]

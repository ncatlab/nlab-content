#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

The notion of [[locale]] is a "point-less" version of that of [[topological space]]. A _localic group_ is much like a [[topological group]], but there are some differences.
For a groupoid generalization see [[localic groupoid]].

## Definition ##


A **localic group** is a [[group object]] [[internalization|in]] the [[category]] of [[locales]].

## Localic groups versus topological groups

Localic groups are similar to [[topological group]]s, and many examples can be considered as either one.  For instance, the real numbers $\mathbb{R}$ under addition can be considered as either a topological group or a localic group.  Since the "space of points" [[functor]] $Loc \to Top$ is a [[right adjoint]], it preserves [[limit]]s and hence [[group object]]s, so every localic group has an underlying topological group.

+-- {: .query}
I feel this might be misleading &#8212; for example, in _Remarks on Localic Groups_ by Isbell, K&#345;i&#382;, Pultr and Rosick&#253;, they construct a nontrivial localic group with only one point (or at least, _Frames and Locales_ by Picado and Pultr claims they do (6.2, p.313 in that book), I don't have institutional access to the paper)
=--

However, the "locale of opens" functor $Top\to Loc$ does not preserve [[product]]s, so not every topological group is a localic group---even if its underlying topological space is [[sober space|sober]] (hence is the space of points of some locale).  In particular, the locale $\mathbb{Q}$ of rational numbers (with [[topology]] induced from that of $\mathbb{R}$) is not a localic group under addition, because the locale product $\mathbb{Q}\times_l \mathbb{Q}$ is "bigger" than the topological-space product (and in particular is not spatial), and the addition map $\mathbb{Q}\times \mathbb{Q}\to \mathbb{Q}$ cannot be extended to the locale product.  However, if $G$ is a [[locally compact space|locally compact]] topological group (such as $\mathbb{R}$), then the space product $G\times G$ does agree with the locale product (using the [[ultrafilter principle]] in the proof), and hence $G$ is also a localic group.

## Examples

* Another important source of localic groups is from [[progroups]]: cofiltered limits of discrete groups.

## Localic subgroups are closed

A remarkable fact about localic groups is the following (which also proves that $\mathbb{Q}$ cannot be a localic group):

+-- {: .un_theorem}
###### Theorem
Any subgroup of a localic group is [[closed sublocale|closed]].
=--
+-- {: .proof}
###### Sketch of Proof
Details can be found in C5.3.1 of the [[Elephant]], in the more general case of localic [[groupoids]].  The basic idea of the proof is to use the fact that the intersection of any two [[dense sublocale]]s is again dense (a fact which very much fails for topological spaces).

If $H\rightarrowtail G$ is a localic subgroup, we construct its closure $\bar{H}$, which is also a localic subgroup in which $H$ is dense.  By [[pullback]], it follows that $H\times \bar{H} \to \bar{H} \times \bar{H}$ is [[fiberwise dense subspace|fiberwise dense]] over $\bar{H}$ via the second projection.  Applying the [[automorphism]] $(g,h) \mapsto (g,g^{-1}h)$ of $G\times G$, we conclude that $H\times \bar{H} \to \bar{H} \times \bar{H}$ is also [[fiber]]wise dense over $\bar{H}$ via the "composition" map.  Dually, $\bar{H}\times H \to \bar{H} \times \bar{H}$ is also fiberwise dense over $\bar{H}$ via the "composition" map, and thus (by the basic fact cited above), so is their intersection, which is $H\times H$.  Since $\bar{H}\times \bar{H}\to \bar{H}$ is an [[epimorphism]], so is $H\times H\to\bar{H}$.  But this map factors through $H\rightarrowtail \bar{H}$ (since $H$ is itself a subgroup of $G$), so that inclusion is also epic.  But it is also a [[regular monomorphism]], and hence an [[isomorphism]]; thus $H$ is closed.
=--


## References

* The [[Elephant]], chapter C5.


[[!redirects localic groups]]

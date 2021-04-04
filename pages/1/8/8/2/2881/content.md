#Contents#
* table of contents goes here
{:toc}


## Idea ##

A *localic group* is a [[group object]] [[internalization|internal]] to [[locales]].

As the notion of *[[locale]]* is a point-free version of that of *[[topological space]]*, a _localic group_ is much like a [[topological group]], but there are some differences.

The further generalization to [[groupoids]] is that of *[[localic groupoids]]*.

## Definition ##


A **localic group** is a [[group object]] [[internalization|in]] the [[category]] of [[locales]].

## Localic groups versus topological groups

Localic groups are similar to [[topological groups]], and many examples can be considered as either one.  For instance, the real numbers $\mathbb{R}$ under addition can be considered as either a topological group or a localic group.

Since the "space of points" [[functor]] $Loc \to Top$ is a [[right adjoint]], it preserves [[limits]] and hence [[group objects]], so every localic group has an underlying topological group.  However, this functor can discard information; for instance, [IKPR](#IKPR) constructs a nontrivial localic group with only one point.

Moreover, the "locale of opens" functor $Top\to Loc$ does not preserve [[product]]s, so not every topological group is a localic group---even if its underlying topological space is [[sober space|sober]] (hence is the space of points of some locale).  In particular, the locale $\mathbb{Q}$ of rational numbers (with [[topology]] induced from that of $\mathbb{R}$) is not a localic group under addition, because the locale product $\mathbb{Q}\times_l \mathbb{Q}$ is "bigger" than the topological-space product (and in particular is not spatial), and the addition map $\mathbb{Q}\times \mathbb{Q}\to \mathbb{Q}$ cannot be extended to the locale product.

But if $G$ is a [[locally compact space|locally compact]] topological group (such as $\mathbb{R}$), then the space product $G\times G$ does agree with the locale product (using the [[ultrafilter principle]] in the proof), and hence $G$ is also a localic group.

## Examples

* Another important source of localic groups is from [[progroups]]: cofiltered limits of discrete groups.
* The [[isotropy group of a topos]] is naturally regarded as a localic group inside the topos.

## Localic subgroups are closed

A remarkable fact about localic groups is the following (Corollary C5.3.2 of the [[Elephant]]; this also proves that $\mathbb{Q}$ cannot be a localic group):

+-- {: .num_theorem #LocalicSubgroupsAreClosed}
###### Theorem
Any [[overt space|overt]] localic subgroup of a localic group is weakly [[closed sublocale|closed]]. If the ambient localic group is in a [[Boolean topos]] then any localic subgroup is a [[closed subgroup]].
=--
+-- {: .proof}
###### Sketch of Proof
Details can be found in C5.3.1 of the [[Elephant]], in the more general case of localic [[groupoids]].  The basic idea of the proof is to use the fact that the intersection of any two [[dense sublocale]]s is again dense (a fact which very much fails for topological spaces).

If $H\rightarrowtail G$ is a localic subgroup, we construct its closure $\bar{H}$, which is also a localic subgroup in which $H$ is dense.  By [[pullback]], it follows that $H\times \bar{H} \to \bar{H} \times \bar{H}$ is [[fiberwise dense subspace|fiberwise dense]] over $\bar{H}$ via the second projection.  Applying the [[automorphism]] $(g,h) \mapsto (g,g^{-1}h)$ of $G\times G$, we conclude that $H\times \bar{H} \to \bar{H} \times \bar{H}$ is also [[fiber]]wise dense over $\bar{H}$ via the "composition" map.  Dually, $\bar{H}\times H \to \bar{H} \times \bar{H}$ is also fiberwise dense over $\bar{H}$ via the "composition" map, and thus (by the basic fact cited above), so is their intersection, which is $H\times H$.  Since $\bar{H}\times \bar{H}\to \bar{H}$ is an [[epimorphism]], so is $H\times H\to\bar{H}$.  But this map factors through $H\rightarrowtail \bar{H}$ (since $H$ is itself a subgroup of $G$), so that inclusion is also epic.  But it is also a [[regular monomorphism]], and hence an [[isomorphism]]; thus $H$ is closed.
=--


## References

* The [[Elephant]], chapter C5.

* [[John Isbell]], [[Igor Křiž]], [[Aleš Pultr]], [[Jiři Rosický]], _Remarks on Localic Groups_, Lecture Notes in Mathematics 1348 (1988), pp. 154-172: [doi](https://doi.org/10.1007/bfb0081357)
{#IKPR}

An expository account of the closed subgroup theorem can be found in

* [[Gavin Wraith]], [_The Closed Subgroup Theorem_](http://www.wra1th.plus.com/gcw/math/closed.html)

[[!redirects localic groups]]

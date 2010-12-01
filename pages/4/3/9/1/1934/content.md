
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Big and little toposes
* automatic table of contents goes here
{:toc}

## Idea

There are two different (related) relationships between [[Grothendieck topoi]] and a notion of "generalized space."  (Recall that a Grothendieck topos $T$ is a [[category of sheaves]] $T = Sh(S)$ on some [[site]] $S$.)

On the one hand, we can regard the topos *itself* as a generalized space.  This tends to be a useful point of view when the site $S$ is the [[category of open subsets]] $Op(X)$ of a [[topological space]] $X$ (or some [[manifold]] or the like), or some other site which we regard as containing data from only "one space."  In this case, we refer to $T$ as a **little topos**, or (if we fail to translate the original French) a **petit topos**.

On the other hand, we can view a topos $T$ as a well-behaved category whose *objects* are generalized spaces.  This tends to be a useful point of view when the site $S$ is a category of _all test [[space]]s_ in some sense, such as [[Top]], [[Diff]], or [[CartSp]].  In this case, we refer to $T$ as a **big topos**, or (in French) a **gros topos**.

These distinctions carry over in a straightforward way to higher topoi such as [[(∞,1)-topoi]].


## Relationships

Objects in a big topos $Sh(S)$ may be thought of as [[space]]s _modeled on $S$_, in the sense described at [[motivation for sheaves, cohomology and higher stacks]] and at [[space]].

On the other hand, the objects of a petit topos, such as $Sh(X)$, can also be regarded as a kind of generalized spaces, but generalized spaces _over $X$_ on which the rigid structure of morphisms in $Op(X)$ (only inclusions of subsets, no more general maps) induces a correspondingly rigid structure so that they are not all that general.  In fact, $Sh(Op(X))$ is equivalent to the category of [[etale space]]s over $X$---i.e. spaces "modeled on $X$" in a certain sense.  More generally, for any topos $E$, the objects of $E$ can be identified with [[local homeomorphisms of toposes]] into $E$.

From the "little topos" perspective, it can be helpful to think of a "big topos" as a "fat point," which is not "spread out" very much spatially itself, but contains within that point lots of different types of "local data," so that even spaces which are "rigidly" modeled on that point can have a lot of interesting cohesion and local structure.  (One should not be misled by this into thinking that a big topos has *only* one [[point of a topos|point]], although it is usually a [[local topos]] and hence has an [[initial object|initial]] point.)


## The big and little topos of an object

If $X$ is a topological space, then the canonical little topos associated to $X$ is the sheaf topos $Sh(X)$.  On the other hand, if $S$ is a site of probes enabling us to regard $X$ as an object of a big topos $H = Sh(S)$, then we can also consider the topos $H/X$ as a representative of $X$.  These two toposes are often called the **little topos of $X$** (or **petit topos of $X$**) and the **big topos of $X$** (or **gros topos of $X$**) respectively.

There might be some debate about whether $H/X$ is, itself, "a little topos" or "a big topos."  While it certainly contains information about the space $X$ specifically, its objects are not "spaces locally modeled on $X$" but rather spaces locally modeled on the big site $S$ which happen to have a map to $X$.  The standard phrase "the big topos of $X$" is the most descriptive.

Note that if $X$ is actually an *object* of the site $S$, then $H/X$ can be identified with the topos of sheaves on the [[slice category|slice]] site $S/X$ (and otherwise, it can be identified with the topos of sheaves on the [[category of elements]] of $X\in Sh(S)$).  This site $S/X$ is often referred to as the [[big site]] of $X$, as compared to the [[little site]], which is $Op(X)$ (or appropriate replacement).  The topos $Sh(S/X)$ can thus be viewed as spaces modelled on $S$, but parameterised by the representable sheaf $X$.

Note that when $S=Top$ with its local-homeomorphism topology, there is a canonical functor $Op(X) \to S/X$ which preserves finite limits and both [[cover-preserving functor|preserves]] and [[cover-reflecting functor|reflects]] covering families.  Therefore, it induces both a geometric morphism $H/X \to Sh(X)$ and one $Sh(X) \to H/X$, of which the latter is the left adjoint of the former in [[Topos]].  In other words, the geometric morphism $H/X \to Sh(X)$ is [[local geometric morphism|local]], and in particular a [[homotopy equivalence of toposes]].  This fact relating the big and little toposes of $X$ also holds in other cases.


## Axiomatizations

* If a site $S$ is given by a [[Grothendieck pretopology]], then one can define an associated notion of a [[little site]] associated to any object of $S$, and hence both a little topos and a big topos, which are related as above.

* One proposed axiomatization of the notion of big topos is that of a [[cohesive topos]].


## Examples

For $X$ a [[topological space]], the _little topos_ that it defines is the [[category of sheaves]] $Sh(X) := Sh(Op(X))$ on the [[category of open subsets]] of $X$. A general object in this topos can be regarded as an [[etale space]] over $X$. The space $X$ itself is incarnated as the [[terminal object]] $X = * \in Sh(X)$.

On the other hand, a _big topos_ in which $X$ is incarnated is a [[category of sheaves]] on a [[site]] of test spaces with which $X$ may be probed. For instance for $C =$ [[Top]], or [[Diff]] or [[CartSp]] with their standard [[coverage]]s, $Sh(C)$ is such a big topos.

In good cases, the intrinsic properties of $X$ do not depend on whether one regards it as a little topos or as an object of a gros topos. For instance at [[cohomology]] in the section <a href="http://ncatlab.org/nlab/show/cohomology#NonabelianSheafCohomology">Nonabelian sheaf cohomology with constant coefficients</a> it is discussed how the [[nonabelian cohomology]] of a [[paracompact space|paracompact]] [[manifold]] $X$ with constant coefficients gives the same answer in each case.


## References

Some aspects of an axiomatic characterization of petit vs. gros toposes is in 

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

A definition of gros vs petit toposes and remarks on applications in [[Galois theory]] is in

* Nick Duncan, _Gros and petit toposes_ ([pdf](http://www.cheng.staff.shef.ac.uk/pssl88/pssl88-duncan.pdf))

There is also something relevant in this article:

* [[Mathieu Anel]], _Grothendieck topologies from unique factorization systems_ ([arXiv:0902.1130](http://arxiv.org/abs/0902.1130))

* [[Mamuka Jibladze]], _Homotopy types for "gros" toposes_, thesis, [pdf](http://www.rmi.acnet.ge/~jib/thesis.pdf)

A discussion and comparison of big vs little approaches to $(\infty,1)$-topos theory began at these blog entries:

* [Cohesive (∞,1)-toposes](http://golem.ph.utexas.edu/category/2010/10/cohesive_toposes.html) and [Petit (∞,1)-toposes](http://golem.ph.utexas.edu/category/2010/10/petit_1toposes.html).


[[!redirects big topos]]
[[!redirects big toposes]]
[[!redirects big topoi]]
[[!redirects gros topos]]
[[!redirects gros toposes]]
[[!redirects gros topoi]]

[[!redirects little topos]]
[[!redirects little toposes]]
[[!redirects little topoi]]
[[!redirects petit topos]]
[[!redirects petit toposes]]
[[!redirects petit topoi]]

[[!redirects big or little topos]]
[[!redirects big or little toposes]]
[[!redirects big or little topoi]]
[[!redirects big and little topos]]
[[!redirects big and little toposes]]
[[!redirects big and little topoi]]
[[!redirects little or big topos]]
[[!redirects little or big toposes]]
[[!redirects little or big topoi]]
[[!redirects little and big topos]]
[[!redirects little and big toposes]]
[[!redirects little and big topoi]]
[[!redirects gros or petit topos]]
[[!redirects gros or petit toposes]]
[[!redirects gros or petit topoi]]
[[!redirects gros and petit topos]]
[[!redirects gros and petit toposes]]
[[!redirects gros and petit topoi]]
[[!redirects petit or gros topos]]
[[!redirects petit or gros toposes]]
[[!redirects petit or gros topoi]]
[[!redirects petit and gros topos]]
[[!redirects petit and gros toposes]]
[[!redirects petit and gros topoi]]

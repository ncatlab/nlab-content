
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Geometry
+-- {: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Between topological spaces

While every [[continuous map]] sends [[compact subsets]] to [[compact subsets]], it is not true in general that the [[preimage]] of a compact set along a continuous map is compact.

A [[continuous function]] $f : X \to Y$ between [[topological space]]s is **proper** if the [[inverse image]] of any [[compact space|compact]] subset is itself compact.

A notion of proper homotopy between proper maps leads to [[proper homotopy theory]].

Similarly, one can consider the conditions on morphisms in other geometric situations, like [[algebraic geometry]], and properness often either reflects or implies good behaviour with respect to the compact objects (cf. also proper push-forward). 


## Between schemes

A __proper morphism of [[scheme]]s__ is by definition a morphism $f:X\to Y$ which is 

1. [[separated morphism|separated]], 

2. of [[finite type morphism|finite type]]

3. [[universally closed morphism|universally closed]] (the latter means that for every $h: Z\to Y$ the pullback $h^*(f): Z\times_Y X\to Z$ is closed). 

There is a classical and very practical [[valuative criterion of properness]] due Chevalley. 

We say that a scheme $X$ is __proper__ if the canonical map $X \to \operatorname{Spec} \mathbb{Z}$ to the [[terminal object]] is proper. 

Proper schemes are analogous to [[compact topological spaces]]. This is one reason why one uses the terminology "quasi-compact" when referring to schemes whose underlying topological space is compact.

The [[base change]] formulas for [[cohomology]] for proper and for smooth morphisms of schemes motivated [[Alexander Grothendieck|Grothendieck]] (in [[Pursuing Stacks]]) to define abstract proper and smooth functors in the setting of [[fibered categories]]; this is further expanded on in 
([Maltsiniotis](#Maltsiniotis)).


## Between locales

Recall that a [[locale]] $L$ is given by a [[frame]] $O(L)$, its [[frame of opens]], and that a [[continuous map]] $f$ from $K$ to $L$ is given by an [[adjunction]] $f^* \dashv f_* \colon O(K) \rightleftarrows O(L)$ such that the [[inverse image]] function $f^*$ preserves finitary [[meets]] (or equivalently is a frame [[homomorphism]], since it must preserve all [[joins]]).

Such a map $f$ is __proper__ iff the [[direct image]] function $f_*$ preserves [[directed joins]] (or equivalently is [[Scott-continuous function|Scott-continuous]], or equivalently is a morphism of [[preframes]]), and also satisfies the [[Frobenius reciprocity]]-like condition that $f_*(U\cup f^*(V)) = f_*(U) \cup V$ (which by itself states that the map is [[closed map|closed]]).

In particular, the map $L\to 1$ is proper iff $L$ is both [[compact locale|compact]] and [[covert space|covert]].  But in this case the second condition is redundant, since every compact locale is automatically covert; see [[covert space]] for a proof.

Proper maps of locales can also be characterized as those that are universally closed, i.e. every pullback of them (along any map of locales) is closed.


## Between toposes

Proper maps of locales can be generalized to [[geometric morphisms]] of [[Grothendieck toposes]]; see [[proper geometric morphism]].

The topos-theoretic condition refers only to directed unions of subterminal objects, suggesting a stronger condition that it preserve all [[filtered colimits]].  This is a strictly stronger condition even for locales (i.e. [[localic toposes]]), called being *tidy*.  In fact properness and tidiness are the first two rungs on an infinite ladder of higher properness for [[higher toposes]].


## Related concepts

* [[proper base change theorem]]

* [[proper homotopy theory]]


## References

* [[Georges Maltsiniotis]], _Structures d'asph&#233;ricit&#233;, foncteurs lisses, et fibrations_, Ann. Math. Blaise Pascal __12__, pp. 1-39 (2005) ([ps](http://people.math.jussieu.fr/~maltsin/ps/asphbl.ps)).
 {#Maltsiniotis}
(TO ADD: The definition of a proper dg algebra, proper dg category, proper A-inf cat ???)

* wikipedia [proper morphism](http://en.wikipedia.org/wiki/Proper_morphism)
* Daniel Halpern-Leistner, Anatoly Preygel, _Mapping stacks and categorical notions of properness_, [arxiv/1402.3204](http://arxiv.org/abs/1402.3204)

[[!redirects proper map]]
[[!redirects proper maps]]
[[!redirects proper continuous map]]
[[!redirects proper continuous maps]]

[[!redirects proper morphism]]
[[!redirects proper morphisms]]
[[!redirects proper scheme]]
[[!redirects proper schemes]]
[[!redirects proper morphism of schemes]]
[[!redirects proper morphisms of schemes]]

[[!redirects proper functor]]
[[!redirects proper functors]]

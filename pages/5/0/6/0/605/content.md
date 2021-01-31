
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}


## Idea

An (oriented) _cobordism_ $\Sigma$ from an (oriented) [[smooth manifold]] $X_{in}$ to an (oriented) smooth manifold $X_{out}$ is a smooth [[manifold with boundary]] $\Sigma$ such that its [[boundary]] is the [[disjoint union]] 

$$
  \partial \Sigma \simeq X_{in} \coprod X_{out}
$$

with induced [[orientation]] agreeing with the given one on $X_{in}$ and being the opposite of that of $X_{out}$. Hence by labelling disjoint components of the boundary of any [[manifold with boundary]] $\Sigma$ as either "incoming" or "outgoing", then $\Sigma$ becomes a cobordism from its incoming to its outgoing boundary components.

(While $X_{in} \coprod X_{out}$ is the [[boundary]] of $\Sigma$, conversely $\Sigma$ is the "co-boundary" of $X_{in}\coprod X_{out}$. This is part of the reason for the "co-" in "cobordism", but sometimes one just says _bordism_. The difference is more pronounced when distinguishing between [[bordism homology theory]] and [[cobordism cohomology theory]].)

With a little bit of technical conditions on the boundary inclusions added, then $(n-1)$-dimensional manifolds with [[diffeomorphism]] classes of $n$-dimensional cobordisms between them form a [[category]] (a [[category of cobordisms]]) whose [[objects]] are the manifolds, whose [[morphisms]] are the cobordisms, and whose [[composition]] operation is the operation of gluing two cobordisms along a common boundary component.
Such a [[category of cobordisms]] $Bord_n$ of some [[dimension]] $n$  is naturally a  [[symmetric monoidal category]] $Bord_n^{\sqcup}$ with the [[tensor product]] being the [[disjoint union]] $\sqcup$ of manifolds.

The [[connected components]] in this category are called _cobordism classes_ of manifolds. Under [[cartesian product]] and [[disjoint union]], these form what is called the [[cobordism ring]] in the given dimension. The study of these classes, hence of manifolds "up to cobordisms", is a central topic in [[algebraic topology]].

A central insight connecting [[algebraic topology]] with [[mathematical physics]] is that a [[strong monoidal functor]] on a [[category of cobordisms]] with values in something like the category [[Vect]] (with its standard [[tensor product of modules]]) may be thought of as a formalized incarnation of what in [[physics]] is called a [[topological quantum field theory]]

$$
  Z \colon Bord_n^\sqcup \longrightarrow Vect^\otimes
  \,.
$$

Here one thinks of a cobordism $\Sigma$ as a piece of [[spacetime]] (or [[worldvolume]]) of dimension $n$, and of the $(n-1)$-dimensional manifolds that this goes between as a piece of [[space]] (or [[brane]]). A functor $Z$ as above is then thought of as sending each $(n-1)$-dimensional space $X$ to its [[space of quantum states]] $Z(X)$ and each spacetime $\Sigma$ between $X_{in}$ and $X_{out}$ to a [[linear map]] $Z(\Sigma)\colon Z(X_{in}) \longrightarrow Z(X_{out})$. 

From the perspective of [[mathematics]], such a functor is a way to break up [[diffeomorphism]] [[invariants]] of [[closed manifolds]] of [[dimension]] $n$ into pieces and being able to reconstruct them from gluing of data associated to manifolds with $(n-1)$-dimensional boundary.

If one considers [[manifolds with corners]] then there is a fairly evident refinement of the concept of cobordism that allows to further refine this process to gluing of [[extended cobordisms]] of any dimension $k$ going between [[extended cobordisms]] of dimension $k-1$. Such extended cobordisms of maximal dimension $n$ form a [[symmetric monoidal (infinity,n)-category]] called, naturally, the [[(infinity,n)-category of cobordisms]]. The [[cobordism hypothesis]] asserts that this is a most fundamental object in [[higher category theory]] and [[higher algebra]], namely that it is the _[[free construction|free]]_ [[symmetric monoidal (infinity,n)-category]] [[(infinity,n)-category with duals|with duals]]. The corresponding extended concept of [[topological quantum field theory]] is accordingly called [[extended TQFT]] or similar.

## Properties

### Relation to Cohomotopy
 {#RelationToCohomotopy}

The [[Pontrjagin-Thom isomorphism]]  says that assigning [[Cohomotopy charge]] identifies suitable [[cobordism classes]]  of [[submanifolds]] or abstract [[manifolds]] with [[cocycles]] in [[Cohomotopy|unstable Cohomotopy]] (see [here](cohomotopy#RelationToCobordismGroup)) or [[stable Cohomotopy]].

The following graphics illustrates the [[Cohomotopy charge map]] of the pair creation/annihilation cobordism for 0-dimensional [[submanifolds]]:

<center>
<a href="https://arxiv.org/pdf/1909.12277.pdf#page=11">
<img src="https://ncatlab.org/schreiber/files/BraneAntibranePairCreationInCohomotopy.jpg" width="700">
</a>
</center>

> graphics grabbed from [SS 19](cohomotopy+charge#SatiSchreiber19)

(See also at _[[Cohomotopy charge]] -- [For charged points](Cohomotopy+charge#ForChargedPoints)_.)

## Related concepts

* [[h-cobordism]]

* [[movie]]

* [[cobordism theory]]

* [[cobordism group]], [[cobordism ring]]

* [[Thom spectrum]], [[Thom's theorem]]

* [[cobordism category]]

* [[(infinity,n)-category of cobordisms]], [[cobordism hypothesis]]

* [[cobordism cohomology theory]]

* [[extended cobordism]] 

* [[B-bordism]]

* [[orbifold cobordism]]

* [[Lagrangian cobordism]]

* [[algebraic cobordism]]

* [[Sullivan chord diagram]]

## References

* {#Pontrjagin55} [[Lev Pontrjagin]], Section 3.6 of: _Smooth manifolds and their applications in Homotopy theory_, Trudy Mat. Inst. im Steklov, No 45, Izdat. Akad. Nauk. USSR, Moscow, 1955 (AMS Translation Series 2, Vol. 11, 1959) ([doi:10.1142/9789812772107_0001](https://www.worldscientific.com/doi/abs/10.1142/9789812772107_0001))

* {#Stong68} [[Robert Stong]], _Notes on Cobordism theory_, 1968 ([toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [publisher page](http://press.princeton.edu/titles/6465.html))

* [[Peter Landweber]], _A survey of bordism and cobordism_, Mathematical Proceedings of the Cambridge Philosophical Society, Volume 100, Issue 2 September 1986 , pp. 207-223 ([doi:10.1017/S0305004100066032](https://doi.org/10.1017/S0305004100066032))


* {#Kochmann96} [[Stanley Kochmann]], section 1.5 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* [[John Francis]] (notes by [[Owen Gwilliam]]), _[Topology of manifolds](http://math.northwestern.edu/~jnkf/classes/mflds/)_, _Lecture 2: Cobordism_ ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/2cobordism.pdf))

* [[Manifold Atlas]], _[Bordism](http://www.map.mpim-bonn.mpg.de/Bordism)_

* Wikipedia, _[Cobordism](http://en.wikipedia.org/wiki/Cobordism)_

For more see at _[[cobordism cohomology theory]]_.

A relation to [[fixed point spaces]]:

* {#Prieto03} Carlos Prieto, _Fixed point theory and framed cobordism_, Topol. Methods Nonlinear Anal. Volume 21, Number 1 (2003), 155-169. ([Euclid](https://projecteuclid.org/euclid.tmna/1475266278))



[[!redirects cobordisms]]

[[!redirects bordism]]
[[!redirects bordisms]]


[[!redirects cobordant manifold]]
[[!redirects cobordant manifolds]]

[[!redirects bordant manifold]]
[[!redirects bordant manifolds]]

[[!redirects cobordism class]]
[[!redirects cobordism classes]]
[[!redirects bordism class]]
[[!redirects bordism classes]]



[[!redirects bordism theory]]



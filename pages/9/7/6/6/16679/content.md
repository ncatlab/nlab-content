+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--

#Content#
* table of contents
{:toc}

## Idea

Multisimplicial sets are the analogs of [[simplicial sets]] with [[simplices]] replaced by [[multisimplices]] (perhaps more appropriately called multiplexes).

## Definition
 {#Definition}

+-- {: .num_defn}
###### Definition

An **$n$-fold multisimplicial set**  is a [[presheaf]] on the $n$-fold [[multisimplex category]] $\Delta^n$, that is, a [[functor]] $X\colon(\Delta^n)^{op}\to Sets$, equivalently a [[multisimplicial object]] in the category [[Set]] of sets.

=--

## Relation to simplicial sets

The category of $n$-fold multisimplicial sets can be
equipped with a [[model structure]] that turns
it into a [[model category]] that is Quillen equivalent
to the standard [[Kan–Quillen model structure]] on [[simplicial sets]].

Cofibrations of multisimplicial sets are precisely [[monomorphisms]].
Weak equivalences are induced from [[simplicial sets]] by the diagonal functor.

The corresponding [[Quillen adjunction]]
is constructed as as a [[nerve-realization adjunction]]
for the functor
$$\Delta^n\to sSet$$
that sends a multisimplex $(m_1,\ldots,m_n)$ to $\Delta^{m_1}\times\cdots\times\Delta^{m_n}$.

The left adjoint is given by a [[left Kan extension]].
The right adjoint sends a [[simplicial set]] $X$ to its multisimplicial nerve,
which sends a multisimplex $(m_1,\ldots,m_n)$ to $sSet(\Delta^{m_1}\times\cdots\times\Delta^{m_n},X)$.

To see that this [[Quillen adjunction]] is a [[Quillen equivalence]],
one can either argue directly, by computing the derived [[unit]] and derived [[counit]] and showing that they are [[weak equivalences]],
or, much more elegantly, invoke a theorem by [[Grothendieck]] and [[Maltsiniotis]].

The latter theorem (\cite{Maltsiniotis}, Proposition 1.6.8)
states that a totally aspherical [[small category]] $C$ with a separating aspherical interval is a [[strict test category]],
and, therefore, the category of presheaves of sets on $C$
admits a [[model structure]] whose cofibrations are monomorphisms
and weak equivalences are induced by the [[category of elements]] functor
from the [[Thomason model structure]] on the category of [[small categories]].
Furthermore, the resulting model category of presheaves of sets on $C$
is a cartesian [[combinatorial model category]] that is Quillen equivalent
to the [[Kan–Quillen model structure]] on the category of [[simplicial sets]].

We now verify the conditions of the theorem:

* The category of multisimplices is nonempty.

* The categorical product of two representable multisimplicial sets is acyclic, i.e., weakly equivalent to the terminal object.

* The multisimplex $([1],[1],\ldots,[1])$ together with the two canonical inclusions of $([0],\ldots,[0])$ is a separating aspherical interval.


## Exterior product

An important operation on multisimplicial sets is the _exterior product_
$$Fun((\Delta^m)^{op},Set)\times Fun((\Delta^n)^{op},Set)\to Fun((\Delta^{m+n})^{op},Set)$$
defined as the [[left Kan extension]] of the tautological functor
$$\Delta^m\times\Delta^n\to\Delta^{m+n}.$$

The exterior product is a [[left Quillen bifunctor]]
whose [[left derived bifunctor]] model the cartesian
product in the [[∞-category]] of spaces.

The exterior product is useful when it is desirable
to have a product operation that does not require subdivision.

## Related concepts

* [[simplicial sets]]

* [[cubical sets]]

* [[Cisinski model category]]

* [[test category]], [[strict test category]]

## References

* [[Zouhair Tamsamani]], _On non-strict notions of $n$-category and $n$-groupoid via multisimplicial sets_ ([arXiv:alg-geom/9512006](http://arxiv.org/abs/alg-geom/9512006))

* [[Gerd Laures]] and [[James E. McClure]],
_Multiplicative properties of Quinn spectra_
([arXiv:0907.2367v2](http://arxiv.org/abs/0907.2367v2))

* Yifeng Liu and Weizhe Zheng,
_Gluing restricted nerves of $\infty$-categories_
([arXiv:1211.5294](http://arxiv.org/abs/1211.5294))

* [[Georges Maltsiniotis]], _La théorie de l'homotopie de Grothendieck_, Astérisque 301 (2005).

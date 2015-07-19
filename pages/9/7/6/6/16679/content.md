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

The category of $n$-fold multisimplicial sets can be
equipped with a [[model structure]] that turns
it into a [[model category]] that is Quillen equivalent
to the standard [[Kan?Quillen model structure]] on [[simplicial sets]].

An important operation on multisimplicial sets is the _exterior product_
$$Fun((\Delta^m)^{op},Set)\times Fun((\Delta^n)^{op},Set)\to Fun((\Delta^{m+n})^{op},Set)$$
defined as the [[left Kan extension]] of the tautological functor
$$\Delta^m\times\Delta^n\to\Delta^{m+n}.$$

The exterior product is a [[left Quillen bifunctor]]
whose [[left derived bifunctor]] model the cartesian
product in the [[∞-category]] of spaces.

The exterior product is useful when it is desirable
to have a product operation that does not require subdivision.

## References

* [[Zouhair Tamsamani]], _On non-strict notions of $n$-category and $n$-groupoid via multisimplicial sets_ ([arXiv:alg-geom/9512006](http://arxiv.org/abs/alg-geom/9512006))

* [[Gerd Laures]] and [[James E. McClure]],
_Multiplicative properties of Quinn spectra_
([arXiv:0907.2367v2](http://arxiv.org/abs/0907.2367v2))

* Yifeng Liu and Weizhe Zheng,
_Gluing restricted nerves of $\infty$-categories_
([arXiv:1211.5294](http://arxiv.org/abs/1211.5294))
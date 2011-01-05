
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .un_def }
###### Definition

An [[(∞,1)-category]] is **sifted** if a [[quasi-category]] $K \in sSet$ modelling it has the property that

1. it is not empty, $K \neq \emptyset$

1. The diagonal $K \to K \times K$ (in [[sSet]]) models a [[cofinal (∞,1)-functor]].

=--

## Properties

+-- {: .un_prop }
###### Proposition


In a category of commutative monoids in a symmetric monoidal $(\infty,1)$-category, sifted colimits are computed as sifted colimits in the underlying $(\infty,1)$-category. See [[commutative monoid in a symmetric monoidal (∞,1)-category]] for details.

=--

+-- {: .un_prop }
###### Proposition

Let $K$ be a sifted $(\infty,1)$-category and let $C$ be an [[(∞,1)-category]] with $K$-shaped [[(∞,1)-colimit]]s and finite [[(∞,1)-products]] such that [[(∞,1)-colimit]]s of shape $K$ are preserved by finite [[(∞,1)-product]]s.

Then $K$-shaped [[(∞,1)-colimit]]s in $C$ commute with finite products. 

=--

This is [[Higher Topos Theory|HTT, lemma 5.5.8.1]].

## Examples

+-- {: .un_prop }
###### Proposition

The [[opposite category]] $\Delta^{op}$ of the [[simplex category]] is a sifted $(\infty,1)$-category.

=--

## Related concepts

* [[sifted category]]

* **sifted $(\infty,1)$-category**

## References

Section 5.5.8 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects sifted (infinity,1)-categories]]
[[!redirects sifted (∞,1)-category]]
[[!redirects sifted (∞,1)-categories]]

[[!redirects cosifted (infinity,1)-category]]
[[!redirects cosifted (infinity,1)-categories]]
[[!redirects cosifted (∞,1)-category]]
[[!redirects cosifted (∞,1)-categories]]

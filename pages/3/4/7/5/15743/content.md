+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable Homotopy theory
+-- {: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The **Waldhausen K-theory** of a [[dg-category]] is defined as the [[Waldhausen K-theory]] of a [[Waldhausen category]] associated to it.  It is an _additive invariant_ in the sense of [[noncommutative motives]].  There is a [[nonconnective K-theory|nonconnective]] variant studied by [[Marco Schlichting]], which is a _localizing invariant_ (again in the sense of [[noncommutative motives]]).

On the other hand, one could define the K-theory of a [[pretriangulated dg-category]] as the [[algebraic K-theory]] of its [[dg-nerve]], which is a [[stable infinity-category]].  This should coincide with the Waldhausen K-theory (presumably).

## Definition

Let $A$ be a [[dg-category]].  Consider the [[triangulated category]] $D(A)$ of [[dg-presheaves]] on $A$, and let $perf(A) \subset D(A)$ denote its [[full subcategory]] of [[compact objects]].  There is the structure of a [[Waldhausen category]] on $perf(A)$ where the [[weak equivalences]] are objectwise [[quasi-isomorphisms]] and the [[cofibrations]] are degreewise [[split monomorphisms]].  The **Waldhausen K-theory** of $A$ is the [[Waldhausen K-theory]] of $perf(A)$ with this Waldhausen structure.

## References

* [[Bernhard Keller]], _On differential graded categories_, International Congress of Mathematicians. Vol. II, 151--190, Eur. Math. Soc., Z&#252;rich, 2006, [pdf](https://www.imj-prg.fr/~bernhard.keller/publ/dgcatX.pdf).

* [[Marco Schlichting]], _Negative K-theory of derived categories_, Math. Z. 253 (2006), no. 1, 97 - 134, [pdf](http://homepages.warwick.ac.uk/~masiap/research/frob5.pdf).

* [[Goncalo Tabuada]], _Higher K-theory via universal invariants_, Duke Mathematical Journal, 145 (2008), no. 1, 121-206, [arXiv](http://arxiv.org/abs/0706.2420).

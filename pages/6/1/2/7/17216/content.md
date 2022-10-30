
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Motivated by the [[Freudenthal suspension theorem]], the _suspension category_ of ([Spanier-Whitehead 53](#SpanierWhitehead53)) has as [[objects]] [[pointed topological space|pointed]]  [[CW-complexes]], and as [[hom-sets]] it has [[colimits]] 

$$
  Hom(X,Y) \coloneqq \underset{\longrightarrow}{\lim}_q [\Sigma^q X , \Sigma^q Y]
$$ 

over [[homotopy classes]] of [[continuous functions]] between their arbitrary high [[suspensions]].

More generally one considers the category whose objects are pairs $(X,n)$ of a [[pointed topological space|pointed]]  [[CW-complex]] $X$ and an [[integer]] $n$ and whose [[hom-sets]] are 

$$
  Hom((X_1,n_1), (X_2,n_2)) \coloneqq \underset{\longrightarrow}{\lim}_{q \gt max({\vert n_1\vert},{\vert n_2\vert})} [\Sigma^{q+n_1} X_1 , \Sigma^{q+n_2} X_2]
  \,.
$$

This is a [[triangulated category]].

But the Spanier-Whitehead category lacks other desirable properties, for instance it does not have all [[coproducts]] and the canonical functor from the homotopy category of [[pointed topological spaces]] does not preserve the coproducts that already exist. As a consequence, in particular a [[Brown representability theorem]] does not hold in the SW-category.

Later it was realized (see e.g. [Whitehead 62](#Whitehead62)) that this all this is fixed by regardeding the SW-category for [[finite CW complexes]] as a [[full subcategory]] on the (shifted) [[suspension spectra]]  inside the larger category of [[spectra]]: the [[stable homotopy category]] (e.g. [Schwede 12, chapter II theorem 7.2](#Schwede12)). As such it is the full subcategory on the [[finite spectra]] (e.g. [Schwede 12, chapter II theorem 7.4](#Schwede12)).


## Related concepts

* [[Spanier-Whitehead duality]]

* [[prestable (∞,1)-category]]

## References

The definition is due to

* {#SpanierWhitehead53} [[Edwin Spanier]], [[George Whitehead]], _A first approximation to homotopy theory_ Proc. Nat. Acad. Sci. U.S.A., 39 (1953), 655-660. 

Survey includes

* {#Whitehead62} [[George Whitehead]], _Some aspects of stable homotopy theory_, International Confress of Mathematics 1962 ([pdf](http://www.mathunion.org/ICM/ICM1962.1/Main/icm1962.1.0502.0506.ocr.pdf))

* H. R. Margolis, _Spectra and the Steenrod algebra_, volume 29 of North-Holland
Mathematical Library. North-Holland Publishing Co., Amsterdam, 1983 

* [[Stefan Schwede]], chapter II, section 7 of  _[[Symmetric spectra]]_, 2012  ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))


Discussion in the abstract generality of categories equipped with an abstract suspension-like functor is in

* {#Heller68} [[Alex Heller]], _Stable homotopy categories_, Bull. Amer. Math. Soc. Volume 74, Number 1 (1968), 28-63. ([Euclid](https://projecteuclid.org/euclid.bams/1183529378))

* [[Ivo Dell'Ambrogio]], _The Spanier-Whitehead category is always triangulated_ ([pdf](http://math.univ-lille1.fr/~dellambr/diploma.pdf))

[[!redirects suspension category]]
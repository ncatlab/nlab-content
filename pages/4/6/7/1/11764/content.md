
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Over a [[site]] of [[complex analytic spaces]], where the [[multiplicative group]] $\mathbb{G}_m$ classifies non-vanishing [[holomorphic functions]] and $\mathbf{B}\mathbb{G}_m$ classifies [[holomorphic line bundles]], then a _holomorphic line 2-bundle_ is a $\mathbb{G}_m$-[[principal 2-bundle]], modulated by maps to $\mathbf{B}^2 \mathbb{G}_m$.

This means that the [[moduli stack]] of holomorphic line 2-bundles on a [[complex analytic space]] or more generally on a [[complex analytic ∞-groupoid]] $X$  is the [[Brauer stack]]  $\mathbf{Br}(X) \coloneqq [X,\mathbf{B}^2 \mathbb{G}_m]$ (the line 2-bundle itself is the [[associated ∞-bundle]] to the $\mathbf{B}\mathbb{G}_m$-[[principal ∞-bundle]] which is the [[homotopy fiber]] of a given map $X \to \mathbf{B}^2 \mathbb{G}_m$). In particular [[equivalence classes]] of holomorphic line 2-bundles form the elements of the [[bigger Brauer group]] of $X$ (the [[Brauer group]] proper if they are torsion).

Discussion in terms of [[bundle gerbes]] includes ([Chatterjee 98](#Chatterjee98),[Brylinski 00](#Brylinski00) [Mathai-Stevenson 02, section 7](#MathaiStevenson02)).

## Properties

### Dixmier-Douady class

The [[Dixmier-Douady class]] of holomorphic line 2-bundles, hence the higher analog of the [[first Chern class]], is given by the [[connecting homomorphism]] on degee 2 of the [[long exact sequence in cohomology]] which is induced by the [[exponential exact sequence]] in [[complex analytic geometry]]:

$$
  DD\;\colon\;  H^2(-,\mathbb{G}_m) \longrightarrow H^3(-,\mathbb{Z})
  \,.
$$

### Relation to higher twistor transforms
 {#RelationToHigherTwistorTransforms}

Holomorphic line 2-bundles appear in the higher degree analogs of [[twistor transforms]]. See ([Chatterjee 98](#Chatterjee98)) and see [twistor -- References -- Application to self-dual 2-forms](twistor%20space#ReferencesApplicationToSelfDual2FormField)

## Related concepts


* [[higher complex analytic geometry]]

* [[holomorphic line n-bundle]]

* [[algebraic line 2-bundle]]

## References

### General

Discussion in relation to [[Beilinson regulators]] is in

* {#Brylinski94} [[Jean-Luc Brylinski]], _Holomorphic gerbes and the Beilinson regulator_, Ast&#233;risque 226 (1994): 145-174 ([[Brylinski94.pdf:file]])

Early discussion in terms of [[bundle gerbes]] includes

* {#Chatterjee98} [[David Chatterjee]], section 5 of _On Gerbs_, 1998  ([pdf](http://people.maths.ox.ac.uk/hitchin/hitchinstudents/chatterjee.pdf))



Discussion with an eye towards of holomorphic [[twisted K-theory]] is in

* {#MathaiStevenson02} [[Varghese Mathai]], [[Danny Stevenson]], _Chern character in twisted K-theory: equivariant and holomorphic cases_, Commun.Math.Phys. 236 (2003) 161-186 ([arXiv:hep-th/0201010v5](http://lanl.arxiv.org/abs/hep-th/0201010v5))

An equivariant example arising from more algebro-geometric origin is in

* [[Giovanni Felder]], [[Andre Henriques]], Carlo A. Rossi, [[Chenchang Zhu]], _A gerbe for the elliptic gamma function_, Duke Math. J. 141(2008), 1-74 [arXiv:math/0601337](http://arxiv.org/abs/math/0601337) ([doi](http://dx.doi.org/10.1215/S0012-7094-08-14111-0))

Discussion connecting explicitly to the holomorphic [[Brauer group]] includes

* {#BenBassat08} [[Oren Ben-Bassat]], _Gerbes and the Holomorphic Brauer Group of Complex Tori_, Journal of Noncommutative Geometry, Volume 6, Issue 3 (2012) 407-455 ([arXiv:0811.2746](http://arxiv.org/abs/0811.2746))

* Edoardo Ballico, [[Oren Ben-Bassat]], _Meromorphic Line Bundles and Holomorphic Gerbes_, Math. Res. Lett. 18 (2011), 6, 1-14 ([arXiv:1101.2216](http://arxiv.org/abs/1101.2216))

See also 

* {#BenBassat11} [[Oren Ben-Bassat]], _Equivariant Gerbes on Complex Tori_ ([arXiv:1102.2312](http://arxiv.org/abs/1102.2312))

### Basic line 2-bundles on reductive groups
 {#ReferencesOnReductiveGroup}

The existence of the "basic" 2-line bundle (see at [[Chern-Simons line 3-bundle]]) on a complex [[reductive group]] (such as $SL(n,\mathbb{C})$) is mentioned in

* [[Jean-Luc Brylinski]], around theorem 5.4.10 (p. 226-227) of _Loop spaces and characteristic classes_, Birkh&#228;user

The actual construction appears in

* {#Brylinski00} [[Jean-Luc Brylinski]], _Gerbes on complex reductive Lie groups_ ([arXiv:math/0002158](http://arxiv.org/abs/math/0002158))

[[!redirects holomorphic line 2-bundles]]

[[!redirects holomorphic bundle gerbe]]
[[!redirects holomorphic bundle gerbes]]

[[!redirects holomorphic 2-line bundle]]
[[!redirects holomorphic 2-line bundles]]
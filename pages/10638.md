
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Tate curve_ is the [[formal neighbourhood]] of the [[nodal curve]] inside the  [[compactification|compactified]] [[moduli stack of elliptic curves]] $\mathcal{M}_{\overline{ell}}$. 

Over a given base ring $R$ it is an elliptic curve over the [[power series]] $R [ [ q ] ]$ which may be thought of as the quotient of the [[multiplicative group]] by $q^{\mathbb{Z}}$.

## Properties

### Relation to complex K-theory
 {#RelationToComplexKTheory}

The Tate curve is naturally an [[oriented elliptic curve]] and as such classified by a map


$$
  Spec \left(  KU ( ( q ) ) \right) \longrightarrow \mathcal{M}^{Der}
$$

in [[derived algebraic geometry]], from the spectrum of the [[power series]] over the [[KU]] [[E-∞ ring]] to the [[derived moduli stack of derived elliptic curves]].

### Relation to Tate K-theory
 {#RelationToTateKTheory}

The [[generalized cohomology theory]] over the Tate curve by the [[Goerss-Hopkins-Miller theorem]] is [[Tate K-theory]] $KO[ [q] ]$.

This is the [[homotopy limit]] over copies $KO \wedge \{1, q, \cdots, q^n\}_+$ of [[KO]] with formal parameters adjoined.

### Relation to the Witten genus

The [[elliptic genus]] associated with the Tate curve is, according to the [above](#RelationToComplexKTheory), a [[formal power series]] of [[K-theory]] classes. This is the _[[Witten genus]]_ ([Hopkins 94](#Hopkins94)).

Physically, Witten obtained this as the [[partition function]] of the [[heterotic string]] in [[perturbation theory]] about configurations where all the [[worldsheet]] sits in a single point of [[target space]]. This limiting case of the [[worldsheet]] is the Tate curve.

Formally this is given by the homotopy groups of the [[String orientation of tmf]] $M String \to tmf$ followed by the map to [[Tate K-theory]] [above](#RelationToTateKTheory), discussed [here](tmf#MapToTateKTheory).

[[!include moduli stack of curves -- table]]


## Related concepts

* [[spin orientation of Tate K-theory]]

## References

Conceptual discussion is in  

* [[Jacob Lurie]], pages 32, 33 of _[[A Survey of Elliptic Cohomology]]_.

Details are spelled out in 

* {#HillLawson13} [[Michael Hill]], [[Tyler Lawson]], section 3.4 of _Topological modular forms with level structure_ ([arXiv:1312.7394](http://arxiv.org/abs/1312.7394))


Basic reviews include

* Wikipedia, _[Tate curve](https://en.wikipedia.org/wiki/Tate_curve)_

See also

*  Antonios Broumas, _Congruences between the coefficients
of the Tate curve via formal groups_, Proc. Amer. Math. Soc. 128 (2000), 677-681 ([doi:10.1090/S0002-9939-99-05133-3](https://doi.org/10.1090/S0002-9939-99-05133-3))


The relation to the [[Witten genus]] originates around

* {#Hopkins94} [[Michael Hopkins]], _Topological modular forms, the Witten Genus, and the theorem of the cube_, Proceedings of the International Congress of Mathematics, Z&#252;rich 1994 ([pdf](http://www.mathunion.org/ICM/ICM1994.1/Main/icm1994.1.0554.0565.ocr.pdf))

More details on this are in ([Hill-Lawson 13, appendix A](#HillLawson13)).

 

[[!redirects Tate curves]]


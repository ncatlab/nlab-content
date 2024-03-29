
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

## Contents
* table of contents
{:toc}

## Idea

Serre duality in [[complex analytic geometry]] is the duality induced by the [[Hodge star operator]] on the [[Dolbeault complex]]. This generalizes to suitable non-singular [[projective algebraic varieties]] over other base rings.

## Statement

### In complex analytic geometry

Let $X$ be a [[Hermitian manifold]] of complex [[dimension]] $dim_{\mathbb{C}}(\Sigma) = n$. Its [[Riemannian metric]] induces a [[Hodge star operator]] which acts on the pieces in the [[Dolbeault complex]] as 

$$
  \star \colon \Omega^{p,q}(X)\to \Omega^{n-q, n-p}(X)
$$

(see at _[Hodge star operator -- On a K&#228;hler manifold](Hodge%20star%20operator#OnAKahlerManifold)_).

Moreover, [[complex conjugation]] gives $\mathbb{C}$-[[antilinear functions]]

$$
  \overline{(-)} \colon \Omega^{p,q}(X)\to \Omega^{q,p}(X)
  \,.
$$

+-- {: .num_defn #ComplexConjugatedHodgeStar}
###### Definition

Write

$$
  \bar \star \;\coloneqq\; \overline{(-)} \circ \star = \star \circ \overline{(-)}
  \;\colon\;
  \Omega^{p,q}(X)\to \Omega^{n-p, n-q}(X)
$$

for the [[composition|composite]] [[antilinear function]].

=--

e.g. ([Huybrechts 04, def. 4.1.6](#Huybrechts04))

+-- {: .num_remark}
###### Remark

By the [basic properties of the Hodge star](Hodge+star+operator#BasicProperties) it follows that restricted to $\Omega^{p,q}(X)$

$$
  \bar \star \circ \bar \star = (-1)^{p+q}
  \,.
$$

=--



+-- {: .num_defn #ThePairing}
###### Definition

For $X$ a [[compact topological space|compact]] [[Hermitian manifold]], define a [[bilinear form]]

$$
  \int_X (-) \wedge \bar \star (-)
  \;\colon\;
  \Omega^{p,q}(X) \otimes \Omega^{n-p,n-q}(X)
   \longrightarrow
   \mathbb{C}
$$

as the [[integration of differential forms]]

$$
  (\alpha,\beta) \mapsto \int_X \alpha \wedge \bar \star \beta
$$

of the wedge product of $\alpha$ with the image of $\beta$ under the complex conjugated Hodge star operator of def. \ref{ComplexConjugatedHodgeStar}.

=--

+-- {: .num_prop #StatementForTrivialBundleOverHermitianManifold}
###### Proposition
**(Serre duality)**

The pairing of def. \ref{ThePairing} induces a non-degenerate sesquilinear (i.e. hermitian) form  on [[Dolbeault cohomology]]

$$
  \int_X (-) \wedge \bar \star (-)
  \;\colon\;
  \H^{p,q}(X) \otimes H^{n-p,n-q}(X)
   \longrightarrow
   \mathbb{C}
$$

=--

e.g. ([Huybrechts 04, prop 4.1.15](#Huybrechts04))

## Properties

### Relation to Poincar&#233; duality

+-- {: .num_remark #SerreDualityActionOnComplexordinaryCohomologyOfKaehlerManifold}
###### Remark

For $\Sigma$ a [[compact topological space|compact]] [[Kähler manifold]] the [[Hodge theorem]] gives an [[isomorphism]]

$$
  H^k(X, \mathbb{C})
  \simeq
  \underset{p+q = k}{\oplus} H^{p,q}(X)
$$

between the [[ordinary cohomology]] of the underlying [[topological space]] with [[coefficients]] in the [[complex numbers]], and the [[direct sum]] of all the [[Dolbeault cohomology]] groups in the same total degree.

Therefore for $\Sigma$ of complex [[dimension]] $dim_{\mathbb{C}}(\Sigma)= n$ then Serre duality in the form of prop. \ref{StatementForTrivialBundleOverHermitianManifold} induces an [[isomorphism]] in [[ordinary cohomology]] of the form

$$
  H^k(X, \mathbb{C})
  \stackrel{\simeq}{\longrightarrow}
  H^{2n-k}(X, \mathbb{C})
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition

The isomorphism in remark \ref{SerreDualityActionOnComplexordinaryCohomologyOfKaehlerManifold}
coincides with [[Poincaré duality]].


=--

## Related concepts

* [[complex conjugation]], [[Hodge star operator]]

## References

* Wikipedia, _[Serre duality](http://en.wikipedia.org/wiki/Serre_duality)_

Discussion in [[complex analytic geometry]] ([[Hermitian manifolds]]) includes

* {#Huybrechts04} [[Daniel Huybrechts]] around prop. 4.1.15 of _Complex geometry - an introduction_. Springer (2004). Universitext. 309 pages. ([pdf](http://www.math.uh.edu/~shanyuji/2012/Geometry/Huybrechts.pdf))

* R.O. Wells, _Differential Analysis on Compact Manifolds_, Second Edition,
Springer, 1980. 14

and review with emphasis on the case of [[Kähler manifolds]] includes

* Julien Meyer, _Hodge theory on K&#228;hler manifolds_ ([pdf](http://homepages.ulb.ac.be/~jmeyer/Templates/hodgetheory.pdf))


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $X$ a [[smooth manifold]] and $H \in \Omega^3(X)$ a closed [[differential form|differential 3-form]], the $H$ **twisted de Rham complex** is the $\mathbb{Z}_2$-[[graded vector space]] $\Omega^{even}(X) \oplus \Omega^{odd}(X)$ equipped with the $H$-twisted [[de Rham differential]]

$$
  d + H \wedge(-) \;\colon\; \Omega^{even/odd}(X) \to \Omega^{odd/even}(X)
  \,,
$$


Notice that this is nilpotent, due to the odd degree of $H$, such that $H \wedge H = 0$, and the closure of $H$, $d H = 0$.

There is also the cohomology of the [[chain complex]] whose maps are just multiplication by $H$. 


$$
  H \wedge(-) \;\colon\; \Omega^{even/odd}(X) \to \Omega^{odd/even}(X)
  \,,
$$

This is also called _[[H-cohomology]]_ ([Cavalcanti 03, p. 19](#Cavalcanti03)). 

## Properties

* Twisted de Rham cohomology is the recipient of the [[twisted Chern character]] in [[twisted differential K-theory]].

+-- {: .num_prop #TwistedDeRhamCohomologyCoincidesWithHCohomologyOnInfinitesimllayThickenedPoint}
###### Proposition

On a [[formal manifold]] extension of a point, hence on an [[infinitesimally thickened point]], $H$-twisted de Rham cohomology for any closed 3-form $H$ coincides with [[H-cohomology]]. 

=--

([Cavalcanti 03, theorem 1.6](#Cavalcanti03)).

## References

* {#Cavalcanti03} [[Gil Cavalcanti]], _New aspects of the ddc-lemma_ ([arXiv:math/0501406](https://arxiv.org/abs/math/0501406))

[[!redirects twisted de Rham complex]]

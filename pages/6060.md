
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

The [[twisted cohomology]]-version of [[de Rham cohomology]] (a simple example of [[twisted differential cohomology]]):

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

If the [[de Rham complex]] $(\Omega^\bullet(X),d_{dr})$ is [[formal dg-algebra|formal]], then for $H \in \Omega_{cl}^3(X)$ a [[closed differential form|closed]] [[differential 3-form]], the $H$-[[twisted de Rham cohomology]] of $X$ coincides with its [[H-cohomology]], for any closed 3-form $H$. 

=--

([Cavalcanti 03, theorem 1.6](#Cavalcanti03)).

## References


### Twist in degree 3
 {#ReferencesForTwistInDegree3}

The concept of $H_3$-twisted de Rham cohomology  was introduced (in discussion of the [[B-field]] in [[string theory]]), in:

* [[Ryan Rohm]], [[Edward Witten]], around (23) and appendix of: _The antisymmetric tensor field in superstring theory_, Annals of Physics Volume 170, Issue 2, September 1986, Pages 454-489 (<a href="https://doi.org/10.1016/0003-4916(86)90099-0">doi:10.1016/0003-4916(86)90099-0</a>)

Further discussion:

* {#CBMMS}  [[Peter Bouwknegt]], [[Alan Carey]], [[Varghese Mathai]], [[Michael Murray]], [[Danny Stevenson]], Section 9.3 of: _Twisted K-theory and K-theory of bundle gerbes_ ,  Commun Math Phys, 228 (2002) 17-49 ([arXiv:hep-th/0106194](http://arxiv.org/abs/hep-th/0106194), [doi:10.1007/s002200200646](https://doi.org/10.1007/s002200200646))

* [[Varghese Mathai]], [[Danny Stevenson]], Section 3 of: _Chern character in twisted K-theory: equivariant and holomorphic cases_, Commun. Math. Phys. 236:161-186, 2003 ([arXiv:hep-th/0201010](https://arxiv.org/abs/hep-th/0201010))

* [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], Section 2 of: _Twisted equivariant K-theory with complex coefficients_, Journal of Topology, Volume 1, Issue 1, 2007 ([arXiv:math/0206257](https://arxiv.org/abs/math/0206257), [doi:10.1112/jtopol/jtm001](https://doi.org/10.1112/jtopol/jtm001))

* [[Constantin Teleman]], around Prop. 3.7 in: _K-theory of the moduli of bundles over a Riemann surface and deformations of the Verlinde algebra_, in: [[Ulrike Tillmann]] (ed.) _Topology, geometry and quantum field theory_, Cambridge 2004 ([arXiv:math/0306347](https://arxiv.org/abs/math/0306347), [spire:660158](https://inspirehep.net/literature/660158))

* {#Cavalcanti03} [[Gil Cavalcanti]], Section I.4 of: _New aspects of the $d d^c$-lemma_, Oxford  2005 ([arXiv:math/0501406](https://arxiv.org/abs/math/0501406))

### Twist in degree 1
 {#ReferencesForTwistInDegree1}

The classical case of twisted de Rham cohomology with twists in *degree 1*, given by [[flat connections]] on [[flat line bundles]] and more generally on [[flat vector bundles]]), and its equivalence to [[sheaf cohomology]] with [[cofficients]] in [[abelian sheaves]] of [[flat sections]] ([[local systems]]):

Review:

* Cailan Li, *Cohomology of Local Systems on $X_\Gamma$* ([pdf](http://math.columbia.edu/~mundy/L3.pdf), [[Li_CohomologyOfLocalSystems.pdf:file]])

Discussion in the context of [[analytic torsion]]:

* [[Varghese Mathai]], [[Siye Wu]], _Analytic torsion for twisted de Rham complexes_, J. Diff. Geom. 88:297-332, 2011 ([arXiv:0810.4204](https://arxiv.org/abs/0810.4204))

### Twist in higher degrees
 {#ReferencesTwistInHigherDegrees}

(...)



[[!redirects twisted de Rham complex]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The _Euler class_ is a [[characteristic class]] of the [[special orthogonal group]], hence of [[oriented]] [[real vector bundles]]. 

The Euler class of the [[tangent bundle]] of a [[manifold]] is its [[Euler characteristic]].

## Properties

### Whitney sum formula
 {#WhitneySumFormula}


+-- {: .num_prop #EulerClassOfWhitneySumIsCupProductOfEulerClasses}
###### Proposition
**([[Euler class]] takes [[Whitney sum]] to [[cup product]])**

The Euler class of the [[Whitney sum]] of two [[orthogonal group|oriented]] [[real vector bundles]] to the [[cup product]] of the separate Euler classes:

$$
  \chi( E \oplus F )
  \;=\;
  \chi(E)  \smile \chi(F)
  \,.
$$

=--

### Poincaré–Hopf theorem

* [[Poincaré–Hopf theorem]]



### Fiber integration

+-- {: .num_prop  #FiberIntegrationOfCupPowersOfChiOver4Sphere}
###### Proposition

Let 

$$
  \array{
    S^4
    &\longrightarrow& 
    B Spin(4)
    \\
    &&
    \big\downarrow^{\mathrlap{\pi}}
    \\
    && 
    B Spin(5)
  }
$$

be the [[spherical fibration]] of [[classifying spaces]] induced from the canonical inclusion of [[Spin(4)]] into [[Spin(5)]] and using that the [[4-sphere]] is equivalently the [[coset space]] $S^4 \simeq Spin(5)/Spin(4)$ ([this Prop.](sphere#nSphereAsCosetSpace)).

Then the [[fiber integration]] of the odd [[cup product|cup powers]] $\chi^{2k+1}$ of the [[Euler class]] $\chi \in H^4\big( B Spin(4), \mathbb{Z}\big)$ (see [this Prop](Spin4#IntegralCohomologyOfClassifyingSpace))  are proportional to [[cup product|cup powers]] of the [[second Pontryagin class]] 

$$
  \pi_\ast
  \left(
    \chi^{2k+1}
  \right)
  \;=\;
  2 \big( p_2 \big)^k 
  \;\;\in\;\;
  H^4\big( B Spin(5), \mathbb{Z} \big) 
  \,,
$$

for instance

$$
  \begin{aligned}
    \pi_\ast
    \big(
      \chi
    \big)
    & = 
    2 
    \\
    \pi_\ast
    \left(
      \chi^3
    \right)
    & = 
    2 p_2 
    \\
    \pi_\ast
    \left(
      \chi^5
    \right)
    & = 
    2 (p_2)^2 
  \end{aligned}
    \;\;\in\;\;
    H^4\big( B Spin(5), \mathbb{Z} \big) 
  \,;
$$

while the [[fiber integration]] of the even [[cup product|cup powers]] $\chi^{2k}$ vanishes

$$
  \pi_\ast
  \left(
    \chi^{2k}
  \right)
  \;=\;
  0
  \;\;\in\;\;
  H^4\big( B Spin(5), \mathbb{Z} \big) 
  \,.
$$

 
=--

([Bott-Cattaneo 98, Lemma 2.1](#BottCattaneo98))




## Related concepts

* [[Pontryagin class]], [[Stiefel-Whitney class]], [[Wu class]]

* [[I8|one-loop anomaly polynomial]]

## References

Review includes

* [[Allen Hatcher]], _Euler and Pontryagin classes_, section 3.2 in _[Vector bundles and K-theory](http://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html)_ ([pdf](http://pi.math.cornell.edu/~hatcher/VBKT/VB.pdf))

* Anant R. Shastri, section 2.1 of _Vector bundles and Characteristic Classes_ ([pdf](http://www.math.iitb.ac.in/~ars/seminar/bundle.pdf))

* Michael Hutchings, section 5 of _Cup product and intersections_ ([pdf](https://math.berkeley.edu/~hutching/teach/215b-2011/cup.pdf))

Discussion for [[projective modules]] 

* Satya Manda, _An overview of Euler class theory_ ([pdf](http://mandal.faculty.ku.edu/talks/amsTalk06.pdf))

Discussion of [[fiber integration]]:

* {#BottCattaneo98} [[Raoul Bott]], [[Alberto Cattaneo]], _Integral Invariants of 3-Manifolds_, J. Diff. Geom., 48 (1998) 91-133 ([arXiv:dg-ga/9710001](https://arxiv.org/abs/dg-ga/9710001))

See also

* Wikipedia [Euler class](http://en.wikipedia.org/wiki/Euler_class)

* Robert F. Brown, _On the Lefschetz number and the Euler class_, Transactions of the AMS __118__, (1965)  ([JSTOR](http://www.jstor.org/pss/1993952))

* Solomon Jekel, _A simplicial formula and bound for the Euler class_, Israel Journal of Mathematics __66__, n. 1-3, 247-259 (1989)

[[!redirects Euler classes]]
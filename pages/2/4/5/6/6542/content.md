
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
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

The _Euler class_ $\chi$ (or $e$) is a [[characteristic class]] of the [[special orthogonal group]], hence of [[oriented]] [[real vector bundles]]. 

The Euler class of the [[tangent bundle]] of a [[smooth manifold]] $X$, evaluated on its [[fundamental class]], is its [[Euler characteristic]] $\chi[X]$.

## Properties

### Cup square
 {#CupSquare}

For $E$ a [[vector bundle]] of [[even number|even]] [[rank of a vector bundle|rank]] $rank(E) = 2 k$, the  [[cup product]] of the [[Euler class]] with itself equals the $k$th [[Pontryagin class]]

\[
  \label{EulerSquareIsPontryagin}
  \chi(E) \smile \chi(E)
  \;=\;
  p_k(E)
  \,.
\]

(e.g. [Walschap 04, Section 6.3, p. 187](#Walschap04))

When the Euler class is represented by the [[Euler form]] of a [[connection]] $\nabla$ on $E$, which then is [[fiber]]-wise proportional to the [[Pfaffian]] of the [[curvature form]] $F_\nabla$ of $\nabla$, the relation (eq:EulerSquareIsPontryagin) corresponds to the fact that the product of a [[Pfaffian]] with itself is the [[determinant]]: $\big( Pf(F_\nabla) \big)^2 = det(F_\nabla)$.

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

(e.g. [Walschap 04, Section 6.4](#Walschap04))

### Relation to top Chern class

\begin{prop}
  The [[top Chern class]] of a [[complex vector bundle]] $\mathcal{V}_X$ equals the [[Euler class]] $e$ of the underlying [[real vector bundle]] $\mathcal{V}^{\mathbb{R}}_X$:

$$
  \mathcal{V}_X
  \;
  \text{has complex rank}\;n
  \;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;   
  c_n
  \big(
    \mathcal{V}_X
  \big)
  \;\;
    =
  \;\;
  e
  \big(
    \mathcal{V}^{\mathbb{R}}_X
  \big)
  \;\;\;\;
  \in
  H^{2n}
  \big(
   X; 
   \,
   \mathbb{Z} 
  \big)
  \,.
$$
\end{prop}

(e.g. [Bott-Tu 82 (20.10.6)](#BottTu82))

For more see at _[[top Chern class]]_.


### Poincaré–Hopf theorem

* [[Poincaré–Hopf theorem]]


### On unit sphere bundles

+-- {: .num_prop #TrivializationOfEulerFormOnUnitSphereBundle}
###### Proposition

Let $X$ be a [[smooth manifold]] and $E \overset{\pi}{\longrightarrow} X$ an oriented [[real vector bundle]] of [[even number|even]] [[rank of a vector bundle|rank]], $rank(E) = 2k + 2$. 

For any choice of [[connection on a bundle|connection]] $\nabla$ on $E$ ($SO(dim(X))$-connection), let $\chi(\nabla_E) \in \Omega^{2k}(X)$ denote the corresponding [[Euler form]].

Then the [[pullback of differential forms|pullback]] of the [[Euler form]] $\chi(\nabla_E)$ to the [[unit sphere bundle]] $S(E) \overset{S(\pi)}{\longrightarrow} X$ is [[exact differential form|exact]] 

$$
  \big( S(\pi) \big)^\ast
  \chi(\nabla_E)
  \;=\;
  d \Omega
$$

such that the trivializing form has (minus) unit [[integration of differential forms|integral]] over any of the [[n-sphere|(2k+1)-sphere]]-[[fibers]] $S^{2k+1}_x \overset{\iota_x}{\hookrightarrow} S(E)$:

\[
  \label{FiberIntegrationOfTrivialization}
  \int_{S^{2k+1}} \iota_x^\ast \Omega 
  \;=\;
  -1
  \,.
\]

=--

(e.g. [Walschap 04, Chapter 6.6, Thm. 6.1, p. 201-202](#Walschap04), [Poor 07, 3.68](#Poor07), [Nie 09](#Nie09))

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

### General


* {#BottTu82} [[Raoul Bott]], [[Loring Tu]], Chapter 11 of  _[[Differential Forms in Algebraic Topology]]_, Graduate Texts in Mathematics 82, Springer 1982 ([doi:10.1007/BFb0063500](https://doi.org/10.1007/BFb0063500))


* [[Allen Hatcher]], _Euler and Pontryagin classes_, section 3.2 in _[Vector bundles and K-theory](http://pi.math.cornell.edu/~hatcher/VBKT/VBpage.html)_ ([pdf](http://pi.math.cornell.edu/~hatcher/VBKT/VB.pdf))

* Anant R. Shastri, section 2.1 of _Vector bundles and Characteristic Classes_ ([pdf](http://www.math.iitb.ac.in/~ars/seminar/bundle.pdf))

* Michael Hutchings, section 5 of _Cup product and intersections_ ([pdf](https://math.berkeley.edu/~hutching/teach/215b-2011/cup.pdf))

* {#Walschap04} Gerard Walschap, chapter 6.3 of _Metric Structures in Differential Geometry_, Graduate Texts in Mathematics, Springer 2004 

Discussion of [[fiber integration]]:

* {#BottCattaneo98} [[Raoul Bott]], [[Alberto Cattaneo]], _Integral Invariants of 3-Manifolds_, J. Diff. Geom., 48 (1998) 91-133 ([arXiv:dg-ga/9710001](https://arxiv.org/abs/dg-ga/9710001), [euclid:jdg/1214460608](https://projecteuclid.org/euclid.jdg/1214460608))


Discussion for [[projective modules]] 

* Satya Manda, _An overview of Euler class theory_ ([pdf](http://mandal.faculty.ku.edu/talks/amsTalk06.pdf))

See also

* Wikipedia [Euler class](http://en.wikipedia.org/wiki/Euler_class)

* Robert F. Brown, _On the Lefschetz number and the Euler class_, Transactions of the AMS __118__, (1965)  ([JSTOR](http://www.jstor.org/pss/1993952))

* Solomon Jekel, _A simplicial formula and bound for the Euler class_, Israel Journal of Mathematics __66__, n. 1-3, 247-259 (1989)


### Euler forms

Discussion of _[[Euler forms]]_ ([[differential form]]-representatives of Euler classes in [[de Rham cohomology]]) as [[Pfaffians]] of [[curvature forms]]:

* {#Chern44} [[Shiing-Shen Chern]], _A Simple Intrinsic Proof of the Gauss-Bonnet Formula for Closed Riemannian Manifolds_, Annals of Mathematics, Second Series, Vol. 45, No. 4 (1944), pp. 747-752 ([jstor:1969302](https://www.jstor.org/stable/1969302))


* {#BottTu82} [[Raoul Bott]], [[Loring Tu]], Chapter 11 of  _[[Differential Forms in Algebraic Topology]]_, Graduate Texts in Mathematics 82, Springer 1982 ([doi:10.1007/BFb0063500](https://doi.org/10.1007/BFb0063500))


* {#MathaiQuillen86} [[Varghese Mathai]], [[Daniel Quillen]], below (7.3) of _Superconnections, Thom classes, and equivariant differential forms_, Topology Volume 25, Issue 1, 1986 (<a href="https://doi.org/10.1016/0040-9383(86)90007-8">10.1016/0040-9383(86)90007-8</a>)

* {#Wu05} Siye Wu, Section 2.2 of _Mathai-Quillen Formalism_, pages 390-399 in _Encyclopedia of Mathematical Physics_ 2006 ([arXiv:hep-th/0505003](https://arxiv.org/abs/hep-th/0505003))

* [Walschap 04, section 6.3](#Walschap04)

* {#Poor07} Walter A. Poor, 3.58 of _Differential Geometric Structures_, Dover Books on Mathematics, 2007


* {#Nie09} Zhaohu Nie, _Secondary Chern-Euler forms and the Law of Vector Fields_ ([arXiv:0909.4754](https://arxiv.org/abs/0909.4754)


* [[Hiro Lee Tanaka]], _Pfaffians and the Euler class_, 2014 ([pdf](http://www.hiroleetanaka.com/pdfs/2014-fall-230a-lecture-26-gauss-bonnet-chern.pdf))

* {#Nicolaescu18} [[Liviu Nicolaescu]], Section 8.3.2 of _Lectures on the Geometry of Manifolds_, 2018 ([pdf](https://www3.nd.edu/~lnicolae/Lectures.pdf), [MO comment](https://mathoverflow.net/a/117982/381))


[[!redirects Euler classes]]

[[!redirects Euler form]]
[[!redirects Euler forms]]

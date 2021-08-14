
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


On the [[stable homotopy type|stable]] [[homotopy type]] of [[mapping spaces]] of (regular) [[rational maps]].

Under good conditions, the [[topological subspace|subspace inclusion]] of the space of [[rational maps]] (regular, see Rem. \ref{NotionsOfRationalMaps}),
between given projective [[complex manifolds]] or [[algebraic varieties]],
into the [[mapping space]] of all [[continuous maps]]  
induces an [[isomorphism]] in integral [[ordinary homology]] in low degrees, while for maps out of the [[Riemann sphere]] this is even an isomorphism on [[homotopy groups]] in low degrees:

$$
  Maps_{rat}(X_1, X_2)
  \xhookrightarrow{ {homology\; iso} \atop {in\; low\; degree} }
  Maps_{cts}(X_1, X_2)
  \,.
$$

This phenomenon originates in results of [Segal 1979](#Segal79) and is commonly referred to by Segal's name (e.g. "theorems of Segal-type" in [Friedlander & Lawson 1997, Sec. 5.C](#FriedlanderLawson97).

Whenever this holds it provides

1. from left to right: [[homotopy theory|homotopy theoretic]] tools for analyzing [[moduli spaces]] of rational hypersurfaces;

1. from right to left: small algebraic models for [[stable homotopy types|stable]] [[homotopy types]] of [[mapping spaces]]

at least up to some dimension.

## Details

Some remarks on the terminology being used:

\begin{remark}\label{NotionsOfDegree}
**("degree")**\linebreak
  Most or all of the following statement invoke an [[integer]] "degree" of [[continuous functions]]. Beware that this is *not* the [[degree of a continuous function]] (see there) in the usual sense of [[algebraic topology]], except in special cases (such as the archetypical example \ref{TheArchetypicalExample}). 
\end{remark}

\begin{remark}\label{NotionsOfRationalMaps}
**("rational maps")** \linebreak
  It it tradition (starting with Segal) to speak of [[rational maps]] in the following, but in the end the focus on *regular rational maps* ("morphisms": e.g. [Friedlander & Lawson 1997, p. 27](#FriedlanderLawson97))), as is necessary to regard them as [[continuous functions]] defined everywhere on the given [[domain]] $X_1$.

In many cases of interest, such as when the [[domain]] $X_1$ is a non-singular [[complex curve]]/[[Riemann surface]] and the [[codomain]] $X_2$ a [[complex projective space]], then all rational maps from $X_1$ to $X_2$ are automatically regular (e.g. [Shafarevich Vol1, Cor. 2.3](rational+map#ShafarevichVol1)). 
\end{remark}

### Maps from a Riemann surface to a projective space

* For $n \in \mathbb{N}_+$, consider [[complex projective n-space]]
$\mathbb{C}P^n$. 

* Say that a [[continuous map]] $f \;\colon\; \Sigma_2 \to \mathbb{C}P^n$ out of a 2-[[dimension of a manifold|dimensional]] [[manifold]] has *degree* $d \in \mathbb{N}$ (Rem. \ref{NotionsOfDegree}) if the [[pullback in cohomology|pullback]] of the generator $1 \in \mathbb{Z} \simeq H^2\big( \mathbb{C}P^n;\, \mathbb{Z}\big)$ (see [here](complex+projective+space#OrdinaryHomologyAndCohomology)) is 

  \[
    \label{DegreeOfAMapToCPn}
    f^\ast(1) 
     \,=\, 
    d 
      \,\in\, 
    \mathbb{Z} 
      \,\simeq\, 
    H^2(\Sigma_2;\, \mathbb{Z})
    \,.
  \]

* For $\Sigma$ a [[compact topological space|compact]] [[connected topological space|connected]] [[Riemann surface]] write $g_\Sigma \in \mathbb{N}$ for its [[genus of a Riemann surface|genus]]. 

\begin{proposition}\label{SegalOnHomotopyTypeOfRationalMapsIntoCPn}
**(Segal's theorem)** \linebreak
  For $\Sigma$ a [[compact topological space|compact]] [[connected topological space|connected]] [[Riemann surface]], the inclusion
  \[
    \label{RationalMappingSpaceInsideContinuousMappingSpace}
    Maps_{
      {rat}
    }^{deg = d}
    \big(
      \Sigma
      ,\,
      \mathbb{C}P^n
    \big)
    \xhookrightarrow{ \;\; i \;\; }
    Maps_{
      {cts}
    }^{deg = d}
    \big(
      \Sigma
      ,\,
      \mathbb{C}P^n
    \big)
  \]
  of 

  * the [[topological subspace]] of [[rational maps]] to [[complex projective n-space]] 

    (the *[[moduli spaces]] of rational [[complex curves]] in [[complex projective n-space|$\mathbb{C}P^n$]]*)

  into 

  * the [[connected component]] of maps of [[degree of a map|degree]] $d$ of the [[mapping space]] (with the [[compact open topology]]) of all [[continuous maps]] 

is

* for $g_\Sigma = 0$ (i.e. $\Sigma$ the [[Riemann sphere]]):

  an [[isomorphism]] on [[homotopy groups]] in degrees $\leq d (2 n -1)$;

* for $g_\Sigma \geq 1$:

  an [[isomorphism]] on [[ordinary homology|ordinary]] [[homology groups]] in degrees $\leq (d - 2g) (2 n -1)$.

\end{proposition}
([Segal 1979, Prop. 1.2, 1.3](#Segal79))

\begin{example}\label{TheArchetypicalExample}
**(the archetypical case)** \linebreak
  In the special case that $n = 1$ and $\Sigma = S^2$ is the [[2-sphere]] with its [[complex structure]], so that both [[domain]] and [[codomain]] are the [[Riemann sphere]] $\mathbb{C}P^1$, Prop. \ref{SegalOnHomotopyTypeOfRationalMapsIntoCPn} says that
$$
    Maps_{
      {rat}
    }^{deg = d}
    \big(
      \mathbb{C}P^1
      ,\,
      \mathbb{C}P^1
    \big)
    \xhookrightarrow{ \;\; i \;\; }
    Maps_{
      {top}
    }^{deg = d}
    \big(
      S^2
      ,\,
      S^2
    \big)
$$

is an isomorphism on [[homotopy groups]] up to degree $\leq d$.
\end{example}
([Segal 1979, Prop. 1.1'](#Segal79)) 

\begin{remark}\label{RelationToYangMillsMonopoles}
**(relation to [[Yang-Mills monopoles]])** \linebreak
Example \ref{TheArchetypicalExample} controls the classification of [[Yang-Mills monopoles]]. See there for more
\end{remark}

\begin{remark}\label{RelationToGromovWittenTheory}
**(relation to [[Gromov-Witten theory]])**
  A compactification and [[quotient stack]] of the space of rational maps 
  in (eq:RationalMappingSpaceInsideContinuousMappingSpace) is considered in [[Gromov-Witten theory]], e.g. [Bertram 2002, p. 9](Gromov-Witten+theory#Bertram02).
\end{remark}

\begin{remark}\label{RelationToTwistorStringTheory}
**(relation to [[twistor string theory]])** \linebreak
  In the context of [[twistor string theory]], 
the spaces of rational maps $\Sigma \to \mathbb{C}P^3$ (eq:RationalMappingSpaceInsideContinuousMappingSpace)  are interpreted as [[moduli spaces]] of [[D1-brane]]-[[instantons]] in the [[twistor space]] [[complex projective 3-space|$\mathbb{C}P^3$]] ([Witten 2004, Sec. 3](twistor+string+theory#Witten04)).

Such rational maps are also argued to encode [[scattering amplitudes]] in [[D=4 N=8 supergravity]] ([Cachazo & Skinner 2012](twistor+string+theory#CachazoSkinner12), [Adamo 2015](twistor+string+theory#Adamo15)).

Here the number of poles in the rational function  is the number $n$ of particles in the [[n-point function]], and the genus and degree encode the particle's [[helicity]] and the [[loop order]] of the [[scattering amplitude]].
\end{remark}


\begin{remark}\label{ComaprisonToHomotopicalOkaPrinciple}
**(comparison to the [[homotopical Oka principle]])** \linebreak
  Prop. \ref{SegalOnHomotopyTypeOfRationalMapsIntoCPn} may be compared to the [homotopical Oka principle](Oka+principle#HomotopicalOkaPrinciple), which applies (since $\mathbb{C}P^n$ is an [[Oka manifold]] by [this Prop.](Oka+manifold#ComplexProjectiveSpaceIsOkaManifold)) to the complementary case of connected *non-compact* ("open") Riemann surfaces $\Sigma$ (which are [[Stein manifolds]] by [this Example](Stein+manifold#SteinSurfacesAreOpenRiemannSurfaces)), in which case it says that the corresponding inclusion of the space of [[holomorphic maps]]

$$
    Maps_{
      {hol}
    }
    \big(
      \Sigma
      ,\,
      \mathbb{C}P^n
    \big)
    \xhookrightarrow{ \;\; i \;\; }
    Maps_{
      {top}
    }
    \big(
      \Sigma
      ,\,
      \mathbb{C}P^n
    \big)
$$

induces an isomorphism on all [[homotopy groups]], hence is a [[weak homotopy equivalence]] -- reflecting the fact that non-compactness of the Riemann surfaces and absence of any asymptotic boundary condition provides a large supply of holomorphic functions.
\end{remark}


### Maps between projective spaces
 {#MapsBetweenProjectiveSpaces}

Generalization to higher dimensional domain spaces:

* Say that the *degree* of a [[rational map]] $f \;\colon\; \mathbb{C}P^{n_1} \to \mathbb{C}P^{n_2}$ between two [[complex projective spaces]] is the degree of the [[polynomials]] that define it.

* In generalization of (eq:DegreeOfAMapToCPn), say that a [[continuous map]] $f \;\colon\; \mathbb{C}P^{n_1} \to \mathbb{C}P^{n_2}$ between two [[complex projective spaces]] has *degree* $d \in \mathbb{N}$ (Rem. \ref{NotionsOfDegree}) if this is the induced factor for [[pullback in cohomology|pullback in]] their second [[integers|integral]] [[ordinary cohomology]] (see [here](complex+projective+space#OrdinaryHomologyAndCohomology))

  \[
    \label{DegreeOfAMapBetweenComplexProjectiveSpaces}
    \array{
      \mathbb{Z}
      \simeq
      H^2\big( \mathbb{C}P^{n_2};\, \mathbb{Z}\big)
      &\xrightarrow{ f^\ast }&
      H^2\big( \mathbb{C}P^{n_1};\, \mathbb{Z}\big)
      \simeq 
      \mathbb{Z}
      \\
      1 &\mapsto& d
    }
    \,.
  \]


\begin{prop}\label{HomologyEquivalenceForMapsBetweenComplexProjectiveSpaces}
  For $1 \leq n_1 \leq n_2$, and $d \in \mathbb{N}$, the inclusion 
  $$
    Maps^{deg = d}_{rat}
    \big(
      \mathbb{C}P^{n_1}
      ,\,
      \mathbb{C}P^{n_2}
    \big)
    \xhookrightarrow{\;\;\;\;}
    Maps^{deg = d}_{cts}
    \big(
      \mathbb{C}P^{n_1}
      ,\,
      \mathbb{C}P^{n_2}
    \big)
  $$
  of the [[topological subspace]] of [[rational maps]] of algebraic degree $d$ into the [[mapping space]] of [[continuous functions]] of degree $d$ in the sense of (eq:DegreeOfAMapBetweenComplexProjectiveSpaces) induces an [[isomorphism]] on integral [[ordinary homology]] in degrees

  $$
    \leq\,
    \big(
      2 n_1 - 2 n_2 + 1
    \big)
    \big(
      \lfloor(d+2)/2\rfloor + 1
    \big)
    \,,
  $$
  where $\lfloor - \rfloor$ denotes the integer [[floor]] of a rational number.
\end{prop}

([Mostovoy 2006, Theorem 2](#Mostovoy06), with corrected proof in [Mostovoy 2012](#Mostovoy12))

An analogous result for [[real projective spaces]] is in [Adamaszek, Kozlowski & Yamaguchi 2008](#AdamaszekKozlowskiYamaguchi08).

Prop. \ref{HomologyEquivalenceForMapsBetweenComplexProjectiveSpaces} generalizes to the case that the [[codomain]] $\mathbb{C}P^{n_2}$ is allowed to be any [[smooth variety|smooth]] [[toric variety]] ([Mostovoy & Munguia-Villanueva 2012](#MostovoyMunguiaVillanueva12), [Kozlowski & Yamaguchi 2018](#KozlowskiYamaguchi18)).


## Related concepts

* [[Yang-Mills monopole]]

* [[Oka principle]]

* [[Cohomotopy]]


## References

### Maps out of Riemann surfaces

The original theorem for maps from compact Riemann surfaces to projective spaces:

* {#Segal79} [[Graeme Segal]], _The topology of spaces of rational functions_, Acta Math. Volume 143 (1979), 39-72 ([euclid:1485890033](https://projecteuclid.org/euclid.acta/1485890033))

Further discussion:

* [[Fred Cohen]], [[Ralph Cohen]], [[B. M. Mann]], [[R. J. Milgram]], _The topology of rational functions and divisors of surfaces_, Acta Math (1991) 166: 163 ([doi:10.1007/BF02398886](https://doi.org/10.1007/BF02398886))

* {#FriedlanderLawson97} [[Eric M. Friedlander]], [[H. Blaine Lawson]], Section 5.C of: *Duality Relating Spaces of Algebraic Cocycles and Cycles*, Topology Volume 36, Issue 2, March 1997, Pages 533-565 ([pdf](https://dornsife.usc.edu/assets/sites/1163/docs/Preprint_versionsPublications/10/projH.pdf))

* [[Ralph L. Cohen]], [[John D. S. Jones]], [[Graeme B. Segal]], *Stability for holomorphic spheres and Morse theory*, in: K. Grove, I. H. Madsen, E. K. Pedersen (eds.) *Geometry and Topology: Aarhus*, Contemporary Mathematics
Volume: 258 (2000)  ([arXiv:math/9904185](https://arxiv.org/abs/math/9904185), [ ISBN:978-0-8218-2158-9](https://bookstore.ams.org/conm-258))

* {#Kamiyama07} Yasuhiko Kamiyama, *Remarks on spaces of real rational functions*, The Rocky Mountain Journal of Mathematics Vol. 37, No. 1 (2007), pp. 247-257 ([jstor:44239357](https://www.jstor.org/stable/44239357))


Generalization to the case that the [[codomain]] is 

... a [[Grassmannian]]:

* [[Frances Kirwan]], *On spaces of maps from Riemann surfaces to Grassmannians and applications to the cohomology of moduli of vector bundles*, Ark. Mat. 24(1-2): 221-275 (1985) ([doi:10.1007/BF02384399](https://www.projecteuclid.org/journals/arkiv-for-matematik/volume-24/issue-1-2/On-spaces-of-maps-from-Riemann-surfaces-to-Grassmannians-and/10.1007/BF02384399.full))

... a [[toric variety]]:

* [[Martin A. Guest]], *The topology of the space of rational curves on a toric variety*, Acta Math. 174(1): 119-145 (1995) ([doi:10.1007/BF02392803](https://projecteuclid.org/journals/acta-mathematica/volume-174/issue-1/The-topology-of-the-space-of-rational-curves-on-a/10.1007/BF02392803.full), [arXiv:alg-geom/9301005](https://arxiv.org/abs/alg-geom/9301005))

... a [[flag manifold]]:

* [[C. P. Boyer]], [[B. M. Mann]], [[J. C. Hurtubise]], [[R. J. Milgram]], *The topology of the space of rational maps into generalized flag manifolds*, Acta Mathematica. 1994 Mar 1;173(1):61-101 ([doi:10.1007/BF02392569](https://projecteuclid.org/journals/acta-mathematica/volume-173/issue-1/The-topology-of-the-space-of-rational-maps-into-generalized/10.1007/BF02392569.full))

* [[J. C. Hurtubise]], *Holomorphic maps of a Riemann surface into a flag manifold*, J. Differential Geom. 43(1): 99-118 (1996) ([doi:10.4310/jdg/1214457899](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-43/issue-1/Holomorphic-maps-of-a-Riemann-surface-into-a-flag-manifold/10.4310/jdg/1214457899.full))

Application to the [[quantization]] of [[Skyrmions]] (via their rational map Ansatz, see the references [there](skyrmion#SkyrmionsFromRationalMapsReferences)):


* [[Steffen Krusch]], *Homotopy of rational maps and the quantization of Skyrmions*, Annals of Physics Volume 304, Issue 2, April 2003, Pages 103-127 (<a href="https://doi.org/10.1016/S0003-4916(03)00014-9">doi:10.1016/S0003-4916(03)00014-9</a>)

* [[Steffen Krusch]], *Skyrmions and Rational Maps*, talk at KIAS 2004  ([pdf](http://newton.kias.re.kr/KH04/talks/krusch.pdf), [[Krusch_SkyrmionsAndRationalMaps.pdf:file]])


* [[Steffen Krusch]], *Quantization of Skyrmions* ([arXiv:hep-th/0610176](https://arxiv.org/abs/hep-th/0610176))


### Maps between projective spaces

On maps between [[complex projective spaces]]:

* {#Mostovoy06} [[Jacob Mostovoy]], *Spaces of rational maps and the Stone–Weierstrass theorem*, Topology Volume 45, Issue 2, March 2006, Pages 281-293 ([doi:10.1016/j.top.2005.08.003](https://doi.org/10.1016/j.top.2005.08.003))

corrected proof in:

* {#Mostovoy12} [[Jacob Mostovoy]], *Truncated Simplicial Resolutions and Spaces of Rational Maps*, The Quarterly Journal of Mathematics, Volume 63, Issue 1, March 2012, Pages 181–187 ([doi:10.1093/qmath/haq031](https://doi.org/10.1093/qmath/haq031))

On maps between [[real projective spaces]]:

* {#AdamaszekKozlowskiYamaguchi08} [[Michal Adamaszek]], [[Andrzej Kozlowski]], [[Kohhei Yamaguchi]], *Spaces of algebraic and continuous maps between real algebraic varieties*, Quart. J. Math. 62 (2011), 771–790 ([arXiv:0809.4893](https://arxiv.org/abs/0809.4893), [doi:10.1093/qmath/haq029](https://doi.org/10.1093/qmath/haq029))

On maps from [[real projective space]] to [[complex projective space]]:

* [[Andrzej Kozlowski]], [[Kohhei Yamaguchi]], *Spaces of algebraic maps from real projective spaces into complex projective spaces* ([arXiv:0812.3954](https://arxiv.org/abs/0812.3954)), in: [[Yves Félix]] et al. (eds.) *Homotopy Theory of Function Spaces and Related Topics*, Contemporary Mathematics Volume: 519; 2010 ([ISBN:978-0-8218-4929-3](https://bookstore.ams.org/conm-519))

and [[equivariant homotopy theory|equivariantly]]:

* [[Andrzej Kozlowski]], [[Kohhei Yamaguchi]], *Spaces of equivariant algebraic maps from real projective spaces into complex projective spaces*, RIMS Kôkyûroku Bessatsu B39 (2013), 051−061 ([arXiv:1109.0353](https://arxiv.org/abs/1109.0353), [published pdf](https://www.kurims.kyoto-u.ac.jp/~kenkyubu/bessatsu/open/B39/pdf/B39_006.pdf))

### Maps from projective spaces to toric varieties

On maps from [[complex projective space]] to smooth [[toric varieties]]:

* {#MostovoyMunguiaVillanueva12} [[Jacob Mostovoy]], Erendira Munguia-Villanueva, *Spaces of morphisms from a projective space to a toric variety*, Revista Colombiana de Matematicas **48** 1 (2014) ([arXiv:1210.2795](https://arxiv.org/abs/1210.2795), [published pdf](http://scm.org.co/archivos/revista/Articulos/1129.pdf))

* {#KozlowskiYamaguchi18} [[Andrzej Kozlowski]], [[Kohhei Yamaguchi]], *The homotopy type of spaces of rational curves on a toric variety*, Topology and its Applications Volume 249, 1 November 2018, Pages 19-42 ([doi:10.1016/j.topol.2018.06.006](https://doi.org/10.1016/j.topol.2018.06.006))



[[!redirects homotopies of rational maps]]

[[!redirects homotopy type of spaces of rational maps]]
[[!redirects homotopy types of spaces of rational maps]]

[[!redirects homotopy type of spaces of rational functions]]
[[!redirects homotopy types of spaces of rational functions]]


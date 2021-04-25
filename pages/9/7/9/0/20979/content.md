


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 
  {#Idea}

A _universal Vassiliev invariant_ is a [[Vassiliev knot invariant]] with [[coefficients]] in [[formal power series]] of [[Jacobi diagrams]] in [[Planck's constant]] $\hbar$ whose leading term in $\hbar$ on a given [[singular knot]] is its [[chord diagram]].

By evaluating (framed) [[weight systems]] on the [[Jacobi diagram]] [[coefficients]] of a universal Vassiliev invariant it defines a [[function]] from framed [[weight systems]] on [[Jacobi diagrams]], [[chord diagrams modulo 4T are Jacobi diagrams modulo STU|equivalently]] on [[round chord diagrams]] to actual ([[ground field]]-valued) [[Vassiliev knot invariants]].

This construction in particular yields the proof that [[weight systems are the associated graded objects of Vassiliev invariants]].

In principle there is a vector space of universal Vassiliev invariants, but all that appear in the literature tend to agree ([BNGRT 97](#BNGRT97))
and are identified  ([AF 96](#AF96)) with the un-traced [[Wilson loop observable]] of [[perturbative quantization of 3d Chern-Simons theory|perturbative Chern-Simons theory]]:

<center>
<img src="https://ncatlab.org/nlab/files/UniversalWilsonLoopObservable.jpg" width="700">
</center>


<center>
<img src="https://ncatlab.org/nlab/files/TheGrandStoryOfVassilievKnotInvariantsII.jpg" width="800">
</center>

> from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


The main other known universal Vassiliev iunvariant is the [[Kontsevich integral]] (see [Lescop 02](#Lescop02) for the comparison).

\linebreak

## Ingredients
 {#Ingredients}

Write 

\[
  \label{CSFeynmanDiagrams}
  \mathcal{D}^{cs} \;\in\; Set^{\mathbb{N}}
\]

for the [[graded set]] of [[isomorphism classes]] of  trivalent framed knot graphs -- [[Feynman diagrams]] for [[Chern-Simons theory]] in the presence of [[Wilson loops]], called "Wilson graphs" [AF 96, Section 1](#AF96), slightly differing from the un-framed knot graphs in [CCRL 02](#CattaneoCottaRamusinoLongoni02).

By definition, a [[graph]] $\Gamma \in \mathcal{D}^{cs}$ must have [[even number]] of [[vertices]], and its degree is half that number ([AF 96, (2.9)](#AF96))

$$
  \Gamma \;\in\; \mathcal{D}^{cs}_{(\# Vert_\Gamma)/2}
  \,.
$$

For any $\Gamma \in \mathcal{D}^{cs}$ write 

$$
  Aut(\Gamma)
  \;\in\;
  Grp
$$

for its [[automorphism group]], a [[finite group]] whose [[order of a group|order]] we denote by

\[
  \label{AutomorphismGroup}
  \left\vert Aut(\Gamma)\right\vert
  \;\in\;
  \mathbb{N}
  \,.
\]

Write 

\[
  \label{KnotGraphComplex}
  \mathcal{G}^\bullet \;\in\; Ch^\bullet(\mathbb{R})
\]

for the framed [[knot graph complex]] and

$$
  H^\bullet(\mathcal{G})_3 
  \subset 
  H^\bullet(\mathcal{G})
$$

for the sub-vector space of its cohomology spanned by cocycles made of trivalent graphs.

Write 

\[
  \label{JacobiDiagramsModuloSTU}
  \mathcal{A}_\bullet 
  \;\coloneqq\;
  Span
  \left( 
    \mathcal{D}^t
  \right)/(STU)
  \;
  \in 
  \;
  Vect_\bullet(\mathbb{R})
\]

for the [[graded vector space]] of [[Jacobi diagrams]] [[quotient vector space|modulo]] the [[STU-relations]].

Also write

\[
  \label{LinearizationMaps}
  \array{ 
    && \mathcal{D}^{cs}
    \\
    & 
      {}^{\mathllap{ [-]_{{}_{\mathcal{A}}} }}
      \swarrow 
    && 
     \searrow^{\mathrlap{ [-]_{\mathcal{G}} }}
    \\
    \mathcal{A}_\bullet
    &&
    &&
    \mathcal{G}^\bullet
  }
\]

for the [[functions]] that send a [[graph]] to the defining [[linear basis|basis]] [[vector]] that it represents in these [[vector spaces]], respectively.


The space $\mathcal{A}_\bullet$ is the graded [[linear dual]] of the space of [[weight systems]] 

$$
  \mathcal{W}^\bullet
  \;\coloneqq\;
  (\mathcal{A}_\bullet)^\ast
  \,.
$$

Hence if we regard 

$$
  \mathcal{A}_\bullet
  \;=\;
  (\mathcal{A}^{-\bullet}, d= 0)
$$

as a [[cochain complex]] in non-positive degree with vanishing [[differential]], then its [[tensor product of cochain complexes]] with the knot graph complex is the [[cochain complex]] whose closed elements are the graded [[linear maps]] from $\mathcal{W}^\bullet$ to the [[cochain cohomology]] $H^\bullet(GraphCplx)$ of the [[knot graph complex]]:

\[
  \label{TensorCochainsAsMaps}
  H^0
  \big( 
    \mathcal{A}_\bullet
    \otimes 
    \mathcal{G}^\bullet
  \big)
  \;\simeq\;
  Hom
  \big(
    \mathcal{W}^\bullet
    ,
    H^\bullet(\mathcal{G})
  \big)
\]





## Statement
  {#Statement}

+-- {: .num_prop}
###### Proposition

The element

\[
  \label{WisonLoopObservable}
    \left\langle
      Tr_{(-)}
      \text{P}\exp
      \left(
        \int_{(-)} A
      \right)
    \right\rangle    
    \;\coloneqq\;
    \underset{
      n \in \mathbb{N}
    }{\sum}
      \hbar^n
    \underset{
     \Gamma \in \mathcal{D}^{cs}_n 
    }{\sum}
    \left(
      \frac{1}{\left\vert \Gamma\right\vert}
      \,
      [\Gamma]_{\mathcal{A}} \otimes [\Gamma]_{\mathcal{G}}
    \right)
   \;
    \in
    \;\;
    \mathcal{A}_\bullet \otimes \mathcal{G}^\bullet
\]

(hence the [[sum]] over [[Feynman diagrams]] (eq:CSFeynmanDiagrams) of the [[tensor product of chain complexes|tensor product]] of their [[images]] (eq:LinearizationMaps) in [[Jacobi diagrams]] [[quotient vector space|modulo]] the [[STU-relations]] (eq:JacobiDiagramsModuloSTU) and in the [[knot graph complex]] (eq:KnotGraphComplex), respectively, weighted by the inverse [[order of a group|order]] of their [[automorphism group]] (eq:AutomorphismGroup) )

is closed

$$
  d_{\mathcal{G}} 
  \left\langle
      Tr_{(-)}
    \text{P}\exp
      \left(
        \int_{(-)} A
      \right)
    \right\rangle    
   \;=\; 
   0
$$

=--

This is [AF 96, Theorem 1](#AF96).

Hence (eq:WisonLoopObservable) defines a [[cochain cohomology]]-[[cohomology  class|class]]

$$
  \begin{aligned}
    \left\langle
      Tr_{(-)}
      \text{P}\exp
      \left(
        \int_{(-)} A
      \right)
    \right\rangle    
    \;\coloneqq\;
    H^0
    \big( 
       \mathcal{A}_\bullet \otimes \mathcal{G}^\bullet
    \big) 
    \\
    & 
    \;\simeq\;
    Hom
    \big(
      \mathcal{W}^\bullet
      ,
      H^\bullet(\mathcal{G})
    \big)
  \end{aligned}
$$

and hence, by (eq:TensorCochainsAsMaps), it defines a graded [[linear function]]

$$
  \mathcal{W}^\bullet
  \overset{
    \left\langle
      Tr_{(-)}
      \text{P}\exp
      \left(
        \int_{(-)} A
      \right)
    \right\rangle
  }{
    \longrightarrow  }
  H^\bullet(\mathcal{G})_3
  \hookrightarrow
  H^\bullet(\mathcal{G})
$$

from [[weight systems]] on [[Jacobi diagrams]] ([[chord diagrams modulo 4T are Jacobi diagrams modulo STU|equivalently]] on [[round chord diagrams]]) to the [[cochain cohomology]] of the framed [[knot graph complex]] spanned by trivalent graphs.

According to [CCRL 02, Prop. 7.6](#CattaneoCottaRamusinoLongoni02) this map is a [[bijection]].

To see this, use 1) [AF 96, Theorem 5, Condition U2](#AF96) to find that the map is an [[injection]], and 2) the fact that [[weight systems are associated graded of Vassiliev invariants]].






## Related concepts

* [[weight systems are cohomology of knot graph complex]]


## References

### General

Textbook account

* {#Lescop20} [[Christine Lescop]], _Invariants of links and 3-manifolds from graph configurations_ ([arXiv:2001.09929](https://arxiv.org/abs/2001.09929))


Original articles:

* {#Kontsevich93} Theorem 2.3 of: [[Maxim Kontsevich]], _Vassiliev's knot invariants_, Advances in Soviet Mathematics, Volume 16, Part 2, 1993 ([pdf](http://pagesperso.ihes.fr/~maxim/TEXTS/VassilievKnot.pdf))


* [[Le Tu Quoc Thang]], [[Jun Murakami]], _The universal Vassiliev-Kontsevich invariant for framed oriented links_, Compositio Math. 102 (1996), 42–64 ([arXiv:hep-th/9401016](https://arxiv.org/abs/hep-th/9401016))

* {#BarNatan95} [[Dror Bar-Natan]], 4.4.2 of: _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))


* [[Le Tu Quoc Thang]], [[Jun Murakami]], _Representation of the category of tangles by Kontsevich's iterated integral_,  Comm. Math. Phys., Volume 168, Number 3 (1995), 535-562. ([euclid.cmp/1104272488](https://projecteuclid.org/euclid.cmp/1104272488))


* Daniel Altschuler, Laurent Freidel, _On Universal Vassiliev Invariants_, Commun. Math. Phys. 170 (1995) 41-62 ([arXivhep-th/9403053](https://arxiv.org/abs/hep-th/9403053))


* {#AF96} Daniel Altschuler, Laurent Freidel, Theorem 5 of: _Vassiliev knot invariants and Chern-Simons perturbation theory to all orders_, Commun. Math. Phys. 187 (1997) 261-287 ([arXiv:q-alg/9603010](https://arxiv.org/abs/q-alg/9603010))

* [[Le Tu Quoc Thang]], [[Jun Murakami]], Tomotada Ohtsuki, _On a universal perturbative invariant of 3-manifolds_, Topology Volume 37, Issue 3, May 1998, Pages 539-574 (<a href="https://doi.org/10.1016/S0040-9383(97)00035-9">https://doi.org/10.1016/S0040-9383(97)00035-9</a>)

Review:

* {#BarNatanStoimenow97} [[Dror Bar-Natan]], Alexander Stoimenow, _The Fundamental Theorem of Vassiliev Invariants_ ([arXiv:q-alg/9702009](https://arxiv.org/abs/q-alg/9702009))

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Section 8.8 of: _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))

* [[David Jackson]], [[Iain Moffat]], Section 18 of: _An Introduction to Quantum and Vassiliev Knot Invariants_, Springer 2019 ([doi:10.1007/978-3-030-05213-3](https://link.springer.com/book/10.1007/978-3-030-05213-3))

### Comparison

Comparison between the two main [[universal Vassiliev invariants]]: the [[Kontsevich integral]] and the [[Wilson loop observable]] of [[perturbative quantization of 3d Chern-Simons theory|perturbatively quantized]] [[Chern-Simons theory]]:

* {#Lescop02} [[Christine Lescop]], _On configuration space integrals for links_, Geom. Topol. Monogr. 4 (2002) 183-199 ([arXiv:math/0211062](https://arxiv.org/abs/math/0211062))

### Special values

Computation of the [[perturbative quantization of 3d Chern-Simons theory|perturbative Chern-Simons]]  [[Wilson loop observable]] ([[universal Vassiliev invariant]]) of the [[unknot]] ("[[Wheels theorem]]"):

* [[Dror Bar-Natan]], [[Le Tu Quoc Thang]], [[Dylan Thurston]], _Two applications of elementary knot theory to Lie algebras and Vassiliev invariants_, Geom. Topol. Volume 7, Number 1 (2003), 1-31 ([euclid.gt/1513883092](https://projecteuclid.org/euclid.gt/1513883092))

following

* {#BNGRT97} [[Dror Bar-Natan]], [[Stavros Garoufalidis]], [[Lev Rozansky]], [[Dylan Thurston]], _Wheels, wheeling, and the Kontsevich integral of  the unknot_ ([q-alg/9703025](http://arxiv.org/abs/q-alg/9703025))




[[!redirects universal Vassiliev invariants]]

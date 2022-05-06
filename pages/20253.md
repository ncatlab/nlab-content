
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[manifold]] of [[dimension]] 8.

## Properties

### Signature
 {#Signature}

Let $X$ be a [[compact topological space|compact]] [[orientation|oriented]] [[smooth manifold|smooth]] [[8-manifold]]. Then its [[signature genus|signature]] is related to the [[second  Pontryagin class]] $p_2$ and the [[cup product]] of the [[first Pontryagin class]] $p_1$ with itself, both evaluated on the [[fundamental class]] of $X$, by

\[
  \label{SignatureFormula}
  \pm 1
  \;=\;
  \sigma[X]
  \;=\;
  \tfrac{1}{45}
  \big(
    7 p_2
    -
    (p_1)^2
  \big)[X]
  \,.
\]

But in addition, due to the dimenion 8, the signature is $\pm 1$, depending on the choice of [[orientation]].

(e.g. [Joachim-Wraith, p. 2](#JoachimWraith))

### G-Structures on 8-Manifolds
 {#GStructuresOn8Manifolds}

We state results on [[cohomology|cohomological]] [[obstructions]] to and characterization of various [[G-structures]] on [[closed manifold|closed]] [[8-manifolds]].

+-- {: .num_prop #Spin5StructureOnConnected8Manifolds}
###### Proposition
**([[Spin(5)]]-[[G-structure|structure]] on [[8-manifolds]])**

Let $X$ be a [[closed manifold|closed]] [[connected topological space|connected]] [[8-manifold]]. Then $X$ has [[G-structure]] for $G =$ [[Spin(5)]] if and only if the following conditions are satisfied:

1. The second and sixth [[Stiefel-Whitney classes]] (of the [[tangent bundle]]) vanish

   $$
     w_2 \;=\; 0 
     \,,
     \phantom{AAA}
     w_6 \;=\; 0
   $$

1. The [[Euler class]] $\chi$ (of the [[tangent bundle]]) evaluated on $X$ (hence the [[Euler characteristic]] of $X$) is proportional to [[I8]] evaluated on $X$:

   $$
     \begin{aligned}
       8 \chi[X]
       &=
       192 \cdot I_8[X]
       \\
       & = 
       4 
       \Big( 
         p_2 - \tfrac{1}{2}\big(p_1\big)^2
       \Big)[X]
     \end{aligned}
   $$

1. The [[Euler characteristic]] is divisible by 4:

   $$
     \tfrac{1}{4}\chi[X] \;\in\; \mathbb{Z}
     \,.
   $$

=--

([Čadek-Vanžura 97, Corollary 5.5](#CadekVanzura97))

\linebreak

+-- {: .num_prop #Spin4StructureOnClosed8dSpinManifolds}
###### Proposition
**([[Spin(4)]]-[[G-structure|structure]] on [[8-manifolds]])**

Let $X$ be a [[closed manifold|closed]] [[connected topological space|connected]] [[spin structure|spin]] [[8-manifold]]. Then $X$ has [[G-structure]] for $G =$ [[Spin(4)]] 

\[
  \label{Spin4Structure}
  \array{
    && 
    B Spin(4)
    \\
    & 
      {}^{\mathllap{ \widehat{T X} }}
      \nearrow
    &
    \big\downarrow
    \\
    X 
    &
    \underset{T X}{\longrightarrow}
    &
    B Spin(8)
  }
\]

if and only if the following conditions are satisfied:

1. the sixth [[Stiefel-Whitney class]] of the [[tangent bundle]] vanishes

   $$
     w_6(T X) \;=\; 0
   $$

1. the [[Euler class]] of the [[tangent bundle]] vanishes 

   $$
     \chi_8(T X)
     \;=\;
     0
   $$

1. the [[I8]]-term evaluated on $X$ is divisible as:

   $$
    \tfrac{1}{32}
     \Big(
        p_2 
        - 
        \big(
          \tfrac{1}{2}
          \big(
            p_1
          \big)^2
        \big) 
     \Big)
     \;\in\;
     \mathbb{Z}
   $$

1. there [[existential quantifier|exists]] an [[integer]] $k \in \mathbb{Z}$ such that

   1. $p_2 = (2k - 1)^2 \left( \tfrac{1}{2} p_1 \right)^2$;

   1. $\tfrac{1}{3} k (k+2) p_2[X] \;\in\; \mathbb{Z}$.


Moreover, in this case we have for $\widehat{T X}$ a given [[Spin(4)]]-[[G-structure|structure]] as in (eq:Spin4Structure) and setting

\[
  \label{TildeG4}
  \widetilde G_4
  \;\coloneqq\;
  \tfrac{1}{2}
  \chi_4(\widehat{T X}) 
   + 
  \tfrac{1}{4}p_1(T X)
\]

for $\chi_4$ the [[Euler class]] on $B Spin(4)$ (which is an integral class, by [this Prop.](Spin4#IntegralCohomologyOfClassifyingSpace))

the following relations:

1. $\tilde G_4$ (eq:TildeG4) is an integer multiple of the [[first fractional Pontryagin class]] by the factor $k$ from above:

   $$
     \widetilde G_4
     \;=\;
     k \cdot \tfrac{1}{2}p_1
   $$

1. The (mod-2 reduction followed by) the [[Steenrod operation]] $Sq^2$ on $\widetilde G_4$ (eq:TildeG4) vanishes:

   $$
     Sq^2
     \left(
       \widetilde G_4
     \right)
     \;=\;
     0
   $$

1. the shifted square of $\tilde G_4$ (eq:TildeG4) evaluated on $X$ is a multiple of 8:

   $$
     \tfrac{1}{8}
     \left(
       \left( 
         \widetilde G_4
       \right)^2
       -
       \widetilde G_4 \big( \tfrac{1}{2} p_1\big)[X]  
     \right)
     \;\in\;
     \mathbb{Z}
   $$


1. The [[I8]]-term is related to the shifted square of $\widetilde G_4$ by

   $$
    4
    \Big(
      \left(
         \widetilde G_4
       \right)^2
       -
       \widetilde G_4 
       \left( 
         \tfrac{1}{2}p_1
       \right)
     \Big)
     \;=\;
     \Big(
       p_2 
       - 
       \big(
         \tfrac{1}{2}p_1
       \big)^2
     \Big)
   $$

=--

([Čadek-Vanžura 98a, Cor. 4.2 with Cor. 4.3](#CadekVanzura98a))

\linebreak

## Examples

### With exotic boundary 7-spheres
 {#ExoticBoundary7Spheres}

Consider $S^4$ the [[4-sphere]] and let $D^4$ denote the 4-[[disk]] regarded as a [[manifold with boundary]]. Then a $D^4$-[[fiber bundle]] over $S^4$ is an 8-dimensional [[manifold with boundary]]. 

By the [[clutching construction]], such bundles are classified by [[homotopy classes]] of maps

$$
  f_{(m,n)}
  \;\colon\;
  S^3 
  \longrightarrow
  SO(4)
$$

from a [[3-sphere]] (the [[equator]] of $S^4$) to [[SO(4)]]. By [this Prop.](SO4#TheExceptionalIso) such maps are classified by [[pairs]] of [[integers]] $(m,n) \in \mathbb{Z} \times \mathbb{Z}$.

If here $m+n = \pm 1$ then the [[boundary]] of the corresponding [[8-manifold]] is [[homotopy equivalent]] to a [[7-sphere]], and in fact [[homeomorphism|homeomorphic]] to the [[7-sphere]].

Assuming this 8-manifold is a [[smooth manifold]], then plugging in the numbers into the [[signature genus|signature]] formula (eq:SignatureFormula) yields the relation

$$
  p_2[X]
  \;\coloneqq\;
  \tfrac{1}{7}
  \big(
    4(2m -1)^2 + 45
  \big)
$$

Here the left hand side must be an [[integer]], while the right hand side is not an integer for all choices of [[pairs]] $(m,n)$. This means that for these choices the [[boundary]] [[7-sphere]] is not [[diffeomorphism|diffeomorphic]] to the standard smooth 7-sphere -- it is instead an [[exotic 7-sphere]].

(see [Joachim-Wraith, p. 2-3](#JoachimWraith))

From the point of view of [[M-theory on 8-manifolds]], these [[8-manifolds]] $X$ with (exotic) [[7-sphere]] [[boundaries]] correspond to [[near horizon limits]] of [[black brane|black]] [[M2 brane]] spacetimes $\mathbb{R}^{2,1} \times X$, where the [[M2-branes]] themselves would be sitting at the center of the [[7-spheres]] (if that were included in the spacetime, see also [[Dirac charge quantization]]).

([Morrison-Plesser 99, section 3.2](#MorrisonPlesser99))

\linebreak



## Related concepts

* [[M-theory on 8-manifolds]]

* [[Cayley 4-form]]

[[!include low dimensional manifolds -- table]]

## References

### General

* Anand Dessai, _Topology of positively curved 8-dimensional manifolds with symmetry_ ([arXiv:0811.1034](https://arxiv.org/abs/0811.1034))

### $G$-Structure

* {#CadekVanzura95} [[Martin Čadek]], [[Jiří Vanžura]], _On the existence of 2-fields in 8-dimensional vector bundles over 8-complexes_, Commentationes Mathematicae Universitatis Carolinae, vol. 36 (1995), issue 2, pp. 377-394 ([dml-cz:118764](https://dml.cz/handle/10338.dmlcz/118764))

* {#CadekVanzura97} [[Martin Čadek]], [[Jiří Vanžura]], _On $Sp(2)$ and $Sp(2) \cdot Sp(1)$-structures  in 8-dimensional vector bundles_, Publicacions Matemàtiques Vol. 41, No. 2 (1997), pp. 383-401 ([jstor:43737249](https://www.jstor.org/stable/43737249))

* {#CadekVanzura98a} [[Martin Čadek]], [[Jiří Vanžura]], _On 4-fields and 4-distributions in 8-dimensional vector bundles over 8-complexes_,  Colloquium Mathematicum (1998), 76 (2), pp 213-228 ([web](http://pldml.icm.edu.pl/pldml/element/bwmeta1.element.bwnjournal-article-cmv76z2p213bwm))

* {#CadekVanzura98b} [[Martin Čadek]], [[Jiří Vanžura]], _Almost quaternionic structures on eight-manifolds_, Osaka J. Math. Volume 35, Number 1 (1998), 165-190 ([euclid:1200787905](https://projecteuclid.org/euclid.ojm/1200787905))

* {#CadekVanzura98c} [[Martin Čadek]], [[Jiří Vanžura]], _Various structures in 8-dimensional vector bundles over 8-manifolds_, Banach Center Publications (1998) Volume: 45, Issue: 1, page 183-197 ([dml:208903](https://eudml.org/doc/208903))

* {#CadekCrabbVanzura08} [[Martin Čadek]], Michael Crabb, [[Jiří Vanžura]],  _Obstruction theory on 8-manifolds_, manuscripta math. 127 (2008), 167-186 ([arXiv:0710.0734](https://arxiv.org/abs/0710.0734))

* {#CadekCrabbVanzura10} [[Martin Čadek]], Michael Crabb, [[Jiří Vanžura]], _Quaternionic structures_, Topology and its Applications Volume 157, Issue 18, 1 December (2010), Pages 2850-2863 ([doi:10.1016/j.topol.2010.09.005](https://doi.org/10.1016/j.topol.2010.09.005))

### Exotic boundary 7-spheres

* {#JoachimWraith} [[Michael Joachim]], D. J. Wraith, _Exotic spheres and curvature_ ([pdf](https://ivv5hpp.uni-muenster.de/u/joachim/exo.pdf))

* {#MorrisonPlesser99} [[David Morrison]], [[M. Ronen Plesser]], section 3.2 of _Non-Spherical Horizons, I_, Adv. Theor. Math. Phys.3:1-81, 1999 ([arXiv:hep-th/9810201](https://arxiv.org/abs/hep-th/9810201))

[[!redirects 8-manifolds]]


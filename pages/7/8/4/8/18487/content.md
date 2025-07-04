

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

While the [[symmetric monoidal (∞,1)-category of spectra]] is not a [[cartesian monoidal (∞,1)-category]], hence while the [[smash product of spectra]] does not admit [[diagonal]] morphisms, it turns out that for each [[prime number]] $p$ there is a analogue of the diagonal into  the $p$-fold [[smash product]]. This is the _Tate diagonal_ (def. \ref{TateDiagonal}). One way that this really does behave like a [[diagonal]] map is the construction of the [[Frobenius morphism]] on [[E-∞ rings]] (see [this def.](Frobenius+morphism#EInfinityFrobenius) and [this example](Frobenius+morphism#EInfinityFrobeniusReducesToOrdinaryFrobenius))

## Definition

For $n \in \mathbb{N}$ a [[natural number]], write $C_n \coloneqq \mathbb{Z}/n\mathbb{Z}$ for the [[cyclic group]] of order $n$.

+-- {: .num_defn #TatedSmashProductOfSpectra}
###### Definition

For $X \in Spectra$ a [[spectrum]] and $n$ a [[natural number]], consider the [[Tate spectrum]]

$$
  (X \wedge \cdots \wedge X)^{t C_n} \in Spectra
$$

where the $n$-fold [[smash product of spectra]] is regarded as equipped with the [[∞-action]] by the [[cyclic group]]  given by cyclic [[permutation]] of smash factors. This construction canonically extends to an [[(∞,1)-functor]]

$$
  T_n
    \;\colon\;
  Spectra
    \longrightarrow
  Spectra
$$

on the [[(∞,1)-category of spectra]].


=--

+-- {: .num_prop #SpaceOfTransformationsFromIdentityToTatedSmashProduct}
###### Proposition

For $p$ a [[prime number]], the [[(infinity,1)-category of (infinity,1)-functors|∞-groupoid of natural transformations]]

$$
  id_{spectra} \longrightarrow T_p
$$ 

from the [[identity functor]] on the [[(∞,1)-category of spectra]] to the [[(∞,1)-functor]] $T_p$ from def. \ref{TatedSmashProductOfSpectra} is equivalent to the [[stabilization|underlying space]] of $T_p$ applied to the sphere spectrum:

$$
  Hom( id_{Specta}, T_p )
  \;\simeq\;
  \Omega^\infty T_p(\mathbb{S}) 
    \simeq
   Hom_{Specta}(\mathbb{S}, T_p(\mathbb{S}))
  \,.
$$

([Nikolaus-Scholze 17, corollary III.1.3](#NikolausScholze17))

=--

+-- {: .num_defn #TateDiagonal}
###### Definition

For $p$ a [[prime number]], the _Tate diagonal_ is the [[natural transformation]] 

$$
  \array{
     id_{Specta} &\overset{\Delta_p}{\longrightarrow}& T_p
     \\
     X &\mapsto& (X \wedge \cdots X)^{t C_p}
  }
$$

is the one which under the equivalence of prop. \ref{SpaceOfTransformationsFromIdentityToTatedSmashProduct} corresponds to the [[composition|composite]] morphism

$$
  \mathbb{S}
    \overset{}{\longrightarrow}
  \mathbb{S}^{C_p}
    \overset{}{\longrightarrow}
  \mathbb{S}^{t C_p}
$$

where the first is the [[adjunction unit|unit]] map into the [[homotopy fixed point]] spectrum, and the second is the defining one of the [[Tate spectrum]].

=--

([Nikolaus-Scholze 17, def. III.1.4](#NikolausScholze17))

## References

* {#NikolausScholze17} [[Thomas Nikolaus]], [[Peter Scholze]], _On topological cyclic homology_ ([arXiv:1707.01799](https://arxiv.org/abs/1707.01799))

[[!redirects Tate diagonals]]

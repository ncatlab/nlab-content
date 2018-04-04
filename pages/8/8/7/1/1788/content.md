

+-- {: .num_prop #dgModelForRationalParameterizedSpectra}
###### Proposition
**(dg-model for rational parameterized spectra)**

There is a natural transformation

$$
  Ho_{\mathbb{Q}}( Sp^{\mathbb{N}}_{\mathcal{S}(A)} )
  \overset{\mathcal{M}_{A}}{\longrightarrow}
  Ho( A\text{-}Mod^{op}  )
$$

with the following properties

1. $\mathcal{M}_{\mathbb{Q}}$ is the equivalence of rational stable homotopy theory

1. generally, at least the restriction

   $$
     \array{
       QCoh_{\mathbb{Q}}( Sp^{\mathbb{N}}_{\mathcal{S}(A)} )
       &\hookrightarrow&
       Ho_{\mathbb{Q}}( Sp^{\mathbb{N}}_{\mathcal{S}(A)} )
       \\
       {}^{\simeq}\downarrow &&  \downarrow^{\mathcal{M}_A}
       \\
       Perf(A)^{op}
       &\hookrightarrow&
       Ho( A\text{-}Mod^{op}  )
     }
   $$

   is an equivalence

=--

+-- {: .proof}
###### Proof

The naturality is corollary 2.7.26. The first property follows by inspection (?), the second is theorem 2.7.31.

=--

+-- {: .num_prop #RationalFiberwiseSuspensionSpectrum}
###### Proposition
**(dg-model for fiberwise suspension spectra)**

For

$$
  \left[
  \array{
    Y
    \\
    \downarrow
    \\
    \mathcal{S}(A)
  }
  \right]
  \;\in\;
  Ho_{\mathbb{Q}}( sSet_{\mathcal{S}(A)} )
$$

a map of rational spaces, we have that under the dg-model functor $\mathcal{M}_A$ from prop. \ref{dgModelForRationalParameterizedSpectra}  its fiberwise suspension spectrum is modeled by $\mathcal{O}(Y)$, regarded as an $A$-module:

$$
  \mathcal{M}_A(\Sigma^\infty_{+, \mathcal{S}(A)} Y)
  \simeq
  \mathcal{O}(Y)
$$

=--

+-- {: .proof}
###### Proof

By the diagram in the proof of lemma 2.7.25 we have the following diagram of left Quillen functors, commuting up to natural isomorphism

$$
  \array{
    sSet_{/\mathcal{S}(A)}
      &\overset{(-)_{+_{\mathcal{S}(A)}}}{\longrightarrow}&
    R_{\mathcal{S}(A)}
      &\overset{\Sigma^\infty_{\mathcal{S}(A)}}{\longrightarrow}&
    Sp^{\mathbb{N}}_{\mathcal{S}(A)}
    \\
    {}^{\mathllap{\mathcal{O}_A}}\downarrow
    &&
    {}^{\mathllap{\mathcal{O}_A}}\downarrow
    &&
    {}^{\mathcal{M}_A}\downarrow
    \\
    (DGAlg^{A/})^{op}
    &\underset{}{\longrightarrow}&
    (DGAlg^{A/}_{/A})^{op}
    &\underset{aug_A}{\longrightarrow}&
    A\text{-}Mod^{op}
    \\
    \\
    B &\mapsto& B \oplus A &\mapsto& B
  }
$$

=--

$\,$

$\,$

$\,$

* D. Cremades, [[Luis Ibáñez]], F. Marchesano, _Intersecting brane models of particle physics and the Higgs mechanism_, JHEP, 0207, 022 2002 ([arXiv:hep-th/0203160](https://arxiv.org/abs/hep-th/0203160))
 
[[HiggsVacuumStabilityIII.png:file]]

<img src="https://ncatlab.org/nlab/files/HiggsVacuumStabilityIII.png" width="700">



[[HiggsPotentials.png:file]]

<img src="https://ncatlab.org/nlab/files/HiggsPotentials.png" width="600">


[[HiggsVacuumStability.png:file]]

<img src="https://ncatlab.org/nlab/files/HiggsVacuumStability.png" width="600">

[[HiggsVacuumStabilityII.png:file]]

<img src="https://ncatlab.org/nlab/files/HiggsVacuumStabilityII.png" width="400">




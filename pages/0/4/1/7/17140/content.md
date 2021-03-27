
> under construction

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

Given a [[spectrum]] $X$, and a [[ring spectrum]] $E$, then the _$E$-nilpotent completion_ of $X$ at $E$ is, for any choice $X_\bullet \to X$ of $E$-[[Adams tower]], the [[homotopy limit]] $\underset{\longleftarrow}{\lim} X_\bullet$ over that tower ([Ravenel 84, def. 1.13](#Ravenel84)).

Under certain finiteness conditions (see [below](#RelationToELocalization)), but not generally, this is equivalent to the $E$-[[Bousfield localization of spectra|Bousfield localization]] $L_E X$ (which, in turn, is in special cases given by [[formal completion]], see at _[[fracture theorem]]_).

The $E$-[[Adams spectral sequence]] induced by the given [[Adams tower]] [[conditionally converges]] to the $E$-nilpotent completion.

## Definition

### Bousfield's definition

+-- {: .num_defn #ENilpotentCompletion}
###### Definition

Let $(E, \mu, e)$ be a [[homotopy commutative ring spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-2#HomotopyCommutativeRingSpectrum)) and $Y \in Ho(Spectra)$ any spectrum. Write $\overline{E}$ for the [[homotopy fiber]] of the unit $\mathbb{S}\overset{e}{\to} E$ as in [this def.](Adams+spectral+sequence#HomotopyFiberOfUnitOfCommutativeRingSpectrum) such that the $E$-Adams filtration of $Y$ ([def.](Adams+spectral+sequence#AdamsEAdamsSpectralSequence)) reads (according to [this lemma](Adams+spectral+sequence#Wp))

$$
  \array{
    \vdots
    \\
    \downarrow
    \\
    \overline{E}^3 \wedge Y
    \\
    \downarrow
    \\
    \overline{E}^2 \wedge Y
    \\
    \downarrow
    \\
    \overline{E} \wedge Y
    \\
    \downarrow
    \\
    Y
  }
  \,.
$$

For $n \in \mathbb{N}$, write

$$
  \overline{E}_n 
   \coloneqq
  hocof( \overline{E}^n \overset{i^n}{\longrightarrow} \mathbb{S})
$$

for the homotopy cofiber. Here $\overline{E}_0 \simeq 0$.
By the [[tensor triangulated category|tensor triangulated]] structure of $Ho(Spectra)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+1-2#TensorTriangulatedStructureOnStableHomotopyCategory)), this homotopy cofiber is preserved by forming [[smash product of spectra|smash product]] with $Y$, and so also

$$
  \overline{E}_n \wedge Y
   \simeq
  hocof( \overline{E}^n \wedge Y \overset{}{\longrightarrow} Y)
  \,.
$$

Now let

$$
  \overline{E}_s 
    \overset{p_{s-1}}{\longrightarrow}
  \overline{E}_{s-1}
$$

be the morphism implied by the [[octahedral axiom]] of the [[triangulated category]] $Ho(Spectra)$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#CategoryWithCofiberSequences), [prop.](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyCategoryIsTriangulated)):


$$
  \array{
    \overline{E}^{s+1}
      &\overset{i}{\longrightarrow}&
    \overline{E}^s
      &\longrightarrow&
    E \wedge \overline{E}^s
      &\longrightarrow&
    \Sigma \overline{E}^{s+1}
    \\
    {}^{\mathllap{=}}\downarrow
      &&
    \downarrow^{\mathrlap{i^s}}
      &&
    \downarrow^{}
      &&
    \downarrow
    \\
    \overline{E}^{s+1}
      &\longrightarrow& 
    \mathbb{S}
      &\longrightarrow&
    \overline{E}_s
      &\longrightarrow&
    \Sigma \overline{E}^{s+1}
    \\
    &&
    \downarrow 
      &&
    \downarrow^{\mathrlap{p_{s-1}}}
    \\
      &&
    \overline{E}_{s-1}
      &\overset{=}{\longrightarrow}&
    \overline{E}_{s-1}
    \\
    &&
    \downarrow 
      &&
    \downarrow
    \\
      &&
    \Sigma \overline{E}^s
      &\longrightarrow&
     \Sigma E \wedge \overline{E}^s
  }
  \,.
$$

By the [[commuting square]] in the middle and using again the [[tensor triangulated category|tensor triangulated]] structure, this yields an inverse sequence under $Y$:

$$
  Y   
    \simeq
  \mathbb{S} \wedge Y
    \longrightarrow
  \cdots
    \overset{p_3 \wedge id}{\longrightarrow}
  \overline{E}_3 \wedge Y
    \overset{p_2 \wedge id}{\longrightarrow}
  \overline{E}_2 \wedge Y
    \overset{p_1 \wedge id}{\longrightarrow}
  \overline{E}_1 \wedge Y
$$

The **[[E-nilpotent completion]]** $Y^\wedge_E$ of $Y$ is the [[homotopy limit]] over the resulting inverse sequence

$$
  Y^\wedge_E
    \coloneqq
  \mathbb{R}\underset{\longleftarrow}{\lim}_n \overline{E}_n \wedge Y
$$

or rather the canonical morphism into it

$$
  Y \longrightarrow Y^\wedge_E
  \,.
$$

Concretely, if 

$$
  Y   
    \simeq
  \mathbb{S} \wedge Y
    \longrightarrow
  \cdots
    \overset{p_3 \wedge id}{\longrightarrow}
  \overline{E}_3 \wedge Y
    \overset{p_2 \wedge id}{\longrightarrow}
  \overline{E}_2 \wedge Y
    \overset{p_1 \wedge id}{\longrightarrow}
  \overline{E}_1 \wedge Y
$$

is presented by a tower of fibrations between fibrant spectra in the [[model structure on topological sequential spectra]], then $Y^\wedge_E$ is represented by the ordinary [[sequential limit]] over this tower.


=--

([Bousfield 79, top, middle and bottom of page 272](#Bousfield79))

### As the totalization of the cosimplicial spectrum
 {#AsLimitOverTotTower}

+-- {: .num_defn #RingSpectrumGivesCosimplicialSpectrum}
###### Definition

Given a [[E-infinity ring spectrum]] $E$,  its **corresponding cosimplicial spectrum** is the augmented [[cosimplicial object|cosimplicial spectrum]]

$$
  E^\bullet
   \;\coloneqq\;
  \left(
     \mathbb{S}
       \overset{e}{\longrightarrow}
     E
       \underoverset
         {\underset{id \wedge e}{\longrightarrow}}
         {\overset{e \wedge id}{\longrightarrow}}
         {\overset{\mu}{\longleftarrow}}
     E \wedge E
        \underoverset
          {\underset{e \edge id}{\longrightarrow}}
          {\overset{id \wedge e}{\longrightarrow}}
          {
            \underoverset
              {\underset{id \wedge \mu}{\longleftarrow}}
              {\overset{\mu \wedge id}{\longleftarrow}}
              {\overset{id \wedge e \wedge id}{\longrightarrow}}
          }
      E \wedge E \wedge E
       \cdots
  \right)
  \,.
$$

(This is the [[formal dual]] of the [[Cech nerve]] of $Spec(E) \to Spec(\mathbb{S})$ in the [[opposite category]], where we write $Spec(E)$ for the object $E$ regarded in the opposite category.)

Moreover, for $X \in Ho(Spectra)$ any spectrum, then there is the corresponding augmented cosimiplicial spectrum $E^\bullet \wedge X$.

=--



+-- {: .num_prop #ENilpotentCompletionIsHolimOverTotTower}
###### Proposition

Given an [[E-infinity ring spectrum]] $E$ and any spectrum $X$, then the $E$-nilpotent completion $X^\wedge_E$ (according to def. \ref{ENilpotentCompletion}) is equivalently the homotopy limit 

$$
  \begin{aligned}
     X^\wedge_E 
      &\simeq 
    Tot(E^\bullet \wedge X)
      \\
     & = 
      \underset{\leftarrow}{holim}_{n \in \Delta} (E^n\wedge X)
    \\
      & \simeq 
     \underset{\leftarrow}{holim}_{n \in \mathbb{N}}Tot^n(E^\bullet \wedge X)
  \end{aligned} 
$$

over the tower of homotopy-[[totalizations]] of the skeleta of the [[cosimplicial object|cosimplicial]] spectrum $E^\bullet \otimes Y$ (def. \ref{RingSpectrumGivesCosimplicialSpectrum}).

=--

This claim originates in ([Hopkins 99, remark 5.5 (ii)](#Hopkins99)). It is taken for granted in ([Lurie 10, lecture 8, lecture 30](#Lurie10)). The first published proof is ([Mathew-Naumann-Noel 15, prop. 2.14](#MathewNaumannNoel15)). See also ([Carlsson 07, e.g. remark 3.1](#Carlsson07)).

+-- {: .num_remark}
###### Remark

Prop. \ref{ENilpotentCompletionIsHolimOverTotTower} implies that the $E$-[[Adams spectral sequence]] may equivalently be regarded as computing [[descent]] of [[quasicoherent infinity-stacks]] in [[E-infinity geometry]] along the canonical morphisms $Spec(E)\longrightarrow $ [[Spec(S)]]. See at _[Adams spectral sequence -- As derived descent](https://ncatlab.org/nlab/show/Adams%20spectral%20sequence#DefinitionInHigherAlgebra)_.

=--


## Properties

### Relation to $E$-localization
 {#RelationToELocalization}

+-- {: .num_remark #CanonicalMapFromELocalizationToTotalization}
###### Remark

There is a canonical map

$$
  L_E X 
    \overset{}{\longrightarrow} 
  \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
$$

from the $E$-[[Bousfield localization of spectra]] of $X$ into the [[totalization]].


=--

We consider now conditions for this morphism to be an [[equivalence]].

+-- {: .num_defn #CoreOfARing}
###### Definition

For $R$ a [[ring]], its _core_ $c R$ is the [[equalizer]] in

$$
  c R 
    \longrightarrow 
  R 
    \stackrel{\longrightarrow}{\longrightarrow}
  R \otimes R
  \,.
$$

=--

+-- {: .num_prop #SufficientConditionsForTotalizationToBeELocalization}
###### Proposition

Let $E$ be a [[connective spectrum|connective]] [[E-∞ ring]] such that the core of $\pi_0(E)$, def. \ref{CoreOfARing}, is either of

* the [[localization of a ring|localization]] of the [[integers]] at a set $J$ of [[primes]], $c \pi_0(E) \simeq \mathbb{Z}[J^{-1}]$;

* $\mathbb{Z}_n$ for $n \geq 2$.

Then the map in remark \ref{CanonicalMapFromELocalizationToTotalization} is an equivalence

$$
  L_E X \stackrel{\simeq}{\longrightarrow} 
  \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
  \,.
$$

=--

([Bousfield 79](#Bousfield79)).



## Examples


The nilpotent completion of a [[connective spectrum]] at the [[Eilenberg-MacLane spectrum]] $H \mathbb{Z}$, happens to be the spectrum itself (by a [[Postnikov tower]] argument).

+-- {: .num_example}
###### Examples

For $X$ a [[connective spectrum]], its $H \mathbb{F}_p$-nilpotent completion is the [[formal completion]] $X^{\wedge}_p$.

The [[MU]]-nilpotent completion of any connective spectrum $X$ is $X$.

The [[BP]]-nilpotent completion at prime $p$ of any connective spectrum $X$ is $X_{(p)}$.

=--
 
([Ravenel 84, example 1.16](#Ravenel84))


## Related concepts

* [[formal completion]]

## References

The concept originates with 

* {#Bousfield79} [[Aldridge Bousfield]], _The localization of spectra with respect to homology_, Topology 18 (1979), no. 4, 257--281. ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/bousfield-topology-1979.pdf))


* {#Ravenel84} [[Douglas Ravenel]], _Localization with respect to certain periodic homology theories_, American Journal of Mathematics, Vol. 106, No. 2, (Apr., 1984), pp. 351-414 ([pdf](https://www.math.rochester.edu/people/faculty/doug/mypapers/loc.pdf))

The re-interpretation in terms of totalization of the cosimplicial spectrum is briefly mentioned in

* {#Hopkins99} [[Mike Hopkins]], section 4 of _Complex oriented cohomology theories and the language of stacks_, course notes 1999 ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/coctalos.pdf))

and tacitly assumed in 

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ (2010) lecture 30: _Localizations and the Adams-Novikov Spectral Sequence_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture30.pdf))

A proof of the equivalence of this re-interpretation appears in 

* {#MathewNaumannNoel15} [[Akhil Mathew]], [[Niko Naumann]], [[Justin Noel]], _Nilpotence and descent in equivariant stable homotopy theory_ ([arXiv:1507.06869](http://arxiv.org/abs/1507.06869))

See also

* {#BakerLazarev01} [[Andrew Baker]], [[Andrey Lazarev]], _On the Adams Spectral Sequence for $R$-modules_, Algebr. Geom. Topol. 1 (2001) 173-199 ([arXiv:math/0105079](http://arxiv.org/abs/math/0105079))

* {#Carlsson07} [[Gunnar Carlsson]], _Derived completions in stable homotopy theory_ ([arXiv:0707.2585](http://arxiv.org/abs/0707.2585))

* {#Lawson09} [[Tyler Lawson]], _Completed representation ring spectra of nilpotent groups_, Algebraic & Geometric Topology 6 (2006) 253&#8211;285 ([arXiv:0902.4867](http://arxiv.org/abs/0902.4867))

[[!redirects E-nilpotent completions]]

[[!redirects nilpotent completion]]
[[!redirects nilpotent completions]]

[[!redirects E-nilpotent completion]]

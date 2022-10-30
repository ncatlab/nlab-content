
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The universal [[elliptic cohomology]] [[cohomology theory|cohomology]] called [[tmf]] may be realized (after [[local spectrum|localization]] at some primes) as the [[homotopy fixed points]] of an [[∞-action]] of the [[modular group]] modulo a [[congruence subgroup]] in direct analogy to how [[KO-theory]] arises as the $\mathbb{Z}_2$-homotopy fixed points of [[KU-theory]] ([Mahowald-Rezk 09](#MahowaldRezk09), [Lawson-Naumann 12](#LawsonNaumann12), [Hill-Lawson 13](#HillLawson13)).

### General

The way this works is roughly indicated in the following table:

[[!include moduli stack of curves -- table]]

For [[K-theory]] this relation induces the $\mathbb{Z}_2$-[[equivariant cohomology]]-version of [[KU]] which is [[KR-theory]]. In direct analogy to this one may hence consider $SL_2(\mathbb{Z}/n\mathbb{Z})$-equivariant versions of [[tmf]] (localized at some primes). This maybe deserves to be called _modular equivariant elliptic cohomology_. 

This hasn't been studied much yet (or not at all), but there is some motivation for this from [[string theory]] (see [below](#MotivationFromStringTheory)) and in this context a relevance of modular equivariant elliptic cohomology theory has been conjectured in ([Kriz-Sati 05](#KrizSati05)).


### Motivation from string theory
 {#MotivationFromStringTheory}

A relevant role of some modular equivariant elliptic cohomology theory in [[string theory]] has been conjectured in ([Kriz-Sati 05](#KrizSati05)):

First of all, $\mathbb{Z}_2$-equivariant [[topological K-theory]], hence [[KR-theory]], is what controls the [[D-brane charges]] in general [[orientifold]] [[vacua]] of [[type II superstring theory]] (hence also of [[type I superstring theory]], which is thereby a special case). 

Next, there are various hints ([Kriz-Sati 04a](#KrizSati04a), [Kriz-Sati 04b](#KrizSati04b) [Kriz-Sati 05](#KrizSati05), [Sati 05](#Sati05)) that lifting [[string theory]] to "[[M-theory]]" involves replacing K-theory by [[elliptic cohomology]]. Not the least of these is the [[String orientation of tmf]] ([Ando-Hopkins-Strickland 01](#AndoHopkinsStrickland01), [Ando-Hopkins-Rezk 10](#AndoHopkinsRezk10)), which shows that where the [[partition function]] of a [[superparticle]] (such as that at the end of the [[type II superstring]] ending on a [[D-brane]]) is give by the [[Todd genus]] in [[KU-theory]], so the partition function of the [[superstring]] itself (possibly itself being the boundary of the [[M2-brane]] ending on a [[O9 plane]] ([[heterotic string]]) or on an [[M5-brane]] (self-dual "M-string")) is given by the refined [[Witten genus]] in [[elliptic cohomology]]/[[tmf]] (thus yielding "O9-plane charge" and [[M5-brane charge]] in 
[[elliptic cohomology]] ([Sati 10](#Sati10))).

Finally, the [[M-theory]]-lift of [[type II string theory]] is (or is naturally identified as) _[[F-theory]]_, which describes the [[axio-dilaton]] of the type II string [[vacua]] including the [[modular group|modular]] [[S-duality]]/[[U-duality]] acting on this as an [[elliptic fibration]] over [[spacetime]] (whose [[monodromy]] "homology invariant" is hence an $SL_2(\mathbb{Z})$-[[local system]]). It is hence natural to suspect that the combined [[worldsheet]]/[[target space]] $\mathbb{Z}_2$-equivariance of [[orientifold]] [[type II superstring]] backgrounds which is captured by [[KR-theory]] lifts in [[F-theory]] to some combined worldsheet/target space [[modular group]]-action. This is excatly what would be captured by modular invariant $tmf$ as indicated above, and and it is what is conjectured in ([Kriz-Sati 05](#KrizSati05)).


## Definition
 {#Definition}

Write $\hat {\mathbb{Z}}$ for the [[profinite completion of the integers]].

Write 

$$
  G \coloneqq SL_2(\hat {\mathbb{Z}})
$$

for the [[special linear group]] in [[dimension]] 2 with [[coefficients]] in $\hat{\mathbb{Z}}$.

Write

$$
  p \;\colon\; SL_2(\mathbb{Z}) \longrightarrow G
$$

for the canonical projection from (the $\mathbb{Z}_2$-[[central extension]] $SL_2(\mathbb{Z}) \to PSL_2(\mathbb{Z})$ of) the [[modular group]].

For $n \in \mathbb{N}$ any [[natural number]] write

$$
  p_n \;\colon\; G \longrightarrow SL_2(\mathbb{Z}/n\mathbb{Z})
$$

for the corresponding [[projection]] to [[coefficients]] in the [[cyclic group]] of [[order of a group|order]] $n$.

Notice that for $\Gamma \hookrightarrow SL_2(\mathbb{Z}/n\mathbb{Z})$ then its [[preimage]] under $p_n$ is a "profinite [[congruence subgroup]]".

The following is a variant of the [[orbit category]] of $G$ which remembers the stage $n$ and consists only of orbits of the form of such [[congruence subgroups]].

+-- {: .num_defn #LevelledOrbitCategory}
###### Definition

Write $\widetilde{Orb}_{SL_2(\hat{\mathbb{Z}})}$
for the [[category]] whose

* [[objects]] are [[pairs]] $(n,\Gamma)$ with $n \in \mathbb{N}$ a [[natural number]] and $\Gamma \hookrightarrow SL_2(\mathbb{Z}/n\mathbb{Z})$ a [[subgroup]];

* [[morphisms]] are  given by

  $$
    Hom((n_1,\Gamma_1), (n_2,\Gamma_2))
    \coloneqq
    \left\{
      \array{
        Hom_G(G/(p_{n_1}^{-1}(\Gamma_1)), G/(p_{n_2}^{-1}(\Gamma_2)))
        & if \; n'|n
        \\
        \emptyset & otherwise
      }
    \right.
    \,.
  $$

=--

This is ([Hill-Lawson 13, def. 3.15](#HillLawson13)).

+-- {: .num_theorem #TheEquivariantConstruction}
###### Theorem 

It is possible to apply a [[Goerss-Hopkins-Miller theorem]] to the [[Deligne-Mumford compactification|compactified]] [[moduli stacks]] of [[elliptic curves with level-n structure]] $\mathcal{M}_{\overline{ell}}[n]$ after [[localization of a spectrum|localization]] at $n$, such that taking [[global sections]] produces a [[functor]]

$$
  Tmf
  \;\colon\;
  \widetilde{Orb}_{SL_2(\hat{\mathbb{Z}})}
  \longrightarrow
  CRing_\infty
$$

from the "levelled [[orbit category]]" of def. \ref{LevelledOrbitCategory}
to [[E-∞ rings]] which is such that

1. $Tmf(1)\simeq $ [[Tmf]];

1. for every [[normal subgroup]]  $K \hookrightarrow \Gamma$ there is an [[equivalence]]

   $$
     Tmf(K)  \simeq Tmf(\Gamma)^{(\Gamma/K)} 
   $$

   between the value on $K$ and the $\Gamma/K$-[[homotopy fixed points]] of the value on $\Gamma$.

=--

This is part of ([Hill-Lawson 13, theorem 9.1](#HillLawson13)).

+-- {: .num_remark}
###### Remark

For each $n\in \mathbb{N}$ theorem \ref{TheEquivariantConstruction} gives a genuine $SL_2(\mathbb{Z}/n\mathbb{Z})$-[[equivariant cohomology]] refinement of [[Tmf]]$[\frac{1}{n}]$.
In total $Tmf(-)$ defines a "levelled" kind of genuine $SL_2(\hat {\mathbb{Z}})$-[[equivariant cohomology]] version of [[Tmf]].

=--

## Related concepts

* related but different: [[equivariant elliptic cohomology]]
 
## References

* {#MahowaldRezk09} [[Mark Mahowald]] [[Charles Rezk]], _Topological modular forms of level 3_, Pure Appl. Math. Quar. 5 (2009) 853-872 ([pdf](http://www.math.uiuc.edu/~rezk/tmf3-paper-final.pdf))

* {#LawsonNaumann12} [[Tyler Lawson]], [[Niko Naumann]], _Strictly commutative realizations of diagrams over the Steenrod algebra and topological modular forms at the prime 2_, Int. Math.
Res. Not. (2013) ([arXiv:1203.1696](http://arxiv.org/abs/1203.1696))

* {#HillLawson13} [[Michael Hill]], [[Tyler Lawson]], _Topological modular forms with level structure_ ([arXiv:1312.7394](http://arxiv.org/abs/1312.7394))

* {#AndoHopkinsStrickland01} [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], _Elliptic spectra, the Witten genus and the theorem of the cube_, Invent. Math. 146 (2001) 595&#8211;687 MR1869850

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))


* {#KrizSati04a} [[Igor Kriz]], [[Hisham Sati]], _M Theory, Type IIA Superstrings, and Elliptic Cohomology_, Adv.Theor.Math.Phys. 8 (2004) 345-395 ([arXiv:hep-th/0404013](http://arxiv.org/abs/hep-th/0404013))

* {#KrizSati04b} [[Igor Kriz]], [[Hisham Sati]], _Type IIB String Theory, S-Duality, and Generalized Cohomology_, Nucl.Phys. B715 (2005) 639-664 ([arXiv:hep-th/0410293](http://arxiv.org/abs/hep-th/0410293))

* {#KrizSati05} [[Igor Kriz]], [[Hisham Sati]], _Type II string theory and modularity_, 	JHEP 0508 (2005) 038 ([arXiv:hep-th/0501060](http://arxiv.org/abs/hep-th/0501060))

* {#Sati05} [[Hisham Sati]], _The Elliptic curves in gauge theory, string theory, and cohomology_, JHEP 0603 (2006) 096 ([arXiv:hep-th/0511087](http://arxiv.org/abs/hep-th/0511087))

* {#Sati10} [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]]_ , part I, Proc. Symp. Pure Math. 81 (2010), 181-236 [arXiv:1001.5020](http://arxiv.org/abs/1001.5020),
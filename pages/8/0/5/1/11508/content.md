
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

The universal [[elliptic cohomology]] [[cohomology theory|cohomology]] called [[tmf]] may be realized (after [[local spectrum|localization]] at some primes) as the [[homotopy fixed points]] of an [[∞-action]] of the [[modular group]] modulo a [[congruence subgroup]] in direct analogy to how [[KO-theory]] arises as the $\mathbb{Z}_2$-homotopy fixed points of [[KU-theory]] ([Mahowald-Rezk 09](#MahowaldRezk09), [Lawson-Naumann 12](#LawsonNaumann12)). This construction extends to equip [[tmf]] [[level structure on an elliptic curve|for level structure]] with -- almost -- the structure of a [[naive G-spectrum]] (hence a [[Bredon cohomology|Bredon equivariant cohomology theory]]) for pieces of the [[modular group]] ([Hill-Lawson 13, theorem 9.1](#HillLawson13)).

### General
  {#General}

The way this works is roughly indicated in the following table ([Lawson-Naumann 12](#LawsonNaumann12), [Hill-Lawson 13](#HillLawson13)):

[[!include moduli stack of curves -- table]]

For [[K-theory]] this relation induces the $\mathbb{Z}_2$-[[equivariant cohomology]]-version of [[KU]] which is [[KR-theory]]. In direct analogy to this one may hence consider $SL_2(\mathbb{Z}/n\mathbb{Z})$-equivariant versions of [[tmf]] (localized at some primes). This maybe deserves to be called _modular equivariant elliptic cohomology_. 

This hasn't been studied much yet (or not at all), but there is some motivation for this from [[string theory]] (see [below](#MotivationFromStringTheory)) and in this context a relevance of modular equivariant elliptic cohomology theory has been conjectured in ([Kriz-Sati 05, p.3, p. 17, 18](#KrizSati05)).


### Motivation from string theory
 {#MotivationFromStringTheory}

A relevant role of some modular equivariant elliptic cohomology theory in [[string theory]] has been conjectured in ([Kriz-Sati 05, p. 3, p. 17, 18](#KrizSati05)):

First of all, $\mathbb{Z}_2$-equivariant [[topological K-theory]], hence [[KR-theory]], is what controls the [[D-brane charges]] in general [[orientifold]] [[vacua]] of [[type II superstring theory]] (hence also of [[type I superstring theory]], which is thereby a special case). 

Next, there are various hints ([Kriz-Sati 04a](#KrizSati04a), [Kriz-Sati 04b](#KrizSati04b) [Kriz-Sati 05](#KrizSati05), [Sati 05](#Sati05)) that lifting [[string theory]] to "[[M-theory]]" involves replacing K-theory by [[elliptic cohomology]]. Not the least of these is the [[String orientation of tmf]] ([Ando-Hopkins-Strickland 01](#AndoHopkinsStrickland01), [Ando-Hopkins-Rezk 10](#AndoHopkinsRezk10)), which shows that where the [[partition function]] of a [[superparticle]] (such as that at the end of the [[type II superstring]] ending on a [[D-brane]]) is given by the [[Todd genus]] in [[KU-theory]], so the partition function of the [[superstring]] itself (possibly itself being the boundary of the [[M2-brane]] ending on a [[O9 plane]] ([[heterotic string]]) or on an [[M5-brane]] (self-dual "M-string")) is given by the refined [[Witten genus]] in [[elliptic cohomology]]/[[tmf]] (thus yielding "O9-plane charge" and [[M5-brane charge]] in 
[[elliptic cohomology]] ([Sati 10](#Sati10))).

[[!include genera and partition functions - table]]

Finally, the [[M-theory]]-lift of [[type II string theory]] is (or is naturally identified as) _[[F-theory]]_, which describes the [[axio-dilaton]] of the type II string [[vacua]] including the [[modular group|modular]] [[S-duality]]/[[U-duality]] acting on this as an [[elliptic fibration]] over [[spacetime]] (whose [[monodromy]] "homology invariant" is hence an $SL_2(\mathbb{Z})$-[[local system]]). It is hence natural to suspect that the combined [[worldsheet]]/[[target space]] $\mathbb{Z}_2$-equivariance of [[orientifold]] [[type II superstring]] backgrounds which is captured by [[KR-theory]] lifts in [[F-theory]] to some combined worldsheet/target space [[modular group]]-action. This is excatly what would be captured by modular [[equivariant cohomology|equivariant]] $tmf$ as indicated above (and as realized by theorem \ref{TheEquivariantConstruction} below), and and it is what is conjectured in ([Kriz-Sati 05, p.3](#KrizSati05)) (there the group $SL_2(\mathbb{Z}/2\mathbb{Z})$ is mentioned, the explicit construction [below](#Definition) does capture this but also includes equivariance under all other $SL_2(\mathbb{Z}/n\mathbb{Z})$).

So by extrapolation from the case of [[orientifolds]], where the [[target space]] $\mathbb{Z}_2$-[[involution]] (the "[[real space]]"-structure) is accompanied by a $\mathbb{Z}_2$-action on the [[worldsheet]] (the [[worldsheet parity operator]]), this would suggest that in modular equivariant F-theory [[S-duality]] operations on the target space background would be accompanied by certain modular action on the worldsheet. 

Mathematically this is precisely what happens in the equivariant version of [[tmf]] established by theorem \ref{TheEquivariantConstruction} below, which by prop. \ref{SystemOfModuliStacks} has the modular group action on the [[spectrum]] induced from the canonical action of the [[modular group]] on moduli of [[elliptic curves]] (hence: [[genus of a surface|genus]]-1 [[worldsheets]]).

Physically such an effect seems not to have been discussed much, but at least the following is knonw: first of all, under [[S-duality]] the [[worldsheet]] theory of the [[type IIB superstring]] certainly is affected: the superstring here is generally a [[(p,q)-string]], being a [[bound state]] of $p$ actual fundamental strings ([[F1-branes]]) with $q$ [[D1-branes]], and the [[S-duality]] [[modular group]] $SL_2(\mathbb{Z})$ does act canonically on these pairs of [[integers]]. Now, that this operation has to be accompanied with a worldsheet [[conformal transformation]] as the above mathematical story would suggest has been highlighted for instance in ([Bandos 00](#Bandos00)).

Generally, notice that the [[elliptic genus]] for [[type II superstrings]] lands in [[modular forms]] for the [[congruence subgroup]] $\Gamma_0(2) \hookrightarrow SL_2(\mathbb{Z})$ inside the full [[modular group]] (see at [Witten genus -- Modularity -- For type II superstring](Witten+genus#ModularityForTypeIISuperstring)), the subgroup which fixes one of the NS-R [[spin structures]]. Therefore if this [[elliptic genus]] does have a "topological" (homotopy theoretic) lift to [[elliptic cohomology]] (as is known for the [[heterotic string]] via the [[string orientation of tmf]]) then not to plain [[TMF]], but to $TMF_0(2) \simeq \Gamma(\mathcal{M}_{ell}(2)_0,\mathcal{O}^{top})$ (this is implified for instance in [Stojanoska 11, remark 6.2](#Stojanoska11)), where $\mathcal{M}_{ell}(2)_0$ is the moduli stack of [[elliptic curves with level structure]] for $\Gamma_0(2)$, see at _[[tmf0(2)]]_.



 

## Definition and construction
 {#Definition}

Write $\hat {\mathbb{Z}}$ for the [[profinite completion of the integers]].

Write 

$$
  G \coloneqq GL_2(\hat {\mathbb{Z}})
$$

for the [[general linear group]] in [[dimension]] 2 with [[coefficients]] in $\hat{\mathbb{Z}}$.

Notice that this is the [[profinite group]] obtained as the [[limit]] over all general linear groups with coefficients in the [[cyclic groups]] (e.g.[Greicius 09, (1.1)](#Greicius09))

$$
  GL_2(\widehat{\mathbb{Z}})
  \coloneqq
  GL_2(\underset{\leftarrow}{\lim})_n GL_2(\mathbb{Z}/n\mathbb{Z})
  \simeq
  \underset{\leftarrow}{\lim}_n GL_2(\mathbb{Z}/n\mathbb{Z})
  \,.
$$

Write

$$
  p \;\colon\; GL_2(\mathbb{Z}) \longrightarrow G
$$

for the canonical projection from (the $\mathbb{Z}_2$-[[central extension]] $GL_2(\mathbb{Z}) \to PSL_2(\mathbb{Z})$ of) the [[modular group]].

For $n \in \mathbb{N}$ any [[natural number]] write

$$
  p_n \;\colon\; G \longrightarrow GL_2(\mathbb{Z}/n\mathbb{Z})
$$

for the corresponding [[projection]] to [[coefficients]] in the [[cyclic group]] of [[order of a group|order]] $n$.

Notice that for $\Gamma \hookrightarrow SL_2(\mathbb{Z}/n\mathbb{Z})$ then its [[preimage]] under $p_n$ is a "profinite [[congruence subgroup]]".

The following is a variant of the [[orbit category]] of $G = GL_2(\hat {\mathbb{Z}})$ which remembers the stage $n$ and consists only of orbits of the form of [[cosets]] by such [[congruence subgroups]].

+-- {: .num_defn #LevelledOrbitCategory}
###### Definition

Write $\widetilde{Orb}_{GL_2(\hat{\mathbb{Z}})}$
for the [[category]] whose

* [[objects]] are [[pairs]] $(n,\Gamma)$ with $n \in \mathbb{N}$ a [[natural number]] and $\Gamma \hookrightarrow GL_2(\mathbb{Z}/n\mathbb{Z})$ a [[subgroup]];

* [[morphisms]] are  given by

  $$
    Hom\left(\left(n_1,\Gamma_1\right), \left(n_2,\Gamma_2\right)\right)
    \coloneqq
    \left\{
      \array{
         Hom_{GL_2\left(\hat{\mathbb{Z}}\right)}
         \left(
            GL_2\left(\hat{\mathbb{Z}}\right)
            /
            p_{n_1}^{-1}\left(\Gamma_1\right), 
            \;
            GL_2\left(\hat{\mathbb{Z}}\right)
            /
            p_{n_2}^{-1}\left(\Gamma_2\right)
          \right)
        & if \; n'|n
        \\
        \emptyset & otherwise
      }
    \right.
    \,.
  $$

=--

This is ([Hill-Lawson 13, def. 3.15](#HillLawson13)).

+-- {: .num_prop #SystemOfModuliStacks}
###### Proposition

The construction for each $(n,\Gamma) \in \widetilde{Orb}_{GL_2(\hat{\mathbb{Z}})}$ of the [[Deligne-Mumford compactification|compactified]] [[moduli stack]] $\mathcal{M}_{\overline{ell}}(\Gamma)$ over $Spec(\mathbb{Z}[\frac{1}{n}])$ of [[elliptic curves with level structure]] determined by $\Gamma$ (a [[modular curve]]) extends to a (lax) [[2-functor]] 

$$
  \mathcal{M}_{\overline{ell}}(-)
  \;\colon\;
  \widetilde{Orb}_{GL_2(\hat{\mathbb{Z}})}
  \longrightarrow
  DMStack
$$

from the levelled orbit category of def. \ref{LevelledOrbitCategory} to the [[2-category]] of [[Deligne-Mumford stacks]], such that 

1.  $\mathcal{M}_{\overline{ell}}(1,1) \simeq \mathcal{M}_{\overline{ell}}$ is the standard compactified [[moduli stack of elliptic curves]] over $Spec(\mathbb{Z})$

1. for each morphism $(n_1,\Gamma_1)\to (n_2,\Gamma_2)$ the induced morphism 

   $$
     \mathcal{M}_{\overline{ell}}(n_1,\Gamma_1)\to \mathcal{M}_{\overline{ell}}(n_2,\Gamma_2)
   $$ 

   is a [[log-etale morphism]] [[covering]];

1. for each $n$ and each [[normal subgroup]] inclusion $K \hookrightarrow \Gamma \hookrightarrow GL_2(\mathbb{Z}/n\mathbb{Z})$ the induced map exhibits the [[homotopy quotient]] [[projection]] by $\Gamma/K$

   $$
     \mathcal{M}_{\overline{ell}}(n,K)\to \mathcal{M}_{\overline{ell}}(n,\Gamma)
     \simeq 
     \mathcal{M}_{\overline{ell}}(n,K)//(\Gamma/K)
     \,.
   $$ 


=--

This is ([Hill-Lawson 13, prop. 3.16, prop. 3.17](#HillLawson13)).


+-- {: .num_theorem #TheEquivariantConstruction}
###### Theorem 

It is possible to extend the [[Goerss-Hopkins-Miller theorem]] to the [[Deligne-Mumford compactification|compactified]] [[moduli stacks]] of [[elliptic curves with level-n structure]] $\mathcal{M}_{\overline{ell}}[n]$ in prop. \ref{SystemOfModuliStacks}, such that taking [[global sections]] produces an [[(∞,1)-presheaf]] on the levelled [[orbit category]] of def. \ref{LevelledOrbitCategory} with values in [[E-∞ rings]] 

$$
  Tmf
  \;\colon\;
  (\widetilde{Orb}_{SL_2(\hat{\mathbb{Z}})})^{op}
  \longrightarrow
  CRing_\infty
$$
which is such that

1. for $n = 1$ (where $SL_2(\mathbb{Z}/\mathbb{Z}) = 1$ and hence $\Gamma = 1$ necessarily) one recovers 

   $Tmf(1,1)\simeq $ [[Tmf]];

1. the morphism induced by any morphism of the form $(n k ,P_k(\Gamma))\to (n,\Gamma)$ is $k$-[[localization of a spectrum|localization]];

1. for any $n \in \mathbb{N}$ and every [[normal subgroup]]  $K \hookrightarrow \Gamma \hookrightarrow GL_2(\mathbb{Z}/n\mathbb{Z})$, we have the $(\Gamma/K)$-[[homotopy fixed points]] of $Tmf(n,\Gamma)$ (induced by action of $\Gamma/K$ on $\mathcal{M}_{\overline{ell}}(\Gamma)$ given by prop. \ref{SystemOfModuliStacks}): 

   $$
     Tmf(n,\Gamma) \stackrel{\simeq}{\longrightarrow} Tmf(K)^{(\Gamma/K)}      \,.
   $$


=--

This is ([Hill-Lawson 13, theorem 9.1](#HillLawson13)).

+-- {: .num_remark}
###### Remark

The system of spectra in theorem \ref{TheEquivariantConstruction} is essentially a [[spectrum with G-action]] (see there) for $G$ the "[[profinite completion of the integers|profinite]] [[modular group]]" $GL_2(\hat {\mathbb{Z}})$, except that the parameterization is not quite over the [[orbit category]] of this $G$, but just to the subcategory on objects which are [[coset spaces]] just by [[congruence subgroups]] and subject to that divisibility constraint on the $n$s, the "levelling".
So $Tmf(-)$ defines a "levelled" kind of genuine $GL_2(\hat {\mathbb{Z}})$-[[equivariant cohomology]] version of [[Tmf]].

=--

The following proposition gives one way how the modular equivariance of [[tmf]] as in theorem \ref{TheEquivariantConstruction}  restricts to the $\mathbb{Z}_2$-equivariance of [[KU]] (hence [[KR-theory]], which is known to be the precise form of [[type II string theory]] [[orientifolds]]).

First observe (see also ([Mahowald-Rezk 09, section 2](#MahowaldRezk09))) that for [[elliptic curve with level structure|level 3 structure]] we have [[congruence subgroups]]

$$
  \Gamma_1(3) \hookrightarrow \Gamma_0(3) \hookrightarrow GL(2,\mathbb{Z}/3\mathbb{Z})
$$

where the first inclusion is a [[normal subgroup]] of [[index of a subgroup|index]] 2.

+-- {: .num_prop}
###### Proposition

The inclusion of the [[nodal cubic|nodal elliptic curve]] with its $\mathbb{Z}/2\mathbb{Z}$-worth of [[automorphisms]] (the [[inversion involution]]) as the [[cusp]] of the [[Deligne-Mumford compactification|compactified]] [[moduli stack of elliptic curves]]

$$
  \array{
    \ast &\to& \mathcal{M}_{\overline{ell}}(3,\Gamma_1)
    \\
    \downarrow^{\mathrlap{\mathbb{Z}/2\mathbb{Z}}}
    &&
    \downarrow^{\mathbb{Z}/2\mathbb{Z}}
    \\
    \ast//(\mathbb{Z}/2\mathbb{Z})
    &\hookrightarrow&
    \mathcal{M}_{\overline{ell}}(3,\Gamma_0)
  }
$$

over $Spec(\mathbb{Z}[\tfrac{1}{3}])$ yields under theorem \ref{TheEquivariantConstruction} a diagram of the form

$$
  \array{
    ku[\frac{1}{3}] &\leftarrow& tmf_1(3)
    \\
    \uparrow && \uparrow
    \\
    ko[\frac{1}{3}] &\leftarrow& tmf_0(3)
  }
  \,.
$$

=--

([Hill-Lawson 13, theorem 9.3](#HillLawson13))

+-- {: .num_remark}
###### Remark

The spectrum 

$$
  Tmf_1(3) \coloneqq Tmf(3,\Gamma_1)
$$

(first considered in ([Mahowald-Rezk 09](#MahowaldRezk09)), see at _[[congruence subgroup]]_ for the notation) is [[complex oriented cohomology theory|complex oriented]] ([Hill-Lawson 13, p.5](#HillLawson13)) (in contrast to [[Tmf]] $\simeq Tmf(1,1)$). This is one more way in which the inclusion

$$
  \array{
    Tmf_1(3)
    \\
    \uparrow
    \\
    Tmf
  }
$$

is analogous to the inclusion of [[KO]] into [[KU]]

=--


## Related concepts

* [[real-oriented generalized cohomology theory]]

* related but different: _[[equivariant elliptic cohomology]]_
 


## References


* {#MahowaldRezk09} [[Mark Mahowald]], [[Charles Rezk]], _Topological modular forms of level 3_, Pure Appl. Math. Quar. 5 (2009) 853-872 ([pdf](http://www.math.uiuc.edu/~rezk/tmf3-paper-final.pdf))

* {#Stojanoska11} [[Vesna Stojanoska]], _Duality for Topological Modular Forms_,  Documenta Math. 17 (2012), 271--311 ([arXiv:1105.3968](http://arxiv.org/abs/1105.3968))

* {#LawsonNaumann12} [[Tyler Lawson]], [[Niko Naumann]], _Strictly commutative realizations of diagrams over the Steenrod algebra and topological modular forms at the prime 2_, Int. Math.
Res. Not. (2013) ([arXiv:1203.1696](http://arxiv.org/abs/1203.1696))

* {#HillLawson13} [[Michael Hill]], [[Tyler Lawson]], _Topological modular forms with level structure_ ([arXiv:1312.7394](http://arxiv.org/abs/1312.7394))

* {#AndoHopkinsStrickland01} [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], _Elliptic spectra, the Witten genus and the theorem of the cube_, Invent. Math. 146 (2001) 595&#8211;687 MR1869850

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))


* {#KrizSati04a} [[Igor Kriz]], [[Hisham Sati]], _M Theory, Type IIA Superstrings, and Elliptic Cohomology_, Adv. Theor. Math. Phys. 8 (2004) 345-395 ([arXiv:hep-th/0404013](http://arxiv.org/abs/hep-th/0404013))

* {#KrizSati04b} [[Igor Kriz]], [[Hisham Sati]], _Type IIB String Theory, S-Duality, and Generalized Cohomology_, Nucl.Phys. B715 (2005) 639-664 ([arXiv:hep-th/0410293](http://arxiv.org/abs/hep-th/0410293))

* {#KrizSati05} [[Igor Kriz]], [[Hisham Sati]], _Type II string theory and modularity_, 	JHEP 0508 (2005) 038 ([arXiv:hep-th/0501060](http://arxiv.org/abs/hep-th/0501060))

* [[Igor Kriz]], Hao Xing, _On effective F-theory action in type IIA compactifications_, Int. J. Mod. Phys. A22:1279-1300, 2007 ([arXiv:hep-th/0511011](http://arxiv.org/abs/hep-th/0511011))

* {#Sati05} [[Hisham Sati]], _The Elliptic curves in gauge theory, string theory, and cohomology_, JHEP 0603 (2006) 096 ([arXiv:hep-th/0511087](http://arxiv.org/abs/hep-th/0511087))

* {#Sati10} [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]]_ , part I, Proc. Symp. Pure Math. 81 (2010), 181-236 [arXiv:1001.5020](http://arxiv.org/abs/1001.5020)

* {#Bandos00} [[Igor Bandos]], _Superembedding Approach and S-Duality. A unified description of superstring and super-D1-brane_, Nucl.Phys.B599:197-227,2001 ([arXiv:hep-th/0008249](http://arxiv.org/abs/hep-th/0008249))

* {#Greicius09} [[Aaron Greicius]], _Elliptic curves with surjective adelic Galois representations_ ([arXiv:0901.2513](http://arxiv.org/abs/0901.2513))


[[!redirects modular equivariant tmf]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
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

A _cyclotomic spectrum_ is an $S^1$-[[equivariant spectrum]] $E$ with [[fixed points]] for all the [[finite group|finite]] [[cyclic groups]] $C_p = \mathbb{Z}/p\mathbb{Z} \hookrightarrow S^1$ inside the [[circle group]], and equipped with $S^1$-equivariant identifications $E^{C_p} \stackrel{\simeq}{\to} E$ of the $C_P$-[[fixed points]] with the full object.

The [[topological Hochschild homology]]-spectra $E = THH(A)$ are naturally cyclotomic spectra, and this is where the concept originates: by the discussion at _[[Hochschild cohomology]]_ $THH(A)$ is the [[E-infinity ring]] of functions on the [[free loop space]] of $Spec(A)$, and cyclotomic structure reflects the structure of free loop spaces: loops that repeat with period $p$ are equivalent to plain loops.

Cyclotomic structure is the origin of the [[cyclotomic trace]] map $THH \longrightarrow TC$ from [[topological Hochschild homology]] to [[topological cyclic homology]].

## Definition
 {#Definition}

Throughout, for $p$ a [[prime number]] write $C_p \subset S^1$ for the [[cyclic group]] $\mathbb{Z}/p\mathbb{Z}$ of order $p$, regarded as a subgroup of the [[circle group]].

A definition says that a cyclotomic spectrum  is an [[circle group]]-[[genuine equivariant spectrum]] $X$ (modeled on [[orthogonal spectra]]) equipped with equivalences to its naive point-set fixed point spectra $\Phi^{C_p} X$ for all the [[cyclic group|cyclic]] [[subgroups]] $C_p \subset S^1$.
 
A more abstract definition was given in [Nikolaus-Scholze 17](#NikolausScholze17):[^HarmonizeLiterature]

[^HarmonizeLiterature]: Maybe this definition does not exactly agree with other definitions in the literature; see $n$Forum discussion [here](https://nforum.ncatlab.org/discussion/6851/cyclotomic-spectrum/?Focus=89589#Comment_89589).

+-- {: .num_defn #CyclotomicSpectrumViaTateSpectra}
###### Definition

A _cyclotomic spectrum_ is 

1. a [[spectrum]] $X$ 

1. a [[circle group]] [[∞-action]] on $X$, i.e. an [[(∞,1)-functor]] $B S^1 \to Spectra$ which takes [[generalized the|the]] unique point of $B S^1$ to $X$;

1. for each prime number $p$ a homomorphism of spectra with such circle group action

   $$
     F_p \;\colon\; X \longrightarrow X^{t C_p}
   $$

   to the [[Tate spectrum]] (the [[homotopy cofiber]] $X^{t C_p} \coloneqq cofib( X_{C_p} \overset{norm_p}{\to} X^{C_p} )$ of the [[norm map]]), where the circle action on the Tate spectrum comes from the canonical identification $S^1/C_p \simeq C_p$.

(These morphisms $F_p$ are called the _[[Frobenius morphisms]]_ of the cyclotomic structure, due to [this def. ](Frobenius+morphism#EInfinityFrobenius), [this example](Frobenius+morphism#EInfinityFrobeniusReducesToOrdinaryFrobenius)).

=--

([Nikolaus-Scholze 17, def. 1.3, def. II.1.1](#NikolausScholze17)).

+-- {: .num_prop}
###### Proposition

For $X$ a spectrum with [[stable homotopy groups]] bounded below, then 
def. \ref{CyclotomicSpectrumViaTateSpectra} is equivaent to the traditional: 

There is an [[(∞,1)-functor]]

$$
  CycSp_-^{gen} \overset{\simeq}{\longrightarrow} CycSp_-
$$ 

from traditional ("genuine") cyclotomic spectra bounded below to bounded below cyclotomic spectra in the sense of def. \ref{CyclotomicSpectrumViaTateSpectra}, and this is an [[equivalence of (∞,1)-categories]].

=--


([Nikolaus-Scholze 17, prop. II.3.4, theorem II.6.9](#NikolausScholze17)). 
  

## Examples
 {#Examples}

+-- {: .num_example #THHCarriesCyclotomicStructure}
###### Example
**([[topological Hochschild homology]])**

For every [[A-∞ ring]] $A$, the [[topological Hochschild homology]] spectrum $THH(A)$ naturally carries the structure of a cyclotomic spectrum (def. \ref{CyclotomicSpectrumViaTateSpectra}).

=--

([Nikolaus-Scholze 17, section II.2, def. III.2.3](#NikolausScholze17))

+-- {: .num_example #TrivialCyclotomicSpectra}
###### Example
**(trivial cyclotomic spectra)**

Every [[spectrum]] $X$ becomes a cyclotomic spectrum $X^{triv}$ in the sense of def. \ref{CyclotomicSpectrumViaTateSpectra} by equipping it 

1. with the trivial [[circle group]] [[∞-action]]

1. for each prime $p$ with the composite morphism

   $$
     f_p
      \;\colon\;
     \mathbb{S} 
      \longrightarrow 
     \mathbb{S}^{C_p} 
       \longrightarrow 
     \mathbb{S}^{t C_p}
   $$

   (the first being the $( B C_p \times (-) \dashv (-)^{C_p} )$-[[unit of an adjunction|unit]] into the [[homotopy fixed points]], the second the defining morphism into the [[Tate spectrum]]  )

1. the $S^1/C_p$-equivariant structure on these morphisms given under the [[adjunction]] between trivial action and homotopy fixed points by the [[adjunct]] morphisms

   $$
     X \longrightarrow \left(X^{t C_p}\right)^{S^1/C_p}
   $$

   as the composite

   $$
     X \to X^{S^1} 
       \simeq 
    \left( X^{C_p} \right)^{S^1/C_p}
     \longrightarrow
    \left( X^{t C_p} \right)^{S^1/C_p}
    \,.
   $$


This construction constitutes a left [[adjoint (infinity,1)-functor]]
to taking [[topological cyclic homology]]

$$
  CycSpectra
    \underoverset{\underset{TC}{\longrightarrow}}{\overset{(-)^{triv}}{\longleftarrow}}{\bot}
  Spectra
  \,.
$$

=--

([Nikolaus-Scholze 17, example II.1.2 (ii) and middle of p. 126](#NikolausScholze17))


+-- {: .num_example #CyclotomicSphereSpectrum}
###### Example
**(cyclotomic sphere spectrum)**

The [[sphere spectrum]] regarded as a cyclotomic spectrum via example \ref{TrivialCyclotomicSpectra} is called the _cyclotomic sphere spectrum_.

As such it is equivalently its [[topological Hochschild homology]] according to example \ref{THHCarriesCyclotomicStructure}:

$$
  \mathbb{S}^{triv} \simeq THH(\mathbb{S})
  \,.
$$

=--

([Nikolaus-Scholze 17, example II.1.2 (ii)](#NikolausScholze17))

## Properties

### Monoidal structure
 {#MonoidalStructure}

The [[tensor unit]] in the [[symmetric monoidal (infinity,1)-category]] of cyclotomic spectra is the cyclotomic sphere spectrum from example \ref{CyclotomicSphereSpectrum} ([Blumberg-Mandell 13, example 4.9](#BlumbergMandell13))


## Related concepts

* [[cyclotomic space]]

* [[cycle category]], [[cyclic set]], [[cyclic object]]

* [[Frobenius homomorphisms]]

* [[Tate spectrum]]

## References

* {#BlumbergMandell13} [[Andrew Blumberg]], [[Michael Mandell]], _The homotopy theory of cyclotomic spectra_ ([arXiv:1303.1694](http://arxiv.org/abs/1303.1694))

* {#BarwickGlasman16} [[Clark Barwick]], [[Saul Glasman]], _Cyclonic spectra, cyclotomic spectra, and a conjecture of Kaledin_ ([arXiv:1602.02163](http://arxiv.org/abs/1602.02163))

* [[Clark Barwick]], [[Saul Glasman]], _Noncommutative syntomic realization_ ([pdf](http://dl.dropbox.com/u/1741495/papers/tornado2.pdf))

* {#Malkiewich15} [[Cary Malkiewich]], _A visual introduction to cyclic sets and cyclotomic spectra_, 2015 ([pdf](http://math.uiuc.edu/~cmalkiew/ytm_2015.pdf))


* {#NikolausScholze17} [[Thomas Nikolaus]], [[Peter Scholze]], _On topological cyclic homology_ ([arXiv:1707.01799](https://arxiv.org/abs/1707.01799))


[[!redirects cyclotomic spectra]]

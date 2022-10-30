
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
 
A more abstract definition was given in ([Nikolaus-Scholze 17](#NikolausScholze17)):

+-- {: .num_defn #CyclotomicSpectrumViaTateSpectra}
###### Definition

A _cyclotomic spectrum_ is 

1. a [[spectrum]] $X$ 

1. a [[circle group]] [[∞-action]] on $X$, i.e. an [[(∞,1)-functor]] $B S^1 \to Spectra$ which takes [[generalized the|the]] unique point of $B S^1$ to $X$;

1. for each prime number $p$ a homomorphism of spectra with such circle group action

   $$
     X \longrightarrow X^{t C_p}
   $$

   to the [[Tate spectrum]] (the [[homotopy cofiber]] $X^{t C_p} \coloneqq cofib( X_{C_p} \overset{norm_p}{\to} X^{C_p} )$ of the [[norm map]]), where the circle action on the Tate spectrum comes from the canonical identification $S^1/C_p \simeq C_p$.

=--

([Nikolaus-Scholze 17, def. 1.3, def. II.1.1](#NikolausScholze17)).

This is equivalent to the traditional definition for spectra whose [[stable homotopy groups]] are bounded from below ([Nikolaus-Scholze 17, theorem 1.4](#NikolausScholze17)).

## Examples
 {#Examples}

+-- {: .num_example #THHCarriesCyclotomicStructure}
###### Example
**([[topological Hochschild homology]])**

For every [[A-∞ ring]] $A$, the [[topological Hochschild homology]] spectrum $THH(A)$ naturally carries the structure of a cyclotomic spectrum (def. \ref{CyclotomicSpectrumViaTateSpectra}).

=--

([Nikolaus-Scholze 17, section II.2, def. III.2.3](#NikolausScholze17))

+-- {: .num_example #CyclotomicSphereSpectrum}
###### Example
**(cyclotomic sphere spectrum)**

Consider the [[sphere spectrum]] $\mathbb{S}$ equipped with the trivial [[circle group]] [[∞-action]]. For each prime number $p$ there is a canonical morphism

$$
   f_p
   \;\colon\;
   \mathbb{S} \longrightarrow \mathbb{S}^{C_p} \longrightarrow \mathbb{S}^{t C_p}
$$

(the first being the $( B C_p \times (-) \dashv (-)^{C_p} )$-[[unit of an adjunction|unit]] into the [[homotopy fixed points]], the second the defining morphism into the [[Tate spectrum]]  ). These canonically carry equivariant structure (...) and hence make $\mathbb{S}$ a cyclotomic spectrum.

As such it is equivalently $\mathbb{S} \simeq THH(\mathbb{S})$ according to example \ref{THHCarriesCyclotomicStructure}.

=--

([Nikolaus-Scholze 17, example II.1.2 (ii)](#NikolausScholze17))

## Properties

### Monoidal structure
 {#MonoidalStructure}

The [[tensor unit]] in the [[symmetric monoidal (infinity,1)-category]] of cyclotomic spectra is the cyclotomic sphere spectrum from example \ref{CyclotomicSphereSpectrum} ([Blumberg-Mandell 13, example 4.9](#BlumbergMandell13))


## Related concepts

* [[Frobenius homomorphisms]]

* [[Tate spectrum]]

## References

* {#BlumbergMandell13} [[Andrew Blumberg]], [[Michael Mandell]], _The homotopy theory of cyclotomic spectra_ ([arXiv:1303.1694](http://arxiv.org/abs/1303.1694))

* {#BarwickGlasman16} [[Clark Barwick]], [[Saul Glasman]], _Cyclonic spectra, cyclotomic spectra, and a conjecture of Kaledin_ ([arXiv:1602.02163](http://arxiv.org/abs/1602.02163))

* [[Clark Barwick]], [[Saul Glasman]], _Noncommutative syntomic realization_ ([pdf](http://dl.dropbox.com/u/1741495/papers/tornado2.pdf))

* {#Malkiewich15} [[Cary Malkiewich]], _A visual introduction to cyclic sets and cyclotomic spectra_, 2015 ([pdf](http://math.uiuc.edu/~cmalkiew/ytm_2015.pdf))


* {#NikolausScholze17} [[Thomas Nikolaus]], [[Peter Scholze]], _On topological cyclic homology_ ([arXiv:1707.01799](https://arxiv.org/abs/1707.01799))


[[!redirects cyclotomic spectra]]

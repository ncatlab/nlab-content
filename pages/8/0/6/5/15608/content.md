
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[stable homotopy theory]] the [[rational homotopy theory|rational]] [[Bousfield localization of spectra]], hence $\mathbb{Q}$-localization $L_{S\mathbb{Q}}$, is accompanied dually by "$\mathbb{Q}$-acyclification" $G_{S\mathbb{Q}}$, forming a natural [[homotopy fiber sequence]]

$$
  G_{S \mathbb{Q}} X \longrightarrow X \longrightarrow L_{S\mathbb{Q}} X
$$

(by [this proposition](Bousfield+localization+of+spectra#LocalizationCofiber)).

This $G_{S\mathbb{Q}}$ is the operation of _universal torsion approximation_.
In the special case of [[chain complexes]] it corresponds to the [[derived functor]] that forms [[torsion subgroups]] (see the discussion at _[fracture theorem -- Arithmetic fracturing of chain complexes](fracture+theorem#CompletionAndTorsionOnDerivedCategories)_).

Similarly, if one already looks at [[p-local spectra]] then torsion approximation is the homotopy fiber of $S\mathbb{Z}[p^{-1}]$-localization.

## Definition


Let $A$  be an [[E-∞ ring]] and $\mathfrak{a} \subset \pi_0 A$ a [[generators and relations|finitely generated]] ideal of its underlying [[commutative ring]]. 


+-- {: .num_defn #TorsionInfinityModule}
###### Definition

An $A$-[[∞-module]] $N$ is an _$\mathfrak{a}$-[[torsion module]]_ if for all elements $n \in \pi_k N$ and all elements $a \in \mathfrak{a}$ there is $k \in \mathbb{N}$ such that $a^k n = 0$.

=--

([Lurie "Completions", def. 4.1.3](#LurieCompletions)).


+-- {: .num_prop #TorsionApproximation}
###### Proposition

The [[full sub-(∞,1)-category]]

$$
  A Mod_{\mathfrak{a}tor}
  \hookrightarrow
  A Mod
$$

is [[reflective sub-(∞,1)-category|co-reflective]] and the co-reflector $&#643;_{\mathfrak{a}}$ -- the _[[torsion approximation]]_ -- is [[smashing localization|smashing]].

=--

([Lurie "Completions", prop. 4.1.12](#LurieCompletions)).

+-- {: .num_prop}
###### Proposition

For $N \in A Mod_{\leq 0}$ then [[torsion approximation]], prop. \ref{TorsionApproximation}, intuced a [[monomorphism]] on $\pi_0$

$$
  \pi_0 &#643;_{\mathfrak{a}} N \hookrightarrow \pi_0 N
$$

including the $\mathfrak{a}$-nilpotent elements of $\pi_0 N$.

=--

([Lurie "Completions", prop. 4.1.18](#LurieCompletions)).

## Properties

### Relation to localization

+-- {: .num_prop}
###### Proposition

There is a [[natural transformation|natural]] [[homotopy fiber sequence]]

$$
  &#643;_{\mathfrak{a}} \longrightarrow id \longrightarrow &#643;_{\mathfrak{a}dR}
$$

relating $\mathfrak{a}$-torsion approximation on the left with $\mathfrak{a}$-[[localization of a module|localization]] on the right.

=--

([Lurie "Completions", remark 4.1.20](#LurieCompletions))

### As a modality in arithmetic cohesion

Under suitable conditions, torsion approximation forms an [[adjoint modality]] with [[adic completion]]. 

[[!include arithmetic cohesion -- table]]

## Related concepts

* [[Pontryagin duality for torsion abelian groups]]

## References

Discussion for [[chain complexes]] is in 

* {#DwyerGreenlees99} [[William Dwyer]], [[John Greenlees]], section 4.1 of _Complete modules and torsion modules_, Amer. J. Math, 1999  ([pdf](https://www3.nd.edu/~wgd/Dvi/Complete.And.Torsion.pdf))

* [[Carles Casacuberta]] et al., _Models for torsion homotopy types_ ([pdf](http://atlas.mat.ub.es/personals/casac/articles/crhp.pdf))

Discussion in the generality of [[E-∞ rings]] and [[∞-modules]] is in 

* {#LurieCompletions} [[Jacob Lurie]], section 4.1 of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_


[[!redirects torsion approximations]]


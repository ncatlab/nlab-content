
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the definition of [[torsors]] and [[principal bundles]] one deals with [[group action]] [[action objects|objects]] $G \times P \overset{\rho}{\longrightarrow} P$ (generally [[over category|over]] some base object $X$) whose [[shear map]] is an [[isomorphism]]:

\[
  \label{ShearMapForBundles}
  \array{
    G \times P
    &
    \underoverset
      {\simeq}
      { (\rho, pr_2) }
      {\longrightarrow}
    &
    P \times_X P
    \\
    (g,p) &\mapsto& \big( \rho(g)(p), p \big)
    \,.
  }
\]


Now *if* $P$ is [[inhabited set|inhabited]] ([[fiber]]-wise over $X$), this implies a ([[fiber]]-wise) [[free action|free]] and [[transitive action|transitive]] (hence [[regular action|regular]]) action, which is typically what is understood to characterize [[torsors]]/[[principal bundles]].

However, the condition alone that the [[shear map]] (eq:ShearMapForBundles) be an isomorphism makes sense (and is then automatically satisfied) also for locally [[empty set|empty]] $P$, meaning for [[fibers]] of $P$ being [[strict initial objects]] ([[internalization|internal]] to the ambient [[category]]). If that case is meant to be included, one speaks, following [[Alexander Grothendieck|Grothendieck]], alternatively of:

1. a *formally principal* action ([Grothendieck 60, p. 312 (15 of 30)](#Grothendieck60)) 

1. a *pseudo-torsor* ([Grothendieck 67, EGA IV.4, 16.5.15](#EGAIV4)) 

1. a *formally principal homogeneous* action (ibid. & [Grothendieck 71, p. 9 (293)](#Grothendieck71)).

Examples of references using this terminology: [StacksProject](#StacksProject), [Moret-Bailly 13, slide 5](#MoretBailly13), [BGA 13, p. 73-74](#BGA13).


## Examples

* Even if a $G$-[[equivariant principal bundle]] is an actual [[torsor]] ([[internalization|in]] [[topological G-spaces]] [[slice category|sliced]] over a given base) its [[fixed loci]] will generally only be (similarly internal) pseudo-torsors.

## Related concepts

* [empty heap](heap#empty)

* [[possibly empty group]]

## References

The term seems to be due to:

* {#Grothendieck60} [[Alexander Grothendieck]], p. 312 (15 of 30) in: *Technique de descente et théorèmes d’existence engéométrie algébrique. I. Généralités. Descente parmorphismes fidèlement plats*, Séminaire N. Bourbaki, 1960, exp. no190, p. 299-327 ([numdam:SB_1958-1960__5__299_0](http://www.numdam.org/item/?id=SB_1958-1960__5__299_0))

* {#Grothendieck67} [[Alexander Grothendieck]], 16.5.15 in: *[[Éléments de géométrie algébrique]]* : IV. *Étude locale des schémas et des morphismes de schémas (Quatrième partie)*, Publications mathématiques de l’I.H.É.S., tome  32 (1967), p. 5-361 ([numdam:PMIHES_1967__32__5_0](http://www.numdam.org/item/PMIHES_1967__32__5_0))

* {#Grothendieck71} [[Alexander Grothendieck]], p. 9 of _Exemples et Complements_ ([doi:10.1007/BFb0058666](https://link.springer.com/chapter/10.1007/BFb0058666), [pdf](https://link.springer.com/content/pdf/10.1007%2FBFb0058666.pdf)), which is p. 293 in:

  [[Alexander Grothendieck]], [[Michèle Raynaud]], *Revêtements étales et groupe fondamental* ([[SGA 1]]),  Lecture Notes in Mathematics **224**, Springer 1971 ([arXiv:math/0206203](https://arxiv.org/abs/math/0206203), [doi:10.1007/BFb0058656](https://link.springer.com/book/10.1007/BFb0058656))

See also:

* {#StacksProject} [[The Stacks Project]], *Pseudo G-Torsor* ([Definition 03AH](https://stacks.math.columbia.edu/tag/03AH), [Definition 0498](https://stacks.math.columbia.edu/tag/0498))


* {#MoretBailly13} [[Laurent Moret-Bailly]], slide 5 of: *Principal Bundles over Valued Fields*, Oberwolfach 2013 ([pdf](https://perso.univ-rennes1.fr/laurent.moret-bailly/exposes/GMBMFOWeb.pdf), [[MoretBaillyPrincipalBundlesValuedFields.pdf:file]])

* {#BGA13} Alessandra Bertapelle, Cristian D. Gonzalez-Aviles, *The Greenberg functor revisited*, European Journal of Mathematics volume 4, pages 1340–1389 (2018) ([arXiv:1311.0051](https://arxiv.org/abs/1311.0051), [doi:10.1007/s40879-017-0210-0](https://doi.org/10.1007/s40879-017-0210-0))

[[!redirects pseudo-torsors]]

[[!redirects pseudo torsor]]
[[!redirects pseudo torsors]]

[[!redirects formally principal homogeneous space]]
[[!redirects formally principal homogeneous spaces]]
[[!redirects formally-principal homogeneous space]]
[[!redirects formally-principal homogeneous spaces]]

[[!redirects formally principal bundle]]
[[!redirects formally principal bundles]]
[[!redirects formally-principal bundle]]
[[!redirects formally-principal bundles]]

[[!redirects formally principal action]]
[[!redirects formally principal actions]]
[[!redirects formally-principal action]]
[[!redirects formally-principal actions]]






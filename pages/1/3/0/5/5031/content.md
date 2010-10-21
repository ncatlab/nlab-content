
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

By __$Topos$__ (or __$Toposes$__) is denoted the [[category]] of [[topos]]es. Usually this means:

* [[object]]s are [[topos]]es;

* [[morphism]]s are [[geometric morphism]]s of toposes.

This naturally a [[2-category]], with the [[2-morphism]]s being [[natural transformation]]s between the [[inverse image]] parts of geometric morphisms.  That is, a 2-morphism $f\to g$ is a natural transformation $f^* \to g^*$ (which is, by [[mate]] calculus, equivalent to a natural transformation $g_* \to f_*$).  Thus, $Toposes$ is equivalent to both of

* the (non-full) [[sub-2-category]] of $Cat^{op}$ on categories that are toposes and morphisms that are the inverse image parts of geometric morphisms, and
* the (non-full) sub-2-category of $Cat^{co}$ on categories that are toposes and morphisms that are the direct image parts of geometric morphisms.

### Related 2-categories

* There is also the sub-2-category $ShToposes = GrToposes$ of [[sheaf topos]]es (i.e. Grothendieck toposes).

* Note that in some literature this 2-category is denoted merely $Top$, but that is also commonly used to denote [[Top|the category]] of [[topological spaces]].

* We obtain a very different 2-category of toposes if we take the morphisms to be [[logical functors]]; this 2-category is sometimes denoted $Log$ or $LogTopos$.

## Limits

The 2-category $Topos$ is not all that well-endowed with limits, but its slice categories are finitely complete [[2-limit|as 2-categories]], and $ShTopos$ is closed under finite limits in $Topos/Set$.  In particular, the [[terminal object]] in $ShToposes$ is the topos [[Set]] $\simeq Sh(*)$.

## From topological spaces to toposes

The operation of forming [[categories of sheaves]]

$$
  Sh(-) : Top \to ShToposes
$$

embeds [[topological space]]s into toposes. For $f : X \to Y$ a [[continuous map]] we have that $Sh(f)$ is the [[geometric morphism]]

$$
  Sh(f) : Sh(X) \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
  Sh(Y)
$$

with $f_*$ the [[direct image]] and $f^*$ the [[inverse image]].

Strictly speaking, this functor is not an [[embedding]] if we consider $Top$ as a 1-category and $Toposes$ as a 2-category, since it is then not [[fully faithful]] in the 2-categorical sense---there can be nontrivial 2-cells between geometric morphisms between toposes of sheaves on topological spaces.

However, if we regard $Top$ as a [[(1,2)-category]] where the 2-cells are inequalities in the [[specialization ordering]], then this functor does become a 2-categorically full embedding (i.e. an equivalence on hom-categories) if we restrict to the full subcategory $SobTop$ of [[sober spaces]].  This embedding can also be extended from $SobTop$ to the entire category of [[locales]] (which can be viewed as "Grothendieck 0-toposes").

## From toposes to higher toposes

There are similar full embeddings $ShTopos \hookrightarrow Sh 2 Topos$ and $ShTopos \hookrightarrow Sh(n,1)Topos$ of sheaf (1-)toposes into sheaf 2-toposes and sheaf $(n,1)$-toposes for $2\le n\le \infty$.


category: category

[[!redirects Topos]]
[[!redirects Topoi]]
[[!redirects Toposes]]

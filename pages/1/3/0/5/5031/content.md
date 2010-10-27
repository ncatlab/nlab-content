
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

This naturally a [[2-category]], with the [[2-morphism]]s being [[natural transformation]]s between the [[inverse image]] parts of geometric morphisms.  That is, a 2-morphism $f\to g$ is a natural transformation $f^* \to g^*$ (which is, by [[mate]] calculus, equivalent to a natural transformation $g_* \to f_*$ between [[direct image]]s).  Thus, $Toposes$ is equivalent to both of

* the (non-full) [[sub-2-category]] of $Cat^{op}$ on categories that are toposes and morphisms that are the inverse image parts of geometric morphisms, and
* the (non-full) sub-2-category of $Cat^{co}$ on categories that are toposes and morphisms that are the direct image parts of geometric morphisms.

### Related 2-categories

* There is also the sub-2-category $ShToposes = GrToposes$ of [[sheaf topos]]es (i.e. Grothendieck toposes).

* Note that in some literature this 2-category is denoted merely $Top$, but that is also commonly used to denote [[Top|the category]] of [[topological spaces]].

* We obtain a very different 2-category of toposes if we take the morphisms to be [[logical functors]]; this 2-category is sometimes denoted $Log$ or $LogTopos$.


## Properties


### From topological spaces to toposes

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


### From toposes to higher toposes

There are similar full embeddings $ShTopos \hookrightarrow Sh 2 Topos$ and $ShTopos \hookrightarrow Sh(n,1)Topos$ of sheaf (1-)toposes into [[2-sheaf]] [[2-topos]]es and sheaf [[(n,1)-topos]]es for $2\le n\le \infty$.



### Limits and colimits {#Limits}

The 2-category $Topos$ is not all that well-endowed with [[limit]]s, but its [[slice categories]] are finitely complete [[2-limit|as 2-categories]], and $ShTopos$ is closed under finite limits in $Topos/Set$.  In particular, the [[terminal object]] in $ShToposes$ is the topos [[Set]] $\simeq Sh(*)$.

The supply with colimits is better:

{#ColimitsByInverseImageLimits}
+-- {: .un_prop}
###### Proposition
All small (indexed) [[2-colimit]]s in $ShTopos$ exists and are computed as (indexed) [[2-limit]]s in [[Cat]] of the underlying [[inverse image]] functors.

=--

This appears as ([Moerdijk, theorem 2.5](#Moerdijk))

+-- {: .un_prop}
###### Proposition

Let 

$$
  \array{
    \mathcal{F} &\stackrel{p_2}{\to}& \mathcal{E}_2
    \\
    {}^{\mathllap{p_1}}\downarrow &\swArrow& \downarrow^{\mathrlap{f_2}}
    \\
    \mathcal{E}_1 &\underset{f_1}{\to}& \mathcal{E}
  }
$$

be a [[2-pullback]] in $Topos$ such that

* $f_1, f_2$ are both [[pseudomonic morphism]]s

* $\mathcal{E}_1 \coprod \mathcal{E}_2 \to \mathcal{E}$ is an [[effective epimorphism]];

then the diagram of [[inverse image]] functors

$$
  \array{
    \mathcal{F} &\stackrel{p_2^*}{\leftarrow}& \mathcal{E}_2
    \\
    {}^{\mathllap{p_1^*}}\uparrow &\swArrow& \uparrow^{\mathrlap{f_2^*}}
    \\
    \mathcal{E}_1 &\underset{f_1^*}{\leftarrow}& \mathcal{E}
  }
$$

is a 2-pullback in [[Cat]] and so by the [above](#ColimitsByInverseImageLimits) the original square is also a 2-pushout.

=--

This appears as theorem 5.1 in ([BungeLack](#BungeLack))

+-- {: .un_prop}
###### Proposition


The 2-category $Topos$ is an [[extensive category]]. Same for toposes bounded over a base.

=--

This is in ([BungeLack, proposition 4.3](#BungeLack)).


## Related concepts

* **Topos**

* [[(∞,1)Topos]]


## References

The characterization of colimits in $Topos$ is in

* [[Ieke Moerdijk]], _The classifying topos of a continuous groupoid. I_ Transaction of the American mathematical society Volume 310, Number 2, (1988) ([pdf](http://www.ams.org/journals/tran/1988-310-02/S0002-9947-1988-0973173-9/S0002-9947-1988-0973173-9.pdf))
{#Moerdijk}

The fact that $Topos$ is extensive is in

* [[Marta Bunge]], [[Steve Lack]], _van Kampen theorem for toposes_ ([ps](http://www.maths.usyd.edu.au/u/stevel/papers/vkt.ps.gz))
{#BungeLack}


category: category

[[!redirects Topos]]
[[!redirects Topoi]]
[[!redirects Toposes]]

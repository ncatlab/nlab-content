
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $C$ a [[small category]], and $PSh(C)$ its [[presheaf topos]], we have that a [[colimit]]-preserving functor $PSh(C) \to Set$ is equivalently itself a copresheaf.

$$
  [PSh(C), Set]_{coc} \simeq CoPSh(C)
  \,.
$$

If we replace in this statement presheaves with [[sheaves]], we obtain the notion of _cosheaf_

$$
  [Sh(C), Set]_{coc} \simeq CoSh(C)
  \,.
$$

## Definition

+-- {: .un_defn}
###### Definition

Let $C$ be a [[site]]. A **cosheaf** on $C$ is a [[copresheaf]]

$$
  F : C \to Set
$$

such that it takes [[cover]]s to [[colimit]]s: for each covering family $\{U_i \to U\}$ in $C$ we have

$$
  F(U) \simeq \lim_{\to}
  \left(
     \coprod_{i j} F(U_i \times_{U} U_j)
     \stackrel{\to}{\to}
     \coprod_i F(U_i)
  \right)
$$


Write $CoSh(C) \subset CoPSh(C)$ for the full [[subcategory]] on cosheaves.

=--

## Proposition

+-- {: .un_prop}
###### Proposition

There is a [[natural transformation|natural]] [[equivalence of categories]]

$$
  CoSh(C) \simeq Func_{coc}(Sh(C), Set)
  \,,
$$

where on the right we have the category of colimit-preserving functors.

Equivalently: a copresheaf is a cosheaf precisely if its [[Yoneda extension]] $PSh(C) \to Set$ factors through [[sheafification]] $PSh(C) \to Sh(C)$.

=--

This is ([BungeFunk, prop. 1.4.3](BungeFunk)).

## Related concepts

* [[presheaf]] /  [[sheaf]] / **cosheaf**

* [[2-sheaf]] / [[stack]]

* [[(∞,1)-sheaf]] / [[∞-stack]] 


## References

section 1.4 of

* [[Marta Bunge]] and Jonathan Funk, _Singular coverings of toposes_ Lecture Notes in Mathematics, (2006) Volume 1890/2006

  chapter 1 _Lawvere Distributions on Toposes_
{#BungeFunk}
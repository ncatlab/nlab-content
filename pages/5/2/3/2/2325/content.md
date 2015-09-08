
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

An [[(∞,1)-topos]] is **$n$-localic** if 

* regarded as a [[little topos]] it behaves like a generalized [[n-groupoid]]; 

* it behaves like the [[(∞,1)-category of (∞,1)-sheaves]] over an [[(∞,1)-site]] that is a [[(n,1)-category]].

More precisely: if [[(∞,1)-geometric morphisms]] into it are fixed by their restriction to the underlying [[(n,1)-toposes]] of $(n-1)$-[[truncated]] objects.

To the tower of [[(n,1)-toposes]] of $(n-1)$-truncated objects 


$$
  \cdots \to \tau_{\leq 3-1} \mathcal{X} \to \tau_{\leq 2-1} \mathcal{X} \to \tau_{\leq 1-1} \mathcal{X} \to \tau_{\leq 0-1} \mathcal{X}
  \to *
$$

of a given [[(∞,1)-topos]] $\mathcal{X}$ corresponds a tower of $n$-localic toposes $\mathcal{X}_n$ such that $\tau_{\leq n -1} \mathcal{X} \simeq \tau_{\leq n-1} \mathcal{X}_n$. We may think of the $n$-localic $\mathcal{X}_n$ as being $n$th stage in the [[Postnikov tower]] decomposition of $\mathcal{X}$.

A 0-localic $(1,1)$-topos is a [[localic topos]] from ordinary [[topos theory]].


## Definition 

We write [[(∞,1)Topos]] for the [[(∞,1)-category]] of [[(∞,1)-toposes]] and [[(∞,1)-geometric morphisms]] between them.

For $\mathcal{X}$ an [[(∞,1)-topos]] we denote by

$$
  \tau_{\leq n-1} \mathcal{X} \hookrightarrow \mathcal{X}
$$ 

the [[(n,1)-topos]] of $(n-1)$-[[truncated]] objects of $\mathcal{X}$.

We write $(n,1)Topos$ for the [[(n,1)-category|(n+1,1)-category]] of [[(n,1)-topos]]es and $(n,1)$-geometric morphisms between them.


+-- {: .num_defn}
###### Definition
**($n$-localic $(\infty,1)$-topos)**


An [[(∞,1)-topos]] $\mathcal{X}$ is **$n$-localic** if for any other
$(\infty,1)$-topos $\mathcal{Y}$ the canonical morphism

$$
  (\infty,1)Topos(\mathcal{Y},\mathcal{X}) \to 
   (n,1)Topos(\tau_{\leq n-1} \mathcal{Y}, \tau_{\leq n-1}\mathcal{Y})
$$

is an [[equivalence of (∞,1)-categories]] (of [[∞-groupoids]]).

More generally,

a [[(n,1)-topos|(k,1)-topos]] $\mathcal{X}$ is **$n$-localic** for $0 \leq n \leq k \leq \infty$ if for any other
$(k,1)$-topos $\mathcal{Y}$ the canonical morphism

$$
  (k,1)Topos(\mathcal{Y},\mathcal{X}) \to 
   (n,1)Topos(\tau_{\leq n-1} \mathcal{Y}, \tau_{\leq n-1}\mathcal{Y})
$$

is an [[equivalence of (∞,1)-categories]] (of [[∞-groupoids]]).

=--


This is ([[Higher Topos Theory|HTT, def. 6.4.5.8]]).

+-- {: .num_remark}
###### Remark

This implies that an $n$-localic $(\infty,1)$-topos is also $(n+1)$-localic and generally $k$-localic for all $k \geq n$.

=--




## Examples
  {#Examples}

+-- {: .num_prop}
###### Proposition

The [[(∞,1)-category of (∞,1)-sheaves]] over an [[(∞,1)-site]] $C$ with finite limits which is an [[(n,1)-category]] is $n$-localic.

=--

This is ([[Higher Topos Theory|HTT, lemma 6.4.5.6]]).

+-- {: .num_remark}
###### Remark

For $n = 0$ this implies the familiar statement from ordinary [[topos theory]]: a [[category of sheaves]] over a [[posite]]=[[(0,1)-site]] is a [[localic topos]] (= 0-localic $(1,1)$-topos).

=--

This is ([LurieStructured, lemma 2.3.16](#JurieStructured)).


+-- {: .num_prop}
###### Proposition

For $n \in \mathbb{N}$ and $\mathcal{X}$ an $n$-localic $(\infty,1)$-topos, the [[over-(∞,1)-topos]] $\mathcal{X}/U$ is $n$-localic precisely if the object $U$ is $n$-[[truncated]].

=--

This is ([StrSp, lemma 2.3.14](#JurieStructured)).


+-- {: .num_prop}
###### Proposition

For $\mathcal{X}$ an $n$-localic $(\infty,1)$-topos let $U \in \mathcal{X}$ be an [[object]]. Then the following are equivalent

1. the restriction of the [[inverse image]] $U^* : \mathcal{X} \to \mathcal{X}/U$ (of the [[etale geometric morphism ]] from the [[over-(∞,1)-topos]]) to $(n-1)$-[[truncated]] objects is an [[equivalence of (∞,1)-categories]];

1. the object $U$ is $n$-[[connected]].

=--

This is ([StrSp, lemma 2.3.14](#JurieStructured)).


## Properties

+-- {: .num_prop}
###### Proposition

Every [[(n,1)-topos]] $\mathcal{Y}$ is the [[(n,1)-category]] of $(n-1)$-[[truncated]] objects in an $n$-localic $(\infty,1)$-topos $\mathcal{X}_n$

$$
  \tau_{n-1} X_n  \stackrel{\simeq}{\to} \mathcal{Y}
  \,.
$$

=--

This is ([[Higher Topos Theory|HTT, prop. 6.4.5.7]]).



Let $\mathcal{G}$ be a [[geometry (for structured (∞,1)-toposes)]].

+-- {: .num_prop}
###### Proposition

If $\mathcal{G}$ is an [[(∞,n)-category]] then a $n$-localic $\mathcal{G}$-[[structured (∞,1)-topos]] is an $n$-[[truncated]] object in the [[(∞,1)-category]] $Topos(\mathcal{G})$.

=--

This is [StrSp, lemma 2.6.17](#LurieStructured)

## Related concepts

* [[localic topos]]

* [[n-localic 2-topos]]

* [[n-types cover]]


## References

The general noion is the topic of section 6.4.5 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

Remarks on the application of $n$-localic $(\infty,1)$-toposes in [[higher geometry]] are in

* [[Jacob Lurie]], _[[Structured Spaces]]_
{#JurieStructured}

[[!redirects localic (∞,1)-topos]]
[[!redirects localic (infinity,1)-topos]]

[[!redirects n-localic (∞,1)-topos]]


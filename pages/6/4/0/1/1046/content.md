+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### [[categories of categories - contents|categories of categories]]
+-- {: .hide}
[[!include categories of categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

**$\infty Grpd$** or **$\mathrm{Ani}$** is the [[(∞,1)-category]] of [[∞-groupoids]] or [[anima]], i.e. of [[(∞,0)-categories]]. This is the archetypical [[(∞,1)-topos]], the home of classical [[homotopy theory]].

[[equivalence of (∞,1)-categories|Equivalently]] this means all of the following:

1. $\infty Grpd$ is the [[simplicial localization]] of the [[category]] [[Top]]${}_k$ of ([[weakly Hausdorff topological space|weakly Hausdorff]]) [[locally compact topological spaces]] at the [[weak homotopy equivalences]]. As such it is the [[∞-category]]-enhancement of the [[classical homotopy category]]: $\tau_0(\infty Grpd) \simeq$ [[Ho(Top)]], itself [[presentable (∞,1)-category|presented]] by the [[classical model structure on topological spaces]]: $\infty Grpd \simeq L_{whe} Top_k$.

1. $\infty Grpd$ is the [[simplicial localization]] of the [[category]] [[sSet]] of [[simplicial sets]] at the simplicial [[weak homotopy equivalences]]. As such it is the [[∞-category]]-enhancement of the [[classical homotopy category]]: $\tau_0(\infty Grpd) \simeq$ [[Ho(sSet)]], itself [[presentable (∞,1)-category|presented]] by the [[classical model structure on simplicial sets]]: $\infty Grpd \simeq L_{whe} sSet$. 

   Hence, as a [[simplicially enriched category|Kan-complex enriched category]] (a [[fibrant object]] in the [[model structure on sSet-categories]]) $\infty Grpd$ is the [[full subcategory|full]] [[simplicially enriched category|sSet enriched]]-[[subcategory]] of [[sSet]] on the [[Kan complexes]].


1. $\infty Grpd$ is the [[full sub-(∞,1)-category]] of [[(∞,1)Cat]] on those [[(∞,1)-categories]] that are [[∞-groupoids]].


## Properties

### As an $(\infty,1)$-topos

As an [[(∞,1)-topos]] $\infty Grpd$ is the [[terminal object|terminal]] $(\infty,1)$-topos: for every other [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaf]] [[(∞,1)-topos]] $\mathbf{H}$ there is up to a [[contractible]] space of  choices a unique [[geometric morphism]] $(LConst \dashv \Gamma) : \mathbf{H}\stackrel{\leftarrow}{\to} \infty Grpd$ -- the [[global section]] geometric morphism. See there for more details.


### Limits and colimits in $\infty Grpd$


[[limit in a quasi-category|Limits and colimits]] over a [[(∞,1)-functor]] with values in $\infty Grpd$ may be reformulation in terms of the  [[universal fibration of (infinity,1)-categories]].

Let the [[(∞,1)-functor]] $Z|_{Grpd} \to \infty Grpd^{op}$ be the [[universal fibration of (infinity,1)-categories|universal ∞-groupoid fibration]] whose fiber over the object denoting some $\infty$-groupoid is that very $\infty$-groupoid.

Then let $X$ be any [[∞-groupoid]] and

$$
  F : X \to \infty Grpd
$$

an [[(∞,1)-functor]]. Recall that the [[Cartesian fibration|coCartesian fibration]] $E_F \to X$ classified by $F$ is the pullback of the [[universal fibration of (∞,1)-categories]] $Z$ along F:

$$
  \array{
    E_F &\to& Z|_{Grpd}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{F}{\to}& \infty Grpd
  }
$$

+-- {: .un_prop }
###### Proposition

Let the assumptions be as above. Then:

* The colimit of $F$ is equivalent to $E_F$:

  $$
    E_F \simeq colim F
  $$

* The limit of $F$ is equivalent to the [[(infinity,1)-category of cartesian section|(∞,1)-groupoid of sections]] of $E_F \to X$

  $$
    \Gamma_X(E_F) \simeq lim F
    \,.
  $$

=-- 

+-- {: .proof}
###### Proof

The statement for the colimit is corollary 3.3.4.6 in [[Higher Topos Theory|HTT]]. The statement for the limit is corollary 3.3.3.4.

=--




##Subcategories

The [[n-truncated object of an (infinity,1)-category|n-truncated objects]] of $\infty Grpd$ are the [[n-groupoids]] (including [[(-1)-groupoid]]s and the [[(-2)-groupoid]]).

## Related categories

* [[Set]]

* [[Grpd]], 

  **$\infty Grpd$**

  [[Top]], [[Ho(Top)]]

* [[Cat]], [[(∞,1)Cat]]

* [[(∞,n)Cat]]

category: category

[[!redirects ∞Groupoid]]
[[!redirects ∞Groupoids]]

[[!redirects ∞Grpd]]
[[!redirects ∞ Grpd]]
[[!redirects ∞-Grpd]]
[[!redirects infinity-Grpd]]
[[!redirects ∞Gpd]]
[[!redirects ∞ Gpd]]
[[!redirects ∞-Gpd]]
[[!redirects infinity-Gpd]]
[[!redirects Infinity-Gpd]]

[[!redirects (∞,1)-category of spaces]]
[[!redirects (infinity,1)-category of spaces]]

[[!redirects Ani]]

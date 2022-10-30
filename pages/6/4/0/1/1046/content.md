**$\infty Grpd$** is the [[(∞,1)-category]] of [[∞-groupoid]]s, i.e. of [[(∞,0)-categories]].

It is the full [[sub-quasi-category|subcategory]] of [[(∞,1)Cat]] on those [[(∞,1)-categories]] that are [[∞-groupoid]]s.

It is also the archetypical [[(∞,1)-topos]].

#Contents#
* automatic table of contents goes here
{:toc}

## Incarnations

### As an $sSet$-category

As an [[simplicially enriched category]] $\infty Grpd$ is the full [[SSet]]-[[enriched category|enriched subcategory]] of [[SSet]] on [[Kan complex]]es.

### As an enriched model category

$\infty Grpd$ is the [[(∞,1)-category]] that is [[presentable (∞,1)-category|presented]] by the Quillen [[model structure on simplicial sets]].

As a [[simplicially enriched category|Kan-complex enriched category]] this is the full [[sSet]]-[[subcategory]] on fibrant-cofibrant objects of the Quillen [[model structure on simplicial sets]].

Under the [[homotopy hypothesis]]-theorem, this means that $\infty Grpd$ is also the full $(\infty,1)$-subcategory of [[Top]] on spaces of the [[homotopy type]] of a [[CW-complex]].

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




## Subcategories

The [[n-truncated object of an (infinity,1)-category|n-truncated objects]] of $\infty Grpd$ are the [[n-groupoid]]s. (including [[(-1)-groupoid]]s and the [[(-2)-groupoid]]).


category: category

[[!redirects ∞Grpd]]
[[!redirects ? Grpd]]
[[!redirects ∞-Grpd]]
[[!redirects infinity-Grpd]]
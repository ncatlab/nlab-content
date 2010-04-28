
<div class="rightHandSide toc">
[[!include quasi-category theory contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The analog of the notion of [[subcategory]] for [[(∞,1)-categories]].

## Definition

Say that an [[equivalence of quasi-categories|equivalence of (∞,1)-categories]] $C \stackrel{\simeq}{\to} D$ exhibits $C$ as a **0-subcategory** of $D$.

Then define recursively, for $n \in \mathbb{N}$: 

an **$n$-subcategory** of an $(\infty,1)$-category $D$ for $n \geq 1$ is an [[(∞,1)-functor]]

$$
  F : C \to D
$$

such that for all objects $x,y \in C$ the component-$(\infty,1)$-functor on the [[hom-object in a quasi-category|hom-objects]] 

$$
  F_{x,y} : Hom_C(x,y) \to Hom_D(F(x), F(y))
$$

exhibits an $(n-1)$-subcategory.

## Special cases

### 1-Subcategory / full subcategory

A **full subcategory** is a 1-subcategory, exhibited by a [[full and faithful (∞,1)-functor]]. 

Let $C$ and $D$ be incarnated specifically as [[model structure on sSet-categories|fibrant]] [[simplicially enriched categories]]. Then for $F : C \to D$ a full and faithful $(\infty,1)$-functor, choose in each preimage $F^{-1}(d)$ for each object $d \in D$ a representative, and let $C'$ be the full [[sSet]]-[[enriched category|enriched]] [[subcategory]] on these representatives.

Then the evident projection functor $C \stackrel{\simeq}{\to} C'$ is manifestly an [[equivalence of quasi-categories|equivalence]] and the original $F : C \to D$ factors as

$$
  F : C \stackrel{\simeq}{\to} C' \hookrightarrow D
  \,,
$$

where the second morphism is an ordinary inclusion of objects and hom-complexes.

### 2-Subcategory

Let the $(\infty,1)$-categories $C$ and $D$ concretely be incarnated as [[model structure on sSet-categories|fibrant]] [[simplicially enriched categories]].

Write $h C := Ho(C)$ and $h D := Ho(D)$ for the corresponding [[homotopy category of an (∞,1)-category]] (hom-wise the connected components of the corresponding [[simplicially enriched category]]).

Let $h D \hookrightarrow h C$ be an ordinary (1-)[[subcategory]] of $h C$. Then the corresponding (ordinary) [[pullback]] $D$  in [[sSet]]-[[Cat]]

$$
  \array{
    D &\to& C
    \\
    \downarrow && \downarrow
    \\
    h D &\to& h C
  }
$$

is what is called a subcategory in [[Higher Topos Theory|HTT, section 1.2.11]].

This pulback manifestly produces the simplicially enriched category whose

* objects are those of $h D$;

* hom-complexes are precisely the unions of those connected components of the hom-complexes of $D$ whose equivalence class is present in $h D$.

Therefore the inclusion functor $D \to C$ is on each hom-complex a [[full and faithful (∞,1)-functor]]. Hence this identifies $D$ as a 2-subcategory of $C$.





## References

What we call a 2-subcategory of an $(\infty,1)$-category appears in  section 1.2.11 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_




## Discussion

A previous version of this entry led to the following discussion

+--{: .query}
[[Mike Shulman]]: Over at [[subcategory]] we sort of decided that when speaking non-evilly, a "1-subcategory" is a fully faithful functor, and a "2-subcategory" is a faithful functor.  By analogy, a fully faithful $(\infty,1)$-functor would be called a 1-subcategory, while a "2-subcategory" would be an $(\infty,1)$-functor such that each hom-action $C(x,y)\to D(F x, F y)$ is fully faithful as a map of $\infty$-groupoids, i.e. equivalent to the inclusion of some subset of connected components.  Am I correct in guessing that the "sub-quasicategories" defined here are precisely the 2-subcategories in this sense?

[[Urs Schreiber]]: thanks, good point. That sounds plausible, given what the above pullback diagram expresses. Let me think about it...

[[Urs Schreiber]]: okay, I have implemented this now. Switched to sSet-categories for the moment just for ease of discussion.

=--


[[!redirects sub-quasi-category]]

[[!redirects sub-quasicategory]]
[[!redirects subquasicategory]]

[[!redirects sub-(∞,1)-category]]
[[!redirects sub-(infinity,1)-category]]

[[!redirects sub-quasi-categories]]
[[!redirects sub-quasicategories]]
[[!redirects subquasicategories]]

[[!redirects sub-(∞,1)-categories]]
[[!redirects sub-(infinity,1)-categories]]
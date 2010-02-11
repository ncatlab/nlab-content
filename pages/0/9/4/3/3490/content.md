
#Contents#
* automatic table of contents goes here
{:toc}

## Idea


The analog of the notion of [[subcategory]] for [[quasi-categories]].

## Definition

Let $C$ be a [[quasi-category]] and write $hC := Ho(C)$ for its [[homotopy category of an (∞,1)-category]] (hom-wise the connected components of the corresponding [[simplicially enriched category]]).

Let $hD \hookrightarrow hC$ be an ordinary [[subcategory]] of $hC$. Then the corresponding (ordinary) [[pullback]] $D$ of [[simplicial set]]s

$$
  \array{
    D &\to& C
    \\
    \downarrow && \downarrow
    \\
    hD &\to& hC
  }
$$

is the **sub-quasi-category** $D$ of $C$ spanned by $hD$. (Here in the bottom line of the pullback diagram we implicitly identify categories with their [[nerve]]s).

This is called a **full** sub-quasi-category if $hD$ is a [[full subcategory]] of $Ho(C)$. In this case the inclusion $D \to C$ is a [[full and faithful (∞,1)-functor]].

+--{: .query}
[[Mike Shulman]]: Over at [[subcategory]] we sort of decided that when speaking non-evilly, a "1-subcategory" is a fully faithful functor, and a "2-subcategory" is a faithful functor.  By analogy, a fully faithful $(\infty,1)$-functor would be called a 1-subcategory, while a "2-subcategory" would be an $(\infty,1)$-functor such that each hom-action $C(x,y)\to D(F x, F y)$ is fully faithful as a map of $\infty$-groupoids, i.e. equivalent to the inclusion of some subset of connected components.  Am I correct in guessing that the "sub-quasicategories" defined here are precisely the 2-subcategories in this sense?

[[Urs Schreiber]]: thanks, good point. That sounds plausible, given what the above pullback diagram expresses. Let me think about it...

=--


## References

section 1.2.11 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects sub-quasicategory]]
[[!redirects subquasicategory]]
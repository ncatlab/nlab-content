
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

## References

section 1.2.11 in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects sub-quasicategory]]
[[!redirects subquasicategory]]
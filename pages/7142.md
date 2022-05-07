
# Kan objects
* table of contents
{: toc}

## Idea

A Kan object $X$ in a category $C$ is a [[simplicial object]] in $C$ satisfying a generalized [[Kan complex|Kan condition]].

This generalization of the notion of [[Kan complex]] takes into account that the category in which $X$ is a simplicial object (namely $C$) is now not equal to, but only enriched over, the category in which the [[horn|horns]] on which the horn-filler condition (the Kan condition) is imposed are simplicial objects (namely $Set$).

Note that a Kan object in a category other than $\Set$ is not per se (a model for) an [[internal infinity-groupoid|internal ∞-groupoid]] (discussed there).

## Motivation

Recall that in the unenriched case (i.e. $C=Set$) a [[simplicial set]] $X$ is a [[Kan complex]] if the following equivalent conditions are satisfied.

1. The map $X\to *$ is a [[Kan fibration]]. This means for all $n\in\mathbb{N}$ and for all $0\le k\le n$ and for all $h_{k , n}$ the is a morphism $\exists_{h_{k, n}}$ making $\array{\Lambda^k[n]&\xrightarrow{h_{k , n}}&X\\\downarrow^{\iota_{k,n}}&\nearrow_{\exists_{h_{k,n}}}&&\\\Delta[n]&&}$ commute where the $\iota_{k,n}$ are the [[horn|horn inclusions]].

1. $hom_\sSet(\Delta[n],X)\to \hom_\sSet(\Lambda^k[n],X)$ is an epimorphism in $\Set$ for all $n$ and all $0\le k\le n$ where $\sSet$ is regarded as a $\Set$-[[enriched category]].


## Definition

+-- {: .num_defn}
###### Definition
Let $C$ be a category, and let $X:\Delta^{op}\to C$ be a [[simplicial object]] in $C$.

The **object of k-horns of n-simplices of**  $X$ is defined to be the [[weighted limit]] $\X^{\Lambda_n^k}\coloneqq \lim_{\Lambda_n^k}X$

$X$ is called a **Kan object** (in $C$) if $X[n]\to \X^{\Lambda_n^k}$ is an [[epimorphism]] for all $n$ and all $0\le k\le n$.  We obtain a family of related notions by requiring these maps to be different kinds of epimorphisms (regular, split, etc.).

=--

Note that this condition---called the **internal horn-filler condition**---coincides with the usual horn-filler condition (i.e. the Kan condition) if $C=\Set$, since for $V$-enriched functors $F:K\to C$ and $W:K\to V$ we have in the case $V=C$ that the [[weighted limit]] $\lim_W F=[K,V](W,F)$ coincides with the [[hom object]]; so in particular $X^{\Lambda_n^k}=\sSet(\Lambda_n^k,X)$.


## Examples

[[Kan simplicial manifolds]] form one possible generalization of [[Lie groupoids]].

If a [[variety of algebras]] $V$ contains a [[Malcev operation]],
then every [[simplicial object]] in $V$ is Kan.

## Related entries

* [[Kan complex]]

* [[Kan simplicial manifold]]

* [[Malcev operation]]

[[!redirects Kan object]]
[[!redirects Kan objects]]

category: ∞-groupoid

category: simplicial object

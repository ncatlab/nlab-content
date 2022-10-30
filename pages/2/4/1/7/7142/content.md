[[!redirects Kan complex]]

## Idea

A Kan object $X$ in a category $C$ is a [[simplicial object]] in $C$ satisfying a generalized [[Kan complex|Kan condition]].

This generalization of the notion of [[Kan complex]] takes into account that the codomain of $X$ is now not equal but only enriched over the codomain of the [[horn|horns]] on which the horn-filler condition (the Kan condition) is imposed.

Note that a Kan object in a category other than $\Set$ is not per se (a model for) an [[internal infinity-groupoid|internal ∞-groupoid]] (discussed there).

## Motivation

Recall that in the unenriched case a [[simplicial set]] $X$ is a [[Kan complex]] if the following equivalent conditions are satisfied

1. The map $X\to *$ is a [[Kan fibration]]. This means for all $n\in\mathbb{N}$ and for all $0\le k\le n$ and for all $h_{k , n}$ the is a morphism $\exists_{h_{k, n}}$ making $\array{\Lambda^k[n]&\xrightarrow{h_{k , n}}&X\\\downarrow^{\iota_{k,n}}&\nearrow_{\exists_{h_{k,n}}}&&\\\Delta[n]&&}$ commute where the $\iota_{k,n}$ are the [[horn|horn inclusions]].

1. $hom_\sSet(\Delta[n],X)\to \hom_\sSet(\Lambda^k[n],X)$ is an epimorphism in $\Set$ for all $n$ and all $0\le k\le n$ where $\sSet$ is regarded as a $\Set$-[[enriched category]].

1. $[\Delta^k[n],X]\xrightarrow{d} K_n:=\{(x_0,...,x_{k-1},x_{k+1},...,x_n|d_i x_j =d_{j-1} x_i, i\neg = k, j\neg =k, i\lt j\}$ is a bijection where $d_i$ denotes the i-th face map and $d:=d_0\times...\times d_{k_1}\times d_{k+1}\times...\times d_n$.


## Definition

+-- {: .num_defn}
###### Definition
Let $C$ be a category, let $X:\Delta^{op}\to C$ be a [[simplicial object]] in $C$.

The **object of  k-horns of n-simplices of**  $X$ is defined to be the [[weighted limit]] $\X^{\Lambda_n^k:}=\lim_{\Lambda_n^k}X$

$X$ is called **Kan object in** $X$ if $X[n]\to \X^{\Lambda_n^k}$ is an $C$-epimorphism for all $n$ and all $0\le k\le n$.

Note that this condition -called **internal horn-filler condition**- coincides with the usual horn-filler condition (i.e. the Kan condition) if $C=\Set$ since for $V$-enriched functors $F:K\to C$ and $W:K\to V$ we have in case $V=C$ that the [[weighted limit]] $\lim_W F=[K,V](W,F)$ coincides with the [[hom object]]; so in particular $X^{\Lambda_n^k}=\sSet(\Lambda_n^k,X)$.


=--


category: groupoid, ∞-groupoid, simplicial object
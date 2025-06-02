
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


# Sound doctrines

* table of contents
{: toc}

## Idea

A [[class]] $\Phi$ of [[diagram]] shapes for [[limits]] --- or more generally a class of [[weighted limits|weights]] for limits --- is called *sound* as a *[[doctrine]] of limits* &lbrack;[Adámek, Borceux, Lack & Rosicky (2002)](#AdámekBorceuxLAckRosicky2002)&rbrack; if it behaves nicely when paired with the class $\Phi^+$ of all [[colimit]] shapes (or weights) that [[commutativity of limits and colimits|commute]] with $\Phi$-limits in [[Set]] (or more generally in the [[enriched category|base of enrichment]]).

## Definition

A collection of small categories $\mathbb{D}$ is a doctrine if, seen as a full subcategory of $Cat$, it is essentially small.


A doctrine is said to be sound if for every small category $C$ the following are equivalent.

1. For every $D \in \mathcal{D}$ and any functor $D^{op} \to C$ the corresponding category of cocones is connected.

2. $C$-colimits commute with $D$-limits in $Set$ for all $D \in \mathbb{D}$.

Note that we always have $2. \implies 1.$, [Adámek, Borceux, Lack, Rosicky, Prop.2.1]. A category $C$ satisfying 2. is called $\mathbb{D}$-filtered.

## References

* {#AdámekBorceuxLackRosicky2002} [[Jiří Adámek]], [[Francis Borceux]], [[Stephen Lack]], [[Jiri Rosicky]], *A classification of accessible categories*, Journal of Pure and Applied Algebra **175** 1–3 (2002)  7-30 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(02)00126-3">doi:10.1016/S0022-4049(02)00126-3</a>&rbrack;

* [n-Cafe discussion about the above paper](https://golem.ph.utexas.edu/category/2014/05/classifying_by_generalizing_th.html)


* C. Centazzo, [[J. Rosický]], [[E. M. Vitale]], _A characterization of locally D-presentable categories_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, Volume 45 (2004), no. 2, pp. 141-146.  [numdam](https://www.numdam.org/item/CTGDC_2004__45_2_141_0/).

* [[Stephen Lack]], [[Jiri Rosicky]], *Notions of Lawvere theory*, [arxiv](https://arxiv.org/abs/0810.2578)

* Mat&#283;j Dost&#225;l, Ji&#345;&#237; Velebil, *An elementary characterisation of sifted weights*, [arxiv](https://arxiv.org/abs/1405.3090)

* [[G. M. Kelly]], V. Schmitt, *Notes on enriched categories with colimits of some class*, [arXiv](https://arxiv.org/abs/math/0509102)

[[!redirects sound doctrines of limits]]

[[!redirects doctrine of limits]]
[[!redirects doctrines of limits]]

[[!redirects sound doctrine]]
[[!redirects sound doctrines]]



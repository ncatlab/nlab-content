[[!redirects II.9, unipotent affine groups, decomposition of affine groups]]
This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

+-- {: .num_theorem}
###### Theorem
Let $G$ be an [[affine scheme|affine]] [[group scheme|k-group]]. Then the following conditions are equivalent.

1. The [[completion]] of the [[Cartier duality|Cartier dual]] $\hat D(G)$ of $G$ is a connected formal group.

1. Any [[multiplicative group scheme|multiplicative subgroup]] of $G$ is zero.

1. For any subgroup $H$ of $G$ with $H\neq 0$ we have $Gr_k(H,\alpha_k)\neq 0$.

1. Any algebraic quotient of $G$ is an extension of subgroups of $\alpha_k$.

1. (If $p\neq 0)$, $\cap Im V^n_G =e$.
=--

+-- {: .num_defn}
###### Definition and Remark
1. A group satisfying the conditions of the previous theorem is called *[[unipotent k-group]]*.

1. Unipotent groups correspond by duality to connected formal $k$-groups.

1. The category $ACu_k$ of affine commutative unipotent groups form a thick subcategory of $AC_k$ which is stable under limits.
=--

The following theorem is the dual to the theorem of the previos chapter.

+-- {: .num_theorem}
###### Theorem
1. An affine $k$ group is in a unique way an extension of a unipotent group by a multiplicative group.

1. This extension splits if $k$ is perfect.

1. If $k$ is perfect any finite group is uniquely the product of four subgroups which are respectively [[étale group scheme|étale]] multiplicative, &#233;tale unipotent, [[infinitesimal group scheme|infinitesimal]] multiplicative and infinitesimal unipotent.

1. The category $F_k$ of finite commutative $k$-groups splits as a product of four subcategories: $Fem_k$, $Feu_k$, $Fim_k$, $Fiu_k$.

1. The categories $Feu_k$ and $Fim_k$ are dual to each other.

1. The categories $Fem_k$ and $Fiu_k$ are selfdual.
=--

+-- {: .num_prop}
###### Proposition
1. Let $p = 0$, then Then $F_k=Fem_k$.

1. Let $p\neq 0$, let $k$ be algebraically closed. Then any commutative finite $k$-group is an extension of copies of $p \alpha_k$, $p \mu_k$ and $(\mathbb{Z}/r\mathbb{Z})_k$ where $r$ is prime.
=--

+-- {: .num_cor}
###### Corollary
If $m$ is a prime and $G$is a finite commutative $k$-group, then$m^\alpha id_G=0$ for large $\alpha$ iff $rk(G)$ is a power of $m$.
=--
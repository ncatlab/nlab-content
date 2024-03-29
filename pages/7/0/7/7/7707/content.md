[[!redirects III.3, the Witt rings over k]]
This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

Let $k$ be a field of prime characteristic $p$. Let $W$ denote the [[Witt ring over Z]]

+-- {: .num_defn}
###### Definition
The **Witt ring over $k$** denoted by is defined by the coefficient extension $W_k:=W\otimes_\mathbb{Z} k$. and $W_{nk}:=W_n\otimes_\mathbb{Z}k$

The [[Witt ring over Z|phantom-components]] $W_k\to \alpha_k$ reduce now to $(a_i)_{0\le i\le n}\mapsto a_0^{p^n}$.

Since $W_k=W_{F_p}\otimes_{F_p}k$ we can identify $W_k^{(p)}$, see Definition [[Frobenius morphism]],  and $W_k$ and the [[Frobenius morphism]] becomes the endomorphism

$$F:\begin{cases}W_k\to W_k\\(a_0,\dots,a_n,\dots)\mapsto (a_0^p,\dots,a_n^p,\dots)\end{cases}$$

This is a ring morphism since since $F$ commutes with products. Similar statements are true for $W_{nk}$ and the affine $k$-group $\Lambda_k$ defined in [[Artin-Hasse exponential series]].
=--

+-- {: .num_prop}
###### Proposition
1. The [[Verschiebung morphism]] of $\Lambda_k$ is given by $\phi(t)\to \phi(t^p)$.

1. The Verschiebung morphism of $K_k$ is the [[Witt ring over Z|translation]] $T$.

1. The Verschiebung morphism of $W_nk$ is $R \cdot T=T\cdot R$.

1. If $x,y\in W_k(R)$, $R\in M_k$, then $V(F x\cdot y)=x\cdot V y$.
=--

+-- {: .num_cor}
###### Corollary

=--

+-- {: .num_cor}
###### Corollary

=--

+-- {: .num_cor}
###### Corollary
Let $k$ be perfect. Then

1. $W(k)$ is a discrete valuation ring.

1. $W(k)$ is complete.

1. $W(k)/p W(k)=k$
=--

+-- {: .num_prop}
###### Proposition
(Witt)
Let $k$ be perfect, let $A$ be compete, noetherian local ring with residue field $k$. Let $\pi:A\to k$ be the canonical projection. There exists a unique ring morphism

$$u:W(k)\to A$$

which is compatible with the projections $W(k)\to k$ and $\pi:A\to k$.

If moreover $A$ is a discrete valuation ring with $p\cdot 1_A\not 0$, then $A$ is a free finite $W(k)$-module of rank $[A/p : A]$.

In particular if $pA=A$, then $u$ is an isomorphism. 
=--
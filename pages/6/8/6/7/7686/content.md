[[!redirects II.7, étale and connected formal k-groups]]
This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

[[étale group scheme|Étale]] affine (resp. &#233;tale formal) $k$-groups are equivalent to finite (resp. all) Galois modules by

$$E\to E\otimes_{k_s}k^\prime=\coprod_{K/k\;\text{separable}}E(k)$$


$G$ is etale iff $ker F_G=e$. This implies that $F$ is an isomorphism.

+-- {: .num_defn}
###### Definition

A $k$-formal group $G=Spf A$ is called  *[[local formal group scheme|local]]* (or *connected*) if the following two equivalent conditions hold:

1. $A$ is local

1. $G(k)=\{0\}$ for any field $K$.

=--

A morphism from a connected group to an &#233;tale group is zero.

+-- {: .num_prop}
###### Proposition
Let $G$ be a $k$-formal group.

1. Then there is an exact sequence

$$0\to G^\circ\to G\to \pi_\circ(G)\to 0$$

where $G^\circ$ is connected and $\pi_\circ(G)$ is &#233;tale. If $R\in Mf_k$ is a finite dimensional $k$-ring and $n_0$ is the [[nilradical]] (i.e. -if $R$ is commutative- the set of all nipotent elements) of $R$ then 

$$G^\circ(R)=ker(G(R)\to G(R/n_0))$$

If $p$ is not $0$, then

$$G^\circ= lim_n \; ker(F\,G^{(p^n)})$$

If $k\to k^\prime$ is a [[field extension]] then $(G\otimes_k k^\prime)^\circ =G^\circ\otimes_k k^\prime$, and $\pi_0(G\otimes_k k^\prime)=\pi_0(G)\otimes_k k^\prime$.

2. If $k$ is perfect, there is a unique isomorphism $G=G^\circ\times \pi_0(G)$
=--

+-- {: .num_defn}
###### Definition

An affine $k$-group $G$ is called *infinitesimal* if it one of the followig conditions is satisfied:

1. $G$ is finite and local.

1. $G$  is algebraic and $G(cl(k))=e$ (the terminal $k$-group)
=--

+-- {: .num_cor}
###### Corollary
A finite group is an extension of an &#233;tale group by an infinitesimal group.

This extension splits if $k$ is perfect.
=--

+-- {: .num_defn}
###### Definition
A (not necessarily commutative) connected formal $k$-group $G=Spf A$ is said to be *of finite type* if $A$ is noetherian. The *dimension of $G$* is defined to be the [[Krull dimension]] of $A$.
=--

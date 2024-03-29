[[!redirects II.11, p-divisible formal groups]]
This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

Let $k$ be a field of prime characteristic $p\gt 0$.

## Definition

+-- {: .num_defn}
###### Definition
($p$-divisible group)

A commutative formal $k$-group $G$ is called *[[p-divisible group|p-divisible formal k-group]]* or *Barsotti-Tate group* if it satisfies the following properties:

: (pdg1) $p\cdot id_G\to G$ is an epimorphism.

: (pdg2) $G$ is a $p$-torsion group in that $G=\cup_j ker(p^j \cdot id_G)$

: (pdg3) $ker(p\cdot id_G)$ is finite.

We have $rk(ker \,p \cdot id_G)=p^h$, $h\in \mathbb{N}$. This $h$ is called the *height $ht(G)$ of $G$*.
=--

+-- {: .num_rem}
###### Definition
(alternative definition of $p$-divisible group)

 Let

$$G_1\stackrel{i_1}{\to}G_2\stackrel{i_2}{\to}G_3\stackrel{i_3}{\to}\cdots$$

be a codirected diagram of [[finite k-group|finite k-groups]] such that

1. $rk(G_j)=p^{h j}$, $h$ a fixed integer,

1. all sequences $0\stackrel{}{\to}G_j\stackrel{i_j}{\to}G_{j+1}\stackrel{p^j}{\to}G^{j+1}$ are exact.

Then $colim_n G_n$ is a $p$-divisible group of height $h$ and $ker(p^n id_G:G\to G)\simeq G_n$.
=--

+-- {: .num_remark}
###### Remark

If $G$ is a p-divisible group in the sense of the first definition, from (pdg1) follows $rk(ker p^j \cdot id_G)0p^{j\cdot ht (G)}$. Since $rk$ is multiplicative

$$0\to ker \,p^j\hookrightarrow ker \,p^{j+k}\stackrel{p^j}{\to}ker\, p^k\to 0$$

is exact.
=--

+-- {: .num_defn}
###### Definition
([[Serre dual]] of a $p$-divisible group)

Let $G$ be a $p$-divisible group $G$. The *Serre dual* $G^\prime$ of $G$ is defined by: let $G_j:=ker(p^j id_G)$ and let $p_j:G_{j+1}\to G_j$ is the map induced by $p id_G$. Then we define

$$G_j^\prime:=D(G_j)$$

$$i_j^\prime:=D(p_j):G^\prime_j\to G^\prime_{j+1}$$

$$G^\prime:=colim_{j^\prime}G_j^\prime$$

This is a $p$-divisible formal group with $ht(G^\prime)=ht(G)$ and we have $p_j^\prime=D(i_j)$ and $(G^\prime)^\prime\simeq G$.

=--

## Examples

+-- {: .num_example}
###### Example
Let $\mathbb{Z}_p$ denote the [[p-adic number|ring of p-adic integers]], let $\mathbb{Q}_p$ denote the [[p-adic number|field of p-adic numbers]]. The constant formal group $(\mathbb{Q}_p /\mathbb{Z}_p)_k$ is a $p$-divisible group of height $1$.

Conversely any $p$-divisible group of height $h$ is isomorphic to $(\mathbb{Q}_p /\mathbb{Z}_p)^h_k$.

=--

+-- {: .num_example}
###### Example
Let $A$ be a commutative [[algebraic group|algebraic k-group]], such that $p id_G:A\to A$ is an epimorphism. Then

1. $ker(p\cdot id_A)$ is finite.

1. $A(p):=\cup_j ker(p^j id_A)$ is a $p$-divisible group containing $\hat A^\circ=\cup_j ker(F^j G)$.

1. If $A=\mu_k$ we have $A(p)=\cup_j p^j \mu_k=(\mathbb{Q}_p /\mathbb{Z}_p)^\prime_k$.

1. If $A$ is an abelian variety of dimension $g$ $p id_A$ is an epimorphism with $rk(her p id_G)=p^{2g}$ and consequently $A(p)$ is a $p$-divisible group of height $2g$. This example is further described in chapter [[V, p-adic cohomology of abelian varieties]], particularly in [[V.3, structure of the p-divisible group A(p)]].
=--

+-- {: .num_prop}
###### Proposition
Let $G$ be a $k$-formal group. Then $G$ is $p$-divisible iff the following conditions hold:

1. $\pi_\circ(G)(\overline k)\simeq (\mathbb{Q}_p /\mathbb{Z}_p)^r$, $r$ finite.

1. $G^\circ$ is of finite type, smooth, and $ker(V:G^{\circ (p)}\to G^\circ)$ is finite.
=--

+-- {: .num_example}
###### Example
Let $A$ be an algebraic unipotent $k$-group, then $\hat A^\circ$ is never $p$-divisible unless $A$ is finite.
=--

+-- {: .num_remark}
###### Remark
Let $G$ be $p$-divisible. Then we have $height(G)=dim(G)+dim(G^\prime)$
=--

+-- {: .num_prop}
###### Proposition
Let $G$ be a connected, finite type, smooth formal group. There exist two subgroups $H$,K\subseteq G$ with $H$ is $p$-divisible, $p^n K = 0$ for large $n$, $H\cap K$ is finite, and $G=H+ K$.
=--

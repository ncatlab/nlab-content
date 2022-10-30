[[!redirects II.10, smooth formal groups]]


This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

+-- {: .num_defn}
###### Definition
A not necesarily commutative connected formal group $G=\Sp f A$ is called *[[smooth formal k-group]] if $A$ is a power-series algebra $k[ [X_1,...X_n] ]$ in $n$ variables

The coproduct $\Delta:A\to A\hat \otimes A$ is given by a set af formal power series $\Phi(X,Y)=(\Phi_i(X_1,..., X_n, Y_1,..., Y_n)), i_1,...,n$ satisfying the axioms (Ass),(Un) and (Com). Such a set $\{\Phi_i\}$ is called a *Dieudonn&#233; group law*.
=--

+-- {: .num_theorem}
###### Theorem
Let $G=Sp f A$ be a (not necessarily commutative) connected formal group of finite type.
1.If $p=0$ then $G$ is smooth.

1. If $p\not =0$ then the following conditions are equivalent


1. $G$ is smooth

1. $A\otimes_k k^{p-1}$ is reduced.

1. $F_G$ is an epimorphism.
=--

The previous theorem can be strengthened:

+-- {: .num_theorem}
###### Theorem
(Cartier)

Let $p=0$, let $G=Sp^* C$ be a connected (not necessarily commutative) formal $k$-group (realized as the [[spectrum of a coring|formal spectrum of a k-coring]] $C$).

1. $C$ is the universal enveloping algebra of the Lie algebra $\mathcal{g}$ of $G$.

1. The category of connected formal $k$-groups is equivalent to the category of all Lie algebras over $k$.

1. If $\mathcal{g}$ is finite dimensional then $G$ is smooth.

1. If $G$ is commutative $\mathcal{g}$ is abelian.

1. $G\simeq (\alpha^\circ)^{(I)}$; by duality any unipotent (commutative) $k$-group is a power of the additive group.
=--

+-- {: .num_theorem}
###### Theorem
(Dieudonn&#233;-Cartier-Gabriel)
Let $p\gt 0$, let $k$ be a [[perfect field]] of [[characteristic]] $p$ let $G=Sp^* C$ be a connected (not necessarily commutative) connected formal $k$[[k-group of finite type|-group of finite type]], let $H$ be a subgroup of $G$, let $G/H:=Spf A$ (this quit ion has not been defined in these lectures).

Then $A$ is of the form

$$k [ [ X_1,\dots,X_n] ][Y_1,\dots,Y_d]/(Y_1^{p^{r_1}},\dots,Y_d^{p^{r_d}})$$

This applies for instance to $A=\hat O_{G,e}$, for an [[algebraic group]] $G$.

=--

+-- {: .num_cor}
###### Corollary
Let $p\ge 0$, let $G$ be a [[connected formal group]] (=local formal group) of [[formal group of finite type|finite type]]. Then

1. If $k$ is prefect, there exists a unique exact sequence of connected groups

$$0\to G_{red}\to G\to G/G_{red}\to 0$$

with $G_{red}$ smooth and $G/G_{red}$ [[infinitesimal k-group|infinitesimal]].

2. For large $r$, the group $G/ker F^r_G$ is smooth.
=--

+-- {: .num_cor}
###### Corollary
Let $G$ be a connected formal group of finite type, let $n:=dim G$. Then $rk(co her F^i_G)$ is bounded and

$$rk(ker F^i_G)=p^{n i}\cdot rk(coker F^i_G)$$
=--

+-- {: .num_cor}
###### Corollary
1. Let $0\to G^\prime\to G\to G^n\to 0$ be an exact sequence of connected formal groups. Then $dim(G)=dim(G^\prime)+dim(G^n)$.

2. If $f:G^\prime \to G$ is a morphism of connected formal groups, with $G$ smooth and $dim G=dim G^\prime$, then $f$ is an epimorphism iff $ker f$ is finite.
=--
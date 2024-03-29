[[!redirects III.6, Dieudonné modules (p-torsion finite k-groups)]]


This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

Recall from [[relation of certain classes of k-groups]] the following:

1. $Feu_k$ denotes the category of formal &#233;tale unipotent affine $k$-groups.

1. $Fiu_k$ denotes the category of formal infinitesimal unipotent $k$-groups.

1. $W(k)$ denotes the Witt ring over $k$.

1. For $D_k$ see [[D_k-module]] in [[III.5, Dieudonné modules (affine unipotent groups)
]].

1. $$M:\begin{cases}
Acu_k&\to& W(k)-Mod
\\
G&\mapsto&M(G)
\end{cases}$$

is a contravariant functor from affine commutative unipotent $k$-groups to the category of $W(k)$-modules.

Recall moreover from [[III.5, Dieudonné modules (affine unipotent groups)
]] that $Tor_V D_k-Mod:=Acu_k(G,W_{nk})=\{m\in M(G)|V^n m =0\}$ is a submodule.

which are $W(k)$-modules of finite length, killed by a power of $V$, Definition [[Verschiebung morphism]], and on which $F$, Definition [[Frobenius morphism]], is bijective  (resp. and killed by a power of $F$).

+-- {: .num_prop}
###### Proposition
(formulation of the statement is unclear)
The functor

$$M:\begin{cases}
Acu_k&\to& W(k)-Mod
\\
G&\mapsto&M(G)
\end{cases}$$

which is a contravariant functor from affine commutative unipotent $k$-groups to the category of $W(k)$-modules induces the following contravariant equivalences of categories:


1. $Feu_k\to Tor_V D_k-Mod\hookrightarrow M(G)$ between the category of affine &#233;tale unipotent $k$-groups to the category of $W_k$-modules of finite length, killed by a power of $V$ on which $F$ is bijective.

1. $Fiu_k\to Tor_F D_k-Mod\hookrightarrow M(G)$ between the category of affine &#233;tale unipotent $k$-groups to the category of $W_k$-modules of finite length, killed by a power of $F$ (and killed by a power of $V$ ?)on which $F$ is bijective.

([Demazure p.69](#lecturesOnPDivGroups))
=--

+-- {: .proof}
###### Proof
This follows from the theorem, and the fact that if $G$ is finite, then G is &#233;tale (resp, infinitesimal) if and only if $F_G$ is an isomorphism (resp. $F_G^n = 0$ for large $n$). 
=--

+-- {: .num_example}
###### Example
1. If $G=(\mathbb{Z}/p\mathbb{Z})_k\in Feu_k$, then $M(G)=k$ with $F=1$, $V=0$.

1. If $G=p \alpha_k\in Fiu_k$, then $M(G)=k$ with $F=0$, $V=0$.
=--

+-- {: .num_cor}
###### Corollary
For $G\in Feu_k$ or $G\in Fiu_k$, we have

$$rk(G)= p^{length(M(G))$$
=--

+-- {: .num_prop}
###### Proposition
Let $m,n$ be two positive integers. Then

1. The canonical injection $m^{W_n}\to W_n$ defines an element $u\in M(m^{W_n})$ satisfying $V^n u= F^n= 0$. This gives a map

$$\lambda_{n,m}: D_k/(D_k F^m + D V^n)\to M(m^W_n)$$

which is bijective.
=--

+-- {: .num_theorem}
###### Theorem
There is an isomorphism

$$M(D(G))\to M(G)^*$$

In prose this means that the autoduality $G\mapsto D(G)$ of $Fiu_k$ corresponds via the Dieudonn&#233;-functor $M$ to the autoduality $M\to M^*$ in the category $fin Tor_{V,F}D_k-Mod$ of $D_k$-modules of finite length killed by a power of $V$ and $F$.
=--

+-- {: .num_defn}
###### Definition
(Dieudonn&#233;-module of an infinitesimal multiplicative $k$-group)

Let $G\in Fim_k$. Then the *Dieudonn&#233;-module of $M(G)*$ is defined by

$$M(G)=M(D(G))^*$$

It follows by the [[Cartier duality]] between $Fim_k$ and $Feu_k$ that the functor $G\mapsto M(G)$ induces a contravariant equivalence

$$Fim_k\to  fin Tor_F Bij_V D_k-Mod$$

between $Fim_k$ and the category of all $D_k$-modules of finite length on which $F$ is nilpotent and $V$ is bijective.
=--

+-- {: .num_remark}
###### Remark
Let $G\in Fimd_k$ (i.e. $G\in Fim_k$ and $G$ diagonalizable). 

$G=D(\Gamma_k)$. Then $D(G)\simeq \Gamma_k$, and

$M(D(G))=colim Acu_k(\Gamma_k,W_{nk})=colimGr(\Gamma,W_n(k))=Gr(\Gamma,W_\infty)=Mod_{W(k)}(W(k)\otimes_\mathbb{Z},W_\infty)=Mod_{W(k)}(W(k)\otimes_\mathbb{Z} \Gamma, W_\infty)$

and hence

$$M(G)\simeq(W(\overline k)\otimes_\mathbb{Z}\Gamma)^\pi$$

where $W_\infty=Quot(W(k))/W(k)=colim_n W_n(k)=\underline W(k)$, see p.66.

For $F$ and $V$ we have

$$F(\lambda \otimes \chi)=\lambda^{(p)}\otimes p\chi$$

$$V(\lambda \otimes \chi)=\lambda^{(p^{-1})}\otimes p\chi$$
=--

+-- {: .num_theorem}
###### Theorem
a) The Dieudonn&#233; functor

$$\begin{cases}
F_p_k=Fiu_k\times Feu_k\times Fim_k\to (fin W(k)-Mod,F,V)
\\
G\to M(G)
\end{cases}$$

is a contravariant equivalence between all finite $k$-groups of $p$-torsion, and the category of all triples $(M,F_M,V_M)$ where $M$ is a finite length $W(k)$-module and $F_M$, $V_M$ two group endomorphisms of $M$ satisfying

$$F_M(\lambda m)=\lambda^{(p)} F_M(m)$$

$$V_M(\lambda^{(p)}m)=\lambda V_M(m)$$

$$F_M V_M=V_M F_M=p\cdot id_M$$

b) $G$ is &#233;tale, infinitesimal, unipotent or multiplicative according as $F_M$ is isomorphic, $F_M$ is nilpotent, $V_M$ is nilpotent, or $V_M$ is isomorphic

c) For any $G\in Fp_k$ we have $rk(G)=p^{length M(G)}$.

d) If $k$ is a perfect extension of $k$, there exists a functorial isomorphism

$$M(D(G))=M(G)^*$$
=--



## References

{#lecturesOnPDivGroups} Michel Demazure, lectures on p-divisible groups [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)
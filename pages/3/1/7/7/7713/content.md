[[!redirects III.4, duality of finite Witt groups]]


This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

+-- {: .num_remark}
###### Remark

Let $m, n\gt 1$ and define $m^{W_n}:=ker(F^m:W_{nk}\to W_{nk})$. Then there are morphisms

$$\array{
m^{W_n}
&\stackrel{t}{\to}&
m^{W_{n+1}}
\\
\downarrow^f&&\downarrow^r
\\
{m-1}^{W_n}
&\stackrel{i}{\hookrightarrow}&
m^{W_n}
}$$

where $i$ is the canonical inclusion, and $r,f,t$ are induced by $R,F,T$ where $F$ is [[Frobenius morphism|Frobenius]], $T$ is [[Witt ring|Verschiebung]] and $R:W\to W_n$ is [[Witt ring|restriction]]. $i$ and $t$ are monomorphisms, $f$ and $r$ are epimorphisms, and for $m^{W_n}$ we have $F=if$ and $V=rt$.
=--

+-- {: .num_defn}
###### Definition and Remark

1. For $R\in M_k$, let $W^\prime(R)$ be the set of all $(\alpha_0,\alpha_1,\dots)\in W_k(R)$ such that $a_n=0$ for large $n$, and $a_n$ nilpotent for all $n$.

1. $W^\prime(R)$ is an ideal in $W_k(R)$.

1. $E(w,t)$ is a polynomial for $w\in W^\prime(R)$.

1. In particular $E(w,1)$ is defined for $w\in W^\prime(R)$, and we have a morphism of groups

$$\tilde E:
\begin{cases}
W^\prime\to \mu_k
\\
w\mapsto E(w,1)
\end{cases}$$

If $x\in W_k(R)$, $y\in W^\prime(R)$ then $xy\in W^\prime(R)$ and $E(xy,1)\in R^*$. (...)

The morphism
$$\begin{cases}
W\times W^\prime\to \mu_k
\\
(x,y)\mapsto E(xy,1)
\end{cases}$$
 is bilinear and hence gives a morphism of groups

$$W^\prime\to D(W_k)$$

which is an isomorphism.
=--

+-- {: .num_defn}
###### Definition
Let

$$\sigma_n:\begin{cases}
W_{nk}\to W_k
\\
(\alpha_0,\dots,\alpha_{n-1})\mapsto(\alpha_0,\dots,\alpha_{n-1},0,\dots)
\end{cases}$$
be the section of $R_n:W_k\to W_{nk}$.

$\sigma_n$ is not a morphism of groups. $\sigma_n$ sends $m^{W_n}$ in $W^\prime$.
=--

+-- {: .num_theorem}
###### Theorem
For $x\in m^{W_n}(R)$, $y\in n^{W_m}(R)$, define

$$\lt x,y\gt:=E(\sigma_n(x)\sigma_m(y),1)$$

then $\lt x,y\gt$ is bilinear and gives an isomorphism

$$m^{W_n}\simeq D(n^{W_m})$$

and satisfies

$$\lt x,t y\gt=\lt f x,y\gt$$

$$\lt x,r y\gt=\lt i x,y\gt$$
=--
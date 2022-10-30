[[!redirects III.1 the Artin-Hasse exponential series]]
This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

Let $p$ be a fixed prime number.

+-- {: .num_defn}
###### Definition
Let $k$ be a ring. Then the assignation

$$\Lambda_k:\begin{cases}
M_k&\to&R[[t]]
\\
R&\to&1+tR[[t]]
\end{cases}$$

sending a [[k-ring]] to the multiplicative group of formal power series with coefficients in $R$ and constant term $1$ is an [[affine k-group]]. As a [[k-functor]] $\Lambda_k$ is equivalent to $O_k^\mathbb{N}$. 
=--

+-- {: .num_remark}
###### Remark
1. There is an exact sequence $0\to \Lambda_k^{(n+1)}\to \Lambda_k^{(n)}\to \alpha_k\to 0$

1. We have $\Lambda_k=lim_n \Lambda_k/\Lambda_k^{(n+1)}$.

1. Each $\Lambda_k /\Lambda_k^{(n+1)}$ is is an $n$-fold extension of the additive group $\alpha_k$.

1. If $k$ is a field then $\Lambda_k$ is a unipotent group.
=--

+-- {: .num_remark}
###### Remark
For $F=(1-t+\cdots )\in \Lambda(k)$ there is an isomorphism of $k$-schemes

$$\phi_F:\begin{cases}
O_k^{\mathbb{N}_{\gt 0}}\to \Lambda_k
\\
(a_n)\mapsto \Pi_n F(a_n t^n)
\end{cases}$$

If $k=\mathbb{Q}$ and $F(t)=exp(-t)$ we have $F(at)F(bt)=F(A(a+b)t)$ and $\phi_F$ is an isomorphism $\phi_F:\alpha_k^{\mathbb{N}_{\gt 0}}\to \Lambda_k$.

If $k$ is a field with characteristic $p$ it is not possible an $F$ such that $F(at)F(bt)=F(ct)$. However there is always a formula $F(at)F(bt)=\Pi_{i\gt 0} F(\lambda_i(a,b)t^i$ where $\lambda_i(X,Y)\in k[X, Y]$. This is verified by [[Möbius inversion]].
=--

+-- {: .num_remark}
###### Remark
([[Möbius inversion]])
Let $\mu$ be the M&#246;bius function. Then [[Möbius inversion]] gives
$$exp(-t)=\Pi_n (1-t^n)^{\mu(n)/n}$$
=--

+-- {: .num_defn}
###### Definition and Remark
The *Artin-Hasse exponential* is defined by the morphism

$$E:\begin{cases}
O^\mathbb{N}_{\mathbb{Z}_{(p)}}\to \Lambda_{\mathbb{Z}_{(p)}}
\\
((a_n),t)\mapsto \Pi_{n\ge 0}F(a_n t^{p^n})
\end{cases}$$

We have $E((a_i),t)E((b_i),t)=E((S_i(a_0,\dots,a_i,b_0,\dots,b_i),t)$ where $s_i\in \mathbb{Z}_{(p)}[X_0,\dots, X_i,Y_0,\dots, Y_i]$

$P\in \Lambda(R)$, $R\in M_{\mathbb{Z}_{(p)}}$ can be uniquely written as

$$P(t)=\Pi_{(n,p)=1} E((a_n),t^n)$$

where $(a_n)\in R^\mathbb{N}$
=--

+-- {: .num_prop}
###### Proposition
The $\mathbb{Z}_{(p)}$-group $\Lambda_{\mathbb{Z}_{(p)}}$ is isomorphic to the n/(n,p)=1-power of the subgroup image of $E$.

By base-change a similar statement applies to $\Lambda_{\mathbb{F}_p}$. This shows that the Artin-Hasse exponential plays over $\mathbb{F}_p$ a similar role as the usual exponential over $\mathbb{Q}$.
=--
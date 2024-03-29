[[!redirects III.2, the Witt rings over Z]]

This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)


The [[Artin-Hasse exponential series]] $E$ can be written as

$$E((a_0,\cdots),t)=exp(-\Sigma_{n\ge 0}t^{p^n}\Phi_n /p^n)$$

with $\Phi_n(a_0,\cdots)=a_0^{p^n} + p a_1^{p^{n-1}}+\dots p^n a_n$

The $S_i$ in the multiplication formula $E((a_i),t)E((b_i),t)=E((S_i(a_0,\dots,a_i,b_0,\dots,b_i),t)$ where $s_i\in \mathbb{Z}_{(p)}[X_0,\dots, X_i,Y_0,\dots, Y_i]$ of the Artin-Hasse exponential series can also be written as $\Phi_n(a_0,\cdots,a_n)+\Phi_n(d_0,\dots,b_n)=\Phi_n(S_0,\dots,S_n)$

+-- {: .num_lemma}
###### Lemma
We have $S_n\in\mathbb{Z}[X_0,\dots,X_n]$
=--

+-- {: .num_theorem}
###### Definition and Theorem
There exists a unique commutative group law $W$ on the $\mathbb{Z}$-group scheme $W:=O_\mathbb{Z}^\mathbb{N}$ called **$\mathbb{Z}$-group of Witt-vectors of finite length relative to $p$** satisfying the following properties:

1. $E:O_\mathbb{Z}^\mathbb{N}\otimes_\mathbb{Z} \mathbb{Z}_{(p)}\to \Lambda_{\mathbb{Z}_{(p)}}$ is a morphism of $k$-groups.

1. Each $\Phi_n:O_\mathbb{Z}^\mathbb{N}\to \alpha_\mathbb{Z}$  is a morphism of $k$-groups.

1. $(a_n)+(b_n)=(S_n(a_0,\dots, a_n,b_0,\dots,b_n))$

For $w=(a_n)\in W(R)=R^\mathbb{N}$, $a_n$ is called the *$n$-th component of $w$* and $\Phi_n(w)$ is called the *$n$-th phantom component of $w$*.  The phantom components of $w$ define a group isomorphism

$$W\otimes_\mathbb{Z}\mathbb{Z}[p^{-1}]\to \alpha^\mathbb{N}_{\mathbb{Z}[p^{-1}]}$$
=--

+-- {: .num_remark}
###### Remark and Definition
There is an endomorphism of the group of Witt vectors

$$T:\begin{cases}
W\to W
\\
(a_o,\dots,a_n,\dots)\mapsto(0,a_o,\dots,a_n,\dots)
\end{cases}$$
called translation.

We define the group $W_n$ of Witt vectors of length $n$ by $W_n(R):=co ker\, T^n(R)$ or equivalently by the exact sequence

$$\label{W_n}0\to W\stackrel{T^n}{\to}W\stackrel{R_n}{\to}W_n\to 0$$

and we have

1. $(a_0,a_1,\dots)=(a_0,\dots,a_{n-1},0,\dots)\overset{\bullet}{+} T^n(a_n,a_{n+1},\dots)$

1. The underlying scheme of $W_n$ is $O_k^n$, the projection morphism $W/to W_n$ is $(a_0,\dots,)\mapsto(a_0,\dots,a_{n-1}$.

1. The group law on $W_n$ is $(a_0,\dots,a_{n-1})\overset{\bullet}{+}(b_0,\dots,b_{n-1})=(S_0(a_0,b_0),\dots,S_{n-1}(a_0,\dots,a_{n-1},b_0,\dots,b_{n-1}))$

1. In particular $W_1=\alpha$

The [[snake lemma]] gives from diagram (1) translation morphisms $T:W_n\to W_{n+1}$ such that $T(a_0,\dots,a_{n-1})=(0,a_0,\dots,a_{n-1})$, projection morphisms $R_W_{n+1}\to W_n$ such that $R(a_0,\dots,a_n)=(a_0,\dots,a_{n-1})$ and exact sequence

$$0\to W_m\stackrel{T^n}{\to}W_{n+m}\stackrel{R^m}{\to}W_n\to 0$$

and the projections $W\to W_n$ give rise to an isomorphism

$$W\simeq lim_n W_n$$
=--

+-- {: .num_lemma}
###### Definition and Lemma
Let $\iota:\begin{cases}O_\mathbb{Z}\to W\\a\to(a,0,\dots)\end{cases}$ be an inclusion.

Then we have $\Phi_n \iota(a)=a^{p^n}$ and$E(\iota(a),t)=F(at)$).
=--

+-- {: .num_theorem}
###### Theorem and Definition

There is a unique ring-structure on the $\mathbb{Z}$-group $W$ such that either of the two following conditions is satisfied:

1. Each $\Phi_n:W\to O_\mathbb{Z}$ is a ring homomorphism.

1. $\iota(ab)=\iota(a)\iota(b)$, $a,b\in R\in M_\mathbb{Z}$.

The $\mathbb{Z}$-ring $W$ is called **Witt-Ring**, each $W_n$ is a quotient ring of $W$. The canonical morphisms $R_n:W\to W_n$ and $R:W_{n+1}\to W_n$ are ring homomorphisms (but not $T$).
=--
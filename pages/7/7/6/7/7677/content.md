## Definition

Let $p$ be a prime number, let $k$ be a field of characteristic $p$. For a $k$-ring $A$ we define

$$f_A:
\begin{cases}
A\to A
\\
x\mapsto x^p
\end{cases}$$

The $k$-ring obtained from $A$ by scalar restriction along $f_k:k\to k$ is denoted by $A_{f}$.

The $k$-ring obtained from $A$ by scalar extension along $f_k:k\to k$ is denoted by $A^{(p)}:=A\otimes_{k,f} k$.

There are $k$-ring morphisms $f_A: A\to A_f$ and $F_A:\begin{cases}
A^{(p)}\to A
\\
x\otimes \lambda\mapsto x^p \lambda
\end{cases}$. 

For a $k$-functor $X$ we define $X^{(p)}:=X\otimes_{k,f_k} k$ which satisfies $X^{(p)}(R)=X(R_f)$. The _Frobenius morphism_ for $X$ is the transformation of $k$-functors defined by

$$F_X:
\begin{cases}
X\to X^{(p)}
\\
X(f_R):X(R)\to X(R_f)
\end{cases}$$

If $X$ is a $k$-scheme $X^{(p)}$ is a $k$-scheme, too.

Since the completion functor ${}^\hat\;:Sch_k\to fSch_k$ commutes with the above constructions the Frobenius morphism can be defined for [[formal scheme|formal k-schemes]], too.

### In terms of symmetric products

We give here another characterization of the [[Frobenius morphism]] in terms of symmetric products.

Let $p$ be a prime number, let $k$ be a field of [[characteristic]] $p$, let $V$ be a $k$-vector space, let $\otimes^p V$ denote the $p$-fold tensor power of $V$, let $TS^p V$ denote the subspace of symmetric tensors. Then we have the symmetrization operator

$$s_V:
\begin{cases}
\otimes^p V\to TS^p V
\\
a_1\otimes\cdots\otimes a_n\mapsto \Sigma_{\sigma\in S_p}a_{\sigma(1)}\otimes\cdots\otimes a_{\sigma(n)}
\end{cases}$$

end the linear map

$$\alpha_V:
\begin{cases}
TS^p V\to\otimes^p V
\\
a\otimes \lambda\mapsto\lambda(a\otimes\cdots\otimes a)
\end{cases}$$

then the map $V^{(p)}\stackrel{\alpha_V}{\to}TS^p V\to TS^p V/s(\otimes^p V)$ is bijective and we define $\lambda_V:TS^p V\to V^{(p)}$ by

$$\lambda_V\circ s=0$$

and

$$\lambda_V \circ \alpha_V= id$$


If $A$ is a $k$-ring we have that $TS^p A$ is a $k$-ring and $\lambda_A$ is a $k$-ring morphism.

If $X=Sp_k A$ is a ring spectrum we abbreviate $S^p X=S^p_k X:=Sp_k (TS^p A)$ and the following diagram is commutative.

$$\array{
X
&\stackrel{F_X}{\to}&
X^{(p)}
\\
\downarrow&&\downarrow
\\
X^p
&\stackrel{can}{\to}& S^p X
}$$

## Properties

+-- {: .num_prop}
###### Proposition
Let $X$ be a $k$-formal scheme (resp. a [[locally algebraic scheme]]) then $X$ is [[etale scheme|étale]] iff the [[Frobenius morphism]] $F_X:X\to X^{(p)}$is a monomorphism (resp. an isomorphism).
=--

## Examples

If $X=Sp_k A$ is a $k$-ring spectrum we have $X^{(p)}=Sp_k A^{(p)}$ and $F_X=Sp_k F_A$.

If $k=\mathbb{F}$ is a finite field we have $X^{(p)}=X$ however $F_X$ will not equal $id_X$ in general.

If $k\hookrightarrow k^\prime$ is a field extension we have $F_{X\otimes_k k^\prime}=F_X\otimes_k k^\prime$.

[[!redirects Frobenius morphism]]


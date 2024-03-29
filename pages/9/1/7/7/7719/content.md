[[!redirects I.10, Frobenius morphism and symmetric products]]


This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

We give here another characterization of the [[Frobenius morphism]] in terms of symmetric products.

Let $p$ be a prime number, let $k$ be a filed of [[characteristic]] $p$, let $V$ be a $k$-vector space, let $\otimes^p V$ denote the $p$-fold tensor power of $V$, let $TS^p V$ denote the subspace of symmetric tensors. Then we have the symmetrization operator

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
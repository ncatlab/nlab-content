[[!redirects II.3, affine k-groups]]
[[!redirects affine k-group]]

This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

Let $A\in M_k$, let $\Delta:A\to A\otimes_k A$.

Then the $k$-group $(Sp_k A, Sp_k \Delta_k)$ is called *affine k-group*.

A *$k$-biring* is defined to be a $k$-module which is a $k$-ring and a $k$-coring such that $A\to A\otimes A$ is a $k$-ring morphism and $A\otimes A\to A$ is a $k$-coring morphism.

## Examples

+-- {: .num_example}
###### Example

The additive $k$-group $\alpha_k$ assigns to a $k$-ring its underlying additive group. We have $O(\alpha_k)=K[t]$ since by the Yoneda lemma we have $O(\alpha_k)=hom(\alpha_k, O_k)=\alpha_k(k[t])$

=--

+-- {: .num_example}
###### Example

The multiplicative $k$-group $\mu_k$ assigns to a $k$-ring the multiplicative group of its invertible elements. We have $O(\mu_k)=K[tt^{-1}]$.

=--

+-- {: .num_example}
###### Example

There is a group homomorphism 

$$n:=n_{\mu_k}:\begin{cases}
\mu_k&\to& \mu_k
\\
x&\to &x^n
\end{cases}$$

its kernel we denote by $n\mu_k:=ker(n)$. We have $n\mu_k(R)=\{x\in R|x^n=1\}$ and $O(n\mu_k)=k[t]/(t^n -1)$. If $k$ is a field and $n$ is not $0$ in $k$ the $k$-group $n\mu_k$ is [[etale scheme|étale]] since $t^n-1$ is a separable polynomial. $n\mu_k(k_s)$ is the Galois module of the $n$-th root of unity.
=--


+-- {: .num_example}
###### Example

Let $k$ be a field of prime [[characteristic]] $p$, let $r$ be an integer. Then there is a $k$-group morphism.

$$p^r:=p^r_{\alpha_k}:\begin{cases}
\alpha_k&\to& \alpha_k
\\
x&\to &x^{p^r}
\end{cases}$$


We have $ker(p^r\alpha_k)(R)=\{x\in R | x^{p^r}=0\}$ and $O(ker(p^r \alpha_k))=K[t]/t^{p^r}$. For any field $K$ we have $ker(p^r_{\alpha_k})(K)=\{0\}$.

=--
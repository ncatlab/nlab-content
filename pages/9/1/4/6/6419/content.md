
# Contents
* table of contents
{: toc}

## Idea

Serre decided to try taking coefficients in the Witt vectors as an early attempt at a [[Weil cohomology theory]]. Ultimately, it wasn't successful for this purpose, but has been generalized in several ways for other purposes with great success.


## Sheaf of Witt vectors

Let $X$ be a [[scheme]] over a [[perfect field]] $k$ of positive [[characteristic]] $p$. Let $W$ and $W_n$ be the functors of [[Witt vectors]] and truncated Witt vectors respectively. The functorial nature allows us to define a [[sheaf]] of Witt vectors $\mathcal{W}$ and $\mathcal{W}_n$ just by taking Witt vectors of the rings of sections of $\mathcal{O}_X$.
 
Note that as a sheaf of sets $\mathcal{W}_n$ is just $\mathcal{O}_X^n$. The ring structure is just the addition and multiplication of the Witt vectors. The operations on the Witt vectors sheafify as well. When $n\geq m$ we have the exact sequence $0\to \mathcal{W}_m\stackrel{V}{\to} \mathcal{W}_n\stackrel{R}{\to}\mathcal{W}_{n-m}\to 0$. If we take $m=1$, then we get the sequence $0\to \mathcal{O}_X\to \mathcal{W}_n\to \mathcal{W}_{n-1}\to 0$


## Definition

The sheaf of Witt vectors is an abelian sheaf, so we just define cohomology $H^q(X, \mathcal{W}_n)$ as the standard sheaf cohomology (on the [[Zariski site]] of $X$). Let $\Lambda=W(k)$, then since $\mathcal{W}_n$ are $\Lambda$-modules annihilated by $p^n\Lambda$, we get that $H^q(X, \mathcal{W}_n)$ are also $\Lambda$-modules annihilated by $p^n\Lambda$.

In fact, all of our old operators $F$, $V$, and $R$ still act on $H^q(X, \mathcal{W}_n)$. They are easily seen to satisfy the formulas $F(\lambda w)=F(\lambda)F(w)$, $V(\lambda w)=F^{-1}(\lambda)V(w)$, and $R(\lambda w)=\lambda R(w)$ for $\lambda\in \Lambda$. If $X$ is projective then $H^q(X, \mathcal{W}_n)$ is a finite $\Lambda$-module.

What is usually referred to with Witt cohomology is $H^q(X, \mathcal{W})$ which is defined to be $lim H^q(X, \mathcal{W}_n)$. Note that even if $X$ is projective, this limit does not have to be a finite type $\Lambda$-module.


## References

* J.P. [[Serre]], Sur la topologie des vari&#233;t&#233;s alg&#233;briques en caract&#233;ristique p, Symposium de Topologie Alg&#233;brique, Mexico (August, 1956)


[[!redirects Witt cohomology]]
[[!redirects Witt Cohomology]]

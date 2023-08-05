\tableofcontents

## Idea

An _Euler system_ is a collection of classes in [[Galois cohomology]] satisfying certain compatibility conditions. The existence of a nontrivial Euler system can imply bounds on the [[Selmer group]] and thus the theory of Euler systems finds applications in the study of [[special values of L-functions]], for instance in Victor Kolyvagin's work on the [[Birch and Swinnerton-Dyer conjecture]]. 

## Definition

The reference for this section is Section 1.4 of [#LoefflerZerbes18](#LoefflerZerbes18).

\begin{definition}

Let $G_{\mathbb{Q}}$ be the [[absolute Galois group]] of $\mathbb{Q}$. Let $V$ be a [[Galois representation]] valued in $\mathbb{Q}_{p}$, and let $T\subset V$ be a $G_{K}$-stable $\mathbb{Z}_{p}$-lattice. Let $\Sigma$ be a finite set of primes containing $p$ and all ramified primes.

Let $P_{\ell}(V,t)$ be the local Euler factor at $\ell$, i.e.

$$P_{\ell}(V,t)=\det(1-t\cdot\rho(\Frob_{v}^{-1})).$$

An _Euler system_ for $(T,\Sigma)$ is a collection $\mathbf{c}=(c_{m})_{m}$, where $c_{m}\in H^{1}(\mathbb{Q}(\mu_{m}),T)$ satisfying the following compatibility conditions:

$$\mathrm{norm}_{\mathbb{Q}(\mu_{m})}^{\mathbb{Q}(\mu_{m\ell})}(c_{m\ell})=

\begin{cases}
c_{m}\;\if \ell\in\Sigma\;\or\;m\vert \ell\\
P_{\ell}(V^{*}(1),\sigma_{\ell}^{-1})\cdot c_{m}\;\otherwise
\end{cases}$$

where $\sigma_{\ell}$ is the image of $\mathrm{Frob}_{\ell}$ in $\mathrm{Gal}(\mathbb{Q}(\mu_{m})/\mathbb{Q})$.

\end{definition}

## Application to bounding the Selmer group

\begin{theorem}(Theorem 2 of [#LoefflerZerbes18](#LoefflerZerbes18))
Suppose $\mathbf{c}$ is an Euler system for $(T,\Sigma)$ with $c_{1}$ nonzero, and suppose that $V$ satisfies certain technical conditions. Then the strict Selmer group $\Sel_{\strict}(\mathbb{Q},V^{*}(1))$ is zero.
\end{theorem}

## Relation to motivic cohomology

One of the ways to construct examples of Euler systems is via [[motivic cohomology]] (see chapter 3 of [#LoefflerZerbes18](#LoefflerZerbes18)).

## References

{#LoefflerZerbes18} David Loeffler and Sarah Zerbes, _Euler Systems_, Arizona Winter School 2018 Notes ([pdf](https://swc-math.github.io/aws/2018/2018LoefflerZerbesNotes.pdf))
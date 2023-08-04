\tableofcontents

## Idea

The Selmer group is a subgroup of the [[Galois cohomology]] satisfying certain local conditions.

It appears in the statement of the Bloch-Kato conjecture on [[special values of L-functions]], generalizing the [[Birch and Swinnerton-Dyer conjecture]].

## Definitions

The reference for this section is [#LoefflerZerbes18](#LoefflerZerbes18).

Let $K$ be a [[number field]]. Let $V$ be a [[Galois representation]], i.e. a representation of $\Gal(\overline{K}/K)$. We have the first [[Galois cohomology]] group, which we will denote with the following shortcut notation

$$H^{1}(K,V):=H^{1}(\Gal(\overline{K}/K),V)$$

For any prime $v$ of $K$, let $K_{v}$ be the completion. We have "localization" maps (we are also using similar notation as above for the local Galois cohomology groups)

$$\loc_{v}:H^{1}(K,V)\to H^{1}(K_{v},V)$$

\begin{definition}
A _local condition_ on $V$ at a prime $v$ is a subspace $\mathcal{F}_{v}\subseteq H^{1}(K_{v},V)$.
\end{definition}

An important example of a local condition is the _unramified local condition_. Letting $G_{K_{v}}$ be the [[absolute Galois group]] of $K_{v}$ and letting $I_{v}$ be its inertia subgroup, the unramified local condition is defined as follows:

$$\mathcal{F}_{v,\unr}:=\im(H^{1}(G_{K_{v}}/I_{v},V^{I_{v}})\to H^{1}(K_{v},V))$$

\begin{definition}
A _Selmer structure_ is a collection $\mathcal{F}=\lbrace\mathcal{F}_{v}\rbrace_{v}$ of local conditions $\mathcal{F}_{v}$, such that $\mathcal{F}_{v}=\mathcal{F}_{v,\unr}$ for all but finitely many primes $v$.

If $\mathcal{F}$ is a Selmer structure, we define the corresponding _Selmer group_ as

$$\mathrm{Sel}_{\mathcal{F}}(K,V)=\lbrace x\in H^{1}(K,V):\loc_{v}\in\mathcal{F}_{v}\forall v\rbrace.$$
\end{definition}

## References

{#LoefflerZerbes18} David Loeffler and Sarah Zerbes, _Euler Systems_, Arizona Winter School 2018 Notes ([pdf](https://swc-math.github.io/aws/2018/2018LoefflerZerbesNotes.pdf))
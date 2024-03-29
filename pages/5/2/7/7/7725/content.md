Let $k$ be a field of prime characteristic $p$.

+-- {: .num_defn}
###### Definition

Let $A$ be an [[abelian variety]] of dimension $g$. Let $l$ be a prime number.

For $n\in \mathbb{N}$ the kernel $ker l^n id_A)$ is a finite $k$-group of rank $l^{2 n g}$. We define

$$A(l):=\cup_n ker(l^n id_A)$$

We have $A(l)\otimes_k \overline k\simeq (\mathbb{Q}(\mathbb{Z}_l))^{2g}$. If $l\neq p$, then $A(l)$ is an [[étale formal k-group]].
=--

+-- {: .num_defn}
###### Definition
We define

$$H^1(A,l):=hom_{\mathbb{Z}_l}(A(l)\otimes_k \overline k, \mathbb{Q}_l /\mathbb{Z}_l)$$

This is a free module of rank $2g$ over $\mathbb{Z}_l$ and also a [[Galois module]].

If $l=p$, then $A(p)$ is a $p$-divisible group of height $2g$. In this case we define

$$H^1(A,p):=M(A(p))$$

as the [[Dieudonné module]] of $A(p)$. It is an [[F-lattice]] (defined in [[Demazure, lectures on p-divisible groups, IV.1, isogenies]]) over $k$, and in particular a free module of rank $2g$ over $W(k)$.

For any prime $l$, the assignation

$$A\mapsto H^1(A,l)$$

is a functor.
=--
[[!redirects strict local rings]]

## Idea

For $Spec \mathbb{Z}$ an [[affine scheme]], the objects which the [[étale topos]] $Sh(X_{et})$ classifies are **strict local rings**. The [[point of a topos|points of this topos]] are _[[strict Henselian rings]]_ ([Hakim, III.2-4](#Hakim)) and ([Wraith](#Wraith)).

## Definition

We need to knead the definition of strict Henselian ring into being geometric.

Let $p = \sum_{i=0}^{n} a_i x^i \in R[x]$ be a monic polynomial of degree $n$ (so $a_n = 1$).

If $R$ is a field, a simple root of $p$ is an $r \in R$ with $p(r) = 0$ and $(p/(x-r))(r) \neq 0$. We generalise this as:

+-- {: .num_defn}
###### Definition
More generally if $R$ is a ring, a _simple root_ of $p$ is an $r \in R$ with $p(r) = 0$ and $p'(r)$ invertible.
=--

If $R$ is a field, $p$ is _unramifiable_ if in any field extension $R \subseteq Q$ in which we can write $p = \prod_i (x-s_i)$, some $s_i$ is a simple root.

To make this definition work for more general rings, some work must be done. Let $R'$ be the ring $R[s_1, \cdots, s_n]/\langle a_k - \sigma_k(\vec s) \mid k \in \{0,\cdots,n\} \rangle$, where $\sigma_k$ is the [[elementary symmetric polynomial]]. Then the _hyperdiscriminant polynomial_ is the polynomial $\Delta(p) = \prod_{i=1}^n (1 + p'(s_i) x) \in R'[x]$. As this polynomial is symmetric in the $s_i$, the theory of symmetric polynomials tells us that $\Delta(p) \in R[x]$.

+-- {: .num_defn}
###### Definition
More generally if $R$ is a ring, $p$ _unramifiable_ if $\Delta(p)-1$ is nonconstant i.e. $1 \in \langle \Delta_1(p), \cdots, \Delta_n(p) \rangle$ where $\Delta_i(p)$ is the $x_i$ coefficient of $\Delta(p)$
=--

This is roughly justified by the following:

+-- {: .num_lemma}
###### Proposition
If $R$ is a local ring and $t_1, \cdots, t_n \in R$, then at least one of $t_1, \cdots, t_n$ is invertible iff $1 \in \langle a_1, \cdots, a_n \rangle$ where $a_i$ are defined so that $\prod_{i=1}^n (1 + t_i x) = 1 + \sum_{i=1}^n a_i x^i$
=--
+-- {: .proof}
###### Proof
Each $a_i$ is a finite sum of a nonempty product of some $t_j$, so if $1$ is in the ideal some $t_j$ is invertible.

Conversely, if $t_j$ is invertible, substituting $x = -1/t_j$ gives $1 = \sum_{i=1}^n a_i (-1)\cdot(-1/t_j)^i$
=--

This lets us arrive at our definition:

+-- {: .num_defn}
###### Definition
A ring $R$ is _separably closed_ iff whenever $p$ is a monic polynomial of positive degree, if $p$ is unramifiable, $p$ has a simple root.

A _strict local ring_ is a separably closed local ring.
=--


## References

III.2-4 of

* [[Monique Hakim]], _Topos annel&#233;s et sch&#233;mas relatifs_
 {#Hakim}

and

* [[Gavin Wraith]], _Generic Galois theory of local rings_
 {#Wraith}

Section 21 of

* [[Ingo Blechschmidt]], _Using the internal language of toposes in algebraic geometry_

includes discussion of what some similar topoi classify, including the étale topology over $Sh(S)$ partially via the internal language.

See also [this MO discussion](http://mathoverflow.net/questions/48690/what-does-an-etale-topos-classify)

See also at _[classifying topos -- For strict local rings](http://ncatlab.org/nlab/show/classifying+topos#StrictLocalRings)_
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--

# Contents # 
* table of contents 
{:toc}

## Idea 

In enumerative [[combinatorics]], a "bijective proof" refers to a basic method of counting the number of structures of a certain type supported on a finite set of underlying points, by analyzing structure in two different ways. It is really a special case of "[[categorification]]": an identity $a = b$ where $a$ and $b$ are [[natural number]] expressions is proved by taking underlying cardinalities of a [[bijection]] $A \cong B$ between sets of structures, hence the name. (If taking cardinalities is an example of "decategorifying", then going the other way from $a = b$ to $A \cong B$ would be "categorifying" or promoting an equation to an isomorphism.) 

In some sense this is what the theory of [[species]] is all about: formalizing the operations adhering to bijective proofs. Often bijective proofs give an impression of elegance or enlightenment: rather than prove natural number or polynomial identities through acts of symbolic manipulation, one *sees* the identity by drawing pictures of structures that the two sides of the identity are counting. 

## Examples 

For the moment we'll just jot down some possible examples for illustrating the method; these are to be filled in later, or to be linked to other nLab articles where the bijective proof is given. 

### Binomial identity 

See for now [[binomial theorem]]. 

### $q$-binomial identity 

For more details, see the [Wikipedia article](https://en.wikipedia.org/wiki/Gaussian_binomial_coefficient). 

Algebraically, one may introduce the $q$-binomial coefficients $\binom{n}{k}_q$ by introducing a $q$-affine plane (or quantum affine plane, to be connected with [[quantum affine algebra]]) and its associated (non-commutative) algebra 

$$k[x, y]_q = k\langle x, y \rangle/(y x = q x y)$$ 

where $q \in k$ is a parameter, and then writing $(x + y)^n = \sum_{k = 0}^n \binom{n}{k}_q x^k y^{n-k}$. 

However, an illuminating combinatorial interpretation of the $q$-binomial coefficients is that they count points in a [[Grassmannian]] consisting of $k$-dimensional linear subspaces of an $n$-dimensional [[vector space]] $\mathbb{F}_q^n$ over a [[finite field]] $\mathbb{F}_q$ of cardinality $q$. This interpretation can be used to provide a bijective proof of the $q$-Pascal identity 

$$\binom{n}{k}_q = \binom{n-1}{k}_q + q^{n-k}\binom{n-1}{k-1}_q.$$ 

For, if we choose a standard affine hyperplane $H = \{x_n = 1\}$ in $\mathbb{F}_q^n$, then any linear $k$-plane $W$ in $\mathbb{F}_q^n$ either intersects $H$ in an affine $(k-1)$-plane in the affine $(n-1)$-space, or intersects $H$ in the empty set, i.e., $W$ is contained in the linear space $\{x_n = 0\}$. The number of $W$ satisfying the latter condition is $\binom{n-1}{k}_q$, and the number of $W$ satisfying the former is in bijection with the number of $(k-1)$-dimensional affine subspaces of $\mathbb{F}_q^{n-1}$, which is $q^{n-1}$ times the number of linear subspaces $\binom{n-1}{k-1}_q$ divided by $q^{k-1}$, the number of translations which stabilize a given affine subspace. (Maybe to be rewritten later.) 

### Counting trees: Cayley's theorem 

Cayley's theorem, here not to be confused with Cayley's observation that every group (monoid) is a subgroup (submonoid) of a permutation group (endofunction monoid), says that the number of tree structures on an $n$-element set $\{x_1, \ldots, x_n\}$ is $n^{n-2}$. 

There are many proofs of this fact in the literature. One, due to Gilbert Labelle and made popular by Andr&#233; Joyal, proceeds by establishing a bijection between trees equipped with a pair $(x_i, x_j)$ of nodes (allowing $x_i = x_j$) and the number of endofunctions on $X = \{x_1, \ldots, x_n\}$. 

On the one hand, such a structure $(T, x_i, x_j)$ on $X$ can be identified with a linearly ordered set (the path $P$ from $x_i$ to $x_j$ in $T$) together with, for each node $y$ along that path, a rooted tree structure $T_y$ consisting of nodes $x \in X$ for which the shortest path in $T$ from $x$ to $P$ ends at $y$. (As a subgraph of $T$, this naturally forms a tree $T_y$ rooted at $y$.) Thus, such a structure $(T, x_i, x_j)$ on $X$ determines and is determined by an equivalence relation $E$ on $X$, a rooted tree structure on each equivalence class, and a linear ordering of the set $X/E$ of equivalence classes. 

On the other hand, each endofunction on $X$, say $f: X \to X$, has an [[eventual image]] or stable set $stab(f) = \bigcap_{n \geq 0} f^n(X)$, on which $f$ acts by a permutation (i.e., bijectively). For each $y \in stab(f)$, there is a rooted tree $T_y$ which consists of all $x \in X$ for which the set of iterates $x, f(x), f^2(x), \ldots$ first lands in $stab(f)$ at $y$. Thus an endofunction on $X$ determines and is determined by an equivalence relation $E$ on $X$, a rooted tree structure on each equivalence class, and a permutation on the set $X/E$ of equivalence classes. 

Since the number of permutations on $X/E$ is equinumerous with the number of linear orderings of $X/E$, we conclude that the set of "bipointed tree" structures on $X$ is equinumerous with the set of endofunctions on $X$. Thus the number of bipointed tree structures $(T, x_i, x_j)$ on $X$ is $n^n$, and therefore the number of tree structures $T$ on $X$ is $n^{n-2}$. 

### Vandermonde identity 

### Stirling number identities 

## Polynomial identities 

One method for proving [[polynomial]] identities (equations $p = q$ between polynomials $p, q \in \mathbb{C}[x_1, \ldots, x_k]$ in several variables) is first to give a bijective proof for the special case in which natural numbers $m_i$ are substituted for the variables $x_i$, and then reason that there are enough natural numbers that the polynomial identity must hold generally. 

More formally, two polynomials are equal, $p(x_1, \ldots, x_k) = q(x_1, \ldots, x_k)$, if $p(m_1, \ldots, m_k) = q(m_1, \ldots, m_k)$ for all choices of natural numbers $m_i$. Relatedly, the set $\mathbb{N}^k \subseteq \mathbb{C}^k$ is Zariski-dense (i.e., the closure of $\mathbb{N}^k$ in $\mathbb{C}^k$ equipped with the [[Zariski topology]] is all of $\mathbb{C}^k$). 

This is intuitively obvious of course. As a public service, we prove a more general result. 

+-- {: .num_prop} 
###### Proposition 
Suppose $B$ is an [[infinite set|infinite]] [[subset]] of an [[integral domain]] $A$. Then a polynomial $p(x_1, \ldots, x_k) \in A[x_1, \ldots, x_k]$ is uniquely determined by its values it takes at arguments $b_1, \ldots, b_k \in B$. 
=-- 

+-- {: .proof} 
###### Proof 
It suffices to show that if $p(b_1, \ldots, b_k) = 0$ for every choice of $b_i \in B$, then $p = 0$. We prove this by induction on $k$. The case $k = 0$ is trivial. 

Assuming the assertion as induction hypothesis for case $k$, suppose $p \in A[x_1, \ldots, x_k, x_{k+1}]$ satisfies $p(b_1, \ldots, b_k, b) = 0$ for all choices $b_i \in B$ and $b \in B$. Then by induction, for each fixed $b \in B$ the polynomial $p(x_1, \ldots, x_k, b) \in A[x_1, \ldots, x_k]$ is identically zero. Thus if $F$ is the [[field of fractions]] of $A[x_1, \ldots, x_k]$, and if we regard $p$ as an element of the [[Euclidean domain]] $F[x_{k+1}]$ under the obvious embedding 

$$A[x_1, \ldots, x_k, x_{k+1}] \cong A[x_1, \ldots, x_k][x_{k+1}] \hookrightarrow F[x_{k+1}],$$ 

then $p$ has infinitely many [[roots]] $b$ in $A$ and thus in $F$, forcing $p$ to be identically zero. 
=-- 

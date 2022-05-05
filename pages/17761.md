#Contents#
* table of contents
{:toc}

## Idea

The **order polynomial** $\Omega_P(n)$ of a finite [[partially ordered set]] $P$ counts the number of ways that $P$ can be extended to a [[linear order]] of size $n$.

## Definition

By a _linear extension_ of $P$ of size $n$, we mean an [[order-preserving function]] from $P$ to $(n) = \{ 1 \lt \cdots \lt n \}$.
To see that
$$\Omega_P(n) = |Hom(P,(n))|$$
defines a [[polynomial]] in $n$, first observe that any function $P \to (n)$ factors as a [[surjection]] from $P$ onto some $(k) = \{ 1 \lt \cdots \lt k \}$ (where $k \le n$), followed by an [[injection]] from $(k)$ to $(n)$. The total number of order-preserving functions from $P$ to $(n)$ can therefore be calculated explicitly as 
$$\Omega_P(n) = \sum_{k=1}^{|P|} e_k \binom{n}{k}$$
where $e_k$ is the number of surjective order-preserving functions from $P$ to $(k)$. Hence $\Omega_P(n)$ is a polynomial of degree equal to the cardinality of $P$.

## Examples

The order polynomial of $(3) = \{ 1 \lt 2 \lt 3 \}$ is
$$n + 2 \binom{n}{2} + \binom{n}{3} = \frac{n^3 + 3n^2 + 2n}{6}$$
For example, evaluating the polynomial at $n=3$ confirms that there are 10 order-preserving functions from $(3)$ to itself.

The order polynomial of the 3-element poset
$$P = \array{&&c&& \\ &\nearrow& &\nwarrow& \\ a &&&& b}$$
is $n + 3 \binom{n}{2} + 2\binom{n}{3} = \frac{2n^3 + 3n^2 + n}{6}$.
Evaluating at $n=2$, we compute that there are 5 order-preserving functions from $P$ onto $(2)$.

## Properties

### Relation to zeta polynomial

Let $P^\downarrow \cong (2)^P$ denote the lattice of [[lower sets]] in $P$. The order polynomial of a finite poset $P$ is related to the [[zeta polynomial]] of its lattice of lower sets $P^\downarrow$ by the equation[^Note]
$$\Omega_P(n+2) = Z_{P^\downarrow}(n)$$
This can be seen as a consequence of the [[currying]] isomorphisms
$$Hom([n], P^\downarrow) \cong Hom([n] \times P, (2)) \cong Hom(P, [n]^\downarrow)$$
together with the isomorphisms $[n]^\downarrow \cong [n+1] \cong (n+2)$.

[^Note]: Note that the definition we use for $Z_P(n)$ has an index shift from the definition that seems to be more standard in combinatorics (see the footnote at [[zeta polynomial]]), so this equation is sometimes expressed as $\Omega_P(n) = Z_{P^\downarrow}(n)$.

### Relation to the strict order polynomial

Let $\bar{\Omega}_P(n)$ denote the number of [[strict order-preserving functions]] from $P$ to $(n)$, that is, functions $f : P \to (n)$ such that $x \lt y$ implies $f(x) \lt f(y)$. This again defines a polynomial in $n$, called the **strict order polynomial** of $P$. The strict order polynomial of a finite poset $P$ is related to its order polynomial by the equation
$$\bar{\Omega}_P(n) = (-1)^p \Omega_P(-n)$$
where $p = |P|$ is the cardinality of $P$. This is an example of a _combinatorial reciprocity theorem_ in the sense of [Stanley (1974)](#Stanley74).

(Notice that we are evaluating the order polynomial at a negative integer, even though the putative definition $\Omega_P(n) = |Hom(P,(n))|$ only makes sense for natural numbers $n$. This is justified because the value of a polynomial on the natural numbers determines its value on arbitrary integers.)

Through [[Möbius inversion]], this equation relating the strict order polynomial to the order polynomial can be connected to the previous one relating the order polynomial to the zeta polynomial. Since the lattice of lower sets $P^\downarrow$ has [[bottom]] and [[top]] elements, we know that
$$
\Omega_P(n) = Z_{P^\downarrow}(n-2) = \zeta^n(\emptyset,P)
$$
where $\zeta^n$ is the $n$-fold convolution of the zeta function of $P^\downarrow$. One can similarly work out that
$$
\bar{\Omega}_P(n) = (-1)^p\mu^n(\emptyset,P)
$$
where $\mu^n$ is the $n$-fold convolution of the [[Möbius function]] of $P^\downarrow$. The equation $\bar{\Omega}_P(n) = (-1)^p \Omega_P(-n)$ then follows formally from the fact that $\mu = \zeta^{-1}$.

### Computational complexity

Counting the number of total linear extensions of a poset (i.e., number of linear extensions of an $n$-element poset to a linear order of size $n$) is a #P-complete problem [(Brightwell and Winkler 1991)](#BW1991), and thus so is the problem of computing the leading coefficient of the order polynomial (cf. [Browning, Hopkins, and Kelley 2017](#BHK2017)).

## Related concepts

* [[zeta polynomial]]
* [[incidence algebra]]
* [[Möbius inversion]]

## References

* Richard P. Stanley. Ordered structures and partitions. Memoirs of the AMS 119, 1972. ([doi](http://www.ams.org/books/memo/0119/)) (Free copy available from the [author's website](http://www-math.mit.edu/~rstan/pubs/), see #9.)
 {#Stanley72}

* Richard P. Stanley. Combinatorial Reciprocity Theorems. Advances in Mathematics 14:194-253, 1974. (Free copy available from the [author's website](http://www-math.mit.edu/~rstan/pubs/), see #22.)
 {#Stanley74}

* Joseph P. S. Kung, [[Gian-Carlo Rota]], Catherine H. Yan. Combinatorics: The Rota Way. Cambridge, 2009.

* {#BW1991} Graham Brightwell and Peter Winkler. Counting Linear Extensions. _Order_ 8:225-242, 1991. [doi](https://doi.org/10.1007/BF00383444)

* {#BHK2017} Thomas Browning, Max Hopkins, and Zander Kelley. Doppelgangers: the Ur-Operation and Posets of Bounded Height. [arXiv:1710.140407](https://arxiv.org/abs/1710.10407)

category: combinatorics
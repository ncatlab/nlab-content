#Contents#
* table of contents
{:toc}

## Idea

The **zeta polynomial** $Z_P(n)$ of a finite [[partially ordered set]] $P$ counts the number of multichains (also known as "weakly increasing sequences") of length $n$ in $P$.

## Definition

By a _multichain_ of length $n$ in $P$, we mean a sequence of elements $x_0 \le x_1 \le \cdots \le x_n$, which can be identified with an [[order-preserving function]] from the [[linear order]] $[n] = \{ 0 \lt 1 \lt \cdots \lt n \}$ into $P$.
To see that
$$Z_P(n) = |Hom([n],P)|$$
defines a [[polynomial]] in $n$,[^Note] first observe that any function $[n] \to P$ factors as a [[surjection]] from $[n]$ onto some $[k] = \{ 0 \lt 1 \lt \cdots \lt k \}$ (where $k \le n$), followed by an [[injection]] from $[k]$ to $P$. The total number of order-preserving functions from $[n]$ to $P$ can therefore be calculated explicitly as 
$$Z_P(n) = \sum_{k=0}^{d} b_k \binom{n}{k}$$
where $b_k$ is the number of _chains_ $x_0 \lt x_1 \lt \cdots \lt x_k$ in $P$ (i.e., injective order-preserving functions from $[k]$ to $P$), and where $d$ is the length of the longest chain. Hence $Z_P(n)$ is a polynomial of degree equal to the length of the longest chain in $P$.

[^Note]: Note that the definition we use here for $Z_P(n)$ has an index shift from the definition that seems to be more standard in combinatorics. For example, the definition in [(Stanley, 3.12)](#StanleyEC1) counts multichains of length $n-2$ rather than of length $n$. Accordingly, one should apply a substitution to get some of the properties stated here to match equivalent results in the literature.

## Examples

The zeta polynomial of $[2] = \{ 0 \lt 1 \lt 2 \}$ is
$$3 + 3n + \binom{n}{2} = \frac{n^2 + 5n + 6}{2}$$
For example, evaluating the polynomial at $n=0$ and $n=1$ confirms that $[2]$ contains 3 points and 6 [[intervals]], while evaluating it at $n=2$ confirms that there are 10 order-preserving functions from $[2]$ to itself.

The zeta polynomial of the 5-element poset
$$P = \array{&&v&& \\ &&\uparrow&& \\ &&u&& \\ &\nearrow& &\nwarrow& \\ y &&&& z \\ &\nwarrow& &\nearrow& \\ &&x&&}$$
is $5 + 9n + 7\binom{n}{2} + 2\binom{n}{3} = \frac{2n^3 + 15n^2 + 37n + 30}{6}$.
Evaluating at $n=1$, we compute that $P$ contains 14 distinct intervals.

## Properties

### Relation to order polynomial

The [[order polynomial]] is related to the  zeta polynomial by the equation
$$
\Omega_P(n+2) = Z_{P^\downarrow}(n)
$$
where $P^\downarrow \cong (2)^P$ is the lattice of [[lower sets]] in $P$.
This can be seen as a consequence of the [[currying]] isomorphisms
$$Hom([n], P^\downarrow) \cong Hom([n] \times P, (2)) \cong Hom(P, [n]^\downarrow)$$
together with the isomorphisms $[n]^\downarrow \cong [n+1] \cong (n+2)$.

### Relation to zeta function

Using the formalism of [[incidence algebras]], the zeta polynomial has a simple expression in terms of the _zeta function_ of $P$ (defined by $\zeta_P(x,y) = 1$ if $x\le y$ and $\zeta_P(x,y) = 0$ otherwise):
$$Z_P(n) = \sum_{x,y\in P} \zeta_P^n(x,y)$$
where $\zeta_P^n$ is the $n$-fold convolution product of $\zeta_P$. (In other words, if we view the zeta function as a square matrix, then the zeta polynomial is the sum of the entries in its $n$-fold matrix product.) This follows immediately from the definition of the convolution product,
$$(f\cdot g)(x,y) = \sum_{x \le z \le y} f(x,z) \cdot g(z,y)$$
since $\zeta_P^n(x,y)$ computes the number of multichains of length $n$ in $P$ from $x$ to $y$.
 
As a special case, if $P$ has both a [[bottom]] element 0 and a [[top]] element 1, then
$$Z_P(n) = \zeta_P^{n+2}(0,1)$$
since an arbitrary multichain $x_0 \le x_1 \le \cdots \le x_n$ of length $n$ can be extended to a multichain $0 \le x_0 \le x_1 \le \cdots \le x_n \le 1$ of length $n+2$ between 0 and 1.

## Related concepts

* [[order polynomial]]
* [[incidence algebra]]
* [[Möbius inversion]]
* [[nerve]]

## References

* Paul H. Edeleman. Zeta Polynomials and the M&#246;bius Function. European Journal of Combinatorics 1(4), 1980.
{#Edelman80}

* Richard P. Stanley, _Enumerative combinatorics_, vol.1 ([pdf](http://www-math.mit.edu/~rstan/ec/ec1.pdf))
{#StanleyEC1}

* Joseph P. S. Kung, [[Gian-Carlo Rota]], Catherine H. Yan. Combinatorics: The Rota Way. Cambridge, 2009.
{#KungRotaYan}
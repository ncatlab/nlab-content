#Contents#
* table of contents
{:toc}

## Idea

The **zeta polynomial** $Z(P,n)$ of a finite [[partially ordered set]] $P$ counts the number of _multichains_ (also known as _weakly increasing sequences_) $x_0 \le x_1 \le \cdots \le x_n$ in $P$.

## Definition

Note that a multichain of length $n$ in $P$ is the same thing as an [[order-preserving function]] from the [[linear order]] $[n] = \{ 0 \lt 1 \lt \cdots \lt n \}$ into $P$.
To see that
$$Z(P;n) = |Hom([n],P)|$$
defines a [[polynomial]] in $n$,[^Note] first observe that any function $[n] \to P$ factors as a [[surjection]] from $[n]$ onto some $[k] = \{ 0 \lt 1 \lt \cdots \lt k \}$ (where $k \le n$), followed by an [[injection]] from $[k]$ to $P$. The total number of order-preserving functions from $[n]$ to $P$ can therefore be calculated explicitly as 
$$Z(P;n) = \sum_{k=0}^{d} b_k \binom{n}{k}$$
where $b_k$ is the number of _chains_ $x_0 \lt x_1 \lt \cdots \lt x_k$ in $P$ (i.e., injective order-preserving functions from $[k]$ to $P$), and where $d$ is the length of the longest chain. Hence $Z(P;n)$ is a polynomial of degree equal to the length of the longest chain in $P$.

[^Note]: Note that the definition we use here for $Z(P;n)$ has an index shift from the definition that seems to be more standard in combinatorics. For example, the definition in [(Stanley, 3.12)](#StanleyEC1) counts multichains of length $n-2$ rather than of length $n$, and accordingly one should apply a substitution $n \mapsto n-2$ to recover his definition from ours.

## Examples

The zeta polynomial of $[2] = \{ 0 \lt 1 \lt 2 \}$ is
$$3 + 3n + \binom{n}{2} = \frac{n^2 + 5n + 6}{2}$$
For example, evaluating the polynomial at $n=0$ and $n=1$ confirms that $[2]$ contains 3 points and 6 intervals, while evaluating it at $n=2$ confirms that there are 10 order-preserving functions from $[2]$ to itself.

The zeta polynomial of the 5-element poset
$$P = \array{&&v&& \\ &&\uparrow&& \\ &&u&& \\ &\nearrow& &\nwarrow& \\ y &&&& z \\ &\nwarrow& &\nearrow& \\ &&x&&}$$
is $5 + 9n + 7\binom{n}{2} + 2\binom{n}{3} = \frac{2n^3 + 15n^2 + 37n + 30}{6}$.
Evaluating at $n=1$, we compute that $P$ contains 14 distinct intervals.

## Properties

### Relation to order polynomial

The [[order polynomial]] is related to the  zeta polynomial by the equation
$$
\Omega(P;n+2) = Z(I(P);n)
$$
where $I(P) \cong [P,[1]]$ is the lattice of [[lower sets]] in $P$.
This can be seen as a consequence of the isomorphisms
$$Hom(P, [n+1]) \cong Hom(P, [[n],[1]]) \cong Hom(P\times [n],[1]) \cong Hom([n], [P,[1]])$$
applying the isomorphism $[n+1] \cong [[n],[1]]$ together with [[currying]].

### Relation to zeta function

Using the formalism of [[incidence algebras]], the zeta polynomial has a simple expression in terms of the _zeta function_ (defined by $\zeta_P(x,y) = 1$ if $x\le y$ and $\zeta_P(x,y) = 0$ otherwise):
$$Z(P;n) = \sum_{x,y\in P} \zeta_P^n(x,y)$$
In other words, the zeta polynomial is the sum of the entries in the $n$-fold convolution product of the zeta function (seen as a matrix). This follows immediately from the definition of the convolution product,
$$(f\cdot g)(x,y) = \sum_{x \le z \le y} f(x,z) \cdot g(z,y)$$
since $\zeta_P^n(x,y)$ is just the number of multichains of length $n$ in $P$ from $x$ to $y$.
 
As a special case, if $P$ has both a [[bottom]] element 0 and a [[top]] element 1, then
$$Z(P;n) = \zeta_P^{n+2}(0,1)$$
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

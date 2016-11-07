The **zeta polynomial** $Z(P,n)$ of a finite [[partially ordered set]] $P$ counts the number of _multichains_ (also known as _weakly increasing sequences_) $x_0 \le x_1 \le \cdots \le x_n$ in $P$. Note that a multichain of length $n$ in $P$ is the same thing as an [[order-preserving function]] from the [[linear order]] $[n] = \{ 0 \lt 1 \lt \cdots \lt n \}$ into $P$.
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

The zeta polynomial of the 3-element poset
$$P = \array{&&c&& \\ &\nearrow& &\nwarrow& \\ a &&&& b}$$
is $2n + 3$.
Evaluating at $n=1$, we compute that $P$ contains 5 distinct intervals.

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

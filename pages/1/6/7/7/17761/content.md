The **order polynomial** of a finite [[partially ordered set]] $P$ is a function $\Omega(P;n)$ counting the total number of [[order-preserving functions]] from $P$ into any [[linear order]]
$$\mathbf{n} = \{ 0 \lt 1 \lt \cdots \lt n-1 \}.$$
To see that this defines a [[polynomial]] in $n$, first observe that any function $P \to \mathbf{n}$ factors as a [[surjection]] from $P$ onto some $\mathbf{k} = \{ 0 \lt 1 \lt \cdots \lt k-1 \}$ (where $k \le n$), followed by an [[injection]] from $\mathbf{k}$ to $\mathbf{n}$. The total number of order-preserving functions from $P$ to $\mathbf{n}$ can therefore be calculated explicitly as 
$$\Omega(P;n) = \sum_{k=1}^{|P|} e_k \binom{n}{k}$$
where $e_k$ is the number of surjective order-preserving functions from $P$ to $\mathbf{k}$. Hence $\Omega(P;n)$ is a polynomial of degree bounded by the cardinality of $P$.

## Examples

The order polynomial of $\mathbf{3} = \{ 0 \lt 1 \lt 2 \}$ is
$$n + 2 \binom{n}{2} + \binom{n}{3} = \frac{n^3 + 3n^2 + 2n}{6}$$
For example, evaluating the polynomial at $n=3$ confirms that there are 10 order-preserving functions from $\mathbf{3}$ to itself.

The order polynomial of the 3-element poset
$$P = \array{&&c&& \\ &\nearrow& &\nwarrow& \\ a &&&& b}$$
is $n + 3 \binom{n}{2} + 3\binom{n}{3} = \frac{2n^3 + 3n^2 + n}{6}$.
Evaluating at $n=2$, we compute that there are 5 order-preserving functions from $P$ onto $\mathbf{2}$.

## References

* Richard P. Stanley. Ordered structures and partitions. Memoirs of the AMS 119, 1972. ([doi](http://www.ams.org/books/memo/0119/)) (Free copy available from the [author's website](http://www-math.mit.edu/~rstan/pubs/).)

* Joseph P. S. Kung, [[Gian-Carlo Rota]], Catherine H. Yan. Combinatorics: The Rota Way. Cambridge, 2009.
Suppose $P$ is a finite [[partially ordered set]], and consider [[order-preserving functions]] from $P$ into a [[natural number]] $n$ viewed as a linear order
$$\mathbf{n} = \{ 0 \lt 1 \lt \cdots \lt n-1 \}.$$
Any such function $P \to \mathbf{n}$ factors as a [[surjection]] from $P$ onto some $\mathbf{k} = \{ 0 \lt 1 \lt \cdots \lt k-1 \}$, followed by an [[injection]] from $\mathbf{k}$ to $\mathbf{n}$. Hence, the total number $\Omega(P;n)$ of order-preserving functions from $P$ to $\mathbf{n}$ can be calculated as 
$$\Omega(P;n) = \sum_{k=1}^{|P|} e_k \binom{n}{k}$$
where $e_k$ is the number of surjective order-preserving functions from $P$ to $\mathbf{k}$. For a given $P$, this defines a polynomial in $n$, called the **order polynomial** of $P$.

## References

* Richard P. Stanley. Ordered structures and partitions. Memoirs of the AMS 119, 1972. ([doi](http://www.ams.org/books/memo/0119/)) (Free copy available from the [author's website](http://www-math.mit.edu/~rstan/pubs/).)

* Joseph P. S. Kung, [[Gian-Carlo Rota]], Catherine H. Yan. Combinatorics: The Rota Way. Cambridge, 2009.
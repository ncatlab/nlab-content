#Contents#
* table of contents
{:toc}

## Idea

The **order polynomial** $\Omega(P;n)$ of a finite [[partially ordered set]] $P$ counts the total number of [[order-preserving functions]] from $P$ into any [[linear order]] $\mathbf{n} = \{ 0 \lt 1 \lt \cdots \lt n-1 \}.$

## Definition

To see that
$$\Omega(P;n) = |Hom(P,\mathbf{n})|$$
defines a [[polynomial]] in $n$, first observe that any function $P \to \mathbf{n}$ factors as a [[surjection]] from $P$ onto some $\mathbf{k} = \{ 0 \lt 1 \lt \cdots \lt k-1 \}$ (where $k \le n$), followed by an [[injection]] from $\mathbf{k}$ to $\mathbf{n}$. The total number of order-preserving functions from $P$ to $\mathbf{n}$ can therefore be calculated explicitly as 
$$\Omega(P;n) = \sum_{k=1}^{|P|} e_k \binom{n}{k}$$
where $e_k$ is the number of surjective order-preserving functions from $P$ to $\mathbf{k}$. Hence $\Omega(P;n)$ is a polynomial of degree equal to the cardinality of $P$.

## Examples

The order polynomial of $\mathbf{3} = \{ 0 \lt 1 \lt 2 \}$ is
$$n + 2 \binom{n}{2} + \binom{n}{3} = \frac{n^3 + 3n^2 + 2n}{6}$$
For example, evaluating the polynomial at $n=3$ confirms that there are 10 order-preserving functions from $\mathbf{3}$ to itself.

The order polynomial of the 3-element poset
$$P = \array{&&c&& \\ &\nearrow& &\nwarrow& \\ a &&&& b}$$
is $n + 3 \binom{n}{2} + 2\binom{n}{3} = \frac{2n^3 + 3n^2 + n}{6}$.
Evaluating at $n=2$, we compute that there are 5 order-preserving functions from $P$ onto $\mathbf{2}$.

## Properties

### Relation to zeta polynomial

The order polynomial is related to the [[zeta polynomial]] by the equation[^Note]
$$
\Omega(P;n+2) = Z(I(P);n)
$$
where $I(P) \cong [I(P),\mathbf{2}]$ is the lattice of [[lower sets]] in $P$.
This can be seen as a consequence of the isomorphisms
$$Hom(P, [n+1]) \cong Hom(P, [[n],[1]]) \cong Hom(P\times [n],[1]) \cong Hom([n], [P,[1]])$$
(where $[n] = \mathbf{n{+}1}$) applying the isomorphism $[n+1] \cong [[n],[1]]$ together with [[currying]].

[^Note]: Note that the definition we use for $Z(P;n)$ has an index shift from the definition that seems to be more standard in combinatorics (see the footnote at [[zeta polynomial]]), so this equation is sometimes expressed as $\Omega(P;n) = Z(I(P);n)$.

### Relation to the strict order polynomial

Let $\bar{\Omega}(P;n)$ be the number of [[strict order-preserving functions]] from $P$ to $\mathbf{n}$, that is, functions $f : P \to \mathbf{n}$ such that $x \lt y$ implies $f(x) \lt f(y)$. This again defines a polynomial in $n$, called the **strict order polynomial** of $P$. The strict order polynomial is related to the order polynomial via a _combinatorial reciprocity theorem_ in the sense of [Stanley](#Stanley74).

+-- {: .num_prop }
###### Proposition

[(Stanley 1972, 1974)](#Stanley74): Let $P$ be a finite partially order set of cardinality $p$. Then $\bar{\Omega}(P;n) = (-1)^p \Omega(P;-n)$.

=--

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
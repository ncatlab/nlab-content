The **zeta polynomial** $Z(P,n)$ of a finite [[partially ordered set]] $P$ counts the total number of [[order-preserving functions]] from any [[linear order]] $\mathbf{n} = \{ 0 \lt 1 \lt \cdots \lt n-1 \}$ into $P$.
To see that
$$Z(P;n) = |Hom(\mathbf{n},P)|$$
defines a [[polynomial]] in $n$,[^Note]
first observe that any function $\mathbf{n} \to P$ factors as a [[surjection]] from $\mathbf{n}$ onto some $\mathbf{k} = \{ 0 \lt 1 \lt \cdots \lt k-1 \}$ (where $k \le n$), followed by an [[injection]] from $\mathbf{k}$ to $P$. The total number of order-preserving functions from $\mathbf{n}$ to $P$ can therefore be calculated explicitly as 
$$Z(P;n) = \sum_{k=1}^{d} b_k \binom{n-1}{k-1}$$
where $b_k$ is the number of injective order-preserving functions from $\mathbf{k}$ to $P$, and where $d$ is the length of the longest chain $x_1 \lt x_2 \lt \cdots \lt x_d$ in $P$. Hence $Z(P;n)$ is a polynomial of degree at most one less than the length of the longest chain in $P$.

[^Note]: Note that the definition we use here is shifted from the more standard one which counts the number of order-preserving functions from $\mathbf{n{-}1}$ into $P$ (a.k.a., "multichains" of length $n-1$ in $P$).

## Related concepts

* [[order polynomial]]
* [[incidence algebra]]
* [[Möbius inversion]]

## References

* Paul H. Edeleman. Zeta Polynomials and the M&#246;bius Function. European Journal of Combinatorics 1(4), 1980.
{#Edelman80}

* Joseph P. S. Kung, [[Gian-Carlo Rota]], Catherine H. Yan. Combinatorics: The Rota Way. Cambridge, 2009.
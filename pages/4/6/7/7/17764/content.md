The **zeta polynomial** $Z(P,n)$ of a finite [[partially ordered set]] $P$ counts the total number of [[order-preserving functions]] from any non-empty [[linear order]] $[n] = \{ 0 \lt 1 \lt \cdots \lt n \}$ into $P$.
Note that an order-preserving function from $[n]$ into $P$ is also called a _multichain_ of length $n$ in $P$, corresponding to a sequence of $n+1$ (possibly repeated) elements $x_0 \le x_1 \le \cdots \le x_n$ in $P$.
To see that
$$Z(P;n) = |Hom([n],P)|$$
defines a [[polynomial]] in $n$, first observe that any function $[n] \to P$ factors as a [[surjection]] from $[n]$ onto some $[k] = \{ 0 \lt 1 \lt \cdots \lt k \}$ (where $k \le n$), followed by an [[injection]] from $[k]$ to $P$. The total number of order-preserving functions from $[n]$ to $P$ can therefore be calculated explicitly as 
$$Z(P;n) = \sum_{k=0}^{d} b_k \binom{n+1}{k+1}$$
where $b_k$ is the number of _chains_ $x_1 \lt x_2 \lt \cdots \lt x_k$ in $P$ (i.e., injective order-preserving functions from $[k]$ to $P$), and where $d$ is the length of the longest chain. Hence $Z(P;n)$ is a polynomial of degree at most the length of the longest chain in $P$.


## Related concepts

* [[order polynomial]]
* [[incidence algebra]]
* [[Möbius inversion]]

## References

* Paul H. Edeleman. Zeta Polynomials and the M&#246;bius Function. European Journal of Combinatorics 1(4), 1980.
{#Edelman80}

* Joseph P. S. Kung, [[Gian-Carlo Rota]], Catherine H. Yan. Combinatorics: The Rota Way. Cambridge, 2009.
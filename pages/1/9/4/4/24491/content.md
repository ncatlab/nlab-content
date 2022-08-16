+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In a [[field]] of [[positive characteristic]], the usual [[derivative]] of [[polynomials]] has bad properties. Let $\mathbb{K}$ be such a field of [[characteristic]] $p \gt 0$. Consider the [[polynomial algebra]] $\mathbb{K}[X]$. The usual derivative of polynomials in one indeterminate defines a [[derivation]] $\mathbb{K}[X] \rightarrow \mathbb{K}[X]$ which associates $P'$ to $P$.

We then have that $(X^{p})'=p.X^{p-1}=0$ but $X^{p} \neq 0$ because $1^{p} = 1 \neq 0$. We thus lack the property that $P' = 0$ iff $P$ is a constant.

The notion of Hasse-Schmidt derivative comes as a replacement of the usual derivative and enjoys better properties.

It seems to be very linked to [[differential linear logic]] and to the notion of [[graded bimonoid]].

## Definition for one indeterminate

Suppose that $R$ is a [[commutative rig]]. For every polynomial $P \in R[X]$ and $n \ge 0$, we define the $n-th$ Hasse-Schmidt derivative $P^{(n)}$ of $P$ by:

* $P^{(0)} = P$

and if $n \ge 1$:

* $(X^{n+p})^{(n)} = \binom{n+p}{n} X^{p}$ if $p \ge 0$
* $(X^{k})^{(n)} = 0$ if $n \gt k$
* $(aP+bQ)^{(n)} = aP^{(n)} + bQ^{(n)}$

## Definition for several indeterminates

Suppose that $R$ is a [[commutative rig]]. We look at the polynomials in $R[X_{1},...,X_{q}]$. For every multiset $Y_{1}...Y_{n} \in \{X_{1},...,X_{q}\}$ and $P \in R[X_{1},...,X_{q}]$ we define the derivative $D_{Y_{1}...Y_{n}}(P)$.

Suppose that $P$ is a monic monomial, that is a multiset of variables in $\{X_{1},...,X_{q}\}$.

* If $Y_{1}...Y_{n}$ doesn't divide $P$, then:
$$
D_{Y_{1}...Y_{n}}(P) = 0
$$

* If $Y_{1}...Y_{n}$ divides $P$, then:
$$
D_{Y_{1}...Y_{n}}(P) = \left[\underset{\substack{1 \le i \le q \\ X_{i} | Y_{1}...Y_{n}}}{\prod}\binom{nbr\;of\;time\;X_{i}\;in\;P}{nbr\;of\;time\;X_{i}\;in\;Y_{1}...Y_{n}}\right]\frac{P}{Y_{1}...Y_{n}}
$$

We then prolongate by linearity:

* $D_{Y_{1}...Y_{n}}(aP+bQ) = aD_{Y_{1}...Y_{n}}(P) + bD_{Y_{1}...Y_{n}}(Q)$ 

There is a very [[combinatorial]] interpretation which makes the link with the notion of [[graded bimonoid]]: if $P$ is a monic monomial, the derivative with respect to $Y_{1}...Y_{n}$ counts the number of ways to extract $Y_{1}...Y_{n}$ from $P$ and then multiplies it by $P$ where $Y_{1}...Y_{n}$ has been extracted. All the instances of a variable $Y_{i}$ in $P$ must be considered as different entities in this counting.

For example there is $\binom{3}{2}\binom{4}{1}$ ways to extract $X^{2}Y$ from $X^{3}Y^{4}$, we have $\binom{3}{2}$ choices of two instance of $X$ in $X^{3}$ and $\binom{4}{1}$ choices of two instances of $Y$ in $Y^{4}$, thus:
$$
D_{X^{2}Y}(X^{3}Y^{4}) = \binom{3}{2}\binom{4}{1}XY^{3} = 3.4.XY^{3} = 12XY^{3}
$$

## Related notions

* [[Hasse-Schmidt derivation]]

## References

The notion was introduced in:

* [[Helmut Hasse]]: *Noch eine Begründung der Theorie der höheren Differrentialquotienten in einem algebraischen Funktionenkörper einer Unbestimmten. (Nach einer brieflichen Mitteilung von [[Friedrich Karl Schmidt|F. K. Schmidt]] in Jena.)*, Reine Angew. Math.  **177** (1937) 215-223 &lbrack;[paper](https://gdz.sub.uni-goettingen.de/id/PPN243919689_0177?tify={%22pages%22:[219],%22view%22:%22export%22})&rbrack;

The definition and basic properties are reviewed on this blog page:

* _Hasse derivative_, Felix' Math Place (2009), [url](https://math.fontein.de/2009/08/12/the-hasse-derivative/)
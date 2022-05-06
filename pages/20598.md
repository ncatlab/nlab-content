# Ribenboim power series

* table of contents
{: toc}

## Idea

A **Ribenboim power series** group (or ring, or field) is a generalization of a [[formal power series]] ring whose exponents can belong to almost any partially ordered *monoid*.  It includes [[formal power series]], [[formal Laurent series]], [[polynomials]], [[Laurent polynomials]], and [[Hahn series]] as special cases.

## Definition

Let $P$ be a [[poset]]; say that a subset of $P$ is *artinian* if it contains no strictly decreasing infinite [[chain]], and *narrow* if it contains no infinite [[antichain]].  Let $A$ be an [[abelian group]].  The space of **Ribenboim power series** from $P$ with coefficients in $A$, denoted $G(P,A)$, is the set of functions $f:P\to A$ whose support $supp(f) = \{ p\in P \mid f(p)\neq 0 \}$ is artinian and narrow.  This is an abelian group under pointwise addition.

Now let $M$ be a strict [[partially ordered|poset]] [[monoid]], i.e. a [[monoid object]] in the [[monoidal category]] $Pos_{str}$ of [[posets]] and strict functions (i.e. morphisms that preserve the strict ordering as well as the non-strict one) whose monoidal structure is the cartesian product of $Pos$ (which is not the cartesian product of $Pos_{str}$).  More explicitly, this means $M$ is a monoid and a poset and the multiplication preserves both orders $\le$ and $\lt$ on both sides.

If $M$ is such a "strict pomonoid" and $R$ a [[ring]], then $G(M,R)$ is again a ring, with multiplication

$$ (f\cdot g)(m) = \sum_{(m_1,m_2) \in X_m(f,g)} f(m_1)\cdot g(m_2) $$

where $X_m(f,g)$ is the set of pairs $(m_1,m_2)\in supp(f) \times supp(g)$ such that $m_1\cdot m_2 = m$.  (The nontrivial fact to verify is that $X_m(f,g)$ is always finite.)

## Examples

* If $M=\mathbb{N}$ with the usual order, we obtain the usual ring of [[formal power series]] with coefficients in $R$.

* If $M=\mathbb{Z}$ with the usual order, we obtain the usual ring of [[formal Laurent series]].

* If $M=\mathbb{N}$ with the discrete order, we obtain the usual ring of [[polynomials]].

* Similarly, for $\mathbb{Z}$ with the discrete order, we obtain the ring of [[Laurent polynomials]].

* If $M$ is a linearly ordered abelian group and $R$ a field, then $G(M,R)$ is the field of [[Hahn series]] with value group $M$.

## Related pages

Other rings of generalized power series include:

* [[Puiseux series]]
* [[Novikov field]]
* [[Hahn series]]

Hahn series are a special kind of Ribenboim power series, but Puiseux and Novikov series are not.  However, they are all instances of the linearization of a [[finiteness space]].  For Puiseux and Ribenboim series, this is shown in [BJCS](#BCJS18).

## References

* P. Ribenboim, Rings of generalized power series: Nilpotent elements, Abh. Math. Semin. Univ. Hambg. 61, pp. 15--3 (1991)

* P. Ribenboim, Noetherian rings of generalized power series, J. Pure Appl. Algebra 79, pp. 293--312 (1992)

* P. Ribenboim, Rings of generalized power series II: Units and zero-divisors, Journal of Algebra 168, pp. 71--89 (1994)

* Richard Blute, Robin Cockett, Pierre-Alain Jacqmin, and Philip Scott, *Finiteness spaces and generalized power series*, [doi](https://doi.org/10.1016/j.entcs.2018.11.002), [arXiv:1805.09836](https://arxiv.org/abs/1805.09836)
 {#BCJS18}

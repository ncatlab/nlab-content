# Stone gamut
* this block creates the table of contents, leave as is
{: toc}

## Idea

The Stone gamut is a unifying representation of several common categories in terms of [[Chu space|Chu spaces]]. It is named after [[Stone duality]].


## Definition 

Let **$Chu_2$** be the category of Chu spaces over the Booleans, with $r : Chu_2 \to \mathbb{N}$ and $c : Chu_2 \to \mathbb{N}$ counting the number of rows and columns respectively, and let **$FinChu_2$** be its [[full subcategory]] of finite Chu spaces. Let a *skeleton* of a Chu space be another Chu space with no repeated rows or repeated columns, and let the *dual* of a Chu space $A$, written $A^{\bot}$, be its transpose. Let a *discreteness* be a function $\delta : FinChu_2 \to [-1, 1]$ such that:

* $\delta$ depends only on the number of rows and columns in its input's skeleton, and
* $\delta(A^{\bot}) = -\delta(A)$

For our purposes, we will consider Pratt discreteness, defined as:

$$
\delta(A) = \frac{P(A) - Q(A)}{P(A) + Q(A)}
$$

Where $P(A) = |2^{r(A)} - c(A)|$ and $Q(A) = |2^{c(A)} - r(A)|$. Intuitively, $P$ and $Q$ count the number of "missing" rows and columns in the skeleton.


## Properties

Note that when $r(A) \gt c(A)$, $r(A) \leq 2^{c(A)}$; and dually, when $c(A) \gt r(A)$, $c(A) \leq 2^{r(A)}$, by the pigeonhole principle.

Pratt notes that their $\delta$ has the "odd property that the only discreteness possible in $[-\frac{1}{3}, \frac{1}{3}]$ is 0" (Pratt 1995).

## Examples

### Stone dualities

Broadly, Stone duality is between [[topological space|topological spaces]], particularly [[Stone space|Stone spaces]], and [[Boolean algebra|Boolean algebras]]. In the Stone gamut, topological spaces have discreteness in $[0, 1]$, and Boolean algebras have discreteness in $[-1, 0]$. We will consider several special cases.

If we require discreteness to be non-zero, then the duality is restricted to connect [[partial order|posets]] with ([[profinite]]) [[distributive lattice|distributive lattices]]. Posets have discreteness in $(\frac{1}{3}, 1]$ and profinite distributive lattices have discreteness in $[-1, -\frac{1}{3})$.

As a notable special case, [[set|sets]] are dual to [[complete atomic Boolean algebra|CABAs]]. The discreteness of a set is 1, and the discreteness of a CABA is -1. This is an equivalence; any Boolean-valued Chu space with discreteness 1 is equivalent to a set since it has a trivial [[equational theory]].


## References

* {#Pratt1995} [[Vaughan Pratt]], _The Stone gamut: a Coordinatization of Mathematics_, Proceedings of Tenth Annual IEEE Symposium on Logic in Computer Science (1995) &lbrack;[doi:10.1109/LICS.1995.523278](https://doi.org/10.1109/LICS.1995.523278), [pdf](http://boole.stanford.edu/pub/gamut.pdf)&rbrack;
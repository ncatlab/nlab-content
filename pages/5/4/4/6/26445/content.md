# Stone gamut
* this block creates the table of contents, leave as is
{: toc}

## Idea

The Stone gamut is a unifying representation of several common categories in terms of [[Chu space|Chu spaces]]. It is named after [[Stone duality]].


## Definition 

Let **$Chu_2$** be the category of Chu spaces over the Booleans, with $r : Chu_2 \to \mathbb{N}$ and $c : Chu_2 \to \mathbb{N}$ counting the number of rows and columns respectively. Let a *skeleton* of a Chu space be another Chu space with no repeated rows or repeated columns, and let the *dual* of a Chu space $A$, written $A^{\bot}$, be its transpose. Let a *discreteness* be a function $\delta : Chu_2 \to [-1, 1]$ such that:

* $\delta$ depends only on the number of rows and columns in its input's skeleton, and
* $\delta(A^{\bot}) = -\delta(A)$

For our purposes, we will consider Pratt discreteness, defined as:

$$
\delta(A) = \frac{P(A) - Q(A)}{P(A) + Q(A)}
$$

Where $P(A) = |2^{r(A)} - c(A)|$ and $Q(A) = |2^{c(A)} - r(A)|$. Intuitively, $P$ and $Q$ count the number of "missing" rows and columns in the skeleton.


## Properties

Pratt notes that their $\delta$ has the "odd property that the only discreteness possible in $[-\frac{1}{3}, \frac{1}{3}]$ is 0" (Pratt 1995).

## Examples

(...)


## References

* {#Pratt1995} [[Vaughan Pratt]], _The Stone gamut: a Coordinatization of Mathematics_, Proceedings of Tenth Annual IEEE Symposium on Logic in Computer Science (1995) &lbrack;[doi:10.1109/LICS.1995.523278](https://doi.org/10.1109/LICS.1995.523278), [pdf](http://boole.stanford.edu/pub/gamut.pdf)&rbrack;
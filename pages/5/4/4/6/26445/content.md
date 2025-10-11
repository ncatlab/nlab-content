# Stone gamut
* this block creates the table of contents, leave as is
{: toc}

## Idea

The Stone gamut is a unifying representation of several common categories in terms of [[Chu space|Chu spaces]]. It is named after [[Stone duality]]. The study of Chu duality and the Stone gamut is known as **chupology**. (Pratt 2006)


## Definition 

Let **$Chu_2$** be the category of Chu spaces over the Booleans, with $r : Chu_2 \to \mathbb{N}$ and $c : Chu_2 \to \mathbb{N}$ counting the number of rows and columns respectively, and let **$FinChu_2$** be its [[full subcategory]] of finite Chu spaces. Let a **skeleton** of a Chu space be another Chu space with no repeated rows or repeated columns, and let the **dual** of a Chu space $A$, written $A^{\bot}$, be its transpose. Let a Chu space be **skeletal** if it is a skeleton. Let a *discreteness* be a function $\delta : FinChu_2 \to [-1, 1]$ such that:

* $\delta$ depends only on the number of rows and columns in its input's skeleton, and
* $\delta(A^{\bot}) = -\delta(A)$

For our purposes, we will consider Pratt discreteness, defined as:

$$
\delta(A) = \frac{P(A) - Q(A)}{P(A) + Q(A)}
$$

Where $P(A) = |2^{r(A)} - c(A)|$ and $Q(A) = |2^{c(A)} - r(A)|$. Intuitively, $P$ and $Q$ count the number of "missing" rows and columns in the skeleton.

A **property** of a skeletal Chu space is a superset of its columns. (Def. 5, Pratt 1999)


## Properties

Note that when $r(A) \gt c(A)$, $r(A) \leq 2^{c(A)}$; and dually, when $c(A) \gt r(A)$, $c(A) \leq 2^{r(A)}$, by the pigeonhole principle.

Pratt notes that their $\delta$ has the "odd property that the only discreteness possible in $[-\frac{1}{3}, \frac{1}{3}]$ is 0" (Pratt 1995).

## Examples

### Contravariant dualities

Category | $\delta$ |[[space and quantity|Spaces $\cong$ Quantities]] | $\delta$ | Category
---|---|---|---|---
[[CABA]] | -1 | [[complete Boolean algebra|CABAs]]/[[overlap algebra|overlap algebras]] $\cong$ sets | 1 | [[Set]]
&mdash; | $[-1, -1 + \varepsilon]$ | finitely disconnected Boolean algebras $\cong$ finitely [[pointed set|pointed sets]] | $[1 - \varepsilon, 1]$ | $\Set_{\ast}$
[[SupLat]] | 0 | [[suplattice|suplattices]] $\cong$ inflattices | 0 | [[InfLat]]
&mdash; | $[-\frac{1}{3}, 0]$ | bounded complete lattices $\cong$ [[strict linear order|tosets]] | $[0, \frac{1}{3}]$ | [[tower|$\mathbb{N}_{\geq}$]]
[[CompLat]] | $[-1, 0]$ | [[complete lattice|complete lattices]] $\cong$ [[partial order|posets]] | $[0, 1]$ | [[Pos]]
[[Vect|$Vect_{\mathbb{F}_2}$]] | 0 | [[vector space|vector spaces]] over $\mathbb{F}_2$ $\cong$ [[dual vector space|dual vector spaces]] over $\mathbb{F}_2$ | 0 | $Vect_{\mathbb{F}_2}$


## References

* {#Pratt1995} [[Vaughan Pratt]], _The Stone gamut: a Coordinatization of Mathematics_, Proceedings of Tenth Annual IEEE Symposium on Logic in Computer Science (1995) &lbrack;[doi:10.1109/LICS.1995.523278](https://doi.org/10.1109/LICS.1995.523278), [pdf](http://boole.stanford.edu/pub/gamut.pdf)&rbrack;
* {#Pratt1999} [[Vaughan Pratt]], _Chu Spaces_, School on Category Theory and Applications, University of Coimbra (1999) &lbrack;[notes (pdf)](http://boole.stanford.edu/pub/coimbra.pdf)&rbrack;
* {#Pratt2006} [[Vaughan Pratt]], _dualities_, *Categories list* mailing list (2006) &lbrack;[list archive](http://www.mta.ca/~cat-dist/archive/2006/06-5)&rbrack;
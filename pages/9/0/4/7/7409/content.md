
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


# Induced characters
* table of contents
{: toc}

## Definition

Let $\phi\colon H\to G$ be a [[group homomorphism]], $V$ a [[representation]] of $H$, and $\chi$ the [[character]] of $V$.  The **induced character** $\phi_!(\chi)$ of $f$ is the character of the [[induced representation|induced]] $G$-representation
$$\phi_!(V) = Ind^G_H(V) = V\otimes_{k[H]} k[G].$$

## Formula

There is a formula for the induced character:

$$ \phi_!(\chi)(g) = \frac{1}{|H|} \sum_{k^{-1} g k = \phi(h)} \chi(h) $$

where the sum is over all pairs $(k\in G, h\in H)$ such that $k^{-1} g k = \phi(h)$.

This formula is usually given only in the case when $\phi$ is injective, when it can be re-expressed as a sum over [[cosets]].  The case when $\phi$ is surjective is [Exercise 7.1 of (Serre)](http://books.google.com/books?id=NCfZgr54TJ4C&pg=PA57&lpg=PA57) and the general case is easy to put together from these.  It can also be derived abstractly using [[bicategorical trace]].

## References

* {#Serre77} [[Jean-Pierre Serre]]: *Linear Representations of Finite Groups*, Graduate Texts in Mathematics **42**, Springer (1977) &lbrack;[doi:10.1007/978-1-4684-9458-7](https://doi.org/10.1007/978-1-4684-9458-7), [pdf](https://www.math.tau.ac.il/~borovoi/courses/ReprFG/Hatzagot.pdf)&rbrack;

* [MO question](http://mathoverflow.net/questions/89928/induced-character-for-non-injective-homomorphisms) about the non-injective case.

[[!redirects induced characters]]

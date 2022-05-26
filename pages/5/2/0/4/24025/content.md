

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

## Definition

Given a [[ring]] $R$, a **left filter** of $R$ is a multiplicative [[submonoid]] $(F, 1, \cdot)$ of $(R, 1, \cdot)$ with [[monoid]] [[monomorphism]] $i:F \hookrightarrow R$ such that for all elements $z \in F$ and $y \in R$, if there is an element $w \in R$ such that $i(z) = w \cdot y$, then there is an element $x \in F$ such that $i(z) = i(x) \cdot y$. 

A **right filter** of $R$ is a multiplicative [[submonoid]] $(F, 1, \cdot)$ of $(R, 1, \cdot)$ with [[monoid]] [[monomorphism]] $i:F \hookrightarrow R$ such that for all elements $z \in F$ and $y \in R$, if there is an element $w \in R$ such that $i(z) = y \cdot w$, then there is an element $x \in F$ such that $i(z) = y \cdot i(x)$. 

A **two-sided filter** is a multiplicative [[submonoid]] $(F, 1, \cdot)$ of $(R, 1, \cdot)$ with [[monoid]] [[monomorphism]] $i:F \hookrightarrow R$ that is both a left filter and a right filter. 

## See also

* [[ideal of a ring]]

## References

* [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))
> This page is about the [[rigs]] with a Kleene star closure operation. For the [[de Morgan algebra]], see [[Kleene algebra]].

----

\tableofcontents

## Definition

A **Kleene algebra** or **Kleene star algebra** is a [[rig]] $(R, 0, 1, +, (-)(-), (-)^*)$

* $+$ is [[idempotent]]: for all $x \in R$, $x + x = x$, making $(R, 0, +)$ into a [[semilattice]]

* for all $x \in R$, $1 + x x^* + x^* = x^*$

* for all $x \in R$, $1 + x^* x + x^* = x^*$

* for all $x \in R$ and $y \in R$, if $x y + y = y$, then $x^* y + y = y$

* for all $x \in R$ and $y \in R$, if $y x + y = y$, then $y x^* + y = y$

## Related concepts

* [[rig]]

* [[star semiring]]

* [[semilattice]]

* [[regular expression]]

* [[closed semiring]]

## References

Under the name "Kleene algebra":

* Wikipedia, [Kleene algebra](https://en.wikipedia.org/wiki/Kleene_algebra)

* [[Dexter Kozen]] (1990). *On Kleene algebras and closed semirings*. In: [[Branislav Rovan]] (editor). Mathematical Foundations of Computer Science 1990. MFCS 1990. Lecture Notes in Computer Science, vol 452. Springer, Berlin, Heidelberg. ([doi:10.1007/BFb0029594](https://doi.org/10.1007/BFb0029594), [pdf](https://www.cs.cornell.edu/~kozen/Papers/kacs.pdf))

[[!redirects Kleene star algebra]]
[[!redirects Kleene star algebras]]
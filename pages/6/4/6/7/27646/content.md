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

* [[John Horton Conway]], *Regular Algebra and Finite Machines*. Mineola, N.Y., Dover; Newton Abbot, 2012. ISBN:978-0486485836

* [[Dexter Kozen]] (1990). *On Kleene algebras and closed semirings*. In: [[Branislav Rovan]] (editor). Mathematical Foundations of Computer Science 1990. MFCS 1990. Lecture Notes in Computer Science, vol 452. Springer, Berlin, Heidelberg. ([doi:10.1007/BFb0029594](https://doi.org/10.1007/BFb0029594), [pdf](https://www.cs.cornell.edu/~kozen/Papers/kacs.pdf))

* [[Damien Pous]], [[Jurriaan Rot]], [[Jana Wagemaker]], *On Tools for Completeness of Kleene Algebra with Hypotheses*, Logical Methods in Computer Science, Volume 20, Issue 2 (May 16, 2024). ([doi:10.46298/lmcs-20(2:8)2024](https://doi.org/10.46298/lmcs-20%282%3A8%292024), [arXiv:2210.13020](https://arxiv.org/abs/2210.13020))

* [[Damien Pous]], [[Jana Wagemaker]], *Completeness Theorems for Kleene algebra with tests and top*, Logical Methods in Computer Science, Volume 20, Issue 3 (September 30, 2024). ([doi:10.46298/lmcs-20(3:27)2024](https://doi.org/10.46298/lmcs-20%283%3A27%292024), [arXiv:2304.07190](https://arxiv.org/abs/2304.07190))

* [[Jana Wagemaker]], *Extensions of (Concurrent) Kleene Algebra*, Thesis ([pdf](https://drive.google.com/file/d/1Abq9mRf_sbTie9MpoOBK829cv1NAQrI2/view))

[[!redirects Kleene star algebra]]
[[!redirects Kleene star algebras]]
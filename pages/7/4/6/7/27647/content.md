
> This article is about the [[rig]] that is the generalization of a [[Kleene star algebra]], with a Kleene star operation. For the $\mathbb{N}$-algebra with an [[anti-involution]], see [[star-algebra]]. 

---

\tableofcontents

## Definition

A **$*$-semiring** or **$*$-rig** is a [[rig]] $(R, 0, 1, +, (-)(-))$ with a function $(-)^*$ such that 

* for all $x \in R$, $1 + x(x^*) = x^*$

* for all $x \in R$, $1 + (x^*)x = x^*$

## Examples

* Assuming [[excluded middle]], the set of non-negative extended reals $[0, \infty]$ together with the usual addition and multiplication of reals is a star semiring with the star operation given by $a^* = \frac{1}{1 - a}$ for $0 \leq a \lt 1$ and $a^* = \infty$ for $a \geq 1$. 

## Related concepts

* [[rig]], [[semiring]]

* [[Conway semiring]]

* [[Kleene star algebra]]

## References

* Wikipedia, [Star semiring](https://en.wikipedia.org/wiki/Star+semiring)

* [[Daniel J. Lehmann]], *Algebraic structures for transitive closure*, Theoretical Computer Science, volume 4, issue 1, pages 59–76, 1977 ([doi:10.1016/0304-3975(77)90056-1](https://doi.org/10.1016%2F0304-3975%2877%2990056-1), [pdf](http://wrap.warwick.ac.uk/46308/7/WRAP_Lehmann_cs-rr-010.pdf))

* [[Manfred Droste]], [[Werner Kuich]], *Semirings and Formal Power Series* (2009). In: Manfred Droste, Werner Kuich, [[Heiko Vogler]], (eds) Handbook of Weighted Automata. Monographs in Theoretical Computer Science. An EATCS Series. Springer, Berlin, Heidelberg. pp. 3–28. ([doi:10.1007/978-3-642-01492-5_1](https://doi.org/10.1007%2F978-3-642-01492-5_1))

[[!redirects star-semiring]]
[[!redirects star-semirings]]
[[!redirects star semiring]]
[[!redirects star semirings]]
[[!redirects *-semiring]]
[[!redirects *-semirings]]
[[!redirects * semiring]]
[[!redirects * semirings]]

[[!redirects star-rig]]
[[!redirects star-rigs]]
[[!redirects star rig]]
[[!redirects star rigs]]
[[!redirects *-rig]]
[[!redirects *-rigs]]
[[!redirects * rig]]
[[!redirects * rigs]]

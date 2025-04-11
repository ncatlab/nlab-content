
> This article is about the $*$-[[rig]] that is the generalization of a [[Kleene star algebra]]. For the $*$-rig that is an $\mathbb{N}$-algebra with an [[anti-involution]], see [[star-algebra]]. 

---

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

A [[rig]] $R$ is a **quasiregular rig** or **quasiregular semiring** or **closed rig** or **closed semiring** or **Lehmann rig** or **Lehmann semiring** or **$*$-rig** or **$*$-semiring** if every element in $R$ is a [[quasiregular element]]; equivalently, $R$ is quasiregular if there is a function $(-)^*:R \to R$ such that for all elements $r \in R$, $r^* = r^* r + 1$ and $r^* = r r^* + 1$. 

## Examples

* Assuming [[excluded middle]], the set of non-negative extended reals $[0, \infty]$ together with the usual addition and multiplication of reals is a quasiregular rig with the star operation given by $a^* = \frac{1}{1 - a}$ for $0 \leq a \lt 1$ and $a^* = \infty$ for $a \geq 1$. 

* The only quasiregular [[ring]] is the [[trivial ring]], because if the multiplicative [[neutral element]] $1$ is quasiregular, then we have $1^* = 1^* 1 + 1$ and $1^* = 1^* + 1$ and thus $0 = 1$. 

* More generally, the only quasiregular [[rig]] with [[cancellative monoid|cancellative]] addition is the [[trivial rig]], because if the multiplicative [[neutral element]] $1$ is quasiregular, then we have $1^* = 1^* 1 + 1$ and $1^* = 1^* + 1$ and thus $0 = 1$ by the cancellative property of addition. 

* A [[commutative rig]] is quasiregular [[if and only if]] it satisfies the Conway product-star axiom: for all $r \in R$ and $s \in R$, $(r s)^* = 1 + r (s r)^* s$. 

## Related concepts

* [[rig]], [[semiring]]

* [[Conway semiring]]

* [[Kleene star algebra]]

* [[quasiregular element]]

## References

* Wikipedia, *[Quasiregular element#Generalization to semirings](https://en.wikipedia.org/wiki/Quasiregular_element#Generalization_to_semirings)*

* Wikipedia, *[Semiring#Star semirings](https://en.wikipedia.org/wiki/Semiring#Star_semirings)*

* [[Daniel J. Lehmann]], *Algebraic structures for transitive closure*, Theoretical Computer Science, volume 4, issue 1, pages 59–76, 1977 ([doi:10.1016/0304-3975(77)90056-1](https://doi.org/10.1016%2F0304-3975%2877%2990056-1), [pdf](http://wrap.warwick.ac.uk/46308/7/WRAP_Lehmann_cs-rr-010.pdf))

* [[Dexter Kozen]] (1990). *On Kleene algebras and closed semirings*. In: [[Branislav Rovan]] (editor). Mathematical Foundations of Computer Science 1990. MFCS 1990. Lecture Notes in Computer Science, vol 452. Springer, Berlin, Heidelberg. ([doi:10.1007/BFb0029594](https://doi.org/10.1007/BFb0029594), [pdf](https://www.cs.cornell.edu/~kozen/Papers/kacs.pdf))

* [[Manfred Droste]], [[Werner Kuich]], *Semirings and Formal Power Series* (2009). In: Manfred Droste, Werner Kuich, [[Heiko Vogler]], (eds) Handbook of Weighted Automata. Monographs in Theoretical Computer Science. An EATCS Series. Springer, Berlin, Heidelberg. pp. 3–28. ([doi:10.1007/978-3-642-01492-5_1](https://doi.org/10.1007%2F978-3-642-01492-5_1))

[[!redirects quasiregular rig]]
[[!redirects quasiregular rigs]]
[[!redirects quasiregular semiring]]
[[!redirects quasiregular semirings]]

[[!redirects quasi-regular rig]]
[[!redirects quasi-regular rigs]]
[[!redirects quasi-regular semiring]]
[[!redirects quasi-regular semirings]]

[[!redirects closed rig]]
[[!redirects closed rigs]]
[[!redirects closed semiring]]
[[!redirects closed semirings]]

[[!redirects Lehmann rig]]
[[!redirects Lehmann rigs]]
[[!redirects Lehmann semiring]]
[[!redirects Lehmann semirings]]

[[!redirects star-rig]]
[[!redirects star-rigs]]
[[!redirects star-semiring]]
[[!redirects star-semirings]]

[[!redirects star rig]]
[[!redirects star rigs]]
[[!redirects star semiring]]
[[!redirects star semirings]]

[[!redirects *-rig]]
[[!redirects *-rigs]]
[[!redirects *-semiring]]
[[!redirects *-semirings]]

[[!redirects * rig]]
[[!redirects * rigs]]
[[!redirects * semiring]]
[[!redirects * semirings]]

[[!redirects starrig]]
[[!redirects starrigs]]
[[!redirects starsemiring]]
[[!redirects starsemirings]]
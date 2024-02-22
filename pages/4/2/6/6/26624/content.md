
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Arithmetic
+-- {: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

\tableofcontents

## Idea

A **transcendental number** is a number which is not a root of a polynomial with rational coefficients. 

## Definition

Given a [[field extension]] of the [[rational numbers]] $\mathbb{Q} \subseteq F$ with a non-trivial [[absolute value]] $\vert - \vert:F \to \mathbb{R}$, a number $\alpha \in F$ is **transcendental** if for all [[polynomial functions]] with [[rational number|rational]] [[coefficients]] $f \in \mathbb{Q}[x] \subseteq F^F$, the absolute value of $f(\alpha)$ is positive 

$$\mathrm{isTranscendental}(\alpha) \coloneqq \forall f \in \mathbb{Q}[x].\vert f(\alpha) \vert \gt 0$$

Equivalently, $\alpha \in F$ is **transcendental** if the absolute value of the difference of $\alpha$ and every algebraic number in $F$ is positive:

$$\mathrm{isTranscendental}(\alpha) \coloneqq \forall \beta \in F.(\beta \in \overline{\mathbb{Q}}) \Rightarrow (\vert \alpha - \beta \vert \gt 0)$$ 

Famous examples are the base ($\mathrm{e} = 2.7\ldots $) and period ($2 \pi \mathrm{i} = 6.28\ldots \mathrm{i}$, or equivalently $\pi = 3.14\ldots $) of the natural [[logarithm]] in the [[complex numbers]] with its [[Archimedean absolute value]], as well as the equivalents $\mathrm{e}$, $2 \pi \mathrm{i}$, and $\pi$ in the [[p-adic complex numbers]] with its [[p-adic norm]]. 

## Related concepts

* [[Archimedean valued field]]

* [[algebraic number]]

* [[irrational number]]

## References

See also

* Wikipedia, _[Transcendental number](https://en.wikipedia.org/wiki/Transcendental_number)_

[[!redirects transcendental number]]
[[!redirects transcendental numbers]]

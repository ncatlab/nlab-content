
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

A **transcendental number** is a [[complex number]] for which the only [[polynomial]] with [[rational number|rational]] [[coefficients]] that has the number as a [[root]] is the zero polynomial. Equivalently in [[classical mathematics]], it is a number which is not a root of a non-zero polynomial with rational coefficients, or a number which is not equal to any [[algebraic number]]. 

## Definition

An complex number $\alpha \in \mathbb{C}$ is **weakly transcendental** if the only [[polynomial function]] with [[rational number|rational]] [[coefficients]] $f \in \mathbb{Q}[x] \subseteq \mathbb{C}^\mathbb{C}$ such that $f(\alpha)$ is equal to zero is the constant polynomial function at zero. 

An complex number $\alpha \in \mathbb{C}$ is **strictly transcendental** if the field extension $\mathbb{Q}(\alpha) \subseteq \mathbb{C}$ is [[isomorphic]] to the [[field of fractions]] $\mathbb{Q}(x)$ of the generic [[polynomial ring]] $\mathbb{Q}[x]$. Equivalently, $\alpha \in F$ is **strictly transcendental** if the complex absolute value of the difference of $\alpha$ and every algebraic number is positive:

$$\mathrm{isTranscendental}(\alpha) \coloneqq \forall \beta \in \mathbb{C}.(\beta \in \overline{\mathbb{Q}}) \Rightarrow (\vert \alpha - \beta \vert \gt 0)$$ 

These two notions coincide in [[classical mathematics]], with both concepts just called **transcendental**; however, they are different in [[constructive mathematics]]. 

## Examples

Famous examples are the base ($\mathrm{e} = 2.7\ldots $) and period ($2 \pi \mathrm{i} = 6.28\ldots \mathrm{i}$, or equivalently $\pi = 3.14\ldots $) of the natural [[logarithm]] in the [[complex numbers]] with its [[Archimedean absolute value]]. 

## Related concepts

* [[absolute value]]

* [[algebraic number]]

* [[irrational number]]

* [[transcendental element]]

## References

See also

* Wikipedia, _[Transcendental number](https://en.wikipedia.org/wiki/Transcendental_number)_

[[!redirects transcendental number]]
[[!redirects transcendental numbers]]

[[!redirects weakly transcendental number]]
[[!redirects weakly transcendental numbers]]

[[!redirects strictly transcendental number]]
[[!redirects strictly transcendental numbers]]
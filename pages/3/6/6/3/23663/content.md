

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

\tableofcontents

## Idea ##

The [[real numbers]] as encountered in prealgebra and high school algebra. 

## Definition ##

Let $\mathbb{Q}$ be the set of [[rational numbers]] and let $[0, 9]$ denote the [[interval]] in the [[natural numbers]] of all natural numbers between $0$ and $9$ inclusive. Infinite decimals representations are elements of $\mathbb{Z} \times [0, 9]^\mathbb{N}$, with the idea that each pair $(i, d)$ consists of an integer $i$ and a sequence of digits $d(n)$ in the infinite decimal representation. The [[series]] 
$$\sum_{n = 0}^\infty i + \frac{d(n)}{10^{n + 1}}$$
can be shown to be a [[Cauchy sequence]]. 

The set of repeating infinite decimal representations is the subset of $\mathbb{Z} \times [0, 9]^\mathbb{N}$ such that for pairs $(i, d)$ in the subset, there exist natural number $k$ and positive natural number $n$ such that the sequence $\lambda m.d(m + k)$ factors through the [[cyclic group]] $\mathbb{Z}/n\mathbb{Z}$. 

$$\lambda m.d(m + k):\mathbb{N} \to \mathbb{Z}/n\mathbb{Z} \to [0, 9]$$

Let $\mathbb{J}$ be the set of non-repeating infinite decimal representations, which is defined here as the [[complement]] of the subset of repeating infinite decimal numbers. These are referred to as the [[irrational numbers]] in the prealgebra and high school algebra literature. 

Then the set of **prealgebra real numbers** or **high school algebra real numbers** is the ([[disjoint union|disjoint]]) [[union]] of $\mathbb{Q}$ and $\mathbb{J}$. The name "prealgebra real numbers" or "high school algebra real numbers" is because this is the definition of the real numbers which most commonly appears in prealgebra and high school algebra textbooks. 

## In constructive mathematics

In [[constructive mathematics]], this definition only results in a subset of the real numbers, since not every real number can be shown to be either a rational number or an irrational number - this statement is equivalent to the [[analytic LPO]] when irrational is defined strictly in the sense of being [[tight apartness relation|apart from]] the rational numbers, and equivalent to the [[analytic WLPO]] when irrational is defined weakly in the sense of the negation of equality with any rational number. 

In addition, not every strictly irrational number is the limit of the series
$$\sum_{n = 0}^\infty i + \frac{d(n)}{10^{n + 1}}$$
given by a non-repeating infinite decimal representation. However, it is still the case that every strictly irrational number which is also a [[Cauchy real number]] is the limit of such a series given by a non-repeating infinite decimal representation. 

## See also ##

* [[real numbers]], [[rational numbers]], [[irrational numbers]]
* [[analytic LPO]], [[analytic WLPO]]
* [[infinite decimal representation of a unit interval]]

## References

* Nichols, Eugene D, et al. Holt Algebra with Trigonometry. Holt, Rinehart and Winston : Harcourt Brace Jovanovich, 1992. 

* Marecek, Lynn, et al. Prealgebra 2e. OpenStax, Rice University, 2020. 

[[!redirects prealgebra real number]]
[[!redirects prealgebra real numbers]]
[[!redirects pre-algebra real number]]
[[!redirects pre-algebra real numbers]]

[[!redirects high school algebra real number]]
[[!redirects high school algebra real numbers]]
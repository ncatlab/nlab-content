
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

Given a [[polynomial function]] with [[complex number|complex]] [[coefficients]] $f:\mathbb{C} \to \mathbb{C}$, a **simple root** $a:\mathbb{C}$ is a [[root]] of $f$ such that the [[derivative]] of $f$ evaluated at $a$ is [[invertible]] in $\mathbb{C}$. 

In classical mathematics (implying acceptance of the law of excluded middle), a simple root $a$ is a root that is not a multiple root: it is not the case that $(x-a)^2$ divides $f(x)$, or "not $f'(a) = 0$". But for the purposes of constructive mathematics, it is preferable to state the condition as "$f(a)$ is [[apartness|apart]] from $0$", or that $f(a)$ is invertible. Hence the definition above. 

## Related concepts

* [[root]]
* [[unramifiable polynomial]]
* [[fundamental theorem of algebra]]

## References

* {#Ruitenberg91} Wim Ruitenberg, Constructing Roots of Polynomials over the Complex Numbers, Computational Aspects of Lie Group Representations and Related Topics, CWI Tract, Vol. 84, Centre for Mathematics and Computer Science, Amsterdam, 1991, pp. 107–128. ([pdf](https://www.mscsnet.mu.edu/~wim/publica/roots_new.pdf))
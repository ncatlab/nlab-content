
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Arithmetic
+-- {: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $\mathcal{C}$ be a [[cartesian monoidal category]] with a [[power object]] [[functor]] $\mathcal{P}:\mathcal{C}\to\mathcal{C}$, and let $M$ be a [[commutative]] [[semigroup]] object in $\mathcal{C}$. There exists a binary endorelation $R = \left( (-) \leq (-)\right)$, $R\colon \mathcal{P}(M \times M)$ such that for all $a,b\colon M$, if there exists a $c\colon M$ such that $a + c = b$, then $(a \leq b) \colon R$. If $\leq$ is a [[preorder]] object, and if for all $a,b\colon M$, there exists a unique smallest element $c$ such that $(a \leq b + c) \colon R$, then $M$ is a __commutative monoid object with monus__, and $c$ is called the __monus__ of $a$ and $b$.

## Related concepts

* [[subtraction]]

* [[difference]]

## See also

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Monus">Monus</a>_
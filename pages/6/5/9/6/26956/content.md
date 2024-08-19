
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[setoid]] or [[Bishop set]] whose [[quotient set]] is a [[local ring]]. 

“local ring setoid” and "Bishop local ring" are placeholder names for a concept which may or may not have another name in the mathematics literature. 

## Definitions

Let $R$ be a [[ring setoid]]. An element $a \in R$ is [[invertible element|invertible]] if there exists an element $b \in R$ such that $a \cdot b \sim 1$. 

A **local ring setoid** or **Bishop local ring** is a [[ring setoid]] (usually also assumed [[commutative ring setoid|commutative]]) such that:

* $0 \sim 1$ is false

* whenever $a + b \sim 1$, $a$ or $b$ is invertible. 

Here are a few equivalent ways to phrase the combined condition:

* Whenever a (finite) [[sum]] is equivalent to $1$, at least one of the summands is invertible.

* Whenever a sum is invertible, at least one of the summands is invertible.

* Whenever a sum of products is invertible, for at least one of the summands, all of its multiplicands are invertible.  (This is not entirely trivial in the noncommutative case, but it\'s still correct.)

* The invertible elements form an [[anti-ideal]]:
  * if $a \sim b$, then $a$ is invertible if and only if $b$ is invertible 
  * $0$ is not invertible 
  * if $a + b$ is invertible, then either $a$ is invertible or $b$ is invertible
  * if $a \cdot b$ is invertible, then $a$ is invertible and $b$ is invertible

In the context of [[excluded middle]], every [[weak local ring setoid]] is a [[local ring setoid]]. Thus, the following is equivalent to the above definitions in classical mathematics:

* The sum of two non-invertible elements is non-invertible.
* The non-invertible elements form an [[ideal]]. 

## Examples

* Given any [[Archimedean ordered field]] $F$, the set of [[Cauchy sequences]] in $F$ is a local ring setoid. 

* Given any [[Archimedean ordered field]] $F$, the set of all [[locators]] of all elements of $F$ is a local ring setoid.

## Related concepts

* [[setoid]]

* [[ring setoid]], [[field setoid]]

* [[local ring]]

[[!redirects local ring setoid]]
[[!redirects local ring setoids]]

[[!redirects Bishop local ring]]
[[!redirects Bishop local rings]]
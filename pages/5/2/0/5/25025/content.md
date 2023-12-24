
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

In this article we [[axioms|axiomatize]] the [[algebra|algebraic]], [[order theory|order theoretic]], and [[metric space|metric]] properties which are common to the basic [[types]] of [[numbers]] found in [[mathematics]]: the [[natural numbers]], [[integers]], [[rational numbers]], and [[Dedekind real numbers]], and which remain valid in [[constructive mathematics|constructive]] and [[predicative mathematics]]. 

## Definition

A **number line rig** $S$ is 

* A [[commutative rig]] $(S, 0, 1, +, \cdot)$. It follows that there is a [[rig homomorphism]] $h:\mathbb{N} \to S$, since the natural numbers are the [[initial object|initial]] [[commutative rig]]
 
* with a [[strict total order]] $(S, \lt)$ such that
  * $0 \lt 1$
  * $0 \lt a$ and $0 \lt b$ imply that $0 \lt a + b$
  * $0 \lt a$ and $0 \lt b$ imply that $0 \lt a \cdot b$
* with a [[tight apartness relation]] $(S, \#)$ such that $a \# b$ if and only if $a \lt b$ or $b \lt a$
* with a [[pseudolattice]] structure $(S, \leq, \min, \max)$ such that 
  * $a \leq b$ if and only if $\neg (b \lt a)$
  * $a \leq b$ if and only if $a + c \leq b + c$
* with a [[metric]] $\rho:S \times S \to S$ such that $\rho(a, b) + \min(a, b) = \max(a, b)$. Every element in the image of $\rho$ is always not less than zero, because by definition of a pseudolattice, $\min(a, b) \leq \max(a, b)$. This can be shown to be a translation-invariant metric, where it follows that addition is a [[cancellative monoid]]:
  * $a = b$ if and only if $\rho(a, b) = 0$
  * $\rho(a, b) = \rho(b, a)$
  * $\rho(a, b) \leq \rho(a, c) + \rho(c, b)$
  * $\rho(a + c, b + c) = \rho(a, b)$. 
* The [[multiplicative subset of cancellative elements]] is the set of elements apart from zero
* and $S$ satisfies the [[Archimedean property]]: for every [[positive number|positive]] element $0 \lt a$, there is a positive natural number $n$ such that $a \lt h(n)$, and there is a positive natural number $m$ such that $1 \lt h(m) \cdot a$. 

## Group completion, rig of fractions, and completions

Given any number line rig, one could construct the [[group completion]], which results in a [[Archimedean integral domain]]. One could also [[localization of a ring|localize]] at the subset of [[regular elements]], which results in a rig of fractions. Doing both results in an [[Archimedean field]]. One could also complete the resulting field by [[Dedekind cuts]], resulting in the [[Dedekind real numbers]], or complete it by [[Cauchy sequences]], resulting in a [[sequentially Cauchy complete]] [[Archimedean field]] such as the [[HoTT book real numbers]]. 

## See also

* [[natural numbers]]
* [[integers]]
* [[rational numbers]]
* [[real numbers]]
* [[streak]]
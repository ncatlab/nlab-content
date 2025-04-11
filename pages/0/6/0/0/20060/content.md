> This page is about [[de Morgan algebras]] satisfying an extra condition.  For Kleene star algebras in relation to [[regular expressions]], see there.

----

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
=--
=--

# Kleene algebra

* table of contents
{: toc}

## Definition

A **Kleene algebra** is a [[de Morgan algebra]] $D$ satisfying $x \wedge \neg x \le y \vee \neg y$ for all $x,y\in D$. Since the order is definable in terms of the lattice operators, this can be stated as the equation

$$ x \wedge \neg x \wedge (y \vee \neg y) = x \wedge \neg x. $$

## Examples

* Any [[Boolean algebra]] is a Kleene algebra, with $\neg$ the logical negation.
* The unit interval $[0,1]$ is a Kleene algebra, with $\neg x = (1-x)$. 

## Related concepts

* Kleene algebras are used in one form of [[cubical type theory]]

## References

* {#CF77} [[William H Cornish]], [[Peter R Fowler]], *Coproducts of de morgan algebras*, Bulletin of the Australian Mathematical Society, 16(01):1–13, 1977. ([pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/D86F551CF77BE8374CD4BFB1A73F73B6/S0004972700022966a.pdf/coproducts-of-de-morgan-algebras.pdf))

* {#CF79} [[William H Cornish]], [[Peter R Fowler]], *Coproducts of kleene algebras*, Journal of the Australian Mathematical Society (Series A), 27(02):209–220, 1979 ([pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/AAD3D8E6D208205C39C54D0873AEB883/S1446788700012131a.pdf/div-class-title-coproducts-of-kleene-algebras-div.pdf))

[[!redirects Kleene algebras]]

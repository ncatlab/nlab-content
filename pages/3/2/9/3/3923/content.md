
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **symmetric monoidal $\dagger$-category** is a [[symmetric monoidal category]] that is also a $\dagger$-[[dagger-category|category]] for which:

1. $(f \otimes g)^\dagger = f^\dagger \otimes g^\dagger$ for every pair of [[morphisms]] $f,g$

1. the [[associator]], left and right [[unitor|unitors]], and [[braiding]] are all [[unitary morphism|unitary]].

If the category is also a [[compact closed category]] in a compatible way, then it is called a [[dagger-compact category]].

## Alternative definition ##

A **symmetric monoidal dagger category** is a [[braided monoidal dagger category]] $C$ which is also a [[symmetric monoidal category]], i.e. such that for all [[objects]] $A \in Ob(C)$ and $B \in Ob(C)$, $\beta_{A,B} \circ \beta_{B, A} = \Iota_{A,B}$. 

## Examples ##

* [[compact closed dagger category]]

* [[symmetric monoidal groupoid]], [[2-group]]

## See also ##

* [[dagger category]]

* [[monoidal dagger category]]

* [[braided monoidal dagger category]]

* [[symmetric monoidal category]]

## References

* [[Peter Selinger|P. Selinger]], Dagger compact closed categories and completely positive maps, _Proceedings of the 3rd International Workshop on Quantum Programming Languages_, Chicago, June 30&#8211;July 1, 2005. [web](http://www.mscs.dal.ca/~selinger/papers.html#dagger)

[[!redirects symmetric monoidal †-category]]
[[!redirects symmetric monoidal †-categories]]
[[!redirects symmetric monoidal dagger-category]]
[[!redirects symmetric monoidal dagger-categories]]
[[!redirects symmetric monoidal dagger categories]]

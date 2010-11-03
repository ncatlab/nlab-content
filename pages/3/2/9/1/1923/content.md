
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
* table of contents
{:toc}

## Idea

A _symmetric monoidal functor_ is a [[functor]] $F : C \to D$ between [[symmetric monoidal category|symmetric monoidal categories]] that is a [[monoidal functor]] which respects the symmetry on both sides.

## Defnition

A [[monoidal functor]] $F : (C,\otimes) \to (D, \otimes)$ between [[symmetric monoidal categories]] is **symmetric** of for all $A,B \in C$ the diagram

$$
  \array{
    F A \otimes F B &\stackrel{\sigma}{\to}& F B \otimes F A
    \\
    {}^{\mathllap{\nabla_{A,B}}}\downarrow 
    && 
    \downarrow^{\mathrlap{\nabla_{B,A}}}
    \\
    F(A\otimes B) &\stackrel{F(\sigma)}{\to}& F(B \otimes A)
  }
$$

commutes, where $\sigma$ denotes the symmetry isomorphism both of $C$ and $D$.



## Properties

As long as it goes between symmetric monoidal categories a symmetric monoidal functor is the same as a [[braided monoidal functor]]. 


## Related concepts

* [[monoidal functor]]

* [[strong monoidal functor]]

* [[lax monoidal functor]]

* [[oplax monoidal functor]]

* [[bilax monoidal functor]]

* [[Frobenius monoidal functor]]

* [[braided monoidal functor]]

* **symmetric monoidal functor**

## References

An exposition is in

* [[John Baez]], [Some definitions everyone should know](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).


[[!redirects symmetric monoidal functor]]
[[!redirects symmetric monoidal functors]]

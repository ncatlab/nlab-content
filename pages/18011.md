
> This entry as written remains a partial duplicate of *[[internal hom]]*. See there for more. But [[lattices]] with internal homs are also known as *[[residuated lattice|residuated lattices]]*.

#Contents#
* table of contents
{:toc}

## Idea

Residuals are "[[exponential object|exponential objects]] for a [[monoidal category]]": they are compatible with the monoidal product $\otimes$. Because $\otimes$ is (in general) not symmetric, we distinguish a *left residual* and a *right residual*. In a [[symmetric monoidal category]], these are the same.

Recall the definition of an exponential object for a cartesian category:

Let $A,C$ be two objects of the cartesian category. An _exponential object_ is an object $C^A$ with data $\mathit{ev},\varepsilon$ such that for every object $B$, there is a one-to-one mapping between morphisms

$$ f : A \times B \to C $$

and morphisms

$$ \varepsilon[f] : B \to C^A \; . $$

The backwards direction is given by $\mathit{ev} : A \times C^A \to A$, namely $f = \mathit{ev} \circ (A \times \varepsilon[f])$. Going back and forth is also required to be the identity: for $g : B \to C^A$, we must have $g = \varepsilon[ev \circ (A \times g)]$.

## Definition

Let $A,C$ be two objects of a monoidal category.

A _left residual_ of $C$ by $A$ is an object $A{\backslash}C$ together with an evaluation map $\mathit{\lev} : A \otimes (A{\backslash}C) \to C$ and for objects $B$ a transformation from morphisms

$$ f : A \otimes B \to C $$

to morphisms

$$ \lambda[f] : B \to A{\backslash}C $$

such that $f = \mathit{\lev} \circ (A \otimes \lambda[f])$, and $g = \lambda[\mathit{\lev} \circ (A \otimes g)]$ for every morphism $g : B \to A{\backslash}C$.

A _right residual_ of $C$ by $A$ is an object $C{/}A$ together with an evaluation map $\mathit{rev} : (C{/}A) \otimes A \to C$ and for objects $B$ a transformation from morphisms

$$ f : B \otimes A \to C $$

to morphisms

$$ \rho[f] : B \to C{/}A $$

such that $f = \mathit{rev} \circ (\rho[f] \otimes A)$, and $g = \rho[\mathit{rev} \circ (g \otimes A)]$ for every morphism $g : B \to C{/}A$.


Mnemonic for the notation: $C{/}A$ looks like dividing $C$ by $A$ on the right, and $A{\backslash}C$ looks like dividing $C$ by $A$ on the left.

## Properties

Left and right residuals are unique up to isomosphism.

## Examples

* In every cartesian category, the exponential objects are left and right residuals.
* Any [[monoidal closed category]] has all right residuals.

## Related concepts

* [[exponential object]]
* [[internal hom]]
* [[monoidal closed category]]

[[!redirects left residual]]
[[!redirects right residual]]

## References

The term "residual" for left/right [[internal homs]] is (non-standard and) used in 

* [[Paul-André Melliès]] and [[Noam Zeilberger]], Def. 12 Functors Are Type Refinement Systems. In _Proceedings of the 42nd Annual ACM SIGPLAN-SIGACT Symposium on Principles of Programming Languages_, POPL '15, 3&#8211;16. New York, NY, USA, 2015. ACM. doi:[10.1145/2676726.2676970](http://doi.acm.org/10.1145/2676726.2676970).

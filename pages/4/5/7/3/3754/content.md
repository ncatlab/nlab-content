
# Semifunctors
* table of contents
{: toc}

## Definition

A **semifunctor** $F$ from a [[semicategory]] $C$ to a semicategory $D$ is a map sending each [[object]] $x \in C$ to an object $F(x) \in D$ and each [[morphism]] $f : x \to y$ in $C$ to morphism $F(f) : F(x) \to F(y)$ in $D$, such that

* $F$ preserves [[composition]]: $F(g\circ f) = F(g)\circ F(f)$ whenever the left-hand side is well-defined.

## Examples

The embedding of a category into another category where $F$ maps $id_X$ to a nontrivial idempotent endomorphism of $F(X)$ is a semifunctor but not a functor.


[[!redirects semifunctor]]
[[!redirects semifunctors]]

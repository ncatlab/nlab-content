
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* tabe of contents
{:toc}

## Definition

For $n \in \mathbb{N}$
a [[morphism]] $f \colon X \to Y$ in an [[(infinity,1)-category]] is an **$n$-monomorphism** equivalently if 

* in its [[n-image]] factorization

  $$
    f \colon X \to im_n(f) \to Y
  $$

  the first morphism is an [[equivalence in an (infinity,1)-category]]

* it is an [[n-connected|(n-2)-truncated morphism]];

### In homotopy type theory

In [[homotopy type theory]], a [[function]] $f \colon X \to Y$ is an $n$-monomorphism if its $n$-image factorization is via an [[equivalence in homotopy type theory]].

More explicitly, given a natural number $n:\mathbb{N}$ and types $A$ and $B$, a function $f:A \to B$ is a __$n$-monomorphism__ if for all terms $b:B$ the [[fiber]] of $f$ over $b$ has an [[homotopy level]] of $n$. 

$$isMonic(n, f) \coloneqq \prod_{b:B} hasHLevel(n, fiber(f, b))$$

A [[equivalence]] is a $0$-monomorphism. $1$-monomorphisms are typically just called __monomorphisms__ or __[[embeddings]]__. 

The type of all $n$-monomorphisms with domain $A$ and codomain $B$ is defined as
$$Monos(n, A, B): \sum_{f:A \to B} isMonic(n, f)$$

## Dual concept

The dual concept is that of _[[n-epimorphism]]_.

## Examples

* $0$-monomorphism are precisely the [[equivalences]]. 

* Every morphism is an $\infty$-monomorphism.

* 1-monomorphisms are often just called [[monomorphisms in an (∞,1)-category]]. The 1-monomorphisms into a fixed object are called the [[subobject in an (∞,1)-category|subobjects]] of that object.

* A 1-monomorphism between [[0-truncated]] objects is precisely an ordinary [[monomorphism]] in the underlying [[1-topos]].

## Related concepts

* [[Postnikov system]]

* [[(n-connected, n-truncated) factorization system]]

* [[subtype]]

[[!redirects n-monomorphisms]]

[[!redirects 0-monomorphism]]
[[!redirects 0-monomorphisms]]
[[!redirects 1-monomorphism]]
[[!redirects 1-monomorphisms]]
[[!redirects 2-monomorphism]]
[[!redirects 2-monomorphisms]]


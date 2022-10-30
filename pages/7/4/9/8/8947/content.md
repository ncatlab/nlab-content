
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
* table of contents
{:toc}

## Definition

In an [[(∞,1)-topos]] a morphism $f \colon X \to Y$ is an _$n$-epimorphism_ for $n \in \mathbb{N}$ equivalently if 

* in its [[n-image]] factorization 

  $$
    f \colon X \to im_n(f) \to Y
  $$

  the second morphism is an [[equivalence in an (∞,1)-category]];

* it is an [[n-connected|(n-2)-connected]] object in the [[slice (∞,1)-topos]] $\mathbf{H}_{/Y}$. 

## Properties

The $n$-epimorphisms in an [[(∞,1)-topos]] are the left half of the [[(n-epi, n-mono) factorization system|((n-2)-epi, (n-2)-mono) factorization system]] which factors every morphism through its [[n-image]].

## Examples

* The $\infty$-epimorphisms are precisely the [[equivalences]].

* The 1-epimorphism are the [[effective epimorphisms in an (∞,1)-category|effective epimorphisms]].

* Every morphism is a $0$-epimorphism.

* The 1-epimorphisms between [[0-truncated]] objects are precisely the ordinary [[epimorphisms]] in the underlying [[1-topos]].

## Related concepts

* [[Postnikov system]]

* [[n-types cover]]

## References

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

Disucssion in [[homotopy type theory]] is in 

* [[Univalent Foundations Project]], section 7.6 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_


[[!redirects n-epimorphisms]]

[[!redirects 1-epimorphism]]
[[!redirects 1-epimorphisms]]



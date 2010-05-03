#Contents#
* automatic table of contents goes here
{:toc}


## Idea

Just as a [[functor]] is a [[morphism]] between [[categories]], so a _closed functor_ is a morphism between [[closed categories]].  Closed functors come in varying levels of strictness and strength.

This is speculative, working in analogy with [[monoidal functors]].  It may or may not already appear in the literature.


## Definition

A __strict closed functor__ is a [[functor]] $F : C \to D$ between [[closed categories]] that respects [[internal homs]] and the unit object on the nose:

$$ F(I_C) = I_D ,$$

$$ F([X,Y]) = [F(X),F(Y)] .$$

One should also consider *weak* (aka *strong*) and *(op)lax* versions, in analogy with [[monoidal functors]].  In the former case, we replace each [[equality]] with a [[natural isomorphism]]; in the latter, we replace it with a possibly non-invertible [[natural transformation]] in one direction or the other.  But these should also be made to satisfy [[coherence law]]s that somebody should work out.


[[!redirects closed functor]]
[[!redirects closed functors]]

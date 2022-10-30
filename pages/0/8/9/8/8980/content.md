
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

Given a [[modal type theory]], hence [[type theory]] equipped with a [[closure operator]] [[modality]] $\Diamond$ ([[monad|monadic]]) or $\Box$ ([[comonad|comonadic]]), the a [[type]] $X$ is _modal_ with respect to $\Diamond$/$\Box$ if 

* the [[unit of an adjunction|unit]] $\eta \colon X \to \Diamond X$

* or the counit $\epsilon \colon \Box X \to X$

is an [[equivalence]]. 

The collection of modal types forms the _closure_ of the given closure operator. 

Under [[propositions as types]] a [[proposition]] that is modal is also called a _[[stable proposition]]_.

## Related concepts

* [[reflective subcategory]]

* [[reflective sub-(∞,1)-category]]

* [[modal type theory]]

[[!redirects modal types]]


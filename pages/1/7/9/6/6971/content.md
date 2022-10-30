
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Extensional type theory_ denotes the flavor of [[type theory]] in which [[identity types]] are demanded to be [[propositions]] / of [[h-level 1]].  In other words, they are determined by their [[extension (semantics)|extensions]] --- the collection of pairs of points which are equal.  Type theory which is not extensional is called _[[intensional type theory]]_.

Note that some type theorists instead use "extensional type theory" to refer to type theory in which [[function extensionality]] holds.  In general this property is orthogonal to the one considered here: function extensionality can hold or fail in both extensional and intensional type theory.  In particular, [[homotopy type theory]] is [[intensional type theory|intensiona]] in that [[identity types]] are crucially _not_ demanded to be [[propositions]], but [[function extensionality]] is often assumed (in terms of these intensional identity types, of course) --- in particular, it follows from the [[univalence axiom]].


## Definition

The basic definition of [[identity types]] as an [[inductive type]] family makes them intensional.  There are many more or less equivalent ways to force them to become extensional.

1. We can add as an axiom the "uniqueness of identity proofs" (UIP) property that any two inhabitants of the same identity type $Id_A(x,y)$ are themselves equal (in the corresponding higher identity type).

1. We can add a definitional [[eta-conversion]] rule for the identity types (see [here](/nlab/show/identity+type#EtaConversion)).

1. We can add an "equality reflection" rule saying that if two terms are propositionally equal (i.e. the identity type $Id_A(x,y)$ is inhabited), then they are also [[definitional equality|definitionally equal]], and moreover any inhabitant of an identity type is definitionally equal to reflexivity.

1. We can add Streicher's *axiom K* which says that any inhabitant of a self-equality type $Id_A(x,x)$ is equal to the identity/reflexivity equality $1_x$.  (Axiom K is so named because $K$ comes after $J$, and $J$ usually denotes the eliminator for identity types.)

1. In the presence of [[dependent sum types]], we can add an axiom saying that if $(a,b_1)$ and $(a,b_2)$ are pairs in a dependent sum $\sum_{x\colon A} B(x)$ with the same first component, and the identity type $Id_{\sum_{x\colon A} B(x)}((a,b_1), (a,b_2))$ is inhabited, then so is $Id_a(b_1,b_2)$.

1. We can allow definition of functions by a strong form of *pattern matching*, as in unmodified [[Agda]].  The relevant "extra strength" is to allow output *types* of a pattern match which are only well-defined *after* the pattern has been matched.

These approaches have different computational properties, but semantically they all have the same effect of making the type theory extensional.


## Properties

### Decidability

Only the intensional, but not the [[extensional type theory|extensional]] [[Martin-Löf type theory]], is [[decidable]].  See _[[intensional type theory]]_ for more on this.

## References

Among the most thorough recent treatments of extensional type theory are

* [[Ieke Moerdijk]], E. Palmgren, _Wellfounded trees in categories_. Ann. Pure Appl. Logic, 104:189-218 (2000)

* [[Ieke Moerdijk]], E. Palmgren, _Type theories, toposes and constructive set theory: predicative aspects of AST_,  Ann. Pure Appl. Logic, 114:155-201, (2002)

[[!redirects extensional type theories]]
[[!redirects uniqueness of identity proofs]]
[[!redirects UIP]]
[[!redirects axiom K]]

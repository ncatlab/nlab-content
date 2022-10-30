
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

_Extensional type theory_ denotes the flavor of [[type theory]] in which [[identity types]] are demanded to be [[propositions]] / of [[h-level 1]].  In other words, they are determined by their [[extension (semantics)|extensions]] --- the collection of pairs of points which are equal.  Type theory which is not extensional is called _[[intensional type theory]]_.

Note that some type theorists instead use "extensional type theory" to refer to type theory in which [[function extensionality]] holds.  In general this property is orthogonal to the one considered here: function extensionality can hold or fail in both extensional and intensional type theory.  In particular, [[homotopy type theory]] is [[intensional type theory|intensional]] in that [[identity types]] are crucially _not_ demanded to be [[propositions]], but [[function extensionality]] is often assumed (in terms of these intensional identity types, of course) --- in particular, it follows from the [[univalence axiom]].


## Definition

The basic definition of [[identity types]] as an [[inductive type]] family makes them intensional.  There are many more or less equivalent ways to force them to become extensional.

1. We can add as an axiom the "uniqueness of identity proofs" (UIP) property that any two inhabitants of the same identity type $Id_A(x,y)$ are themselves equal (in the corresponding higher identity type).

1. We can add a definitional [[eta-conversion]] rule for the identity types (see [here](/nlab/show/identity+type#EtaConversion)).

1. We can add an "equality reflection" rule saying that if two terms are propositionally equal (i.e. the identity type $Id_A(x,y)$ is inhabited), then they are also [[definitional equality|definitionally equal]], and moreover any inhabitant of an identity type is definitionally equal to reflexivity.

1. We can add Streicher's *axiom K* which says that any inhabitant of a self-equality type $Id_A(x,x)$ is equal to the identity/reflexivity equality $1_x$.  (Axiom K is so named because $K$ comes after $J$, and $J$ usually denotes the eliminator for identity types.)

1. In the presence of [[dependent sum types]], we can add an axiom saying that if $(a,b_1)$ and $(a,b_2)$ are pairs in a dependent sum $\sum_{x\colon A} B(x)$ with the same first component, and the identity type $Id_{\sum_{x\colon A} B(x)}((a,b_1), (a,b_2))$ is inhabited, then so is $Id_a(b_1,b_2)$.

1. We can allow definition of functions by a strong form of *pattern matching*, as in unmodified [[Agda]].  The relevant "extra strength" is to allow output *types* of a pattern match which are only well-defined *after* the pattern has been matched.

These approaches have different computational properties, but semantically they all have the same effect of making the type theory extensional.

+-- {: .query}
I don't want to unilaterally edit this page, but #3 above is fairly different than any of the others (except maybe #2), and it is pretty much the only one that I've ever heard type theorists talking about when they say "extensional type theory." It is the difference between Martin-L&#246;f's intensional and extensional type theory. Intensional has the J eliminator, and extensional has the _inference rule_ from propositional equality to judgmental equality.

Dependent pattern matching, K, uniqueness of identity proofs and the like don't get you the equivalent of reflecting the propositions back into the judgments, and that is what makes extensional type theory in the eyes of type theorists (as far as I've encountered), not the dimension of the identity types. For instance, Agda is considered intensional despite having K, and even Observational Type Theory ala Conor McBride, which adds lots of extensionality axioms for various types, and eta-ish rules when possible, is still arguably intensional in this sense. And that is the whole point in OTT's case, because the decidability issues (mentioned below) are tied to extensionality in the inference rule sense, not any homotopy sense.'

Also, I expect the bit about functional extensionality came from a discussion with me on n-cafe. But, it's not really true that type theorists use 'extensional type theory' to refer to theories in which functional extensionality holds. I believe my point in that discussion was that 'extensional equality type' (or similar) suggested to me a type that reified the extensional equivalence (equality) relation of the type it was defined for (so, Eq A a b would have an inhabitant if a is extensionally equal to b of type A), and didn't immediately suggest an identity type that was a homotopy proposition. For instance, the identity types in OTT reify extensional equality in this sense. And extensional type theories (for instance, NuPRL) typically incorporate this, because they can, whereas Agda (for instance) does not. HTT identity types are reifying extensional equality of functions, as well, and perhaps would work for coinductive types as well (whenever those get worked out).

But that is about my impression of "(extensional identity) type" not "extensional (identity type)," the latter of which might be an identity type in extensional type theory, which has little to do with what sort of relations it's reifying.

--- Dan Doel

=--

## Properties

### Decidability

Only the intensional, but not the extensional, [[Martin-Löf type theory]] is [[decidable]].  See _[[intensional type theory]]_ for more on this.


## References

Among the most thorough recent treatments of extensional type theory are

* [[Ieke Moerdijk]], E. Palmgren, _Wellfounded trees in categories_. Ann. Pure Appl. Logic, 104:189-218 (2000)

* [[Ieke Moerdijk]], E. Palmgren, _Type theories, toposes and constructive set theory: predicative aspects of AST_,  Ann. Pure Appl. Logic, 114:155-201, (2002)



[[!redirects extensional type theory]]
[[!redirects extensional type theories]]
[[!redirects uniqueness of identity proofs]]
[[!redirects UIP]]
[[!redirects axiom K]]
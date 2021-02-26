
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

The _interval type_ is an [[axiom|axiomatization]] of the cellular [[interval object]] in the context of [[homotopy type theory]].

## Definition

As a [[higher inductive type]], the interval is given by

    Inductive Interval : Type
      | left : Interval
      | right : Interval
      | segment : Id Interval left right

This says that the type is inductive constructed from two [[terms]] in the interval, whose [[semantics|interpretation]] is as the endpoints of the interval, together with a term in the [[identity type]] of paths between these two terms, which interprets as the 1-cell of the interval

$$
  left \stackrel{segment}{\to} right
  \,.
$$

## Properties

* An interval type is provably [[contractible type|contractible]].  Conversely, any contractible type satisfies the rules of an interval type up to propositional equality.

* On the other hand, postulating an interval type with *definitional* computation rules for `left` and `right` implies [[function extensionality]]. ([Shulman](#Shulman)).

* An interval type is a [[suspension type]] of the [[unit type]]. 

## Related concepts

* [[interval]], [[interval object]]

* [[suspension type]]

## References

* [[Mike Shulman]], _An interval type implies functional extensionality_ ([blog post](http://homotopytypetheory.org/2011/04/04/an-interval-type-implies-function-extensionality/#comment-697))
 {#Shulman}

[[!redirects interval types]]
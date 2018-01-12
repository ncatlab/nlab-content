+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

If a [[functor]] represents a given [[profunctor]], then the action of the functor on morphisms is determined by the action of the profunctor and the representation isomorphism.

This lemma can make it easier to define certain [[adjoint functors]], and is also implicit in [[type theory]] where type connectives are presentation of functors, but the action on morphisms is derivable rather than primitive.

## Statement

Let $R : C $&#8696;$ D$ be a profunctor, i.e., a functor from $D^{op}\times C \to Set$ and $F : C\to D$ a functor that [[representable functor|represents]] it by a natural isomorphism $\alpha : R \Rightarrow D(-,F=)$.
Then the action of $F$ on morphisms is determined by $R,\alpha$ by the formula:

$$F(f : c \to c') = \alpha(R(id_{F c}, f)(\alpha^{-1}(id_{F c}))$$

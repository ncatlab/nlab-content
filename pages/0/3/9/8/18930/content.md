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

## Examples

Consider the [[cartesian product]] functor, which can be defined by saying that it represents the profunctor $R_{\times} : C^2 $&#8696;$ C$ defined by 
\[ R(A,(B,C)) = R(A,B) \times R(A,C) \]

whose action is defined as $R(f,(g,h))(k,l) = (g \circ k \circ f, h \circ l \circ f)$.
Then the universal property of the product functor $\times : C^2 \to C$ is encapsulated in the natural isomorphism $\alpha_{A,B,C} : R_{\times}(A,(B,C)) \Rightarrow C(A,B\times C)$.
The forward direction of $\alpha$ is the "pairing" operation of the product, so we write it as $(-,=)$.
By the [[Yoneda lemma]], the inverse of $\alpha$ can be reconstructed from it's action on the identity, which in this case gives us the two projections: $(\pi_{A,B},\pi'_{A,B}) = \alpha^{-1}_{A\times B, A,B}$.

Then, by the above lemma, the action of $\times$ on functions is equal to:
$$f \times g = (f \circ \pi_{A,B}, g \circ \pi'_{A,B})$$

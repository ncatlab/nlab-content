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

## Representation Presentation of a Functor

Since the action of the functor on morphisms is determined by the data of a representation of a profunctor, we can even *define* the functor by giving that data. Crucially though, what does it mean for $\alpha$ to be natural if we have not yet defined the action of $F$? It turns out that it is sufficient to require naturality in $D$ only. Furthermore, $\alpha^{-1}$ can be recovered from its action on the identity by the [[Yoneda lemma]].

A *right functor presentation* from $C$ to $D$ consists of

1. A profunctor $R : C $&#8696;$ D$.
2. An object function $F_0 : C_0 \to D_0$.
3. An "introduction rule" $\iota_{c,d} : R(d,c) \to D(d,F_0c)$.
4. A "universal morphism" $\epsilon_c : R(c,F_0c)$.

satisfying

1. *left-naturality of $\iota$* $\iota \circ R(f,id)) = D(f,id) \circ \iota$
2. *isomorphism*, $R(-,id)(\epsilon)$ is an inverse to $\iota$.

Then given a right functor presentation $(R, F_0, \iota, \epsilon)$, we can define a functor that represents $R$ by extending $F$ to act on morphisms by $F_1(f) = \iota(R(id, f)(c))$. Then the functoriality of $F$ and naturality of $\alpha$ and $\alpha^{-1}$ follow from the above equalities.

## In Type Theory

A right functor presentation consists of exactly the data that define a [[negative type]] in type theory. The introduction rule corresponds to the introduction rule of course. The universal morphism corresponds to the (0 or more) elimination rules that are collected into $R(c,F_0 c)$. The isomorphism property corresponds to the $\beta$ and $\eta$ equalities.

This lemma is usually not explicitly invoked in initiality theorems for type theories, but gives an explanation for why the "dogma" of introduction and elimination rules is so effective in practice.

## Examples

Consider the [[cartesian product]] functor, which can be defined by saying that it represents the profunctor $R_{\times} : C^2 $&#8696;$ C$ defined by 
\[ R(A,(B,C)) = R(A,B) \times R(A,C) \]

whose action is defined as $R(f,(g,h))(k,l) = (g \circ k \circ f, h \circ l \circ f)$.
Then the universal property of the product functor $\times : C^2 \to C$ is encapsulated in the natural isomorphism $\alpha_{A,B,C} : R_{\times}(A,(B,C)) \Rightarrow C(A,B\times C)$.
The forward direction of $\alpha$ is the "pairing" operation of the product, so we write it as $(-,=)$.
By the [[Yoneda lemma]], the inverse of $\alpha$ can be reconstructed from it's action on the identity, which in this case gives us the two projections: $(\pi_{A,B},\pi'_{A,B}) = \alpha^{-1}_{A\times B, A,B}$.

Then, by the above lemma, the action of $\times$ on functions is equal to:

$$f \times g = (f \circ \pi_{A,B}, g \circ \pi'_{A,B})$$

## References

A similar theorem, but for presenting [[adjoint functors]] without defining $R$ first is given (and generalized to the internal setting) in

* [[Ross Street]], [The core of adjoint functors](https://arxiv.org/abs/1112.0094)

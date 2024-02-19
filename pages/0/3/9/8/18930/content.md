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

This theorem can make it easier to define certain [[adjoint functors]], and is also implicit in [[type theory]] where type connectives are presentation of functors, but the action on morphisms is derivable rather than primitive.

## Statement

Let $R : C $&#8696;$ D$ be a profunctor, i.e., a functor from $D^{op}\times C \to Set$ and $F : C\to D$ a functor that [[representable functor|represents]] it by a natural isomorphism $\alpha : R \Rightarrow D(-,F=)$.
Then the action of $F$ on morphisms is determined by $R,\alpha$ by the formula:

$$F(f : c \to c') = \alpha \Big( R(id_{F c}, f)\big(\alpha^{-1}(id_{F c})\big) \Big)$$
or the following composite acting on $id_{F c}$:
$$ D(F c, F c) \xrightarrow{\alpha^{-1}} R (Fc, c) \xrightarrow{R (id_{F c}, f)} R (F c, c') \xrightarrow{\alpha} D(F c, F c') $$

## Representation Presentation of a Functor

Since the action of the functor on morphisms is determined by the data of a representation of a profunctor, we can even *define* the functor by giving that data. Crucially though, what does it mean for $\alpha$ to be natural if we have not yet defined the action of $F$? It turns out that it is sufficient to require naturality in $D$ only. Furthermore, $\alpha^{-1}$ can be recovered from its action on the identity by the [[Yoneda lemma]].

A *right functor presentation* from $C$ to $D$ consists of

1. A profunctor $R : C $&#8696;$ D$.
2. An object function $F_0 : C_0 \to D_0$.
3. An "introduction rule" $\iota_{c,d} : R(d,c) \to D(d,F_0c)$.
4. A "universal morphism" $\epsilon_c : R(F_0c,c)$.

satisfying

1. *left-naturality of $\iota$*, meaning $\iota \circ R(f,id) = D(f,id) \circ \iota$
2. *isomorphism*, $R(-,id)(\epsilon)$ is an inverse to $\iota$.

+-- {: .num_theorem}
###### Theorem

Given a profunctor $R : C $&#8696;$ D$, right functor presentations representing $R$ are in bijection with functors $F : C \to D$ with a natural isomorphism $\alpha_{c,d} : R(c,d) \equiv D(c,Fd)$.

=--

Given a right functor presentation $(R, F_0, \iota, \epsilon)$, we can define a functor that represents $R$ by extending $F$ to act on morphisms by $F_1(f) = \iota(R(id, f)(c))$. Then the functoriality of $F$ and naturality of $\alpha$ and $\alpha^{-1}$ follow from the above equalities.

Given a functor representing $R$, the universal morphism is defined as in the [[Yoneda lemma]]: $\epsilon_c = \alpha^{-1}(id)$.

## In Type Theory

A right functor presentation consists of exactly the data that define a [[negative type]] in type theory. The introduction rule of the presentation, unsurprisingly corresponds to the introduction rule in the type theory. The universal morphism corresponds to the (0 or more) elimination rules that are collected into $R(c,F_0 c)$. Left-naturality corresponds to the definition of [[substitution]] for the introduction rule. The isomorphism property corresponds to the $\beta$ and $\eta$ equalities.

This theorem is usually not explicitly invoked in initiality theorems for type theories, but gives an explanation for why the "dogma" of introduction and elimination rules is so effective in practice.

## Examples

1. Decategorifying to the poset case, we get that if a function $f : A \to B$ represents a "relational profunctor" $R$ , i.e. a subset $R \subseteq A \times B$ that is downward closed in $A$ and upper closed in $B$, then $f$ is monotone.
2. Consider the [[cartesian product]] functor, which can be defined by saying that it represents the profunctor $R_{\times} : C^2 $&#8696;$ C$ defined by 
\[ R_{\times}(a,(b_1,b_2)) = C(a,b_1) \times C(a,b_2) \]

whose action is defined as $R_{\times}(f,(g,h))(k,l) = (g \circ k \circ f, h \circ l \circ f)$.
Then the universal property of the product functor $\times : C^2 \to C$ is encapsulated in the natural isomorphism $\alpha_{a,b_1,b_2} : R_{\times}(a,(b_1,b_2)) \Rightarrow C(a,b_1\times b_2)$.
By the [[Yoneda lemma]], the inverse of $\alpha$ can be reconstructed from its action on the identity, which in this case gives us the two projections: $(\pi_1,\pi_2) = \alpha^{-1}_{b_1\times b_2, b_1,b_2}(id)$.

Then, by the above theorem, the action of $\times$ on functions is equal to:

$$f \times g = \alpha(f \circ \pi_1, g \circ \pi_2)$$

## References

A similar theorem, but for presenting [[adjoint functors]] without defining $R$ first is given (and generalized to the internal setting) in

* [[Ross Street]], [The core of adjoint functors](https://arxiv.org/abs/1112.0094)

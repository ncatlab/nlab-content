+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
In any context it is interesting to ask when a contravariant hom-functor $\operatorname{Hom}(-,X)$ reflects isomorphisms, i.e. if homming into an object is enough to distinguish isomorphism classes. In a $2$-categorical setting, the analogous question is if homming into an object reflects equivalences.

## Definition

_Conceptual completeness_ refers to the result of Makkai and Reyes that in the $2$-category $\mathbf{Pretop}$ of [[pretopos]]es, homming into the pretopos [[Set]] $\operatorname{Hom}_{\mathbf{Pretop}}(-,\mathbf{Set}) : \mathbf{Pretop} \to \mathbf{Cat}$ reflects equivalences.

That is, if $f : T_1 \to T_2$ is a pretopos morphism and $- \circ f : \operatorname{Hom}_{\mathbf{Pretop}}(T_2, \mathbf{Set}) \to \operatorname{Hom}_{\mathbf{Pretop}}(T_1,\mathbf{Set})$ is an equivalence, then $f$ was also. Pretopos morphisms are just [[interpretation|interpretations]] of theories; a pretopos morphism into [[Set]] is an interpretion of the source theory into the [[internal logic]] of [[Set]], and is therefore a [[model]].

Since pretoposes are just [[exact completion|effectivizations]] of [[syntactic categories]] of [[first-order theories]], this means: if a functor between the categories of models of $T_1$ and $T_2$ is an equivalence and is induced by an interpretation $T_1 \to T_2$, then that interpretation must be part of a bi-interpretation, i.e. $T_1$ and $T_2$ are equivalent as syntactic categories via pretopos morphisms.

[[Makkai duality]] states that $\operatorname{Hom}_{\mathbf{Pretop}}(-,X)$ factors through the $2$-category of [[ultracategories]] (categories equipped with [[ultraproduct functors]]) (which also contains $\mathbf{Set}$) and that $\operatorname{Hom}_{\mathbf{Pretop}}(-,\mathbf{Set})$ is left-adjoint to $\mathbf{Hom}_{\mathbf{Ult}}(-,\mathbf{Set})$.

Furthermore, the unit of this adjunction is an equivalence, so that a pretopos $T$ is equivalent to the category of ultrafunctors (ultraproduct-preserving functors) from $\mathbf{Mod}(T)$ to $\mathbf{Set}$, i.e. any ultrafunctor $\mathbf{Mod}(T) \to \mathbf{Set}$ is induced by taking points in models of some definable set $X \in T$.

This means: when viewed as a functor to the $2$-category of ultracategories instead, $\operatorname{Hom}_{\mathbf{Pretop}}(-,\mathbf{Set})$ creates equivalences also, so that the pretopos/theory $T$ can be reconstructed up to bi-interpretability from its ultracategory of models. This is what is known as _strong conceptual completeness_.

##Remarks
In his AMS monograph on duality and definability in first-order logic, Makkai refined the above reconstruction result to work with just the (ultra) [[core]] of the ultracategory of models of $T$. Awodey and his students replace the ultracategory structure on this groupoid with a related topology instead; this is the "spectral groupoid" which forms the basis of the [[logical scheme]] approach.

## Examples
(Maybe I'll add some explicit computations later.)

## Related concepts

- [[ultraproduct]]
- [[Makkai duality]]
- [[Stone duality]]

##References

* [[Michael Makkai]] and [[Gonzalo Reyes]], _First order categorical logic: Model-theoretical methods in the theory of topoi and related categories_, Springer-Verlag, 1977.

* [[Michael Makkai]], _Strong Conceptual Completeness for First-Order Logic_ , APAL **40** (1988) pp.167-215.  (freely available online)

* [[Peter Johnstone]], _[[Sketches of an Elephant]] vol. II_ , Oxford UP 2002. (sec. D3.5, pp.931-939)

* {#Lurie} [[Jacob Lurie]], _Ultracategories_, ([pdf](http://www.math.harvard.edu/~lurie/papers/Conceptual.pdf))


An approach which reframes conceptual completeness in terms of [[logical schemes]] is adopted in section 4.4 of

* [[Spencer Breiner]], _Scheme representation for first-order logic_, ([arXiv:1402.2600](http://arxiv.org/abs/1402.2600))

For the $(\infty, 1)$-analog of conceptual completeness, see section A.9 of 

* [[Jacob Lurie]], [[Spectral Algebraic Geometry]]

[[!redirects strong conceptual completeness]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


\tableofcontents


## Idea 

In [[type theory]], a type may be classified by its "polarity", either [[positive type|positive]] or [[negative type|negative]], according to whether its _[[term constructors]]_ or its _[[term eliminators]]_ are regarded as primary, respectively. The idea is due to [[Jean-Marc Andreoli]] and [[Jean-Yves Girard]].

[[positive type|Positive types]] are [[inductive type|inductively]] defined by their [[term introduction]] rules and correspond, under [[categorical semantics]], to [[objects]] defined as covariant [[representable functors]] ($C \to Set$) such as [[colimits]] and [[left adjoints]]. 
On the other hand, [[negative types]] are [[coinductive type|coinductively]] defined by their [[term elimination]] rules and correspond under [[categorical semantics]] to [[objects]] defined as [[contravariant functor|contravariant]] [[representable functors]] ($C^{op} \to Set$) such as [[limits]] and [[right adjoints]].

Note that polarity is not so much a property of the [[types]] themselves, but rather of their presentation by introduction and elimination rules: It may happen that a positive and a negative type are [[equivalence in type theory|equivalent]] (this is the case, for example, for the [[product type]] in [[simply typed lambda calculus]]). 
In terms of [[categorical semantics]] this is simply the fact that a single [[object]] may exhibit multiple [[universal properties]].

Generally, in [[computational effect|effectful]] languages, the [[positive type|positive types]] are better behaved in [[call-by-value]] evaluation strategies and [[negative type|negative types]] are better behaved in [[call-by-name]] and other [[lazy evaluation]] strategies.
A [[category theory|category-theoretic]] explanation of this fact is that [[call-by-value]] languages can be modeled by the [[Kleisli category]] of a [[monad]] $T$ on a category $C$. Usually, the category $C$ will have both [[limits]] (negatives) and [[colimits]] (positives), however the canonical functor $F \colon C \to C_T$ is a [[left adjoint]] so it only generally preserves the colimits (positives). Dually, call-by-name languages can be modeled by the Kleisli category of a [[comonad]] $W$ and the canonical functor $U \colon C \to C_W$ is a [[right adjoint]], and [[right adjoints preserve limits|so]] [[preserved limit|preserves]] [[limits]] (negatives).

## Related concepts

* [[positive type]]

* [[negative type]]

* [[focusing]]

## References

* [[Noam Zeilberger]], _The Logical Basis of Evaluation Order and Pattern-Matching_, ([pdf](http://noamz.org/thesis.pdf))

* [[Robert Harper]], _Polarity in Type Theory_, ([blog post](https://existentialtype.wordpress.com/2012/08/25/polarity-in-type-theory/))
##Idea 

In [[type theory]], a type may be classed as having a polarity, either [[positive type|positive]] or [[negative type|negative]], according to whether its _constructors_ or _eliminators_ are regarded as primary. The idea is due to [[Jean-Marc Andreoli]] and [[Jean-Yves Girard]].

Positive types are inductively defined by their introduction rules and correspond to objects defined as covariant [[representable functors]] ($C \to Set$) such as [[colimits]] and [[left adjoints]] whereas negative types are coinductively defined by their elimination rules and correspond to objects defined as contravariant [[representable functors]] ($C^o \to Set$) such as [[limits]] and [[right adjoints]].
Note that polarity is really a property of the presentation of the type by introduction and elimination rules, and it might turn out that a positive and a negative connective are always isomorphic, for instance, the [[product type]] in simply typed lambda calculus. On the category side this is simply the fact that a single object may exhibit multiple universal properties.

Generally, in effectful languages, the [[positive type|positive types]] are better behaved in [[call-by-value]] evaluation strategies and [[negative type|negative types]] are better behaved in [[call-by-name]] and other [[lazy evaluation]] strategies.
A category-theoretic explanation of this fact is that [[call-by-value]] languages can be modeled by the [[Kleisli category]] of a monad $T$ on a category $C$. Usually, the category $C$ will have both limits (negatives) and colimits (positives), however the canonical functor $F : C \to C_T$ is a left adjoint so it only generally preserves the colimits (positives). Dually, call-by-name languages can be modeled by the Kleisli category of a [[comonad]] $W$ and the canonical functor $U : C \to C_W$ is a right adjoint, and so preserves limits (negatives).

### Related concepts

* [[positive type]]
* [[negative type]]
* [[focusing]]

## References

* [[Noam Zeilberger]], _The Logical Basis of Evaluation Order and Pattern-Matching_, ([pdf](http://www.cs.cmu.edu/~rwh/theses/zeilberger.pdf))
* [[Robert Harper]], _Polarity in Type Theory_, ([blog post](https://existentialtype.wordpress.com/2012/08/25/polarity-in-type-theory/))
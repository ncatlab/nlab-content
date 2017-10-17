##Idea 

In [[type theory]], a type may be classed as having a polarity, either [[positive type|positive]] or [[negative type|negative]], according to whether its _constructors_ or _eliminators_ are regarded as primary. The idea is due to [[Jean-Marc Andreoli]] and [[Jean-Yves Girard]].

Positive types are inductively defined by their introduction rules and correspond to [[colimits]] and other "mapping-out" [[universal properties]]; negative types are coinductively defined by their elimination rules and correspond to [[limits]] and other "mapping-in" universal properties.
Some types may be defined as both positive and negative, see, for instance, [[product type]].

Generally, in effectful languages, the [[positive type|positive types]] are better behaved in [[call-by-value]] evaluation strategies and [[negative type|negative types]] are better behaved in [[call-by-name]] and other [[lazy evaluation]] strategies.
A category-theoretic explanation of this fact is that [[call-by-value]] languages can be modeled by the [[Kleisli category]] of a monad $T$ on a category $C$. Usually, the category $C$ will have both limits (negatives) and colimits (positives), however the canonical functor $F : C \to C_T$ is a left adjoint so it only generally preserves the colimits (positives). Dually, call-by-name languages can be modeled by the Kleisli category of a [[comonad]] $W$ and the canonical functor $U : C \to C_W$ is a right adjoint, and so preserves limits (negatives).

### Related concepts

* [[positive type]]
* [[negative type]]
* [[focusing]]

## References

* [[Noam Zeilberger]], [The Logical Basis of
Evaluation Order and Pattern-Matching](http://www.cs.cmu.edu/~rwh/theses/zeilberger.pdf)
* [[Robert Harper]], _Polarity in Type Theory_, ([blog post](https://existentialtype.wordpress.com/2012/08/25/polarity-in-type-theory/))
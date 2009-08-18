## Idea

One can turn [[monads]] into [[adjunctions]] and adjunctions into monads, but one doesn\'t always return where one started.  Every monad comes from an adjunction, but only a _monadic adjunction_ comes from a monad.


## Definition

We give the definitions in [[Cat]] and leave it to future readers and writers to generalise.

Let $(C,D,f,g,\iota,\epsilon)$ be an adjunction in $Cat$; that is, $f: C \to D$ and $g: D \to C$ are [[adjoint functors]] with $f \dashv g$, where $\iota$ and $\epsilon$ are the unit and counit.  Let $T$ be $g \circ f$; $T$ has the structure of a monad on $C$, so consider the [[Eilenberg–Moore category]] $C^T$ of [[module for a monad|modules (algebras)]] for $T$.  Then $G \circ \epsilon$ is a [[functor]] $K: D \to C^T$.

The adjunction $f \dashv g$ is __monadic__ if this functor $K$ is an [[equivalence of categories]].


## References

This definition may be found in Section 3.6 of _[[Stone Spaces]]_, but probably there are some better references that one could site here.
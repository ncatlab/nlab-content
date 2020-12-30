
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

In a [[category]] with [[internal homs]] $[-,-]$, given an [[object]] $S$, the _continuation monad_ is the [[endofunctor]] $X \mapsto [[X, S], S]$.

In [[computer science]] this [[monad (in computer science)]] is used to model [[continuation-passing style]] of programming, and therefore this is called the _continuation monad_. The idea here is that a morphism $f \colon X \to Y$ in the [[Kleisli category]] of the continuation monad, hence a morphism in the original category of the form $X\longrightarrow [[Y,S],S]$ is much like a map from $X$ to $Y$ only that instead of "returning" its output directly it instead feeds it into a given function $Y \to S$ which hence _continues_ the computation.


## Examples

* [[double negation monad]]

* [[dualizing object in a closed category]]

* [[extensive quantity]]

* [[selection monad]]

## Related concepts

* [[continuation-passing style]]

* [[maybe monad]]

* [[state monad]]

## References

The continuation monad is discussed in the generality of [[linear type theory]] as the linear [[double negation monad]] in

* [[Paul-André Melliès]], Nicolas Tabareau, _Linear continuation and duality_, 2008 ([pdf](http://hal.inria.fr/docs/00/33/91/56/PDF/linear-control.pdf))

* [[Paul-André Melliès]], _The parametric continuation monad_, Mathematical Structures in Computer Science, Festschrift in honor of Corrado B&#246;hm for his 90th birthday (2013). ([[MelliesContinuation.pdf:file]])


[[!redirects continuation monads]]
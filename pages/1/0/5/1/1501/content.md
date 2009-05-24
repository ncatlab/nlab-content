A _rigid_ [[monoidal category]] is essentially a [[monoidal category]] where every [[object]] has a dual. Conventions differ as to the precise way in which this is used. 

One convention is as follows: a _right dual_ of an object $V$ in a monoidal category is an object $V^*$ equipped with unit $\eta : 1 \rightarrow V^* \otimes V$ and counit maps $\epsilon: V \otimes V^* \rightarrow 1$ satisfying the snake diagrams. Similarly for left duals.

This convention fits in with the standardized conventions regarding [[adjoint functor]]s. Namely according to this convention, an endofunctor $F : C \rightarrow C$ has a right adjoint $F^* : C \rightarrow C$ if and only if $F^*$ is a right dual of $F$ in the [[monoidal category]] $End(C)$. 

**Definition.** A [[monoidal category]] is _rigid_ if every object has both a right dual and a left dual. 

Note that this definition only asserts the existence of the dual objects. It does _not_ assert that specific duals have been chosen. Nor does it assert that the right dual of an object is isomorphic to its left dual (this need not be the case).



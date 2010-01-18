
> [[Urs Schreiber]]: here is an attempt of mine to write out the very little that I think I learned of this topic from discussion elsewhere. Probably partly wrong.

A **theory** is...

Examples are 

* [[essentially algebraic theory]]

* [[algebraic theory]]

  * [[commutative algebraic theory]]

  * finitary algbraic theory: [[Lawvere theory]]

    * [[Fermat theory]]

* [[geometric theory]]

A **[[model]]** for a theory is...

Typically for a theory $T$ there exists a [[category]] $C_T$ -- the  **syntactic category** $C_T$ -- such that a model for $T$ is a [[functor]] $C_T \to \mathcal{T}$ into some [[topos]] $T$, satisfying certain conditions.

For instance the syntactic categories of [[Lawvere theory|Lawvere theories]] are precisely those categories that have finite cartesian [[product]]s and in which every object is [[isomorphic]] to a finite cartesian power $x^n$ of a distinguished object $x$. A model for a Lawvere theory is precisely a finite product preserving functor $C_T \to \mathcal{T}$.

We say a functor $\mathcal{T}_1 \to \mathcal{T}_2$ of toposes (for instance a [[logical morphism]] or a [[geometric morphism]]) _preserves a theory_ $T$ if for every model $C_T \to \mathcal{T}_1$ of $T$ in $\mathcal{T}_1$, the composite $C_T \to \mathcal{T}_1 \to \mathcal{T}_2$ is a model of $T$ in $\mathcal{T}_2$.

For instance, every [[geometric morphism]] preserves every [[Lawvere theory]] since, being a [[right adjoint]], it preserves [[limit]]s, hence finite products.
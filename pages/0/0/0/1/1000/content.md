A [[monad]] $(T,\mu,i)$ on the category of sets, is an __algebraic monad__ if the underlying endofunctor $T:\mathrm{Set}\to\mathrm{Set}$ commutes with [[filtered category|filtered]] [[colimit]]s. In other words, an algebraic monad is a monoid in the category of algebraic endofunctors on $\mathrm{Set}$.

Algebraic monad $(T,\mu,i)$ is completely determined by its value on all finite ordinals $n\in\mathbb{N}_0$ considered as standard [[finite set]]s.  $T(n)$ is then the set of $n$-ary operations.  The notion of algebraic monad is hence similar to the notion of a nonsymmetric [[operad]] in $\mathrm{Set}$, but it is not equivalent, because of the possibility of duplicating or discarding inputs.

+--{: .query}
[[Mike Shulman|Mike]]: Does anyone besides Durov use this terminology?  In category theory these already have two standard names: "finitary monads" and "(Lawvere) theories."
=--

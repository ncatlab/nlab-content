A **contravariant functor** $F$ from a [[category]] $C$ to a category $D$ is simply a [[functor]] from the [[opposite category]] $C^op$ to $D$.

To emphasize that one means a functor $C \to D$ as stated and _not_ as a functor $C^{op} \to D$ one sometimes says **covariant functor** for non-contravariant, for emphasis. 

Equivalently, a contravariant functor from $C$ to $D$ may be thought of as a functor from $C$ to $D^op$, but the version above generalises better to functors of many variables. 

Also notice that while the objects of the [[functor category]] $[C^{op}, D]$ are in canonical bijection with those in the functor category $[C, D^{op}]$ (both are contravariant functors from $C$ to $D$), the morphisms in the two functor categories are in general different, as

$$
  [C^{op}, D] \simeq [C, D^{op}]^{op}
  \,.
$$

This matters when discussing a [[natural transformation]] from one contravariant functor to another.
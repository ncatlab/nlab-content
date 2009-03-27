A __pre-abelian category__ is an [[additive category]] (in the stricter sense) such that every morphism has a [[kernel]] and a [[cokernel]].  An __abelian category__ is a pre-abelian category in which every morphism decomposes [[generalized the|uniquely up to a unique isomorphism]] into a composition of an [[epimorphism]] followed by [[monomorphism]].

+--{: .query}
[[Mike Shulman|Mike]]: In [[Categories Work]], and on [Wikipedia](http://en.wikipedia.org/wiki/Abelian_category), an abelian category is defined to be (in the terms above) a pre-abelian category such that every monic is a kernel and every epi is a cokernel.  This implies that (epi, mono) is an [[orthogonal factorization system]], but I don't see why the converse should hold, as this seems to assert.
=--

Equivalently, an abelian category is a category enriched over the category [[Ab]] of abelian groups, with a [[zero object|null object]], binary [[biproduct]]s, kernels, cokernels and such that
$$
coker (ker f) = ker (coker f),
$$
where the inner kernel (or cokernel) is understood as the universal arrow and the outer as its vertex object, and the equality is given by the canonical isomorphism from the cokernel object of the kernel arrow to the kernel object of the cokernel arrow.

If an abstract category $C$ has null object, binary products and binary coproducts, kernels, cokernels and the property that every monic is a kernel arrow and every epi is a cokernel arrow (so that all monos and epis are [[normal monomorphism|normal]]), then it can be equipped with a unique addition on the morphism sets such that the composition is biadditive bifunctor and $C$ is abelian with respect to this structure.

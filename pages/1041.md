A __pre-abelian category__ is an [[additive category]] (in the stricter sense) such that every morphism has a [[kernel]] and a [[cokernel]].  An __abelian category__ is a pre-abelian category in which every morphism decomposes [[generalized the|uniquely up to a unique isomorphism]] into a composition of an [[epimorphism]] followed by [[monomorphism]]. Equivalently, it is a pre-abelian category which is [[balanced category|balanced]] (every monic epi is iso). Equivalently it is a pre-abelian category such that every monic is a kernel and every epi is a cokernel.

+--{: .query}
[[Mike Shulman|Mike]]: In [[Categories Work]], and on [Wikipedia](http://en.wikipedia.org/wiki/Abelian_category), an abelian category is defined to be (in the terms above) a pre-abelian category such that every monic is a kernel and every epi is a cokernel.  This implies that (epi, mono) is an [[orthogonal factorization system]], but I don't see why the converse should hold, as this seems to assert.

[[Zoran Skoda]] It is very late night here in Bonn, so check on my reasoning, but I think that the answer is 
simple. Let $f: A\to B$. The canonical map $\coker(\ker f)\to \ker (\coker f)$ exists as long as we have additive category admitting kernels and cokernels. The arrow from A to coker (ker f) is epi as every cokernel arrow, and the arrow of $\ker(\coker f) \to B$ is mono. Now canonical arrow in between the two is automatically both mono and epi. For all that reasoning I did not yet assume the axiom on uniquely unique factorization. Now assume it and you get
that the canonical map must be isomorphism because it is the unique iso between the two decompositions of $f$: one in which you take epi followed by (the composition of) two monics and another in which you have (the composition of) two epis followed by one monic. Right ?

Now do this for $f$ a monic and you get a decomposition into iso iso kernel and for $f$ an epi and you get 
the cokernel iso iso as required.

[[Mike Shulman|Mike]]: Why is the canonical comparison map mono and epi?  It's late for me too right now, but I think that maybe a counterexample is the "multiplication by 2" map $\mathbb{Z}\to \mathbb{Z}$ in the  category of torsion-free abelian groups.

However, if you assume explicitly that that comparison map is always an isomorphism, then I believe it for the reasons that you gave.

[[Zoran Skoda]] I do not see this as a counterexample, as this is not a pre-abelian category, you do not have cokernels in this category ? In a pre-abelian category always the canonical map from coker ker to ker coker has its own kernel 0 and cokernel 0.

[[Mike Shulman|Mike]]: Torsion-free abelian groups are reflective in abelian groups, and therefore cocomplete.  In particular, they have cokernels, although those cokernels are not computed as in [[Ab]].  In particular, the cokernel of $2:\mathbb{Z}\to\mathbb{Z}$ is 0.
=--

Equivalently, an abelian category is a category enriched over the category [[Ab]] of abelian groups, with a [[zero object|null object]], binary [[biproduct]]s, kernels, cokernels and such that
$$
coker (ker f) = ker (coker f),
$$
where the inner kernel (or cokernel) is understood as the universal arrow and the outer as its vertex object, and the equality is given by the canonical isomorphism from the cokernel object of the kernel arrow to the kernel object of the cokernel arrow.

If an abstract category $C$ has null object, binary products and binary coproducts, kernels, cokernels and the property that every monic is a kernel arrow and every epi is a cokernel arrow (so that all monos and epis are [[normal monomorphism|normal]]), then it can be equipped with a unique addition on the morphism sets such that the composition is biadditive bifunctor and $C$ is abelian with respect to this structure.

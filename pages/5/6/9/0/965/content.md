
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

## Definition

A **suplattice** is a [[partial order|poset]] which has all [[joins]] (and in particular is a join-[[semilattice]]).  By the [[adjoint functor theorem]] for posets, a suplattice necessarily has all [[meet|meets]] as well and so is a [[complete lattice]].  However, a **suplattice homomorphism** preserves joins, but not necessarily meets.  Furthermore, a *[[proper class|large]]* semilattice which has all *small* joins need not have all meets, but might still be considered a large suplattice (even though it may not even be a lattice).

Dually, an __inflattice__ is a poset which has all [[meets]], and an __inflattice homomorphism__ in a monotone function that preserves all meets.

A __[[frame]]__ (dual to a [[locale]]) is a suplattice in which finitary meets distribute over arbitrary joins.  (Frame homomorphisms preserve all joins and finitary meets.)

The [[category]] [[SupLat]] of suplattices and suplattice homomorphisms admits a [[tensor product]] which represents "bilinear maps," i.e. functions which preserve joins separately in each variable.  Under this tensor product, the category of suplattices is a [[star-autonomous category]] in which the dualizing object is the suplattice dual to the object $TV$ of [[truth-values]].  A [[semigroup object|semigroup]] in this [[monoidal category]] is a __[[quantale]]__, including [[frames]] as a special case when the quantale is idempotent and unital. Modules over them are [[modules over quantales]] (quantic modules with special case of localic modules, used in the localic analogue of the Grothendieck's descent theory in Joyal and Tierney). 

* [[André Joyal]], M. Tierney, _An extension of the Galois theory of Grothendieck_, Mem. Amer. Math. Soc. 51 (1984), no. 309, vii+71 pp.

## The free suplattice on a poset

There is a forgetful functor 

$$
U \colon SupLat \to Poset 
$$

This has a left adjoint

$$
F \colon Poset \to SupLat
$$

where for any poset $P$, the suplattice $F(P)$ is the poset of downsets of $P$, ordered by inclusion.   Here a **downset** of a poset $P$ is a subset $S \subseteq P$ such that 

$$ s \in S, s' \le s \quad  \implies \quad s' \in S. $$

This set of all downsets in $P$, say $\hat{P}$, is ordered by inclusion, and it's a suplattice: any union of downsets is a downset.  There's an embedding of $P$ in  $\hat{P}$ that sends each $p \in P$ to its **principal** downset $\{s \in P : \; s \le p \}$.   (To give a downset is to give an [[antichain]], and so the free suplattice is sometimes described equivalently in terms of antichains.)

To understand this description of the free suplattice on a poset, some [[enriched category theory]] is useful.  [[preorder|Preorders]] are the same as $Bool$-enriched categories, where $Bool$ is the monoidal category with two objects $F$, $T$ and one nontrivial morphism $F \implies T$, its monoidal structure being "and".   Using this idea, the downsets of a poset $P$ correspond in a one-to-one way with $Bool$-enriched functors $f \colon P^{op} \to Bool$, just as presheaves on a category $C$ are functors $f \colon C^{op} \to Set$.   The embedding $y \colon P \to \hat{P}$ that sends each $p \in P$ to its principal downset is the $Bool$-enriched version of the Yoneda embedding.   So, just as the category of presheaves on a category $C$ is the [[free cocompletion|free cocomplete category]] on $C$, $\hat{P}$ is the free cocomplete $Bool$-enriched category on $P$.   But a cocomplete $Bool$-enriched category that happens to be a poset is just the same as a suplattice. 

## The category of suplattices 

The category of suplattices is monadic over the category of posets, and each algebra structure $\xi: \hat{P} \to P$ is left adjoint to the Yoneda embedding $y: P \to \hat{P}$. This makes suplattices the same thing (up to equivalence) as [[total categories]] in the $Bool$-[[enriched category theory|enriched]] sense. Notice that algebra structure maps, being left adjoints, are cocontinuous and therefore suplattice morphisms. This makes the monad a [[commutative monad]], and therefore according to general theory, $SupLat$ is a [[symmetric monoidal closed category]] where the internal hom $Hom(P, Q)$ between two suplattices is the suplattice of cocontinuous maps $P \to Q$, which are the same as left adjoints $P \to Q$ according to the poset version of the [[adjoint functor theorem]]. 

$SupLat$ is also monadic over $Set$, where the monad $P: Set \to Set$ is the covariant [[power set]] functor. It therefore is a complete and cocomplete [[Barr-exact category]]. The [[Kleisli category]] of this monad is equivalent to [[Rel]], the category of sets and relations. Thus the objects of $Rel$ may be thought of as the free suplattices.

As stated above, the symmetric monoidal closed category $SupLat$ is a [[star-autonomous category]] where the star-[[involution]] takes a suplattice $P$ to the [[opposite category|opposite]] poset $P^{op}$. In part this says that a suplattice is also an [[inflattice]], a fact which holds internally in any [[topos]] (where we use an internal covariant power-object functor to form an appropriate monad). Thus the tensor product $P \otimes Q$ may be formed as the suplattice $Hom(P, Q^{op})^{op}$. The presence of the equivalence 

$$\ast = (-)^{op}: SupLat^{op} \to SupLat$$ 

(which takes a morphism $f: P \to Q$ to $g^{op}: Q^{op} \to P^{op}$, where $g$ is right adjoint to $f$) also means that colimits may be formed as appropriate limits, which are in turn formed pointwise by monadicity over $Set$. 


[[!redirects suplattice]]
[[!redirects sup lattice]]
[[!redirects sup-lattice]]
[[!redirects suplattices]]
[[!redirects sup lattices]]
[[!redirects sup-lattices]]

[[!redirects inflattice]]
[[!redirects inf lattice]]
[[!redirects inf-lattice]]
[[!redirects inflattices]]
[[!redirects inf lattices]]
[[!redirects inf-lattices]]

[[!redirects complete semilattice]]
[[!redirects complete semilattices]]
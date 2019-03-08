

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A **meet-semilattice** is a [[poset]] which admits all [[finite set|finite]] [[meet|meets]], or equivalently which admits a top element $\top$ and binary meets $a\wedge b$.  If we think of a poset as a category, a meet-semilattice is the same as a poset with finite limits, or equivalently, a poset with finite products.

In a meet-semilattice the binary meet $\wedge$ is commutative, associative, has $\top$ as a unit, and is *idempotent*: $a\wedge a =a$.  And in fact, given any commutative and idempotent [[monoid]] $(A,\wedge,\top)$, we can define $a\le b$ to mean $a \wedge b = a$ to make it into a poset with finite meets; thus we have an equivalent algebraic definition of a meet-semilattice.

Dually, a **join-semilattice** is a poset which admits all finite joins, including a bottom element $\bot$ and binary joins $\vee$.  Once again $\vee$ is commutative, associative, unital for $\bot$, and idempotent, and we can recover the order from it.  If we think of a poset as a category, a join-semilattice is the same as a poset with finite colimits, or equivalently, a poset with finite coproducts.

Note that the algebraic definition of both types of semilattice is the same: a commutative idempotent monoid.  The difference comes in how we define the order, or if we work purely algebraically, in the notation we use (just as we distinguish additive and multiplicative groups notationally).  It would also be possible to take one as standard and call the other a _cosemilattice_ (compare [[direction|directed]] and [[codirection|codirected]] sets), but this may not have ever been done.

If a poset is both a meet- *and* a join-semilattice, then we call it a [[lattice]].


## Bounded semilattices and semipseudolattices
 {#BoundedAndPseudo}

Traditionally, a semilattice need have only finite [[inhabited set|inhabited]] meets/joins; that is, it need not have a top/bottom element.  Algebraically, this means that a semilattice need not be a monoid, but is any commutative idempotent [[semigroup]].

One might call a semilattice that does have a top/bottom element a __bounded semilattice__; the problem with this is that a [[bounded poset]] already means a poset that has both top *and* bottom elements, whereas here we really only want to require one.

Another approach is to define a semilattice, as above, to require a top/bottom element and then use the term __pseudosemilattice__ or __semipseudolattice__ to allow for the possibility that it might not.

See [[lattice]] for more discussion of this issue.


## Semilattice homomorphisms

A homomorphism of join-semilattices $f: A \to B$ is a function that preserves finite joins, or equivalently:
$$ f(x \vee y) = f(x) \vee f(y),\; f(\bot) = \bot .$$
Note that such a homomorphism is necessarily a [[monotone function]], but the converse fails.  Thus, a semilattice is a poset with [[property-like structure]].

A homomorphism of meet-semilattices is defined in a similar (i.e., dual) way.

Semilattices and semilattice homomorphims form a [[concrete category]] [[SemiLat]].

## The free join-semilattice on a poset

There is a category $JSemiLatt$ with join-semilattices as objects and homomorphisms of these as morphisms, and a forgetful functor to the category of posets:

$$
U \colon JSemiLatt \to Poset 
$$

This has a left adjoint

$$
F \colon Poset \to JSemiLatt
$$

where for any poset $P$, the join-semilattice $F(P)$ is the poset of finitely generated downsets of $P$, ordered by inclusion.   Here a **downset** of a poset $P$ is a subset $S \subseteq P$ such that 

$$ s \in S, s' \le s \quad  \implies \quad s' \in S. $$

This set of all downsets in $P$, say $\hat{P}$, is ordered by inclusion, and it's a complete join-semilattice: any union of downsets is a downset.  There's an embedding of $P$ in  $\hat{P}$ that sends each $p \in P$ to its **principal** downset $\{s \in P : \; s \le p \}$.  A downset is **finitely generated** if it is the union of finitely many principal downsets. To give a finitely generated downset is to give a finite [[antichain]], and so the free join-semilattice is sometimes described equivalently in terms of finite antichains. 

To understand this description of the free join-semilattice on a poset, some [[enriched category theory]] is useful.  We can think of posets, or more generally preorders, as $Bool$-enriched categories, where $Bool$ is the monoidal category with two objects $F$, $T$ and one nontrivial morphism $F \implies T$, its monoidal structure being "and".   The downsets of a poset $P$ correspond in a one-to-one way with order-preserving maps $f \colon P^{op} \to Bool$, just as presheaves on a category $C$ are functors $f \colon C^{op} \to Set$.   The embedding $y \colon P \to \hat{P}$ that sends each $p \in P$ to its principal downset is the $Bool$-enriched version of the Yoneda embedding.   So, just as the category of presheaves on a category $C$ is the [free cocomplete category](https://ncatlab.org/nlab/show/free+cocompletion) on $C$, $\hat{P}$ is the free cocomplete $Bool$-enriched category with on $P$.   But a cocomplete $Bool$-enriched category is just the same as a complete join-semilattice.  

Similarly, the free join-semilattice on a poset is a $Bool$-enriched analogue of the free _finitely_ cocomplete category on a category $C$: objects in this category are presheaves that are finite colimits of representables.

## Examples

* [[semilattice of commutative subalgebras]]


[[!redirects meet-semilattice]]
[[!redirects join-semilattice]]
[[!redirects meet semilattice]]
[[!redirects join semilattice]]
[[!redirects cosemilattice]]
[[!redirects bounded semilattice]]
[[!redirects pseudosemilattice]]
[[!redirects semipseudolattice]]
[[!redirects semilattices]]
[[!redirects meet-semilattices]]
[[!redirects join-semilattices]]
[[!redirects meet semilattices]]
[[!redirects join semilattices]]
[[!redirects cosemilattices]]
[[!redirects bounded semilattices]]
[[!redirects pseudosemilattices]]
[[!redirects semipseudolattices]]
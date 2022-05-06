

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

### General

A **join-semilattice** is a [[poset]] which admits all [[finite set|finite]] [[join|joins]], or equivalently which admits a bottom element $\bot$ and binary joins $a\vee b$.  If we think of a poset as a category, a join-semilattice is the same as a poset with finite colimits, or equivalently, a poset with finite coproducts.

In a join-semilattice the binary join $\vee$ is commutative, associative, has $\bot$ as a unit, and is **idempotent**:  $a\vee a =a$.  And in fact, given any commutative and idempotent [[monoid]] $(A,\vee,\bot)$, we can define $a\le b$ to mean $a \vee b = b$ to make it into a poset with finite joins; thus we have an equivalent algebraic definition of a join-semilattice.   

Dually, a **meet-semilattice** is a poset which admits all finite [[meet|meets]], including a top element $\top$ and binary meets $\wedge$.  Once again $\wedge$ is commutative, associative, unital for $\top$, and idempotent.  Once again we can recover the order from it, but this time defining $a\le b$ to mean $a \wedge b = a$.  If we think of a poset as a category, a meet-semilattice is the same as a poset with finite limits, or equivalently, a poset with finite products.

If we treat join- and meet-semilattices purely algebraically there is no difference: they are both just idempotent commutative monoids.   The difference comes in how we define the order starting the commutative monoid structure, or in the notation we use (just as we distinguish additive and multiplicative groups notationally).   

Since the opposite of a join-semilattice is a meet-semilattice, it would be possible to take one as standard and call the other a _cosemilattice_ (compare [[direction|directed]] and [[codirection|codirected]] sets), but this may not have ever been done.

If a poset is both a join- *and* a meet-semilattice, then we call it a [[lattice]].


### Bounded semilattices and semipseudolattices
 {#BoundedAndPseudo}

Traditionally, a semilattice need have only finite [[inhabited set|inhabited]] meets/joins; that is, it need not have a top/bottom element.  Algebraically, this means that a semilattice need not be a monoid, but is any commutative idempotent [[semigroup]].

One might call a semilattice that does have a top/bottom element a __bounded semilattice__; the problem with this is that a [[bounded poset]] already means a poset that has both top *and* bottom elements, whereas here we really only want to require one.

Another approach is to define a semilattice, as above, to require a top/bottom element and then use the term __pseudosemilattice__ or __semipseudolattice__ to allow for the possibility that it might not.

See [[lattice]] for more discussion of this issue.

### Semilattice homomorphisms

A homomorphism of join-semilattices $f: A \to B$ is a function that preserves finite joins, or equivalently:
$$ f(x \vee y) = f(x) \vee f(y),\; f(\bot) = \bot .$$
Note that such a homomorphism is necessarily a [[monotone function]], but the converse fails.  Thus, a semilattice is a poset with [[property-like structure]].

A homomorphism of meet-semilattices is defined in an analogous (i.e., dual) way.  In what follows we take join-semilattices as the default, but all results apply to meet-semilattices with slight modifications.

### The category of semilattices 

Semilattices and semilattice homomorphims form a [[concrete category]] [[SemiLat]].  By the remarks above, this is equivalent to the category of commutative idempotent monoids.  Since these are algebras of a [[Lawvere theory]], or equivalently a [[finitary monad]] on $Set$, the category $Semi Lat$ has all the properties that [[algebraic category|finitary monadic categories]] enjoy.

The poset $\{F,T\}$ where $F \le T$ becomes a commutative [[rig]] with $\vee$ and meet $\wedge$ as addition and multiplication, respectively; let us call this rig $Bool$.    We can define a module of a rig much as we define a module of a ring, but with the module's underlying abelian group generalized to be a commutative monoid (thus eliminating the need for negatives).   The underlying commutative monoid of a $Bool$-module is idempotent because, writing addition in this monoid as $+$, we have $a + a = (T \vee T)a = T a = a$.  Conversely, any idempotent commutative monoid becomes a $Bool$-module in a unique way.  Thus, the category $Semi Lat$ is equivalent to the category of $Bool$-modules.

## Properties

### The free join-semilattice on a poset

There is a [[forgetful functor]]
$$
U \colon SemiLat \to Poset 
$$

This has a [[left adjoint]]

$$
F \colon Poset \to SemiLat
$$

where for any poset $P$, the join-semilattice $F(P)$ is the poset of finitely generated downsets of $P$, ordered by inclusion.   Here a **downset** of a poset $P$ is a subset $S \subseteq P$ such that 

$$ s \in S, s' \le s \quad  \implies \quad s' \in S. $$

This set of all downsets in $P$, say $\hat{P}$, is ordered by inclusion, and it's a [[suplattice]]: any union of downsets is a downset.  There's an embedding of $P$ in  $\hat{P}$ that sends each $p \in P$ to its **principal** downset $\{s \in P : \; s \le p \}$.  A downset is **finitely generated** if it is the union of finitely many principal downsets.  (To give a finitely generated downset is to give a finite [[antichain]], and so the free join-semilattice is sometimes described equivalently as the set of finite antichains in $P$ equipped with a certain partial order.)

To understand this description of the free join-semilattice on a poset, some [[enriched category theory]] is useful.  A [[preorder]] is the same as  a $Bool$-enriched category, where now $Bool$ stands for the monoidal category with two objects $F$, $T$ and one nontrivial morphism $F \implies T$, its monoidal structure being "and".   The downsets of a poset $P$ correspond in a one-to-one way with order-preserving maps $f \colon P^{op} \to Bool$, but in terms of enriched category theory these are precisely the $Bool$-enriched functors $f \colon P^{op} \to Bool$, just as presheaves on a category $C$ are functors $f \colon C^{op} \to Set$.   Thus, the embedding $y \colon P \to \hat{P}$ that sends each $p \in P$ to its principal downset is the $Bool$-enriched version of the Yoneda embedding.   So, just as the category of presheaves on a category $C$ is the [[free cocompletion|free cocomplete category]] on $C$, $\hat{P}$ is the free cocomplete $Bool$-enriched category on $P$.   But a cocomplete $Bool$-enriched category that happens to be a poset (instead of a mere preorder) is the same as a suplattice.  Thus, the free suplattice on $P$ is $\hat{P}$.

Similarly, the free join-semilattice on a poset $P$ is the $Bool$-enriched analogue of the free _finitely_ cocomplete category on a category $C$, since objects in this category are presheaves that are finite colimits of representables.

## Examples

* [[semilattice of commutative subalgebras]]

* [[suplattice]]

## Related concepts

* [[band]]


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
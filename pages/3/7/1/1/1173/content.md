
> The article is about bounded [[semilattices]] in the sense of [[join-semilattices]] having a [[bottom element]] or [[meet-semilattices]] having a [[top element]]. For "bounded semilattices" which have both a [[top element]] and a [[bottom element]] and thus are a [[bounded poset]], see *[[01-bounded semilattice]]*. 

----

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


\tableofcontents


## Definition

### General

A **join-semilattice** is a [[poset]] which admits all [[finite set|finite]] [[join|joins]], or equivalently which admits a bottom element $\bot$ and binary joins $a\vee b$.  If we think of a poset as a category, a join-semilattice is the same as a poset with finite colimits, or equivalently, a poset with finite coproducts.

In a join-semilattice the binary join $\vee$ is commutative, associative, has $\bot$ as a unit, and is **idempotent**:  $a\vee a =a$.  And in fact, given any commutative and idempotent [[monoid]] $(A,\vee,\bot)$, we can define $a\le b$ to mean $a \vee b = b$ to make it into a poset with finite joins; thus we have an equivalent algebraic definition of a join-semilattice.   

Dually, a **meet-semilattice** is a poset which admits all finite [[meet|meets]], including a top element $\top$ and binary meets $\wedge$.  Once again $\wedge$ is commutative, associative, unital for $\top$, and idempotent.  Once again we can recover the order from it, but this time defining $a\le b$ to mean $a \wedge b = a$.  If we think of a poset as a category, a meet-semilattice is the same as a poset with finite limits, or equivalently, a poset with finite products.

If we treat join- and meet-semilattices purely algebraically there is no difference: they are both just idempotent commutative monoids.   The difference comes in how we define the order starting the commutative monoid structure, or in the notation we use (just as we distinguish additive and multiplicative groups notationally).   

Since the opposite of a join-semilattice is a meet-semilattice, it would be possible to take one as standard and call the other a _cosemilattice_ (compare [[direction|directed]] and [[codirection|codirected]] sets), but this may not have ever been done.

If a poset is both a join- *and* a meet-semilattice, then we call it a [[lattice]].

### Bounded and unbounded semilattices

There is also the question of whether semilattices are bounded or not, in the sense of a [[bounded lattice]]. With the algebraic definition of a semilattice, one could either assume that semilattices have [[neutral elements]] $1$ or [[absorbing elements]] $0$ or both or neither. In the order-theoretic definition, one can assume that semilattices have [[top elements]] or [[bottom elements]] or both or neither. This yields four different kinds of semilattices: 

* those semilattices without either neutral elements or absorbing elements are **unbounded semilattices** or **pseudosemilattices**.  

* those semilattices with only neutral elements are **bounded semilattices**  

* those semilattices with only absorbing elements do not seem to have a name in the literature, but are still bounded from the opposite direction. 

* those semilattices with both neutral and absorbing elements are **[[01-bounded semilattices]]**

In a join-semilattice, the [[top element]], if it exists, is a [[neutral element]] and the [[bottom element]], if it exists, is an [[absorbing element]] for the [[join]] operation. Likewise, in a meet-semilattice, the [[bottom element]], if it exists, is a [[neutral element]] and the [[top element]], if it exists, is an [[absorbing element]] for the [[meet]] operation. 

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

* [[01-bounded semilattice]]

## In dependent type theory

In [[dependent type theory]], one can consider a type with a binary operation satisfying the equational axioms of a [[semilattice]] without postulating that the algebraic structure is an [[h-set]], hence a higher semilattice in the sense of [[higher algebra]]. 

However, [Wärn 2026](#Wärn26), [Escardo 2026](#Escardo26), and [de Jong 2026](#deJong26) have all shown that any type $T$ with a binary operation $\lambda x, y:T.x \cdot y$ on $T$ that is 

1. associative in the sense that the type $\prod_{x, y, z:T} (x \cdot y) \cdot z = x \cdot (y \cdot z)$ has an element

1. commutative in the sense that the type $\prod_{x, y:T} x \cdot y = y \cdot x$ has an element

1. idempotent in the sense that the type $\prod_{x:T} x \cdot x = x$ has an element

is automatically an [[h-set]] and thus an algebraic [[semilattice]]. Hence, every higher semilattice is a semilattice in the set-theoretic sense. 

This implies that, unlike most mathematical structures, neither the algebraic definition of a semilattice nor the order-theoretic definitions of a join-semilattice or a meet-semilattice requires explicit [[set-truncation]] in the definition of a semilattice in dependent type theory; instead, the fact that semilattices are sets can be proven from the definitions themselves. This also means that many other algebraic structures, such as 

* [[lattices]], [[total orders]]

* [[distributive lattices]]

* [[inflattices]], [[suplattices]]

* [[sigma-complete lattices|$\sigma$-complete lattices]], [[complete lattices]]

* [[sigma-frames|$\sigma$-frames]], [[frames]]

* [[Boolean algebras]], [[Heyting algebras]]

* [[additively idempotent semirings]]

* [[commutative semiring|commutative]] and [[multiplicatively idempotent semirings]], 

* [[Boolean rings]]

* [[lattice ordered abelian groups]], [[totally ordered abelian groups]]

* [[lattice ordered rings]], [[totally ordered rings]]

can also be defined without explicit [[set-truncation]] in [[dependent type theory]], as they all carry in one way or another an associative, commutative, and idempotent binary operation. 

## Related concepts

* [[band]], [[idempotent monoid]]

* [[enriched poset]]

* [[presemilattice]]

* [[semilattice object]]

* [[join-semilattice object]]

* [[meet-semilattice object]]

## References

See also:

* Wikipedia: *[Semilattice](https://en.wikipedia.org/wiki/Semilattice)*

On higher semilattices automatically being sets:

* {#Wärn26} [[David Wärn]]. *Idem*, [[Agda]] code, 17 February 2026 &lbrack;[web](https://dwarn.se/agda/Idem.html)&rbrack;

* {#Escardo26} [[Martin Escardo]], *AlgebraicStructuresForcingSethood.Semilattices*, [[Agda]] code, 23 February 2026 &lbrack;[web](https://martinescardo.github.io/TypeTopology/AlgebraicStructuresForcingSethood.Semilattices.html)&rbrack;

* {#deJong26} [[Tom de Jong]], *AlgebraicStructuresForcingSethood.Semilattices-streamlined*, [[Agda]] code, 27 February 2026 &lbrack;[web](https://martinescardo.github.io/TypeTopology/AlgebraicStructuresForcingSethood.Semilattices-streamlined.html)&rbrack;

[[!redirects meet-semilattice]]
[[!redirects join-semilattice]]
[[!redirects meet semilattice]]
[[!redirects join semilattice]]
[[!redirects cosemilattice]]
[[!redirects pseudosemilattice]]
[[!redirects semipseudolattice]]
[[!redirects semilattices]]
[[!redirects meet-semilattices]]
[[!redirects join-semilattices]]
[[!redirects meet semilattices]]
[[!redirects join semilattices]]
[[!redirects cosemilattices]]
[[!redirects pseudosemilattices]]
[[!redirects semipseudolattices]]

[[!redirects bounded semilattice]]
[[!redirects bounded semilattices]]

[[!redirects bounded meet-semilattice]]
[[!redirects bounded meet-semilattices]]

[[!redirects bounded join-semilattice]]
[[!redirects bounded join-semilattices]]

[[!redirects unbounded semilattice]]
[[!redirects unbounded semilattices]]

[[!redirects unbounded meet-semilattice]]
[[!redirects unbounded meet-semilattices]]

[[!redirects unbounded join-semilattice]]
[[!redirects unbounded join-semilattices]]

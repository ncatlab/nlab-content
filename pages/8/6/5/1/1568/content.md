
# Contents
* table of contents
{: toc}

## Definitions

Ideals show up both in [[ring]] theory and in [[lattice]] theory.  We recall both of these below and look at some slight generalizations.


### In rings (and other rigs)

A __left ideal__ in a [[ring]] (or even [[rig]]) $R$ is a [[subset]] $I$ of (the underlying set of) $R$ such that:

*  $0 \in I$;
*  $x + y \in I$ whenever $x, y \in I$;
*  $x y \in I$ whenever $y \in I$, regardless of whether $x \in I$.

A __right ideal__ in $R$ is a subset $I$ such that:

*  $0 \in I$;
*  $x + y \in I$ whenever $x, y \in I$;
*  $x y \in I$ whenever $x \in I$.

A __two-sided ideal__ in $R$ is a subset $I$ that is both a left and right ideal; that is:

*  $0 \in I$;
*  $x + y \in I$ whenever $x \in I$ and $y \in I$;
*  $x y \in I$ whenever $x \in I$ or $y \in I$.

This generalises to:

*  $x_1 + \cdots + x_n \in I$ whenever $x_k \in I$ for every $k$;
*  $x_1 \cdots x_n \in I$ whenever $x_k \in I$ for some $k$.

Notice that all three kinds of ideal are equivalent for a commutative ring.

+-- {: .num_remark} 
###### Remarks 
* A left ideal in a ring $R$ may be equivalently defined as an $R$-submodule of $R$, viewing the latter as a left $R$-[[module]]. 
* A right ideal in a ring $R$ may be equivalently defined as an $R$-submodule of $R$, viewing the latter as a right $R$-[[module]]. 
* A two-sided ideal in a ring $R$ may be equivalently defined as a sub-bimodule of $R$, viewing the latter as an $R$-[[bimodule]]. 
* The collection of all two-sided ideals in a ring $R$ form a [[concrete category]], see [[category of two-sided ideals in a ring]]
* The preceding remarks apply to rigs as well. 
* Considering the category of rings as a Barr-exact category, there is a natural bijection between [[congruence|congruence relations]] on a ring $R$ (internal to the category of rings) and two-sided ideals of $R$; this associates to each ideal $I$ the relation $\sim_I$ where $x \sim_I y$ means $x - y \in I$. This observation does not apply to the category of rigs. 
=-- 

This definition also makes sense for [[nonassociative rings]] (or rigs), with the left/right/two-sided coincidence in the commutative case.

In the case of a [[nonunital ring]] (or rig), if $R$ is being thought of as a [[module]] over some other ring $K$, then it won\'t immediately follow that $I$ is a [[submodule]] of $R$ over $K$, and so one usually includes that requirement as well:

*  $a x \in I$ whenever $a \in K$ and $x \in I$

in the case of left-modules, and similarly in the case of right modules or [[bimodules]].  (Technically, this should be distinguished in the terminology, say by calling $I$ an __ideal of $R$ over $K$__ or the like.)  In particular, a (real or complex) [[Lie ideal]] of a [[Lie algebra]] $R$ is an ideal of $R$ over the real or complex field $K$.


### In lattices (and other prosets)

An __ideal__ in a [[lattice]] (or even [[preorder|proset]]) $L$ is a [[subset]] $I$ of (the underlying set of) $L$ such that:

*  There is an element of $I$ (so that $I$ is [[inhabited set|inhabited]]);
*  if $x, y \in I$, then $x, y \leq z$ for some $z \in I$;
*  if $x \in I$ and $y \leq x$, then $y \in I$ too.

We can make this look more algebraic if $L$ is a (bounded) join-[[semilattice]]:

*  $\bot \in I$;
*  $x \vee y \in I$ if $x, y \in I$;
*  $y \in I$ whenever $x \vee y \in I$.

If $L$ is indeed a lattice, then we can make this look just like the ring version:

*  $\bot \in I$;
*  $x \vee y \in I$ whenever $x, y \in I$;
*  $x \wedge y \in I$ whenever $x \in I$.

The concept of ideal is dual to that of [[filter]].  A subset of $L$ that satisfies the first two of the three axioms for an ideal in a proset is precisely a [[direction|directed subset]] of $L$; notice that this is weaker than being a sub-join-semilattice even if $L$ is a lattice.


### In both at once

There are some common situations where these two kinds of ideal might seem to clash but fortunately do not:

* A [[distributive lattice]] is both a lattice and a commutative rig; the two concepts of ideal are the same, as can be seen by comparing the definition for rigs to the last definition for lattices.

* A [[Boolean algebra]] is a both a distributive lattice and a [[Boolean ring]]; again, the two concepts of ideal are the same (partly because the multiplication operators are the same, although there is still some checking to do regarding closure under addition).

On the other hand, every poset is a poset in an [[opposite poset|opposite]] way, and this does *not* give the same concept of ideal; an ideal in one is a [[filter]] in the opposite one.  We are lucky that the convention for interpreting a Boolean ring as a lattice goes in the correct direction, or the two notions of ideal in a Boolean algebra would not match; or perhaps it is not a matter of luck, but the convention for which way to define ideals in a lattice was chosen precisely to match the conventions for Boolean algebras!


### In monoids

There is a notion of ideal in a [[monoid]] (or even [[semigroup]]), or more generally in a [[monoid object]] in any [[monoidal category]] $C$, which generalises the notion of ideal in a ri(n)g or in a (semi)lattice.  That is, if $C$ is [[Ab]], then a monoid in $C$ is a [[ring]]; if $C$ is [[Ab Mon]], then a monoid in $C$ is a [[rig]]; and a [[semilattice]] is a commutative idempotent monoid in [[Set]].  A left (right) ideal in a monoid (or semigroup) is a subset closed under multiplications with arbitrary elements in the semigroup from the left (right). See [[ideal in a monoid]].

This generalizes all of the above notions of ideal *except* for ideals in prosets that are not (possibly unbounded) join-semilattices.


### In categories

More generally still, passing from monoids to their many-object version and from prosets to their many-morphism version, a right ideal or _[[sieve]]_ in a [[category]] is a subcategory closed under precomposition with morphisms from the entire category, and a left ideal or _[[cosieve]]_ is the dual notion closed under postcompositions with morphisms in the entire category.  See [[sieve]] and [[cosieve]].

### In additive categories 

In ringoids (small additive categories) and additive categories in general, a left/right/2-sided ideal is just the ideal (sieve/cosieve) in the sense of categories which is also closed under group operations in hom groups. 

## Kinds of ideals

Ideals form [[complete lattices]] where arbitrary meets are given by set-theoretic intersection. In other words, ideals form a [[Moore collection]] of subsets of $R$ if $R$ is a rig, or of $L$ if $L$ is a lattice. This implies we have an ideal __generated__ by any [[subset]]: the intersection of all ideals containing the subset.  A subset $S$ that generates a given ideal $I$ may be called a __[[subbase]]__ of $I$; then $S$ is a __[[base]]__ if every element of $I$ is a multiple (in a rig) or a predecessor (in an order) of some element of $S$.  (In particular, every [[singleton subset]] is a base of its generated ideal.)  See also [[filter base]] and dualize for more about bases and subbases of ideals in lattices and other posets.

Certain kinds of ideals are often characterized by the roles they play in ideal lattices, or in terms of the Moore [[closure operator]]. Some examples follow. 

The top element of an ideal lattice is called the *improper ideal*. That is to say, an ideal $I$ is the improper ideal if $x \in I$ for every $x$ (which follows if $1 \in I$ for the case of rigs, or $\top \in I$ for the case of bounded lattices). An ideal $I$ is _proper_ if it is not the improper ideal: if there exists an element $x$ such that $x \notin I$.  So in a [[rig]], $I$ is proper iff $1 \notin I$; in a (bounded) lattice, $I$ is proper iff $\top \notin I$. 

An ideal is a __[[maximal ideal]]__ if it is maximal among *proper* ideals.  A maximal ideal in a rig (including in a distributive lattice, but not in every lattice) is necessarily [[prime ideal|prime]]; conversely, a prime ideal in a [[Boolean algebra]] is necessarily maximal. 

An ideal $I$ is a __[[principal ideal]]__ if it is generated by a singleton. This means there exists an element $x \in I$ such that $y$ is a multiple of $x$ (in a rig) or $y \leq x$ (in an ordered set) whenever $y \in I$; we say that $I$ is __generated__ by $x$. Thus every element $x$ generates a unique principal ideal, the set of all left/right/two-sided multiples of $x$ ($a x$, $x b$, or $a x b$ if we are talking about left/right/two-sided ideals in a rig) or the [[downset]] of $x$ (in an an order). Clearly, every ideal $I$ is a join over all the principal ideals $P_x$ generated by the elements $x$ of $I$. 

As discussed at [[ideals in a monoid]], there is for two-sided ideals an operation of ideal multiplication, making the ideal lattice a [[quantale]] (cf. [[Day convolution]]). Namely, if $I, J$ are ideals, then their product $I J$ is the ideal generated by all products $x y$ with $x \in I, y \in J$ in the case of rigs. Similarly, in the case of lattices, we could define $I J$ to be the ideal generated by all meets $x \wedge y$ -- but in this case the result is the same as $I \cap J$. In any case, we say that a proper ideal $P$ is __[[prime ideal|prime]]__ if for any ideals $I, J$, the condition $I J \subseteq P$ implies $I \subseteq P$ or $J \subseteq P$. In [[order theory]], the term 'prime ideal' is usually used for a _[[strongly irreducible ideal]]_, since the two are equivalent for prosets.

An (left, right, or two-sided) ideal $I$ is __[[irreducible ideal|irreducible]]__ if it is proper and, whenever it is written as the [[intersection]] of two ideals (of the same kind) $I = J \cap K$, then at least one of $J$ and $K$ equals $I$.  If we replace equality here by containment, then we get something more analogous to the definition of prime ideal, called a __[[strongly irreducible ideal]]__.  (Indeed, for [[prosets]], prime ideals and strongly irreducible ideals are the same.)  In general, prime ideals are strongly irreducible, and strongly irreducible ideals are irreducible, but the converses fail.  An ideal is __[[completely irreducible ideal|completely irreducible]]__ if whenever $I$ is an intersection of any (possibly infinite) collection of ideals, $I$ is equal to at least one of them.  (This is _not_ analogous to [[completely prime ideals]].)

An ideal $I$ is a __nil ideal__ if for every $x\in I$, there is an $n\in \mathbb{N}$ with $x^n=0$. That is, every element of the ideal is nilpotent. If on the other hand, there is an $n\in \mathbb{N}$, such that for every $x\in I$, $x^n=0$, the ideal is called __nilpotent__.

+-- {: .num_prop} 
###### Proposition 
A maximal ideal $M$ is prime. 
=-- 

+-- {: .proof} 
###### Proof 
Because the ideal lattice is a [[quantale]], multiplication of ideals distributes over ideal joins. Suppose $I J \subseteq M$ for two ideals $I, J$. If neither is contained in $M$, then $I \vee M = \top = J \vee M$ (the improper ideal) since $M$ is maximal. Then 

$$\top = \top \cdot \top = (I \vee M) \cdot (J \vee M) = I J \vee M J \vee I M \vee M M$$ 

where all four summands are contained in $M$ ($I J \subseteq M$ by supposition, and the other containments hold since $M$ is an ideal). Thus their join is contained in $M$, so we have proved $\top \subseteq M$, contradiction. 
=-- 

That every ideal is contained in a prime ideal is a [[prime ideal theorem]]; that every ideal is contained in a maximal ideal is a [[maximal ideal theorem]].

## Related concepts

* [[differential ideal]]

* [[germ-determined ideal]]

* [[ideal in a monoid]]

* [[filter of a ring]]

* [[modular ideal]]

* [[ideal predicate]]

* [[anti-ideal]]


[[!redirects ideal]]
[[!redirects ideals]]

[[!redirects ideal of a ring]]
[[!redirects ideals of a ring]]
[[!redirects ideals of rings]]
[[!redirects ideal in a ring]]
[[!redirects ideals in a ring]]
[[!redirects ideals in rings]]
[[!redirects ideal of a semiring]]
[[!redirects ideals of a semiring]]
[[!redirects ideals of semirings]]
[[!redirects ideal in a semiring]]
[[!redirects ideals in a semiring]]
[[!redirects ideals in semirings]]
[[!redirects ideal of a rig]]
[[!redirects ideals of a rig]]
[[!redirects ideals of rigs]]
[[!redirects ideal in a rig]]
[[!redirects ideals in a rig]]
[[!redirects ideals in rigs]]

[[!redirects ideal of a lattice]]
[[!redirects ideals of a lattice]]
[[!redirects ideals of lattices]]
[[!redirects ideal in a lattice]]
[[!redirects ideals in a lattice]]
[[!redirects ideals in lattices]]
[[!redirects ideal of a semilattice]]
[[!redirects ideals of a semilattice]]
[[!redirects ideals of semilattices]]
[[!redirects ideal in a semilattice]]
[[!redirects ideals in a semilattice]]
[[!redirects ideals in semilattices]]
[[!redirects ideal of a poset]]
[[!redirects ideals of a poset]]
[[!redirects ideals of posets]]
[[!redirects ideal in a poset]]
[[!redirects ideals in a poset]]
[[!redirects ideals in posets]]

[[!redirects left ideal]]
[[!redirects left ideals]]
[[!redirects right ideal]]
[[!redirects right ideals]]
[[!redirects two-sided ideal]]
[[!redirects two-sided ideals]]

[[!redirects proper ideal]]
[[!redirects proper ideals]]

[[!redirects generated ideal]]
[[!redirects generated ideals]]
[[!redirects ideal generated]]
[[!redirects ideals generated]]
[[!redirects ideal base]]
[[!redirects ideal bases]]
[[!redirects base of an ideal]]
[[!redirects bases of an ideal]]
[[!redirects bases of ideals]]
[[!redirects ideal subbase]]
[[!redirects ideal subbases]]
[[!redirects subbase of an ideal]]
[[!redirects subbases of an ideal]]
[[!redirects subbases of ideals]]

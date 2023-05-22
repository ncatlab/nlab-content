
# Boolean rings
* table of contents
{: toc}

## Idea

A [[Boolean algebra]] is an algebraic structure that models the fragment of the classical propositional calculus that deals with the connectives “and”, “or”, “implies”, and “not”.  In some approaches the definition of Boolean algebra is rather lengthy, but Boolean algebras are equivalent to **Boolean rings**, which are simply rings obeying the identity $x^2 = x$.

In a boolean ring, the multiplication can be interpreted as the conjunction, the multiplicative unit $1$ as the truth value "true", the additive unit $0$ as the truth value "false". The unary operation $x \mapsto 1 + x$ provides the negation. Compared to [[boolean algebras]], which are also [[semiring| semirings]] but not rings (except the trivial boolean algebra), the addition expresses the exclusive disjunction and not the inclusive disjunction. The fact that the exclusive disjunction of $x$ and $x$ is the truth value "false" makes the commutative additive monoid an abelian group where $-x = x$.

## Definitions

A [[ring with unit]] $R$ is __Boolean__ if the operation of multiplication is [[idempotent]]; that is, $x^2 = x$ for every element $x$. Although the terminology would make sense for rings without unit, the common usage assumes a unit. 

Boolean rings and the [[ring]] [[homomorphisms]] between them form a [[category]] $Bool Ring$.


## Properties

*  The characteristic of $R$ divides $2$ (meaning that $x + x = 0$ for all $x$):
   $$ 2 x = 4 x - 2 x = 4 x^2 - 2 x = (2 x)^2 - 2 x = 2 x - 2 x = 0 .$$
R is of characteristic $2$ except if it is the trivial ring, in which case it is of characteristic $1$. 

*  $R$ is commutative (meaning that $x y = y x$ for all $x, y$):
   $$ y x = x + y - x - y + y x = (x + y)^2 - x^2 - y^2 + y x = x^2 + x y + y x + y^2 - x^2 - y^2 + y x = x y + 2 y x = x y .$$

Thus, multiplication in a Boolean ring makes it into a [[semilattice]], while addition makes it into a [[vector space]] over the field with two elements, $\mathbb{F}_2$. 

Define $x \vee y$ to mean $x + x y + y$.  Then:

*  $\vee$ is commutative (as it would be in any commutative ring) and idempotent:
   $$ x \vee x = x + x^2 + x = 3 x = x .$$
*  The absorption law ($x \vee x y = x$) also holds:
   $$ x \vee x y = x + x^2 y + x y = x + 2 x y = x .$$
   We could now prove the other absorption law to conclude that $R$ is a [[lattice]] using multiplication as [[meet]] and $\vee$ as [[join]].
*  But in fact, we can skip that step since it follows the distributive law ($x (y \vee z) = x y \vee x z$):
   $$ x (y \vee z) = x (y + y z + z) = x y + x y z + x z = x y + x^2 y z + x z = x y + (x y) (x z) + x z = x y \vee x z .$$
   Thus $R$ is a [[distributive lattice]].

Next define $\neg{x}$ to be $x + 1$.  Then:

*  $\neg{x}$ is a pseudocomplement of $x$ (meaning that $x (\neg{x}) = 0$):
   $$ x (\neg{x}) = x (x + 1) = x^2 + x = 2 x = 0 .$$
   By relativising from $x + 1$ to $x y + x + 1$, we can show that $R$ is a [[Heyting algebra]].
*  But don\'t bother, because $\neg{x}$ is also an op-pseudocomplement of $x$:
   $$ x \vee \neg{x} = x + x (x + 1) + (x + 1) = x^2 + 3 x + 1 = x + x + 1 = 1 .$$
   Therefore, $\neg{x}$ is a [[complement]] of $x$, and $R$ is a [[Boolean algebra]].


Conversely, starting with a Boolean algebra $R$ (with the meet written multiplicatively), let $x + y$ be $x (\neg{y}) \vee (\neg{x}) y$ (which is called [[exclusive disjunction]] in $\{\top,\bot\}$ and [[symmetric difference]] in $2^X$).  Then $R$ is a Boolean ring.

In fact, we have:
+-- {: .standout}
Boolean rings and Boolean algebras are equivalent.
=--

The category of Boolean algebras is discussed further in [[BoolAlg]], but some of the results about this category are  proved there by working with the equivalent category of Boolean rings.  

The above equivalence extends to an equivalence of [[concrete category|concrete categories]]; that is, given the underlying [[set]] $R$, the set of Boolean ring structures on $R$ is [[natural isomorphism|naturally]] (in $R$) [[bijection|bijective]] with the set of Boolean algebra structures on $R$.

Here is a very convenient result: although a Boolean ring $R$ is a [[rig]] in two different ways (as a ring or as a distributive lattice), these have the same concept of [[ideal]]!


## Examples

The most familiar example is the [[power set]] $\mathcal{P}S$ of any set $S$.  This is a Boolean ring with [[symmetric difference]] as the addition and the intersection of sets as the multiplication. 

The free Boolean ring on a set $X$ can be identified with $\mathcal{P}_f \mathcal{P}_f X$, where $\mathcal{P}_f \colon Set \to Set$ assigns to any set the set of all its finite subsets.  In fact $\mathcal{P}_f \colon Set \to Set$ can be made into a monad in two different ways: the monad for [[semilattices]] (which we use to describe multiplication in a Boolean ring) and the monad for [[vector spaces]] over $\mathbb{F}_2$  (which we use to describe addition in a Boolean ring). These two monads are related by a distributive law which expresses the distributivity of multiplication over addition.   This makes $\mathcal{P}_f \mathcal{P}_f$ into the monad for Boolean rings.

## Terminology

Back in the day, the term 'ring' meant (more often than now is the case) a possibly *non*unital ring; that is a [[semigroup]], rather than a [[monoid]], in [[Ab]].  This terminology applied also to Boolean rings, and it changed even more slowly.  Thus older books will make a distinction between 'Boolean ring' (meaning an idempotent semigroup in $Ab$) and 'Boolean algebra' (meaning an idempotent monoid in $Ab$), in addition to (or even instead of) the difference between $+$ and $\vee$ as fundamental operation.  This distinction survives most in the terminology of $\sigma$-[[sigma-ring|rings]] and $\sigma$-[[sigma-algebra|algebras]]. 

+-- {: .num_remark} 
###### Remark 
We pause to note that "idempotent monoid" doesn't make sense a priori in a general monoidal category: generally speaking the idempotency axiom would be expressed by an equation 

$$1_M = \left(M \stackrel{\delta_M}{\to} M \otimes M \stackrel{mult}{\to} M \right)$$ 

where $\delta_M$ is an appropriate diagonal map, not generally available for monoidal categories. But in a *[[concrete category|concrete]]* monoidal category $\mathbf{M}$ where the underlying-set functor $U: \mathbf{M} \to Set$ is [[lax monoidal functor|lax monoidal]], the meaning is that the evident equation holds: 

$$1_{U(M)} = \left(U(M) \stackrel{\delta}{\to} U(M) \times U(M) \stackrel{\lambda}{\to} U(M \otimes M) \stackrel{U(mult)}{\to} U(M) \right)$$
where $\lambda$ is a lax monoidal constraint. 
=--


## Analogues

Inasmuch as a [[semilattice]] is a commutative idempotent monoid, a Boolean ring may be defined as a semilattice in $Ab$.  However, with Boolean rings, we do not need to hypothesize commutativity; it follows.  That is, any idempotent monoid in $Ab$ is commutative; indeed, any idempotent [[magma]] in $Ab$ is commutative. 

+-- {: .proof} 
###### Proof 
Write the magma operation as $(x, y) \mapsto x y$. Then for any element $x$, idempotence and bilinearity imply 

$$x + x = (x + x)(x + x) = (x + x)x + (x + x)x = (x x + x x) + (x x + x x) = (x + x) + (x + x)$$ 

which by cancellation gives $x + x = 0$, or $x = -x$. Similarly, for any elements $x, y$, 

$$x + y = (x + y)(x + y) = (x + y)x + (x + y)y = (x x + y x) + (x y + y y) = x + y x + x y + y$$ 

which by cancellation gives $y x + x y = 0$, or $y x = -(x y) = x y$. 
=--

[[!redirects Boolean ring]]
[[!redirects boolean ring]]
[[!redirects Boolean rings]]
[[!redirects boolean rings]]
[[!redirects Boo Rng]]
[[!redirects BooRng]]
[[!redirects Boo Ring]]
[[!redirects BooRing]]
[[!redirects Bool Ring]] 
[[!redirects BoolRing]]

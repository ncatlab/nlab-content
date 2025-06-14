
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Boolean rings
* table of contents
{: toc}

## Idea

A [[boolean algebra]] is an algebraic structure that models the fragment of the classical propositional calculus that deals with the connectives “and”, “or”, “implies”, and “not”.  In some approaches the definition of boolean algebra is rather lengthy, but boolean algebras are equivalent to **boolean rings**, which are simply rings obeying the identity $x^2 = x$. 

In a boolean ring, the multiplication can be interpreted as the conjunction, the multiplicative unit $1$ as the truth value "true", the additive unit $0$ as the truth value "false". The unary operation $x \mapsto 1 + x$ provides the negation. Compared to [[boolean algebras]], which are also [[semiring| semirings]] but not rings (except the trivial boolean algebra), the addition expresses the exclusive disjunction and not the inclusive disjunction. The fact that the exclusive disjunction of $x$ and $x$ is the truth value "false" makes the commutative additive monoid an abelian group where $-x = x$.

## Definitions

### As a ring

A [[ring with unit]] $R$ is __boolean__ if the operation of multiplication is [[idempotent]]; that is, $x^2 = x$ for every element $x$, thus making multiplication a [[band]]. Although the terminology would make sense for rings without unit, the common usage assumes a unit. 

Boolean rings and the [[ring]] [[homomorphisms]] between them form a [[category]] $Bool Ring$.

### As a rig

In fact, the additive inverse of a [[ring]] is not needed to define a Boolean ring; one only needs the structure of a [[rig]]. A **Boolean ring** is a [[rig]] which 

* is [[multiplicatively idempotent rig|multiplicatively idempotent]] in that $x^2 = x$ for all $x$; 

* has [[characteristic of a rig|characteristic]] $(0, 2)$ in that $x + x = 0$ for all $x$.  

The axiom $x + x = 0$ automatically implies that the rig is a [[ring]] with [[characteristic]] $2$, with the additive inverse defined as the [[identity function]] on the rig. This also implies that every [[rig]] [[homomorphism]] between rigs with characteristic $(0, 2)$ is a [[ring homomorphism]]. 

Thus, Boolean rings and the [[rig]] [[homomorphisms]] between them form a [[category]] $Bool Ring$.

## Properties

*  A boolean ring is an [[algebra]] over the [[field]] [[prime field|$\mathbb{F}_2$]] with two elements, since 
   $$ 2 x = 4 x - 2 x = 4 x^2 - 2 x = (2 x)^2 - 2 x = 2 x - 2 x = 0 .$$

*  $R$ is commutative (meaning that $x y = y x$ for all $x, y$):
   $$ y x = x + y - x - y + y x = (x + y)^2 - x^2 - y^2 + y x = x^2 + x y + y x + y^2 - x^2 - y^2 + y x = x y + 2 y x = x y .$$

Thus, multiplication in a boolean ring makes it into a [[01-bounded semilattice]], while addition makes it into a [[vector space]] over the field with two elements, $\mathbb{F}_2$. 

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


Conversely, starting with a boolean algebra $R$ (with the meet written multiplicatively), let $x + y$ be $x (\neg{y}) \vee (\neg{x}) y$ (which is called [[exclusive disjunction]] in $\{\top,\bot\}$ and [[symmetric difference]] in $2^X$).  Then $R$ is a boolean ring.

In fact, we have:
\begin{proposition} 
The categories of Boolean rings and Boolean algebras are equivalent.
\end{proposition} 

+-- {: .proof} 
###### Proof 
Since the Boolean algebra operations $\wedge, \vee, \neg, 0, 1$ are definable from the Boolean ring operations $+, -, \cdot, 0, 1$, and conversely, it follows that a function $f: {|A|} \to {|B|}$ between the underlying sets of Boolean rings is a Boolean ring homomorphism (i.e., preserves the Boolean ring operations) if and only if it is a Boolean algebra homomorphism (between the Boolean algebra structures defined on the same sets). In other words, the subsets 

$$BoolRing(A, B) \hookrightarrow Set({|A|}, {|B|}), \qquad BoolAlg(A, B) \hookrightarrow Set({|A|}, {|B|})$$

coincide. Therefore the categories of Boolean rings and of Boolean algebras are equivalent as [[concrete categories]]. 
=-- 

The category of Boolean algebras is discussed further in [[BoolAlg]], but some of the results about this category are  proved there by working with the equivalent category of Boolean rings.  

Here is a very convenient result: although a boolean ring $R$ is a [[rig]] in two different ways (as a ring or as a distributive lattice), these have the same concept of [[ideal]]!

Finally, let [[Ab]] be the [[concrete category|concrete]] [[monoidal category]] of [[abelian groups]], and let $U: Ab \to Set$ be the [[lax monoidal functor|lax monoidal]] underlying-set functor. Then,

\begin{theorem}
Every Boolean ring $R$ satisfies the equation
$$1_{U(R)} = \left(U(R) \stackrel{\delta}{\to} U(R) \times U(R) \stackrel{\lambda}{\to} U(R \otimes R) \stackrel{U(mult)}{\to} U(R) \right)$$
where $\lambda$ is a lax monoidal constraint. 
\end{theorem}

## Examples

The most familiar example is the [[power set]] $\mathcal{P}S$ of any set $S$. This is a boolean ring with [[symmetric difference]] as the addition and the intersection of sets as the multiplication. In [[constructive mathematics]], one would use the set of [[decidable subsets]] $2^S$ instead of the set of all subsets $\mathcal{P}S$ to get the corresponding boolean ring.

More generally, given any Boolean ring $R$ and a set $S$, the [[function ring]] $R^S$ is a Boolean ring. 

In classical mathematics the free boolean ring on a set $X$ can be identified with $\mathcal{P}_f \mathcal{P}_f X$, where $\mathcal{P}_f X$ is  the set of all finite subsets of $X$.  In fact $\mathcal{P}_f$ can be extended to a functor in two different ways, which agree on objects but differ on morphisms, and each of these gives a monad:

* the monad for [[semilattices]], $M \colon Set \to Set$ (which we use to describe multiplication in a boolean ring) 

* the monad for [[vector spaces]] over the [[field]] with 2 elements, $S \colon Set \to Set$ (which we use to describe addition in a boolean ring). 

These two monads are related by a distributive law which expresses the distributivity of multiplication over addition.   Their composite $S \circ M$ is then the monad for Boolean rings.

## Terminology

Back in the day, the term 'ring' meant (more often than now is the case) a possibly *non*unital ring; that is a [[semigroup]], rather than a [[monoid]], in [[Ab]].  This terminology applied also to boolean rings, and it changed even more slowly.  Thus older books will make a distinction between 'boolean ring' (meaning [[multiplicatively idempotent semiring|multiplicatively idempotent]] [[non-unital ring]]) and 'boolean algebra', in addition to (or even instead of) the difference between $+$ and $\vee$ as fundamental operation. This distinction survives most in the terminology of $\sigma$-[[sigma-ring|rings]] and $\sigma$-[[sigma-algebra|algebras]]. 

## Analogues

Inasmuch as a [[semilattice]] is a commutative idempotent monoid, a boolean ring can be defined as a ring whose multiplication is a [[semilattice]]. However, with boolean rings, we do not need to hypothesize commutativity; it follows. That is, any ring whose multiplication is an [[idempotent monoid]] is commutative; indeed, any idempotent bilinear [[magma]] is commutative. 

\begin{proof}
Write the magma operation as $(x, y) \mapsto x y$. Then for any element $x$, idempotence and bilinearity imply 

$$x + x = (x + x)(x + x) = (x + x)x + (x + x)x = (x x + x x) + (x x + x x) = (x + x) + (x + x)$$ 

which by cancellation gives $x + x = 0$, or $x = -x$. Similarly, for any elements $x, y$, 

$$x + y = (x + y)(x + y) = (x + y)x + (x + y)y = (x x + y x) + (x y + y y) = x + y x + x y + y$$ 

which by cancellation gives $y x + x y = 0$, or $y x = -(x y) = x y$. 
\end{proof}

## Related concepts

* [[Boolean algebra]]
* [[BoolAlg]] - the category of boolean algebras
* [[multiplicatively idempotent rig]]
* [[01-bounded semilattice]]
* [[band]], [[idempotent monoid]]

## References

* Wikipedia, *[Boolean ring](https://en.wikipedia.org/wiki/Boolean_ring)*

* {#Rogers24} [[Morgan Rogers]], *From free idempotent monoids to free multiplicatively idempotent rigs* &lbrack;[arXiv:2408.17440](https://arxiv.org/abs/2408.17440)&rbrack;

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

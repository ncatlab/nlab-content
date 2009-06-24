A [[ring]] $R$ is __Boolean__ if the operation of multiplication is [[idempotent]]; that is, $x^2 = x$ for every element $x$.


Consequences:

*  $R$ has characteristic $2$ (meaning that $x + x = 0$ for all $x$):
   $$ 2 x = 4 x - 2 x = 4 x^2 - 2 x = (2 x)^2 - 2 x = 2 x - 2 x = 0 .$$
*  $R$ is commutative (meaning that $x y = y x$ for all $x, y$):
   $$ y x = x + y - x - y + y x = (x + y)^2 - x^2 - y^2 + y x = x^2 + x y + y x + y^2 - x^2 - y^2 + y x = x y + 2 y x = x y .$$


Define $x \vee y$ to mean $x + x y + y$.  Then:

*  $\vee$ is commutative (as it would be in any commutative ring) and idempotent:
   $$ x \vee x = x + x^2 + x = 3 x = x .$$
*  The absorption law ($x \vee x y = x$) also holds:
   $$ x \vee x y = x + x^2 y + x y = x + 2 x y = x .$$
   We could now prove the other absoprtion law to conclude that $R$ is a [[lattice]] using multiplication as [[meet]] and $\vee$ as [[join]].
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

This extends to an equivalence of [[concrete category|concrete categories]]; that is, given the underlying [[set]] $R$, the set of Boolean ring structures on $R$ is [[natural isomorphism|naturally]] (in $R$) [[bijection|bijective]] with the set of Boolean algebra structures on $R$.

Here is a very convenient result: although a Boolean ring $R$ is a [[rig]] in two different ways (as a ring or as a distributive lattice), these have the same concept of [[ideal]]!


## Terminology

Back in the day, the term 'ring' meant a possibly *non*unital ring; that is, a [[semigroup]], rather than a [[monoid]], in [[Ab]].  This terminology applied also to Boolean rings, and it changed even more slowly.  Thus older books will make a distinction between 'Boolean ring' (meaning an idemptotent semigroup in $Ab$) and 'Boolean algebra' (meaning an idempotent monoid in $Ab$), in addition to (or even instead of) the difference between $+$ and $\vee$ as fundamental operation.  This distinction survives most in the terminology of $\sigma$-[[sigma-ring]]s and $\sigma$-[[sigma-algebra]]s.
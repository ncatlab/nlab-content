
> this entry is about the notion of [[colimits]] in [[posets]]. For the concepts of _[[join of topological spaces]]_, _[[join of simplicial sets]]_, _[[join of categories]]_ and _[[join of quasi-categories]]_ see there.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

If $x$ and $y$ are elements of a [[partial order|poset]] $P$, then their __join__ (or __supremum__, abbreviate _sup_, or __least upper bound__, abbreviated _lub_), is an element $x \vee y$ of the poset such that:

* $x \leq x \vee y$ and $y \leq x \vee y$;
* if $x \leq a$ and $y \leq a$, then $x \vee y \leq a$.

(These may be combined as: for all $a$, $x \vee y \leq a$ iff $x \leq a$ and $y \leq a$.)  Such a join may not exist; if it does, then it is unique.

If $P$ is a [[preorder|proset]], then join may be defined similarly, but it need not be unique.  (However, it is still unique up to the natural [[equivalence]] in $P$.)

The above definition is for the join of two elements of $P$, but it can easily be generalised to any number of elements.  It may be more common to use 'join' for a join of finitely many elements and 'supremum' for a join of (possibly) infinitely many elements, but they are the same concept.  The join may also be called the **maximum** if it equals one of the original elements.

A poset that has all finite joins is a **join-[[semilattice]]**.  A poset that has all suprema is a **[[suplattice]]**.

A join of [[subset]]s or [[subobject]]s is called a [[union]].


## Special cases

A join of zero elements is a [[bottom]] element.  Any element $a$ is a join of that one element.


## Properties

As a poset is a special kind of [[category]], so a join is simply a [[coproduct]] in that category.


## In constructive mathematics {#constructive}

In [[constructive analysis]], we sometimes want a stronger notion of supremum.  (Dual remarks apply to [[infima]].)

Let $S$ be a set of [[real numbers]], and let $M$ be a real number.  We say (as above) that $M$ is a __least upper bound__ (lub) of $S$ if for each real number $a$, $M \leq a$ iff for each member $x$ of $S$, $x \leq a$.  But we say that $M$ is a __supremum__ of $S$ if for each real number $a$, $M \gt a$ iff for some member $x$ of $S$, $x \gt a$.  In [[constructive mathematics]], we can prove that lubs and suprema are both unique when they exist and that every supremum is an lub, but we cannot prove that every lub is a supremum.  (We can prove that, if $M$ is an lub of $S$ and $M \gt a$, then there is [[double negation|not not]] some member $x$ of $S$ such that $x \gt a$, but not that there is such an member $x$.  For a specific [[weak counterexample]], let $p$ be any [[truth value]], and let $S$ be the [[subsingleton]] $\{0 \;|\; p\}$.  Then $0$ is a supremum of $S$ iff $p$ is true, while $0$ is an lub of $S$ iff $p$ is not not true.)

This generalizes to any set $P$ equipped with a relation $\gt$ (better written $\nleq$ in the general case) that is an [[irreflexive relation|irreflexive]] [[connected relation|connected]] [[comparison]] (properties [[de Morgan duality|dual]] to the properties that define a [[partial order]]) if $\leq$ is defined as the [[negation]] of $\nleq$ (which forces $\leq$ to be a partial order).  It\'s not even necessary for $\nleq$ to be a comparison, as long as its negation is a partial order (which still forces $\nleq$ to be irreflexive and connected).

Still more generally, let $P$ be a set equipped with the [[antithesis interpretation]] of a partial order.  This consists of two [[binary relations]] $\leq$ and $\nleq$ such that $\leq$ is a partial order, $\nleq$ is irreflexive, and $\leq$ and $\nleq$ are compatible:

* $y \geq x \nleq z$ implies $y \nleq z$,
* $x \nleq z \geq y$ implies $x \nleq y$.

Then we have two versions of a join $M$:

* for each element $a$ of $P$, $M \leq a$ iff for each member $x$ of $S$, $x \leq a$;
* for each element $a$ of $P$, $M \nleq a$ iff for some member $x$ of $S$, $x \nleq a$.

Then neither of these implies the other, and we probably really want to demand *both* at once.  The extended [[MacNeille real numbers]] provide a good example here.


## Related concepts

* **join**

* [[meet]]


[[!redirects join]]
[[!redirects joins]]
[[!redirects supremum]]
[[!redirects supremums]]
[[!redirects suprema]]
[[!redirects sup]]
[[!redirects sups]]
[[!redirects least upper bound]]
[[!redirects least upper bounds]]
[[!redirects lub]]
[[!redirects lubs]]
[[!redirects (0,1)-colimit]]
[[!redirects (0,1)-colimits]]

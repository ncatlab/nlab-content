+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

> For other kinds of units see also _[[unit of an adjunction]]_ and _[[unit of a monad]]_. Different (but related) is _[[physical unit]]_. 

****

# Units
* table of contents
{: toc}

## Idea

Considering a [[ring]] $R$, then by _the unit element_ or _the multiplicative unit_ one usually means the [[neutral element]] $1 \in R$ with respect to [[multiplication]]. This is the sense of "unit" in terms such as _[[nonunital ring]]_.

But more generally _a unit element_ in a unital (!) ring is any element that has an [[inverse element]] under [[multiplication]]. 

This concept generalizes beyond [[rings]], and this is what is discussed in the following.



## Definitions

Exactly what this means depends on context.  A very general definition is this:

Given [[sets]] $R$ and $M$, and a [[function]] ${\cdot}\colon R \times M \to M$, an [[element]] $u$ of $M$ is a __unit__ (relative to the operation ${\cdot}$) if, given any element $x$ of $M$, there exists a unique element $a$ of $R$ such that $x = a \cdot u$.

That is, every element of $M$ is a multiple (in a unique way) of $u$, where 'multiple' is defined in terms of the operation ${\cdot}$.


### Units in rings

If $R$ is a [[ring]] (or [[rig]]), then $R$ comes equipped with a multiplication map ${\cdot}\colon R \times R \to R$.  So $R$ can play the role of both $R$ and $M$ above, although there are two ways to do this: on the left and on the right.

We find that $u$ is a __left unit__ if and only if $u$ has a [[left inverse]], and $u$ is a __right unit__ if and only if $u$ has a [[right inverse]].  First, an element $u$ with an inverse is a unit because, given any element $x$, we have
$$ x = (x u^{-1}) u $$
(on the left) or
$$ x = u (u^{-1} x) $$
(on the right).  Conversely, a unit must have an inverse, since there must a solution to
$$ 1 = a u $$
(on the left) or
$$ 1 = u a $$
(on the right).

The collection of all units in a unital ring form a [[group]], the *[[group of units]]*.

In a [[commutative ring]] (or rig), a __unit__ is an element of $R$ that has an [[inverse element|inverse]], period.  Of course, a commutative ring $R$ is a [[field]] just when every non-[[zero]] element is a unit.


### Units in monoids

Notice that addition plays no role in the characterisation above of a unit in a ring.  Accordingly, a unit in a [[monoid]] may be defined in precisely the same way.

A [[group]] is precisely a monoid in which every element is a unit.


### Units in rngs or semigroups

In a [[rng]] (or, ignoring addition, in a [[semigroup]]), we cannot speak of inverses of elements.  However, we can still talk about units; $u$ is a __left unit__ if, for every $x$, there is an $a$ such that
$$ x = a u ;$$
and $u$ is a __right unit__ if, for every $x$, there is an $a$ such that
$$ x = u a .$$


### Units in nonassocative rings or magmas

In a [[nonassociative algebra|nonassociative ring]] (or, ignoring addition, in a [[magma]]), even if we have an identity element, an invertible element might not be a unit.  So we must use the same explicit definition as in a rng (or semigroup) above.

A [[quasigroup]] is precisely a magma in which every element is a two-sided unit.


### Units in modules

If $R$ is a [[ring]] (or [[rig]]) and $M$ an $R$-[[module]], then a __unit__ in $M$ is an element $u \in M$ such that every other $x \in M$ can be written as $x = a u$ (or $x = u a$ for a right module) for some $a \in R$.  This is the same as a [[generator]] of $M$ as an $R$-module.  There is no need to distinguish left and right units unless $M$ is a [[bimodule]].  Note that a (left or right) unit in $R$ _qua_ ring is the same as a unit in $R$ _qua_ (left or right) $R$-module.


### Units of measurement
 {#UnitsOfMeasurement}

In [[physics]], the quantities of a given dimension generally form an $\mathbb{R}$-[[line]], a $1$-dimensional [[real vector space]]. Since $\mathbb{R}$ is a [[field]], any non-[[zero]] element is a unit, called in this context a __[[unit of measurement]]__.  This is actually a special case of a unit in a module, where $R \coloneqq \mathbb{R}$ and $M$ is the line in question.

Often (but not always) these quantities form an [[orientation|oriented]] line, so that nonzero quantities are either positive or negative.  Then we usually also require a unit of measurement to be positive.  In fact, for some dimensions, there is no physical meaning to a negative quantity, in which case the quantities actually form a module over the rig $\mathbb{R}_{\ge 0}$ and every nonzero element is "positive."

For example, the [[kilogram]] is a unit of mass, because any mass may be expressed as a real multiple of the kilogram.  Further, it is a positive unit; the mass of any physical object is a nonnegative quantity (so that mass quantities actually form an $\mathbb{R}_{\ge 0}$-module) and may be expressed as a nonnegative real multiple of the kilogram.


## Identities as units

Often the term 'unit' (or 'unity') is used as a synonym for '[[identity element]]', especially when this identity element is denoted $1$.  For example, a 'ring with unit' (or 'ring with unity') is a ring with an identity (used by authors who say 'ring' for a rng).  Of course, a rng with identity has a unit, since $1$ itself is a unit; the converse also holds.

\begin{prop}
A rng with a unit must have an identity.
\end{prop}

\begin{proof}
Let $R$ be a rng with a unit $u$;\linebreak

For any $a,b\in R$ denote by ${}_a u^{-1}$ the unique element s.t. $a= {}_a u^{-1} \cdot u$, and denote by $u^{-1}_b$ the unique element s.t. $b= u\cdot u^{-1}_b$;\linebreak
the goal is to show that $u^{-1}_u= {}_u u^{-1}$ and that is the identity of $R$.

One has
$$ a\cdot u^{-1}_u= {}_a u^{-1}\cdot u \cdot u^{-1}_u= {}_a u^{-1} \cdot u = a$$
and also
$$ {}_u u^{-1} \cdot b= {}_u u^{-1} \cdot u\cdot u^{-1}_b=u\cdot u^{-1}_b=b,$$
for all $a,b\in R$;\linebreak
therefore, it remains to show that $u^{-1}_u= {}_u u^{-1}$.

To accomplish this, notice that, on one hand, one has $u = {}_u u^{-1}\cdot u$;\linebreak
on the other hand, one has $u\cdot u^{-1}_u \cdot u=u\cdot u$, hence $u\cdot (u^{-1}_u\cdot u-u)=0$, which must imply $u= u^{-1}_u\cdot u$ since $u$ is neither a left nor a right zero divisor (The equations $0=x\cdot u$ and $0=u\cdot x$ both have $0$ as a solution, and that must be unique).

By uniqueness of the solution to $u=x\cdot u$, one concludes that $u^{-1}_u= {}_u u^{-1}$.
\end{proof}

It is this meaning of 'unit' which gives rise to the [[unit of an adjunction]].

## Related concepts

* [[group of units]]

* [[unit object]]

* [[unit of an adjunction]]

* [[unit of a monad]]

* [[monad terminology]]

* [[exponential ring]]


## References

See also 

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Unit_(ring_theory)">Unit (Ring theory)</a>_

[[!redirects unit]]
[[!redirects units]]

[[!redirects unit element]]
[[!redirects unit elements]]

[[!redirects unit of measurement]]
[[!redirects unit of measurements]]
[[!redirects units of measurement]]
[[!redirects units of measurements]]




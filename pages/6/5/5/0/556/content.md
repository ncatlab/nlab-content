# Idea #

A **2-categorical limit** is the type of [[limit]] that is appropriate in a [[2-category]].  There are two notable changes when passing from ordinary 1-categorical limits to 2-categorical limits:

1. Limits can be either strict or weak, depending on whether their universal property is expressed by an [[equivalence]] of categories or an [[isomorphism]] of categories.

1. Since 2-categories are [[enriched category|enriched]] over [[Cat]] (this is precise in the [[strict 2-category|strict]] case, and "weakly" true in the [[bicategory|weak]] case), Cat-[[weighted limit]]s become important.  This means that both the diagrams we take limits of and the shape of "cones" that limits represent can involve 2-cells as well as 1-cells.

# Classification #

## Limits in a 2-category ##

In a [[strict 2-category]] $K$, there are several different types of limits.

* A **strict limit**, or _2-limit_ is just a [[Cat]]-enriched (weighted) limit.  This means that its cones must commute strictly (although weakness can be built in via the weighting, see below), and its universal property is expressed by an isomorphism of categories.

* A **pseudo limit**  is a limit whose cones commute up to coherent 2-cell isomorphism, but whose universal property can still be expressed by an _isomorphism_ of categories.  For any weight $W$, there is another weight $W'$ (a [[cofibrant replacement]] of $W$) such that pseudo $W$-weighted limits are equivalent to strict $W'$-weighted ones.  The idea is that $W'$ includes explicitly all the extra isomorphisms in a pseudo $W$-cone.

* A **lax limit** is a limit whose cones commute only up to a coherent transformation in one direction, but again whose universal property is expressed by an isomorphism.  Likewise we have **oplax limits** where the transformation goes in the other direction.  Lax and oplax limits can also be rephrased as strict limits for a different weight.

## Limits in a bicategory ##

In a [[bicategory]] $K$, it makes little sense to do anything any stricter than up to 2-cell isomorphism and equivalence of categories.  Thus, in this case,

* A **bicategorical limit**, formerly called a _bilimit_ and often called just a _limit_ if it is clear we are working in a bicategory, has cones that commute up to specified isomorphism, and has a universal property expressed by an equivalence of categories.

* A **lax bicategorical limit**, or _lax bilimit_ or just _lax limit_, has cones that commute up to a transformation, and a universal property expressed by an equivalence.

_NB: The term "weak limit" may seem attractive, but unfortunately it has a different meaning._

## Comparison ##

Since any strict 2-category can be regarded as a bicategory with trivial constraints, bicategorical limits can also be defined in a strict 2-category.  Then we have:

* Since any isomorphism of categories is _a fortiori_ an equivalence of categories, any pseudo limit is also a bicategorical limit.  Likewise, any (op)lax limit is also an (op)lax bicategorical limit.

* More generally, any [[flexible limit]], and hence also any [[PIE-limit]], is also a bicategorical limit.  Morally, these are the non-[[evil]] limits: since they don't demand equality of objects, they can still exist even when everything becomes weak.  Since pseudo limits are PIE-limits, it follows that any strict 2-category which admits PIE-limits also admits all bicategorical limits, even if it fails to admit some (evil) strict 2-categorical limits (such as equalizers).

* However, not every bicategorical limit in a strict 2-category is a pseudo limit, even when pseudo limits exist.  Any object equivalent to a bicategorical limit is also a bicategorical limit; thus any object that is equivalent, but not isomorphic, to a pseudo limit, is a bicategorical limit but not a pseudo limit.

* Bicategorical limits can also exist even if pseudo limits fail to exist.  For instance, the 2-category of monoidal categories, (strong) monoidal functors, and monoidal transformations has a bicategorical initial object, but it is not a strict 2-limit of any sort.

# Examples #

(To be continued...)

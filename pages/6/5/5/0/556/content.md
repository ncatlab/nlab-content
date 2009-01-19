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

* More generally, any non-[[evil]] limit (one which doesn't demand equality of objects) can still exist even when everything becomes weak.  Two formal versions of this statement involve [[flexible limit]]s and the more restrictive [[PIE-limit]]s.  In particular, any strict flexible limit is also a bicategorical limit.  Since pseudo limits are PIE-limits, it follows that any strict 2-category which admits PIE-limits also admits all bicategorical limits, even if it fails to admit some (evil) strict 2-categorical limits.  The category of algebras and pseudo morphisms for any [[2-monad]], such as [[MonCat]], is a good example of a 2-category having strict PIE-limits but not all strict limits.

* However, not every bicategorical limit in a strict 2-category is a pseudo limit, even when pseudo limits exist.  Any object equivalent to a bicategorical limit is also a bicategorical limit; thus any object that is equivalent, but not isomorphic, to a pseudo limit, is a bicategorical limit but not a pseudo limit.

* Bicategorical limits can also exist even if pseudo limits fail to exist.  For instance, the 2-category of monoidal categories, (strong) monoidal functors, and monoidal transformations has a bicategorical initial object, but it is not a strict 2-limit of any sort.

# Examples #

* Any ordinary limit can be made into a strict 2-categorical limit simply by boosting up its ordinary universal property (a bijection of sets) to an isomorphism of hom-categories.  Thus we have strict products, strict pullbacks, strict equalizers, and so on.  Of these, strict products (including terminal objects) are non-evil, hence give bicategorical products as well, while all others such as pullbacks and equalizers tend to be evil.

* Any ordinary limit can also be made into a bicategorical limit by making everything happen up to isomorphism.  Thus, a bicategorical pullback is a square that commutes up to specified isomorphism, with a universal property expressed by an equivalence of categories.

* The **comma object** $(f/g)$ of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a generalization of the [[comma category]] in $Cat$; it is a universal object equipped with projections $p:(f/g)\to A$ and $q:(f/g)\to B$ and a 2-cell $f p \to g q$.  This can be interpreted either strictly or weakly.  Since it is non-evil, the strict case is a special case of the bicategorical one.

* An **iso-comma object** is like a comma object, except that the 2-cell $f p \to g q$ is required to be invertible.  Similar but distinct (in the strict case) is a **pseudo-pullback**, which is an object $P$ equipped with projections $p:P\to A$, $q:P\to B$, and $r:P\to C$ with 2-cell isomorphisms $f p \cong r$ and $g q \cong r$.  Both are non-evil, and both are a bicategorical pullback.  Hence, if both exist, they are equivalent (though not isomorphic).

* The **inserter** of a pair of parallel arrows $f,g:A \;\rightrightarrows\; B$ is a universal object $I$ equipped with a map $i:I\to A$ and a 2-cell $f i \to g i$.  It has strict and weak versions, and is non-evil.

* Unsurprisingly, an **iso-inserter** is like an inserter except that the 2-cell is an isomorphism.  It is distinct from the **pseudo-equalizer** which comes with maps $i:I\to A$ and $j:I\to B$ and isomorphisms $f i \cong j$ and $g i \cong j$.  Both are non-evil and represent a bicategorical limit which is sometimes called a "biequalizer" or "pseudoequalizer," but which [[Mike Shulman|I]] prefer to also call a "(bicategorical) iso-inserter," since it behaves noticeably differently from an equalizer in a 1-category.

* The **equifier** of a pair of parallel 2-cells $\alpha,\beta: f\to g: A\to B$ is a universal object $E$ equipped with a map $e:E\to A$ such that $\alpha e = \beta e$.  It is non-evil in its strict form.

* The **inverter** of a 2-cell $\alpha:f\to g:A\to B$ is a universal object $V$ with a map $v:V\to A$ such that $\alpha v$ is invertible. It is non-evil in its strict form.

* The **[[power]]** of an object $A$ by a category $C$ is a universal object $A^C$ equipped with a functor $C\to K(A^C,A)$.  It is non-evil in its strict form.

* [[descent object|Descent objects]] are another important example.

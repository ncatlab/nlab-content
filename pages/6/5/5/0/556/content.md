# Idea #

A **2-categorical limit** is the type of [[limit]] that is appropriate in a [[2-category]].  There are two notable changes when passing from ordinary 1-categorical limits to 2-categorical limits:

1. Limits can be either strict or weak, depending on whether their universal property is expressed by an [[equivalence]] of categories or an [[isomorphism]] of categories.

1. Since 2-categories are [[enriched category|enriched]] over [[Cat]] (this is precise in the [[strict 2-category|strict]] case, and "weakly" true in the [[bicategory|weak]] case), Cat-[[weighted limit]]s become important.  This means that both the diagrams we take limits of and the shape of "cones" that limits represent can involve 2-cells as well as 1-cells.

+--{.query}
Just as we now say '$2$-category' for [[2-category|the general notion]] and 'strict $2$-category' if we really want [[strict 2-category|the strict case]], shouldn\'t we say '$2$-limit' for the general notion here (which would presumably lead us to [[2-limit|move the page]]) and 'strict $2$-limit' if we really want the strict case? &#8212;Toby

_Mike_: Well, suppose I quote what you wrote at [[bicategory]]:

> Even in a strict 2-category, while we might need to say "strict" sometimes to be clear, we don't need to say "2-", since we know that we are not working in a mere category. (Max Kelly pushed this point.)

So when we are in a 2-category (strict or weak), I think "limit" should mean "2-categorical limit" without the need for a prefix.  And in a strict 2-category we can say "strict limit" if that's what we mean.
=--

# Classification #

## Limits in a weak 2-category ##

In a weak 2-category (of which the commonest model is a [[bicategory]]), it makes little sense to do anything any stricter than up to 2-cell isomorphism and equivalence of categories.  Thus, in this case,

* A **bicategorical limit**, formerly called a _bilimit_ and often called just a _limit_ if it is clear we are working in a weak 2-category, has cones that commute up to specified isomorphism, and has a universal property expressed by an equivalence of categories.

* A **lax bicategorical limit**, or _lax bilimit_ or just _lax limit_, has cones that commute up to a transformation, and a universal property expressed by an equivalence.

If we know that we are working in a weak 2-category, then no other sort of limit makes sense, so we can just use the word "limit" for a bicategorical limit; a prefix is only necessary to distinguish it from strict limits in a strict 2-category or in a 1-category.

_NB: The term "weak limit" may seem attractive, but unfortunately it has a different meaning.  Therefore, although on the nLab we usually say "weak 2-category" instead of "bicategory" (with "weak" only added for emphasis if necessary), on this page and elsewhere we use "bicategorical" for the up-to-equivalence type of limit._


## Limits in a strict 2-category ##

Of course, every [[strict 2-category]] can be regarded as a weak one, so we can talk about bicategorical limits and lax bicategorical limits, and usually these are the ones we are "really" interested in.  However, we can also talk about stricter types of limits, of which there are several different ones.

* A **strict limit**, or _2-limit_ is just a [[Cat]]-enriched (weighted) limit.  This means that its cones must commute strictly (although weakness can be built in via the weighting, see below), and its universal property is expressed by an isomorphism of categories.

* A **pseudo limit**  is a limit whose cones commute up to coherent 2-cell isomorphism, but whose universal property can still be expressed by an _isomorphism_ of categories.  For any weight $W$, there is another weight $W'$ (a [[cofibrant replacement]] of $W$) such that pseudo $W$-weighted limits are equivalent to strict $W'$-weighted ones.  The idea is that $W'$ includes explicitly all the extra isomorphisms in a pseudo $W$-cone.

* A **lax limit** is a limit whose cones commute only up to a coherent transformation in one direction, but again whose universal property is expressed by an isomorphism.  Likewise we have **oplax limits** where the transformation goes in the other direction.  Lax and oplax limits can also be rephrased as strict limits for a different weight.


## Comparison ##

As remarked above, since any strict 2-category can be regarded as a weak 2-category, bicategorical limits can also be defined in a strict 2-category.  Then we have:

* Since any isomorphism of categories is _a fortiori_ an equivalence of categories, any pseudo limit is also a bicategorical limit.  Likewise, any (op)lax limit is also an (op)lax bicategorical limit.

* More generally, any non-[[evil]] limit (one which doesn't demand equality of objects) can still exist even when everything becomes weak.  Two formal versions of this statement involve [[flexible limit]]s and the more restrictive [[PIE-limit]]s.  In particular, any strict flexible limit is also a bicategorical limit.  Since pseudo limits are PIE-limits, it follows that any strict 2-category which admits PIE-limits also admits all bicategorical limits, even if it fails to admit some (evil) strict 2-categorical limits.  The category of algebras and pseudo morphisms for any [[2-monad]], such as [[MonCat]], is a good example of a 2-category having strict PIE-limits but not all strict limits.

* However, not every bicategorical limit in a strict 2-category is a pseudo limit, even when pseudo limits exist.  Any object equivalent to a bicategorical limit is also a bicategorical limit; thus any object that is equivalent, but not isomorphic, to a pseudo limit, is a bicategorical limit but not a pseudo limit.

* Bicategorical limits can also exist even if pseudo limits fail to exist.  For instance, the strict 2-category of monoidal categories, (strong) monoidal functors, and monoidal transformations has a bicategorical initial object, but it is not a strict 2-limit of any sort.

# Examples #

* Any ordinary limit can be made into a strict 2-categorical limit simply by boosting up its ordinary universal property (a bijection of sets) to an isomorphism of hom-categories.  Thus we have strict products, strict pullbacks, strict equalizers, and so on.  Of these, strict products (including terminal objects) are non-evil, hence give bicategorical products as well, while all others such as pullbacks and equalizers tend to be evil.

* Any ordinary limit can also be made into a bicategorical limit by making everything happen up to isomorphism.  Thus, a bicategorical pullback is a square that commutes up to specified isomorphism, with a universal property expressed by an equivalence of categories.

As mentioned above, adding **pseudo** in front of an ordinary limit has a precise meaning: it means that all the triangles in the limit cone now commute up to specified isomorphism, and the universal property is still expressed by an isomorphism of categories.  In particular, there is still a specified projection to _each_ object in the diagram.  For example:

* The **pseudo-pullback** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $P$ equipped with projections $p:P\to A$, $q:P\to B$, and $r:P\to C$ and 2-cell isomorphisms $f p \cong r$ and $g q \cong r$.

* The **pseudo-equalizer** of a pair of arrows $f,g:A\rightrightarrows B$ is a universal object $E$ equipped with morphisms $h:E\to A$ and $k:E\to B$ and 2-cell isomorphisms $f h \cong k$ and $g h \cong k$.

These are to be distinguished from:

* The **(strict) iso-comma object** of $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $P$ equipped with projections $p:P\to A$ and $q:P\to B$ and a 2-cell isomorphism $f p \cong g q$.

* The **(strict) iso-inserter** of $f,g:A\rightrightarrows B$ is a universal object $E$ equipped with a morphism $e:E\to A$ and a 2-cell isomorphism $f e \cong g e$.

The pseudo-pullback, pseudo-equalizer, iso-comma object, and iso-inserter are all strict Cat-weighted limits; their universal property is expressed by an isomorphism of categories.  Usually the pseudo-pullback and iso-comma object are not isomorphic, and likewise the pseudo-equalizer and iso-inserter are not isomorphic.  However, both the pseudo-pullback and iso-comma object are non-evil and represent a *bicategorical* pullback; therefore they are _equivalent_ when they both exist.  Likewise, the pseudo-equalizer and iso-inserter both represent a "bicategorical equalizer," and are equivalent when they both exist.

If one is mostly interested in bicategorical limits, then there is little harm in using "pseudo-pullback" to mean "iso-comma object" or "bicategorical pullback," as is common in the literature.  However, with _lax_ limits the situation is more serious.  Speaking precisely, in the **lax** version of a limit, the triangles in the limiting cone are made to commute up to a specified transformation in one direction, but there are still specified projections to _each_ object in the diagram.  For example:

* The **lax limit of an arrow** $f:A\to B$ is a universal object $L$ equipped with projections $p:L\to A$ and $q:L\to B$ and a 2-cell $f p \to q$.

* The **lax pullback** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $P$ equipped with projections $p:P\to A$, $q:P\to B$, $r:P\to C$, and 2-cells $f p \to r$ and $g q \to r$.

In particular, the lax pullback is quite different from the following more common limit.

* The **comma object** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a generalization of the [[comma category]] in $Cat$; it is a universal object $(f/g)$ equipped with projections $p:(f/g)\to A$ and $q:(f/g)\to B$ and a 2-cell $f p \to g q$.

Lax limits, including lax pullbacks, and comma objects both come in strict versions and bicategorical versions, and as they are non-evil, their strict cases are a special case of their bicategorical ones.  However, even in their bicategorical forms, the lax pullback and comma object are distinct.  Usually the comma object is the more important one, but calling it a "lax pullback" should be avoided.  For example, there are some (weak) 2-categories known to admit all lax (or oplax) limits, but this does not, in general, imply that they admit comma objects.

Here are some more important examples of 2-categorical limits, all of which come in strict and weak forms and are non-evil.

* The **inserter** of a pair of parallel arrows $f,g:A \;\rightrightarrows\; B$ is a universal object $I$ equipped with a map $i:I\to A$ and a 2-cell $f i \to g i$.

* The **equifier** of a pair of parallel 2-cells $\alpha,\beta: f\to g: A\to B$ is a universal object $E$ equipped with a map $e:E\to A$ such that $\alpha e = \beta e$.

* The **inverter** of a 2-cell $\alpha:f\to g:A\to B$ is a universal object $V$ with a map $v:V\to A$ such that $\alpha v$ is invertible.

* The **[[power]]** of an object $A$ by a category $C$ is a universal object $A^C$ equipped with a functor $C\to K(A^C,A)$.

* [[descent object|Descent objects]] are another important example.


## Finite Limits ##

A 2-categorical limit is called **finite** if its diagram shape and its [[weighted limit|weight]] are both [[finitely presentable object|finitely presentable]].  Pullbacks, comma objects, inserters, equifiers, and so on are all finite limits, as are powers by any finitely presented category.  All finite limits can be constructed from pullbacks, a terminal object, and powers with the arrow category $(\cdot\to\cdot)$.


#In terms of homotopy limits (?)#

+--{.query}

[[Urs Schreiber|Urs]]: I'd enjoy the (re)formulation in terms of [[homotopy limit]]s using the [[folk model structure]] on $2Cat$. I'll try a bit myself to write something about that here eventually, but if any experts can speed ahead and provide some comments here, it would be appreciated.

=--

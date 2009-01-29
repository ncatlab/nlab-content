# Idea #

In general, a _2-limit_ is the sort of limit appropriate in a (weak) [[2-category]].  See [[2-limit]] for details.  However, when we happen to be in a [[strict 2-category]] we also have another notion at our disposal.  Since strict 2-categories are just categories  [[enriched category|enriched]] over [[Cat]], we can apply the usual notions of [[weighted limit]]s in enriched categories verbatim.  (Historically, these were called _2-limits_ while the up-to-isomorphism limits were called _bilimits_.)

Because enriched category theory doesn't know anything about the 2-categorical nature of Cat, the resulting limits can have cones that commute strictly and have universal properties expressed by isomorphisms of categories; thus they can be [[evil]].  However, such strict limits often turn out to be technically useful even if we are fundamentally only interested in the "up-to-isomorphism" notions, since in many strict 2-categories we can use tools of enriched category theory to construct strict 2-limits, and then by considering suitably non-evil strict limits we can construct "up-to-isomorphism" 2-limits.  This is reminiscent of the use of strict structures in [[homotopy theory]] as a tool to get at weak ones, and in fact a precise comparison can be made (see below).


# Classification #

* A **strict 2-limit** (or just _strict limit_) in a strict 2-category is just a [[Cat]]-enriched (weighted) limit.  This means that its cones must commute strictly (although weakness can be built in via the weighting, see below), and its universal property is expressed by an isomorphism of categories.

+--{.query}
_Mike_: Can anyone think of good terminology for these next two?  Historically they are just called "pseudo limit" and "lax limit" but if we are using "limit" or "2-limit" for the up-to-isomorphism notion and thus "lax limit" for the lax and up-to-isomorphism notion, what should we call the lax and up-to-identity notion?  "lax strict limit"?
=--

* A **pseudo limit**  is a limit whose cones commute up to coherent 2-cell isomorphism, but whose universal property can still be expressed by an _isomorphism_ of categories.  For any weight $W$, there is another weight $W'$ (a [[cofibrant replacement]] of $W$) such that pseudo $W$-weighted limits are equivalent to strict $W'$-weighted ones.  The idea is that $W'$ includes explicitly all the extra isomorphisms in a pseudo $W$-cone.  Since any isomorphism of categories is _a fortiori_ an equivalence of categories, any pseudo limit is also an up-to-isomorphism 2-limit.

* A **lax limit** is a limit whose cones commute only up to a coherent transformation in one direction, but again whose universal property is expressed by an isomorphism.  Likewise we have **oplax limits** where the transformation goes in the other direction.  Lax and oplax limits can also be rephrased as strict limits for a different weight.  As in the pseudo case, any (op)lax limit is also an (op)lax bicategorical limit.

More generally, any non-[[evil]] limit (one which doesn't demand equality of objects) can still exist even when everything becomes weak.  Two formal versions of this statement involve [[flexible limit]]s and the more restrictive [[PIE-limit]]s.  In particular, any strict flexible limit is also an up-to-isomorphism 2-limit.  Since pseudo limits are PIE-limits, it follows that any strict 2-category which admits PIE-limits also admits all up-to-isomorphism 2-limits, even if it fails to admit some (evil) strict 2-categorical limits.  The category of algebras and pseudo morphisms for any [[2-monad]], such as [[MonCat]], is a good example of a 2-category having strict PIE-limits but not all strict limits.


# Examples #

Any ordinary limit can be made into a strict 2-categorical limit simply by boosting up its ordinary universal property (a bijection of sets) to an isomorphism of hom-categories.  Thus we have strict products, strict pullbacks, strict equalizers, and so on.  Of these, strict products (including terminal objects) are non-evil, while others such as pullbacks and equalizers tend to be evil.

* For example, a strict terminal object is an object 1 such that $K(X,1)$ is _isomorphic_ to the [[terminal category]], for any object $X$.

* Likewise, a strict product of $A$ and $B$ is an object $A\times B$ with projections $p:A\times B\to A$ and $q:A\times B\to B$ such that (1) given any $f:X\to A$ and $g:X\to B$, there exists a unique $h:X\to A\times B$ such thath $p h = f$ and $q h = g$ (equal, not isomorphic), and (2) given any $h,k:X\to A\times B$ and $\alpha: p h \to p k$ and $\beta:q h \to q k$, there exists a unique $\gamma:h\to k$ such that $p\gamma = \alpha$ and $q\gamma =\beta$.

As mentioned above, adding **pseudo** in front of an ordinary limit has a precise meaning: it means that all the triangles in the limit cone now commute up to specified isomorphism, and the universal property is still expressed by an isomorphism of categories.  In particular, there is still a specified projection to _each_ object in the diagram.  For example:

* The **pseudo-pullback** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $P$ equipped with projections $p:P\to A$, $q:P\to B$, and $r:P\to C$ and 2-cell isomorphisms $f p \cong r$ and $g q \cong r$.

* The **pseudo-equalizer** of a pair of arrows $f,g:A\rightrightarrows B$ is a universal object $E$ equipped with morphisms $h:E\to A$ and $k:E\to B$ and 2-cell isomorphisms $f h \cong k$ and $g h \cong k$.

These are to be distinguished from:

* The **iso-comma object** of $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $P$ equipped with projections $p:P\to A$ and $q:P\to B$ and a 2-cell isomorphism $f p \cong g q$.

* The **iso-inserter** of $f,g:A\rightrightarrows B$ is a universal object $E$ equipped with a morphism $e:E\to A$ and a 2-cell isomorphism $f e \cong g e$.

The pseudo-pullback, pseudo-equalizer, iso-comma object, and iso-inserter are all strict Cat-weighted limits; their universal property is expressed by an isomorphism of categories.  Usually the pseudo-pullback and iso-comma object are not isomorphic, and likewise the pseudo-equalizer and iso-inserter are not isomorphic.  However, both the pseudo-pullback and iso-comma object are non-evil and represent an up-to-isomorphism pullback; therefore they are _equivalent_ when they both exist.  Likewise, the pseudo-equalizer and iso-inserter both represent an up-to-isomorphism equalizer, and are equivalent when they both exist.

If one is mostly interested in up-to-isomorphism limits, then there is little harm in using "pseudo-pullback" to mean "iso-comma object" or "pullback," as is common in the literature.  However, with _lax_ limits the situation is more serious.  Speaking precisely, in the **lax** version of a limit, the triangles in the limiting cone are made to commute up to a specified transformation in one direction, but there are still specified projections to _each_ object in the diagram.  For example:

* The **lax limit of an arrow** $f:A\to B$ is a universal object $L$ equipped with projections $p:L\to A$ and $q:L\to B$ and a 2-cell $f p \to q$.

* The **lax pullback** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $P$ equipped with projections $p:P\to A$, $q:P\to B$, $r:P\to C$, and 2-cells $f p \to r$ and $g q \to r$.

In particular, the lax pullback is quite different from the following more common limit.

* The **comma object** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a generalization of the [[comma category]] in $Cat$; it is a universal object $(f/g)$ equipped with projections $p:(f/g)\to A$ and $q:(f/g)\to B$ and a 2-cell $f p \to g q$.

Lax limits, including lax pullbacks, and comma objects both come in strict versions and non-strict versions, and as they are non-evil, their strict cases are a special case of their non-strict ones.  However, even in their non-strict forms, the lax pullback and comma object are distinct.  Usually the comma object is the more important one, but calling it a "lax pullback" should be avoided.  For example, there are some (weak) 2-categories known to admit all lax (or oplax) limits, but this does not, in general, imply that they admit comma objects.

Here are some more important examples of 2-categorical limits, all of which come in strict and weak forms and are non-evil.

* The **inserter** of a pair of parallel arrows $f,g:A \;\rightrightarrows\; B$ is a universal object $I$ equipped with a map $i:I\to A$ and a 2-cell $f i \to g i$.

* The **equifier** of a pair of parallel 2-cells $\alpha,\beta: f\to g: A\to B$ is a universal object $E$ equipped with a map $e:E\to A$ such that $\alpha e = \beta e$.

* The **inverter** of a 2-cell $\alpha:f\to g:A\to B$ is a universal object $V$ with a map $v:V\to A$ such that $\alpha v$ is invertible.

* The **[[power]]** of an object $A$ by a category $C$ is a universal object $A^C$ equipped with a functor $C\to K(A^C,A)$.




# References #

* Street, "Limits indexed by category-valued 2-functors"

* Kelly, "Elementary observations on 2-categorical limits"

* Lack, [A 2-categories companion](http://arxiv.org/abs/math.CT/0702535)

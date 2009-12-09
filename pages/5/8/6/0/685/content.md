# Idea #

A **2-limit** is the type of [[limit]] that is appropriate in a (weak) [[2-category]].  There are three notable changes when passing from ordinary 1-limits to 2-limits:

1. Since in a 2-category we avoid [[evil]], the "cones" in a 2-limit are required to commute only up to isomorphism.

1. The universal property of the limit is expressed by an [[equivalence of categories]] rather than a bijection of sets.  This means that (1) every other cone over the diagram that commutes up to isomorphism factors through the limit, up to isomorphism, and (2) every transformation _between_ cones also factors through a 2-cell in the limit.  We will give some examples below.

1. Since 2-categories are [[enriched category|enriched]] over [[Cat]] (this is precise in the [[strict 2-category|strict]] case, and [[bicategory|weakly]] true otherwise), Cat-[[weighted limit]]s become important.  This means that both the diagrams we take limits of and the shape of "cones" that limits represent can involve 2-cells as well as 1-cells.


# $2$-colimits

Everything below applies dually to __$2$-colimits__, the higher analogues of [[colimits]].  (But somebody might want to make a separate page that gives appropriate examples of these.)


# Strictness and terminology #

In a [[strict 2-category]], one can also consider [[strict 2-limit|strict 2-limits]], which are precisely Cat-weighted limits in the sense of ordinary [[enriched category]] theory.  In a strict 2-category these "strict" limits are often technically useful in constructing the "up-to-isomorphism" 2-limits we consider here.  See [[strict 2-limit]] for details.

When we know we are working in a (weak) 2-category, the only type of limit that makes sense is a 2-limit.  Therefore, we usually call these simply "limits."  To emphasize the distinction with the strict 2-limits in a strict 2-category, the "up-to-isomorphism" 2-limits were historically often called _bilimits_ (by analogy with [[bicategory]] for "weak 2-category").  However, this terminology is somewhat unfortunate, not only because it doesn't generalize well to $n$, but because it leads to words like "biproduct," which also has the [[biproduct|completely unrelated meaning]] of an object that is both a product and a coproduct (which is common in [[additive category|additive categories]]).

Unfortunately, we probably shouldn't use "weak limit" to emphasize the "up-to-isomorphism" nature of these limits, because that also has the [[weak limit|completely unrelated meaning]] of an object in a 1-category satisfying the existence, but not the uniqueness property of an ordinary limit.


# Examples #

Any ordinary type of limit can be "2-ified" by boosting its ordinary universal property up to a 2-categorical one.  In the following examples we work in a 2-category $K$.

* A **[[terminal object]]** in $K$ is an object 1 such that $K(X,1)$ is equivalent to the [[terminal category]] for any object $X$.  This means that for any $X$ there is a morphism $X\to 1$ and for any two morphisms $f,g:X\to 1$ there is a unique isomorphism $f\cong g$.

* A **[[product]]** of two objects $A,B$ in $K$ is an object $A\times B$ together with a natural equivalence of categories $K(X,A\times B) \simeq K(X,A)\times K(X,B)$.  This means that we have projections $p:A\times B\to A$ and $q:A\times B\to B$ such that (1) for any $f:X\to A$  and $g:X\to B$, there exists an $h:X\to A\times B$ and isomorphisms $p h\cong f$ and $q h\cong g$, and (2) for any $h,k:X\to A\times B$ and 2-cells $\alpha:p h \to p k$ and $\beta: q h \to q k$, there exists a unique $\gamma:h \to k$ such that $p \gamma = \alpha$ and $q \gamma = \beta$.

* A **[[pullback]]** of a [[co-span]] $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ consists of an object $A\times_C B$ and projections $p:A\times_C B\to A$ and $q:A\times_C B\to B$ together with an isomorphism $\phi:f p \cong g q$, such that (1) for any $m:X\to A$ and $n:X\to B$ with an isomorphism $\psi:f m \cong g n$, there exists an $h:X\to A\times_C B$ and isomorphisms $\alpha:p h \cong m$ and $\beta:q h \cong n$ such that $g\beta . \phi h . f \alpha = \psi$, and (2) a suitable condition on 2-cells as well.  This is sometimes called the _pseudo-pullback_ but that term more properly refers to a particular [[strict 2-limit]].

* An **[[equalizer]]** of $f,g:A\to B$ consists of an object $E$ and a morphism $e:E\to A$ together with an isomorphism $f e \cong g e$, which is universal in a sense the reader should now be able to write down.  This is sometimes called the _pseudo-equalizer_ but that term more properly refers to a particular [[strict 2-limit]].  Note that frequently, such as in the construction of all limits from basic ones, equalizers need to be replaced by [[descent object]]s.

There are also various important types of 2-limits that involve 2-cells in the diagram shape or in the weight, and hence are not just "boosted-up" versions of 1-limits.

* The **[[comma object]]** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $(f/g)$ and projections $p:(f/g)\to A$ and $q:(f/g)\to B$ together with a transformation (not an isomorphism) $f p \to g q$.  In [[Cat]], comma objects are [[comma category|comma categories]].  Comma objects are sometimes called _lax pullbacks_ but that term more properly refers to the lax version of a pullback; see "lax limits" below.

* The **[[inserter]]** of a pair of parallel arrows $f,g:A \;\rightrightarrows\; B$ is a universal object $I$ equipped with a map $i:I\to A$ and a 2-cell $f i \to g i$.

* The **[[equifier]]** of a pair of parallel 2-cells $\alpha,\beta: f\to g: A\to B$ is a universal object $E$ equipped with a map $e:E\to A$ such that $\alpha e = \beta e$.

* The **[[inverter]]** of a 2-cell $\alpha:f\to g:A\to B$ is a universal object $V$ with a map $v:V\to A$ such that $\alpha v$ is invertible.

* The **[[power]]** of an object $A$ by a category $C$ is a universal object $A^C$ equipped with a functor $C\to K(A^C,A)$.  Of particular importance is the case when $C$ is the [[walking arrow]] $\mathbf{2}$.


# Lax limits #

A **lax limit** is like a 2-limit, except that the triangles in the definition of a cone are required only to commute up to a specified _transformation_, not necessarily an isomorphism.  The lax limit of one diagram can always be converted to an ordinary 2-limit by changing the weight.

* Lax terminal objects and lax products are the same as ordinary ones, since there are no commutativity conditions on the cones.

* The **lax limit of an arrow** $f:A\to B$ is a universal object $L$ equipped with projections $p:L\to A$ and $q:L\to B$ and a 2-cell $f p \to q$.  Note that this is equivalent to a comma object $(f/1_B)$.

* The **lax pullback** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $P$ equipped with projections $p:P\to A$, $q:P\to B$, $r:P\to C$, and 2-cells $f p \to r$ and $g q \to r$.

Note that lax pullbacks are _not_ the same as comma objects.  In general comma objects are much more useful, but there are 2-categories that admit all lax limits but do not admit comma objects, so using "lax pullback" to mean "comma object" can be misleading.


# Finite Limits #

A 2-limit is called **finite** if its diagram shape and its weight are both "finitely presentable" in a suitable sense.  Pullbacks, comma objects, inserters, equifiers, and so on are all finite limits, as are powers by any finitely presented category.  All finite limits can be constructed from pullbacks, a terminal object, and powers with $\mathbf{2}$.


# References #

* Street, "Limits indexed by category-valued 2-functors"

* Kelly, "Elementary observations on 2-categorical limits"

* Street, "Fibrations in Bicategories" and correction.

* Lack, [A 2-categories companion](http://arxiv.org/abs/math.CT/0702535)


[[!redirects 2-categorical limit]]
[[!redirects 2-categorial limit]]
[[!redirects 2-colimit]]
[[!redirects 2-limits]]
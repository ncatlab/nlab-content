
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea 

In general, a _[[2-limit]]_ is the sort of [[limit]] appropriate in a (weak) [[2-category]].  However, when we happen to be in a [[strict 2-category]] we also have another notion at our disposal:

Since strict 2-categories are equivalently categories [[enriched category|enriched]] over [[Cat]] (i.e. over the [[very large category|very large]] [[1-category]] of [[categories]] with [[functors]] between them), we can apply the usual notions of [[weighted limits]] in [[enriched categories]] verbatim to speak of certain 2-limits ([Street 1976](#Street76), [Kelly 1989](#Kelly89)). Here we refer to these [[Cat]]-[[enriched category|enriched]] [[weighted limits]] as *strict 2-limits*.  (Beware that, historically, these were called _2-limits_ while the properly 2-category-theoretic limits were called _bilimits_.)

Because [[enriched category theory]] doesn't know anything about the [[2-category theory|2-category theoretic]] nature of [[Cat]], the resulting *strict 2-limits* can have [[cones]] that [[commuting diagram|commute]] strictly and have [[universal properties]] expressed by [[isomorphisms]] of categories (instead of [[equivalences of categories]]); thus they can violate the [[2-category theory|2-category theoretic]] [[principle of equivalence]].  

However, strict 2-limits often turn out to be technically useful even if one is ultimately interested only in weak 2-limits, since in many situations strict 2-limits may serve as stepping stones for the constrction of weak [[2-limits]].  This is reminiscent of the use of strict structures in [[homotopy theory]] as a tool to get at weak ones, and in fact a precise comparison can be made (see below).


## Classification 

By a **limit** we will mean the fully 2-categorical notion described at [[2-limit]], in which cones [[commuting diagram|commute]] up to invertible [[2-morphisms]] and the [[universal property]] is expressed by an [[equivalence of categories]].

+-- {: .query}
It just occured to me that 'strict initial object' conflicts with this.  But unlike 'weak limit', that doesn't generalise very far.

Heh, you're right.  I suppose we could try calling strict initial objects _stable initial objects_, which would make more sense anyway since they are really the 0-ary version of a stable coproduct.  But there's probably not likely to be any real confusion created by the two uses of strict.
=--

* A **strict 2-limit** (or just _strict limit_) in a strict 2-category is just a [[Cat]]-enriched [[weighted limit]].  This means that its cones must commute strictly (although weakness can be built in via the weighting, see below), and its universal property is expressed by an isomorphism of categories.  Note that a strict limit is not necessarily a limit, because it may violate the [[principle of equivalence]].  (cf. [[red herring principle]].)

* A **pseudo limit** (or _strict pseudo limit_ if it is necessary to emphasize the strictness) is a limit whose cones commute up to coherent 2-cell isomorphism, but whose universal property can still be expressed by an _isomorphism_ of categories.  For any weight $W$, there is another weight $W'$ (a [[cofibrant replacement]] of $W$) such that pseudo $W$-weighted limits are equivalent to strict $W'$-weighted ones.  The idea is that $W'$ includes explicitly all the extra isomorphisms in a pseudo $W$-cone.  Since any isomorphism of categories is _a fortiori_ an equivalence of categories, any pseudo limit is also a limit.

* A **strict lax limit** is a limit whose cones commute only up to a coherent transformation in one direction, but again whose universal property is expressed by an isomorphism.  Likewise we have **strict oplax limits** where the transformation goes in the other direction.  Strict lax and oplax limits can also be rephrased as strict (non-lax) limits for a different weight.  As in the pseudo case, any strict (op)lax limit is also an (op)lax limit.

More generally, any strict limit respects the [[principle of equivalence]] (one which doesn't demand equality of objects) will also be a limit.  Two formal versions of this statement involve [[flexible limit]]s and the more restrictive [[PIE-limit]]s.  In particular, any strict flexible limit is also a limit.  Since pseudo limits are PIE-limits, it follows that any strict 2-category which admits (strict) PIE-limits also admits all limits, even if it fails to admit some equivalence-violatiing strict limits.  The category of algebras and pseudo morphisms for any [[2-monad]], such as [[MonCat]], is a good example of a 2-category having strict PIE-limits but not all strict limits.


## Pseudo limits and homotopy limits 

If there is a [[model category]] structure on the 1-category underlying the given strict 2-category $C$, then in addition to whatever 2-categorical notions of limit exist in $C$, there is the notion of [[homotopy limit]]s in $C$.  If $C$ is a [[model 2-category]] with the "trivial" or "natural" model structure constructed in (Lack 2006), then these two notions coincide (Gambino 2007).  For example, this is the case in [[Cat]] and [[Grpd]], so the examples listed at [[homotopy limit]] are also examples of pseudo limits.  In general, homotopy limits in a model 2-category give (non-strict) limits in its "homotopy 2-category."


## Examples 


Any ordinary 1-limit can be made into a strict 2-limit simply by boosting up its ordinary universal property (a bijection of sets) to an isomorphism of hom-categories.  Thus we have strict [[products]], strict [[pullbacks]], strict [[equalizers]], and so on.  Of these, strict products (including [[terminal objects]]) respect the 2-category theoretic [[principle of equivalence]] (and thus are also 2-limits), while others such as pullbacks and equalizers tend to violate the 2-category theoretic [[principle of equivalence]].

* For example, a strict terminal object is an object 1 such that $K(X,1)$ is _isomorphic_ to the [[terminal category]], for any object $X$.

* Likewise, a strict product of $A$ and $B$ is an object $A\times B$ with projections $p:A\times B\to A$ and $q:A\times B\to B$ such that (1) given any $f:X\to A$ and $g:X\to B$, there exists a unique $h:X\to A\times B$ such thath $p h = f$ and $q h = g$ (equal, not isomorphic), and (2) given any $h,k:X\to A\times B$ and $\alpha: p h \to p k$ and $\beta:q h \to q k$, there exists a unique $\gamma:h\to k$ such that $p\gamma = \alpha$ and $q\gamma =\beta$.

As mentioned above, adding **pseudo** in front of an ordinary limit has a precise meaning: it means that all the triangles in the limit cone now commute up to specified isomorphism, and the universal property is still expressed by an isomorphism of categories.  In particular, there is still a specified projection to _each_ object in the diagram.  For example:

* The **pseudo [[pullback]]** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $P$ equipped with projections $p:P\to A$, $q:P\to B$, and $r:P\to C$ and 2-cell isomorphisms $f p \cong r$ and $g q \cong r$.

* The **pseudo [[equalizer]]** of a pair of arrows $f,g:A\rightrightarrows B$ is a universal object $E$ equipped with morphisms $h:E\to A$ and $k:E\to B$ and 2-cell isomorphisms $f h \cong k$ and $g h \cong k$.

These are to be distinguished from:

* The **iso-[[comma object]]** of $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $P$ equipped with projections $p:P\to A$ and $q:P\to B$ and a 2-cell isomorphism $f p \cong g q$.

* The **iso-[[inserter]]** of $f,g:A\rightrightarrows B$ is a universal object $E$ equipped with a morphism $e:E\to A$ and a 2-cell isomorphism $f e \cong g e$.

The pseudo pullback, pseudo equalizer, iso-comma object, and iso-inserter are all strict Cat-weighted limits; their universal property is expressed by an isomorphism of categories.  Usually the pseudo pullback and iso-comma object are not isomorphic, and likewise the pseudo equalizer and iso-inserter are not isomorphic.  However, both the pseudo pullback and iso-comma object respect the [[principle of equivalence]] and represent a pullback; therefore they are _equivalent_ when they both exist.  Likewise, the pseudo equalizer and iso-inserter both represent an equalizer, and are equivalent when they both exist.

If one is mostly interested in (non-strict) limits, then there is little harm in using "pseudo pullback" to mean "iso-comma object" or "pullback," as is common in the literature.  However, with _lax_ limits the situation is more serious.  Speaking precisely, in the _lax_ version of a limit, the triangles in the limiting cone are made to commute up to a specified transformation in one direction, but there are still specified projections to _each_ object in the diagram.  For example:

* The **strict lax limit of an arrow** $f:A\to B$ is a universal object $L$ equipped with projections $p:L\to A$ and $q:L\to B$ and a 2-cell $f p \to q$.

* The **strict lax pullback** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $P$ equipped with projections $p:P\to A$, $q:P\to B$, $r:P\to C$, and 2-cells $f p \to r$ and $g q \to r$.


In particular, the strict lax pullback in the following list of examples  is quite different from the following more common limit.

* The **comma object** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a generalization of the [[comma category]] in $Cat$; it is a universal object $(f/g)$ equipped with projections $p:(f/g)\to A$ and $q:(f/g)\to B$ and a 2-cell $f p \to g q$.

Even in their non-strict forms, the lax pullback and comma object are distinct.  Usually the comma object is the more important one, but calling it a "lax pullback" should be avoided.

Here are some more important examples of 2-limits, all of which come in strict and weak forms and respect the [[principle of equivalence]].

* The **[[inserter]]** of a pair of parallel arrows $f,g:A \;\rightrightarrows\; B$ is a universal object $I$ equipped with a map $i:I\to A$ and a 2-cell $f i \to g i$.

* The **[[equifier]]** of a pair of parallel 2-cells $\alpha,\beta: f\to g: A\to B$ is a universal object $E$ equipped with a map $e:E\to A$ such that $\alpha e = \beta e$.

* The **[[inverter]]** of a 2-cell $\alpha:f\to g:A\to B$ is a universal object $V$ with a map $v:V\to A$ such that $\alpha v$ is invertible.

* The **[[power]]** of an object $A$ by a category $C$ is a universal object $A^C$ equipped with a functor $C\to K(A^C,A)$.


## References 

Original articles on Cat-enriched weighted limits:

* {#Street76} [[Ross Street]], _Limits indexed by category-valued 2-functors_, Journal of Pure and Applied Algebra Volume 8, Issue 2, June 1976, Pages 149-181 (<a href="https://doi.org/10.1016/0022-4049(76)90013-X">doi:10.1016/0022-4049(76)90013-X</a>)

* {#Kelly89} [[Max Kelly]], *Elementary observations on 2-categorical limits*, Bulletin of the Australian Mathematical Society, 39(2), 301-317 ([doi:10.1017/S0004972700002781](https://doi.org/10.1017/S0004972700002781), [pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/C14F8C3C46D45BCEC748660630EA7535/S0004972700002781a.pdf/div-class-title-elementary-observations-on-2-categorical-limits-div.pdf))

Review and list of examples:

* {#Lack10} [[Steve Lack]], around Sec. 6.8 in: _A 2-categories companion_,  In: Baez J., May J. (eds.) *[[Towards Higher Categories]]*. The IMA Volumes in Mathematics and its Applications, vol 152. Springer 2010 ([arXiv:math.CT/0702535](http://arxiv.org/abs/math.CT/0702535), [doi:10.1007/978-1-4419-1524-5_4](https://doi.org/10.1007/978-1-4419-1524-5_4))

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], Section 5.3 of: *2-Dimensional Categories*, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))


See also:

* [[Steve Lack]], _Homotopy theoretic aspects of 2-monads_ ([arXiv:math.CT/0607646](http://www.arxiv.org/abs/math.CT/0607646)).

* [[Nicola Gambino]], _Homotopy limits for 2-categories_ ([pdf](http://www1.maths.leeds.ac.uk/~pmtng/Publications/homotopy.pdf))

[[!redirects strict 2-limits]]
[[!redirects strict 2-colimit]]
[[!redirects strict 2-colimits]]

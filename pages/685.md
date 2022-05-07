
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $\infty$-Limits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
----
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

A **2-limit** is the type of [[limit]] that is appropriate in a (weak) [[2-category]]. (Since general 2-categories are often called _[[bicategories]]_, 2-limits are often called _[[bilimits]]_.)

There are three notable changes when passing from ordinary 1-limits to 2-limits:

1. In order to satisfy the [[principle of equivalence]], the "cones" in a 2-limit are required to commute only up to [[2-morphism|2-isomorphism]].

2. The [[universal property]] of the limit is expressed by an [[equivalence of categories]] rather than a [[bijection]] of [[sets]].  This means that 

   1. every other cone over the diagram that commutes up to isomorphism factors through the limit, up to isomorphism, and 

   2. every transformation _between_ cones also factors through a 2-cell in the limit.  We will give some examples below.

3. Since 2-categories are [[enriched category|enriched]] over [[Cat]] (this is precise in the [[strict 2-category|strict]] case, and [[bicategory|weakly]] true otherwise), $Cat$-[[weighted limit]]s become important.  This means that both the diagrams we take limits of and the shape of "cones" that limits represent can involve $2$-cells as well as $1$-cells.


## Definition

Let $K$ and $D$ be [[2-categories]], and $J\colon D\to Cat$ and $F\colon D\to K$ be [[2-functors]].  A **$J$-weighted (2-)limit of $F$** is an object $L\in K$ equipped with a [[pseudonatural equivalence]]
$$ K(X,L) \simeq [D,Cat](J,K(X,F-)). $$
where $[D,Cat]$ denotes the 2-category of [[2-functors]] $D\to Cat$, [[pseudonatural transformations]] between them, and [[modifications]] between those.

A 2-limit in the [[opposite 2-category]] $K^{op}$ is called a **2-colimit** in $K$.  Everything below applies dually to 2-colimits, the higher analogues of [[colimits]].  (But somebody might want to make a separate page that gives appropriate examples of these.)


### Strictness and terminology 
 {#Terminology}

If $K$ and $D$ are [[strict 2-categories]], $J$ and $F$ are [[strict 2-functors]], and if we replace this pseudonatural equivalence by a (strictly 2-natural) isomorphism *and* the 2-category $[D,Cat]$ by the 2-category $[D,Cat]_{strict}$ of strict 2-functors and strict 2-natural transformations, then we obtain the definition of a **[[strict 2-limit]]**.  This is precisely a Cat-weighted limit in the sense of ordinary [[enriched category]] theory.  See [[strict 2-limit]] for details.

On the other hand, if $K$, $D$, $J$, and $F$ are strict as above, and we replace the equivalence by an isomorphism but keep the weak meaning of $[D,Cat]$, then we obtain the notion of a **strict pseudolimit**.  Strict pseudolimits are, in particular, 2-limits, whereas strict 2-limits are not always (although some, such as [[PIE-limits]] and [[flexible limits]], are).  In a strict 2-category, these types of strict limits are often technically useful in constructing the "up-to-isomorphism" 2-limits we consider here.

When we know we are working in a (weak) 2-category, the only type of limit that makes sense is a (non-strict) 2-limit.  Therefore, we usually call these simply "limits."  To emphasize the distinction with the strict 2-limits in a strict 2-category, the "up-to-isomorphism" 2-limits were historically often called _bilimits_ (by analogy with [[bicategory]] for "weak 2-category").  However, this terminology is somewhat unfortunate, not only because it doesn't generalize well to $n$, but because it leads to words like "biproduct," which also has the [[biproduct|completely unrelated meaning]] of an object that is both a product and a coproduct (which is common in [[additive category|additive categories]]).

Unfortunately, we probably shouldn't use "weak limit" to emphasize the "up-to-isomorphism" nature of these limits, because that also has the [[weak limit|completely unrelated meaning]] of an object in a 1-category satisfying the existence, but not the uniqueness property of an ordinary limit.


## Examples

### 2-limits over diagrams of special shape

Any ordinary type of limit can be "2-ified" by boosting its ordinary universal property up to a 2-categorical one.  In the following examples we work in a 2-category $K$.

* A **[[terminal object]]** in $K$ is an object 1 such that $K(X,1)$ is equivalent to the [[terminal category]] for any object $X$.  This means that for any $X$ there is a morphism $X\to 1$ and for any two morphisms $f,g:X\to 1$ there is a unique morphism $f\to g$, and this morphism is an isomorphism.

* A **[[product]]** of two objects $A,B$ in $K$ is an object $A\times B$ together with a natural equivalence of categories $K(X,A\times B) \simeq K(X,A)\times K(X,B)$.  This means that we have projections $p:A\times B\to A$ and $q:A\times B\to B$ such that (1) for any $f:X\to A$  and $g:X\to B$, there exists an $h:X\to A\times B$ and isomorphisms $p h\cong f$ and $q h\cong g$, and (2) for any $h,k:X\to A\times B$ and 2-cells $\alpha:p h \to p k$ and $\beta: q h \to q k$, there exists a unique $\gamma:h \to k$ such that $p \gamma = \alpha$ and $q \gamma = \beta$.

* A **[[pullback]]** of a [[co-span]] $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ consists of an object $A\times_C B$ and projections $p:A\times_C B\to A$ and $q:A\times_C B\to B$ together with an isomorphism $\phi:f p \cong g q$, such that (1) for any $m:X\to A$ and $n:X\to B$ with an isomorphism $\psi:f m \cong g n$, there exists an $h:X\to A\times_C B$ and isomorphisms $\alpha:p h \cong m$ and $\beta:q h \cong n$ such that $g\beta . \phi h . f \alpha^{-1} = \psi$, and (2) given any two morphisms $h,k:X\to A\times_C B$ and 2-cells $\mu:p h \to p k$ and $\nu:q h \to q k$ such that $f \mu = g \nu$ (modulo the given isomorphism $f p \cong g q$), i.e., $\phi k . f\mu = g\nu . \phi h$, there exists a unique 2-cell $\gamma:h\to k$ such that $p \gamma = \mu$ and $q \gamma = \nu$.  This is sometimes called the _pseudo-pullback_ but that term more properly refers to a particular [[strict 2-limit]].

* An **[[equalizer]]** of $f,g:A\to B$ consists of an object $E$ and a morphism $e:E\to A$ together with an isomorphism $f e \cong g e$, which is universal in a sense the reader should now be able to write down.  This is sometimes called the _pseudo-equalizer_ but that term more properly refers to a particular [[strict 2-limit]].  Note that frequently, such as in the construction of all limits from basic ones, equalizers need to be replaced by [[descent object]]s.

There are also various important types of 2-limits that involve 2-cells in the diagram shape or in the weight, and hence are not just "boosted-up" versions of 1-limits.

* The **[[comma object]]** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $(f/g)$ and projections $p:(f/g)\to A$ and $q:(f/g)\to B$ together with a transformation (not an isomorphism) $f p \to g q$.  In [[Cat]], [[comma objects]] are [[comma category|comma categories]].  Comma objects are sometimes called _lax pullbacks_ but that term more properly refers to the lax version of a pullback; see "lax limits" below.

* The **[[inserter]]** of a pair of parallel arrows $f,g:A \;\rightrightarrows\; B$ is a universal object $I$ equipped with a map $i:I\to A$ and a 2-cell $f i \to g i$.

* The **[[equifier]]** of a pair of parallel 2-cells $\alpha,\beta: f\to g: A\to B$ is a universal object $E$ equipped with a map $e:E\to A$ such that $\alpha e = \beta e$.

* The **[[inverter]]** of a 2-cell $\alpha:f\to g:A\to B$ is a universal object $V$ with a map $v:V\to A$ such that $\alpha v$ is invertible.

* The **[[power]]** of an object $A$ by a category $C$ is a universal object $A^C$ equipped with a functor $C\to K(A^C,A)$.  Of particular importance is the case when $C$ is the [[walking arrow]] $\mathbf{2}$.


### Finite 2-Limits 

A 2-limit is called **finite** if its diagram shape and its weight are both "finitely presentable" in a suitable sense (defined in terms of [[computads]]; see [Street's article](#StreetLimitsIndexed) _Limits indexed by category-valued 2-functors_ ).  Pullbacks, comma objects, inserters, equifiers, and so on are all finite limits, as are powers by any finitely presented category.  All finite limits can be constructed from pullbacks, a terminal object, and powers with $\mathbf{2}$.


### $(2,1)$-limits
  {#(2,1)limit}

If the ambient [[2-category]] is in fact a [[(2,1)-category]] in that all [[2-morphism]]s are invertible then there is a rich set of tools available for handling the 2-limits in this context. We may say **$(2,1)$-limits** and **$(2,1)$-colimits** in this case.

These are then a special case of the more general [[(∞,1)-limit]]s and [[(∞,1)-colimit]]s in a [[(∞,1)-category]]. A [[(2,1)-category]] is a special case of an [[(∞,1)-category]].

Traditionally, [[(∞,1)-limit]]s are best known in terms of the presentation of $(\infty,1)$-catgeories by [[categories with weak equivalences]] in general and [[model categories]] in particular.  (2,1)-limits can often also be viewed in this way.  The corresponding presentation of the $(\infty,1)$-limits / $(2,1)$-limits is called **[[homotopy limit]]s** and **[[homotopy colimit]]s**.

For instance 2-limits in the [[(2,1)-category]] [[Grpd]] of [[groupoid]]s, [[functor]]s and (necessarily) [[natural isomorphism]]s. Are equivalently computed as [[homotopy limit]]s in the [[model structure on simplicial sets]] $sSet_{Quillen}$ of diagrams of [[1-truncated]] [[Kan complex]]es. (The equivalence of homotopy limits with $(\infty,1)$-limits is discussed at [[(∞,1)-limit]]).

Or for instance, more generally, the 2-limits in any [[(2,1)-sheaf]](=[[stack]]) [[(2,1)-topos]] may be computed as [[homotopy limit]]s in a [[model structure on simplicial presheaves]] over the given [[(2,1)-site]] of diagrams of [[1-truncated]] [[simplicial presheaves]]. This includes as examples [[big topos|big (2,1)-toposes]] such as those over the large sites [[Top]] or [[SmoothMfd]] where computations with [[topological groupoid]]s/[[topological stack]]s, [[Lie groupoid]]s/[[differentiable stack]]s etc. take place.


### Lax limits
{#lax}

A **lax limit** can be defined like a 2-limit, except that the triangles in the definition of a cone are required only to commute up to a specified _transformation_, not necessarily an isomorphism.  In other words, in place of the 2-category $[D,Cat]$ we use the 2-category $[D,Cat]_l$ whose morphisms are [[lax natural transformations]]; thus the lax limit $L$ of a diagram $F$ weighted by $J$ is equipped with a universal lax natural transformation $J\to K(L,F-)$.

This may look like a different concept, but in fact, for any weight $J$ there is another weight $Q_l(J)$ such that lax $J$-weighted limits are the same as $Q_l(J)$-weighted 2-limits.  Here $Q_l$ is the [[lax morphism classifier]] for 2-functors.  Therefore, lax limits are really a special case of 2-limits.  Similarly, **oplax limits**, in which we use oplax natural transformations, are also a special case of 2-limits.

There is a further simplification of lax limits in the case of "conical" lax limits where the weight $J=\Delta 1$ is constant at the [[terminal category]].  In this case, it is easy to check that a lax natural transformation $\Delta 1 \to K(X,F-)$ is the same as a lax natural transformation $\Delta X \to F$.  Thus, a conical lax limit of $F$ is a representing object for such lax transformations.

Here are some examples.

* Lax terminal objects and lax products are the same as ordinary ones, since there are no commutativity conditions on the cones.

* The **lax limit of an arrow** $f:A\to B$ is a universal object $L$ equipped with projections $p:L\to A$ and $q:L\to B$ and a 2-cell $f p \to q$.  Note that this is equivalent to a comma object $(f/1_B)$.

* The **lax pullback** of a cospan $A \overset{f}{\to} C \overset{g}{\leftarrow} B$ is a universal object $P$ equipped with projections $p:P\to A$, $q:P\to B$, $r:P\to C$, and 2-cells $f p \to r$ and $g q \to r$.

Note that lax pullbacks are _not_ the same as [[comma objects]].  In general comma objects are much more useful, but there are 2-categories that admit all lax limits but do not admit comma objects, so using "lax pullback" to mean "comma object" can be misleading.

A **lax colimit** in $K$ is, of course, a lax limit in $K^{op}$.  Thus, it is a representing object for lax natural transformations $J \to K(F-,L)$.  There is a subtlety here, however, because in the case $J=\Delta 1$, a lax natural transformation $\Delta 1 \to K(F-,L)$ is the same as an *oplax* natural transformation $F \to \Delta L$.  Thus, it is easy to mistakenly say "lax colimit" when one really means "oplax colimit" and vice versa.

+-- {: .un_remark}
###### Remark
With this in mind, one might be tempted to switch the meanings of "lax colimit" and "oplax colimit", but there is a good reason not to.  Recall that a lax $J$-weighted limit is the same as an ordinary $Q_l(J)$-weighted limit.  Standard terminology in enriched category theory is that a $W$-weighted colimit in an enriched category $K$ is the same as a $W$-weighted limit in $K^{op}$, and indeed in that generality there is no other option.  Thus, a lax $J$-weighted colimit in $K$ should be an ordinary $Q_l(J)$-weighted colimit in $K$, hence a $Q_l(J)$-weighted limit in $K^{op}$, and thus a lax $J$-weighted limit in $K^{op}$.
=--

Here are some examples of lax and oplax colimits:

* A [[Kleisli object]] is a lax colimit of a [[monad]], regarded as a diagram in a 2-category.

* The [[collage]] of a [[profunctor]] is its lax colimit, regarded as a diagram in the 2-category [[Prof]].

* When $C$ is a category, the [[Grothendieck construction]] of a functor $C\to Cat$ is the same as its *oplax* colimit; see [here](http://ncatlab.org/nlab/show/Grothendieck+construction#AsALaxColimit).


### 2-Colimits in $Cat$
 {#2ColimitsInCat}

As shown [here](http://ncatlab.org/nlab/show/Grothendieck+construction#AsALaxColimit), if $C$ is an ordinary category and $F \colon C \to Cat$ is a [[pseudofunctor]], then the [[oplax colimit]] of $F$ is given by the [[Grothendieck construction]] $\int F$ --- and its [[pseudo-colimit]] is given by [[localization|formally inverting]] the [[cartesian morphism|opcartesian]] morphisms in $\int F$.  This yields a construction of certain pseudo 2-colimits in $Cat$.

Moreover, a similar result holds more generally when $C$ is a [[bicategory]].  In this case, $\int F$ is also a bicategory: a 2-cell from $(m \colon c \to d, f \colon m_*x \to y)$ to $(n \colon c \to d, g \colon n_*x \to y)$ is given by a 2-cell $\mu \colon m \Rightarrow n$ in $C$ such that $\mu_* x$ is a morphism $f \to g$ over $y$.

Let $\pi_*$ denote the functor that sends a bicategory $K$ to the category whose objects are those of $K$ and whose hom-sets are the [[connected category|connected components]] of the hom-categories of $K$; let also $d_*$ denote the functor that sends a category $X$ to the corresponding locally discrete bicategory.  Then there is an equivalence of categories

$$ [K, d_* X] \simeq [\pi_* K, X]  $$

It is straightforward to check that the first of the above facts extends to the bicategorical case:

$$ Lax(F, \Delta X) \simeq [{\textstyle \int} F, d_* X] $$

as does the fact that a lax transformation on the left is pseudo if and only if the corresponding functor on the right inverts the opcartesian morphisms in $\int F$.  It is almost trivial that the adjunction $\pi_* \dashv d_*$ holds when restricted to the functor $[-, -]_{S^{-1}}$ that takes two categories or bicategories to the full subcategory of functors that invert the class $S$ of morphisms.  Taking $S$ to be the opcartesian morphisms in $\int F$, then, we have

$$
  Ps(F, \Delta X) \simeq [{\textstyle \int} F, d_* X]_{S^{-1}}
  \simeq [\pi_* {\textstyle \int} F, X]_{S^{-1}}
  \simeq [(\pi_* {\textstyle \int} F)[S^{-1}], X]
$$

Hence the pseudo colimit of $F$ is got by taking its bicategory of elements, applying the 'local $\pi_0$' functor, and then inverting the (images of the) opcartesian morphisms as usual.


## Related concepts

* [[limit]]

* **2-limit**

* [[(∞,1)-limit]]

  * [[homotopy limit]]

  * [[lax (∞,1)-colimit]]

* [[coherence for bicategories with finite limits]]

* [[representable 2-category]]

## References 

* {#StreetLimitsIndexed} [[Ross Street]], _Limits indexed by category-valued 2-functors_ Journal of Pure and Applied Algebra **8**, Issue 2 (1976) pp 149-181. doi:[10.1016/0022-4049(76)90013-X](https://doi.org/10.1016/0022-4049(76%2990013-X)
  

* [[Max Kelly]], _Elementary observations on 2-categorical limits_, Bulletin of the Australian Mathematical Society (1989), 39: 301-317, doi:[10.1017/S0004972700002781](https://doi.org/10.1017/S0004972700002781)

* [[Ross Street]], _Fibrations in Bicategories_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, Volume **21** (1980) no. 2, pp 111-160.  [Numdam](http://www.numdam.org/item?id=CTGDC_1980__21_2_111_0 ) and correction, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, Volume **28** (1987) no. 1, pp 53-56 [Numdam](http://www.numdam.org/item?id=CTGDC_1987__28_1_53_0 )

Section 6, page 37 in 

* [[Steve Lack]], _A 2-categories companion_. In: Baez J., May J. (eds) Towards Higher Categories. The IMA Volumes in Mathematics and its Applications, vol **152** 2010 Springer, New York, NY. doi:[10.1007/978-1-4419-1524-5_4](https://doi.org/10.1007/978-1-4419-1524-5_4), arXiv:[math.CT/0702535](http://arxiv.org/abs/math.CT/0702535).

* G. J. Bird, [[Max Kelly]], [[John Power]], [[Ross Street]], _Flexible limits for 2-categories_, Journal of Pure and Applied Algebra **61** Issue 1 (1989) pp 1-27. doi:[10.1016/0022-4049(89)90065-0](http://dx.doi.org/10.1016/0022-4049(89%2990065-0)
Chapters 3,4,5 in 

* [[Thomas Fiore]], _Pseudo Limits, Biadjoints, and Pseudo Algebras: Categorical Foundations of Conformal Field Theory_, Mem. Amer. Math. Soc. **182** (2006), no. 860 ([arXiv:math/0408298](http://arxiv.org/abs/math/0408298)) ([AMS page](http://bookstore.ams.org/memo-182-860), [Google Books](https://books.google.com.au/books?id=y_DUCQAAQBAJ))


[[!redirects 2-limits]]
[[!redirects 2-colimit]]
[[!redirects 2-colimits]]
[[!redirects 2-categorical limit]]
[[!redirects 2-categorical limits]]
[[!redirects 2-categorial limit]]
[[!redirects 2-categorial limits]]
[[!redirects 2-categorical colimit]]
[[!redirects 2-categorical colimits]]
[[!redirects 2-categorial colimit]]
[[!redirects 2-categorial colimits]]


[[!redirects bicolimit]]
[[!redirects bicolimits]]

[[!redirects lax limit]]
[[!redirects lax limits]]
[[!redirects lax colimit]]
[[!redirects lax colimits]]
[[!redirects oplax limit]]
[[!redirects oplax limits]]
[[!redirects oplax colimit]]
[[!redirects oplax colimits]]
[[!redirects colax limit]]
[[!redirects colax limits]]
[[!redirects colax colimit]]
[[!redirects colax colimits]]

[[!redirects strict lax limit]]
[[!redirects strict lax limits]]
[[!redirects strict lax colimit]]
[[!redirects strict lax colimits]]
[[!redirects strict oplax limit]]
[[!redirects strict oplax limits]]
[[!redirects strict oplax colimit]]
[[!redirects strict oplax colimits]]
[[!redirects strict colax limit]]
[[!redirects strict colax limits]]
[[!redirects strict colax colimit]]
[[!redirects strict colax colimits]]

[[!redirects pseudolimit]]
[[!redirects pseudolimits]]
[[!redirects pseudo limit]]
[[!redirects pseudo limits]]
[[!redirects pseudo-limit]]
[[!redirects pseudo-limits]]
[[!redirects pseudocolimit]]
[[!redirects pseudocolimits]]
[[!redirects pseudo colimit]]
[[!redirects pseudo colimits]]
[[!redirects pseudo-colimit]]
[[!redirects pseudo-colimits]]

[[!redirects strict pseudolimit]]
[[!redirects strict pseudolimits]]
[[!redirects strict pseudo limit]]
[[!redirects strict pseudo limits]]
[[!redirects strict pseudo-limit]]
[[!redirects strict pseudo-limits]]
[[!redirects strict pseudocolimit]]
[[!redirects strict pseudocolimits]]
[[!redirects strict pseudo colimit]]
[[!redirects strict pseudo colimits]]
[[!redirects strict pseudo-colimit]]
[[!redirects strict pseudo-colimits]]

[[!redirects (2,1)-limit]]
[[!redirects (2,1)-limits]]
[[!redirects (2,1)-colimit]]
[[!redirects (2,1)-colimits]]



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--




#Contents#
* automatic table of contents goes here
{:toc}

## Idea

_Higher category theory_ is the generalization of [[category theory]] to a context where there are not only [[morphism]]s between [[object]]s, but generally [[k-morphism]]s between $(k-1)$-morphisms, for all $k \in \mathbb{N}$.

Higher category theory studies the generalization of [[∞-groupoid]]s  -- and hence, via the [[homotopy hypothesis]], of [[topological space]]s -- to that of [[directed space]]s and their _combinatorial or algebraic models_ . It is to the theory of [[∞-groupoid]]s as [[category theory]] is to the theory of [[groupoids]] (and hence of [[groups]]).

These [[geometric definition of higher category|combinatorial]] or [[algebraic definition of higher category|algebraic]] models are known as [[n-category|n-categories]] or, when $n \to \infty$, as [[∞-category|∞-categories]] or [[∞-category|∞-categories]], or, in more detail, as [[(n,r)-category|(n,r)-categories]]: 

* the natural number $n$ denotes the maximal dimension of _non-trivial_ cells in the model, 

* while the natural number $r$ denotes the maximal dimension of the _directed_ cells.

So an ordinary [[topological space]] or [[∞-groupoid]] is an [[(∞,0)-category]]: it has cells of arbitrary dimension and all of them are reversible.

In contrast to that, a [[geometric definition of higher category|combinatorial]] or [[algebraic definition of higher category|algebraic]] model for a [[directed space]] in which the 1-dimensional paths may not all be reversible is an [[(∞,1)-category]]: it still has cells of arbitrary dimension, but only those of dimension greater than 1 are guaranteed to be reverible.

Often it is convenient in practice to consider the case where the possible dimension $n$ of non-trivial cells is finite. This is familiar from how a [[topological space]] that happens to have vanishing [[homotopy group]]s in dimension above some $n$ -- a [[homotopy n-type]] -- is modeled by an [[n-groupoid]]. A fully directed version of this is an [[n-category]], which is short for [[(n,n)-category]]: non-trivial cells up to and including dimension $n$, and all of them allowed to be non-reversible. Actually, it is possible to go on to an $(n,n+1)$-category, or $(n+1)$-[[n-poset|poset]]; you can either consider than the $n$-cells are ordered, or else consider that there are irreversible $(n+1)$-cells which are indistinguishable. (Reversible indistinguishable $(n+1)$-cells are all identities and so might as well not exist.)

For low $n$ very explicit [[algebraic definition of higher category|algebraic models]] for $n$-categories are available but in their full generality become quickly rather untractable as $n$ increases: the series starts with [[bicategory]], [[tricategory]] and [[tetracategory]]. While bicategories have found plenty of applications, already the axioms of tricategories are rather involved and their theory mainly serves to produce the statement that there is a good [[semi-strict infinity-category|semi-strictifications]] of tricategories called [[Gray-category|Gray-categories]]. 

Indeed, there are many _strictified_ models for higher categories: combinatorial or algebraic models that sacrifice full generality for a better concrete control. Notably there is a useful combinatorial/algebraic model for [[strict ∞-category|strict ∞-categories]] which, while falling short, already goes a long way towards describing general higher categorical structures. In fact, by [[Simpson's conjecture]] every [[∞-category]] is equivalent to one that looks like a [[strict ∞-category]] except for possibly having weak unit laws.

The challenge of describing fully general [[∞-category|∞-categories]]/[[∞-category|∞-categories]] is to achieve a combinatorial or algebraic control of all the higher composition rules of higher cells. One can distinguish roughly two orthogonal approaches to dealing with the problem:

in the [[algebraic definition of higher category]] an algebraic machinery is set up that allows to concretely handle the explicit _choices_ of composites of cells. Such machinery usually involves [[operad]]ic tools in one way or other. The most sophisticated definitions of this kind are the closely related [[Batanin ∞-category]] and [[Trimble n-category|Trimble ∞-category]].

On the other hand, in the [[geometric definition of higher category]] a combinatorial machinery is set up that allows to guarantee _existence_ of composites of cells. In the [[simplicial model for weak omega-categories|simplicial models for weak ∞-categories]] higher categories are characterized as [[simplicial set]]s with the extra [[stuff, structure, property|property]] that certain composites exist. The issue here is to characterize these existence laws correctly.

The basic example for such "existence laws" is the _Kan-filler condition_ that characterizes simplicial sets that are [[Kan complex]]es, the models for [[(∞,0)-category|(∞,0)-categories]]. More general higher categories are obtained by relaxing the Kan condition in just the right way. For instance by simply restricting the Kan-condition to just a certain sub-set of all cells yields the definition of simplicial sets that are called [[quasi-category|quasi-categories]]. These model [[(∞,1)-category|(∞,1)-categories]].

The right further relaxation of the (weak) Kan filler condition is more involved. An approach to capture this has been given by [[Dominic Verity]]'s definition of simplicial sets that are called [[complicial set]]s and [[weak complicial set]]s.

One expects that every algebraic definition of higher categories admits a construction called a [[nerve]] that maps it to a [[simplicial set]] that would constitute the corresponding geometric model. 

Another approach to handle the geometric definition of higher categories is a recursive one that uses $n$-fold simplicial sets. This is based on the notion of [[complete Segal space]], which is essentially a variation of the concept of [[quasi-category]]. Its advantage is that its definition may be applied recursively to yield the notion of [[n-fold complete Segal space]]s. These model [[(∞,n)-category|(∞,n)-categories]] for finite $n$.

Finally, a large supply of further models exists for [[(∞,1)-category|(∞,1)-categories]] in terms of [[enriched category theory]]. [[simplicial model category|Simplicially enriched model categories]] are a highly-developed toolkit for handling [[presentable (infinity,1)-category|presentable (∞,1)-categories]]. [[pretriangulated dg-category|Pretriangulated dg-enriched categories]] and [[A-infinity category|A-∞ categories]] are a comparably highly developed toolkit for handling [[stable (∞,1)-category|stable (∞,1)-categories]].


## Basic concepts

The basic concept on which higher category theory is built is the notion of **[[k-morphism]]** for all $k \in \mathbb{N}$, equipped with a notion of composition, such that **[[coherence law]]s** are satisfied.

This is what it's all about. 


## Basic constructions


### Higher presheaves

* [[higher topos theory]]

### Higher universal constructions

* [[2-limit]]

* [[adjoint (∞,1)-functor|(∞,1)-adjunction]]

* [[(∞,1)-Kan extension]]

  * [[limit in a quasi-category|(∞,1)-limit]]

* [[(∞,1)-Grothendieck construction]]



## Basic theorems

* [[homotopy hypothesis]]-theorem

* [[delooping hypothesis]]-theorem

* [[periodic table]]

* [[stabilization hypothesis]]-theorem

* [[michaelshulman:exactness hypothesis]]

* [[holographic principle of higher category theory|holographic principle]]


## Applications 

See

* [[applications of (higher) category theory]].

### Extended cobordisms 

One major application of higher category theory and to a large extent a driving force in developing it has been [[FQFT|extended functorial quantum field theory]]. This has recently led to what may become one of the central theorems of higher category theory, the proof of the [[cobordism hypothesis]]. This roughly characterizes the [[(∞,n)-category of cobordisms]] $Bord_n$ as the free [[(∞,n)-category]] with duals on a single generator.

Since it is [thought](http://golem.ph.utexas.edu/category/2008/02/new_hire_at_ucr.html#c016709) that $Bord_n$ for $n = \infty$ is essentially the [[complex cobordism cohomology theory|cobordism spectrum]], this indicates a useful way in which higher category theory subsumes and refines [[stable homotopy theory]].






## Models

There are many different _models_ for bringing the abstract notion of higher category onto paper.

* [[(n,r)-category]]

  * [[Theta-space]]

  * [[∞-category]]/[[∞-category]]

  * [[(∞,n)-category]]

    * [[n-fold complete Segal space]]

  * [[(∞,2)-category]]

  * [[(∞,1)-category]]

    * [[quasi-category]]

      * [[algebraic quasi-category]]

    * [[simplicially enriched category]]

    * [[complete Segal space]]

    * [[model category]]

  * [[(∞,0)-category]]/[[∞-groupoid]]

    * [[Kan complex]]

      * [[algebraic Kan complex]]

      * [[simplicial T-complex]]

  * [[n-category]] = (n,n)-category

    * [[2-category]], [[(2,1)-category]]

    * [[1-category]]

    * [[0-category]]

    * [[(?1)-category]]

    * [[(?2)-category]]

  * [[n-poset]] = (n&#8722;1,n)-category

    * [[2-poset]]

  * [[n-groupoid]] = (n,0)-category

    * [[2-groupoid]], [[3-groupoid]]


* [[categorification]]/[[decategorification]]

* [[geometric definition of higher category]]

  * [[Kan complex]]

  * [[quasi-category]]

  * [[simplicial model for weak ∞-categories]]

    * [[complicial set]]

    * [[weak complicial set]]

* [[algebraic definition of higher category]]

  * [[bicategory]]

  * [[bigroupoid]]

  * [[tricategory]]

  * [[tetracategory]]

  * [[strict ∞-category]]

  * [[Batanin ∞-category]]

  * [[Trimble n-category|Trimble ∞-category]]

  * [[Grothendieck-Maltsiniotis ∞-categories]]

* [[stable homotopy theory]]

  * [[symmetric monoidal category]]

  * [[symmetric monoidal (∞,1)-category]]

  * [[stable (∞,1)-category]]
  
    * [[dg-category]]

    * [[A-∞ category]]

    * [[triangulated category]]




### 1-categorical models

* [[homotopical category]]

* [[model category|model category theory]]

* [[enriched category theory]]


## Related concepts

* [[category theory]]

* [[2-category theory]]

* [[(∞,1)-category theory]]

* **higher category theory**



## References

For a very gentle introduction to higher category theory, try [The Tale of <em>n</em>-Categories](http://math.ucr.edu/home/baez/week73.html#tale), which begins in "week73" of This Week's Finds and goes on from there... keep clicking the links.

For a slightly more formal but still pathetically easy introduction, try:

* [[John Baez]], [An Introduction to n-Categories](http://arxiv.org/abs/q-alg/9705009), in
<em>7th Conference on Category Theory and Computer Science</em>, eds.
E. Moggi and G. Rosolini, Springer Lecture Notes in
Computer Science vol. 1290, Springer, Berlin, 1997. 

For a free introductory text on $n$-categories that's <i>full of pictures</i>, try this:

* [[Eugenia Cheng]] and [[Aaron Lauda]], [Higher-Dimensional Categories: An Illustrated Guidebook](http://www.cheng.staff.shef.ac.uk/guidebook/).

[[Tom Leinster]] has written about "comparative $\infty$-categoriology" (to [borrow](http://golem.ph.utexas.edu/category/2008/01/comparative_smootheology.html) a term):

* Tom Leinster, _A Survey of Definitions of n-Category_ ([arXiv](http://arxiv.org/abs/math.CT/0107188))

* Tom Leinster, _Higher Operads, Higher Categories_ ([arXiv](http://arxiv.org/abs/math/0305049))

A grand pciture of the theory of higher categories is drawn in 

* [[Carlos Simpson]], _[[Homotopy Theory of Higher Categories]]_ ([pdf](http://hal.archives-ouvertes.fr/docs/00/44/98/26/PDF/main.pdf))

Another collection of discussions of definitions of higher categories is given at

* [[John Baez]], [[Peter May]] [[Approaching Higher Category Theory]]

A brief useful survey of approaches to the definition of higher categories is provided by the set of slides

* [[Andre Joyal]], [[Tim Porter]], [[Peter May]], _Weak categories_ ([pdf](http://www.ima.umn.edu/talks/workshops/SP6.7-18.04/may/PorterMay.pdf))

The theory of [[quasi-categories]] as [[(∞,1)-categories]] has reached a point where it is well developed and being applied to a wealth of problems with

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ ([arXiv](http://arxiv.org/abs/math.CT/0608040))



There's a lot more to add here, even if we restrict ourselves to very general texts.  (More specialized stuff should go under more specialized subcategories!)



[[!redirects higher category theory]]

[[!redirects higher category]]
[[!redirects higher categories]]

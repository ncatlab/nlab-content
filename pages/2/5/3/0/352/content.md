
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# $\infty$-categories
* table of contents
{: toc}

## Idea

$\infty$-Categories are the entities studied in [[higher category theory]]. See also there.

In generalization to how an ordinary [[category]] has [[morphism|morphisms]] going between [[object|objects]], and a [[2-category]] has both morphisms (or 1-morphisms) between objects and 2-morphisms (or 2-cells) going between 1-morphisms, in an $\infty$-category (sometimes called an $\omega$-[[omega-category|category]]), there are $j$-morphisms going between $(j-1)$-morphisms for all $j = 1, 2, \ldots$.  (The $0$-morphisms are the objects of the $\infty$-category.)

If all the $j$-morphisms in an $\infty$-category are [[equivalence|equivalences]] in some suitable sense, we call the $\infty$-category an $\infty$-[[infinity-groupoid|groupoid]].  In this case we can think of the $j$-morphisms for $j\ge 1$ as "homotopies" and the $\infty$-groupoid as a model for a "space."  By analogy, we can, if we wish, think of an arbitrary $\infty$-category as a combinatorial model for a [[directed space]] containing [[directed homotopy theory|higher directed homotopies]].

There are many different definitions realizing the general idea of $\infty$-category.  Models for $\infty$-categories usually fall into two classes:

* in the [[geometric definition of higher category]] an $\infty$-category is a conglomerate of [[geometric shapes for higher structures]] with extra _properties_;

  * examples are: [[Kan complex]], [[quasi-category]], [[Segal category]], [[opetopic n-category]].

* in the [[algebraic definition of higher category]] an $\infty$-category is a conglomerate of [[geometric shapes for higher structures]] with extra _structure_;

  * examples are: [[bicategory]], [[tricategory]], [[simplicially enriched category]], [[strict omega-category]].

One of the tasks of [[higher category theory]] is to relate and organize all these different models to a coherent general theory.


## Strict versus weak

There are many different definitions of $\infty$-categories, which may differ in particular in the degree to which certain structural identities are required to hold as equations or allowed to hold up to higher morphisms.

* See [[semi-strict infinity-category]].

* See the discussion we had at [[discussion on terminology -- omega-category]].


## Literature

For a very gentle introduction to higher category theory, try [The Tale of <em>n</em>-Categories](http://math.ucr.edu/home/baez/week73.html#tale), which begins in "week73" of This Week's Finds and goes on from there... keep clicking the links.

For a slightly more formal but still pathetically easy introduction, try:

* John Baez, [An Introduction to n-Categories](http://arxiv.org/abs/q-alg/9705009), in
<em>7th Conference on Category Theory and Computer Science</em>, eds.
E. Moggi and G. Rosolini, Springer Lecture Notes in
Computer Science vol. 1290, Springer, Berlin, 1997. 

For a free introductory text on $n$-categories that's <i>full of pictures</i>, try this:

* Eugenia Cheng and Aaron Lauda, [Higher-Dimensional Categories: An Illustrated Guidebook](http://cheng.staff.shef.ac.uk/guidebook/index.html).

[[Tom Leinster]] has written about "comparative $\infty$-categoriology" (to [borrow](http://golem.ph.utexas.edu/category/2008/01/comparative_smootheology.html) a term):

* Tom Leinster, _A Survey of Definitions of n-Category_ ([arXiv](http://arxiv.org/abs/math.CT/0107188))

* Tom Leinster, _Higher Operads, Higher Categories_ ([arXiv](http://arxiv.org/abs/math/0305049))

Recently $(\infty, 1)$-categories (see [[homotopy theory]]) have attracted much attention :

* Jacob Lurie, _Higher Topos Theory_ ([arXiv](http://arxiv.org/abs/math.CT/0608040))

There's a lot more to add here, even if we restrict ourselves to very general texts.  (More specialized stuff should go under more specialized subcategories!)


[[!redirects $infinity$-category]]
[[!redirects $infinity$-categories]]
[[!redirects ∞-category]]
[[!redirects ∞-categories]]
[[!redirects $\infty$-category]]
[[!redirects $\infty$-categories]]

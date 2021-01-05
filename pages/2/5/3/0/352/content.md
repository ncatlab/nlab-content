
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

The term "$\infty$-category" refers to a joint higher generalization of the notion of [[groupoid]], [[category]], and [[2-groupoid]], [[3-groupoid]], ... [[∞-groupoid]]. 

Generalising how in an ordinary [[category]], one has [[morphisms]] going between [[objects]], and in a [[2-category]], one has both morphisms (or _[[1-morphisms]]_ or _1-cells_) between objects and _[[2-morphisms]]_ (or _2-cells_) going between 1-morphisms, in an $\infty$-category, there are [[n-morphism|k-morphisms]] going between $(k-1)$-morphisms for all $k = 1, 2, \ldots$.  (The $0$-morphisms are the objects of the $\infty$-category.)

There are two crucially different uses of the term: 

1. If one speaks strictly only of the joint generalization of _[[category]]_ and _[[∞-groupoid]]_, hence of the notion of [[category object in an (∞,1)-category|internal category]] in [[homotopy theory]], then the "$\infty$-"-prefix is to be read as in _[[A-∞ algebra]]_, _[[E-∞ algebra]]_, _[[L-∞ algebra]]_ and, in fact, _[[A-∞ category]]_: in all these cases it means that the defining structural relations such as [[associativity]] of [[morphisms]] are taken to hold up to [[coherence|coherent]] higher [[homotopy]], also called _strong homotopy_.

   This meaning of "$\infty$-category" is also, less ambiguously, called **[[(∞,1)-category]]** (following the pattern of _[[(n,r)-categories]]_). For more on this notion **turn to the entry _[[(∞,1)-category]]_.**

1. In a more encompassing view on [[higher category theory]] one may take the maximal "weakening" of structures as implicit and speak of just _[[2-category]]_ to mean a _[[bicategory]]_ or rather a _[[(∞,2)-category]]_, of just _[[3-category]]_ to mean a _[[tricategory]]_ or rather a _[[(∞,n)-category|(∞,3)-category]]_, of just _[[4-category]]_ to mean a _[[tetracategory]]_ or rather _[[(∞,n)-category|(∞,4)-category]]_, and so on. With this counting then an "$\infty$-category" is some limiting notion of $(\infty,\infty)$-category. With this meaning one also often speaks of _[[∞-categories]]_.

   This is hence a much more encompassing notion of $\infty$-category than that of [[(∞,1)-category]]. It is also much harder to formalize. While there is by now a very good [[(∞,1)-category theory]]/[[homotopy theory]] of [[(∞,n)-categories]] for all $n \in \mathbb{N}$, the limiting case where $n \to \infty$ is currently still poorly understood. While there are several existing proposed definitions for what a single [[∞-category]] is, in the most general sense, there is no real understanding of the correct morphisms between them, hence of the correct [[(∞,1)-category]] of [[∞-categories]]. But this may of course change with time.


If all the $j$-morphisms in an $\infty$-category are [[equivalence|equivalences]] in some suitable sense, we call the $\infty$-category an [[∞-groupoid]].  In this case we can think of the $j$-morphisms for $j\ge 1$ as "homotopies" and the $\infty$-groupoid as a model for a [[homotopy type]]. By analogy, we can, if we wish, think of an arbitrary $\infty$-category as a combinatorial model for a [[directed homotopy theory|directed homotopy type]].

There are many different definitions realizing the general idea of $\infty$-category.  Models for $\infty$-categories usually fall into two classes:

* in the [[geometric definition of higher category]] an $\infty$-category is a conglomerate of [[geometric shapes for higher structures]] with extra _properties_;

  * examples are: [[Kan complex]], [[quasi-category]], [[Segal category]], [[opetopic n-category]].

* in the [[algebraic definition of higher category]] an $\infty$-category is a conglomerate of [[geometric shapes for higher structures]] with extra _structure_;

  * examples are: [[bicategory]], [[tricategory]], [[simplicially enriched category]], [[strict omega-category]].

One of the tasks of [[higher category theory]] is to relate and organize all these different models to a coherent general theory.


## Strict versus weak

There are many different definitions of $\infty$-categories, which may differ in particular in the degree to which certain structural identities are required to hold as equations or allowed to hold up to higher morphisms.

* See [[semi-strict infinity-category]].

## Related entries

* [[0-category]], [[(0,1)-category]]

* [[category]]

* [[2-category]]

* [[3-category]]

* [[n-category]]

* [[(∞,0)-category]]

* [[(n,1)-category]]

* [[(∞,1)-category]], [[internal (∞,1)-category]], [[∞-groupoid]]

  [[table - models for (∞,1)-categories]]

* [[(∞,2)-category]]

* [[(∞,n)-category]]

* [[(n,r)-category]]


## References

(For detailed references see at _[[(∞,1)-category]]_, _[[(∞,n)-category]]_, _[[(n,r)-category]]_ and _[[∞-category]]_.)

For a very gentle introduction to notions of higher categories, try [The Tale of <em>n</em>-Categories](http://math.ucr.edu/home/baez/week73.html#tale), which begins in "week73" of This Week's Finds and goes on from there... keep clicking the links.

For a slightly more formal but still fairly gentle introduction, try:

* [[John Baez]], [An Introduction to n-Categories](http://arxiv.org/abs/q-alg/9705009), in <em>7th Conference on Category Theory and Computer Science</em>, eds. E. Moggi and G. Rosolini, Springer Lecture Notes in Computer Science vol. 1290, Springer, Berlin, 1997. 

For a free introductory text on $n$-categories that's <i>full of pictures</i>, try this:

* [[Eugenia Cheng]], [[Aaron Lauda]], [Higher-Dimensional Categories: An Illustrated Guidebook](http://cheng.staff.shef.ac.uk/guidebook/index.html).

[[Tom Leinster]] has written about "comparative $\infty$-categoriology" (to [borrow](http://golem.ph.utexas.edu/category/2008/01/comparative_smootheology.html) a term):

* [[Tom Leinster]], _A Survey of Definitions of n-Category_ ([arXiv](http://arxiv.org/abs/math.CT/0107188))

* [[Tom Leinster]], _Higher Operads, Higher Categories_ ([arXiv](http://arxiv.org/abs/math/0305049))

[[Emily Riehl]] gave a [minicourse](http://hessbellwald-lab.epfl.ch/ytm2015) on infinity categories at the Young Topologists' Meeting 2015.

A [[syntax|syntactic]] definition is given by [[Eric Finster]] in terms of [[opetopic type theory]], see there for details

[[!redirects infinity-categories]]

[[!redirects $infinity$-category]]
[[!redirects $infinity$-categories]]
[[!redirects ∞-category]]
[[!redirects ∞-categories]]
[[!redirects $\infty$-category]]
[[!redirects $\infty$-categories]]

[[!redirects (infinity,infinity)-category]]
[[!redirects (infinity,infinity)-categories]]

[[!redirects (∞,?)-category]]
[[!redirects (∞,?)-categories]]



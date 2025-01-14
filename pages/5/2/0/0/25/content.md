
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Categorification
+-- {: .hide}
[[!include categorification - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

_Horizontal categorification_ or _Oidification_ 
describes the process by which 

 1. a concept is realized to be equivalent to a certain type of [[category]] or [[magmoid]] with a _single [[object]]_;

 2. and then this concept is generalized -- or oidified -- by passing to instances of such types of categories with more than one object.

## Remarks

* This is to be contrasted with [[vertical categorification]].

* It can be argued that the term 'categorification' should be reserved for [[vertical categorification]],  since we can use 'oidification' for the horizontal concept.

* It has rightly been remarked that [[groupoid]]s are more fundamental than [[groups]], [[algebroids]] are more fundamental than algebras, etc. Hence in a better world, the suffix would be characterizing the one-object special cases, not the general concepts.

## Examples

* The horizontal categorification of [[groups]] are [[groupoids]]: [[category|categories]] in which every morphism is invertible.

* A horizontal categorification of [[algebras]] are [[algebroids]]: [[enriched category|enriched categories]] in the category of vector spaces. 

* A horizontal categorification of rings are [[ringoid]]s: [[enriched category|enriched categories]] over the category of abelian groups. ([blog](http://golem.ph.utexas.edu/category/2006/09/ringoids.html))

* A horizontal categorification of $C^*$-algebras hence ought to be known as _$C^*$--algebroids_  but is usually known as [[C-star-category|C*-categories]].

* Since, by the [[Gelfand-Naimark theorem]], [[C-star algebra]]s are dual to [[topological space]]s, Paolo Bertozzini et. al proposed to define [[spaceoid]]s to be entities dual to $C^*$-categories ([blog](http://golem.ph.utexas.edu/category/2008/01/spaceoids.html)).

* {#Monoidoid} And an **exception to the rule**: a many-object [[monoid]] is _not_ called a _[[monoidoid]]_ -- but is called a [[category]]! 

  On the other hand, if the category is $R$-linear ([[enriched category|enriched]] in [[R Mod]]) then it may again be referred to as an *[[algebroid]]* over $R$.

* A horizontal categorification of the notion of *[[monads]]* is that of *[[categories enriched in a bicategory]]*.

* A horizontal categorification of a single-sorted [[Lawvere theory]] is a multisorted Lawvere theory. Analogously an [[operad]] categorifies to a many-colored operad.

* {#InTypeTheory} In [[type theory]]/[[programming language theory]], horizontal categorification is analogous to *introducing a type distinction*: an untyped language is a special case of a typed language where there is exactly one [[type]]. This fits with the [[categorical semantics]]: untyped [[lambda calculus]] has models in [[Lawvere theories]], whereas (simply) [[typed lambda calculus]] has models in Cartesian [[multicategories]].

[[!include oidification - table]]

## General definition of horizontal categorification
Tom Leinster's book "Higher Operads, Higher Categories"
contains a general theory of horizontal categorification of a notion of algebraic structure, as long as the algebraic structure can be defined as the category of algebras for an operad. Leinster proves that if $P$ is a (non-symmetric) operad in the category of sets, then $P$ can be extended to an "fc-multicategory" $\Sigma P$, the *suspension* of $P$, which is a kind of generalized operad which acts on directed graphs. So, for example, the horizontal categorification of the algebraic theory of monoids, as an operad, is the algebraic theory of categories, as a generalized operad. Eugenia Cheng has extended this definition of suspension so that it works for non-symmetric operads in a monoidal category $\mathcal{V}$ satisfying certain co/completeness assumptions. For example, one can take $\mathcal{V}= \mathbf{Cat}$. In this case, the operad $P$ whose algebras are monoidal categories has for its suspension (i.e., its horizontal categorification) the generalized operad whose algebras are precisely bicategories.

## Further discussion

Related $n$-Caf&#233;-discussion is in 

* [[John Baez]], [_What is categorification?_](http://golem.ph.utexas.edu/category/2008/10/what_is_categorification.html)

* [[John Baez]], [_Ringoids_](http://golem.ph.utexas.edu/category/2006/09/ringoids.html)
* [[John Baez]], [_Higher Operads, Higher Categories_](https://arxiv.org/abs/math/0305049)
* [[Eugenia Cheng]], [_Comparing operadic theories of $n$-category_](https://arxiv.org/pdf/0809.2070)


[[!redirects Oidification]]
[[!redirects oidification]]
[[!redirects oidifications]]
[[!redirects horizontal categorifications]]

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

* A horizontal categorification of [[algebras]] are _algebroids_: [[enriched category|enriched categories]] in the category of vector spaces. 

* A horizontal categorification of rings are [[ringoid]]s: [[enriched category|enriched categories]] over the category of abelian groups. ([blog](http://golem.ph.utexas.edu/category/2006/09/ringoids.html))

* A horizontal categorification of $C^*$-algebras hence ought to be known as _$C^*$--algebroids_  but is usually known as [[C-star-category|C*-categories]].

* Since, by the [[Gelfand-Naimark theorem]], [[C-star algebra]]s are dual to [[topological space]]s, Paolo Bertozzini et. al proposed to define [[spaceoid]]s to be entities dual to $C^*$-categories ([blog](http://golem.ph.utexas.edu/category/2008/01/spaceoids.html)).

* {#Monoidoid} And an **exception to the rule**: a many-object [[monoid]] is _not_ called a _[[monoidoid]]_ -- but is called a [[category]]! 

  On the other hand, if the category is $R$-linear ([[enriched category|enriched]] in [[R Mod]]) then it may again be referred to as an *[[algebroid]]* over $R$.

* A horizontal categorification of a [[Lawvere Theory]] is a [[Cartesian multicategory]]. Analogously an [[operad]] categorifies to a many-colored operad.

* In [[type theory]]/[[programming language theory]], horizontal categorification is analogous to *introducing a type distinction*: an untyped language is a special case of a typed language where there is exactly one type. This fits with the semantic view: untyped [[lambda calculus]] has models in Lawvere Theories, whereas (simply) typed lambda calculus has models in Cartesian multicategories.

[[!include oidification - table]]

## Further discussion

Related $n$-Caf&#233;-discussion is in 

* [[John Baez]], [_What is categorification?_](http://golem.ph.utexas.edu/category/2008/10/what_is_categorification.html)

* [[John Baez]], [_Ringoids_](http://golem.ph.utexas.edu/category/2006/09/ringoids.html)


[[!redirects Oidification]]
[[!redirects oidification]]
[[!redirects oidifications]]
[[!redirects horizontal categorifications]]
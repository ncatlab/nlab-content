
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

* It has rightly been remarked that [[groupoid]]s are more fundamental than groups, algebroids are more fundamental than algebras, etc. Hence in a better world, the suffix would be characterizing the one-object special cases, not the general concepts.

## Examples

* The horizontal categorification of [[group]]s are [[groupoid]]s: [[category|categories]] in which every morphism is invertible.

* A horizontal categorification of [[algebra]]s are _algebroids_: [[enriched category|enriched categories]] in the category of vector spaces. 

+--{: .query}
[[David Roberts]]: How do Lie algebroids fit into this framework?

[[Urs Schreiber]]: at a rough level it is clear that the base space of a Lie algebroid has to be regardedas the "space of objects". Certainly a Lie algebroid over a point is precisely a Lie algebra.

But for a more precise statement one needs a more conceptual way to think of Lie algebroids. I am claiming at [[schreiber:∞-Lie algebroid]] that there is a way to regard Lie algebroids precisely as certain kinds of synthetically smooth groupoids, namely those all whose morphisms have "infinitesimal extension" in some sense. In such a picture Lie algebroids are on the same footing as Lie groupoids and are precisely the many-object version of Lie algebras = infinitesimal Lie groups.

=--

* A horizontal categorification of rings are [[ringoid]]s: [[enriched category|enriched categories]] over the category of abelian groups. ([blog](http://golem.ph.utexas.edu/category/2006/09/ringoids.html))

* A horizontal categorification of [[magma|magmas]] are [[magmoid|magmoids]]. 

* A horizontal categorification of $C^*$-algebras hence ought to be known as _$C^*$--algebroids_  but is usually known as [[C-star-category|C*-categories]].

* Since, by the [[Gelfand-Naimark theorem]], [[C-star algebra]]s are dual to [[topological space]]s, Paolo Bertozzini et. al proposed to define [[spaceoid]]s to be entities dual to $C^*$-categories ([blog](http://golem.ph.utexas.edu/category/2008/01/spaceoids.html)).

* And finally the **exception to the rule**: a many-object [[monoid]] is _not_ called a _monoidoid_ -- but is called a [[category]]! :-)

+--{: .query}
[[Mike Shulman|Mike]]: Is there (and do we want there to be) a general rule about whether an X-oid means an [[internal category]] whose one-object version is an X, or an [[enriched category]] whose one-object version is an X?  The examples above seem to be taking the "internal" side, but the Cafe discussion on "ringoids" was about the "enriched" version; the two are very different!  And "dg-algebroid" was suggested for [[dg-category]], which is an enriched oidification of a [[dg-algebra]], but a [[Hopf algebroid]] is an internal oidification of a [[Hopf algebra]].

[[Urs Schreiber|Urs]]: good point. We should say this at the beginning and split the list of examples in two sorts 
=--

+--{: .query}
[[Theresa May]]: Could a [[quiver]] be said to be a horizontal categorification of a [[set]], even though quivers are not categories?
=--

## Further discussion

Related $n$-Caf&#233;-discussion is in 

* [[John Baez]], [_What is categorification?_](http://golem.ph.utexas.edu/category/2008/10/what_is_categorification.html)

* [[John Baez]], [_Ringoids_](http://golem.ph.utexas.edu/category/2006/09/ringoids.html)


[[!redirects Oidification]]
[[!redirects oidification]]
[[!redirects oidifications]]
[[!redirects horizontal categorifications]]
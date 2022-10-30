A [[category]] is **small** if it has a [[set]] of objects and a set of morphisms.  In other words, a small category is an [[internal category]] in the category [[Set]].  Small categories are free of some of the subtleties that apply to [[large category|large categories]].

A category is said to be **essentially small** if it is [[equivalence of categories|equivalent]] to a small category.  Assuming the [[axiom of choice]], this is the same as saying that it has a small [[skeleton]], or equivalently that it is [[locally small category|locally small]] and has a small number of isomorphism classes of objects.

A **small category structure** on a category $C$ is an [[essentially surjective functor]] from a set (as a [[discrete category]]) to $C$.  A category is essentially small iff it has a small category structure; this does not require the axiom of choice.

#Smallness in the conext of Grothendieck universes#

If [[Grothendieck universe]]s are being used, then for $U$ a fixed Grothendieck universe, a category $C$ is **$U$-small** if its collection of objects and collection of morphisms are both elements of $U$.  $C$ is **essentially $U$-small** if there is a [[bijection]] from its set of morphisms to an element of $U$ (the same for the set of objects follows); this condition is non-evil.

So let $U\Set$ be the category of $U$-small sets. Then
* a $U$-category (a [[locally small category|locally U-small]])-category is a category [[enriched category|enriched over]] $U Set$;
* a $U$-small category is a category [[internal category|internal to]] $U Set$.

Note that in this context, 'large' is used more strictly than in general category theory.  A category is **$U$-large** if its set of objects and set of morphisms are both subsets of $U$; usually one does not count $U$-small categories as $U$-large.  However, some categories (such as the category of $U$-large categories) are 'too large to be large'.


[[!redirects essentially small category]]
[[!redirects small categories]]
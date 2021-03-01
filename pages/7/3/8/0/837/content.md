
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An $n$-poset is any of several concepts that generalize [[partial order|posets]] in [[higher category theory]]. In fact, $n$-posets are the same as $(n-1,\infty)$-[[(n,r)-category|categories]].


## Definition

Fix a meaning of $(\infty,\infty)$-[[infinity-category|category]], however weak or strict you wish. Then an __$n$-poset__ is a $(n-1)$-[[truncation]] of an $(\infty,\infty)$-category. As all $j$-morphisms for $j \geq n$ are equivalent in an $(n-1)$-truncated $(\infty,r)$-category,  all [[parallel morphisms|parallel]] pairs of $j$-morphisms are [[equivalence|equivalent]] for $j \geq n$ by definition, which means that $(n-1,\infty)$-categories are the same as $(n-1,n)$-categories. Thus, up to equivalence, there is no point in mentioning anything beyond $n$-morphisms, not even whether two given parallel $n$-morphisms are equivalent. This definition makes sense as low as $n = -1$; the statement that parallel $(-1)$-morphisms are equivalent simply means that there exists an object (a $0$-morphism).


## Special cases

* The concept of $(-1)$-[[(-1)-poset|poset]] is trivial.

* A $0$-[[0-poset|poset]] is a [[truth value]].

* A $1$-[[1-poset|poset]] or [[(0,1)-category]] is simply a [[partial order|poset]].

  Because, by the definition of $(0,1)$-category, we have that any two $1$-morphisms with the same source and target are equivalent. Hence there is, up to equivalence, at most one morphism for every ordered pair of objects. The rest of the axioms say that this is all the information there is in a $(0,1)$-category. Therefore, by the discussion at _[poset -- As a category with extra properties](http://ncatlab.org/nlab/show/partial+order#AsACategoryWithExtraProperties)_, a $(0,1)$-category is a poset.  (See also [[thin category]].)

* A $2$-[[2-poset|poset]] or [[(1,2)-category]] is a [[locally posetal 2-category]].

* In general, an $n$-poset is an $n$-[[n-category|category]] in which all parallel pairs of $n$-morphisms are equal.

* An $\infty$-poset is the same thing as an $(\infty,\infty)$-[[infinity-category|category]].

In the light of the general definition, one must interpret 'is' up to [[equivalence of categories]].  The last statement also depends on how strict your definition of $(\infty,\infty)$-category or $n$-category is; it is actually simpler to define $n$-posets from scratch as given above than to define them in terms of $n$-categories.


## Basic theorems

The $(\infty,\infty)$-category of ([[small category|small]]) $n$-posets, as a [[full subcategory|full sub-(∞,∞)-category]] of the $(\infty,\infty)$-category of $(\infty,\infty)$-categories, is an $(n+1)$-poset.  That is, $n$-posets form an $(n+1)$-poset.  This is well known for small values of $n$.

[[!redirects n-poset]]
[[!redirects n-posets]]
[[!redirects (n-1,n)-category]]
[[!redirects (n-1,n)-categories]]
[[!redirects (n-1,infinity)-category]]
[[!redirects (n-1,infinity)-categories]]
[[!redirects (n-1,∞)-categories]]
[[!redirects (n-1,∞)-categories]]
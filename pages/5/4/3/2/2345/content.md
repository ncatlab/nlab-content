+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A __$2$-functor__ is a [[functor]] between $2$-[[2-category|categories]].

Of course, any sort of morphism between $2$-categories, if it deserves to be called anything like 'functor', will be a $2$-functor, so the prefix is not really necessary.  (For discussion of this issue in general, see [[higher functor]].)  On the other hand, sometimes the more precise terminology helps to clarify that one really is thinking of $2$-categories rather than an underlying $1$-[[1-category|category]]; for instance, not every $1$-functor $Cat \to Cat$ extends to a $2$-functor.

In any case, one does need to take care to write the definition correctly.  There are actually (at least) two ways to do this, corresponding to the two kinds of $2$-categories: [[strict 2-category|strict]] and [[bicategory|weak]].  So for the definitions, see:
*  [[strict 2-functor]]
*  [[pseudo functor]]

Compare [[lax 2-functor]], which should *not* be called simply 'functor' (although 'lax functor' is usually fine).

It usually doesn\'t make sense to speak of strict $2$-functors between weak $2$-categories[^1], but it does make sense to speak of weak $2$-functors between strict $2$-categories.  Indeed, the weak $3$-[[3-category|category]] [[Bicat]] of bicategories, pseudofunctors, [[pseudonatural transformations]], and [[modifications]] is  [[equivalence of categories|equivalent]] to its full sub-3-category spanned by the strict 2-categories.  However, it is not equivalent to the $3$-category [[Str2Cat]] of strict $2$-categories, *strict* $2$-functors, transformations, and modifications.

For the generalisation of this to higher categories, see [[semistrict higher category]].

[^1]: Although there are certain contexts in which it does.  For instance, there is a [[model structure]] on the category of [[bicategories]] and strict 2-functors between them, which models the homotopy theory of bicategories and weak 2-functors.

[[!redirects 2-functors]]
[[!redirects strict 2-functor]]
[[!redirects strict 2-functors]]

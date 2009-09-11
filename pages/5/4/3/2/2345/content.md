A __$2$-functor__ is simply a [[functor]] between $2$-[[2-category|categories]].

Of course, anything sort of morphism between $2$-categories, if it deserves to be called anything like 'functor' at all, will be a $2$-functor, so the prefix is not really necessary.  (For discussion of this issue in general, see [[higher functor]].)  On the other hand, sometimes the more precise terminology helps to clarify that one really is thinking of $2$-categories, as with a pseudo functor (a weak $2$-functor, see below) to [[Cat]].  This can also be helpful when dealing with strict 2-categories that have underlying 1-categories, to clarify whether one is considering them as 2-categories or 1-categories; for instance, not every 1-functor $Cat\to Cat$ extends to a 2-functor.

In any case, one does need to take care to write the definition correctly.  There are actually (at least) two ways to do this, corresponding to the two kinds of $2$-categories: [[strict 2-category|strict]] and [[bicategory|weak]].  So for the definitions, see:
*  [[strict 2-functor]]
*  [[pseudo functor]]

Compare [[lax 2-functor]], which should *not* be called simply 'functor' (although the '2-' can also be dropped in this case, if there is no danger of confusion).

It usually doesn\'t make sense to speak of strict $2$-functors between weak $2$-categories[^1], but it does make sense to speak of weak $2$-functors between strict $2$-categories.  Indeed, the weak $3$-[[3-category|category]] [[Bicat]] of bicategories, pseudofunctors, [[pseudonatural transformations]], and [[modifications]] is  [[equivalence of categories|equivalent]] to its full sub-3-category spanned by the strict 2-categories.  However, it is not equivalent to the $3$-category [[Str2Cat]] of strict $2$-categories, *strict* $2$-functors, transformations, and modifications.

For the generalisation of this to higher categories, see [[semistrict higher category]].

[^1]: Although there are certain contexts in which it does.  For instance, there is a [[model structure]] on the category of [[bicategories]] and strict 2-functors between them, which models the homotopy theory of bicategories and weak 2-functors.

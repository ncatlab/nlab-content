There are two big questions about category theory and the logical foundations of mathematics:

 1. What foundations are adequate to formulate category theory?
 2. How can category theory provide a foundation for mathematics?

These questions also apply to [[higher category theory]], which also involves the relation between them. (Two-categories as a foundation for categories, for example.)

# Mathematical foundations of category theory

The standard view seems to be to found category theory on a theory of sets and classes; see [the English Wikipedia\'s definition](https://secure.wikimedia.org/wikipedia/en/wiki/Category_%28mathematics%29#Definition), for example. But the standard reference, Saunders Mac Lane\'s _Categories for the Working Mathematician_, assumes the existence of a universe (an inaccessible cardinal) instead. Both of these approaches rely on a distinction between *small* and *large* categories. There is a category of all [[small category|small categories]], but this category is not itself small; there is no category of all categories.

Alexander Grothendieck needed more; he used what we now call [[Grothendieck universe]]s. He assumed that every set is contained within a universe; that is, for every cardinal number $\kappa$, there is a cardinal inaccessible from $\kappa$. (This is still a rather moderate axiom, compared to some of the large-cardinal axioms studied by set theorists.) Now one has a relative notion of small and large; the category of all $U$-small categories (where $U$ is some universe) is $U$-large but must be $U'$-small for some other universe $U'$, and there exists a category (which is both $U$-large and $U'$-large) of all $U'$-small categories.

If one does not accept the [[axiom of choice]], then there are additional complications in general category theory. In particular, one must distinguish between a universal *property* (for example, having all [[product]]s) and having a universal *structure* realising that property (in the example, a functor taking each pair $(x,y)$ of objects to a specific product cone $x \leftarrow x \times y \rightarrow y$). This difficulty was overcome by Michael Makkai using [[anafunctor]]s, but these have not been widely adopted, even by constructivists.

For a summary of the mathematical foundations of category theory, see Mike Shulman, _Set theory for category theory_, [arXiv:0810.1279](http://arxiv.org/abs/0810.1279).

# Categorial foundations of mathematics

Bill Lawvere proposed to found mathematics on a first-order axiomatisation of [[Cat|the category of categories]]. This has not been very successful, but his other proposal, a first-order axiomatisation of [[Set|the category of sets]], works well.

Lawvere\'s system [[ETCS]] (for 'the Elementary Theory of the Category of Sets') essentially states that the category of sets is a [[topos]] with certain properties, in particular a [[well-pointed topos]]. This can be stated in elementary (first-order) terms; indeed, Lawvere invented the now-standard notion of [[elementary topos]] (in contrast to the earlier [[Grothendieck topos]]) to do this.

...

For a summary of this categorial foundation of mathematics, see [[ETCS]].

# Categorial foundations of category theory

...
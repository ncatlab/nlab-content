There are two big questions about category theory and the logical foundations of mathematics:

 1. What foundations are adequate to formulate category theory?
 2. How can category theory provide a foundation for mathematics?

These questions also apply to [[higher category theory]], which also involves the relation between them. (Two-categories as a foundation for categories, for example.)

# Mathematical foundations of category theory

The standard view seems to be to found category theory on a theory of sets and classes; see [the English Wikipedia article](https://secure.wikimedia.org/wikipedia/en/wiki/Category), for example. But the standard reference, Saunders Mac Lane\'s _Categories for the Working Mathematician_, assumes the existence of a universe (an inaccessible cardinal) instead. Both of these approaches rely on a distinction between *small* and *large* categories. There is a category of all [[small category|small categories]], but this category is not itself small; there is no category of all categories.

Alexander Grothendieck needed more; he used what we now call [[Grothendieck universe]]s. He assumed that every set is contained within a universe; that is, for every cardinal number $\kappa$, there is a cardinal inaccessible from $\kappa$. This is still a rather moderate axiom, compared to some of the large-cardinal axioms studied by set theorists.

If one does not accept the [[axiom of choice]], then there are additional complications in general category theory. In particular, one must distinguish between the *property* of having some universal structure (for example, having all [[product]]s) and the *structure* of being equipped with an operation realising that structure (in the example, a functor taking each pair $(x,y)$ of objects to a specific product $x \times y$). This difficulty was overcome by Michael Makkai using [[anafunctor]]s.

For a summary of the mathematical foundations of category theory, see Mike Shulman, _Set theory for category theory_, [arXiv:0810.1279](http://arxiv.org/abs/0810.1279).

# Categorial foundations of mathematics

...

For a summary of this categorial foundation of mathematics, see [[ETCS]].

# Categorial foundations of category theory

...
# Idea #

A _partial order_ on a set is a way of ordering its elements to say that some elements precede others, but allowing for the possibility that two elements may be incomparable without being the same.

# Definition #

Given a [[set]] $S$, a __partial order__ on $S$ is a (binary) [[relation]] $\leq$ with the following properties:
* reflexivity: $x \leq x$ always;
* transitivity: if $x \leq y \leq z$, then $x \leq z$;
* antisymmetry: if $x \leq y \leq x$, then $x = y$.

A __[[poset]]__ is a set equipped with a partial order.

# Categorial formulation #

A [[poset]] can be understood as a [[skeleton|skeletal]] [[category]] in which any two [[parallel morphisms]] are equal.  Accordingly, we may define a partial order on $S$ as a way to make $S$ the set of objects of such a category.
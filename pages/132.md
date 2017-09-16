# Categorical meaning #

A [[category]] is **discrete** if it contains only identity morphisms.  The idea is that in a discrete category no two points are connectable by any "path".  ([[small category|Small]]) discrete categories may be identified with [[set|sets]].

Conversely, for $S$ a collection, one says that the _discrete category over $S$_ is the category with $S$ as its collection of objects and only identity morphisms.  

The notion of "discrete category" is [[evil]].  A corresponding non-evil property is that any two parallel morphisms are equal and invertible; this is the same as being [[equivalence of categories|equivalent]] to a discrete category.


# Topological meaning #

If $C$ is a category [[enriched category|enriched]] or [[internal category|internal]] to [[topological space|topological spaces]], then there is another completely different meaning of **discrete**: that the _topology_ on the arrows (and the objects, in the internal case) is the discrete topology.

This is especially confusing if one extends the use of "discrete category over $S$" to the case of internal categories, when $S$ is an object of some ambient category.  With this usage, if $S$ is a topological space, then the "discrete internal category over $S$" in [[Top]] will not be discrete in the topological sense: it still remembers the topology on that space.

+--{.query}

What is the difference between a discrete category and a [[0-category]]? - [[Eric Forgy|Eric]]

Well, depending on your definition, a 0-category might _be_ a set (rather than the discrete category _on_ a set), or a discrete category, or a category that is _equivalent_ to a discrete category, or an $\omega$-category that is equivalent to a discrete one.  But morally, there is little difference.  - [[Mike Shulman|Mike]]

What is the difference between a set and a discrete category on a set? :) - [[Eric Forgy|Eric]]

Well, a set is just a set, whereas a discrete category is a set of objects together with a set of arrows as well as source, target, identity, and composition maps (which happen to all be bijections).  The category of sets is equivalent to the category of discrete categories, but not isomorphic to it (unless you play games with the formal definition of "category").  That's all that I meant. - Mike

Thanks Mike. I was just looking at [[3-category]] and [[2-category]] and even [[0-category]] and it seemed that in all cases the "higher" identity morphisms were somehow deemed irrelevant. If that is the case, then I didn't see why a discrete category would be "different" then a 0-category, which is just a [[set]], because the identity 1-morphisms were irrelevant. It would make sense to me if a discrete category were morally just a set, but I'm probably confused (as usual). - [[Eric Forgy|Eric]]

=--

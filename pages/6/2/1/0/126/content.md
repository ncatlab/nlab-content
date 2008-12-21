Given a [[category]] $C$, a _subcategory_ $D$ consists of a subcollection of the collection of [[object|objects]] of $C$ and a subcollection of the collection of [[morphism|morphisms]] of $D$ such that:

* If the morphism $f : x \to y$ is in $D$, then so are $x$ and $y$.

* If $f : x \to y$ and $g : y \to z$ are in $D$, then so is the [[composition|composite]] $g f : x \to z$.  

* If $x$ is in $D$ then so is the [[identity]] morphism $1_x$.

These conditions ensure that $D$ is a category in its own right.  We say $D$ is a _full subcategory_ if additionally 

* If $x$ and $y$ are in $D$, every morphism $f : x \to y$ is in $D$.

More generally, one may define a _subcategory_ of $C$ as a category $D$ equipped with a [[faithful functor|faithful]] [[functor]] $F: D \to C$. This is the same as a subcategory (in the sense above) of a category [[equivalence|equivalent]] to $C$.  In these terms, we define a _full subcategory_ to be a category equipped with a [[full functor|full]] and faithful functor $F : D \to C$.

+--{.query}
_[[Mike Shulman|Mike]] says_: I have a few objections to considering any faithful functor to be a "subcategory."

1. I really have a hard time convincing myself that the category of groups is a subcategory of the category of sets.  A group is a set with extra [[property, structure, and stuff|structure]], not a set satisfying some property.
2. Every functor between [[discrete category|discrete categories]] is faithful.  Therefore, if every faithful functor is a subcategory, every set (considered as a discrete category) would be a subcategory of every other (nonempty) set.
3. In particular, the terminal category would have a proper class of inequivalent subcategories.

If one really wants a notion of "non-full subcategory" that is invariant under equivalence of categories, I propose that [[pseudomonic functor|pseudomonic functors]] are a better candidate than faithful ones.
=--

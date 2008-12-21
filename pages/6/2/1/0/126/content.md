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

_Mathieu Dupont says_: For 1., you can "enlarge" $\mathrm{Set}$ to an equivalent category $\mathrm{Set}'$ by adding, for each group $G$, an object $\hat{G}$ and an isomorphism from $\hat{G}$ to the underlying set of $G$.  Then the category of groups is a "naive" subcategory of $\mathrm{Set}'$ (i.e. a subcategory as defined at the beginning of this entry).  Perhaps is this cheating?

A problem with pseudomonic functors is that not all inclusions of "naive" subcategories are pseudomonic.

_[[Mike Shulman|Mike]] replies_: Yes, I'm aware that, as the original entry said, any faithful functor is a naive subcategory of some equivalent category.  It doesn't make me any happier about calling $Grp$ a "subcategory" of $Set$, or about calling a discrete large category a "subcategory" of the terminal category.  I would be more inclined to _exclude_ non-pseudomonic naive subcategories from the notion of "subcategory" than to include all faithful functors.  Are there naturally occurring examples of non-pseudomonic naive subcategories (other than those obtained by doing violence to a naturally occurring faithful functor)?

Another way to phrase the question is, what is a good notion of "subobject" in a 2-category?  Not that there has to be only one such notion; even in a 1-category there are many (monic, strong monic, regular monic, etc.).  But it seems to me that to be worthy of the name "subobject" such a notion should be a conservative extension of some established notion of "subobject" for 1-categories; that is, it should reduce to something that deserves the name "subobject" when interpreted in locally-discrete 2-categories.  Full-and-faithful functors and pseudomonic functors both reduce to monomorphisms in a locally-discrete 2-category, but _every_ morphism in a locally-discrete 2-category is faithful.

I'm not disputing the importance of faithful functors, or more generally of faithful morphisms in a 2-category.  I just think that calling them "subobjects" is stretching the meaning of the prefix "sub-" so far that it becomes counterintuitive and confusing.

=--

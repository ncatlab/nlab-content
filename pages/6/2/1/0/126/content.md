Given a [[category]] $C$, a _subcategory_ $D$ consists of a subcollection of the collection of [[object|objects]] of $C$ and a subcollection of the collection of [[morphism|morphisms]] of $D$ such that:

* If the morphism $f : x \to y$ is in $D$, then so are $x$ and $y$.

* If $f : x \to y$ and $g : y \to z$ are in $D$, then so is the [[composition|composite]] $g f : x \to z$.  

* If $x$ is in $D$ then so is the [[identity]] morphism $1_x$.

These conditions ensure that $D$ is a category in its own right.  We say $D$ is a _full subcategory_ if additionally 

* If $x$ and $y$ are in $D$, every morphism $f : x \to y$ is in $D$.

More generally, one may define a _subcategory_ of $C$ as a category $D$ equipped with a [[faithful functor|faithful]] [[functor]] $F: D \to C$. This is the same as a subcategory (in the sense above) of a category [[equivalence|equivalent]] to $C$.  In these terms, we define a _full subcategory_ to be a category equipped with a [[full functor|full]] and faithful functor $F : D \to C$.

# Discussion
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

_Mathieu says_: I agree with the fact that there is a terminological problem : full subcategories should be called "subcategories" and subcategories should be given a new name ("2-subcategories"?).  Then a subcategory of a set will be a subset, so the prefix "sub" preserves its original meaning in this case.

An example of non-pseudomonic naive subcategory is given, for a non-skeletal internal category $C$ in $\mathrm{Set}$, by the inclusion of the discrete category on the set of objects $C_0$ into the realisation of $C$ as a category.

My answer to the question "what is a good notion of "subobject" in a 2-category?", at least in the case where every 2-cell is invertible, is that there are two such notions (plus their normal, regular, strong, etc., variations): fully faithful arrows with a given codomain, and faithful arrows with a given codomain.  That's the way I understood it when writing [my PhD thesis](http://arxiv.org/abs/0809.1760). 2-dimensional kernels are in general faithful (and not pseudomonic), so I'm inclined to think of the faithful kind of subobjects as the 2-dimensional counterpart of 1-dimensional subobjects.

[[Toby Bartels]]: My opinion is more with Mathieu than Mike (although perhaps this is because I don\'t fully appreciate pseudomonic functors). In fact, I submit that Mathieu\'s description of how Grp becomes a na&#239;ve subcategory of Set is how ordinary mathematicians actually use the language, down to the idea that being a group is a property of a set. On the other hand, since there\'s a very important sense that being a group is *not* just a property of a set (that the forgetful functor, while faithful, is *not* full, not even on isomorphisms), probably we should fight against this abuse of language by not using the word 'subcategory' in this na&#239;ve sense (hence nor in its equivalence-invariant generalisation). Either Mathieu\'s version ('subcategory' means full subcategory, hence given by a full and faithful functor) or Mike\'s version ('subcategory' means pseudomic subcategory, hence given by a pseudomonic functor) will do this.

_Mike:_ After thinking it over, while I would prefer defining "subcategory" to mean "pseudomonic functor" over defining it to mean "faithful functor," I would actually most prefer that we _not attempt_ to give "subcategory" an equivalence-invariant definition, because I don't think there is one that is free of confusion.  I would prefer we use some related, but different, terminology, which makes it clear that, as Mathieu says, there are a number of different notions of "subobject" in an $n$-category.  If, as Mathieu suggests, we use "2-subcategory" for "faithful functor," then it would be natural to use "1-subcategory" for "full and faithful functor."  In the appendix of [n-categories and cohomology](http://arxiv.org/abs/math.CT/0608420) I called faithful functors "1-monic" and full-and-faithful functors "0-monic," but at the moment I don't see any compelling reason for starting the numbering at one place or another.

_Mathieu_:  If a "1-subcategory" of $C$ is a fully faithful functor with codomain $C$, there is still room for "0-subcategories" (i.e. equivalences with codomain C) [and of course there are also "$\omega$-subcategories", i.e. any functor with codomain C].  But my principal reason for numbering in this way was that 1-monic = monic in the one-dimensional case, like 1-category = category.  By the way, here is a family of simple examples of subcategories which are not pseudomonic: any inclusion of a proper subgroup into a group seen as a one-objet groupoid.

_Mike_: Re: subgroups, point taken; non-pseudomonic subcategories do happen.  I think my motivation for starting the numbering as I did was that I was thinking that we should have 0-monic = monic for maps between 0-categories (sets).  But at the moment I'm feeling more sympathetic towards your argument that we should have instead 1-monic = monic for maps _in_ a 1-category.  Have we reached a point in the discussion where we are willing to change the main entry?

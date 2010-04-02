# Subcategories
* table of contents
{: toc}


## Definition

Given a [[category]] $C$, a __subcategory__ $D$ consists of a subcollection of the collection of [[object|objects]] of $C$ and a subcollection of the collection of [[morphism|morphisms]] of $D$ such that:

* If the morphism $f : x \to y$ is in $D$, then so are $x$ and $y$.

* If $f : x \to y$ and $g : y \to z$ are in $D$, then so is the [[composition|composite]] $g f : x \to z$.  

* If $x$ is in $D$ then so is the [[identity morphism]] $1_x$.

These conditions ensure that $D$ is a category in its own right and the inclusion $D\hookrightarrow C$ is a [[functor]].  Additionally, we say that $D$ is...

* A __[[full subcategory]]__ if for any $x$ and $y$ in $D$, every morphism $f : x \to y$ in $C$ is also in $D$ (that is, the inclusion [[functor]] $D\hookrightarrow C$ is [[full functor|full]]).

* A __[[replete subcategory]]__ if for any $x$ in $D$ and any isomorphism $f:x\cong y$ in $C$, both $y$ and $f$ are also in $D$.

* A __[[wide subcategory]]__ if every object of $C$ is also an object of $D$.


## Non-evil variants

Just as subsets of a [[set]] $X$ can be identified with isomorphism classes of [[monomorphism|monic]] functions into $X$, subcategories of a category $C$ can be identified with isomorphism classes of monic _functors_ into $C$.  A functor is easily verified to be monic iff it is [[faithful functor|faithful]] and injective on objects.  This can be generalized to monomorphisms in a [[strict 2-category]].

However, this notion is [[evil]] since being injective-on-objects refers to equality of objects.  This raises the question: what is a good non-evil definition of **subobject** in a [[2-category]]?  It is the contention of the authors of this page that there are multiple such definitions.  Two evident ones are:

* A morphism $f: A\to B$ in a 2-category $K$ is **1-monic** if it is full and faithful, i.e. $K(X,A) \to K(X,B)$ is full and faithful for all $X$.  A **1-subobject** of $B$ is an [[equivalence]] class of 1-monomorphisms into $B$, and a **1-subcategory** is a 1-subobject in $Cat$.
* Likewise, $f$ is **2-monic** if $K(X,A) \to K(X,B)$ is faithful for all $X$.  A **2-subobject** of $B$ is an equivalence class of 2-monomorphisms into $B$, and a **2-subcategory** is a 2-subobject in $Cat$.

The obvious generalizations (at least, obvious once you start thinking in terms of $k$-[[k-surjective functor|surjectivity]]) are that every morphism is 3-monic, while the 0-monic morphisms are the equivalences.  (Note that this numbering is offset by one from that used in [Baez and Shulman](http://arxiv.org/abs/math.CT/0608420).)  There is likewise an evident generalization to $k$-monomorphisms in any $n$-[[n-category|category]].

It is fairly undisputed that 1-subobjects, as defined above, are a good notion of subobject in a 2-category.  In particular, any full and faithful functor $C\to D$ in $Cat$ is equivalent to the inclusion of a full subcategory $C'\to D$ (here $C'$ is the full image of $C$).  Also, in a 1-category considered as a locally discrete 2-category, the 1-monomorphisms are precisely the usual sort of [[monomorphism]].

In fact, any faithful functor is likewise equivalent to the inclusion of a (non-full) subcategory, but in this case the codomain must be modified as well as the domain.  It is somewhat more disputable whether 2-subcategories all deserve to be called "subcategories;" for instance, is [[Grp]] a "subcategory" of [[Set]]?  Note also that any functor between [[discrete category|discrete categories]] is faithful, so that the [[terminal category]] has a proper class of inequivalent 2-subcategories, and similarly every morphism in a locally discrete 2-category is 2-monic.  However, kernels of morphisms between 2-groups are 2-subobjects, not 1-subobjects, and likewise for any subgroup of a [[group]] (considered as a 1-object category).  This motivates the term "2-subobject," to make it clear that there is some relationship with the sort of subobjects we are used to in 1-categories, but also some notable generalization.

Other types of morphism in a 2-category which have some claim to be considered "subobjects" include [[pseudomonic functor|pseudomonic]] morphisms and [[conservative functor|conservative]] morphisms.  Pseudomonic morphisms might merit a name such as **(2,1)-subcategory**, since a functor is pseudomonic iff it is faithful (a 2-subcategory) and its induced functor between [[underlying groupoid]]s is fully faithful (a 1-subcategory).  See also [[stuff, structure, property]].


## Discussion

The above discussion of non-evil variants is the result of the following discussion.

+--{.query}

_[[Mike Shulman|Mike]] says_: I have a few objections to considering any faithful functor to be a "subcategory."

1. I really have a hard time convincing myself that the category of groups is a subcategory of the category of sets.  A group is a set with extra [[stuff, structure, property|structure]], not a set satisfying some property.
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

_Toby_: For what it\'s worth, I would be happy with that.

=--


[[!redirects subcategory]]
[[!redirects subcategories]]

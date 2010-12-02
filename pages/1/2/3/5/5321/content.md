
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Let $\mathbf{U}$ and $\mathbf{V}$ be set-theoretic [[universes]] (such as [[Grothendieck universes]] or [[universe in a topos|universes in an ambient topos]]), and let $C$ be a [[category]] "in the world of $\mathbf{U}$," i.e. whose objects are $\mathbf{U}$-[[small category|small]] and which itself is $\mathbf{U}$-[[large category|large]].  Its **universe enlargement** is supposed to be a category "in the world of $\mathbf{V}$" which is "the same" or at least similar to $C$, and perhaps better behaved.

### Notation

An enlargement of a specific category, such as [[Set]], [[Cat]], [[Grp]], or [[Top]], is often denoted by writing its name in all capitals: SET, CAT, GRP, TOP.

As a notation for the operation on a general category $C$, the notation $\Uparrow C$ has been proposed.


## Definitions

Since the enlargement is not well-specified by the above intuitive description, there are several different definitions, which are often equivalent but not always.

Henceforth we fix two universes $\mathbf{U}$ and $\mathbf{V}$ with $\mathbf{U}\in \mathbf{V}$.  We will refer to sets in $\mathbf{U}$ as *small*, sets in $\mathbf{V}$ as *large*, and sets not necessarily in $\mathbf{V}$ (or in the next larger universe $\mathbf{W}$) as *very large*.

### Models of a theory

If $C$ is the category of small models of some [[theory]], then we can take $\Uparrow C$ to be the category of large models of the same theory.  For instance:

* the large category $Set$ of small sets is the category of small models of the theory with one sort and no operations or relations.  The category of large models of this theory is just the very large category $SET$ of large sets.

* Similarly, from categories such as $Grp$, $Cat$, and $Top$ of small groups, categories, and spaces, we obtain the categories $GRP$, $CAT$, and $TOP$ of large groups, categories, and spaces.

Note that the theory could be [[algebraic theory|algebraic]], as for $Grp$, or [[essentially algebraic theory|essentially algebraic]], as for $Cat$, or even [[higher-order logic|higher-order]], as for $Top$.  We will refer to this as the **logical enlargement**.  In practice, this enlargement usually suffices, but for theoretical reasons it would be nice to have a construction which works on *any* large category.


### Locally presentable enlargement

For any large category $C$, the very large [[presheaf category]] $[C^{op},SET]$ contains $C$ as a [[full subcategory]].  Furthermore, $[C^{op},SET]$ is $SET$-bicomplete, i.e. it has all large [[limits]] and [[colimits]], whether or not $C$ was $Set$-complete or cocomplete, and the [[Yoneda embedding]] $C \hookrightarrow [C^{op},SET]$ [[preserved limit|preserves]] all limits that exist in $C$.

However, it hardly preserves any *colimits* (since it is a [[free cocompletion]], after all).  If we want an enlargement of $C$ which preserves some class $\Phi$ of colimits in $C$, then we can restrict to the full subcategory of $[C^{op},SET]$ consisting of the presheaves $C^{op}\to SET$ which preserved limit the colimits $\Phi$ (i.e. take them to limits in $SET$).  Let's denote this category by $\Uparrow_\Phi C$.  Since [[representable functors]] preserve all limits, the Yoneda embedding of $C$ factors through $\Uparrow_\Phi C$, and all the colimits in $\Phi$ are preserved by this restricted embedding.

Moreover, $\Uparrow_\Phi C$ is closed under limits in $[C^{op},SET]$, so it is itself $SET$-complete.  And as long as the (diagrams sizes of the) colimits in $\Phi$ are at most *large*, then (by theorems of Day etc.) $\Uparrow_\Phi C$ is reflective in $[C^{op},SET]$, and hence also $SET$-cocomplete.  Since usually, the only colimits we might care about in a large category $C$ are *small*, a natural choice for $\Phi$ is the class of all small colimits existing in $C$.

We will refer to this $\Uparrow_\Phi C$ as the **locally presentable enlargement**, since it is a [[locally presentable category]] relative to $\mathbf{V}$.  (In fact, it is locally $\kappa$-presentable, where $\kappa$ is the [[cardinality]] of the first universe $\mathbf{U}$.)  Moreover, we have the following (where $\lambda Cts(A,B)$ denotes the category of $\lambda$-small-limit preserving functors).

+-- {: .un_theorem}
###### Theorem
Suppose $C$ is locally presentable relative to $\mathbf{U}$, so that there is a small cardinal $\lambda$ and a small category $A$ with $\lambda$-small colimits such that $C\simeq \lambda Cts(A^{op},Set)$.  If $\Phi$ denotes the class of all small colimits in $C$, then $\Uparrow_\Phi C \simeq \lambda Cts(A^{op},SET)$.
=--

Note that in this case, $\lambda Cts(A^{op},SET)$ is the category of large models of the theory (namely $A^{op}$) of which $C$ is the category of small ones.  Thus, the theorem says that when $C$ is locally presentable, the locally presentable enlargement is the same as the logical one.

+-- {: .proof}
###### Proof
Write $C' \coloneqq \lambda Cts(A^{op},SET)$.  Then we have a full embedding $C\hookrightarrow C'$, which preserves limits and colimits since they are calculated in the same way in both categories.

Now every object of $C$ is a small colimit of objects of $A$, and the objects of $A$ are all $\lambda$-presentable in $C$ and in $C'$.  Thus, every object of $C$ is $\kappa$-presentable in $C'$, where $\kappa$ is the size of the universe $\mathbf{U}$.  Conversely, since $C'$ is locally $\lambda$-presentable (relative to $\mathbf{V}$), any $\kappa$-presentable object in it is a $\kappa$-small colimit of $\lambda$-presentable objects---so since $C$ is closed under small colimits in $C'$, it must consist exactly of the $\kappa$-presentable objects.  However, since $C'$ is locally $\lambda$-presentable, it is also locally $\kappa$-presentable, so this implies that $C' \simeq \kappa Cts(C^{op},SET)$.  But $\kappa Cts(C^{op},SET)$ is precisely $\Uparrow_\Phi C$.
=--

However, if $C$ is not locally presentable, then its logical and locally-presentable enlargements can disagree.  In fact, they will *usually* disagree in this case, since if $C$ is not locally presentable relative to $\mathbf{U}$, its logical enlargement will usually not be locally presentable relative to $\mathbf{V}$ either, whereas its locally-presentable enlargement is, by definition, locally presentable relative to $\mathbf{V}$.  For example, the logical and locally presentable enlargements of $Top$ are quite different.


### Accessible enlargement

There is a simple modification of the locally-presentable enlargement which makes it agree with the logical enlargement for all [[accessible categories]], not just locally presentable ones.  Namely, instead of $\kappa Cts(C^{op},SET)$, we consider $\kappa Flat(C^{op},SET)$, the category of $\kappa$-[[flat functors]] (functors that "would preserve all $\kappa$-small limits if they existed").  We call this the **accessible enlargement**.

Essentially the same proof as for the theorem above shows that if $C$ is accessible relative to $\mathbf{U}$, hence $C\simeq \lambda Flat(A^{op},Set)$, then the accessible enlargement is equivalent to $\lambda Flat(A^{op},SET)$, which is of course the logical enlargement.

Note that if $C$ has all small limits, then its accessible and locally-presentable enlargements are the same, since a functor defined on a category with $\kappa$-small limits is $\kappa$-continuous iff it is $\kappa$-flat.  However, if $C$ does not have small limits, then its locally-presentable enlargement *does* have all large limits, whereas its accessible enlargement does not.

Thus, when $C$ is "poorly behaved," its accessible enlargement is "closer to it" (in particular, identical to its logical enlargement if $C$ is accessible) and thus equally poorly behaved, whereas its locally-presentable enlargement is further from it, but better behaved (complete and cocomplete).  For some purposes one may want one of these behaviors; for other purposes one may want the other.

## Monoidal enlargements

One may further ask for an enlargement which inherits whatever additional structure $C$ has, such as [[monoidal category|monoidal structure]].  The logical enlargement will usually inherit such structure trivially, while the [[Day convolution]] theorem implies that when $C$ is monoidal, so is its locally-presentable enlargement---and moreover, the latter is [[closed monoidal category|closed]] even if $C$ is not!


## References

* Sections 2.6 and 3.11--3.12 of [Basic Concepts of Enriched Category](http://tac.mta.ca/tac/reprints/articles/10/tr10abs.html).

* [Blog post](http://golem.ph.utexas.edu/category/2010/11/universe_enlargement.html)

[[!redirects universe enlargements]]
[[!redirects change of universe]]
[[!redirects changes of universe]]

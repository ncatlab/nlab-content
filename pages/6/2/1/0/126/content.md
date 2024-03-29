
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
=--
=--


# Subcategories
* table of contents
{: toc}


## Definition

Given a [[category]] $C$, a __subcategory__ $D$ consists of a subcollection of the collection of [[object|objects]] of $C$ and a subcollection of the collection of [[morphism|morphisms]] of $C$ such that:

* If the morphism $f : x \to y$ is in $D$, then so are $x$ and $y$.

* If $f : x \to y$ and $g : y \to z$ are in $D$, then so is the [[composition|composite]] $g f : x \to z$.  

* If $x$ is in $D$ then so is the [[identity morphism]] $1_x$.

These conditions ensure that $D$ is a category in its own right and the inclusion $D\hookrightarrow C$ is a [[functor]].  Additionally, we say that $D$ is...

* A __[[full subcategory]]__ if for any $x$ and $y$ in $D$, every morphism $f : x \to y$ in $C$ is also in $D$ (that is, the inclusion [[functor]] $D\hookrightarrow C$ is [[full functor|full]]).

* A __[[replete subcategory]]__ if for any $x$ in $D$ and any isomorphism $f:x\cong y$ in $C$, both $y$ and $f$ are also in $D$.

* A __[[wide subcategory]]__ if every object of $C$ is also an object of $D$.


## Variants in accord with the principle of equivalence
 {#VariantsInAccordWithThePrincipleOfEquivalence}

Just as subsets of a [[set]] $X$ can be identified with isomorphism classes of [[monomorphism|monic]] functions into $X$, subcategories of a category $C$ can be identified with isomorphism classes of monic _functors_ into $C$.  A functor is easily verified to be monic iff it is [[faithful functor|faithful]] and injective on objects.  This can be generalized to monomorphisms in a [[strict 2-category]].

However, this notion violates the [[principle of equivalence]] since being injective-on-objects refers to equality of objects.  This raises the question: what is a good definition of **subobject** in a [[2-category]] in accord with the [[principle of equivalence]]?  It is the contention of the authors of this page that there are multiple such definitions.  Two evident ones are:

* A morphism $f: A\to B$ in a 2-category $K$ is **1-monic** if it is [[fully faithful|full and faithful]], i.e. $K(X,A) \to K(X,B)$ is full and faithful for all $X$.  A **1-subobject** of $B$ is an [[equivalence]] class of 1-monomorphisms into $B$, and a **1-subcategory** is a 1-subobject in $Cat$.
* Likewise, $f$ is **2-monic** if $K(X,A) \to K(X,B)$ is faithful for all $X$.  A **2-subobject** of $B$ is an equivalence class of 2-monomorphisms into $B$, and a **2-subcategory** is a 2-subobject in $Cat$.

The obvious generalizations (at least, obvious once you start thinking in terms of $k$-[[k-surjective functor|surjectivity]]) are that every morphism is 3-monic, while the 0-monic morphisms are the equivalences.  (Note that this numbering is offset by one from that used in [Baez and Shulman](http://arxiv.org/abs/math.CT/0608420).)  There is likewise an evident generalization to $k$-monomorphisms in any $n$-[[n-category|category]].

It is fairly undisputed that 1-subobjects, as defined above, are a good notion of subobject in a 2-category.  In particular, any [[full and faithful functor]] $C\to D$ in $Cat$ is [[equivalence of categories|equivalent]] to the inclusion of a [[full subcategory]] $C'\to D$ (here $C'$ is the full image of $C$).  Also, in a 1-category considered as a locally discrete 2-category, the 1-monomorphisms are precisely the usual sort of [[monomorphism]].

In fact, any faithful functor is likewise equivalent to the inclusion of a (non-full) subcategory, but in this case the codomain must be modified as well as the domain.  It is somewhat more disputable whether 2-subcategories all deserve to be called "subcategories;" for instance, is [[Grp]] a "subcategory" of [[Set]]?  Note also that any functor between [[discrete category|discrete categories]] is faithful, so that the [[terminal category]] has a proper class of inequivalent 2-subcategories, and similarly every morphism in a locally discrete 2-category is 2-monic.  However, kernels of morphisms between 2-groups are 2-subobjects, not 1-subobjects, and likewise for any subgroup of a [[group]] (considered as a 1-object category).  This motivates the term "2-subobject," to make it clear that there is some relationship with the sort of subobjects we are used to in 1-categories, but also some notable generalization.

Other types of morphism in a 2-category which have some claim to be considered "subobjects" include [[pseudomonic functor|pseudomonic]] morphisms and [[conservative functor|conservative]] morphisms.  Pseudomonic morphisms might merit a name such as **(2,1)-subcategory**, since a functor is pseudomonic iff it is faithful (a 2-subcategory) and its induced functor between [[underlying groupoid]]s is fully faithful (a 1-subcategory).  See also [[stuff, structure, property]].

### As Displayed Categories

A different way to describe subcategories is as [[displayed categories]] satisfying certain properties. This is analogous to defining a [[subset]] by its [[characteristic function]], which allows to define subsets without a notion of global membership.

A __subcategory__ of a category $C$ is a displayed category $D$ over $C$ such that all $D(c)$ and $D_f(A,B)$ are [[mere proposition|propositions]]. We can recover a subcategory in the original sense by taking the [[Grothendieck construction]] of $D$. The identity and composition in the displayed category correspond precisely to the inclusion of the subcategory being closed under identity and composition.

We can also capture the above flavors of subcategory by adding further conditions to $D$. We say $D$ is...

* A __full subcategory__ if all $D_f(A,B)$ are true.
* A __wide subcategory__ if all $D(c)$ are true.
* A __replete subcategory__ if $D$ is an [[isofibration]].

## Related concepts

[[!include notions of subcategory]]

* [[embedding of categories]]

[[!redirects subcategory]]
[[!redirects subcategories]]
[[!redirects inclusion functor]]
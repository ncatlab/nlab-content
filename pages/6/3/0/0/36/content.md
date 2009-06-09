#Idea#

Many structures whose "traditional" definition takes place in [[Set]] can be formulated "internally" to any other category (or categorical structure) $C$ with "enough structure."  The structure required on $C$ is often referred to as a [[doctrine]], although it is not necessarily obvious that it will always be a doctrine in the formal sense (that is, a [[2-monad]], possibly in a weak sense, on [[Cat]]).

Like [[vertical categorification|categorification]] or [[horizontal categorification|oidification]], there is currently no completely general formal definition of this process, although there are one or two fairly general theorems.  However, its reverse is precise: given a doctrine $D$ to which $\Set$ (or some canonical Set-like category) belongs and a definition of foo internalized in the doctrine $D$, if this definition of foo in $\Set$ reduces to the usual definition of foo, then the definition is acceptable; foos are a _deinternalisation_ of internal foos.

#Examples#

* [[monoid|Monoids]] can be internalized in the doctrine of [[monoidal category|monoidal categories]].  For example:

  * A [[ring]] is a monoid internal to [[Ab]] with its usual tensor product.

  * An [[algebra]] is a monoid internal to [[Vect]], with its usual tensor product.

  * A strict monoidal category is a monoid internal to [[Cat]], with its cartesian product.

* Since any category with finite [[product|products]] is a [[cartesian monoidal category]], monoids can also be internalized in the doctrine of categories with finite products.

* [[group|Groups]] can also be internalized in the doctrine of categories with finite products, but not in the doctrine of monoidal categories, since diagonal maps are necessary to define what it means to have inverses.

* Monoids can also be internalized in the doctrine of [[multicategory|multicategories]].

* Commutative monoids can be internalized in the doctrine of [[symmetric monoidal category|symmetric monoidal categories]].

* Categories and groupoids can be internalized in the doctrine of [[finitely complete category|lex categories]], producing the notion of [[internal category]].

  * The classical fact that monoids can be identified with one-object categories has the following internal analogue: monoids in a lex category $C$ (qua category with finite products) can be identified with categories internal to $C$ whose object-of-objects is [[terminal object|terminal]].  However, monoids in a non-cartesian monoidal category (such as $Ab$ or $Vect$) cannot, in general, be identified with any sort of internal category.

* [[ring|Rings]] can be internalized in the doctrine of categories with finite products.

* More generally, the algebras for any [[Lawvere theory]] can be internalized in the doctrine of categories with finite products, and the algebras for any (symmetric) [[operad]] (in $Set$) can be internalized in the doctrine of (symmetric) monoidal categories.

* Pretty much any structure at all in mathematics can be internalized in a [[topos]].  Note, though, that since the [[internal logic]] of a topos is constructive, differences in axiomatization that make no difference classically can result in actual differences in behavior in a topos.  See [[constructive mathematics]] for some examples.  On the other hand, if the topos satisfies the [[axiom of choice]] (and in particular is [[Boolean topos|Boolean]]), then this complication won\'t happen.

#Internalization versus enrichment#

In the case of categories, there is a dichotomy between [[internal category|internal categories]] and [[enriched category|enriched categories]], both of which are ways of generalizing the notion of category.  In some cases, one is a special case of the other, but in general they are incomparable.

As described on this page, __internalization__ is a quite general phenomenon, of which internal categories are a particular case. However, the distinction between "internalization" and "enrichment" becomes less clear in generality.  For example, in addition to categories enriched over a monoidal category, one can define categories enriched over a [[bicategory]] or an [[fc-multicategory]]. It then turns out that a category enriched over the bicategory (or fc-multicategory) of [[span|spans]] in a lex category $C$ _which has one object_ is precisely an _internal_ category in $C$.

Perhaps from the perspective of this page, internal categories and enriched categories are just two _different_ ways of internalizing the notion of category in two _different_ doctrines?

#General Results#

Often, the structure on the ambient category $C$ allowing a certain type of structure to be internalized in it is itself a [[vertical categorification|categorified]] version of that same structure (for example, monoids in monoidal categories).  This is an example of the [microcosm principle](http://golem.ph.utexas.edu/category/2008/12/the_microcosm_principle.html).

As one formal result along these lines, Tom Leinster has shown that for any [[cartesian monad]] $T$, $T$-algebras can be naturally internalized/enriched in $T$-multicategories, and in particular in $T$-structured categories.  For example, when $T$ is the monad whose algebras are monoids, this says that monoids can be internalized in multicategories and monoidal categories.

On the other hand, this is not always true.  For example, the categorification of a [[rig]] is a [[rig category]], but it is difficult to see how to define a rig internal to a rig category, and the usual definition of rig in $Set$ does not use the rig-category structure of $Set$ but only that it has finite products.

A very different sort of general result has to do with the [[internal logic]] of certain categories.  If a category has enough structure to interpret a certain fragment of first-order logic, then any first-order theory definable in that fragment can be internalized in that category. For example, the theory of categories can be formulated in [[cartesian logic]] and thus is interpretable in any cartesian (= lex) category. The statement that almost anything can be internalized in a topos is the high-end case of this, since the internal logic of a topos is full intuitionistic type theory.

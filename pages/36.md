
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Any [[mathematical structure]] whose traditional [[Bourbaki]]-style definition is formulated within [[set theory]] can be formulated *internally* to any [[category]]that admits all those types of operations (usually: [[universal constructions]]) on its [[objects]] that the traditional definition applies to [[sets]], hence to the [[objects]] of the [[base topos|base]] category of [[Sets]].

* If the category is equipped with the structure of a [[site]], then geometrical notions, such as defining [[morphisms]] locally on the domain with patching conditions (or more generally [[descent]] theory), exist inside it. 

* If it is a [[finitely complete category]], the existence of [[finite products]] and [[terminal objects]] means that [[variety of algebras|varieties of algebras]] can be defined. 

* If the category is a [[topos]] with a [[natural numbers object]], then one can do a certain sort of "ordinary" mathematics inside it, specifically [[predicative mathematics|impredicative]] [[constructive mathematics]] without the fancier tools of [[model theory]] or (ironically) [[category theory]].

* Further extra conditions on the category, such as being a [[Boolean topos]] or being a [[superextensive site]], bring the internal mathematics closer to that of $Set$.

* If the category is a [[(infinity,1)-topos]], then one could do most of ordinary constructive mathematics inside of it, including category theory, set theory, model theory, and higher category theory. Adding the [[principle of excluded middle]] or the [[axiom of choice|axiom]] of [[choice object|choice set]]/[[0-groupoids]] results in internal classical mathematics. 

The structure required on $C$ is often referred to as a [[doctrine]].  The question of what exactly a "doctrine" is is a tricky one, but for purposes of this page, we take a "doctrine" to mean a certain type of structure (or [[property-like structure]]) with which a category can be equipped.  For example, there is a doctrine of monoidal categories, a doctrine of categories with finite limits, a doctrine of cartesian closed categories, and so on.

Like [[vertical categorification|categorification]] or [[horizontal categorification|oidification]], there is currently no completely general formal definition of this process, although there are one or two fairly general theorems.  However, its reverse is precise: given a doctrine $D$ to which $\Set$ (or some canonical Set-like category) belongs and a definition of foo internalized in the doctrine $D$, if this definition of foo in $\Set$ reduces to the usual definition of foo, then the definition is acceptable; foos are a _deinternalisation_ of internal foos.


## Examples

* [[monoid|Monoids]] can be internalized in the doctrine of [[monoidal category|monoidal categories]] ([[monoid objects]]).  For example:

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

* Categories themselves can be internalised, as algebras of an [[essentially algebraic theory]] (giving [[strict categories]]), in any [[finitely complete category]]; see [[internal category]].


## Internalization versus enrichment

In the case of categories, there is a dichotomy between [[internal category|internal categories]] and [[enriched category|enriched categories]], both of which are ways of generalizing the notion of category.  In some cases, one is a special case of the other, but in general they are incomparable.

As described on this page, __internalization__ is a quite general phenomenon, of which internal categories are a particular case. However, the distinction between "internalization" and "enrichment" becomes less clear in generality.  For example, in addition to categories enriched over a monoidal category, one can define categories enriched over a [[bicategory]] or an [[virtual double category]]. It then turns out that a category enriched over the bicategory (or virtual double category) of [[span|spans]] in a lex category $C$ _which has one object_ is precisely an _internal_ category in $C$.

Perhaps from the perspective of this page, internal categories and enriched categories are just two _different_ ways of internalizing the notion of category in two _different_ doctrines?


## General Results

Often, the structure on the ambient category $C$ allowing a certain type of structure to be internalized in it is itself a [[vertical categorification|categorified]] version of that same structure (for example, monoids in monoidal categories).  This is an example of the [microcosm principle](http://golem.ph.utexas.edu/category/2008/12/the_microcosm_principle.html).

As one formal result along these lines, [[Tom Leinster]] has shown that for any [[cartesian monad]] $T$, $T$-algebras can be naturally internalized/enriched in $T$-multicategories, and in particular in $T$-structured categories.  For example, when $T$ is the monad whose algebras are monoids, this says that monoids can be internalized in multicategories and monoidal categories.

On the other hand, this is not always true.  For example, the categorification of a [[rig]] is a [[rig category]], but it is difficult to see how to define a rig internal to a rig category, and the usual definition of rig in $Set$ does not use the rig-category structure of $Set$ but only that it has finite products.

A very different sort of general result has to do with the [[internal logic]] of certain categories.  If a category has enough structure to interpret a certain fragment of first-order logic, then any first-order theory definable in that fragment can be internalized in that category. For example, the theory of categories can be formulated in [[cartesian logic]] and thus is interpretable in any cartesian (= lex) category. The statement that almost anything can be internalized in a topos is the high-end case of this, since the internal logic of a topos is full intuitionistic type theory.

## Examples

* [[monoid object]], 

* [[group object]], 

* [[ring object]], 

* [[monoid object in an (∞,1)-category]]

* [[Lie algebra object]]

* [[action object]]

* [[internal category]], [[internal diagram]], [[internal groupoid]], [[groupoid object in an (∞,1)-category]], [[category object in an (∞,1)-category]]

* [[internal (co-)limit]]

* [[internal site]], [[internal locale]]


* [[internal logic]]



## References
 {#References}

On internalization with focus on [[H-spaces]], [[internal monoids]] and [[internal groups]] (and proving the [[Eckmann-Hilton argument]]):

* [[Beno Eckmann]], [[Peter Hilton]], *Structure maps in group theory*, Fundamenta Mathematicae 50 (1961), 207-221 ([doi:10.4064/fm-50-2-207-221](https://www.impan.pl/en/publishing-house/journals-and-series/fundamenta-mathematicae/all/50/2/94854/structure-maps-in-group-theory))

* [[Beno Eckmann]], [[Peter Hilton]], _Group-like structures in general categories I multiplications and comultiplications_, Math. Ann. 145, 227–255 (1962) ([doi:10.1007/BF01451367](https://doi.org/10.1007/BF01451367))

* [[Beno Eckmann]], [[Peter Hilton]], _Group-like structures in general categories III primitive categories_,  Math. Ann. **150** 165–187 (1963) ([doi:10.1007/BF01470843](https://doi.org/10.1007/BF01470843)) 

Highlighting the role of the [[Yoneda lemma]] in internalization:

* [[Saunders MacLane]], Section III.6 in: _[[Categories for the Working Mathematician]]_, Springer (1971) 

Moreover with discussion of [[action objects]]:

* [[Saunders Mac Lane]], [[Ieke Moerdijk]], Section V.6 of: _[[Sheaves in Geometry and Logic]]_, Springer 1992 ([doi:10.1007/978-1-4612-0927-0](https://link.springer.com/book/10.1007/978-1-4612-0927-0))

* [[Francis Borceux]], [[George Janelidze]], [[Gregory Maxwell Kelly]], around p. 8 of: _Internal object actions_, Commentationes Mathematicae Universitatis Carolinae (2005) Volume: 46, Issue: 2, page 235-255 ([dml:249553](https://eudml.org/doc/249553))

See also:

* Tao Lu, Zhenzhen Zhu, _The Action of Group Object in A Topos_,   Proceedings of:  _2015 International Conference on Management, Education, Information and Control_ ([doi:10.2991/meici-15.2015.312](https://doi.org/10.2991/meici-15.2015.312))

More general internalization via [[sketches]]:

* [[Andrée Bastiani]], [[Charles Ehresmann]], _Categories of sketched structures_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, Tome 13 (1972) no. 2, pp. 104-214 ([numdam:CTGDC_1972__13_2_104_0](http://www.numdam.org/item/?id=CTGDC_1972__13_2_104_0))

* [[Michael Barr]], [[Charles Wells]], Section 4 of: _[[Toposes, Triples, and Theories]]_, Originally published by: Springer-Verlag, New York, 1985, republished in: Reprints in [Theory and Applications of Categories, No. 12 (2005) pp. 1-287](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)


For more see at:

* [[algebra over a Lawvere theory|algebras over]]$\,$ [[algebraic theories]]

* [[algebra over a monad|algebras over]]$\,$ [[monads]]

* [[algebra over an operad|algebras over]]$\,$ [[operads]]





[[!redirects Internalization]]
[[!redirects internal]]
[[!redirects internal to]]
[[!redirects internally]]
[[!redirects internally to]]
[[!redirects internalisation]]
[[!redirects internalization]]

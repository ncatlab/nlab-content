#The Idea#

The idea of an enriched category is that we take the definition of [[locally small category]] and replace the [[hom-set|hom-sets]] by objects in some [[monoidal category]] $K$.  So, a _category enriched over $K$_, say $C$, has a collection $C_0$ of objects and for each pair $x,y \in C_0$, a 'hom-object' 
$$ hom(x,y) \in K .$$
We then mimic the usual definition of category.  In particular, composition is a morphism in $K$:
$$ \circ : hom(y,z) \otimes hom(x,y) \to hom(x,z)  $$
where $\otimes$ is the tensor product in $K$.

We may similarly define a _functor enriched over $K$_
and a _natural transformation enriched over $K$_.

More generally, we may allow $K$ to be a [[multicategory]], a [[bicategory]], a [[double category]], or an [[fc-multicategory]].

#The Details#

The details are an exercise for future contributors to this page. If you get stuck, try Max Kelly's book, cited in the page on [[enriched category theory]].

Also see John Armstrong's article: [Enriched categories](http://unapologetic.wordpress.com/2007/08/13/enriched-categories/). 

##Internalization versus Enrichment##

The idea of enriched categories is not unrelated to that of [[internal category|internal categories]], but is different.  One difference is that in a $K$-enriched category, the objects still form a _set_ (or a proper class) while the arrows are replaced by objects of $K$, while in a category internal to $K$, both the set of objects _and_ the set of arrows are replaced by objects of $K$.

Another difference is that for $K$-enriched categories, $K$ can be any monoidal category, while for $K$-internal categories, it must have pullbacks, which can be thought of as a generalization of [[cartesian monoidal category|cartesian monoidal structure]].  In particular, a $K$-internal category with one object (that is, whose object-of-objects is a [[terminal object]]) is a [[monoid]] in $K$ with respect to the cartesian product, whereas a one-object $K$-enriched category is a monoid in $K$ with respect to whatever monoidal structure we use to define enriched categories.

Nevertheless, internalization and enrichment are related in several ways.  On the one hand, internal categories and enriched categories are both instances of [[monad|monads]] in bicategories (the bicategory of spans and the bicategory of matrices, respectively).  On the other hand, when $K$ is an $\infty$-[[extensive category]], such as [[Set]] or [[simplicial set|simplicial sets]] (or more generally any [[Grothendieck topos]]), (small) $K$-enriched categories can be identified with $K$-internal categories whose object-of-objects is discrete (that is, a coproduct of copies of the terminal object).


#Examples#

* A [[horizontal categorification|ringoid]] is a category enriched over [[Ab]].
* An [[algebroid]] is a category enriched over [[Vect]].
* A [[strict 2-category]] is a category enriched over [[Cat]].

* A strict $n$-category is a category enriched over strict $(n-1)$-categories. In the limit $n \to \infty$ this leads to [[strict omega-category|omega-categories]].

(In all these cases the standard monoidal structure on the monoidal categories is understood.)

* A (Lawvere) [[metric space]] is a category enriched over the poset $([0, \infty], \geq)$ of extended positive real numbers, where $\otimes$ is $+$.
* A [[poset]] is a category enriched over the category of [[truth value]]s, where $\otimes$ is [[conjunction]].
* An [[apartness relation|apartness space]] is a [[groupoid]] enriched over the opposite of the category of truth values, where $\otimes$ is [[disjunction]].

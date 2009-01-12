#The Idea#

The idea of an enriched category is that we take the definition of [[locally small category]] and replace the [[hom-set|hom-sets]] by objects in some [[monoidal category]] $K$.  So, a _category enriched over $K$_, say $C$, has a collection $ob(C)$ of objects and for each pair $x,y \in ob(C)$, a 'hom-object' 
$$ hom(x,y) \in K .$$
We then mimic the usual definition of category.  In particular, composition is a morphism in $K$:
$$ \circ : hom(y,z) \otimes hom(x,y) \to hom(x,z)  $$
where $\otimes$ is the tensor product in $K$.

We may similarly define a _functor enriched over $K$_
and a _natural transformation enriched over $K$_, obtaining a [[strict 2-category]] of $K$-enriched categories.  By general 2-category theory, we thereby obtain notions of _$K$-enriched adjunction_, _$K$-enriched equivalence_, and so on.

There is also an enriched notion of [[limit]] called a [[weighted limit]], but it is somewhat more subtle (and in particular, it is difficult to construct purely on the basis of the 2-category $K$-Cat).

More generally, we may allow $K$ to be a [[multicategory]], a [[bicategory]], a [[double category]], or an [[fc-multicategory]].

#The Details#

The details are an exercise for future contributors to this page. If you get stuck, try Max Kelly's book, cited in the page on [[enriched category theory]].

Also see John Armstrong's article: [Enriched categories](http://unapologetic.wordpress.com/2007/08/13/enriched-categories/). 

##Passage between ordinary categories and enriched categories##

Every $K$-enriched category $C$ has an _underlying ordinary category_, usually denoted $C_0$, defined by $C_0(x,y) = K(I, hom(x,y))$ where $I$ is the unit object of $K$.

If $K(I, -): K \to Set$ has a left adjoint $- \cdot I: Set \to K$ (taking a set $S$ to the tensor or [[power|copower]] $S \cdot I$, viz. the coproduct of an $S$-indexed set of copies of $I$), then any ordinary category $C$ can be regarded as enriched in $K$ by forming the composite  

$$Ob(C) \times Ob(C) \stackrel{\hom}{\to} Set \stackrel{-\cdot I}{\to} K$$

More generally, a (lax) [[monoidal functor]] $F: K \to L$ between monoidal categories can be regarded as a "change of base", so that by applying $F$, any category enriched over $K$ can be seen as enriched over $L$. 

##Internalization versus Enrichment##

The idea of enriched categories is not unrelated to that of [[internal category|internal categories]], but is different.  One difference is that in a $K$-enriched category, the objects still form a _set_ (or a proper class) while the arrows are replaced by objects of $K$, while in a category internal to $K$, both the set of objects _and_ the set of arrows are replaced by objects of $K$.

Another difference is that for $K$-enriched categories, $K$ can be any monoidal category, while for $K$-internal categories, it must have pullbacks, which can be thought of as a generalization of [[cartesian monoidal category|cartesian monoidal structure]].  In particular, a $K$-internal category with one object (that is, whose object-of-objects is a [[terminal object]]) is a [[monoid]] in $K$ with respect to the cartesian product, whereas a one-object $K$-enriched category is a monoid in $K$ with respect to whatever monoidal structure we use to define enriched categories.

Nevertheless, internalization and enrichment are related in several ways.  On the one hand, internal categories and enriched categories are both instances of [[monad|monads]] in bicategories (the bicategory of spans and the bicategory of matrices, respectively).  On the other hand, when $K$ is an $\infty$-[[extensive category]], such as [[Set]] or [[simplicial set|simplicial sets]] (or more generally any [[Grothendieck topos]]), (small) $K$-enriched categories can be identified with $K$-internal categories whose object-of-objects is discrete (that is, a coproduct of copies of the terminal object).


#Examples#

* A category enriched in [[Set]] is a [[locally small]] category.

* A category enriched in [[chain complex|chain complexes]] is a [[DG-category]].

* A category enriched in [[simplicial set|simplicial sets]] is a [[simplicially enriched category|simplicial category]], and are one model for $(\infty,1)$-[[(infinity,1)-category|categories]].

* Categories enriched in [[Top]] are also a model for $(\infty,1)$-categories.

* A category enriched in [[Cat]] is a [[strict 2-category]].

* A strict $n$-category is a category enriched over strict $(n-1)$-categories. In the limit $n \to \infty$ this leads to [[strict omega-category|strict omega-categories]].

* A [[horizontal categorification|ringoid]] is a category enriched over [[Ab]].

* An [[algebroid]] is a category enriched over [[Vect]].

(In all these cases the standard monoidal structure on the monoidal categories is understood.)

* A (Lawvere) [[metric space]] is a category enriched over the poset $([0, \infty], \geq)$ of extended positive real numbers, where $\otimes$ is $+$.

* An [[ultrametric space]] is a category enriched over the poset $([0, \infty], \geq)$ of extended positive real numbers, where $\otimes$ is $\max$.

* A [[poset]] is a category enriched over the category of [[truth value]]s, where $\otimes$ is [[conjunction]].

* An [[apartness relation|apartness space]] is a [[groupoid]] enriched over the opposite of the category of truth values, where $\otimes$ is [[disjunction]].

* A [[group torsor]] (over a group $G$) is an (occupied) category enriched over the category whose objects are elements of $G$ and whose only morphisms are identity arrows, and where $\otimes$ is the group operation.


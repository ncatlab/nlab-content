#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

The idea of an enriched category is that we take the definition of [[locally small category]] and replace the [[hom-set|hom-sets]] by objects in some [[monoidal category]] $K$.  So, a __category enriched over $K$__ (also called a __category enriched in $K$__, or simply a __$K$-category__), say $C$, has a collection $ob(C)$ of objects and for each pair $x,y \in ob(C)$, a '[[hom-object]]' 
$$ hom(x,y) \in K .$$
We then mimic the usual definition of category.  In particular, composition is a morphism in $K$:
$$ \circ : hom(y,z) \otimes hom(x,y) \to hom(x,z)  $$
where $\otimes$ is the tensor product in $K$.

We may similarly define a _functor enriched over $K$_
and a _natural transformation enriched over $K$_, obtaining a [[strict 2-category]] of $K$-enriched categories.  By general 2-category theory, we thereby obtain notions of _$K$-enriched adjunction_, _$K$-enriched equivalence_, and so on.

There is also an enriched notion of [[limit]] called a [[weighted limit]], but it is somewhat more subtle (and in particular, it is difficult to construct purely on the basis of the 2-category $K$-Cat).

More generally, we may allow $K$ to be a [[multicategory]], a [[bicategory]], a [[double category]], or an [[fc-multicategory]].

See also [[enriched category theory]].

#Definition#


Let $V$ be a [[monoidal category]] with

* tensor product $\otimes : C \times C \to C$;

* tensor unit $I \in Obj(V)$;

* associator $\alpha_{a,b,c} : (a \otimes b)\otimes c \to a \otimes (b \otimes c)$;

* left unitor $l_a : I \otimes a \to a$;

* right unitor $r_a : a \otimes I \to a$.

A (small) **$V$-category** $C$ (or **$V$-enriched category** or **category enriched over/in $V$**) is

* a [[set]] $Obj(C)$ -- called the set of objects;

* for each ordered pair $(a,b) \in Obj(C) \times Obj(C)$ of objects in $C$ an object $C(a,b) \in Obj(V)$ -- called the [[hom-object]] or _object of morphisms_ from $a$ to $b$;

* for each ordered triple $(a,b,c)$ of objects of $V$ a morphism $\circ_{a,b,c} : C(b,c) \otimes C(a,b) \to C(a,c)$ in $V$ -- called the _composition morphism_;

* for each object $a \in Obj(V)$ a morphism $j_a : I \to C(a,a)$ -- called the _identity [[global element|element]]_ 

* such the following diagrams commute:

for all $a,b,c,d \in Obj(V)$:

$$
  \array{
     (C(c,d)\otimes C(b,c)) \otimes C(a,b)
     &&\stackrel{\alpha}{\to}&&
     C(c,d) \otimes (C(b,c) \otimes C(a,b))
     \\
     \downarrow^{\circ_{b,c,d}\otimes Id_{C(a,b)}} 
     &&&& \downarrow^{Id_{C(c,d)\otimes \circ_{a,b,c}}}
     \\
     C(b,d)\otimes C(a,b)
     &\stackrel{\circ_{a,b,c}}{\to}&
       C(a,d)
     &\stackrel{\circ_{a,c,d}}{\leftarrow}&
     C(c,d) \otimes C(a,c)
  }
$$ 

this says that composition in $C$ is _associative_;

and

$$
  \array{
    C(b,b)\otimes C(a,b)
    &\stackrel{\circ_{a,b,b}}{\to}&
    C(a,b)
    &\stackrel{\circ_{a,a,b}}{\leftarrow}&
    C(a,b) \otimes C(a,a)
    \\
    \uparrow^{j_b \otimes Id_{C(a,b)}}
    & \nearrow_{l}&& {}_r\nwarrow& 
    \uparrow^{Id_{C(a,b)}\otimes j_a}
    \\
    I \otimes C(a,b)
    &&&&
    C(a,b) \otimes I
  }
$$

this says that composition is _unital_.


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

* A category enriched in [[Set]] is a [[locally small category]].

* A category enriched in [[chain complex|chain complexes]] is a [[dg-category]].

* A category enriched in [[simplicial set|simplicial sets]] is a [[simplicially enriched category|simplicial category]], and are one model for $(\infty,1)$-[[(infinity,1)-category|categories]].

* Categories enriched in [[Top]] are also a model for $(\infty,1)$-categories.

* A category enriched in [[Cat]] is a [[strict 2-category]].

* A strict $n$-category is a category enriched over strict $(n-1)$-categories. In the limit $n \to \infty$ this leads to [[strict omega-category|strict omega-categories]].

* A [[ringoid]] is a category enriched over [[Ab]].

* An [[algebroid]] is a category enriched over [[Vect]].

(In all these cases the standard monoidal structure on the monoidal categories is understood.)

* A (Lawvere) [[metric space]] is a category enriched over the poset $([0, \infty], \geq)$ of extended positive real numbers, where $\otimes$ is $+$.

* An [[ultrametric space]] is a category enriched over the poset $([0, \infty], \geq)$ of extended positive real numbers, where $\otimes$ is $\max$.

* A [[partial order|poset]] is a category enriched over the category of [[truth value]]s, where $\otimes$ is [[conjunction]].

* An [[apartness relation|apartness space]] is a [[groupoid]] enriched over the opposite of the category of truth values, where $\otimes$ is [[disjunction]].

* A [[group torsor]] (over a group $G$) can be modeled by a category enriched over the [[discrete category]] on the set $G$, where $\otimes$ is the group operation.  Not every such category determines a torsor, however; it must be nonempty as well as [[Cauchy complete category|Cauchy complete]].


#References#

The standard reference on enriched categories is

* G. M. Kelly, _Basic concepts of enriched category theory_ ([tac](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html) ,[pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))



#Blog entries#

* John Armstrong: [Enriched categories](http://unapologetic.wordpress.com/2007/08/13/enriched-categories/).


[[!redirects enriched categories]]
[[!redirects category enriched]]
[[!redirects categories enriched]]
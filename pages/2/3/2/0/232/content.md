+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The notion of _enriched category_ is a generalization of the notion of [[category]].

Very often instead of merely having a _[[set]]_ of [[morphism]]s from one [[object]] to another, a category will have a _[[vector space]]_ of morphisms, or a _[[topological space]]_ of morphisms, or some other such thing.  This suggests that we should take the definition of ([[locally small category|locally small]]) category and generalize it by replacing the [[hom-set]]s by _hom-objects_ , which are objects in a suitable category $K$.
This gives the concept of 'enriched category'.

The category $K$ must be [[monoidal category|monoidal]], so that we can define composition as a morphism
$$ \circ : hom(y,z) \otimes hom(x,y) \to hom(x,z)  $$
So, a __category enriched over $K$__ (also called a __category enriched in $K$__, or simply a __$K$-category__), say $C$, has a collection $ob(C)$ of objects and for each pair $x,y \in ob(C)$, a '[[hom-object]]' 
$$ hom(x,y) \in K .$$
We then mimic the usual definition of category.  

We may similarly define a _functor enriched over $K$_
and a _natural transformation enriched over $K$_, obtaining a [[strict 2-category]] of $K$-enriched categories, [[category of V-enriched categories|$K$-Cat]].  By general 2-category theory, we thereby obtain notions of _$K$-enriched adjunction_, _$K$-enriched equivalence_, and so on.

There is also an enriched notion of [[limit]] called a [[weighted limit]], but it is somewhat more subtle (and in particular, it is difficult to construct purely on the basis of the 2-category $K$-Cat).

More generally, we may allow $K$ to be a [[multicategory]], a [[bicategory]], a [[double category]], or a [[virtual double category]].

See also [[enriched category theory]].

## Definition

Ordinarily enriched categories have been considered as _enriched over_ a [[monoidal category]]. This is discussed in the section

* [Enrichment in a monoidal category](#InMonoidCat)

More generally, one may think of a monoidal category as a [[bicategory]] with a single object (so that the monoidal product becomes [[horizontal composition]]) and this way regard enrichment in a monoidal category as the special case of _enrichment in a bicategory_ . This is discussed in the section

* [Enrichment in a bicategory](#InBicat)

Enriched categories and [[enriched functors]] between them form themselves a category, the _[[category of V-enriched categories]]_.

### Enrichment in a monoidal category {#InMonoidCat}

Let $V$ be a [[monoidal category]] with

* tensor product $\otimes : V \times V \to V$;

* tensor unit $I \in Obj(V)$;

* associator $\alpha_{a,b,c} : (a \otimes b)\otimes c \to a \otimes (b \otimes c)$;

* left unitor $l_a : I \otimes a \to a$;

* right unitor $r_a : a \otimes I \to a$.

A (small) **$V$-category** $C$ (or **$V$-enriched category** or **category enriched over/in $V$**) is

* a [[set]] $Obj(C)$ -- called the set of objects;

* for each ordered pair $(a,b) \in Obj(C) \times Obj(C)$ of objects in $C$ an object $C(a,b) \in Obj(V)$ -- called the [[hom-object]] or _object of morphisms_ from $a$ to $b$;

* for each ordered triple $(a,b,c)$ of objects of $C$ a morphism $\circ_{a,b,c} : C(b,c) \otimes C(a,b) \to C(a,c)$ in $V$ -- called the _composition morphism_;

* for each object $a \in Obj(C)$ a morphism $j_a : I \to C(a,a)$ -- called the _identity [[global element|element]]_ 

* such the following diagrams commute:

for all $a,b,c,d \in Obj(C)$:

$$
  \array{
     (C(c,d)\otimes C(b,c)) \otimes C(a,b)
     &&\stackrel{\alpha}{\to}&&
     C(c,d) \otimes (C(b,c) \otimes C(a,b))
     \\
     \downarrow^{\circ_{b,c,d}\otimes Id_{C(a,b)}} 
     &&&& \downarrow^{Id_{C(c,d)}\otimes \circ_{a,b,c}}
     \\
     C(b,d)\otimes C(a,b)
     &\stackrel{\circ_{a,b,d}}{\to}&
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

#### Enrichment through lax monoidal functors #### 

If $V$ is a monoidal category, then an alternative way of viewing a $V$-category is as a set $X$ together with a (lax) [[monoidal functor]] $\Phi = \Phi_d$ of the form 

$$V^{op} \stackrel{yon_V}{\to} Set^{V} \stackrel{d}{\to} Set^{X \times X}$$ 

where the codomain is identified with the monoidal category of spans on $X$, i.e., the local hom-category $\hom(X, X)$ in the [[bicategory]] of [[span]]s of sets. Given an $V$-category $(X, d: X \times X \to V)$ under the ordinary definition, the corresponding monoidal functor $\Phi$ takes an object $v$ of $V^{op}$ to the span 

$$\Phi(v)_{x, y} := \hom_V(v, d(x, y))$$ 

Under the composition law, we get a natural map 

$$\hom(v, d(x, y)) \times \hom(v', d(y, z)) \to \hom(v \otimes v', d(x, y) \otimes d(y, z)) \stackrel{\hom(1, comp)}{\to} \hom(v \otimes v', d(x, z))$$ 

which gives the tensorial constraint $\Phi(v) \circ \Phi(v') \to \Phi(v \otimes v')$ for a monoidal functor; the identity law similarly gives the unit constraint. 

Conversely, by using a Yoneda-style argument, such a monoidal functor structure on $\Phi = \Phi_d$ induces an $M$-enrichment on $X$, and the two notions are equivalent. 

Alternatively, we can equivalently describe a $V$-enriched category as precisely a bicontinuous lax monoidal functor of the form 

$$Set^V \to Set^{X \times X}$$ 

since bicontinuous functors of the form $Set^V \to Set^{X \times X}$ are precisely those of the form $Set^d$ for some function $d: X \times X \to V$, at least if $V$ is [[Cauchy complete category|Cauchy complete]]. 

### Enrichment in a bicategory 
 {#InBicat}

Let $B$ be a [[bicategory]], and write $\otimes$ for horizontal (1-cell) composition (written in Leibniz order). A [[category enriched in a bicategory|category enriched in the bicategory]] $B$ consists of a [[set]] $X$ together with 

* A function $p: X \to B_0$, 
* A function $\hom: X \times X \to B_1$, satisfying the typing constraint $\hom(x, y): p(x) \to p(y)$, 
* A function $\circ: X \times X \times X \to B_2$, satisfying the constraint $\circ_{x, y, z}: \hom(y, z) \otimes \hom(x, y) \to \hom(x, z)$, 
* A function $j: X \to B_2$, satisfying the constraint $j_x: 1_{p(x)} \to \hom(x, x)$, 

such that the associativity and unitality diagrams, as written above, commute. Viewing a monoidal category $M$ as a 1-object bicategory $\Sigma M$, the notion of enrichment in $M$ coincides with the notion of enrichment in the bicategory $\Sigma M$. 

If $X$, $Y$ are sets which come equipped with enrichments in $B$, then a $B$-functor consists of a function $f: X \to Y$ such that $p_Y \circ f = p_X$, together with a function $f_1: X \times X \to B_2$, satisfying the constraint $f_1(x, y): \hom_X(x, y) \to \hom_Y(f(x), f(y))$, and satisfying equations expressing coherence with the composition and unit data $\circ$, $j$ of $X$ and $Y$. (Diagram to be inserted, perhaps.)

### Enrichment in a double category {#InDoubleCat}

It is also natural to generalize further to categories enriched in a (possibly weak) [[double category]].  Just like for a bicategory, if $D$ is a double category, then a $D$-**enriched category** $\mathbf{X}$ consists of a set $X$ together with

* for each $x\in X$, an object $p(x)$ of $D$,
* for each $x,y\in X$, a horizontal arrow $\hom(x, y)\colon p(x) \to p(y)$ in $D$, 
* for each $x,y,z\in X$, a 2-cell in $D$:
  $$\array{p(x) & \overset{hom(x,y)}{\to} & p(y) & \overset{hom(y,z)}{\to} & p(z) \\
  \Vert && \circ_{x,y,z} && \Vert\\
  p(x) && \underset{hom(x,z)}{\to} && p(z)}$$
* for each $x\in X$, a 2-cell in $D$:
  $$\array{p(x) & \overset{id}{\to} & p(x)\\
    \Vert && \Vert\\
    p(x) & \underset{hom(x,x)}{\to} & p(x)}$$

satisfying analogues of the associativity and unit conditions.  Note that is is exactly the same as a category enriched in the horizontal bicategory of $D$; the vertical arrows of $D$ play no role in the definition.  However, they *do* play a role when it comes to define functors between $D$-enriched categories.  Namely, if $\mathbf{X}$ and $\mathbf{Y}$ are $D$-enriched categories, then a $D$-functor $f\colon \mathbf{X}\to \mathbf{Y}$ consists of:

* a function $f\colon X\to Y$,
* for each $x\in X$ a vertical arrow $f_x\colon p_X(x) \to p_Y(f(x))$ in $D$,
* for each $x,y\in X$ a 2-cell in $D$:
  $$\array{p(x) & \overset{hom_X(x,y)}{\to} & p(y)\\
    ^{f_x}\downarrow && \downarrow^{f_y}\\
    p(f(x))& \underset{hom_Y(f(x),f(y))}{\to} & p(f(y))}$$

satisfying suitable equations.  If $D$ is vertically discrete, i.e. just a bicategory $B$ with no nonidentity vertical arrows, then this is just the same as a $B$-functor as defined above.  However, for many $D$ this notion of functor is more general and natural.


## Change of enriching category {#BaseChange}

### Passage between ordinary categories and enriched categories

Every $K$-enriched category $C$ has an [[underlying ordinary category]], usually denoted $C_0$, defined by $C_0(x,y) = K(I, hom(x,y))$ where $I$ is the unit object of $K$.

If $K(I, -): K \to Set$ has a left adjoint $- \cdot I: Set \to K$ (taking a set $S$ to the tensor or [[power|copower]] $S \cdot I$, viz. the coproduct of an $S$-indexed set of copies of $I$), then any ordinary category $C$ can be regarded as enriched in $K$ by forming the composite  

$$Ob(C) \times Ob(C) \stackrel{\hom}{\to} Set \stackrel{-\cdot I}{\to} K$$

These two operations form [[adjoint functors]] relating the [[2-category]] [[Cat]] to the 2-category $K$-Cat.

### Lax monoidal functors

More generally, any (lax) [[monoidal functor]] $F: K \to L$ between monoidal categories can be regarded as a "[[change of enriching category|change of base]]".  By applying $F$ to its hom-objects, any category enriched over $K$ gives rise to one enriched over $L$, and this forms a [[2-functor]] from $K$-Cat to $L$-Cat, and in fact from $K$-Prof to $L$-Prof; see [[profunctor]] and [[2-category equipped with proarrows]].

Moreover, this operation is itself functorial from $MonCat$ to $2Cat$.  In particular, any [[monoidal adjunction]] $K\rightleftarrows L$ gives rise to a [[2-adjunction]] $K Cat\rightleftarrows L Cat$ (and also for profunctors).  The adjunction $Cat \rightleftarrows K Cat$ described above is a special case of this arising from the adjunction $-\cdot I: Set \rightleftarrows K : K(I,-)$.

This and further properties of such "[[change of enriching category|change of base]]" are explored in [Crutwell 14](#Crutwell14)

##Internalization versus Enrichment

The idea of enriched categories is not unrelated to that of [[internal category|internal categories]], but is different.  One difference is that in a $K$-enriched category, the objects still form a _set_ (or a proper class) while the arrows are replaced by objects of $K$, while in a category internal to $K$, both the set of objects _and_ the set of arrows are replaced by objects of $K$.

Another difference is that for $K$-enriched categories, $K$ can be any monoidal category, while for $K$-internal categories, it must have pullbacks, which can be thought of as a generalization of [[cartesian monoidal category|cartesian monoidal structure]].  In particular, a $K$-internal category with one object (that is, whose object-of-objects is a [[terminal object]]) is a [[monoid]] in $K$ with respect to the cartesian product, whereas a one-object $K$-enriched category is a monoid in $K$ with respect to whatever monoidal structure we use to define enriched categories.

Nevertheless, internalization and enrichment are related in several ways.  On the one hand, internal categories and enriched categories are both instances of [[monad|monads]] in bicategories (the bicategory of spans and the bicategory of matrices, respectively) and so are both forms of [[generalized multicategory]].  On the other hand, when $K$ is an $\infty$-[[extensive category]], such as [[Set]] or [[simplicial set|simplicial sets]] (or more generally any [[Grothendieck topos]]), (small) $K$-enriched categories can be identified with $K$-internal categories whose object-of-objects is discrete (that is, a coproduct of copies of the terminal object).

Internalization and enrichment may also be understood as the result of interpreting the theory of categories seen respectively as an [[essentially algebraic theory]] and as a [generalized algebraic theory](generalized+algebraic+theory#relationship_to_enriched_categories). 

See also at [internal category](internal+category#InternalAndEnrichedCategories).

## Examples

* A category enriched in [[Set]] is a [[locally small category]].

* A category enriched in [[chain complexes]] is a [[dg-category]].

* A category enriched in [[simplicial sets]] is called a [[simplicially enriched category|simplicial category]], and these form one model for [[(∞,1)-categories]].  

  Beware: the term 'simplicial category' is also used to mean a category [[internalization|internal to]] simplicial sets.  In fact, a category enriched in simplicial sets is a special case of a category internal to simplicial sets, namely one where the simplicial set of objects is discrete.

* A category enriched in [[Top]] is a [[topologically enriched category]].  These are also a model for [[(∞,1)-categories]].  

  Again beware: the term 'topological category' is perhaps more commonly used to mean a category [[internalization|internal to]] Top.  People also use it for _[[topological concrete category]]_. And again: a category enriched in Top is a special case of one internal to Top, namely one where the space of objects is discrete.

* A category enriched in [[Cat]] is a [[strict 2-category]].

* A [[strict n-category]] is a category enriched over strict $(n-1)$-categories. In the limit $n \to \infty$ this leads to [[strict omega-category|strict omega-categories]].

* An [[algebroid]], or [[linear category]], is a category enriched over [[Vect]].  Here $Vect$ is the category of vector spaces over some fixed [[field]] $K$, equipped with its usual tensor product.  It is common to emphasize the dependence on $K$ and call a category enriched over Vect a **$K$-linear category**.  

* More generally, if $K$ is any [[commutative ring]], a category enriched over $K\,$[[Mod]] is sometimes called a $K$-linear category.

* In particular, taking $K$ to be $\mathbb{Z}$ (the ring of [[integers]]), a [[ringoid]] (or [[Ab-enriched category]]) is a category enriched over [[Ab]].

* A (Lawvere) [[metric space]] is a category enriched over the poset $([0, \infty], \geq)$ of extended positive real numbers, where $\otimes$ is $+$.

* An [[ultrametric space]] is a category enriched over the poset $([0, \infty], \geq)$ of extended positive real numbers, where $\otimes$ is $\max$.

* A [[preorder]] is a category enriched over the category of [[truth value]]s, where $\otimes$ is [[logical conjunction|conjunction]].

* An [[apartness relation|apartness space]] is a [[groupoid]] enriched over the opposite of the category of truth values, where $\otimes$ is [[disjunction]].

* A [[torsor]] over some group $G$ may be modeled by a category enriched over the [[discrete category]] on the set $G$, where $\otimes$ is the group operation.  Not every such category determines a torsor, however; it must be nonempty as well as [[Cauchy complete category|Cauchy complete]].

* [[F-categories]] are categories enriched over a subcategory of $Cat^{\to}$, and similarly [[M-categories]] are categories enriched over a subcategory of $Set^{\to}$.

* [[2-categories with contravariance]] (and generalizations such as [[3-categories with contravariance]]) can also be described as enriched categories.

* [[tangent bundle categories]] can be described as a certain kind of enriched category with certain [[powers]]; see [Garner 2018](#Garner2018) for details.

* [[Lawvere theories]] can be represented as enriched categories as well; see [Garner 2013](#Garner2014) and [Garner and Power 2017](#GarnerPower2017) for details. 

## Related concepts

* [[enriched monad]]

* [[enriched bicategory]]

* [[category enriched over a bicategory]]

* [[model structure on enriched categories]]

* [[enriched model category]]

* [[cartesian closed enriched category]], [[locally cartesian closed enriched category]]

* [[enriched (∞,1)-category]]

## References

Textbook accounts:

* [[Max Kelly]], _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press 1982, 245 pp. ([ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029)); 

  republished as:

  Reprints in Theory and Applications of Categories, No. 10 (2005) pp. 1-136 ([tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))

* [[Francis Borceux]], Chapter 6 of: _[[Handbook of Categorical Algebra]] Vol 2: Categories and Structures_, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994) ([doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865))

Also 

* [[Francis Borceux]], I. Stubbe, _Short introduction to enriched categories_ ([pdf](http://www-lmpa.univ-littoral.fr/~stubbe/PDF/EnrichedCatsKLUWER.pdf))

* [[Emily Riehl]], chapter 3 _Basics of enriched category theory_ in _[[Categorical Homotopy Theory]]_

Discussion of [[change of enriching category]] is in 

* {#Crutwell14} [[Geoff Cruttwell]], chapter 4 of _Normed spaces and the Change of Base for Enriched Categories_, 2014 ([pdf](http://pages.cpsc.ucalgary.ca/~gscruttw/publications/thesis4.pdf))

Vista of some modern generalizations is in

* [[Tom Leinster]], _Generalized enrichment for categories and multicategories_,  [math.CT/9901139](http://arxiv.org/abs/math.CT/9901139)

* [[Tom Leinster]], _Generalized enrichment of categories_, Journal of Pure and Applied Algebra __168__ (2002), no. 2-3, 391-406, [math.CT/0204279](http://arxiv.org/abs/math.CT/0204279)

* John Armstrong, _[Enriched categories](http://unapologetic.wordpress.com/2007/08/13/enriched-categories/)_

Further examples are discussed in

* {#Garner2013} [[Richard Garner]], *Lawvere theories, finitary monads and Cauchy-completion*, Journal of Pure and Applied Algebra, 2014, [arxiv](https://arxiv.org/abs/1307.2963)

* {#GarnerPower2017} [[Richard Garner]] and [[John Power]], *An enriched view on the extended finitary monad--Lawvere theory correspondence*, 2017 
([arXiv:1707.08694
](https://arxiv.org/abs/1707.08694)

* {#Garner2018} [[Richard Garner]], *An embedding theorem for tangent categories*, Advances in Mathematics, 2018, [doi](https://www.sciencedirect.com/science/article/pii/S0001870817303122), [arxiv](https://arxiv.org/abs/1704.08386)



[[!redirects enriched categories]]
[[!redirects category enriched]]
[[!redirects categories enriched]]

[[!redirects enriched groupoid]]
[[!redirects enriched groupoids]]

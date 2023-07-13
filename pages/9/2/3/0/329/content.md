
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


# Strict $2$-categories
* table of contents
{: toc}

## Idea
 {#Idea}

The concept of *strict 2-categories* is the simplest generalization of that of [[categories]] to the *[[n-categories|$n$-categories]]* of [[higher category theory]]. It is a one-step [[vertical categorification|categorification]] of the concept of a *[[category]]* with strict choice of structure morphisms.

More concretely, a strict 2-category is a [[directed n-graph|directed 2-graph]] equipped with [[horizontal composition|horizontal-]] and [[vertical composition]] of adjacent 1-cells ([[1-morphisms]]) and 2-cells ([[2-morphisms]]), respectively, which is strictly [[unitality|unital]] and [[associativity|associative]] in both directions, and such that both types of composition are compatible (the "[[interchange law]]").

A quick way of making this precise is to say that strict 2-categories are [[Cat]]-[[enriched categories]], see [below](#DefinitionStrictTwoCategories).

The term _2-category_ implicitly refers to a [[geometric shapes for higher structures|globular]] structure.  By contrast, [[double category|double categories]] are based on [[cubes]] instead.  The two notions are closely related, however: every strict 2-category gives rise to several strict double categories, and every double category has several [[underlying]] 2-categories.

Notice that _[[double category]]_ is another term for _[[n-fold category|2-fold category]]_.  Strict 2-categories may be identified with those strict 2-fold/double categories whose category of vertical morphisms is [[discrete category|discrete]], or those whose category of horizontal morphisms is discrete.

(And similarly, strict globular [[n-category|n-categories]] may be identified with those [[n-fold category|n-fold categories]] for which all cube faces "in one direction" are discrete. A similar statement for weak $n$-categories is to be expected, but little seems to be known about this.)


## Definition

### Strict 2-categories
 {#DefinitionStrictTwoCategories}

A _strict 2-category_, often called simply a _2-category_, is a [[enriched category|category enriched over]] [[Cat]], where [[Cat]] is regarded as the [[1-category]] of [[strict categories]] with [[functors]] between them and equipped with the [[cartesian monoidal category|cartesian monoidal]]-[[structure]] given by forming [[product categories]].

### Strict 2-groupoids

Similarly, a [[strict 2-groupoid]] is a [[enriched groupoid|groupoid enriched]] over the [[1-category]] [[Grpd]]. This is also called a *[[geometric shapes for higher structures|globular]] strict 2-groupoid*, to emphasise the underlying geometry. 

The category of strict 2-groupoids is [[equivalence of categories|equivalent]] to the category  of [[crossed modules]] over groupoids. It is also equivalent to the category of (strict) [[double groupoids]] "with connections". 

They are also special cases of strict globular omega-groupoids, and the category of these is equivalent to the category of [[crossed complex]]es. 


### Details

Working out the meaning of *[[Cat]]-[[enriched category]]* ([above](#DefinitionStrictTwoCategories)), we find that a strict 2-category $K$ is given by

* a [[class]] $ob K$ of [[objects]] $a,b,c,\ldots$, together with

* a [[hom-category]] $K(a,b)$ for each $a,b$, and

* [[functors]]

  * ([[identity morphisms]]) $1_a : \mathbf{1} \to K(a,a)$ 

  * ([[composition]]) $comp : K(b,c) \times K(a,b) \to K(a,c)$ 

  for each $a,b,c$, satisfying [[associativity]] and [[unitality]] [[axioms]] (as given at *[[enriched category]]*).

As for ordinary ($Set$-enriched) [[categories]], an object $f \in K(a,b)$ is called a _[[1-morphism]]_ or _1-cell_ from $a$ to $b$ and written $f:a\to b$ as usual.  But given $f,g:a\to b$, it is now possible to have non-trivial arrows $\alpha:f\to g \in K(a,b)$, called *[[2-morphisms]]* or _2-cells_ from $f$ to $g$ and written as $\alpha : f \Rightarrow g$.  Because the hom-objects $K(a,b)$ are by definition categories, 2-cells carry an associative and unital operation called _vertical composition_.  The identities for this operation, of course, are the identity 2-cells $1_f$ given by the category structure on $K(a,b)$.

The functor $comp$ gives us an operation of _horizontal_ composition on 2-cells.  Functoriality of $comp$ then says that given $\alpha : f \Rightarrow g : a\to b$ and $\beta : f' \Rightarrow g' : b\to c$, the composite $\comp(\beta,\alpha)$ is a 2-cell $\beta \alpha : f'f \Rightarrow g'g : a \to c$.  Note that the boundaries of the composite 2-cell are the composites of the boundaries of the components.

We also have the _[[interchange law]]_ (also called _Godement law_ or _middle 4 interchange law_): because $comp$ is a functor it commutes with composition in the hom-categories, so we have (writing [[vertical composition]] with $\circ$ and [[horizontal composition]] as juxtaposition):
$$
 (\beta' \circ \beta)(\alpha' \circ \alpha) = (\beta' \alpha') \circ (\beta \alpha)
$$


The [[axioms]] for [[associativity]] and [[unitality]] of $comp$ ensure that [[horizontal composition]] behaves just like [[composition]] of [[morphisms]] in a [[1-category]].  In particular, the action of $comp$ on objects $f,g$ of [[hom-categories]] (i.e. 1-cells of $K$) is the usual composite of morphisms.


### More details 
{#detailedDefn}

(See also the section below on [[sesquicategories]], which provide a conceptual package for the [[stuff, structure, property|stuff and structure]] described below.) 

In even more detail, a strict $2$-category $K$ consists of *stuff*: 

*  a collection $Ob K$ or $Ob_K$ of _[[objects]]_ or _$0$-cells_,

*  for each object $a$ and object $b$, a collection $K(a,b)$ or $Hom_K(a,b)$ of _[[1-morphisms]]_ or _$1$-cells_ $a \to b$, and

*  for each object $a$, object $b$, morphism $f\colon a \to b$, and morphism $g\colon a \to b$, a collection $K(f,g)$ or $2 Hom_K(f,g)$ of _[[2-morphisms]]_ or _$2$-cells_ $f \Rightarrow g$ or $f \Rightarrow g\colon a \to b$,

that is equipped with the following *[[structure]]*: 

*  for each object $a$, an _[[identity morphism|identity]]_ $1_a\colon a \to a$ or $\id_a\colon a \to a$,

*  for each $a,b,c$, $f\colon a \to b$, and $g\colon b \to c$, a _composite_ $f ; g\colon a \to c$ or $g \circ f\colon a \to c$,

*  for each $f\colon a \to b$, an _identity_ $1_f\colon f \Rightarrow f$ or $\Id_f\colon f \Rightarrow f$,

*  for each $f,g,h\colon a \to b$, $\eta\colon f \Rightarrow g$, and $\theta\colon g \Rightarrow h$, a _[[vertical composition|vertical composite]]_ $\theta \bullet \eta\colon f \Rightarrow h$,

*  for each $a,b,c$, $f\colon a \to b$, $g,h\colon b \to c$, and $\eta\colon g \Rightarrow h$, a _left [[whiskering]]_ $\eta \triangleleft f\colon g \circ f \Rightarrow h \circ f$, and
*  for each $a,b,c$, $f,g\colon a \to b$, $h\colon b \to c$, and $\eta\colon f \Rightarrow g$, a _right [[whiskering]]_ $h \triangleright \eta \colon h \circ f \Rightarrow h \circ g$,

satisfying the following properties: 

1.  for each $f\colon a \to b$, the composites $f \circ \id_a$ and $\id_b \circ f$ each equal $f$,

1.  for each $a \overset{f}\to b \overset{g}\to c \overset{h}\to d$, the composites $h \circ (g \circ f)$ and $(h \circ g) \circ f$ are equal,
1.  for each $\eta\colon f \Rightarrow g\colon a \to b$, the vertical composites $\eta \bullet \Id_f$ and $\Id_g \bullet \eta$ both equal $\eta$,
1.  for each $f \overset{\eta}\Rightarrow g \overset{\theta}\Rightarrow h \overset{\iota}\Rightarrow i\colon a \to b$, the vertical composites $\iota \bullet (\theta \bullet \eta)$ and $(\iota \bullet \theta) \bullet \eta$ are equal,
1.  for each $a \overset{f}\to b \overset{g}\to c$, the [[whiskerings]] $\Id_g \triangleleft f$ and $g \triangleright \Id_f$ both equal $\Id_{g \circ f }$,
1.  for each $\eta\colon f \Rightarrow g\colon a \to b$, the [[whiskerings]] $\eta \triangleleft \id_a$ and $\id_b \triangleright \eta$ equal $\eta$,
1.  for each $f\colon a \to b$ and $g \overset{\eta}\Rightarrow h \overset{\theta}\Rightarrow i\colon b \to c$, the vertical composite $(\theta \triangleleft f) \bullet (\eta \triangleleft f)$ equals the [[whiskering]] $(\theta \bullet \eta) \triangleleft f$,
1.  for each $f \overset{\eta}\Rightarrow g \overset{\theta}\Rightarrow h\colon a \to b$ and $i\colon b \to c$, the vertical composite $(i \triangleright \theta) \bullet (i \triangleright \eta)$ equals the [[whiskering]] $i \triangleright (\theta \bullet \eta)$,
1.  for each $a \overset{f}\to b \overset{g}\to c$ and $\eta\colon h \Rightarrow i\colon c \to d$, the left [[whiskerings]] $\eta \triangleleft (g \circ f)$ and $(\eta \triangleleft g) \triangleleft f$ are equal,
1.  for each $\eta\colon f \Rightarrow g\colon a \to b$ and $b \overset{h}\to c \overset{i}\to d$, the right [[whiskerings]] $i \triangleright (h \triangleright \eta)$ and $(i \circ h) \triangleright \eta$ are equal,
1.  for each $f\colon a \to b$, $\eta\colon g \Rightarrow h\colon b \to c$, and $i\colon c \to d$, the [[whiskerings]] $i \triangleright (\eta \triangleleft f)$ and $(i \triangleright \eta) \triangleleft f$ are equal, and
1.  for each $\eta\colon f \Rightarrow g\colon a \to b$ and $\theta\colon h \Rightarrow i\colon b \to c$, the vertical composites $(i \triangleright \eta) \bullet (\theta \triangleleft f)$ and $(\theta \triangleleft g) \bullet (h \triangleright \eta)$ are equal.

The construction in the last axiom is the _[[horizontal composition|horizontal composite]]_ $\theta \circ \eta\colon h \circ f \to i \circ g$.  It is possible (and probably more common) to take the [[horizontal composition|horizontal composite]] as basic and the [[whiskerings]] as derived operations.  This results in fewer, but more complicated, axioms.

## 2-categories as sesquicategories 
 {#AsSesquicategories}

The fine-grained description in the [previous subsection](#detailedDefn) can be concisely repackaged by saying that a 2-category is a [[sesquicategory]] that satisfies the [[interchange axiom]], i.e., the last axiom (12) which gives the [[horizontal composition]]-construction. This description is essentially patterned after the "five rules of functorial calculus" introduced by [Godement (1958)](#Godement58) for the special case [[Cat]]. 

So to say it again, but a little differently: a sesquicategory consists of a category $K$ (giving the $0$-cells and $1$-cells) together with a functor 

$$
  K(-, -)
  \;\colon\; 
  K^{op} \times K 
    \longrightarrow 
  Cat
$$ 

such that composing $K(-, -)$ with the functor $ob: Cat \to Set$ (the one sending a category to its set of objects) gives $\hom_K: K^{op} \times K \to Set$, the hom-functor for the category $K$. So: for $0$-cells $a, b$, the objects of the category $K(a, b)$ are $1$-cells $f \in \hom_K(a, b)$. The morphisms of $K(a, b)$ are $2$-cells (with $0$-source $a$ and $0$-target $b$). Composition within the category $K(a, b)$ corresponds to [[vertical composition]]. 

For each object $a$ of $K$ and each morphism $h: b \to c$ of $K$, there is a functor $K(a, h): K(a, b) \to K(a, c)$. This is *right [[whiskering]]*; it sends a [[2-morphism|2-cell]] $\eta$ (a morphism of $K(a, b)$) to a morphism $h \triangleright \eta$ of $K(b, c)$. Similarly, for each object $c$ and morphism $f: a \to b$, there is a functor $K(f, c): K(b, c) \to K(a, c)$. This is *left [[whiskering]]*; it sends a [[2-morphism|2-cell]] $\eta$ (a morphism of $K(b, c)$) to a morphism $\eta \triangleleft f$ of $K(a, c)$. 

The long list of compatibility properties enumerated in the previous subsection, all except the last, are concisely summarized in the definition of sesquicategory as recalled above. For example, property (8) just says that left [[whiskering]] preserves [[vertical composition]], as it must since it is a [[functor]] (a morphism in $Cat$). 

In summary, a sesquicategory consists of "stuff" and structure as described in the [previous subsection](/nlab/show/strict+2-category#detailedDefn), satisfying properties 1-11. A 2-category is then a sesquicategory that further satisfies the [[interchange axiom]] (12). Some further illumination of this point of view can be obtained by contemplating [[string diagrams]] for 2-categories, where the [[interchange axiom]] corresponds to [[isotopies]] of (planar, progressive) string diagrams during which the relative heights of nodes labeled by 2-cells are interchanged. 

## Remarks

* Strict 2-categories are the same as a [[strict omega-categories]] which are trivial in degree $n \geq 3$.

* This is to be contrasted with a _weak 2-category_ called a [[bicategory]]. In a strict 2-category composition of 1-morphisms is strictly associative and composition with [[identity morphism]]s strictly satisfies the required identity law. In a weak 2-category these laws may hold only up to coherent 2-morphisms.

## In dependent type theory

In [[dependent type theory]], there are multiple notions of a "strict 2-category", because there are multiple notions of a [[category]]:

* A strict 2-category could be a [[precategory]] enriched over the [[cartesian monoidal category]] [[Cat]] of [[strict categories]]
* A strict 2-category could be a [[strict category]] enriched over the cartesian monoidal category Cat of strict categories
* A strict 2-category could be a [[univalent category]] enriched over the cartesian monoidal category Cat of strict categories

The first definition is a naive translation of "strict 2-category" from set theory to dependent type theory, but in the absence of [[axiom K]] or a similar axiom, these strict 2-categories behave differently from the strict 2-categories as defined in [[set theory]]. The second definition adds a [[0-truncation]] condition to the type of objects to ensure that the strict 2-categories actually behave like the strict 2-categories in set theory. The third definition satisfies the [[principle of equivalence]]: equality of objects is the same as isomorphism of strict categories, and ensures that strict 2-categories are [[h-groupoids]]. 

## Related concepts

* [[strict 2-groupoid]]

* [[strict 2-functor]]

* [[strict 2-natural transformation]]

* [[strict adjoint 2-functor]]

* [[strict 2-group]]

## History 

As intimated above, the essential rules which abstractly govern the behavior of functors and natural transformations and their various compositions were made explicit by [Godement (1958)](#Godement58), in his "five rules of functorial calculus". He did not however go as far as use these rules to define the abstract notion of 2-category; this step was taken later by [Bénabou (1965)](#Bénabou65). In any event, the primitive compositional operations in [Godement (1958)](#Godement58) were what we call *[[vertical composition]]* and *[[whiskering]]*, with [[horizontal composition]] of [[natural transformations]] being a derived operation (made unambiguous in the presence of the interchange axiom). Indeed, [[horizontal composition]] is often called the *Godement product*. 

A few years after introducing 2-categories, B&#233;nabou introduced the more general notion of *[[bicategories]]*. 

Literature references for the abstract notion of [[sesquicategory]], a structure in which vertical compositions and whiskerings are primitive, do not seem to be abundant, but they are mentioned for example in [Street (1996)](#Street96) together with the observation that 2-categories are special types of sesquicategories (page 535). 


## References 
 {#References}

The "five rules of functorial calculus" ([above](#AsSesquicategories)) were formulated (as: *cinq règles de calcul fonctoriel*) in:

* {#Godement58} [[Roger Godement]], Appendice (pp. 269) of:  *Topologie algébrique et theorie des faisceaux*, Actualités Sci. Ind. **1252**, Hermann, Paris (1958) &lbrack;[webpage](https://www.editions-hermann.fr/livre/topologie-algebrique-et-theorie-des-faisceaux-roger-godement), [[Godement-TopologieAlgebrique.pdf:file]]&rbrack;
 
The definition of "[[double categories]]" (of which, at least in hindsight, strict 2-categories are an immediate special case) is due to:

* {#Ehresmann63} [[Charles Ehresmann]], *Catégories double et catégories structurées*, C.R. Acad. Paris 256 (1963) 1198-1201 &lbrack;[[Ehresmann-CategoriesDoubles.pdf:file]], [gallica](https://gallica.bnf.fr/ark:/12148/bpt6k3208j/f1246)&rbrack;

also discussed (according to [reviewers](https://www.jstor.org/stable/2314770) who have seen the text) in:

* [[Charles Ehresmann]], *Catégories et structures*, Dunod, Paris, (1965)

However, Ehresmann did not isolate the notion of strict 2-categories as such.

But apparently inspired by [Ehresmann (1963)](#Ehresmann63) the actual definition of strict 2-categories is due to:

* {#Bénabou65} [[Jean Bénabou]], Example (5) of: *Catégories relatives*, C. R. Acad. Sci. Paris **260** (1965) 3824-3827 &lbrack;[gallica](https://gallica.bnf.fr/ark:/12148/bpt6k4019v/f37.item)&rbrack;

  > (conceived as [[Cat]]-[[enriched categories]] and under the name "2-categories")

* {#Maranda65} [[Jean-Marie Maranda]], Def. 1 in: *Formal categories*, Canadian Journal of Mathematics **17** (1965) 758-801 &lbrack;[doi:10.4153/CJM-1965-076-0](https://doi.org/10.4153/CJM-1965-076-0), [pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/A7C463460EB8CAC64C2CA340F870CF80/S0008414X00039729a.pdf/formal-categories.pdf)&rbrack;

  > (conceived as [[Cat]]-[[enriched categories]] and under the name "categories of the second type")

* {#EK65} [[Samuel Eilenberg]], [[G. Max Kelly]], p. 425 of: *Closed Categories*,  in:  [[Samuel Eilenberg|S. Eilenberg]], [[D. K. Harrison]], [[S. MacLane]], [[H. Röhrl]] (eds.): *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;

  > (expressed entirely in components and under the name *hypercategories*)

and the notion is invoked for various purposes (such as in speaking of [[Cat]] as a 2-category) in:

* {#Bénabou68} [[Jean Bénabou]], *Structures algébriques dans les catégories*, Cahiers de topologie et géométrie différentielle, **10** 1 (1968) 1-126 &lbrack;[doi:CTGDC_1968__10_1_1_0](http://www.numdam.org/item/?id=CTGDC_1968__10_1_1_0)&rbrack;

Exposition and review:

* {#Street96}  [[Ross Street]], p. 535 in: *Categorical Structures*, in Handbook of Algebra Vol. 1 (ed. M. Hazewinkel), Elsevier Science, Amsterdam (1996) &lbrack;<a href="https://doi.org/10.1016/S1570-7954(96)80019-2">doi:10.1016/S1570-7954(96)80019-2</a>, [pdf](http://maths.mq.edu.au/~street/45.pdf), [[Street-CategoricalStructures.pdf:file]] [ISBN:978-0-444-82212-3](https://shop.elsevier.com/books/handbook-of-algebra/hazewinkel/978-0-444-82212-3)&rbrack;

* [[Saunders MacLane]], §XII.3 of: *[[Categories for the Working Mathematician]]*, Graduate Texts in Mathematics **5** Springer (second ed. 1997) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* {#Lack10} [[Steve Lack]], _A 2-categories companion_,  In: Baez J., May J. (eds.) *[[Towards Higher Categories]]*. The IMA Volumes in Mathematics and its Applications, vol 152. Springer 2010 ([arXiv:math.CT/0702535](http://arxiv.org/abs/math.CT/0702535), [doi:10.1007/978-1-4419-1524-5_4](https://doi.org/10.1007/978-1-4419-1524-5_4))

* {#Richter19} [[Birgit Richter]], Section 9.5 of: _From categories to homotopy theory_, Cambridge Studies in Advanced Mathematics 188, Cambridge University Press 2020 ([doi:10.1017/9781108855891](https://doi.org/10.1017/9781108855891), [book webpage](https://www.math.uni-hamburg.de/home/richter/catbook.html), [pdf](https://www.math.uni-hamburg.de/home/richter/bookdraft.pdf))

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], Section 2.3 of: _2-Dimensional Categories_, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))

See also 

* Wikipedia, *[Strict 2-category](https://en.wikipedia.org/wiki/Strict_2-category)*

The special case of [[strict (2,1)-categories]]:

* [[Peter H. H. Fantham]], [[Eric J. Moore]], *Groupoid Enriched Categories and Homotopy Theory*, Canadian Journal of Mathematics **35** 3 (1983) 385-416 ([doi:10.4153/CJM-1983-022-8](https://doi.org/10.4153/CJM-1983-022-8))


[[!redirects strict 2-category]]
[[!redirects strict 2-categories]]
[[!redirects globular strict 2-category]]
[[!redirects globular strict 2-categories]]
[[!redirects strict globular 2-category]]
[[!redirects strict globular 2-categories]]

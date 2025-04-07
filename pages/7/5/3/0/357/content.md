
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


# Contents
* tic
{: toc}

## Idea

A **virtual double category** or **$fc$-multicategory** is a common generalization of a [[monoidal category]], a [[bicategory]], a [[double category]], and a [[multicategory]].  It contains:

* objects
* tight arrows, which form a category
* loose arrows, which do not have identities or composites, and
* 2-cells which have
  * tight source and target arrows,
  * a loose multi-source, i.e. a string of loose arrows, and
  * a loose target arrow.

2-cells are usually drawn like this:

[[virtual-double-category-cell.png:pic]]

Note that this includes the case when $n=0$, i.e. a cell of "nullary" source.  In this case, we must have $X_0 = X_n$. 

Note that the "empty" case of a string of loose arrows this has a single object $X$ in which case the 2-cell looks like:

\begin{tikzcd}% https://q.uiver.app/?q=WzAsNCxbMSwwLCJYIl0sWzAsMiwiWV8wIl0sWzIsMiwiWV8xIl0sWzEsMSwiXFxEb3duYXJyb3cgXFxhbHBoYSJdLFswLDEsImYiLDJdLFswLDIsImciXSxbMSwyLCJxIiwyLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiYmFycmVkIn19fV1d
	& X \\
	& {\Downarrow \alpha} \\
	{Y_0} && {Y_1}
	\arrow["f"', from=1-2, to=3-1]
	\arrow["g", from=1-2, to=3-3]
	\arrow["q"', "\shortmid"{marking}, from=3-1, to=3-3]
\end{tikzcd}

Finally, the 2-cells can be composed in a more or less evident way, akin to composition in a multicategory:

[[virtual-double-category-composite.png:pic]]

Virtual double categories are related to double categories precisely as ordinary multicategories are related to monoidal categories (see [[generalized multicategory]] and [[tensor product]]).

The dual notion in which 2-cells have a single loose source and a multi-ary loose target may be called a covirtual double category, although the term oplax double category also exists in the literature e.g. [Dawson, Paré, Pronk](#DawsonParePronk10).

## Definition

A virtual double category can be defined in two equivalent ways:

* It is a $T$-[[generalized multicategory|multicategory]], in the sense of Leinster, relative to the monad $T$ on [[quiver|directed graphs]] whose algebras are categories.  For this reason, Leinster originally called them **fc-multicategories**, where "fc" is a name for this monad $T$ which stands for "free-category."

* It is a generalized multicategory, in the sense of Hermida, Cruttwell-Shulman, and others, relative to the monad $T$ on graphs-internal-to-Cat whose algebras are double categories.  This is the origin of the name "virtual double category," in line with the general terminology "virtual $T$-algebra" of Cruttwell-Shulman for such generalized multicategories.

We can also give an explicit definition, which was more or less already given in the "Idea" section: all that is missing are identities and associativity for 2-cell composition.

## Examples

* A [[multicategory]] is a virtual double category with a single object and a single tight morphism (the identity morphism). 
* Any double category is an example, and thus also any bicategory
viewing the arrows as loose.
* For any [[monoidal category]] $V$, there is a virtual double category
of $V$-matrices whose objects are sets, tight arrows are functions
and a loose arrow $p : X \to Y$ is a family of objects $p_{y,x}
\in V$ for each $x\in X, y \in Y$, and a 2-cell from $X_0
\overset{p_1}{\to} X_1 \to\dots \to X_n$ to $Y_0 \overset{q}{\to} Y_1$
along $f : X_0 \to Y_0, g : X_n \to Y_n$ is a family of arrows
$\alpha_{x_0,...} : p_1(x_1,x_0)\otimes p_2(x_2,x_1)\otimes\dots \to
q(g(x_n),f(x_0))$ in $V$ (using the unit of the monoidal category if the source string is empty).
If $V$ has certain colimits that are preserved by $\otimes$ then
composites exist and this virtual double category is pseudo.
* Given a monad on a virtual double category, the [[generalized multicategory| loose kleisli
double category]] produces a virtual double
category that is only pseudo under strong conditions on the monad. In
particular, "free monoid" monad on the double category of sets and
spans does not produce a pseudo double category.


## Higher categories of virtual double categories

There are notions of **functor**, **transformation**, and **profunctor** between virtual double categories.  The neatest way to define all of these notions at once is to use the general framework of [[generalized multicategories]]: from the monad $fc$ on the [[virtual equipment]] $Span = Span(Set)$ we can construct a new virtual equipment $vDblProf = KMod(Span,fc)$ whose objects are virtual double categories, whose arrows are functors between them, whose proarrows are profunctors between them, and whose cells are transformations.  But we can also give explicit definitions of all of these notions.

### Functors and transformations

A **functor** of virtual double categories is fairly obvious; it takes each kind of morphism/cell to the same kind, preserving sources, targets, composition, and identities.

The relevant **transformations** are a "virtual" version of [[tight transformations]] between ordinary double categories.  Specifically, a transformation $\alpha\colon F\to G$ has a tight arrow component $\alpha_X\colon F X\to G X$ for each object $X$ of the domain, and a cell component
$$\array{F X & \overset{F p}{\to} & F Y\\
  ^{\alpha_X}\downarrow & \Downarrow ^{\alpha_p}& \downarrow^{\alpha_Y}\\
  G X& \underset{G p}{\to} & G Y}$$
for each loose arrow $p\colon X\to Y$ in the domain.  These must be natural with respect to tight composition of arrows and of 2-cells, where we must of course allow composites with arbitrary arities in the latter case.

Virtual double categories, functors, and transformations form a [[strict 2-category]], and thus we can apply all notions of 2-category theory to it.  In particular, we have a notion of a [[monad]] *on* a virtual double category, which is the starting point for one theory of [[generalized multicategories]].


### Profunctors

The **profunctors** between virtual double categories are a similar "virtualization" of the notion of [[double profunctor]] between double categories.  Explicitly, a profunctor $H\colon C &#8696; D$ consists of:

* An ordinary [[profunctor]] $H_0\colon C_0 &#8696; D_0$ between the categories of objects and tight arrows.
* For each string of loose arrows $X_0 \overset{p_1}{\to} X_1 \to\dots \to X_n$ in $D$, each loose arrow $Y_0 \overset{q}{\to} Y_1$ in $C$, and each pair of elements $f \in H_0 (X_0,Y_0)$ and $g\in H_0(X_n,Y_1)$, a set of "hetero-cells" of shape

  [[virtual-double-category-cell.png:pic]]


* The hetero-cells are acted on by the 2-cells of $D$ on the top, and by the 2-cells of $C$ on the bottom, in an evident way, respecting the given action of tight arrows of $D$ and $C$ on the elements of $H_0$.

Every [[double profunctor]] induces such a profunctor in an evident way, but even if $C$ and $D$ are (non-virtual) double categories, not every "virtual double profunctor" from $C$ to $D$ need be a double functor; only those for which the "hetero-cells" also factor uniquely through the opcartesian cells in $D$ which make it "representable."

As mentioned above in the context of the abstract definition, virtual double categories, functors, transformations, and profunctors form another virtual double category, which is in fact a [[virtual equipment]].


### Monads on virtual double categories {#Monads}

+-- {: .un_defn}
###### Definition

A _monad on a virtual double category_  is a [[monad]] in the [[2-category]] [[vDbl]]. 

=--

So a monad on a $X \in vDbl$ consists of a functor

$$
  T : \mathbb{X} \to \mathbb{X}
$$

and transformations $\eta : Id  \to T$ and $\mu : T T \to T$ satisfying [[associativity]] and [[unitality]].


#### Monoids and modules


+-- {: .un_defn}
###### Definition

For $T$ a monad on $\mathbb{X} \in $ [[vDbl]], a **$T$-monoid** is 

* an object $X_0 \in \mathbb{X}$;

* a loose morphism $X_0 \stackrel{X}{&#8696;} T X_0$

* an [[action]] [[2-morphism]]

  $$
    \array{
       X_0 &\stackrel{X}{&#8696;} & T X_0 
        & \stackrel{T X}{&#8696;} T^2 &  X_0
       \\
       {}^{\mathllap{=}}\downarrow && \Downarrow^{\bar x}
       &&  \downarrow^{\mathrlap{\mu}}
       \\
       X_0 && \underset{X}{&#8696;}  && T X_0
    }
  $$

  and a [[unit]] 2-morphism

  $$
    \array{
       && X_0
       \\
       & {}^{\mathllap{=}}\nearrow &\Downarrow^{\bar x}& \searrow^{\mathrlap{\eta}}
       \\
       X_0 &&\underset{X}{&#8696;}&& T X_0
    }
  $$

satisfying the evident compatibility conditions.

=--

This is ([CruttwellShulman, def. 4.2](#CruttwellShulman)).


+-- {: .un_defn}
###### Definition

A $T$-monoid $X_0 \stackrel{X}{&#8696;} T X_0$ is called **normalized** if its unit 2-morphism

$$
  \array{
    X_0 &\stackrel{U_{X_0}}{\to}& X_0
    \\
    {}^{\mathllap{=}}\downarrow && \downarrow^{\mathrlap{\eta}}
    \\
    X_0 &\underset{X}{&#8696;}& T X_0
  }
$$

is a [cartesian 2-morphism](#...).

=--


#### Generalized multicategories


+-- {: .un_defn}
###### Definition

A **[[generalized multicategory]]** is a normalized $T$-monoid for some monad $T$ on a [[virtual equipment]] $\mathbb{X} \in $ [[vDbl]].

=--

This is ([CruttwellShulman, page 7](#CruttwellShulman)).

## Properties

* The 2-category of virtual double categories is the 2-category of algebras for a [[lax-idempotent 2-comonad]] on the 2-category of (strict) [[double categories]] and strict double functors, specifically that induced by the inclusion of the 2-category of double categories and strict double functors into the 2-category of double categories and lax double functors: see §2 of [DPP06](#DPP06). (This is analogous to the relationship between [[multicategories]] and [[monoidal categories]].) The same is true of **normal** virtual double categories, i.e. those with identity [[loose morphisms]].


## Enriching categories

Virtual double categories can be viewed as "the natural place in which to enrich categories."  Specifically, for any set $A$, there is a virtual double category $A_{ch}$ which has $A$ as its objects, only identity tight arrows, exactly one loose arrow from every object to every other object, and exactly one 2-cell in every possible niche.  For any other virtual double category $W$, a functor $A_{ch}\to W$ of virtual double categories is the same as a $W$-enriched category with object set $A$.

## Related pages

* [[double category]]
* [[virtual equipment]]
* [[augmented virtual double category]]

## References

Virtual double categories were first considered by [[Albert Burroni]] under the name **multicatégorie** on page 61 of:

* [[Albert Burroni]], _$T$-catégories (catégories dans un triple)_, Cahiers de topologie et géométrie différentielle catégoriques **12**.3 (1971) 215-321 &lbrack;[dml:91097](https://eudml.org/doc/91097), [pdf](http://www.numdam.org/article/CTGDC_1971__12_3_215_0.pdf)&rbrack;

Later, they were considered in:

* [[Tom Leinster]], _Higher Operads, Higher Categories_, [link](http://www.maths.gla.ac.uk/~tl/book.html), [arXiv:0305049](http://arxiv.org/abs/math/0305049)

* [[Tom Leinster]], **fc**-multicategories, [arxiv](https://arxiv.org/abs/math/9903004) (1999)

They are called **lax double categories** in:

* {#DPP06} [[Robert Dawson]], [[Robert Paré]] and [[Dorette Pronk]], _Paths in double categories_, Theory and Applications of Categories, Vol. 16, No. 18, 2006, pp. 460-521. &lbrack;[TAC](http://www.tac.mta.ca/tac/volumes/16/18/16-18abs.html)&rbrack;

and the dual concept is called **oplax double category** in:

* {#DawsonParePronk10} R. Dawson, [[Robert Paré]], [[Dorette Pronk]], _The span construction_, Theory Appl. Categ. __24__ (2010), No. 13, 302&#8211;377, [TAC](http://www.tac.mta.ca/tac/volumes/24/13/24-13abs.html) [MR2720187](http://www.ams.org/mathscinet-getitem?mr=2720187)

The name **virtual double category** is introduced in:

* {#CruttwellShulman} [[Geoff Cruttwell]], [[Mike Shulman]], _A unified framework for generalized multicategories_ &lbrack;[arXiv:0907.2460](http://arxiv.org/abs/0907.2460)&rbrack;

On a [[string diagram]]-calculus for ([[virtual double category|virtual]]) [[double categories]] with ([[virtual equipment|virtual]]) [[2-category equipped with proarrows|pro-arrow equipments]]:

* {#Myers16} [[David Jaz Myers]], _String Diagrams For Double Categories and (Virtual) Equipments_ &lbrack;[arXiv:1612.02762](https://arxiv.org/abs/1612.02762)&rbrack;

* [[David Jaz Myers]], *String Diagrams for (Virtual) Proarrow Equipments* (2017) &lbrack;slides: [pdf](http://www.mat.uc.pt/~ct2017/slides/myers_d.pdf), [[Myers-StringDiagrams2017.pdf:file]]&rbrack;



[[!redirects virtual double categories]]
[[!redirects fc-multicategory]]
[[!redirects fc-multicategories]]
[[!redirects covirtual double category]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}

## Idea


The notion of a _2-category_ generalizes that of [[category]]: a 2-category is a [[higher category theory|higher category]], where on top of the objects and morphisms, there are also 2-morphisms.

A 2-category consists of 

* [[objects]];

* 1-[[morphisms]] between objects;

* [[2-morphisms]] between morphisms.

The morphisms can be [[composition|composed]] along the objects, while the 2-morphisms can be composed in two different directions: along objects -- called [[horizontal composition]] -- and along morphisms -- called [[vertical composition]].  The composition of morphisms is allowed to be associative only up to [[coherent]] [[associator]] 2-morphisms.

2-categories are also a [[horizontal categorification]] of [[monoidal categories]]: they are like monoidal categories with many objects. 

2-categories provide the context for discussing

* [[adjunction]]s;

* [[monad]]s.

The concept of 2-category generalizes further in [[higher category theory]] to [[n-categories]], which have [[k-morphism]]s for all $k\le n$.

2-categories form a [[3-category]], [[2Cat]].

## Definitions

### Strict 2-categories

The easiest definition of 2-category is that it is a category [[enriched category|enriched]] over the [[cartesian monoidal category]] [[Cat]].  Thus it has a collection of objects,. and for each pair of objects a category $hom(x,y)$.  The objects of these hom-categories are the morphisms, and the morphisms of these hom-categories are the 2-morphisms.  This produces the classical notion of [[strict 2-category]].

### General 2-categories
 {#Weak}

For some purposes, strict 2-categories are too strict: one would like to allow composition of morphisms to be associative and unital only up to coherent invertible 2-morphisms.  A direct generalization of the above "enriched" definition produces the classical notion of [[bicategory]].

One can also obtain notions of 2-category by specialization from the case of higher categories.  Specifically, if we fix a meaning of $\infty$-[[infinity-category|category]], however weak or strict we wish, then we can define a __$2$-category__ to be an $\infty$-category such that every 3-morphism is an [[equivalence]], and all parallel pairs of $j$-morphisms are equivalent for $j \geq 3$.  It follows that, up to equivalence, there is no point in mentioning anything beyond $2$-morphisms, except whether two given parallel $2$-morphisms are equivalent.  In some models of $\infty$-categories, it is possible to make this precise by demanding that all parallel pairs of $j$-morphisms are actually *equal* for $j\geq 3$, producing a simpler notion of 2-category in which we can speak about [[equality]] of 2-morphisms instead of equivalence.  (This is the case for both strict $2$-categories and bicategories.)

All of the above definitions produce "equivalent" theories of 2-category, although in some cases (such as the fact that every bicategory is equivalent to a strict 2-category) this requires some work to prove.  On the nLab, we often use the word "2-category" in the general sense of referring to whatever model one may prefer, but usually one in which composition is weak; a [[bicategory]] is an adequate definition.  One should beware, however, that in the literature it is common for "2-category" to refer only to *strict* 2-categories.

A 2-category in which all 1-morphisms and 2-morphisms are invertible is a [[2-groupoid]].

## Examples

* The archetypical 2-category is [[Cat]], the 2-category whose

  * objects are [[categories]];

  * morphisms are [[functor]]s;

  * 2-morphisms are [[natural transformation]];

    horizontal composition of 2-morphisms is the [[Godement product]].

  This happens to be a [[strict 2-category]].

* More generally, for $V$ any enriching category (such as a Benabou [[cosmos]]), there is a 2-category $V Cat$ whose

  * objects are $V$-[[enriched categories]];
  * morphisms are $V$-enriched functors; and
  * 2-morphisms are $V$-natural transformations.

* On the other hand, for any such $V$ we also have a [[bicategory]] $V$-[[Prof]] whose

  * objects are $V$-[[enriched categories]];
  * morphisms are $V$-[[profunctor]]s; and
  * 2-morphisms are natural transformations between these.

* If $C$ is a category with [[pullbacks]], then there is a bicategory [[Span]]$(C)$ whose

  * objects are the objects of $C$;
  * morphisms are [[spans]] in $C$; and
  * 2-morphisms are morphisms of spans.

* Every [[monoidal category]] $C$ may be thought of as a [[bicategory]] $\mathbf{B}C$ (its [[delooping]]). This has

  * a single object $\bullet$;

  * morphisms are the objects of $C$: $(\mathbf{B}C)_1 = C_0$;

  * 2-morphisms are the morphisms of $C$ : $(\mathbf{B}C)_2 = C_1$;

  [[horizontal composition]] in $\mathbf{B}C$ is the [[tensor product]] in $C$ and [[vertical composition]] in $\mathbf{B}C$ is composition in $C$.

  Conversely, every 2-category with a single object comes from a monoidal category this way, so the concepts are effectively equivalent. (Precisely: the 2-category of  _pointed_ 2-categories with a single object is equivalent to that of monoidal categories).  For more on this relation see [[delooping hypothesis]], [[k-tuply monoidal n-category]], and [[periodic table]].

* Every [[2-groupoid]] is a 2-category. For instance

  * for $A$ any [[abelian group]], the double [[delooping]] $\mathbf{B}^2 A$ is the strict 2-category with a single object, a single 1-morphisms, set of 2-moprhisms being $A$ and both horizontal composition as well as [[vertical composition]] being the product in $A$.

  * for $G$ any [[2-group]], its single [[delooping]] is a 2-groupoid with a single object.

* Every [[topological space]] has a [[path 2-groupoid]].

* Every [[(∞,2)-category]] has a **homotopy 2-category**, obtained by dividing out all 3-morphisms and higher.

## Properties

### Double nerve

An ordinary  [[category]] has a [[nerve]] which is a [[simplicial set]]. For 2-categories one may consider their [[double nerve]] which is a [[bisimplicial set]].

There is also a 2-nerve. ([LackPaoli](#LackPaoli))

(...)


### Model category structure {#ModelCategoryStructure}

There is a [[model category]] structure on 2-categories -- sometimes known as the [[folk model structure]] -- that models the [[(2,1)-category]] underlying [[2Cat]] ([Lack](#LackFolkModel)).

For strict 2-categories this is the restriction of the corresponding [[folk model structure]] on [[strict omega-categories]]. 

* The weak equivalences are the [[2-functor]]s that are equivalences of 2-categories.

* The acyclic fibrations are the [[k-surjective functor]]s for all $k$.


#### Free resolutions {#FreeResolution}


**Theorem** A strict 2-category $C$ is cofibrant precisely if the underlying 1-category $C_1$ is a [[free category]].

This is theorem 4.8 in ([LackStrict](#LackStrict)). This is a special case of the more general statement that free strict $\omega$-categories are given by [[computad]]s.

**Example (free resolution of a 1-category).** Let $C$ be an ordinary category (a 1-category) regarded as a strict 2-category. Then the cofibrant resolution $\hat C \stackrel{\simeq}{\to} C$ is the strict 2-category given as follows:

* the objects of $\hat C$ are those of $C$;

* the morphisms of $\hat C$ are finite sequences of composable morphisms of $C$, and composition is concatenation of such sequences

  (hence $(\hat C)_1$ is the [[free category]] on the [[quiver]] underlying $C$);

* the 2-morphisms of $\hat C$ are _generated_ from 2-morphisms $c_{f,g}$ of the form

  $$
    \array{
       && y
       \\
       & {}^{\mathllap{f}}\nearrow &\Downarrow^{c_{f,g}}& \searrow^{\mathrlap{g}}
       \\
       x && \underset{g \circ_C f }{\to} && z
    }
  $$

  and their formal inverses

  $$
    \array{
       && y
       \\
       & {}^{\mathllap{f}}\nearrow &\Uparrow^{c_{f,g}^{-1}}& \searrow^{\mathrlap{g}}
       \\
       x && \underset{g \circ_C f }{\to} && z
    }
  $$


  for all composable $f,g \in Mor(C)$ with composite (in $C$!) $g \circ_C f$;

  subject to the _relation_ that for all composable triples $f,g,h \in Mor(C)$
  the following equation of 2-morphisms holds

  $$
    \array{
       y &\to& &\stackrel{g}{\to}& &\to& && z
       \\
       \uparrow &\seArrow^{c_{f,g}}& && & \nearrow & && \downarrow
       \\
       {}^{\mathllap{f}}\uparrow &&  & \nearrow & &&&& \downarrow^{\mathrlap{h}}
       \\
       \uparrow & \nearrow & && &\Downarrow^{c_{h,(g\circ_C f)}}& && \downarrow
       \\
       x &\to& &\underset{h \circ (g \circ_C f)}{\to}& &\to& &\to& w
    }
    \;\;\;
    = 
    \;\;\;
        \array{
       y &\to& &\stackrel{g}{\to}& &\to& && z
       \\
       \uparrow &\searrow& && & & &\swArrow_{c_{g,h}}& \downarrow
       \\
       {}^{\mathllap{f}}\uparrow &&  & \searrow & &&&& \downarrow^{\mathrlap{h}}
       \\
       \uparrow &\Downarrow_{c_{f,(g \circ_C h)}}& && &\searrow& && \downarrow
       \\
       x &\to& &\underset{( h \circ_C g) \circ f}{\to}& &\to& &\to& w
    }
  $$

**Observation** Let $D$ be any strict 2-catgeory. Then a [[pseudofunctor]] $C \to D$ is the same as a strict 2-functor $\hat C \to D$.

## 2-categorical concepts

**extra properties**

* [[regular 2-category]] 
* [[exact 2-category]]
* [[coherent 2-category]] 
* [[extensive 2-category]] 
* [[2-pretopos]]
* [[2-topos]]

**types of morphisms**

* [[subcategory]]
* [[faithful morphism]]
* [[fully faithful morphism]]
* [[conservative morphism]]
* [[pseudomonic morphism]]
* [[discrete morphism]]

**specific versions**

* globular [[strict 2-category]]
* [[bicategory]]

**limit notions**

* [[2-limit]]
* [[strict 2-limit]]
* [[flexible limit]]
* [[PIE limit]]

**model structures**

* [[canonical model structure]]
* [[2-trivial model structure]]

## Related concepts

* [[0-category]], [[(0,1)-category]]

* [[category]]

* **2-category**

  [[equivalence in a 2-category]]
  
  [[localization of a 2-category]]

* [[3-category]]

* [[n-category]]

* [[(∞,0)-category]]

* [[(∞,1)-category]]

* [[(∞,2)-category]]

* [[(∞,n)-category]]

* [[(n,r)-category]]

## References

A brief account of the definition is in

* [[Ross Street]], _Encyclopedia article on 2-categories and bicategories_ ([pdf](http://www.maths.mq.edu.au/~street/Encyclopedia.pdf))

A more detailed account of the definition, including a discussion of its  [[coherence theorem]], is in

* [[Tom Leinster]], _Basic bicategories_ ([arXiv:9810017](http://arxiv.org/abs/math/9810017))

A comprehensive monograph is

* {#JohnsonYau20} [[Niles Johnson]], [[Donald Yau]], _2-Dimensional Categories_, Oxford University Press 2021 ([arXiv:2002.06055](http://arxiv.org/abs/2002.06055), [doi:10.1093/oso/9780198871378.001.0001](https://oxford.universitypressscholarship.com/view/10.1093/oso/9780198871378.001.0001/oso-9780198871378))

Some 2-category theory, including [[2-limit]]s/2-colimit is discussed in

* [[Steve Lack]], _A 2-categories companion_ ([arXiv:0702535](http://arxiv.org/abs/math/0702535))

and

* [[John Power]], _2-Categories_ ([pdf](http://www.brics.dk/NS/98/7/BRICS-NS-98-7.pdf))

An older reference which introduces some of the basic notions is

* [[Max Kelly]] and [[Ross Street]], *Review of the elements of 2-categories*, Sydney Category Seminar 1972/1973, LNM 420

A relation between bicategories and Tamsamani weak 2-categories is established in 

* [[Steve Lack]], [[Simona Paoli]], _2-nerves for bicategories_ ([arXiv](http://arxiv.org/abs/math/0607271))
{#LackPaoli}

The reverse construction is in

* [[Simona Paoli]], _From Tamsamani weak 2-categories to bicategories_ ([arXiv](http://www.maths.mq.edu.au/~simonap/Bicategories_Rev_4.pdf))

There is a [[model category]] structure on 2-categories -- the [[canonical model structure]] -- that models the [[(2,1)-category]] underlying [[2Cat]]:

* [[Steve Lack]],  _A Quillen Model Structure for 2-Categories_, K-Theory 26: 171&#8211;205, 2002. ([website](http://www.maths.usyd.edu.au/u/stevel/papers/qmc2cat.html))
{#LackStrict}

* [[Steve Lack]],  _A Quillen Model Structure for Biategories_, K-Theory 33: 185-197, 2004. ([website](http://www.maths.usyd.edu.au/u/stevel/papers/qmcbicat.html))
{#LackFolkModel}

Discussion of weak 2-categories in the style of [[A-infinity categories]] is (using [[dendroidal sets]] to model the higher [[operads]]) in

* Andor Lucacs, _Dendroidal weak 2-categories_ ([arXiv:1304.4278](http://de.arxiv.org/abs/1304.4278))

* Jonathan Chiche, _La th&#233;orie de l'homotopie des 2-cat&#233;gories_, thesis, [arXiv](http://arxiv.org/abs/1411.6936).

[[!redirects 2-category]]
[[!redirects 2-categories]]
[[!redirects weak 2-category]]
[[!redirects weak 2-categories]]

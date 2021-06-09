
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Depending on the chosen [[model category]] structure, the [[category]] [[sSet]] of [[simplicial set]]s may model [[∞-groupoids]] (for the standard [[model structure on simplicial sets]]) or [[(∞,1)-categories]] in the form of [[quasi-categories]] (for the [[Joyal model structure]]) on [[SSet]].

Accordingly, there are [[model category]] structures on [[sSet-categories]] that similarly model [[(n,r)-categories]] with $r$ shifted up by 1:

* there is a model structure on $SSet$-enriched categories whose fibrant objects are [[∞-groupoid]]/[[Kan complex]]-enriched categories and which models [[(∞,1)-categories]];

This we discuss [below](ModelForInfinityCategories).

* there is another model structure on [[sSet-categories]] whose fibrant objects are [[(∞,1)-category]]/[[quasi-category]]-enriched categories, and which model [[(∞,2)-categories]]. 

  For more on this see [elsewhere](%28infinity%2C2%29-category#TotMod)

Both are special cases of a [[model structure on enriched categories]].


## Model for $(\infty,1)$-categories
 {#ModelForInfinityCategories}

Here we describe the model category structure on [[SSet Cat]] that 
makes it a model for the [[(∞,1)-category of (∞,1)-categories]].

+-- {: .num_defn}
###### Definition

An [[sSet]]-[[enriched functor]] $F : C \to D$ between [[sSet-categories]] is called a **weak equivalence** precisely if

* it is **essentially surjective** in that the induced functor of [[homotopy categories]] is an ordinary [[essentially surjective functor]];

* it is an $\infty$-[[full and faithful functor]] in that for all objects $x,y \in C$ the morphism

  $$
    F_{x,y} : C(x,y) \to D(F(x), F(y))
  $$

  is a weak equivalence in the standard [[model structure on simplicial sets]].

Such a morphism is also called a **Dwyer-Kan weak equivalence** after the work by Dwyer-Kan on [[simplicial localization]]. 

=--


+-- {: .num_prop}
###### Proposition

A [[Quillen equivalence]] $C \stackrel{\leftarrow}{\to} D$ between [[model categories]] induces a Dwyer-Kan-equivalence $L C \leftrightarrow L D$ between their [[simplicial localization]]s.

=--

+-- {: .num_prop #BergnerModelStructure}
###### Proposition

The category [[SSet Cat]] of [[small category|small]] [[simplicially enriched categories]] carries the structure of a [[model category]] with

* weak equivalences the Dwyer-Kan equivalences;

* fibrations those [[sSet]]-[[enriched functor]]s $F : C \to D$ such that

  1. for all $x, y \in C$ the morphism $F_{x,y} : C(x,y) \to D(F(x), F(y))$ is a fibration in the standard [[model structure on simplicial sets]];


  1. the induced functor $\pi_0(F) : Ho(C) \to Ho(D)$ on [[homotopy categories]] is an [[isofibration]].

=--

([Bergner 04](#Bergner04))

+-- {: .num_remark}
###### Remark

In particular, the fibrant objects in this structure are the [[Kan complex]]-enriched categories, i.e. the strictly [[∞-groupoid]]-enriched ones (see [[(n,r)-category]]).

=--



## Properties

+-- {: .num_prop #RightProperness}
###### Proposition

The Bergner model structure of prop. \ref{BergnerModelStructure} is a [[proper model category]].


=--

A reference for right properness is ([Bergner 04, prop. 3.5](#Bergner04)). A reference for left properness is ([Lurie, A.3.2.4](#Lurie)) and ([Lurie, A.3.2.25](#Lurie)).


## Related concepts

* [[model structure for quasi-categories]]

* [[relation between quasi-categories and simplicial categories]]

* [[simplicial localization]]

[[!include table - models for (infinity,1)-operads]]


## References


A model category structure on the category of $sSet$-categories with a fixed set of objects was first given in 

* [[William Dwyer]], [[Dan Kan]], _Simplicial localization of categories_ , J. Pure and Applied Algebra 17 (3) (1980) ([pdf](https://www3.nd.edu/~wgd/Dvi/SimplicialLocalizations.pdf))

Dywer, Spalinski and later [[Charles Rezk|Rezk]] then pointed out that there ought to exist a model category structure on the collection of all $sSet$-categories that models the [[(∞,1)-category of (∞,1)-categories]]. This was then constructed in

* {#Bergner04} [[Julie Bergner]], _A model category structure on the category of simplicial categories_, Trans. AMS ([arXiv:0406507](http://arxiv.org/abs/math/0406507))

Also:

* {#Lurie} [[Jacob Lurie]], Section A.3.2 of: _[[Higher Topos Theory]]_

* [[Jacob Lurie]], _$(\infty,2)$-categories and the Goodwillie calculus_, [GoodwillieI.pdf](http://www.math.harvard.edu/~lurie/papers/GoodwillieI.pdf)

Survey and review:

* [[Julie Bergner]], Section 3 of: _A survey of $(\infty,1)$-categories_ ([arXiv:math/0610239](http://arxiv.org/abs/math/0610239))

* [[Emily Riehl]], Section 16 of: _[[Categorical Homotopy Theory]]_, Cambridge University Press, 2014 ([pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf), [doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457))




Recall the slight but crucial difference between the two notions of "[[simplicial categories]]", the other being an [[internal category]] in [[sSet]]. But also for this latter concept there is a [[model category]] structure which presents [[(infinity,1)-categories]], see

* {#Horel14} [[Geoffroy Horel]], _A model structure on internal categories_, Theory and Applications of Categories, Vol. 30, 2015, No. 20, pp 704-750 ([arXiv:1403.6873](http://arxiv.org/abs/1403.6873)).


[[!redirects model structure on SSet-categories]]
[[!redirects model structure on simplicial categories]]
[[!redirects model structure on simplicially enriched categories]]
[[!redirects Bergner model structure]]
[[!redirects Bergner model structure on simplicially enriched categories]]
[[!redirects Dwyer–Kan–Bergner model structure]]
[[!redirects Dwyer–Kan–Bergner model structure on simplicially enriched categories]]
[[!redirects Dwyer--Kan--Bergner model structure]]
[[!redirects Dwyer--Kan--Bergner model structure on simplicially enriched categories]]

[[!redirects Dwyer-Kan equivalence]]
[[!redirects Dwyer-Kan weak equivalence]]
[[!redirects Dwyer-Kan equivalence of simplicial categories]]
[[!redirects Dwyer-Kan equivalences]]
[[!redirects Dwyer-Kan weak equivalences]]
[[!redirects Dwyer-Kan equivalences of simplicial categories]]

[[!redirects Dwyer–Kan equivalence]]
[[!redirects Dwyer–Kan weak equivalence]]
[[!redirects Dwyer–Kan equivalence of simplicial categories]]
[[!redirects Dwyer–Kan equivalences]]
[[!redirects Dwyer–Kan weak equivalences]]
[[!redirects Dwyer–Kan equivalences of simplicial categories]]

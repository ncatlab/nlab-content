
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
* automatic table of contents goes here
{:toc}

## Idea

Depending on the chosen [[model category]] structure, the [[category]] [[sSet]] of [[simplicial set]]s may model [[∞-groupoids]] (for the standard [[model structure on simplicial sets]]) or [[(∞,1)-categories]] in the form of [[quasi-categories]] (for the [[Joyal model structure]]) on [[SSet]].

Accordingly, there are [[model category]] structures on [[sSet-categories]] that similarly model [[(n,r)-categories]] with $r$ shifted up by 1:

* there is a model structure on $SSet$-enriched categories whose fibrant objects are [[∞-groupoid]]/[[Kan complex]]-enriched categories and which models [[(∞,1)-categories]];

* there is another model structure on [[sSet-categories]] whose fibrant objects are [[(∞,1)-category]]/[[quasi-category]]-enriched categories, and which model [[(∞,2)-categories]].

## Model for $(\infty,1)$-categories

Here we describe the model category structure on [[SSet Cat]] that 
makes it a model for the [[(∞,1)-category of (∞,1)-categories]].

**Definition** An [[sSet]]-[[enriched functor]] $F : C \to D$ between [[sSet-categories]] is called a **weak equivalence** precisely if

* it is **essentially surjective** in that the induced functor of [[homotopy category|homotopy categories]] is an ordinary [[essentially surjective functor]];

* it is an $\infty$-[[full and faithful functor]] in that for all objects $x,y \in C$ the morphism

  $$
    F_{x,y} : C(x,y) \to D(F(x), F(y))
  $$

  is a weak equivalence in the standard [[model structure on simplicial sets]].

Such a morphism is also called a **Dwyer-Kan weak equivalence** after the work by Dwyer-Kan on [[simplicial localization]]. 

**Propositon** A [[Quillen equivalence]] $C \stackrel{\leftarrow}{\to} D$ between [[model categories]] induces a Dwyer-Kan-equivalence $L C \leftrightarrow L D$ between their [[simplicial localization]]s.

**Proposition** The category [[SSet Cat]] of [[small category|small]] [[simplicially enriched categories]] carries the structure of a [[model category]] with

* weak equivalences the Dwyer-Kan equivalences;

* fibrations those [[sSet]]-[[enriched functor]]s $F : C \to D$ such that

  1. for all $x, y \in C$ the morphism $F_{x,y} : C(x,y) \to D(F(x), F(y))$ is a fibration in the standard [[model structure on simplicial sets]];


  1. for every $x_1 \in C$, $y \in D$ and [[homotopy equivalence]] $e : F(x_1) \to y$, there exists an object $x_2 \in C$ and a homotopy equivalence $d : x_1 \to x_2$ such that $F(d) = e$.


In particualar, the fibrant objects in this structure are the [[Kan complex]]-enriched categories, i.e. the strictly [[∞-groupoid]]-enriched ones (see [[(n,r)-category]]).

### References

A model category structure on the category of $sSet$-categories with a fixed set of objects was first given in 

* Dwyer, [[Dan Kan]], _Simplicial localization of categories_ , J. Pure and Applied Algebra 17 (3) (1980), 

Dywer, Spalinski and later Rezk then pointed out that there ought to exist a model category structrue on the collection of all $sSet$-categories that models the [[(∞,1)-category of (∞,1)-categories]]. This was then constructed in

* [[Julie Bergner]], _A model category structure on the category of simplicial categories_ , Trans. AMS ([arXiv:0406507](http://arxiv.org/abs/math/0406507))

A survey is in section 3 of

* [[Julie Bergner]], _A survey of $(\infty,1)$-categories_ ([arXiv](http://arxiv.org/abs/math/0610239))

See also section A.3.2 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


## Model for $(\infty,2)$-categories

> for the moment see [[(∞,2)-category]] for more on this

### References

* [[Jacob Lurie]], _$(\infty,2)$-categories and the Goodwillie calculus_, [GoodwillieI.pdf](http://www.math.harvard.edu/~lurie/papers/GoodwillieI.pdf)

* MathOverflow: [cofibrations-of-simplical-categories-in-the-bergner-model-structure...](http://mathoverflow.net/questions/34959/cofibrations-of-simplical-categories-in-the-bergner-model-structure-induce-c)

[[!redirects model structure on SSet-categories]]
[[!redirects model structure on simplicial categories]]
[[!redirects model structure on simplicially enriched categories]]
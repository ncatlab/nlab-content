

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


This entry collects links related to the book

* [[Jacob Lurie]], 

  _Higher Topos Theory_,

  Annals of Mathematics Studies 170,

  Princeton University Press 2009

  ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))

which discusses the [[higher category theory]] of [[(∞,1)-categories]] in general and that of [[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-categories of (∞,1)-sheaves]] (i.e. of [[∞-stack]]s) -- called (Grothendieck-Rezk-Lurie) [[(∞,1)-topos]]es -- in particular.

The book is available online from the arXiv and also from Lurie's web site:

* [PDF of published version](https://www.math.ias.edu/~lurie/papers/highertopoi.pdf) from Lurie's web site

* [arXiv:math.CT/0608040](http://arxiv.org/abs/math.CT/0608040) -- this has been updated since the publication of the print version, including addition of some new material!

* [updated version from Lurie's web site](https://www.math.ias.edu/~lurie/papers/HTT.pdf) -- more recent even than the arXiv version, as of 2019

An online textbook of a similar content is developing at:

* [[Jacob Lurie]], _[[Kerodon]]_


#Contents#
* table of contents
{:toc}

#Related entries#

For general information on higher category and higher topos theory see also

* [[higher category theory]]

* [[higher topos theory]].

If you need basics, see

* [[category theory]]

* [[sheaf and topos theory]].

If you need more motivation see

* [[motivation for sheaves, cohomology and higher stacks]].

If you need to see applications see for instance

* [[cohomology]]

* [[structured (∞,1)-topos]]

* [[A Survey of Elliptic Cohomology]]

#Summary#

## General idea ## 

Recall the following familiar 1-categorical statement:

* Working in the 1-[[category]] [[Set]] of [[0-category|0-categories]] is the same as  doing [[set theory]]. The point of [[Categories and Sheaves|categories and sheaves]] is to pass to _parameterized_ [[0-category|0-categories]], namely [[presheaf]] categories: these [[topos|topoi]] behave much like the category [[Set]] but their objects are generalized [[space and quantity|spaces]] that may carry more structure, for instance they may be [[generalized smooth space]]s if one considers (pre)[[sheaf|sheaves]] on [[Diff]].

One can think of Lurie's book as a comprehensive study of the generalization of the above statement  from $1$ to $(\infty,1)$  (recall the notion of [[(n,r)-category]]):

* Working in the $(\infty,1)$-[[category]] [[∞Grpd]] of [[infinity-groupoid|(∞,0)-categories]] is the same as  doing [[topology]]. The point of  [[∞-stacks]] is to pass to _parameterized_ [[infinity-groupoid|(∞,0)-categories]], namely [[(∞,1)-presheaf]] categories: these [[(infinity,1)-topos|(∞,1)-topoi]] behave much like the $(\infty,1)$category [[∞Grpd]] but their objects are generalized [[space and quantity|spaces]] with higher [[homotopy|homotopies]] that may carry more structure, for instance they may be $\infty$-[[differentiable stack]]s if one considers [[∞-stacks]] on [[Diff]].

## First part, sections 1-4

Based on work by Andr&#233; Joyal on the [[quasi-category]] model for [[(∞,1)-categories]], Lurie presents a comprehensive account of the theory of [[(∞,1)-categories]] including the definitions and properties of all the standard items familiar from category theory (limits, fibrations, etc.)

## Second part, sections 5-7 ##

Given the $(\infty,1)$-categorical machinery from the first part there are natural $(\infty,1)$-categorical versions of $(\infty,1)$-[[presheaf]] and $(\infty,1)$-[[sheaf]] categories (i.e. $(\infty,1)$-categories of [[∞-stacks]]): the "$\infty$-topoi" that give the book its title (more descriptively, these would be called "Grothendieck $(\infty,1)$-topoi"). Lurie investigates their properties in great detail and thereby in particular puts the work by Brown, Joyal, Jardine, To&#235;n on the [[model structure on simplicial presheaves]] into a coherent $(\infty,1)$-categorical context by showing that, indeed, these are [[models for ∞-stack (∞,1)-toposes]].


#How to read the book#


## 1-categorical background ##

The book _Higher topos theory_ together with Lurie's work on [[Stable ∞-Categories]] is close to an $(\infty,1)$-categorical analog of the 1-categorical material as presented for instance in

* Kashiwara and Shapira, [[Categories and Sheaves]].

## Sections with crucial concepts ##

The book discusses crucial concepts and works out plenty of detailed properties. On first reading it may be helpful to skip over all the technical parts and pick out just the central conceptual ideas. These are the following:

* [section 1.1](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=13) : the concept of [[(∞,1)-category]]

* [section 5.1](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=256): the concept of [[(∞,1)-presheaves]]

* [section 6.1](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=426): the concept of [[(infinity,1)-topos|(∞,1)-topoi]]

* [section 6.2](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=459) 
[section 6.5](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=521) 
and : relation to the Brown-Joyal-Jardine-To&#235;n
theory of [[models for ∞-stack (∞,1)-toposes]] in terms of the [[model structure on simplicial presheaves]].


#Content#

##1 An overview of higher category theory

* [[higher category theory]]

  * [[∞-category]]

  * [[(n,r)-category]]

  * [[(∞,0)-category]]

    * [[∞-groupoid]]

    * [[Kan complex]]

    * [[topological space]]

  * [[(∞,1)-category]]

    * [[quasi-category]]

      * [[equivalence of quasi-categories]]

    * [[simplicially enriched category]]

      * [[homotopy coherent nerve]]

    * [[relation between quasi-categories and simplicial categories]]

    * [[complete Segal space]]

    * [[Segal category]]

  * [[(∞,n)-category]]
 

* constructions in quasi-categories

  * [[homotopy category of an (∞,1)-category]]

  * [[join of quasi-categories]]

    * [[join of simplicial sets]]

  * [[over quasi-category]]

  * [[terminal object in a quasi-category]]

  * [[limit in quasi-categories]]

  * [[sub-quasi-category]]

  * [[opposite (∞,1)-category]]/[[opposite quasi-category]]

* [[(∞,1)-functor]]

  * [[full and faithful (∞,1)-functor]]

  * [[(∞,1)-presheaf]]

  * [[(∞,1)-category of (∞,1)-functors]]

* [[adjoint functor|adjoint (∞,1)-functor]]





##2 Fibrations of Simplicial Sets ##

* [[model structure for quasi-categories]]

* [[fibrations of quasi-categories]]

  * [[Kan fibration]]
 
  * [[inner Kan fibration]]

  * [[left Kan fibration]]

  * [[right Kan fibration]]

  * [[Cartesian fibration]]

    * [[Cartesian morphism]]

  * [[anodyne morphism]]

### 2.1 Left fibrations

* [[left fibration]]

* [[model structure for left fibrations]]

### 2.2 Simplicial categories and $\infty$-categories

* [[relation between quasi-categories and simplicial categories]]

* [[model structure for quasi-categories]]

### 2.3 Inner fibrations

* [[inner fibration]]

#### 2.3.1 Correspondences

* [[correspondence]]

* [[graph of a functor]], [[cograph of a functor]]

#### 2.3.2 Stability properties of inner fibrations

(...)

#### 2.3.3 Minimal fibrations

* [[minimal inner fibration]]

#### 2.3.4 $n$-Categories

* [[(n,1)-category]]

* [[coskeleton]]


### 2.4 Cartesian fibrations

#### 2.4.1 Cartesian morphisms

* [[Cartesian morphism]]

#### 2.4.2 Cartesian fibrations

* [[Cartesian fibration]]

* [[model structure on marked simplicial over-sets]]

* [[(∞,1)-Grothendieck construction]]

#### 2.4.3 Stability properties of Cartesian fibrations

#### 2.4.4 Mapping spaces and Cartesian fibrations

#### 2.4.5 Application: Invariance of Undercategories

#### 2.4.6 Application: Categorical fibrations over a point

#### 2.4.7 Bifibrations

* [[codomain fibration]]

##3 The $\infty$-Category of $\infty$-Categories

* the [[(∞,2)-category]] [[(∞,1)Cat]]

* the [[(∞,1)-category of (∞,1)-categories]]

* [[(∞,1)-Grothendieck construction]]

  * [[cartesian fibration]]

    * [[cartesian morphism]]

  * [[model structure on marked simplicial over-sets]]

    * [[marked simplicial set]]

  * [[universal fibration of (∞,1)-categories]]

* [[limit in a quasi-category|limits of (∞,1)-categories]]

##4 Limits and Colimits {#Limits}


* [[limit in quasi-categories]]

  * [[fibration sequence]]

* [[idempotent]]

  * [[split idempotent]]

  * [[Karoubi envelope]]

### 4.1 Cofinality

* [[cofinal (∞,1)-functor]]

### 4.2 Techniques for computing colimits

* [[homotopy limit]]


### 4.3 Kan extensions

#### 4.3.1 Relative colimits

* [[relative (infinity,1)-colimit]]

...

### 4.4 Examples of colimits

...

##5 Presentable and Accessible $\infty$-Categories##

### 5.1 $(\infty,1)$-Categories of presheaves ###

* [[(∞,1)-category of (∞,1)-presheaves]]

* [[Yoneda lemma for (∞,1)-categories]]

### 5.2 Adjoint $(\infty,1)$-functors ###

* [[adjoint (∞,1)-functor]]

  * [[graph of a functor]]

  * [[cograph of a functor]]

  * [[adjoint functor theorem]]

  * [[Quillen adjunction]] / [[derived functor]]

#### 5.2.8 Factorization systems

* [[orthogonal factorization system in an (∞,1)-category]]

### 5.3 $(\infty,1)$-Categories of inductive limits ###

#### 5.3.1 Filtered $\infty$-categories

* [[cardinal number]]

* [[filtered (∞,1)-category]]


#### 5.3.2 Right exactness

* [[exact (∞,1)-functor]]


#### 5.3.3 Filtered colimits

#### 5.3.4 Compact objects

* [[compact object in an (∞,1)-category]]

#### 5.3.5 Ind-objects

* [[ind-object in an (∞,1)-category]]

* [[pro-object in an (∞,1)-category]]


#### 5.3.6 Adjoining colimits to $\infty$-categories


### 5.4 Accessible $(\infty,1)$-categories ###

#### 5.4.1 Locally small $\infty$-categories

* [[essentially small (∞,1)-category]]

* [[locally small (∞,1)-category]]

#### 5.4.2 Accessible $(\infty,1)$-categories

* [[accessible (∞,1)-category]]

* [[accessible (∞,1)-functor]]

#### 5.4.3 Accessible and idempotent-complete $(\infty,1)$-categories

* [[idempotent-complete (∞,1)-category]]


### 5.5 Presentable $(\infty,1)$-categories ###

#### 5.5.1 Presentability

* [[locally presentable (∞,1)-category]]



#### 5.5.2 Representable functors and the adjoint functor theorem

* [[adjoint (∞,1)-functor theorem]]


#### 5.5.3 Limits and colimits of presentable $\infty$-categories

* [[symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]]

#### 5.5.4 Local objects

* [[localization of an (∞,1)-category]]

  * [[reflective sub-(∞,1)-category]]

  * [[local object]]

  * [[local equivalence]]


#### 5.5.5 Factorization systems on presentable $\infty$-categories


#### 5.5.6 Truncated objects

* [[n-truncated object of an (∞,1)-category]]

  * [[monomorphism in an (∞,1)-category]]

  * [[subobject in an (∞,1)-category]]

* [[Postnikov tower in an (∞,1)-category]]


#### 5.5.7 Compactly generated $\infty$-categories

* [[compactly generated (∞,1)-category]]

#### 5.5.8 Nonabelian Derived Categories

* [[sifted (∞,1)-category]]

* [[(∞,1)-algebraic theory]]

#### 5.5.9 Quillen's model for $\mathcal{P}_\Sigma(C)$

* [[(∞,1)-algebraic theory|model structure for (∞,1)-algebras over (∞,1,)-algebraic theories]]

##6 $\infty$-Topoi##

### 6.1 Definitions and characterizations ###

#### 6.1.1 Giraud's Axioms in the $\infty$-Categorical setting

* [[∞-topos]]

  * [[(∞,1)-topos]]

* [[Giraud's axioms]]

  * [[groupoid object in an (∞,1)-category]]

  * [[universal colimits]]

* [[object classifier]]

#### 6.1.2 Groupoid objects

* [[simplicial object in an (∞,1)-category]]

* [[groupoid object in an (∞,1)-category]]

  * [[?ech nerve]]

  * [[effective epimorphism]]

  * [[simplicial resolution]]

  * [[delooping]]

    * [[quotient object]]


#### 6.1.3 $\infty$-Topoi and descent

* [[descent]]

* [[(∞,2)-sheaf]]

#### 6.1.4 Free Groupoids

(...)

#### 6.1.5 Giraud's theorem for $\infty$-Topoi

* [[Giraud's theorem]]

#### 6.1.6 $\infty$-Topoi and classifying objects
 {#ClassifyingObjects}

* [[object classifier in an (infinity,1)-topos]]


### 6.2 Constructions of $(\infty,1)$-toposes ###

#### 6.2.1 Left exact localization

* [[exact functor]]

* [[reflective sub-(∞,1)-category|exact reflective sub-(∞,1)-category]]


#### 6.2.2 Grothendieck topologies and sheaves in higher category theory

* [[(∞,1)-category of (∞,1)-sheaves]]

  * [[(∞,1)-site]]

  * [[(∞,1)-sheaf]]

  * [[topological localization]]

  * [[hypercompletion]]

  * [[local object]]

  * [[descent]]

  * [[sheaf]]

  * [[stack]]

  * [[∞-stack]]  

  * [[derived stack]]

  * [[∞-stackification]]

* [[models for ∞-stack (∞,1)-toposes]]

* [[model structure on simplicial presheaves]]

  * [[simplicial presheaf]]

  * [[global model structure on simplicial presheaves]]

  * [[local model structure on simplicial presheaves]]

  * [[local model structure on simplicial sheaves]]

  * [[descent for simplicial presheaves]]

#### 6.2.3 Effective epimorphisms

* [[(∞,1)-semitopos]]

* [[effective epimorphism in an (∞,1)-category]]

### 6.3 The $\infty$-Category of $\infty$-Topoi

#### 6.3.1 Geometric morphisms

* [[(∞,1)-geometric morphism]]

* [[(∞,1)Toposes]]

#### 6.3.2 Colimits of $\infty$-topoi

#### 6.3.3 Filtered limits of $\infty$-topoi

#### 6.3.4 General limits of $\infty$-topoi

#### 6.3.5 Etale Morphisms of $\infty$-topoi

* [[étale geometric morphism]]


### 6.4 $n$-Topoi ###

* [[(n,1)-topos]]

* [[n-localic (∞,1)-topos]]

### 6.5 Homotopy theory in an $(\infty,1)$-topos 


#### 6.5.1 Homotopy groups

* [[homotopy groups in an (∞,1)-topos]]

  * [[n-truncated object of an (∞,1)-topos]]

  * [[n-connected object of an (∞,1)-topos]]

  * [[Eilenberg-MacLane object]]

* [[cohomology]]

#### 6.5.2 $\infty$-Connectedness

#### 6.5.3 Hypercovering

* [[(∞,1)-sheafification]]/[[∞-stackification]]

* [[hypercover]]

* [[hypercomplete (∞,1)-topos]]

* [[Whitehead theorem]]

#### 6.5.4 Descent versus Hyperdescent

* [[topological localization]]

* [[hypercompletion]]

##7 Higher Topos Theory in Topology


### 7.1 Paracompact spaces

* [[shape of an (∞,1)-topos]]

* [[shape theory]]

### 7.2 Dimension theory

* [[homotopy]]

* [[cohomology]]

  * [[cocycle]]

  * [[Eilenberg-MacLane object]]

  * [[gerbe]], [[∞-gerbe]]

* [[dimension]]

  * [[homotopy dimension]]

  * [[cohomological dimension]] 

  * [[covering dimension]]

  * [[Heyting dimension]]


##Appendix##

### A.1 Category theory 


* [[category theory]]

* [[presentable category]]

* [[accessible category]]

* [[weak factorization system]]

* [[transfinite composition]]

* [[small object argument]]


* [[enriched category theory]]

  * [[monoidal category]]


### A.2 Model categories {#ModelCategories}

* [[homotopy theory]]

* [[category with weak equivalences]]

* [[homotopical category]]

  * [[enriched homotopical category]]

  * [[category of fibrant objects]]

  * [[Waldhausen category]]

  * [[simplicial localization]]
 
  * [[model category]]
 
    * [[Quillen adjunction]]

      * [[Quillen equivalence]]

    * [[Quillen bifunctor]]

    * [[monoidal model category]]

    * [[enriched model category]]

    * [[localization of a simplicial model category]]

      * [[Bousfield localization]]

  * [[Reedy model structure]]

### A.3 Simplicial categories


  * [[presentable (∞,1)-category]]

#### A.3.1 Enriched and monoidal model categoires

* [[enriched model category]]

* [[monoidal model category]]

* [[Quillen bifunctor]]

* [[simplicial model category]]



#### A.3.2 The model structure on $\mathbf{S}$-enriched categories

* [[simplicially enriched category]]

* [[combinatorial simplicial model category]]

* [[excellent model category]]

* [[model structure on sSet-categories]]

#### A.3.3 Model structures on diagram categories

* [[global model structure on functors]]

* [[Reedy model structure]]

* [[homotopy Kan extension]]


  * [[homotopy limit]]

  * [[homotopy colimit]]

#### A.3.4 Path spaces in $\mathbf{S}$-enriched categories

* [[(∞,1)-category of (∞,1)-functors]]

#### A.3.5 Homotopy colimits of $\mathbf{S}$-enriched categories

...

#### A.3.5 Exponentiation in model categories

...

#### A.3.7 Localizations of simplicial model categories

* [[Bousfield localization of model categories]]

* [[localization of a simplicial model category]]

* [[Combinatorial model categories have presentations]]

category: reference

[[!redirects HTT]]
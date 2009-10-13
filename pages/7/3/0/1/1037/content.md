<div class="rightHandSide toc">
[[!include mathematicscontents]]
***
[[!include (infinity,1)-topos - contents]]
</div>



This entry is about the book

* [[Jacob Lurie]], _Higher Topos Theory_ ([arXiv](http://arxiv.org/abs/math.CT/0608040), [published version](http://www-math.mit.edu/~lurie/papers/highertopoi.pdf))

which discusses the [[higher category theory]] of [[(∞,1)-categories]] in general and that of [[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-categories of (∞,1)-sheaves]] (i.e. of [[∞-stack]]s) -- called (Grothendieck-Rezk-Lurie) [[(∞,1)-topos]]es -- in particular.

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

* Working in the 1-[[category]] 
[[Set]]
of [[0-category|0-categories]] is the same as 
doing [[set theory]]. The point of 
[[Categories and Sheaves|categories and sheaves]]
is to pass to _parameterized_ 
[[0-category|0-categories]], namely 
[[presheaf]] categories: these [[topos|topoi]]
behave much like the category [[Set]]
but their objects are generalized 
[[space and quantity|spaces]] that may carry 
more structure, for instance they may
be [[generalized smooth space]]s if one considers
(pre)[[sheaf|sheaves]] on [[Diff]].

One can think of Lurie's book as a comprehensive study
of the generalization of the above statement 
from $1$ to $(\infty,1)$ 
(recall the notion of [[(n,r)-category]]):

* Working in the $(\infty,1)$-[[category]] 
[[∞Grpd]]
of [[infinity-groupoid|(∞,0)-categories]] 
is the same as 
doing [[topology]]. The point of 
[[∞-stacks]]
is to pass to _parameterized_ 
[[infinity-groupoid|(∞,0)-categories]], 
namely 
[[(∞,1)-presheaf]] categories: 
these [[(infinity,1)-topos|(∞,1)-topoi]]
behave much like the $(\infty,1)$category 
[[∞Grpd]]
but their objects are generalized 
[[space and quantity|spaces]] 
with higher [[homotopy|homotopies]]
that may carry 
more structure, for instance they may
be $\infty$-[[differentiable stack]]s if one considers
[[∞-stacks]] on [[Diff]].



## First part, sections 1-4

Based on work by Andr&eacute; Joyal on the [[quasi-category]] model for [[(∞,1)-categories]], Lurie presents a comprehensive account of the theory of [[(∞,1)-categories]] including the definitions and properties of all the standard items familiar from category theory (limits, fibrations, etc.)

## Second part, sections 5-7 ##

Given the $(\infty,1)$-categorical machinery from the first part there are natural $(\infty,1)$-categorical versions of $(\infty,1)$-[[presheaf]] and $(\infty,1)$-[[sheaf]] categories (i.e. $(\infty,1)$-categories of [[∞-stacks]]): the "$\infty$-topoi" that give the book its title (more descriptively, these would be called "Grothendieck $(\infty,1)$-topoi"). Lurie investigates their properties in great detail and thereby in particular puts the work by Brown, Joyal, Jardine, To&#235;n on the [[model structure on simplicial presheaves]] into a coherent $(\infty,1)$-categorical context by showing that, indeed, these are [[models for ∞-stack (∞,1)-toposes]].



#How to read this book#

## General remark ##

Don't be put-off by the sheer size. On top of everything else, Lurie is a great expositor. 

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
and : relation to the Brown-Joyal-Jardine-To&euml;n
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

    * [[complete Segal space]]

    * [[Segal category]]

  * [[(∞,n)-category]]
 

* $(\infty,1)$-categories

  * [[homotopy category of an (∞,1)-category]]

  * [[join of quasi-categories]]

    * [[join of simplicial sets]]

    * [[over quasi-category]]

  * [[terminal object in a quasi-category]]

* [[(∞,1)-functor]]

  * [[(∞,1)-presheaf]]

  * [[(∞,1)-category of (∞,1)-functors]]

* [[adjoint functor|adjoint (∞,1)-functor]]

* [[limit in quasi-categories]]




##2 Fibrations of Simplicial Sets ##

* [[model structure on simplicial sets]]

* [[fibrations of simplicial sets]]

  * [[Kan fibration]]
 
  * [[inner Kan fibration]]

  * [[left Kan fibration]]

  * [[right Kan fibration]]

  * [[Cartesian fibration]]

    * [[Cartesian morphism]]

  * [[anodyne morphism]]

##3 The $\infty$-Category of $\infty$-Categories

* [[(∞,1)-category of (∞,1)-categories]]

* [[Grothendieck construction]]

  * [[cartesian fibration]]

    * [[cartesian morphism]]

  * [[model structure on marked simplicial over-sets]]

    * [[marked simplicial set]]

  * [[universal fibration of (∞,1)-categories]]

* [[limit in a quasi-category|limits of (∞,1)-categories]]

##4 Limits and Colimits##

* [[homotopy limit]]

* [[limit in quasi-categories]]

  * [[fibration sequence]]

* [[idempotent]]

  * [[split idempotent]]

  * [[Karoubi envelope]]


##5 Presentable and Accessible $\infty$-Categories##

## 5.1 $(\infty,1)$-categories of presheaves ##

* [[(∞,1)-category of (∞,1)-presheaves]]

## 5.2 adjoint $(\infty,1)$-functors ##

* [[adjoint (∞,1)-functor]]

  * [[graph of a functor]]

  * [[cograph of a functor]]

  * [[adjoint functor theorem]]

## 5.3 $(\infty,1)$-categories of inductive limits ##

* [[ind-object in an (∞,1)-category]]

  * [[cardinal number]]

  * [[filtered (∞,1)-category]]

  * [[compact object in an (∞,1)-category]]

  * [[accessible (∞,1)-category]]

  * [[presentable (∞,1)-category]]

## 5.4 accessible $(\infty,1)$-categories ##

* [[accessible (∞,1)-category]]

## 5.5 presentable $(\infty,1)$-categories ##

* [[symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]]

* [[localization of an (∞,1)-category]]

  * [[reflective (∞,1)-subcategory]]

  * [[local object]]

  * [[local equivalence]]


##6 $\infty$-Topoi##


* [[∞-topos]]

  * [[(∞,1)-topos]]

* [[Giraud's axioms]]

  * [[groupoid object in an (∞,1)-category]]

  * [[universal colimits]]

* [[object classifier]]

* [[n-localic (∞,1)-topos]]

* [[(∞,1)-category of (∞,1)-sheaves]]

  * [[local object]]

  * [[descent]]

  * [[sheaf]]

  * [[stack]]

  * [[∞-stack]]  

  * [[derived stack]]

  * [[∞-stackification]]

  * [[hypercompletion]]


* [[models for ∞-stack (∞,1)-toposes]]

* [[model structure on simplicial presheaves]]

  * [[simplicial presheaf]]

  * [[global model structure on simplicial presheaves]]

  * [[local model structure on simplicial presheaves]]

  * [[local model structure on simplicial sheaves]]

  * [[descent for simplicial presheaves]]

* [[groupoid object in an (∞,1)-category]]

  * [[Cech nerve]]

  * [[effective epimorphism]]

  * [[simplicial resolution]]

  * [[delooping]]

    * [[quotient object]]

* [[cohomology]]

  * [[nonabelian cohomology]]

  * [[Cech cohomology]]

  * [[fibration sequence]]

    * [[principal ∞-bundle]]
   
      * [[gerbe (general idea)]]
  
      * [[gerbe (as a stack)]]
     
      * [[bundle gerbe]]

      * [[principal 2-bundle]]

* [[homotopy group (of an ∞-stack)]]

  * [[n-truncated object of an (∞,1)-topos]]
     
##7 Higher Topos Theory in Topology






##Appendix##

### Category theory ###


* [[category theory]]

* [[presentable category]]

* [[accessible category]]

* [[weak factorization system]]

* [[transfinite composition]]

* [[small object argument]]


* [[enriched category theory]]

  * [[monoidal category]]


### Model categories ###

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

### Simplicial model categories

* [[simplicially enriched category]]

* [[simplicial model category]]

  * [[localization of a simplicial model category]]

  * [[Bousfield localization]]

* [[combinatorial simplicial model category]]

  * [[presentable (∞,1)-category]]


category: reference

[[!redirects HTT]]
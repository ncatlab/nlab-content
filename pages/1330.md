#Idea#


A _[[localization]]_ of an [[(infinity,1)-category]] $C$ is a functor $L : C \to C_0$ to an $(\infty,1)$-subcategory $C_0 \hookrightarrow C$ such that with $c$ any object there is a morphism connecting it to its localization 

$$
  c \to L(c)
$$

in a suitable way. This "suitable way" just says that 
$f$ is left adjoint to the fully faithful inclusion functor.


Since localizations are entirely determined by which morphisms in $C$ are sent to equivalences in $C_0$, they can be thought of as sending $C$ to the result of "inverting" all these morphisms, a process familiar from forming the [[homotopy category]] of a [[homotopical category]].



#Definition#

The left adjoint $(\infty,1)$-functor

$$
  f : C \to C_0
$$

to a [[reflective (infinity,1)-subcategory]] $C_0 \hookrightarrow C$ is called 
a **localization** of $C$.

#Examples#

* [[simplicial model category|Simplicial model categories]] model [[(infinity,1)-category|(infinity,1)-categories]]. [[localization of a simplicial model category]] accordingly models localization of the corresponding $(\infty,1)$-category.


#Examples#

* [[infinity-stackification]] is the localization of an [[(infinity,1)-category]] of [[(infinity,1)-presheaf|(infinity,1)-presheaves]] to the $(\infty,1)$-subcategory [[(infinity,1)-category of (infinity,1)-sheaves|of (infinity,1)-sheaves]].


#References#

[definition 5.2.7.2](http://www-math.mit.edu/~lurie/papers/highertopoi.pdf#page=296) of

* [[Jacob Lurie]], [[Higher Topos Theory]]

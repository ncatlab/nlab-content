[[!redirects Pi-algebras]]
[[!redirects Pi-algebras]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}
 
##Idea

A _$\Pi$-algebra_ is an algebraic model for the [[homotopy group]]s $\pi_*X$ of a pointed [[topological space]], $X$, together with the [[action]] of the [[primary homotopy operation]]s on them, in the same sense that algebras over the [[Steenrod algebra]] are models for the [[cohomology]] of a space.


## The category $\Pi$ of homotopy operations

The [[category]] $\Pi$ of homotopy operations has

* as [[object]]s - pointed [[CW-complex]]es with the [[homotopy type]] of a finite [[wedge product]] of [[sphere]]s of [[dimension]]s $\geq 1$;


* as [[morphism]]s - homotopy classes of (pointed) [[continuous function]]s between them.

### Properties

*  $\Pi$ is a pointed category and has finite coproducts (given by the finite wedges), but not products.

 *  There is a [[functor]], _smash product_ $i : \Pi\times \Pi \to \Pi$, which sends an object $(U,V)$ to $U\wedge V = (U\times V)/((U\times *)\vee(*\times V))$, which preserves [[coproduct]]s in each variable.


##$\Pi$-algebras

Let $Set_*$ denote the category of [[pointed sets]].

+--
{: . un_defn}
######Definition

A _$\Pi$-algebra_ is a [[functor]] $A: \Pi^{op}\to Set_*$, which sends [[coproduct]]s to [[products]].

A morphism of $\Pi$-algebras is a natural transformation between the corresponding functors.

=--

### Properties

* A $\Pi$-algebra $A$ satisfies $A* = *$.

* The values of a $\Pi$-algebra $A$ are determined by the values $A_n = A(S^n)$, that it takes on the spheres, $S^n$, $n\geq 1$.

*  A $\Pi$-algebra can be considered to be a graded [[group]] $\{A_n\}_{n=1}^\infty$ with $A_n$ abelian for $n\gt 1$, together with  

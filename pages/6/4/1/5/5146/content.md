
#Contents#
* table of contents
{:toc}
 
##Idea
A _$\Pi$-algebra_ is an algebraic model for the homotopy groups $\pi_*X$ of a pointed space, $X$, together with the action of the [[primary homotopy operations]] on them, in the same sense that algebras over the Steenrod algebra are models for the cohomology of a space.


##The category $\Pi$ of homotopy operations
This has

* as objects - pointed CW-complexes with the homotopy type of a finite wedge of spheres of dimensions $\geq 1$;


* as morphisms - homotopy classes of (pointed) maps between them.

###Note
   *  $\Pi$ is a pointed category and has finite coproducts (given by the finite wedges), but not products.

   *  There is a functor, _smash product_ $i : \Pi\times \Pi \to \Pi$, which sends an object $(U,V)$ to $U\wedge V = (U\times V)/((U\times *)\vee(*\times V))$, which preserves coproducts in each variable.


##$\Pi$-algebras
Let $Set_*$ denote the category of [[pointed sets]].

+--
{: . un_defn}
######Definition

A _$\Pi$-algebra_ is a functor $A: \Pi^{op}\to Set_*$, which sends coproducts to products.

A morphism of $\Pi$-algebras is a natural transformation between the corresponding functors.

=--

###Note

* A $\Pi$-algebra $A$ satisfies $A* = *$.

* The values of a $\Pi$-algebra $A$ are determined by the values $A_n = A(S^n)$, that it takes on the spheres, $S^n$, $n\geq 1$.

*  A $\Pi$-algebra can be considered to be a graded group $\{A_n\}_{n=1}^\infty$ with $A_n$ abelian for $n\gt 1$, together with  
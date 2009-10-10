
#Idea#

An _enriched model category_ is an [[enriched category]] $C$ together with the structure of a [[model category]] on the underlying [[category]] $C_0$ such that both structures are compatible in a reasonable way.


#Definition#

Let $V$ be a [[monoidal model category]].

A **$V$-enriched model category** is

* an V-[[enriched category]] $C$

  * which is [[power]]ed and [[copower]]ed over $V$;

* with the structure of a [[model category]] on the underlying category $C_0$

* such that for every cofibration $i : A \to B$ and every fibration $p : X \to Y$ in $C_0$ the morphism in $V$ $C(B,X) \stackrel{i^* \times p_*}{\to} C(A,X) \times_{C(A,Y)} C(B,Y)$ is a fibration with respect to the model structure on $V$;

* and such that this fibration is an acyclic fibration whenever either $i$ or $p$ are acyclic.

The last two conditions here are equivalent to the fact that the [[copower]]

$$
  \otimes : C \times V \to X
$$

is a [[Quillen bifunctor]].

#Remarks#

* The concept can be generalized to [[enriched homotopical category]].


#Examples#

* The most familiar examples of enriched model categories are [[simplicial model category|simplicial model categories]].


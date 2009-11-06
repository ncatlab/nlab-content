<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#

* tic
{:toc}

## Idea ## 

A Quillen bifunctor is a [[functor]] of two variables between [[model category|model categories]] that respects combined cofibrations in its two arguments in a suitable sense.

The notion of Quillen bifunctor enters the definition of [[monoidal model category]] and of [[enriched model category]].

##Definition##

+-- {: .un_defn}
###### Definition
**(Quillen bifunctor)**

Let $C, D, E$ be [[model category|model categories]]. A
[[functor]] $F : C \times D \to E$ is a **Quillen bifunctor** 
if it satisfies the following two conditions:

1. for any cofibration $i : c \to c'$ in $C$ and cofibration 
   $j : d \to d'$ in $D$, the induced morphism 
   
   $$
     F(c', d) \coprod_{F(c,d)} F(c,d') \to F(c', d')
   $$

   is a cofibration in $E$, which is a weak equivalence if either $i$ or $j$ is  a weak equivalence

1. it preserves [[colimit]]s separately in each variable

=--

##Remarks##

In full detail the [[pushout]] appearing in the first condition is the one sitting in the pushout diagram

$$
  \array{
    F(c,d) &\stackrel{F(Id,j)}{\to}& F(c,d')
    \\
    \;\;\downarrow^{F(i,Id)} && \downarrow
    \\
    F(c',d) &\stackrel{}{\to}&
    F(c', d) \coprod_{F(c,d)} F(c,d') 
  }
  \,.
$$

In particular, if $i = (\emptyset \hookrightarrow c)$ we have $F(\emptyset, d) = F(\emptyset, d') = \emptyset$ (since the [[initial object]] is the [[colimit]] over the empty diagram and $F$ is assumed to preserve colimits) and the above pushout diagram reduces to

$$
  \array{
    \emptyset &{\to}& \emptyset
    \\
    \;\;\downarrow && \downarrow
    \\
    F(c,d) &\stackrel{}{\to}&
    F(c,d) 
  }
  \,.
$$

Therefore for $c$ a cofibrant object the condition is that $F(c,-) : D \to E$ preserves cofibrations and acyclic cofibrations. Similarly for $d$ cofibrant the condition is that $F(-,d) : C \to E$ preserves cofibrations and acyclic cofibrations.


## Applications ##

* In a [[monoidal model category]] $C$ the [[tensor product]] $\otimes : C \times C \to C$
  is required to be a Quillen bifunctor.
  
* An [[enriched model category]] $D$ over the [[monoidal model category]] $C$ is one that is [[power]]ed and [[copower]]ed over $D$ such that the [[copower]] $\otimes : D \times C \to D$ is a Quillen bifunctor.

## Properties ##

The following proposition asserts that under mild conditions
a Quillem bifunctor on $C \times D$ lifts to a Quillen bifunctor
on [[functor category|functor categories]] of functors to $C$ and $D$.



+-- {: .un_prop}
###### Proposition

Let $\otimes : C \times D \to E$ be a Quillen functor. Let 

* $S$ be a [[Reedy category]] 
  and take the [[functor category|functor categories]] 
  $[S,C]$ and $[S^{op},C]$ be equipped with the corresponding[[Reedy model structure]].
  
* _or_ assume that $C$ and $D$ are [[combinatorial model category|combinatorial model categories]]
  and let $[S,C]$ and $[S^{op},A]$ be equipped, respective with the projective and
  the injective globel [[global model structure on functors|model structure on functor categories]].
  
Then the [[coend]] [[functor]]

$$
  \int^{S} (- \otimes -) : [S,C]\times [S^{op},D] \to E
$$

is again a &#180;Quillen bifunctor.

=--

+-- {: .proof}
###### Proof

This is proposition A.2.9.26 together with remark A.2.9.27 in 

* [[Jacob Lurie]], [[Higher Topos Theory]]

=--

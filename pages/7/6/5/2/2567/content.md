

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ## 

A _(left) Quillen [[bifunctor]]_ is a [[functor]] of two variables between [[model category|model categories]] that respects combined [[cofibrations]] in its two arguments in a suitable sense.

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

## Properties {#Properties}


+-- {: .un_prop}
###### Proposition

Let $\otimes : C \times D \to E$ be an [[adjunction of two variables]] between model categories and assume that $C$ and $D$ are [[cofibrantly generated model categories]]. Then $\otimes$ is a Quillen bifunctor precisely if it satisfies its axioms on generating (acyclic) cofibrations, i.e. if for $f : c_1 \to c_2$ and $g : d_1 \to d_2$ we have for the morphism

$$
 (c_1 \otimes d_2) \coprod_{c_1 \otimes d_1} (c_2 \otimes d_1)
  \to
  c_2 \otimes d_2
$$

is 

* a cofibration if both $f$ and $g$ are generating cofibrations;

* an acyclic cofibration if one is a generating cofibration and the other a generating acyclic cofibration.


=--

This appears for instance as Corollary 4.2.5 in 

* [[Mark Hovey]], _Model Categories_

## Applications ##


### Monoidal and enriched model categories ###

* In a [[monoidal model category]] $C$ the [[tensor product]] $\otimes : C \times C \to C$
  is required to be a Quillen bifunctor.
  
* An [[enriched model category]] $D$ over the [[monoidal model category]] $C$ is one that is [[power]]ed and [[copower]]ed over $D$ such that the [[copower]] $\otimes : D \times C \to D$ is a Quillen bifunctor.


### Lift to coends over tensors ###
 {#CoendsOverTensors}


The following proposition asserts that under mild conditions
a Quillen bifunctor on $C \times D$ lifts to a Quillen bifunctor
on [[functor category|functor categories]] of functors to $C$ and $D$.



+-- {: .un_prop}
###### Proposition

Let $\otimes : C \times D \to E$ be a Quillen functor. Let 

* $S$ be a [[Reedy category]] 
  and take the [[functor category|functor categories]] 
  $[S,C]$ and $[S^{op},C]$ be equipped with the corresponding[[Reedy model structure]].
  
* _or_ assume that $C$ and $D$ are [[combinatorial model category|combinatorial model categories]]
  and let $[S,C]$ and $[S^{op},A]$ be equipped, respectively with the projective and
  the injective globel [[global model structure on functors|model structure on functor categories]].
  
Then the [[coend]] [[functor]]

$$
  \int^{S} (- \otimes -) : [S,C]\times [S^{op},D] \to E
$$

is again a &#180;Quillen bifunctor.

=--


This [Lurie, prop. A.2.9.26 with remark A.2.9.27](#Lurie). 

It follows that the corresponding left [[derived functor]] computes the corresponding [[homotopy coend]].

### Bousfield-Kan type homotopy colimits ###

This is an application of the above application.

Let $C$ be a [[category]] and $A$ be a [[simplicial model category]]. Let $F : C \to A$ be a functor and let ${*} : C^{op} \to A$ be the functor constant on the terminal object.

Consider the [[global model structure on functors]] $[C^{op},SSet]_{proj}$ and $[C^{op},A]_{inj}$ and let
$Q({*})_{proj}$ be a cofibrant replacement for ${*}$ in $[C^{op},Set]_{proj}$ and $Q_{inj}(F)$ a cofibrant replacement for $F$ in $[C,A]_{inj}$.

One show that the [[homotopy colimit]] over $F$ is computed as the [[coend]] or [[weighted limit]]

$$
  hocolim F = \int Q_{proj}({*}) \cdot Q_{inj}(F)
  \,.
$$

One possible choice is 

$$
  Q_{proj}({*})
  =
  N(-/C)^{op}
  \,.
$$

That this is indeed a projectively cofibrant resulution of the constant on the [[terminal object]] is for instance proposition 14.8.9 of

* Hirschhorn, _Model categories and their localization_ .

For the case that $C = \Delta^{op}$ this is the classical choice by Bousfield and Kan, see [[Bousfield-Kan map]].

Assume that $A$ takes values in cofibrant objects of $A$, then it is already cofibrant in the injective model structure $[C,A]_{inj}$ on functors and we can take $Q_{inj}(F) = F$. Then the above says that

$$
  hocolim F = \int N(-/C)^\op \cdot F
  \,.
$$

For $C = \Delta$ this is the classical prescription by Bousfield-Kan for homotopy colimits, see also the discussion at [[weighted limit]].

Using the above proposition, it follows in particular explicitly that the homotopy colimit preserves degreewise cofibrations of functors over which it is taken.

A nice discussion of this is in ([Gambino](#Gambino)).


## References

Appendix A.2 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
{#Lurie}

* Nicola Gambino, _Weighted limits in simplicial homotopy theory_ ([pdf](http://www.crm.cat/Publications/08/Pr790.pdf))
{#Gambino}
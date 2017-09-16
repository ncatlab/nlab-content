The Yoneda lemma is an elementary but deep and central result in [[category theory]] and in particular in [[sheaf and topos theory]]. It is essential background behind the central concepts of [[representable functor]] and [[universal construction]]. 

#Preliminaries#

Recall that for $C$ a [[locally small category]] and $[C^{op}, Set] (= Set^{C^{op}} = Hom(C^{op},Set))$ the category of [[presheaf|presheaves]] on $C$, there naturally is a functor 

$$
  Y : C \to [C^op,Set]
$$

-- called the [[Yoneda embedding]] for reasons explained below -- which sends $C$ to the category of presheaves over it: this is just the image of the Hom-functor

$$
  C(-,-) : C^op \times C \to Set
$$

under the Hom-adjunction 

$$
  Hom(C^{op} \times C, Set) \stackrel{\simeq}{\to}
  Hom(C, [C^{op}, Set])
$$

in the [[closed monoidal category|closed]] [[monoidal category|symmetric monoidal category]] of categories.

Hence $Y$ sends any object $c \in C$ to the presheaf which assigns to any other object $d$ of $c$ the set of morphisms from $d$ into $c$:

$$
  Y(c) : C^{op} \stackrel{C(-,c)}{\to} Set
  \,.
$$

## Remarks ##

One way to appreciate the meaning of this and of what the Yoneda lemma has to say about it is to regard this in the context of [[space and quantity]]: thinking of the objects of $C$ as test spaces, presheaves on $C$ are generalized spaces modeled on $C$ which are characterized by the way one can map objects of $C$ into them. 

The Yoneda lemma states that the functor $Y$ has good properties which make this interpretation consistent.

#The Yoneda Lemma#

Let $C$ be a [[locally small category]], $[C^{op}, Set]$ the category of [[presheaf|presheaves]] on $C$, then

$$
  [C^op,Set](C(-c),X) \simeq X(c)
$$

naturally for all $c \in C$.

##Remarks##

In the light of the interpretation in terms of [[space and quantity]] mentioned above this says that for $X$ a generalized space modeled on $C$, and for $c$ a test space, morphisms from $c$ to $X$ with $c$ regarded as a generalized space are just the morphisms from $c$ into $X$.

#Corollary: Yoneda embedding#

As an immediate corollary the Yoneda lemma implies that the [[Yoneda embedding]] functor $Y : C \to [C^op,Set]$ really is an _embedding_ in that it is a [[full and faithful functor]], because for $c,d \in C$ it naturally induces the isomorphism of Hom-sets.

$$
  [C^{op},Set](C(-,c),C(-,d)) \simeq (C(-,d))(c) = C(c,d)
$$

#Generalizations#

The Yoneda lemma tends to carry over to all important generalizations of the context of [[locally small category|categories]]:

* There is an analog of the Yoneda lemma in [[enriched category theory]].

* In the context of [[module]]s (see also [[Day convolution]]) the Yoneda lemma becomes the important statement of [[Yoneda reduction]], which identifies the bimodule $\hom_C(-, -)$ as a unit bimodule.

* In the context of [[infinity-category|infinity-categories]] the Yoneda lemma becomes the [[descent and codescent]] condition on [[infinity-stack]]s. This is described in [[infinity-stack homotopically]].

* In [[functional programming]], the Yoneda embedding is the [[continuation passing style]] transform.

#Related constructions#

* The [[co-Yoneda lemma]].

#References#

* Tom Leinster, [[LeinsterYoneda.ps:file]] 
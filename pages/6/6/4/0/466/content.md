<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


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

Let $C$ be a [[locally small category]], $[C^{op}, Set]$ the category of [[presheaf|presheaves]] on $C$, then for all $c \in C$ there is a canonical [[isomorphism]]

$$
  [C^op,Set](C(-,c),X) \simeq X(c)
  \,.
$$

This is _natural_ in $c$ and $X$, i.e. there is in fact an [[isomorphism]] in the [[functor category]] $[C^{op} \times [C^{op},Set],Set]$ between the left and the right side.


## Proof ##

The crucial point is that the naturality condition on any [[natural transformation]] $\eta : C(-,c) \Rightarrow X$ is sufficient to ensure that $\eta$ is already entirely fixed by the value $\eta_c(Id_c) \in F(c)$ of its component $\eta_c : C(c,c) \to X(c)$ on the [[identity morphism]] $Id_c$.
And every such value extends to a natural transformation $\eta$.


More in detail, the bijection is established by the map

$$
  [C^{op}, Set](C(-,c),X)
  \stackrel{|_{c}}{\to}
  Set(C(c,c), X(c))
  \stackrel{ev_{Id_c}}{\to}
  X(c)
$$

where the first step is taking the component of a [[natural transformation]] at $c \in C$ and the second step is evaluation at $Id_c \in C(c,c)$. 

The inverse of this map takes $f \in X(c)$ to the natural transformation $\eta^f$ with components
$$
  \eta^f_d := X(-)(f) : C(d,c) \to X(d)
  \,.
$$




##Remarks##

In the light of the interpretation in terms of [[space and quantity]] mentioned above this says that for $X$ a generalized space modeled on $C$, and for $c$ a test space, morphisms from $c$ to $X$ with $c$ regarded as a generalized space are just the morphisms from $c$ into $X$.

#Corollaries#

The Yoneda lemma has the following direct consequences. As the Yoneda lemma itself, these are as easily established as they are useful and important.

## corollary I: Yoneda embedding#

The Yoneda lemma implies that the [[Yoneda embedding]] functor $Y : C \to [C^op,Set]$ really is an _embedding_ in that it is a [[full and faithful functor]], because for $c,d \in C$ it naturally induces the isomorphism of Hom-sets.

$$
  [C^{op},Set](C(-,c),C(-,d)) \simeq (C(-,d))(c) = C(c,d)
$$


## corollary II: uniqueness of representing objects ##

Since the [[Yoneda embedding]] is a [[full and faithful functor]], an [[isomorphism]] of [[representable functor|representable presheaves]] $Y(c) \simeq Y(d)$ must come from an [[isomorphism]] of the representing objects $c \simeq d$:

$$
  Y(c) \simeq Y(d) \;\; \Leftrightarrow \;\;
  c \simeq d
$$

### corollary III: universality of representing objects ###

A [[nLab:presheaf|presheaf]] $X : C^{op} \to Set$ is [[nLab:representable functor|representable]] precisely if the [[nLab:comma category|comma category]] $(Y,const_X)$ has a [[nLab:terminal object|terminal object]]. If a [[nLab:terminal object|terminal object]] is $(d, f : Y(d) \to X) \simeq (d, f \in X(d))$ then $X \simeq Y(d)$.

This follows from unwrapping the definition of morphisms in the [[nLab:comma category|comma category]] $(Y,const_X)$ and applying the Yoneda lemma to find

$$
  (Y,const_X)((c,f \in X(c)), (d, g \in X(d)))
  \simeq
  \{
    u \in C(c,d) : X(u)(g) = f
  \}
  \,.
$$

Hence $(Y,const_X)((c,f \in X(c), (d, g \in X(d))) \simeq pt$ says precisely that $X(-)(f) : C(c,d) \to X(c)$ is a bijection.

## Interpretation ##

For emphasis, here is the interpretation of these three corollaries in words:

* **corollary I** says that the interpretation of presheaves in $C$ as generalized objects probeable by objects of $c$ is consistent: the probes of $X$ by $c$ are indeed the maps of generalized objects from $c$ into $X$;

* **corollary II** says that probes by objects of $C$ are sufficient to distinguish objects of $C$: two objects of $C$ are the same if they have the same probes by other objects of $C$.

* **corollary III** characterizes [[representable functor]]s by a [[universal property]] and is hence the bridge between the notion of [[representable functor]] and [[universal construction]]s.


#Generalizations#

The Yoneda lemma tends to carry over to all important generalizations of the context of [[locally small category|categories]]:

* There is an analog of the Yoneda lemma in [[enriched category theory]].

* In the context of [[module]]s (see also [[Day convolution]]) the Yoneda lemma becomes the important statement of [[Yoneda reduction]], which identifies the bimodule $\hom_C(-, -)$ as a unit bimodule.

* In the context of [[infinity-category|infinity-categories]] the Yoneda lemma becomes the [[descent]] condition on [[infinity-stack]]s. This is described in [[infinity-stack homotopically]].

* In [[functional programming]], the Yoneda embedding is the [[continuation passing style]] transform.

#Related constructions#

* [[Yoneda reduction]]

* [[co-Yoneda lemma]]

#References#

* [[Tom Leinster]], [[LeinsterYoneda.ps:file]] 
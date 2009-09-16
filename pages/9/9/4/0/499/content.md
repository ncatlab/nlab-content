#Definition#

The **Yoneda embedding** for $C$ a [[locally small category]] is the functor

$$
  Y : C \to [C^{op}, Set]
$$

from $C$ to the category of [[presheaf|presheaves]] over $C$
which is the image of the Hom-functor

$$
  Hom : C^{op} \times C \to Set
$$

under the Hom adjunction

$$
  Hom(C^{op} \times C , Set) \simeq
  Hom(C, [C^{op}, Set])
$$

in the [[closed monoidal category|closed]] [[monoidal category|symmetric monoidal category]] $Cat$.

Hence $Y$ sends any object $c \in C$ to the presheaf which assigns to any other object $d$ of $c$ the set of morphisms from $d$ into $c$:

$$
  Y(c) : C^{op} \stackrel{C(-,c)}{\to} Set
  \,.
$$

# Properties

It follows from the [[Yoneda lemma]] the functor $Y$ is a [[full and faithful functor]]. It is also preserving colimits (= right continuous functor), but in general not preserving limits. 

The Yoneda embedding of a [[small category]] $S$ into the category of [[presheaf|presheaves]] on $S$ gives a [[free cocompletion]] of $S$.
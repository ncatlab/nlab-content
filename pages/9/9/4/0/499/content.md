The _Yoneda embedding_ for $C$ a [[locally small]] category is the functor

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

in the [[closed category|clossed]] [[monoidal category|symmetric monoidal category]] $Cat$:

for $c \in C$ any object the presheaf $Y(c)$ is given by

$$
  Y(c) : C^{op} \stackrel{C(-,c)}{\to} Set
  \,.
$$

It follows from the [[Yoneda lemma]] the functor $Y$ is a [[full and faithful functor]].

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For $C$ a [[locally small category]], every [[object]] $X$ of $C$ induces a [[presheaf]] on $C$: the [[representable presheaf]] $h_X$ represented by $X$. This assignment extends to a [[functor]] $C \to [C^{op}, Set]$ from $C$ to its [[category of presheaves]].
The [[Yoneda lemma]] implies that this functor is [[full and faithful functor|full and faithful]] and hence realizes $C$ as a [[full subcategory]] inside its category of presheaves.

Recall from the discussion at [[representable presheaf]] that the presheaf represented by an objct $X$ of $C$ is the functor $h_X :C^{op} \to Set$ whose assignment is illustrated by

<img src="http://ncatlab.org/ericforgy/files/hxalpha3.jpg" width = "400"/>

which sends each object $U$ to $Hom_C(U,X)$ and each morphism $\alpha:U'\to U$ to the function

$$h_X\alpha: Hom_C(U,X)\to Hom_C(U',X).$$

Moreover, for $f : X \to Y$ an [[morphism]] in $C$, this induces a [[natural transformation]] $h_f : h_X \to h_Y$, whose component on $U$ in $X$ is illustrated by

<img src="http://ncatlab.org/ericforgy/files/hf.jpg" width = "400"/>

For this to be a natural transformation, we need to have the commuting diagram

$$\array{
h_X U & \stackrel{h_f U}{\rightarrow} & h_Y U \\
\mathllap{h_X\alpha\quad}{\downarrow} & {} & \mathrlap{\downarrow}{\quad h_Y\alpha} \\
h_X U' & \stackrel{h_f U'}{\rightarrow} & h_Y U'
}$$

but this simply means that it doesn't matter if we first "comb" the strands back to $U'$ and then comb the strands forward to $Y$, or comb the strands forward to $Y$ first and then comb the strands back to $U'$


<img src="http://ncatlab.org/ericforgy/files/nattrans.jpg" width = "600"/>

which follows from associativity of composition of morphisms in $C$.




 

## Definition

The **Yoneda embedding** for $C$ a [[locally small category]] is the [[functor]]

$$
  Y : C \to [C^{op}, Set]
$$

from $C$ to the [[category of presheaves]] over $C$
which is the image of the [[hom-functor]]

$$
  Hom : C^{op} \times C \to Set
$$

under the Hom [[adjunction]]

$$
  Hom(C^{op} \times C , Set) \simeq
  Hom(C, [C^{op}, Set])
$$

in the [[closed monoidal category|closed]] [[monoidal category|symmetric monoidal category]] [[Cat]].

Hence $Y$ sends any [[object]] $c \in C$ to the [[representable presheaf]] which assigns to any other object $d$ of $C$ the [[hom-set]] of [[morphism]]s from $d$ into $c$:

$$
  Y(c) : C^{op} \stackrel{C(-,c)}{\to} Set
  \,.
$$

## Properties

It follows from the [[Yoneda lemma]] that the functor $Y$ is [[full and faithful functor|full and faithful]]. It is also [[limit]] preserving (= [[continuous functor]]), but does in general not preserve [[colimit]]s. 

The Yoneda embedding of a [[small category]] $S$ into the category of [[presheaf|presheaves]] on $S$ gives a [[free cocompletion]] of $S$.
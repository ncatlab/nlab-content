#Idea#

An _adjunction of two variables_ is a straightforward generalization of an internal hom in a [[closed category|biclosed]] [[monoidal category]] and of a $V$-enriched category which is [[tensored category|tensored]] and cotensored over $V$ by extracting the cdentral pattern.

#Definition#

Let $C$, $D$ and $E$ be [[category|categories]]. An **adjunction of two variables**

$$
 (\otimes, hom_l, hom_r) : C \times D \to E
$$

consists of functors

$$
\begin{aligned}
  \otimes & : C \times D \to E
  \\
  hom_l &: C^{op} \times E \to D
  \\
  hom_r &: D^{op} \times E \to C
\end{aligned}
$$

together with natural [[isomorphism]]s

$$
  Hom_E(C \otimes D, E)
  \simeq
  Hom_C(D, hom_l(C,E))
  \simeq
  Hom_D(C, hom_l(D,E))
  \,.
$$

#References#

This is in chapter 4 of

* Mark Hovey. Model Categories, volume 63 of Mathematical Surveys and Monographs. American Mathematical Society, 1999.
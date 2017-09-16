#Definition#

For $C$ any [[category]], its _arrow category_ is the [[functor category]]

$$
  Arr(C) := Funct(I,C)
$$

for $I = \{a \to b\}$ the [[category]] with two objects and with one single non-trivial morphism going between these objects (a combinatorial model for the interval, indeed, the directed [[interval object]] in [[Cat]]).  $Arr(C)$ is also written $[\mathbf{2},C]$ or $C^{\mathbf{2}}$, since $\mathbf{2}$ is a common [[notation]] for the category $I$ (it is the finite ordinal $2$ regarded as a category).

#Remarks#

* This means that the [[object]]s of $Arr(C)$ are the [[morphism]]s (the "arrows", therefore the name) of $C$, while the [[morphism]]s of $Arr(C)$ are commuting square [[diagram]]s in $C$. 

* $Arr(C)$ plays the role of a directed [[homotopy|path object]] for categories in that functors
$$
  X \to Arr(Y)
$$
are the same as [[natural transformation|natural transformations]] between functors between $X$ and $Y$.


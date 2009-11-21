#Definition#

For $C$ any [[category]], its **arrow category** is the [[functor category]]

$$
  Arr(C) := Funct(I,C)
$$

for $I$ the [[interval category]] $\{0 \to 1\}$.  $Arr(C)$ is also written $[\mathbf{2},C]$ or $C^{\mathbf{2}}$, since **[[2]]** is a common [[notation]] for the interval category.

#Remarks#

* This means that the [[objects]] of $Arr(C)$ are the [[morphisms]] (the "arrows", therefore the name) of $C$, while the [[morphisms]] of $Arr(C)$ are commuting square [[diagrams]] in $C$. 

* $Arr(C)$ plays the role of a directed [[homotopy|path object]] for categories in that functors
$$
  X \to Arr(Y)
$$
are the same as [[natural transformations]] between functors between $X$ and $Y$.

* $Arr(C)$ is the [[comma category]] $(id/id)$ where $id : C \to C$ is the identity functor.

A **simplicial homotopy** is a [[homotopy]] in the classical [[model structure on simplicial sets]].

#Definition#

[[SSet]] has a [[cylinder functor]] given by [[cartesian monoidal category|cartesian]] product with the standard 1-[[simplex]] $I := \Delta^1$. 

Therefore for $f,g : X \to Y$ two morphisms of [[simplicial set]]s, a [[homotopy]] $\eta : f \Rightarrow g$ is a morphism $\eta : X \times \Delta^1 \to Y$ such that the diagram

$$
  \array{
    X \simeq X\times \Delta^0 &\stackrel{Id \times \delta^1}{\to}& X \times \Delta^1 \simeq Y
   &
   \stackrel{Id \times \delta^0}{\leftarrow}&
   Y \times \Delta^0
   \\
   &
    {}_f\searrow &\downarrow^\eta& \swarrow_{g}
   \\
   &&
   Y
  }
$$

commutes.

#Remarks#

* Since in the standard [[model structure on simplicial sets]] every simplicial set is cofibrant, this indeed defines left homotopies.

#References#

* Goerss, Jardine, _Simplicial homotopy theory_ ([ps](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-1.dvi))
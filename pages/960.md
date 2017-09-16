The __smash product__ $A \wedge B$ of two [[pointed set]]s $A$ and $B$ is the [[quotient set]] of the [[cartesian produce]] $A \times B$ where all points with the basepoint as a coordinate (the one from $A$ or the one from $B$) are identified.

The subset that is 'smashed' here can be identified with the [[wedge sum]] $A \vee B$, so the definition of the smash product can be summarised as follows:
$$ A \wedge B = \frac{A \times B}{A \vee B} $$

The smash product [[tensor product]] in the [[closed monoidal category]] of pointed sets.  That is,
$$ Fun_*(A \wedge B, C) \cong Fun_*(A, Fun_*(B, C)) $$
Here, $Fun_*(A,B)$ is the set of basepoint-preserving [[function]]s from $A$ to $B$, itself made into a pointed set by taking as basepoint the [[constant function]] from all of $A$ to the basepoint in $B$.
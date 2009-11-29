The __smash product__ $A \wedge B$ of two [[pointed set]]s $A$ and $B$ is the [[quotient set]] of the [[cartesian product]] $A \times B$ where all points with the basepoint as a coordinate (the one from $A$ or the one from $B$) are identified.

The subset that is 'smashed' here can be identified with the [[wedge sum]] $A \vee B$, so the definition of the smash product can be summarised as follows:
$$ A \wedge B = \frac{A \times B}{A \vee B} $$

This easily generalizes to the smash products of many spaces, but they do not necessarily agree with iterated version: it is not necessarily $A\wedge B\wegde C \cong (A\wedge B)\wedge C$. 

The smash product is the [[tensor product]] in the [[closed monoidal category]] of pointed sets.  That is,
$$ Fun_*(A \wedge B, C) \cong Fun_*(A, Fun_*(B, C)) $$
Here, $Fun_*(A,B)$ is the set of basepoint-preserving [[function]]s from $A$ to $B$, itself made into a pointed set by taking as basepoint the [[constant function]] from all of $A$ to the basepoint in $B$.

Smash products can be defined for [[pointed object]]s in any category $C$ with finite limits and colimits.  The most common case when $C$ is a category of [[topological space]]s.  In that case, the natural map $A\wedge B\wedge C\to (A\wedge B)\wedge C$ is a homeomorphism provided $C$ is locally compact Hausdorff space. Thus if both $A$ and $C$ are locally compact Hausdorff, then we have the associativity $A\wedge(B\wedge C)\cong (A\wedge B)\wedge C$. For pointed compactly generated Hausdorff spaces, the smash product is associative. 


If finite products in $C$ preserve finite colimits, then the smash product is associative, and if $C$ is also [[cartesian closed category|cartesian closed]], then it makes the category of pointed objects in $C$ closed monoidal.  However, if finite products in $C$ do not preserve finite colimits, the smash product can fail to be associative; this is already the case in the category [[Top]] of all topological spaces (although, of course, not in any [[convenient category of topological spaces]], since these are cartesian closed).

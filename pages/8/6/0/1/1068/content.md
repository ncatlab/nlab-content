#Definition#

A **category with translation** is a [[category]] $C$ equipped with an [[equivalence|auto-equivalence]] 
$$
  T : C \to C
  \,.
$$
A **functor of categories with translation** $F:(C,T)\to (C',T')$ is a functor $F:C\to C'$ equipped with an isomorphism $F\circ T\cong T'\circ F$. If $C$,$C'$ are additive and $F$ is additive $F$ is a "functor of additive categories with translation". 

In any additive category with translation a **triangle** is a sequence of morphisms of the form
$$a\stackrel{f}\to b\stackrel{g}\to c\stackrel{h}\to Ta.$$


#Examples#

* The "translation" functor models the shift operation in a [[triangulated category]], where one chooses a distinguished collection of triangles satisfying some axioms. Sometimes instead of translation one requires an endofunctor which is not invertible, what enters a definition of a weakened version of triangulated category, so-called [[presuspended category]] of Keller and Vossieck. 
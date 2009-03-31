#Definition#

A **category with translation** is a [[category]] $C$ equipped with an [[equivalence|auto-equivalence]] 
$$
  T : C \to C
  \,.
$$
Frequently $C$ is an [[additive category]] in which case $F$ is also required to be an _additive_ functor.

A **morphism of categories with translation** $F:(C,T)\to (C',T')$ is a [[functor]] $F:C\to C'$ equipped with an [[isomorphism]] $F\circ T\cong T'\circ F$:

$$
  \array{
    C &\stackrel{F}{\to}& C'
    \\
    \downarrow^T &\Downarrow^{\simeq}& \downarrow^{T'}
    \\
    C &\stackrel{F}{\to}& C'
  }
  \,.
$$

 If $C$,$C'$ are [[additive category|additive]] and $F$ is additive $F$ is a "morphism of additive categories with translation". 

In any additive category with translation a **triangle** is a sequence of morphisms of the form
$$a\stackrel{f}\to b\stackrel{g}\to c\stackrel{h}\to T a.$$

#Remarks#

* In some variants the translation endofunctor $T$ is not required to be an [[equivalence]]. This is the case for instance for the 
[[presuspended category|presuspended categories]] of Keller and Vossieck. 

#Examples#

* The "translation" functor models the shift operation in a [[triangulated category]], where one chooses a distinguished collection of triangles satisfying some axioms. 
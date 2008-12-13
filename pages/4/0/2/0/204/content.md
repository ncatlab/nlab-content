A [[functor]] $F: C \to D$ from the category $C$ to the category $D$ is _full_ if for each pair of objects $x, y \in C$, the function

$$F : hom(x,y) \to hom(F(x), F(y))$$

is onto.  

More abstractly, we may say a functor is full if it is [[k-surjectivity|1-surjective]] - or heuristically speaking, 'surjective on morphisms'.  (Note that a functor may be full without literally being surjective on morphisms, since $F$ is allowed to not hit morphisms between objects that are not in the image of $F$.)
A [[functor]] $F: C \to D$ from the category $C$ to the category $D$ is _full_ if for each pair of objects $x, y \in C$, the function

$$F : hom(x,y) \to hom(F(x), F(y))$$

is onto.  

More abstractly, we may say a functor is full if it is [[k-surjectivity|1-surjective]] &#8211; or heuristically speaking, 'surjective on morphisms between given objects'.  (Note that a functor may be full without being surjective on morphisms,overall, since $F$ is allowed to not hit morphisms between objects that are not in the image of $F$.)

Fullness is most important for functors which are also [[faithful functor|faithful]].  Full and faithful functors are often called _fully faithful_, although there is no real sense in which "full" modifies "faithful."  A [[subcategory]] is called a **full subcategory** if its inclusion functor (which is automatically faithful) is also full, and any full and faithful functor exhibits an equivalence of its domain with a full subcategory of its codomain.  The phrase "full and faithful" is also sometimes abbreviated to "ff"; see [[bo-ff factorization system]].

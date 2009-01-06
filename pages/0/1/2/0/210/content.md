A [[functor]] $F: C \to D$ from the category $C$ to the category $D$ is _full_ if for each pair of objects $x, y \in C$, the function

$$F : hom(x,y) \to hom(F(x), F(y))$$

is onto.  

More abstractly, we may say a functor is full if it is [[k-surjectivity|1-surjective]] &#8211; or heuristically speaking, 'surjective on morphisms between given objects'.  (Note that a functor may be full without being surjective on morphisms,overall, since $F$ is allowed to not hit morphisms between objects that are not in the image of $F$.)

Fullness is most important for functors which are also [[faithful functor|faithful]].  As a relic of this, full and faithful functors are often called _fully faithful_, although there is no real sense in which "full" modifies "faithful."  A [[subcategory]] is called a **full subcategory** if its inclusion functor (which is automatically faithful) is also full, and any full and faithful functor exhibits an equivalence of its domain with a full subcategory of its codomain.  The phrase "full and faithful" is also sometimes abbreviated to "ff"; see [[bo-ff factorization system]].

### Discussion ###

_Mathieu says:_ I agree that, for functors, there is no reason to say "fully faithful" rather than "full and faithful".  But for arrows in a 2-category (like in the new version of the entry on [[subcategory|subcategories]]), there are reasons.  I quote myself (from my thesis): &#171;Remark: we say _fully faithful_ and not _full and faithful_, because the condition that, for all $X:\C$, $C(X,f)$ be full is not equivalent in $\mathrm{Gpd}$ to $f$ being full. Moreover, in $\mathrm{Gpd}$, this condition implies faithfulness.  We will define (Definition 197) a notion of full arrow in a $\mathrm{Gpd}$-category which, in $\mathrm{Gpd}$ and $2-\mathrm{GpS}$ (symmetric 2-groups), gives back the ordinary full functors.&#187;  Note that this works only for some good groupoid enriched categories, not for $\mathrm{Cat}$, for example.
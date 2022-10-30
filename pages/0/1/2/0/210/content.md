A [[functor]] $F: C \to D$ from the category $C$ to the category $D$ is _full_ if for each pair of objects $x, y \in C$, the function

$$F : hom(x,y) \to hom(F(x), F(y))$$

is onto.  

More abstractly, we may say a functor is full if it is $1$-[[k-surjective functor|surjective]] -- or, in simple terms, 'surjective on morphisms between given objects'.  (Note that a functor may be full without being surjective on morphisms,overall, since $F$ is allowed to not hit morphisms between objects that are not in the image of $F$.)

Fullness is most important for functors which are also [[faithful functor|faithful]], and full and faithful functors are often called _fully faithful_.  For ordinary functors this may sound odd, because there is no real sense in which "full" modifies "faithful."  However, in some contexts (such as for morphisms in a general [[2-category]]), there is a good notion of "full-and-faithful" or "fully faithful," but the right notion of "full" alone is not so clear.  "Fully faithful" is also sometimes abbreviated to "ff"; see also [[bo-ff factorization system]].

A [[subcategory]] is called a _[[full subcategory]]_ if its inclusion functor (which is automatically faithful) is also full, and any full and faithful functor exhibits an equivalence of its domain with a full subcategory of its codomain.


### Discussion ###

_Mathieu says:_ I agree that, for functors, there is no reason to say "fully faithful" rather than "full and faithful".  But for arrows in a 2-category (like in the new version of the entry on [[subcategory|subcategories]]), there are reasons.  I quote myself (from my thesis): &#171;Remark: we say _fully faithful_ and not _full and faithful_, because the condition that, for all $X:\C$, $C(X,f)$ be full is not equivalent in $\Grpd$ to $f$ being full. Moreover, in $\Grpd$, this condition implies faithfulness.  We will define (Definition 197) a notion of full arrow in a $\Grpd$-category which, in $\Grpd$ and $\Symm2\Grp$ (symmetric 2-groups), gives back the ordinary full functors.&#187;  Note that this works only for some good groupoid enriched categories, not for $\Cat$, for example.

_Mike_ says: Do you have a reason to care about full functors which are not also faithful?  I've never seen a very compelling one.  (Maybe I should just read your thesis...)  I agree that "full morphism" (in the representable sense) is not really a useful/correct concept in a general 2-category, and that therefore "full and faithful" is not entirely appropriate, so I usually use "ff" in that context.  I've changed the entry above a bit to reflect your comment; is it satisfactory now?  Maybe all this should actually go at [[full and faithful functor]] (and/or [[fully faithful functor]])?

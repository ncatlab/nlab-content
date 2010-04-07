<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>

## Idea

A **pseudofunctor** is a specific algebraic notion of _weak $2$-[[2-functor|functor]]_ between [[bicategory|bicategories]] (including [[strict 2-category|strict 2-categories]]), i.e. a functor which preserves composition and identities only up to coherent specified isomorphism.

+--{: .query}
[[Tim]]: in specifying a pseudo functor $F$ you have to decide whether the isomorphism goes from $F(g f)$ to $F(g) F(f)$ or in the other direction. Of course they are equivalent as each will be inverse to the other. You might say that one is lax and pseudo the other op-lax and pseudo. When specifying the Grothendieck construction for such a functor, which is to be preferred? 

Both are about equally represented in the literature that I have seen which gets confusing. (In other words, I'm confused!)

_Toby_:  As you suggest, the two versions are equivalent, so in a way it doesn\'t make a difference.  But it might be nice to settle a convention in case we need it.


[[Tim]]: I have been using (for the Menagerie) the idea that there are pseudofunctors presented in two equivalent flavours lax pseudofunctor and oplax ones. 

[[Mike Shulman|Mike]]: Well, the natural comparison maps that you get in a [[Grothendieck fibration]] go in the "lax" direction $F(g) F(f) \to F(g f)$, since they are induced by the universal property of cartesian arrows.  In particular, if you have a functor with "weakly cartesian" liftings that don't compose, then it is a lax functor.  Not a very strong argument, but if we just want _some_ convention it might be a reason to pick lax.  I think that making too big a deal out of the difference would be misleading, though.
=--


In general, there is not much reason to say "pseudofunctor" instead of "functor," since the only relevant type of functor between arbitrary bicategories is weak.  However, if the domain and codomain are known to be [[strict 2-category|strict 2-categories]] (including ordinary $1$-[[1-category|categories]]), it can be helpful to say "pseudofunctor" or "weak functor" to emphasize that it is not a [[strict 2-functor]].  Note that if the codomain is a $1$-category, then there is no difference.

Pseudo or weak functors are also to be distinguished from [[lax functor]]s and [[lax functor|oplax functor]]s, which preserve identities and composition only up to a  transformation in one direction or the other, which may be non-invertible.

An older terminology, which should probably be avoided at all costs, uses "homomorphism of bicategories" for a weak functor and "morphism of bicategories" for a lax one.


## Definition

... put a precise definition here; pick a convention ...




[[!redirects pseudo functor]]
[[!redirects pseudo-functor]]
[[!redirects pseudofunctors]]
[[!redirects pseudo functors]]
[[!redirects pseudo-functors]]
A **pseudofunctor** is a specific algebraic notion of _weak functor_ between [[bicategory|bicategories]] (or [[strict 2-category|strict 2-categories]]), i.e. a functor which preserves composition and identities only up to coherent specified isomorphism.
+--{: .query}
[[Tim]]: in specifying a pseudo functor $F$ you have to decide whether the isomorphism goes from $F(gf)$ to $F(g)F(f)$ or in the other direction. Of course they are equivalent as each will be inverse to the other. You might say that one is lax and pseudo the other op-lax and pseudo. When specifying the Grothendieck construction for such a functor, which is to be preferred? 

Both are about equally represented in the literature that I have seen which gets confusing. (In other words, I'm confused!)
=--


When the domain and codomain are known to be bicategories, there is not much reason to say "pseudofunctor" instead of "functor," since in most situations the only relevant type of functor between bicategories is weak.  
+--{: .query}
[[Tim]]: This wording is inconsistent with general principles elsewhere in the Lab I think. Any 1-category or strict 2-category _is_ a bicategory by default. I cannot think of a wording that gets around that without destroying the good sense that the paragraph talks about.   
=--
However, if the domain and codomain are [[strict 2-category|strict 2-categories]] (including the case of ordinary 1-categories equipped with only identity 2-cells), it can be helpful to say "pseudofunctor" or "weak functor" to emphasize that the functor is not strict.

Pseudo or weak functors are also to be distinguished from [[lax functor|lax]] and oplax functors, which preserve identities and composition only up to a  transformation in one direction or the other, which may be non-invertible.

An older terminology, which should probably be avoided at all costs, uses "homomorphism of bicategories" for a weak functor and "morphism of bicategories" for a lax one.


[[!redirects pseudo functor]]
[[!redirects pseudo-functor]]
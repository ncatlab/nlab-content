#Idea#

A _weak equivalence_ is a [[morphism]] in a [[category]] $C$ which is supposed to be a true [[equivalence]] in a [[higher category theory|higher categorical]] refinement of $C$.

For example, a weak equivalence between categories themselves is a functor that is [[full and faithful functor|fully faithful]] and [[essentially surjective functor|essentially surjective]]; this is the proper notion to use even in the absence of the [[axiom of choice]] (but see [[equivalence]] for how to get around that).

The bare minimum of axioms to be satisfied by a weak equivalence are encoded in the concepts of [[category with weak equivalences]] and [[homotopical category]].  For such categories one can consider 

* the corresponding [[homotopy category]], which is the universal solution to turning all weak equivalences into [[isomorphism]]s;

* the corresponding $(\infty,1)$-[[(infinity,1)-category|category]], which is, roughly, the universal solution to turning all weak equivalences into higher categorical [[equivalence]]s.  There are various versions of this construction depending on what model for $(\infty,1)$-categories is chosen.

  * The [[Dwyer-Kan localization]] uses [[simplicially enriched   category|simplicially enriched categories]] to model $(\infty,1)$-categories.

  * If we use [[complete Segal space]]s or [[quasi-category|quasicategories]] to model $(\infty,1)$-categories, then the construction is a version of _fibrant replacement_.

Often, categories having weak equivalences also have extra structure that makes them easier to work with.  A very powerful, and commonly occurring, level of such structure is called a [[model category|model structure]].  There are also various weaker levels of structure, such as a [[category of fibrant objects]].

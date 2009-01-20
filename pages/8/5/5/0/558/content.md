The _homotopy hypothesis_ states that $n$-groupoids model homotopy $n$-types. As a slogan:

* $\infty$-groupoids are combinatorial models for spaces.

To some extent the homotopy hypothesis is not a hypothesis but a _requirement_ on the definition of [[infinity-groupoid]]: for every "good" definition of $\infty$-groupoid there should be an "obvious" morphism from the collection of all $\infty$-groupoids to (well behaved) topological spaces, and this map should be an equivalence in a "suitable" sense.

The homotopy hypothesis is known to be true for some definitions of "$\infty$-groupoid".  For example, there is a good case to be made that a [[Kan complex]] is a notion of $\infty$-groupoid, and it's been known for a long time in [[homotopy theory]] that Kan complexes model spaces, homotopically speaking.  However, for other notions of [[higher category theory|higher category]], it remains a hypothesis/requirement.

+--{.query}

[[Tim Porter|Tim]]: I would like to pose a question on the Homotopy Hypothesis.  Playing devil's advocate for the moment, since Kan complexes, and simplicially enriched categories, both satisfy the homotopy hypothesis, why bother to search for other models?  That is a bit severe of course so a more 'constructive' form of the question is what criteria should we be looking to be satisfied so as to say that a model of homotopy types is a good one?  (Perhaps things like that the basic homotopy operations, such as Whitehead or Samelson products, should have clear formulations and clear interpretations.  The higher operations could then be gradually required.  The relation between obstructions to interchange laws (interchangeator!) and the low dimensional Whitehead products are 'clear' even if not that immediately evident in most writing on the subject (and I include my own in that!), but in higher dimensions .... ?

_[[Mike Shulman|Mike]]_: My perspective is that we are looking for good notions of _$\infty$-category_ such that the _induced_ notion of $\infty$-groupoid satisfies the homotopy hypothesis.  If all you want is to do homotopy theory, then homotopy theorists have gotten along quite well for decades with topological spaces, Kan complexes, and the like (although one might certainly hope, as you suggest, to get information about homotopy operations out as well).  But as category theorists, we want a notion of $\infty$-category with not all cells necessarily invertible, which behaves well _categorically_ rather than homotopically, but whose induced notion of $\infty$-groupoid still satisfies the homotopy hypothesis as a "check" or "anchor."  It's hard to exhibit Kan complexes as the $(\infty,0)$-case of a notion of $\infty$-category; there are [[quasicategory|quasicategories]] for $(\infty,1)$-categories but beyond that it gets tricky (there is Street's original definition, but it's quite difficult to work with).

[[Urs Schreiber|Urs]]: Lurie is now talking in (electronic) print about $(\infty,n)$-categories, [here](http://www-math.mit.edu/~lurie/papers/cobordism.pdf).

_Mike_: When I glanced at that, it looked as though he was actually using [[Segal category|Segal categories]] for his $(\infty,n)$-categories rather than some generalization of quasicategories.

=--

#Remarks#

* In analogy to the homotopy hypothesis, there are attempts to relate general [[infinity-category|infinity-categories]] which need not be groupoidal to [[directed space]]s, in which a morphism which is not invertible would model a path in the space that can only be traversed in one direction.

 
#References#

* John Baez, _The Homotopy Hypothesis_ ([web](http://math.ucr.edu/home/baez/homotopy/), [pdf](http://math.ucr.edu/home/baez/homotopy/homotopy.pdf))

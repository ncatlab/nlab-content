The idea here is to create an enormous list of well-known categories and their properties.  As the list gets large we'll have to figure out a good structure for it, but right now I'll just do a few entries in alphabetical order.  [[Andrew Stacey]] solicits input about making this a real database; see [the Forum](https://nforum.ncatlab.org/discussion/57/).

We can import new entries by looking at [category:category](http://ncatlab.org/nlab/list/category), which should have all articles dedicated to specific categories.

* [[Ab]]: [[abelian group|abelian groups]] as objects, homomorphisms as morphisms.  Since this category consists of models of a [[Lawvere theory]] it has all small [[limit|limits]] and [[colimit|colimits]].  It is the prototypical [[abelian category]] and also a [[closed symmetric monoidal category]] under the [[tensor product]] of abelian groups.

* [[Alg]]: [[algebra|algebras]] as objects, homomorphisms as morphisms.  This is actually many different categories, depending on a choice of ground [[field]] or more generally [[commutative ring]].  Since any one of these categories consists of models of a [[Lawvere theory]], it has all small [[limit|limits]] and [[colimit|colimits]].

* [[Bicat]]: [[bicategories]]($=$weak 2-categories) as objects, [[2-functors]] as its 1-cells, [[pseudonatural transformations]] between its 1-cells as its 2-cells, and [[modifications]] between its 2-cells as its 3-cells. BiCat is a [[tricategory]]. BiCat is sometimes denoted $Hom$.

* [[CartSp]]: spaces $\mathbb{R}^n$ as objects, smooth maps as morphisms.

* [[Cat]]: [[small category|small categories]] as objects, [[functor|functors]] as morphisms.  Since this category consists of models of a [[finite limits theory]], it has all small [[limit|limits]] and [[colimit|colimits]].  It is [[cartesian closed category|cartesian closed]], and its [[internal hom]]s make it into a [[2-category]].

* [[Diff]]: smooth [[manifold]]s as objects, smooth maps as morphisms.  This category has finite but not infinite [[products]], and all small [[coproducts]].  It does not have equalizers or coequalizers, and is not [[cartesian closed category|cartesian closed]].

* [[diffeological space|Diffeological spaces]] as objects, smooth maps as morphisms.  This category has all small limits and colimits, it is [[cartesian closed category|cartesian closed]], and it has a weak [[subobject classifier]].  So, it is a [[quasitopos]].

* [[Grp]]: [[group]]s as objects, homomorphisms as morphisms.  Since this category consists of models of a [[Lawvere theory]] it has all small [[limit|limits]] and [[colimit|colimits]].

* $Mod_R$: (right) $R$-[[modules]] as objects, $R$-module homomorphisms as morphisms.  There is one such category for any [[ring]] $R$ (or more generally, any small [[Ab-enriched category]].  This is also the category of models of a [[Lawvere theory]] and is thus complete and cocomplete.  It is an [[abelian category]] and even [[Grothendieck category]].  If $R$ is commutative, then $Mod_R$ is a [[closed symmetric monoidal category]] under the [[tensor product]] of $R$-modules.

* [[M-Set]]: Category of $M$-sets, a [[topos]].

* [[MultiSet]]: Category of [[multisets]].

* [[Rel]]: [[sets]] as objects, [[relation|relations]] as morphisms.  This is an [[allegory]] and therefore a [[dagger category]].   The empty set is an [[zero object]], and disjoint union plays the role of [[biproduct]].   This category does not have [[equalizer|equalizers]] or [[coequalizer|coequalizers]].

* [[Ring]]: [[ring|rings]] as objects, ring homomorphisms as morphisms.  Since this category consists of models of a [[Lawvere theory]] it has all small [[limit|limits]] and [[colimit|colimits]]. (maybe we should have unital rings $Ring_1$ separately; the difference is important sometimes). 

* [[SimpSet]]: [[simplicial sets]] as objects, simplicial maps as morphisms.  This is a [[presheaf]] [[topos]].

* [[Set]]: [[sets]] as objects, [[functions]] as morphisms.
This has the following properties:

  * It is a [[topos]], and in particular it is [[locally cartesian closed category|locally cartesian closed]].
  * It is [[locally small category|locally small]].
  * It is [[complete category|complete]] and [[cocomplete category|cocomplete]], and therefore $\infty$-[[extensive category|extensive]] (as is any cocomplete topos).
  * It is [[well-pointed topos|well-pointed]].

  At least assuming [[classical logic]], these properties suffice to characterize $Set$ uniquely up to equivalence among all categories.  Note, however, that the definitions of "locally small" and "(co)complete" presuppose a notion of _small_ and therefore a knowledge of what a _set_ is.

  See also [[Understanding Set]].

* [[Top]]: [[topological space]]s as objects, continuous functions as morphisms.   This has all small limits and colimits, but is not cartesian closed --- a problem that may be addressed by introducing a [[convenient category of topological spaces]].

* $k$-[[Vect]]: [[vector space]]s as objects, linear maps as morphisms.  This is actually many different categories, depending on a choice of [[field]] $k$; in fact, it is a special case of $Mod_R$ when $R$ is a field.  Since any one of these categories consists of models of a [[Lawvere theory]], it has all small [[limit|limits]] and [[colimit|colimits]].

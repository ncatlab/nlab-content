The idea here is to create an enormous list of well-known categories and their properties.  As the list gets large we'll have to figure out a good structure for it, but right now I'll just do a few entries in alphabetical order. 

We can import new entries by looking at [category:category](http://ncatlab.org/nlab/list/category), which should have all articles dedicated to specific categories.

* [[Ab]] - [[abelian group|abelian groups]] as objects, homomorphisms as morphisms.  Since this category consists of models of a [[Lawvere theory]] it has all small [[limit|limits]] and [[colimit|colimits]].

* [[Alg]] - [[algebra|algebras]] as objects, homomorphisms as morphisms.  This is actually many different categories, depending on a choice of ground [[field]] or more generally [[commutative ring]].  Since any one of these categories consists of models of a [[Lawvere theory]], it has all small [[limit|limits]] and [[colimit|colimits]].

* [[CartSp]] - spaces $\mathbb{R}^n$ as objects, smooth maps as morphisms.

* [[Cat]] - [[small category|small categories]] as objects, [[functor|functors]] as morphisms.  Since this category consists of models of a [[finite limits theory]], it has all small [[limit|limits]] and [[colimit|colimits]].

* [[Diff]] - smooth [[manifold]]s as objects, smooth maps as morphisms.  This category has finite but not infinite [[products]], and all small [[coproducts]].  It does not have equalizers or coequalizers, and is not [[cartesian closed category|cartesian closed]].

* [[diffeological space|Diffeological spaces]] as objects, smooth maps as morphisms.  This category has all small limits and colimits, it is [[cartesian closed category|cartesian closed]], and it has a weak [[subobject classifier]].  So, it is a [[quasitopos]].

* [[Grp]] - [[group]]s as objects, homomorphisms as morphisms.  Since this category consists of models of a [[Lawvere theory]] it has all small [[limit|limits]] and [[colimit|colimits]].

* [[Rel]] - [[sets]] as objects, [[relation|relations]] as morphisms.  This is an [[allegory]].

* [[Ring]] - [[ring|rings]] as objects, ring homomorphisms as morphisms.  Since this category consists of models of a [[Lawvere theory]] it has all small [[limit|limits]] and [[colimit|colimits]].

* [[Set]] - [[sets]] as objects, [[functions]] as morphisms.
This has the following properties:

  * It is a [[topos]], and in particular it is [[locally cartesian closed category|locally cartesian closed]].
  * It is [[locally small category|locally small]].
  * It is [[complete category|complete]] and [[cocomplete category|cocomplete]], and therefore $\infty$-[[extensive category|extensive]] (as is any cocomplete topos).
   * It is [[well-pointed topos|well-pointed]].

    At least assuming [[classical logic]], these properties suffice to characterize $Set$ uniquely up to equivalence among all categories.  Note, however, that the definitions of "locally small" and "(co)complete" presuppose a notion of _small_ and therefore a knowledge of what a _set_ is.

* [[Top]] - [[topological space]]s as objects, continuous functions as morphisms.   This has all small limits and colimits, but is not cartesian closed --- a problem that was addressed by introducing a 'convenient category' of topological spaces, such as $k$-spaces.

* [[Vect]] - [[vector space]]s as objects, linear maps as morphisms.  This is actually many different categories, depending on a choice of [[field]].  Since any one of these categories consists of models of a [[Lawvere theory]], it has all small [[limit|limits]] and [[colimit|colimits]].

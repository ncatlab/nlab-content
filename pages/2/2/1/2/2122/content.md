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

+-- {: .query}
Rafael Borowiecki: I could add something of the order 100 categories here, but i know very little of their properties. Should i add them anyway?

It would also be helpful to have a list of properties to fill in for each category to make it a real database. As a start i suggest: size, concrete, complete, enrichment, topos. This list could also get very large resulting in an even larger table (written as a list). For instance one could also add cartesian closedness, monoidality, model structure.

I don't know where to put this request but the logging of changes should be automated. Simply add a smaller box one might fill in if one wishes below the editing box and hope that not every edit will also edit this changes box. It could be limited to size.

_Toby_:  I also could add hundreds of categories.  At this stage, I\'m inclined to add only categories that we have pages for.  On the other hand, often people only create pages because there are links to them, so perhaps people should also add categories that they think are important and conspicuously missing?  As long as the page isn\'t flooded with a huge list, it will be manageable.  And maybe we could even manage a huge list?  I\'d like to hear what [[John Baez|John]] thinks.  (Sorry to be so indecisive!)

Automatic logging is not an option with Instiki, which is why we use [[latest changes]] instead.  You could request that it be added as a feature to [Instiki](http://www.instiki.org/show/HowToContribute), but (unless you can program it) don\'t hold your breath.  *However*, not that there is a page [Recently Revised](http://ncatlab.org/nlab/recently_revised); it\'s disabled now, but that should be temporary.  (Try [this one](http://ncatlab.org/tobybartels/recently_revised) to see how it\'s supposed to work.)  When it comes back, it will take care of much of the need for automatic logging, requiring people only to report major changes that others need to know about.
=--
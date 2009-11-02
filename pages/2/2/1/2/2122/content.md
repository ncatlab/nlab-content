The idea here is to create an enormous list of well-known categories and their properties.  As the list gets large we'll have to figure out a good structure for it, but right now I'll just do a few entries in alphabetical order.  [[Andrew Stacey]] solicits input about making this a real database; see [the Forum](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=57).

We can import new entries by looking at [category:category](http://ncatlab.org/nlab/list/category), which should have all articles dedicated to specific categories.

* [[Ab]]: [[abelian group|abelian groups]] as objects, homomorphisms as morphisms.  Since this category consists of models of a [[Lawvere theory]] it has all small [[limit|limits]] and [[colimit|colimits]].  It is the prototypical [[abelian category]] and also a [[closed symmetric monoidal category]] under the [[tensor product]] of abelian groups.

* [[Alg]]: [[algebra|algebras]] as objects, homomorphisms as morphisms.  This is actually many different categories, depending on a choice of ground [[field]] or more generally [[commutative ring]].  Since any one of these categories consists of models of a [[Lawvere theory]], it has all small [[limit|limits]] and [[colimit|colimits]].

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

+-- {: .query}
Rafael Borowiecki: I could add something of the order 100 categories here, but i know very little of their properties. Should i add them anyway?

It would also be helpful to have a list of properties to fill in for each category to make it a real database. As a start i suggest: size, concrete, complete, enrichment, topos. This list could also get very large resulting in an even larger table (written as a list). For instance one could also add functoriality (is it a category of functors?, notice that the Yoneda lemma do not hold for any category), cartesian closedness, monoidality, model structure.

I don't know where to put this request but the logging of changes should be automated. Simply add a smaller box one might fill in if one wishes below the editing box and hope that not every edit will also edit this changes box. It could be limited to size.

_Toby_:  I also could add hundreds of categories.  At this stage, I\'m inclined to add only categories that we have pages for.  On the other hand, often people only create pages because there are links to them, so perhaps people should also add categories that they think are important and conspicuously missing?  As long as the page isn\'t flooded with a huge list, it will be manageable.  And maybe we could even manage a huge list?  I\'d like to hear what [[John Baez|John]] thinks.  (Sorry to be so indecisive!)

Automatic logging is not an option with Instiki, which is why we use [[latest changes]] instead.  You could request that it be added as a feature to [Instiki](http://www.instiki.org/show/HowToContribute), but (unless you can program it) don\'t hold your breath.  *However*, note that there is a page [Recently Revised](http://ncatlab.org/nlab/recently_revised); it\'s disabled now, but that should be temporary.  (Try [this one](http://ncatlab.org/tobybartels/recently_revised) to see how it\'s supposed to work.)  When it comes back, it will take care of much of the need for automatic logging, requiring people only to report major changes that others need to know about.

_Rafael_: I was wondering what happened to Recently Revised. Now i know it is not improved to Latest changes and will be back. Thx for the information.

_[[John Baez]]_: I don't see any use of listing categories here unless one includes information about their basic categorical properties: for starters, which sorts of limits and/or colimits they have:

* binary products
* binary coproducts
* terminal object
* initial object
* pullbacks
* pushouts
* equalizers
* coequalizers
* finite limits
* finite colimits
* small limits
* small colimits

whether they admit interesting monoidal structures, whether they are cartesian (or monoidal) closed, and whether they are topoi, quasitopoi or allegories.  In short: the basic properties one instantly wants to know about any category one meets.

My idea is that this article should be a quick place to look up basic categorical properties of categories, including categories that may not have their own entry yet.   The entries here should not become full-fledged articles on the categories involved, since we already have or can create those.
 
By the way: people have been talking to Rafael on [Recently Revised](http://ncatlab.org/nlab/recently_revised) for many weeks now, but he doesn't seem to reply to their comments there, which is making some people annoyed.

_Toby_:  I can see that a list of categories *with properties* could be useful.

John, you don\'t mean Recently Revised; you mean [[latest changes]].  (Your link will break when Recently Revised itself comes back.)

Rafael, I don\'t know if you\'ve been checking [[latest changes]], but I often log your edits there after I see them.  But I don\'t see why anyone would get upset that you don\'t read their commentary if they leave it on the wrong page.

_Rafael_: I am sorry to have missed the logging but i only recently by accident noticed that you also log at Latest Changes. I thought that all changes were in Recently Revised. Since Toby is logging for me, thanks Toby, i will try to remember to do it myself so others don't have to do it for me.

_John_: Sorry, I meant [[latest changes]].  It's a good way to discuss what's going on with various new entries.

_Andrew_: Actually, it's a very bad way to _discuss_ what's going on, but an okay way to _announce_ what's going on.  But that's another battle for another day.  What I'm really here for is to ponder the format of this page a little.  At the moment, we can't do a proper database-based page of all this stuff so we have to think of the next best thing.  Is the current format most useful?  Or would a table with loads of 'X's be more appropriate?  The categories would, of course, be linked to their pages where one could find out more.  For example, here we would merely record that, say, Rel didn't have all limits and colimits.  On the actual page there would be an example showing why not.  One would need a few "codes" for the entries along the lines of "Yes", "No", "Don't Know", "Sort of Yes", "Sort of No".  That sort of thing.  One could then search by name using the browser search.  What you wouldn't get, that you would get from a database, would be the ability to, say, only show complete categories.  But how likely is that to be a request?  I'd expect the main use to be "I don't remember if Frolicher spaces are locally cartesian closed or not.".  I would think that a table format would be more useful than this list format, but I may be in a minority here (I usually am) and I'd rather not go to the effort of putting it in that format only to find no-one else likes it.

[[Zoran Škoda]]: I agree with John that the main purpose is to list many properties of well known categories, rather than listijng definitions of exotic categories. Those categories which already have their page on the nlab could be expanded on those pages rather than here. For some not only existence of limits but also a construction of limits can be useful. 

_Toby_:  I agree with Andrew about everything from 'Actually,' to 'it.'.  However, making a table with specific columns can be somewhat limiting, so we would need to make clear up top that adding new columns is fine.  Blank entries in the table should default to &#8249;Nobody has bothered to put the answer here yet.&#8250;, which should be distinguished from &#8249;This is an unsolved problem.&#8250;.  Other useful entries besides 'Yes' or 'No' might be 'if and only if $R$ is [[noetherian ring|noetherian]]', 'equivalent to the [[ultrafilter principle]]', and the like.  Some standard abbreviations might be useful here; tables can be hard to deal with when they get too wide.
=--

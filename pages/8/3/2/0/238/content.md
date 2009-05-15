[[!include all changes]]

A list of all recently edited entries can be seen here:

* [Recently Revised](http://ncatlab.org/nlab/recently_revised).

But that list tends to contain lots of minor changes: it's not easy to spot the important ones.

So, if you feel people's attention should be drawn to some changes you make, please mention them *here*.  That will help [[Contributors|the rest of us]] spot them, so we can learn what you know --- and maybe make further improvements!

These comments should go in _reverse_ chronological order, so that the latest are on top of the list. To keep the list international, use the date in UTC (the date given by the server for your edits).

***

# 2009-05-15 #

* [[David Corfield|David]]:

  * began [[synthetic differential geometry]] and [[analytic versus synthetic]]

* [[Urs Schreiber|Urs]]:

  * further refined the discussion of the relation to localization at [[geometric embedding]]

# 2009-05-14 #

* [[Urs Schreiber|Urs]]:

  * added some bits to [[subobject classifier]]: a short intro, the realization in presheaf topoi and a paragraph on $n$-catgorical generalizations and the interpretation of $true$ as a $-1$-category.

  * created [[power object]], which is mentioned in the alternative definition at [[topos]] --  guessed the definition from the _Axiom of power sets_ at [[Trimble on ETCS I]], but I am not really sure -- somebody please have a look and check

  * expanded and restructured [[Grothendieck topos]]

  * added what should be a detailed proof to [[geometric embedding]] that for every geometric embedding $f_* : F \hookrightarrow E$ the category $F$ is equivalent to the localization of $E$ at the morphisms that are sent by $f^*$ to isos 

    * there are two possibilities here: either I am mixed up or this is somewhere in the literature. If the latter, can anyone give me a pointer to a reference that mentions this explicitly?

  * created [[geometric embedding]] -- am in the process of filling in a detailed discussion of the relation to [[localization]]

  * added a paragraph to [[localization]] describing and emphasizing the point that lots of localizations one runs into in practice are [[reflective subcategory|reflective subcategories]] or actually [[geometric embedding|geometric embeddings]]. In particular [[Bousfield localization]] presents the corresponding [[reflective (infinity,1)-subcategory]]. I am still not really satisfied with the entry [[localization]], though, I am hoping we can eventually present the conceptual basis here more clearly. After all, the perspective on sheaves and sheafification in terms of localization/geometric embedding has been shown to be the workable road to $\infty$-stacks, which, as tradition has it, are well worth pursuing in general and on an $n$Lab in particular :-) It is curious that there seems to be a cultural divide in the literature here: the book by Kashiwara-Schapira for instance amplifies sheafification as localization, which paves the road for $\infty$-stacks presented by the [[model structure on simplicial presheaves]], while the book by MacLane-Moerdijk amplifies sheafification as geometric embedding, which paves the road for the simple definition of [[(infinity,1)-sheafification]] by [[reflective (infinity,1)-subcategory]]. Lurie's book effectively gives the unified perspective, which I think is worthwhile presenting very clearly here on the $n$Lab, since it is coceptually so simple and transparent and in practice so powerful. Over.

  * added example to [[localization of a simplicial model category]]

  * added a little proposition to [[dependent product]] and a little example to [[geometric morphism]]

*  [[Tim Porter|Tim]]: I have given a partial reply to [[Urs Schreiber|Urs]] question at [[homotopy coherent nerve]].


# 2009-05-12 #

*  [[Toby Bartels]]:  An extensive rewrite and expansion of [[predicative mathematics]], including material on the non-[[constructive mathematics|constructive]] school (which rejects function sets), thanks to reading sparked by [one of Jonathan's posts](http://golem.ph.utexas.edu/category/2009/04/taming_the_boundless.html#c023753) to the Caf&#233;.

* [[Urs Schreiber|Urs]]

  * created [[derived smooth manifold]], but will have to continue tomorrow

  * created [[category of local models]] and [[locally modeled monoid]]

  * expanded a bit more on the "good limits"-motivation at [[derived stack]], alongside the [blog discussion](http://golem.ph.utexas.edu/category/2009/05/journal_club_geometric_infinit_3.html#c023770)

  * added a few more details to [[generalized smooth algebra]] -- and have a question on that on the blog [here](http://golem.ph.utexas.edu/category/2009/05/journal_club_geometric_infinit_3.html#c023762)

  * added a few bits and pieces to [[derived stack]], [[ind-object in an (infinity,1)-category]], [[perfect infinity-stack]]

* [[David Corfield|David]]

  * began [[Eckmann-Hilton duality]]. Referred to it from [[duality]], but maybe that page needs some adjustment. By the way, I still don't think I have answers to questions posed [here](http://golem.ph.utexas.edu/category/2009/04/cohomology.html#c023057) and below.

  * began [[initial algebra]] and [[terminal coalgebra]].

* [[Urs Schreiber|Urs]]

  * added the coherence diagrams to [[braided monoidal category]]

  * added the enriched versions to [[representable functor]] and [[opposite category]]

# 2009-05-11 #

*  [[Toby Bartels]]:  I moved all of the <abbr title="scalable vector graphics">SVG</abbr> out of article pages and into included subpages as described at [[HowTo]].  (Note that this is supposed to be a temporary fix until we get a working automated system to include somehthing like TikZ; see [the discussion](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=20).)

* [[Urs Schreiber|Urs]]:

  * added more details to and slightly restructured [[exact functor]] 

    * in particular added a remark on and a link to "[[flat functor]]", which overlaps in content

    * I changed at [[flat functor]] the condition that $(d/F)$ be filtered to the condition that it be cofiltered. Please check that I am not hallucinating! But see for instance [[Categories and Sheaves|KashSch prop. 3.3.2]]

  * after reading it I got the idea that [[Toby Bartels|Toby]]'s latest addition to [[stuff, structure, property]] is really about higher subobject classifiers as discussed at [[generalized universal bundle]]. I added corresponding remarks, but didn't find the time to look into this very carefully.

*  [[David Corfield|David]]: Started [[locally finitely presentable category]]

*  [[Toby Bartels]]:
   *  Added a sort of logical interpretation to [[stuff, structure, property]].  (This has some links that ought to be filled out.)
   *  There\'s more work going on at [[SVG Sandbox]] and being discussed in [a Forum post](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=20).  See also the new [[Inclusion Sandbox]].
   *  There\'s been some work recently at [[generalized element]], in response to a reader\'s question.

# 2009-05-08 #

*  [[Toby Bartels]]:  Fixed the last 'heuristic', at [[local system]], among other such fixes.  (You gotta open them up for editing and look at the source!)

* [[Urs Schreiber|Urs]]:

  * tied up the loose end at [[descent]] using the expected result that Dominic Verity was kind enough to proof on request and then confirm by private communication

* [[Andrew Stacey|Andrew]]: (I forget whether I'm supposed to add this to my earlier comment, or here, or add a word of this to each of the other entries of the day).  I've created [[SVG Sandbox]] expressly for the purpose of mucking about with SVGs to get them to look right.  My rationale is explained at the top of that page, together with some suggestions on how it might work.  The point is that one SVG can be rather large and I think that putting them in the regular Sandbox to test stuff is a bit anti-social.  Hopefully we can get stuff in the [[FAQ]] and [[HowTo]] on good ways of importing SVGs as there seem to be a few "special features".  I've shifted the recent SVG-related stuff from the original [[Sandbox]] to the [[SVG Sandbox]], but I shifted the discussion that Bruce started to the [nForum](http://www.math.ntnu.no/~stacey/Vanilla/nForum).

  * [[Urs Schreiber|Urs]]: I believe [[Mike Shulman|Mike]] had requested that we announce each change here always on the very top of the list, even if we had earlier logs the same day with other people's logs already on top of them. Seems to be a reasonable practice if the point of this page here is to alert others of changes. Which it is. So, yes, the way you did it should be the preferred way.

* [[Urs Schreiber|Urs]]:

  * recalled [[Tim Porter]]'s comment at [[simplicial set]] and moved [[simplicial nerve of simplicial categories]] to [[homotopy coherent nerve]];

  * started expanding, polishing and reorganizing [[simplicial set]] -- still not satisfied, though.

* [[Bruce Bartlett|Bruce]]: Added discussion to [[Sandbox]] about Andrew's TikZ->SVG method. Maybe we can get good and easy graphics going soon in Instiki!

* [[Urs Schreiber|Urs]]:

  * added lots of further stuff to [[simplex category]]

* [[Andrew Stacey|Andrew]]: Finished off the heuristic shift.  Bizarrely, one page, [[local system]], comes up in the Instiki search as having "heuristic" in it but I can't find it.  The other instances of "heuristic" that are left are either correct or within discussions.

* [[Urs Schreiber|Urs]]:

  * added explicitly the description in terms of weighted (co)limits and in terms of (co)ends to [[Kan extension]]; also reorganized the existing material somewhat.

  * added the definition of composition to [[enriched functor category]];

  * thanks to [[Andrew Stacey|Andrew]] for the thing about "heuristic". I'll be aware of that in the future.

    * following [[Toby Bartels|Toby]] I made [[heuristic introduction to sheaves, cohomology and higher stacks|heuristic intro...]] a redirection to [[motivation for sheaves, cohomology and higher stacks]]

*  [[Toby Bartels]]:
   *  I split [[identity]] into [[identity morphism]] and [[identity element]].  Maybe I\'ll do the same to [[inverse]] later, but not now.
   *  More details at [[extensional relation]].

# 2009-05-07 #

*  [[Toby Bartels]]:  Reply to Andrew below:
   *  Yeah, that\'s pretty much how to do it.  Except that you mark the old page as `category: redirect` rather than as `category: delete`, since it contains edit history that we want to preserve.  (Instiki has no cool page-move feature like MediaWiki does.)  As you did, I also usually decline to change links from discussion.
   *  I would move [[heuristic introduction to sheaves, cohomology and higher stacks]] to [[motivation for sheaves, cohomology and higher stacks]], since Urs doesn\'t like [[introduction to sheaves, cohomology and higher stacks]].

* [[Andrew Stacey|Andrew]]

  * Heuristically altered records containing the word "heuristic".  The original list of records matching the search term "heuristic" is below (so anyone worried can check what I've done).  Most actually were references to [[heuristic introduction to sheaves, cohomology and higher stacks]] which obviously needs to be renamed before the other pages are changed (what's the best way to rename a page?  Is it: create a new one, copy over the content, put in a redirect, change all referring pages, mark old one for delete?  Or is there a simpler way?).  In a couple of the others the word was used in a discussion so I didn't change those.  One I even left as I thought it was (almost) correctly used!

    * [[2009 April changes]]
    * [[Categories and Sheaves]]
    * [[General Discussion]]
    * [[Grothendieck's Galois theory]]
    * [[cohomology]]
    * [[full functor]]
    * [[geometric infinity-function theory]]
    * [[heuristic introduction to sheaves, cohomology and higher stacks]]
    * [[hyperstructure]]
    * [[induced representation]]
    * [[limit]]
    * [[local system]]
    * [[sheaf]]
    * [[sheaf cohomology]]
    * [[space and quantity]]
    * [[stuff, structure, property]]
    * [[weighted limit]]
    * [[why (infinity,1)-categories?]]

* [[Urs Schreiber|Urs]]

  * as a reaction to the discussion taking place there I expanded the text at [[simplicial model for weak omega-categories]] -- also added references

# 2009-05-06 #

* [[Urs Schreiber|Urs]]

  * reacted to the discussion at [[Day convolution]] and provided the requested further details in the main entry

  * corrected the statement about the relation of $SetMod$ to $Span(Set)$ at [[distributor]] by adding the missing clause about discrete categories

  * created [[structured generalized space]]

  * created [[string theory]]


# 2009-05-05 #

* [[David Corfield|David]]:

  * began [[things to be categorified]]

*  [[Toby Bartels]]:
   *  Fixed up [[extensional relation]], although there seems to be a problem with one of the counterexamples.
   *  I also have an opinion at [[simplicial model for weak omega-categories]].

* [[Urs Schreiber|Urs]]:

  * added a pedagogical example to [[enriched functor category]]

* [[David Corfield|David]]:

  * began [[microcosm principle]]

* [[Urs Schreiber|Urs]]:

  * added details to [[enriched functor]]

  * added a bit more detail to [[closed monoidal structure on presheaves]]

  * replied at [[cohomology]]

# 2009-05-04 #

* [[Urs Schreiber|Urs]]

  * worked on [[end]]: added a section "End as equalizer" where I try to motivate the formula for the end over $V$-valued functors from the equalizer formula for limits, then give the equalizer formula for ends -- personally I find this a bit more helpful than dinatural transformations, but that is certainly just my ignorance -- I added an "Idea" and a "References" and an "Examples" section 

  * added the definition to [[enriched category]] (yes, that was still "left as an exercise")

# 2009-05-03 #

*  [[Toby Bartels]]:
   *  Wrote [[FOLDS]] (and [[Michael Makkai]]), [[identity functor]], [[identity natural transformation]], [[anafunctor category]], [[identity anafunctor]], [[anabicategory]], and [[ananatural transformation]] to be linked from the below.
   *  Rewrote [[equivalence of categories]], moving one paragraph to [[Cat]] and otherwise expanding.
   *  Urs and I would like some advice from [[Tim Porter]] at [[simplicial nerve]].

* [[Urs Schreiber|Urs]]: 

  * further expanded section 2 of [[geometric infinity-function theory]], which I am to "report" on next Monday in our Journal Club. 

  * finally created [[simplicial nerve of simplicial categories]], but more details necessary...

  * am trying to find out, for [[A-infinity ring]] and [[E-infinity ring]] to which extent the two definitions "algebra over an $\infty$-operad" and "algebra object in a monoidal $(\infty,1)$-category" are equivalent, as one would expect...

  * created [[symmetric monoidal (infinity,1)-category]], [[commutative algebra in an (infinity,1)-category]], [[smash product of spectra]], [[associative ring spectrum]], [[A-infinity ring]], [[commutative ring spectrum]], [[E-infinity ring]]

  * expanded the intro at [[higher algebra]] a bit

  * thanks, [[Toby Bartels|Toby]], for your editorial help! Yes, right, "[[higher algebra]]" should be lower case, true.

# 2009-05-02 #

*  [[Toby Bartels]]:
   *  Disambiguated [[simplicial category]], hopefully correctly, at [[(infinity,1)-category]], [[derived stack]], and [[pretriangulated dg-category]].
   *  Wrote [[proper class]].
   *  Moved [[Higher Algebra]] to [[higher algebra]] because it *seemed* to be about the subject rather than about just Lurie\'s two papers, but I may have been wrong about that.
   *  Formatted theorems at [[descent for simplicial presheaves]] and [[descent]].
   *  Answered questions at [[biproduct]], [[comma category]], [[exponential object]], and [[context]].

# 2009-05-01 #

* [[Finn Lawler]]

  * Created [[lax 2-adjunction]], complete with spiffy PNGs.

  * Added some links at [[Gray-adjointness-for-2-categories]] to entries on concepts in the book.  Some of these are to non-existent pages like [[lax natural transformation]].  Do pages on 'elementary' stuff like this belong here on nLab, or should we add them to Wikipedia and link there?

   +--{: .query}
   [[Mike Shulman|Mike]]: If we have a page on [[category|categories]], we can certainly have a page on lax natural transformations!

   [[Jonas Frey]]: The problem about lax natural transformations is that there is no consensus about the orientation of constraints in the literature. Johnstone in the elephant and Gurski in his PhD-thesis for example use an other orientation than Leinster and Borceux in their books.

   _Toby_:  All the more reason to write an article to explain the differences!
   =--

* [[Urs Schreiber|Urs]]

  * created new top-level link list [[Higher Algebra]] -- to be filled with content...

  * considerably expanded [[(infinity,1)-category]] -- motivation was really to write [[relation between quasi-categories and simplicial categories]], but then ran out of steam

  * removed all existing logs here and archived them as [[2009 April changes]]


***

[[2008 changes|First list]] &#8212; [[2009 April changes|Previous list]] &#8212; No next list &#8212; **Current list**

***

category: meta
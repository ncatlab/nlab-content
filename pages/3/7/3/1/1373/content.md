<div class="rightHandSide toc">
[[!include all changes]]
</div>

Archive of changes made during April 2009.
The substantive content of this page should **not** be altered.
For past versions of this page beyond its own history, start [here](http://ncatlab.org/nlab/revision/2009+June+changes/632) and work backwards.

***


# 2009-04-30 #

* [[Urs Schreiber|Urs]]: 

  * continued filling in material at [[geometric infinity-function theory]] -- am hoping that my co-journalists will eventually start helping me there

  * replied to [[David Corfield|David]] at [[why (infinity,1)-categories?]]

  * added

    * [[(infinity,1)-category of (infinity,1)-presheaves]]

    * [[(infinity,1)-category of (infinity,1)-functors]]

    * [[(infinity,1)-category of (infinity,1)-categories]]

* [[David Corfield|David]]:

  * asked question at [[why (infinity,1)-categories?]]

* [[Urs Schreiber|Urs]]: 

  * added one more paragraph to [[why (infinity,1)-categories?]]

* [[David Corfield|David]]:

  * asked question at [[context]]

* [[Urs Schreiber|Urs]]:

  * expanded [[presentable (infinity,1)-category]] by adding the theorem that every presentable $(\infty,1)$-category is indeed presented by a combinatorial simplicial model category.

* [[David Corfield|David]]:

  * asked questions at [[exponential object]]

* [[Urs Schreiber|Urs]]:

  * started [[localization of a simplicial model category]]

  * created [[enriched model category]] and [[simplicial model category]]

# 2009-04-29 #

* [[Mike Shulman|Mike]]:

  * Moved the discussion about comma categories from this page to the   query box at [[comma category]].
  * Will look at [[descent]] when I get a chance.
  * Created a couple of firefox search plugins for the nLab and uploaded them to the [[HowTo]].

* [[Urs Schreiber|Urs]]: 

  * based on [[Zoran Skoda|Zoran]]'s references at [[enhanced triangulated category]] I created [[pretriangulated dg-category]] and [[twisted complex]], but then ran out of steam

  * moved a bit of material from [[derived infinity-stack]] to [[derived stack]] and then made [[derived infinity-stack]] a redirect to [[derived stack]]

  * finally wrote at least a blurb at [[stack]], only to make it look less orphaned in between [[sheaf]] and [[(infinity,1)-sheaf]].

  * created [[Verdier site]]

  * further fine-tuned the [DHI](http://arxiv.org/PS_cache/math/pdf/0205/0205027v2.pdf)-review at [[descent]]: now I dropped the discussion of homotopy limits entirely, as it's not really necessary; but I did include for a smoother presentation the assumption that we are on a [[Verdier site]], so that hypercovers "split" ([section 9](http://arxiv.org/PS_cache/math/pdf/0205/0205027v2.pdf#page=29)) which happens to be a Reedy fibrancy kind of condition after all ([page 11](http://arxiv.org/PS_cache/math/pdf/0205/0205027v2.pdf#page=11))

  * I browsed a bit through Dominic Verity's work and created entries on [[stratified simplicial set]], [[complicial set]], [[weak complicial set]], [[simplicial weak omega-category]] and [[Verity-Gray tensor product]] -- my main motivation was the claim now recounted at [[stratified simplicial set]] that the $\omega$-nerve on strict $\omega$-categories with values in $Strat$ has a strong monoidal left adjoint

* [[Zoran Škoda]]: created [[enhanced triangulated category]]

* [[Urs Schreiber|Urs]]:
 
  * filled the "details" section at [[descent for simplicial presheaves]] with the relevant material copy-and-pasted from [[descent]].

  * keep polishing, expanding and rearranging [[descent]] --  when [[Mike Shulman|Mike]] comes back online I am hoping to discuss a bit more the relation between Street's descent for $Str \omega Cat$-valued presheaves and the standard descent for their SSet-valued image under the $\omega$-nerve. As the new version indicates: the homotopy limit may be a red herring and the lack of monoidalness of the left adjoint of the nerve might be fixed by recourse to stratified simplicial sets using Verity's results (?)

  * added a pullback description to [[double comma object]]

* [[Mike Shulman|Mike]]:

  * I've noticed that Urs (in particular) has been widely using the notation $(f,g)$ for [[comma category|comma categories]] that Toby tried to prevent me from denigrating.  But I haven't heard any convincing arguments in favor of that notation, and I have lots of reasons to dislike it; see the discussion at [[comma category]].  If general opinion is against me, I'll shut up, but I want to hear from more people.  If you use the notation $(f,g)$, do you have positive reasons to prefer it to $(f/g)$ or $(f\downarrow g)$?

# 2009-04-28 #

* [[Mike Shulman|Mike]]: 

  * I have a question about [[biproduct]]s.

* [[Urs Schreiber|Urs]]:

  * created [[Bousfield-Kan map]]

  * created [[category of simplices]]

  * following [[Toby Bartels|Toby]]'s suggestion I moved [[descent and codescent]] to [[descent]] -- then I entriely rewrote it! Now it starts with very general nonsense on localization of $(\infty,1)$-presheaves and then derives descent conditions as concrete realizations of that localization. Currently where it ends I am planning to add discussion about how to further get from descent to gluing conditions (i.e. to $\Delta$- and oriental-weighted limits) following discussion that I am having with [[Mike Shulman|Mike]] on the blog [here](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit.html#c023460)

  * added more details to [[ind-object]], relating the two different definitions

  * added standard examples of presheaves on open subsets to [[inverse image]]

  * started adding a list "properties" to [[colimit]] analogous to the one at [[limit]]

*  [[Toby Bartels]]:
   *  Since I\'m making up a word at [[exponential object]], I decided that both terms should be adjectives, leaving the verb simpler.
   *  I included some lower-dimensional cases at [[associahedron]].  I managed to get down to $K_1$.

# 2009-04-27 #

* [[Urs Schreiber|Urs]]

  * added a list of basic propeties to the end of [[limit]]

# 2009-04-26 #

* [[Mike Shulman|Mike]]: 

  * Added a couple new examples, and tried to uniformize the descriptions, at [[A-infinity-operad]].

  * Created [[indiscrete category]].

# 2009-04-25 #

* [[Urs Schreiber|Urs]]: 

  * added a discussion of hom-objects in terms of homotopy limits at [[simplicial presheaf]] (in a new section "Properties")

  * created [[reflective (infinity,1)-subcategory]] and [[localization of an (infinity,1)-category]] and [[local object]]

  * created [[hypercompletion]] and [[descent for simplicial presheaves]]

  * created [[associahedron]] (see the discussion with [[Jim Stasheff]] over at the blog, [here](http://golem.ph.utexas.edu/category/2009/04/categorification_and_topology.html#c023441))

  * expanded [[A-infinity-operad]]: a bit about associahedra, but mostly more detailed links to references

# 2009-04-24 #

* [[Urs Schreiber|Urs]]

  * created [[A-infinity operad]]  and [[category over an operad]] and gave the operadic definition at [[A-infinity category]]

*  [[Toby Bartels]]:
   *  Changed the numbering at [[k-tuply connected n-category]] but haven\'t moved the page yet.
   *  Created a new [category: lexicon](/nlab/list/lexicon) to find Tim\'s lexicon entries.  (If these are incorporated into more mainstream $n$Lab entries, then we could get rid of this category, but for now it\'s nice to be able to track them down without running through the whole list.)
   *  I answered Mike\'s question at [[Boolean topos]].
   *  I coined a new term at [[exponential object]].
   *  I finished [[dependent product]].

* [[Urs Schreiber|Urs]]: 

  * came across the useful interrelation diagram and associated literature list on "enhancements of triangulated categories" [here](http://www.math.uni-bonn.de/people/schwede/EnhancedSeminar.pdf) and added this to [[stable (infinity,1)-category]], together with some links it suggests, to entries still to be created -- I am hoping we'll eventually be able to accumulate a good collection of material on this topic

  * added Lie $\infty$-links to [[rational homotopy theory]]

  * added missing links back and forth between [[Yoneda extension]] and [[free cocompletion]]

  * added to [[generalized universal bundle]] the remark that it is a means to compute the "lax pullback" (really: [[comma object]]) of a point.

  * added at [[category of elements]] the equivalent definition in terms of comma category and in terms of pullbacks of the universal Set-bundle -- and in terms of "lax pullback" (comma object) of the point

    * added a link to [[category of elements]] at [[ind-object]] where we recently had a discussion about this point

  * added the discussion and diagram at [[comma category]] characterizing it as a [[comma object]] 

    * added link and remark to [[comma object]] and [[comma category]] at [[co-Yoneda lemma]]

  * made the comma category explicit on which a [[simplicial local system]] is a functor

*  [[Tim Porter|Tim]]: I have created a few entries relating to the interaction of [[local system]] with ideas from rational homotopy theory, especially algebras of differential forms on simplicial sets, based on Sullivan and further back Thom and Whitney. These included [[simplicial local system]], see Urs comment below, to which I have started replying. Perhaps I will be able to add more shortly. These entries are not yet finished and do not yet deal with the Sullivan-Thom-Whitney stuff.

* [[Urs Schreiber|Urs]]: have some questions at [[simplicial local system]]

# 2009-04-23 #

* [[Mike Shulman|Mike]]: Since no one objected to my proposal on how to resolve the duplication between [[category of fractions]] and [[multiplicative system]], I implemented it.  The relevant material is now at [[calculus of fractions]].  I deleted a bit of the material about derived functors because it was not really specific to calculi of fractions, belonging more at [[derived functor]].

*  [[Toby Bartels]]:  A question (not a dispute!, what do you know?) on terminology at [[exponential object]].

* [[Mike Shulman|Mike]]: 

  * Disagreed with Toby at [[k-tuply connected n-category]]: I think connectedness should be 0-connectedness, not '1-tuple' connectedness.

* [[Urs Schreiber|Urs]]: 

  * created [[path groupoid]] -- other realizations of that idea should be stated there, too

  * started creating a random list of some examples at [[limits and colimits by example]] -- but not in the intended detailed form yet

  * started reworking [[local system]] as we discussed there -- still lots of room for improvement left, of course!, in particular many references could use more details and links

    * notice that I moved the discussion box to the end of the entry; _not_ to imply that the discussion is closed, but so that the box does not disturb the structure of the entry; I think this is reasonable for every discussion that concerns an entry as a whole more than a particular point in it

*  [[Toby Bartels]]:
   *  From our first spam post (which I will not link to), I\'d like to preserve this: 'with a country like India, the [[limit]]s are [[end]]less' (links added).
   *  Wrote [[k-tuply connected n-category]].  I also made the numbering consistent on the other pages; connectedness should be $1$-tuple connectedness, not $0$-tuple connectedness.
   *  Tried my hand at a constructive version of [[cyclic order]].  Interestingly, the apartness relation doesn\'t seem to be recoverable from the cyclic order relation (which is related to the difficulty of doing antisymmetry and thus a reflexive version, which as well is not ---even classically--- equivalent to the negation of the irreflexive version).

* [[Urs Schreiber|Urs]]: 

  * have a reply at [[local system]]

  * found time to work a bit more on [[Lie infinity-algebroid representation]]

    * request to [[Tim Porter|Tim]] and others: there is naturally a kind of "twisting function" appearing there. One aim of my presentation is not to postulate it, but to derive that it arises from a (co)fibration of DGCAs. I am thinking that all the [[twisting function]]s and [[twisting cochain]]s should have such a _conceptual_ definition, from which one derives the usual component-wise definition by unravelling the component-wise mechanisms. I think here on the $n$Lab we should try to find and give conceptual categorical explanations as far as possible. My personal feelling is that all discussion of "twisting cochains" and related phenomena would become considerably clearer and less confusing if one had this.

*  [[Toby Bartels]]:  Please note that there are no actual links to [[Differential Nonabelian Cohomology]] (except this one just now).  That there appear to be is actually a bug in Instiki (which I haven\'t bothered to report to Jacques yet).

* [[Tim Porter|Tim]]:  

   * I have added a request  at [[local system]]. Basically the current entry reads as if it related to a relatively recent idea. I suggest we look at the origins of the idea,  at least as old as 'Steenrod (1943)' if not before.  It is central to much of the nLab work. Probably we need to be much less restrictive in the motivation of this entry.

   * I have added some historical and motivational perspective in [[twisting function]] and would suggest that a similar section is needed for [[twisting cochain]].  The two threads of twisting the fibre and _deforming_ the local structure of a 'product' are at the origin of both concepts.

# 2009-04-22 #

* [[Urs Schreiber|Urs]]: created [[Lie infinity-algebroid representation]] -- but ran out of time before done with polishing

* [[Mike Shulman|Mike]]: Created [[cyclic order]] in order to propose a clean definition of the [[Connes' cyclic category|cycle category]].

* [[Zoran Škoda]]: [[quasicompact]]

# 2009-04-21 #

* [[Zoran Škoda]]: created [[quasicoherent sheaf]],[[kernel functor]], [[Gabriel composition of filters]], [[Gabriel filter]], [[uniform filter]], [[Serre subcategory]]. Corrected [[Gabriel multiplication]], thanks Toby. Created [[ringed space]] differing from [[ringed site]].

* [[Urs Schreiber|Urs]]: edited [[geometric infinity-function theory]] to go along with [this](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit.html#c023356) blog message

*  [[Toby Bartels]]:
   *  Started to expand on [[dependent product]], but I need to leave now without finishing, so I\'ll let Mike do it.  (^_^)
   *  A request at [[fibered n category]].
   *  There\'s an obvious typo at [[Gabriel multiplication]], but I don\'t know which way to fix it.

* [[Urs Schreiber|Urs]]: 

  * have two questions on examples at [[semi-abelian category]]

  * created [[dependent product]] just to satisfy the link from [[universe in a topos]]

  * added a list with a handful of general properties to [[adjoint functor]]
 
  * moved the old discussion at [[representable functor]] to the bottom of the page

* [[Zoran Škoda]]: I have made [[D-module]] and [[local system]] somewhat more precise; actually I have put lots of more precise statements; the subtleties on wheather we work over a complex manifold, variety, variety in char zero, or nonsingular variety in char 0, may affect some of the statements. To suplement this I was forced to create a comprehensive entry [[regular differential operator]]. I see that for some reason people continue talking connections and 
avoid going down to sheaves, resolutions of diagonal, de Rham site and regular differential operators, which are all necessary to cover this subject properly in my view; there are missing related items like [[holonomic D-module]], treatment of costratification, crystals and so on. I created [[coreflective subcategory]], just giving the definition and saying that the rest of abstract preoprteis are dual to [[reflective subcategory]] where more is written. But one should write specific examples which call specifically for coreflective subcategories. Created [[topologizing subcategory]], [[thick subcategory]] and [[Gabriel multiplication]] in the generality of abelian categories (one should add the proper discussion of thick, topologizing in triangulated and suspended categories, and Gabriel mult. for filters, but I run out of energy for today); one needs to add entry on Serre subcategory which is easy in module and Grothendieck categories, but more subtle in general abelian categories. There is a query under [[fibered n category]], I think we should have both entry [[fibered n category]] and [[n-fibration]]; the first entry dedicated to STRICT n-categories and consequently strict universal properties and the name due Grothendieck, Gabriel, Gray and Hermida; and the latter in weak version and with homotopy style nomenclature accordingly. My praise for creative expansion to Mike.  

* [[David Roberts]]:

  * Added examples to [[semi-abelian category]] - the opposite of the category of pointed objects in a topos, and the category of crossed modules.

# 2009-04-20 #

* [[Urs Schreiber|Urs]]: 

  * created stub for [[local system]] in the context of a comment I left [here](http://sbseminar.wordpress.com/2009/04/20/three-ways-of-looking-at-a-local-system-introduction-and-connection-to-cohomology-theories/)

  * created [[derived stack]] to go along with our [Journal Club activity](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit.html)

*  [[Toby Bartels]]:  I think that the naming discussion at [[ind-object]] is still current until Eric is happy.
   *  [[Urs Schreiber|Urs]] responds:  sure, I just thought for readability the discussion would be better had at the bottom of the page -- a big green box in the middle of the entry gives the reader the impression that he or she needs to beware of some urgent unsettled issue before reading on.
   *  _Toby_:  Ah, whereas I see the big green box up top as simply indicating an unsettled issue, urgent or otherwise.
   *  _Urs_:  okay, that makes sense, let's leave it this way -- maybe eventually we need some mechanism to decide when to move a disscussion box to the bottom of the page -- probably the mechanism should be that the one who started the discussion is the one decide

* [[Finn Lawler]]:  Replied to Toby at [[minimal logic]], and slightly expanded [[paraconsistent logic]] to incorporate some of our discussion.

* [[Urs Schreiber|Urs]]:

  * added to [[Yoneda lemma]] the following: a word on the proof, two further corollaries, a word on the meaning of the first two corollaries

*  [[Toby Bartels]]:  Put [[well-order|simulations]] everywhere.  I need to think about this (and read Aczel) some more, but I\'m fairly sure that Mike is right about them.

* [[Urs Schreiber|Urs]]:

  * started polishing the typesetting at [[bundle gerbe]], but there is still plenty of room for further improvement

  * added a summary list to the section "Example: universes in SET" at [[universe in  a topos]]

* [[Mike Shulman|Mike]]: 

  * Added the correct equivalent definition to [[semi-abelian category]] and deleted the discussion about what it might be.

  * Added another version of [[Cantor's theorem]].

  * Expanded [[extensional relation]] to discuss several possible notions of extensionality, reserving the term 'extensional' for the one that I think is most important (but feel free to disagree).

  * Commented on the right notions of morphism for [[relation]], [[well-founded relation]], [[well-order]], and [[extensional relation]].

* [[David Corfield|David]]:

  * imported Urs' material on [[bundle gerbe]]. nLab doesn't seem to like latex within lists. How do we fix this?

* [[Urs Schreiber|Urs]]: 

  * created [[limits and colimits by example]] for purposes discussed on the blog [here](http://golem.ph.utexas.edu/category/2009/01/nlab_general_discussion.html#c023321) and [here](http://golem.ph.utexas.edu/category/2009/04/graphical_category_theory_demo.html#c023323)

*  [[Toby Bartels]]:
   *  Yet more at [[pure set]].  See the pretty pictures!  Or rather ... make them pretty if you know how, for I do not.  (;_;)
   *  Another question for Finn, now at [[minimal logic]].
   *  More correct material at [[pure set]].

# 2009-04-19 #

*  [[Toby Bartels]]:  I\'ve started a dispute at [[paraconsistent logic]].
   +--{: .query}
   [[Finn Lawler|Finn]]: No, you haven't -- I was wrong.
   =--

# 2009-04-18 #

* [[Finn Lawler]]:

  * created [[sequent calculus]] and [[paraconsistent logic]]: just brief explanations and links to Wikipedia.

* [[Urs Schreiber|Urs]]: 

  * created a stub for [[differential cohomology]]

# 2009-04-17 #

* [[Zoran Škoda]]: created [[comodule]], [[flat module]], [[cotensor product]].

*  [[Toby Bartels]]:  Added information on morphisms to [[relation]], [[extensional relation]], [[well-founded relation]], and [[well-order]].  I hope that all of my claimed theorems are true, in which case I\'m sure that all of my proposed definitions are good.  (^_^)

* [[David Corfield|David]]

  * made a request at Mike's [categorified logic](http://ncatlab.org/michaelshulman/show/categorified+logic)

  * created [[D-module]]

  * created [[coherent logic]]

  * added John's blog exposition to [[induced representation]]. Is the style OK?

* [[Urs Schreiber|Urs]]: 

  * expanded [[hom-set]] a bit

  * remarked at [[semi-abelian category]] that the now deprecated second equivalent definition was taken directly from the (single) reference we give. I think instead of just removing it we should try to correct it.

*  [[Toby Bartels]]:
   *  Wrote [[axiom of extensionality]] and [[transitive closure]] while writing the below.
   *  Added the more general definition to [[extensional relation]].  It seems right to me and I can prove that it\'s correct for well-founded relations, but I must admit that I made it up just now.
   *  More details about how to model [[pure set]]s in structural set theory, applying the above.
   *  Wrote [[Cantor's theorem]], including a constructive version from Paul Taylor.

# 2009-04-16 #

* [[Zoran Škoda]]: created [[Tohoku]], [[quasi-pointed category]], made changes to [[sheafification]],[[additive and abelian categories]], [[torsion]], [[torsion subgroup]]

* [[Mathieu Dupont|Mathieu]]:

  * corrected [[semi-abelian category]] and answered to Mike

* [[Urs Schreiber|Urs]]: 

  * added some links to [[Tim Porter|Tim]]'s latest addition to [[rational homotopy theory]] -- in that context I created [[torsion]] and [[torsion subgroup]]

  * finally created [[exact sequence]] which was requested by a bunch of entries

  * added to the "Idea" section of [[Grothendieck category]] a statement suggesting that these are _precisely_ those additive categories for which sheafification exists. Is that right?

  * [[Zoran Skoda|Zoran]] kindly looked up the definition of AB6-category which was still missing at [[additive and abelian categories]], I put it in now 

* [[Tim Porter|Tim]]:

  * I created the next entry in the rational homotopy lexicon series with the ungainly title [[differential graded algebras and differential graded Lie algebras-relationships]]. 

  * I added another viewpoint to [[rational homotopy theory]] which is more in keeping with Quillen's 1969 paper.

* [[Urs Schreiber|Urs]]:

  * created [[GUT]] and [[induced representation]] as places for collection of material currently discussed on the blog

  * included [[Todd Trimble|Todd]]'s proof of MacLane's co-Yoneda into [[co-Yoneda lemma]]

  * tried to bring [[A-infinity-category]] into some shape by adding more introductory discussion and ordering the references a bit -- also have a question

* [[Tim Porter|Tim]]:

  * Replied to [[Urs Schreiber|Urs]] at [[bar and cobar construction]] (at least I hope the reply goes some way to answering the query).

  * Created [[reduced suspension]] as I needed it for my 'reply' above.

* [[Urs Schreiber|Urs]]: 

  * replied to [[David Roberts|David]] at [[ind-object]]

  * have a request and a question at [[bar and cobar construction]]

* [[David Roberts]]: 

  * Added a comment in section generalizations at [[ind-object]], re comma category.

# 2009-04-15 #

* [[Zoran Škoda]]: created [[fibered n category]], [[Karoubian category]], [[pseudo-abelian category]] (redirect),  [[Koszul duality]], [[pure motive]], [[Voevodsky motive]], [[motives and dg-categories]] (there needs to be a separate big entry on [[mixed motive]], then [[motivic complexes]], [[standard conjectures]], [[Hodge filtration]] etc.), [[element in abelian category]]; created book-page [[Gray-adjointness-for-2-categories]]; additions and references to [[A-infinity category]], [[dg-category]], [[twisting cochain]].

* [[Urs Schreiber|Urs]]: 

  * created [[ind-object in an (infinity,1)-category]] 

  * created [[cofinal functor]] and [[cofinally small category]], but just the bare defintion so far

  * expanded [[ind-object]]: added more motivation in "Idea" section, added examples, added list of properties

# 2009-04-14 #

* [[Urs Schreiber|Urs]]:

  * added a discussion to [[universe in a topos]] with more details on how to get back the Grothendieck universe axioms in $SET$. Please check. I'd be grateful for improvement.

  * to Andrew: I think we want here on the $n$Lab as much detail as we can get hold of -- if an entry becomes too long, though, it might be an option to split off entries from it "more details on xyz" or the like and link to them

* [[Andrew Stacey|Andrew Stacey]]: Added the basic definitions to [[Chen space]] and some of the other variants of [[generalized smooth space|generalised smooth space]].  How much detail do we want on these pages?

* [[Andrew Stacey|The English Pedant]]: I'm not convinced about the use of the word "heuristic" on the n-Lab.  I've started a discussion on the [n-Forum](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=17) rather than force my views on the English language on the n-Lab.  I realise that this is a little against the Wiki-spirit but I figured that if I went through changing all occurrences of the word "heuristic" then someone would object and we'd have a discussion about it; so to save a bit of agro, I'm instigating the discussion first.

*  [[Toby Bartels]]:  I started a new category, `foundational axiom`, in which I put the pages that contain axioms that one might (or might not) want in one [[foundations]] of mathematics.  That way, anyone with opinions on the matter can check them to see that one\'s views are represented.  (A few don\'t really have much in the way of an axiom right now, but one could be added or noted there.)  This does not include things like the axioms for a [[group]], but rather axioms for [[set theory]] (or other foundational theory).  (Although [[set theory]] itself I don\'t think should really be included, but [[ETCS]] is in there.)

#2009-04-13

* [[Mike Shulman|Mike]]: Did some massaging of [[well-order]], [[well-ordering theorem]], [[well-founded relation]], [[choice object]], and [[axiom of choice]], and created [[extensional relation]].

* [[Zoran Škoda]]: completed the definition of [[congruence]].

#2009-04-12

* [[Zoran Škoda]]: Today a Hopf algebraist resurrected in me...grrr...[[Hopf action]], [[measuring]], [[Heisenberg double]], [[bimonoid]], [[module algebra]], [[comodule algebra]]. Well, I am writing an article about a special case of a Heisenberg double, maybe that is why.  

#2009-04-11

*  [[Toby Bartels]]:
   *  Wrote [[axiom of foundation]], [[well-founded relation]], and [[well-ordering theorem]].
   *  Added to [[successor]], [[inaccessible cardinal]], [[well-order]], [[partial function]], [[ordinal number]], and [[cardinal number]].
   *  Commented on [[direct sum]], [[presentable (infinity,1)-category]], [[stable (infinity,1)-topos]], [[sequential convergence space]], and [[quantale]].
   *  Moved material from [[Cat]] to [[n-category]].
   *  Moved [[ordinal]] to [[ordinal number]], partly because it\'s more noun-like and partly to match [[cardinal number]].
   *  Moved $1$-categorial material from [[compact object in an (infinity,1)-category]] to [[compact object]].

* [[Mike Shulman|Mike]]:  Thanks Finn!  It was great to meet you too.  I sliced up your paragraph mentioning fibrations and incorporated the material in other places where I thought it fit better.

* [[Zoran Škoda]]: Created [[Frobenius category]]; added material in [[dg-category]] on dg-modules, Yoneda functor and  "pre-triangulated". One should also explain the pre-triangulated envelope functor.

#2009-04-10

*  [[Finn Lawler]]:

   * Created [[minimal logic]] and [[intuitionistic logic]], as very small stubs.  Introduced yet more broken links there, which I'll fill in later.

   * Slightly corrected Mike's new entry [[type theory]], and added a paragraph mentioning fibrations.  I'm not sure it's in the right place, though.  (PS. Mike: it was great to meet you in Cambridge!  Also, Bruce: thanks for finding me a seat in the restaurant!)

*  [[Toby Bartels]]:  I aksed an idle question at [[combinatorial spectrum]] about Kan complexes and $\mathbf{Z}$-groupoids.

* [[Mike Shulman|Mike]]: 

  * Created [[type theory]] with an introduction for category-theorists.  Additions and corrections are welcome.

  * Some improvements and corrections to [[cardinal number]], [[ordinal]], [[well-order]] (what an ugly noun!), [[transitive set]], and [[inaccessible cardinal]], and created [[von Neumann hierarchy]].  In particular, I added the structural point of view to complement the naive and material ones.

* [[Urs Schreiber|Urs]]:

  * added a reference with a remark to [[A-infinity category]]. Would be nice to have more literature here, and more discussion on the relation to [[dg-category]] and [[stable (infinity,1)-category]] 

* [[Zoran Škoda]]: I have made additions to [[cardinal number]]: Urs uses a naive set definition where cardinals are equipotence classes of sets hence his cardinals are proper classes; I follow a choice of representative among ordinals ([[well-order]]ed [[transitive set]]s); to this aim I created [[transitive set]], [[ordinal]], [[successor]], [[inaccessible cardinal]]. In doing this I used some intro parts of my lectures on sheaf theory which I currently teach in Zagreb in Croatian (and which initially started with cardinals, universes and categories). I created [[twisting function]].

* [[Urs Schreiber|Urs]]:

  * added a remark on the $(\infty,1)$-version at [[Dold-Kan correspondence]]

  * created [[accessible (infinity,1)-category]] and [[accessible (infinity,1)-category]], but incomplete

  * created [[compact object in an (infinity,1)-category]], but incomplete

  * created [[cardinal number]] and [[well-order]], but experts should please check these

  * created [[sigma-model]]

  * created an entry [[geometric infinity-function theory]] to go along with the $n$Caf&eacute; entry [Journal Club -- Geometric Infinity-Function Theory](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit.html)

  * created [[natural numbers object]] just to saturate links (and it should indeed be "natural numbers object", not "natural number object", agreed?)

  * worked comment by [[David Ben-Zvi]] into [[why (infinity,1)-categories?]], but more needs to be done

#2009-04-09

* [[Urs Schreiber|Urs]]: 

  * I had been asked by students to say something about why they should care about learning about $(\infty,1)$-categories. I thought that would be a good thing to try to answer in an $n$Lab entry, so I started an entry [[why (infinity,1)-categories?]]. This is just a first attempt. Maybe somebody would enjoy adding his or her own points of views of correcting/improving mine.

  * created [[Connes fusion]], but filled in only pointers to further references

* [[Zoran Škoda]]: created [[von Neumann algebra]] emphasising on sources of relations to category theory and low dimensional topology (particularly G. Segal's program on relations between CFT and elliptic cohomology). There is a good wikipedia entry on von Neumann algebras with lost of references and details, but neglecting the connection to the above topics which should be expanded on. Moreover somebody should mayve write entres on related topics as [[Connes fusion]], [[modular functor]] etc. as those are relevant for some of us.

*  [[Toby Bartels]]:  I came to some sort of decision at [[direct sum]].

#2009-04-08

* [[Urs Schreiber|Urs]]:

  attempted a (long-winded) reply to [[David Corfield|David]]s question "What does it mean" at [[Coyoneda lemma]] (and would anyone mind if we renamed that to [[co-Yoneda lemma]]?)

* [[Mike Shulman|Mike]]: 

  * Following Toby's suggestion, moved [[subsequential space]] to [[sequential convergence space]].  Split [[convergence space]] and [[Cauchy space]] off from [[filter]], and added some stuff about pseudotopological spaces to [[convergence space]].

  * Created [[Reedy category]].

* [[David Corfield|David]]: Created [[Coyoneda lemma]]. What does it mean?

#2009-04-07

* [[Mike Shulman|Mike]]: Created [[subsequential space]] with a bit of propaganda.

* [[Zoran Škoda]]: I created entries [[orbit category]], [[Dold-Thom theorem]] and [[satellite]] with most basic definitions, properties and references, but quickly run out of energy; one should at least add the definition of the morphism part of the satellite functors, the connecting morphism for long exact sequence of satellites, and connection to the Kan extensions. Made some additions to [[Dold-Kan correspondence]].

*  [[Toby Bartels]]:  I have a terminological question at [[direct sum]].  (It\'s a rather elementary question in universal algebra.)

#2009-04-06

* [[Urs Schreiber|Urs]]: 

  * created [[Deligne cohomology]]

  * reacted to [[Bruce Bartlett|Bruce]]'s question at [[heuristic introduction to sheaves, cohomology and higher stacks]] by expanding further on the notion of morphisms of sheaves

  * expanded slightly at [[AQFT]] -- still just a stub entry, though

  * touched [[combinatorial spectrum]]: replied to [[Mike Shulman|Mike]], expanded the discussion of examples and changed the notation there a bit. But please check. I'll send a request about this to the blog.

  * replied to [[Tim Porter|Tim]]'s comments on [[Zoran Skoda|Zoran]]'s comment at [[differential graded Lie algebra]]

  * replied to the questions that were at [[restriction and extension of sheaves]] (on notation and existence) by adding more details

* [[Tim Porter|Tim]]: 

  * I have adjusted an addition to [[differential graded Lie algebra]]. This used the term 'simply', but it is often not clear that one definition is 'simpler' than another.  'Simplicity' is sometimes clear, but is often in the eye of the beholder. I would love to see some discussion on this as it is an easy trap to fall into (as I know to my cost!) and there are several other similar traps out there which are just as difficult to avoid! Perhaps on the caf&#233;???

#2009-04-05

* [[Urs Schreiber|Urs]]:

  * added a few links to examples at [[space and quantity]] (we have a general problem that many entries created eraly on don't currently point to entries created more recently which de facto they should point to)

  * touched [[combinatorial spectrum]]: replied to [[Mike Shulman|Mike]], added a list of examples and have further questions

#2009-04-04

* [[Tim Porter|Tim]]: 

  * I have put another of the Lexicon series of entries up.  It is [[bar and cobar construction]]. This looks at the differential algebra behind those constructions, and sketches the bar-cobar adjunction. 

  *  I have tried to provide more links to and from this series of 'lexicon' entries. (soon will be finished!)

* [[Urs Schreiber|Urs]]: 

  * further polished [[nonabelian cohomology]]

  * created [[combinatorial spectrum]]

  * expanded [[abelian sheaf cohomology]]

  * created [[cohomology]]

  * created [[heuristic introduction to sheaves, cohomology and higher stacks]]

#2009-04-03

* [[Urs Schreiber|Urs]]: 

  * added a bit more details to [[abelian sheaf cohomology]]

  * added discussion of the sheaf version to [[Dold-Kan correspondence]]

  * started an entry [[abelian sheaf cohomology]], but have just the "Idea"-section so far (aiming to provide the right $\infty$-categorical perspective)

  * provided, using [[Todd Trimble|Todd]]'s help, the details on the relations between the two definitions at [[closed monoidal structure on presheaves]] and created a supplementary entry [[functors and comma categories]] on properties of, well, functors on comma categories

#2009-04-02

* [[Tim Porter|Tim]]: 

  * I have put another of the Lexicon series of entries up.  It is [[differential graded Hopf algebra]]. 

* [[Urs Schreiber|Urs]]:

  * reorganized the entry [[mathematics]] a bit -- I am hoping that eventually this becomes a useful top of a small hierarchy of link-list entries which allow the reader to get an idea of the scope of topics covered (and not yet covered) by the $n$Lab, and possibly to facilitate searches by topic rather than by keyword

  * as discussed with [[Timothy Porter]], I created a stub for [[rational homotopy theory]] whose main purpose at the moment is to contain the link list to his lexicon entries on concepts in differential graded algebra

  * created [[closed monoidal structure on presheaves]] and [[closed monoidal structure on sheaves]], but am being dense: have a question at the former

  * created [[direct image]] and [[inverse image]] and [[restriction and extension of sheaves]]

  * moved discussion from [[semi-abelian category]] to [[Dold-Kan correspondence]] and added references

  * added explicit formulas to [[Yoneda extension]] (not the [[end]]-yoga, though)

  * added a question to [[Mike Shulman|Mike]]'s question at [[semi-abelian category]] (probably for [[Tim Porter|Tim]])

  * polished [[infinity-topos]]

#2009-04-01

* [[Urs Schreiber|Urs]]:

  * prodded by [[Tim Porter|Tim]]'s latest comment at [[Dold-Kan correspondence]] I looked up and then created an  entry for [[semi-abelian category]]

* [[Tim Porter|Tim]]: (I seem to remember a request to put more recent changes at the top, even if you have one on today's page so ... .)

  * I have put another of the Lexicon series of entries up.  It is [[differential graded Lie algebra]].

* [[Urs Schreiber|Urs]]

  * created [[infinity-stackification]]

  * added a section "Idea" to [[abelian sheaf]]

  * added a section "Idea" to [[Dold-Kan correspondence]]

  * created [[injective object]]

  * created [[complex]]

  * created [[Grothendieck category]] -- it feels like this should make me say something about that axiom list at [[additive and abelian categories]]...

  * tried to resolve/incorporate parts of the discussion at [[localization]] by reworking the entry a bit -- also left a comment there

  * noticed that we have considerable overlap now between [[multiplicative system]] and [[category of fractions]]. Left a comment there to remind us. Somebody who knows the precise status of these two terms in the math community should please go ahead and merge the material in one entry, keeping a redirect page for the respective other term

* [[Tim Porter|Tim]]:

  * I have added a comment on the terminology [[localization]]. Perhaps an algebraic geometric historical perspective could be useful here to help explain the terminology. (I'm not sure that I am competent to provide this however!)

  * I have put another of the Lexicon series of entries up.  It is [[differential graded coalgebra]].

* [[David Roberts]]:

  * Added [[bicategory of fractions]], [[category of fractions]] and [[wide subcategory]].
  * Started adding the construction of the [[localization]] of a category, as well as a speculative comment at that page on computing this as a [[fundamental category]].

  * Migrated [[2009 March changes|March changes]] 

  * Continued discussion with Urs at my private page [[davidroberts:comments on chapter 2]].


***

[[2008 changes|First list]] --- [[2009 March changes|Previous list]] --- [[2009 May changes|Next list]] --- [Current list](http://www.math.ntnu.no/~stacey/Vanilla/nForum/?CategoryID=5)

***

category: meta
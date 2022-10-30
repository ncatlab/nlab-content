[[!include all changes]]


All non-trivial additions or changes to the $n$Lab should briefly be indicated here. This way [[Contributors|the rest of us]] can spot them, so we can learn what you know --- and maybe make further improvements!

+-- {: .standout}

Please log all your non-trivial changes to the $n$Lab here!

=--

Here "non-trivial" means: anything that any other contributor might be interested in taking notice of. If you fix a trivial typo in the text somewhere, that is highly appreciated but unlikely to be controversial and hence need not be logged here. But already if you fix a typo in some _formula_, it may be of interest. Generally: the more you log your activity here, the better. Even when in doubt whether anyone else might be interested in changes you made, drop a note here on what you did.

These comments should go in _reverse_ chronological order, so that the latest are on top of the list. To keep the list international, use the date in UTC (the date given by the server for your edits).  However, regardless of that, be sure to **add new comments to the top** of the list.

***

## 2009-08-03

* [[Zoran Škoda]]: To assist [[John Baez]]'s links, created [[Eilenberg-Moore category]], [[Kleisli category]] and added details and redirects to [[monadic functor]]. To John's question: I think most basic facts in Tannaka reconstruction including sort of those on coalgebra level are in chapter 3 of [Bodo Pareigis' online notes](http://www.mathematik.uni-muenchen.de/~pareigis/pa_schft.html); his emphasis is on [[end]]s and coends. However I hope you find Kazhdan's notes, they must be great. I created entry [[Tomasz Maszczyk]] with very interesting past seminar abstract at the bottom relating a new reconstruction theorem coming from nc geometry. 

* [[Urs Schreiber]]: expanded the example list at [[twisted cohomology]] -- in particular added "cohomology with local coefficients" as a special case. Added to the very beginning of [[local system]] a paragraph on how strictly speaking local systems were meant to be such "local systems of coefficients".

* [[Zoran Škoda]]: created [[smooth scheme]], [[flat morphism]], [[smooth morphism of schemes]], [[EGA IV]], [[locally affine space]], [[relativization in algebraic geometry]]. Notice that this is extending a series on regularity/smoothness/differential calculus in algebraic framework which included our earlier entries [[regular differential operator]], [[quasi-free dga]], [[formally smooth morphism]] and so on.
  
  * John and Ramesh thank you for the nice detailed material on Lawvere reconstruction theorem, I'd suggest to create a separate lab entry [[Lawvere reconstruction theorem]] on it, moving the most of the material there (regarding the size and number of other reconstruction theorems waiting to be covered in detail the same way) with a link and short comment on the main [[reconstruction]] page. 

* [[John Baez]] expanded [[reconstruction theorem]] (it seems)

  * [[Sridhar Ramesh]] expanded this a little more, in particular discussing the infinitary analogue of Lawvere's reconstruction theorem and the monadic perspective on this, as well as cursorily noting how this is all nothing more and nothing less than the Yoneda embedding lemma cast into logical guise

* [[Urs Schreiber]] created [[Chevalley-Eilenberg cochain complex]]

* [[Zoran Škoda]]: posted _[[jibladzeCoeffLargeCats.djvu:file]]_ and linked it to [[crossed profunctor]].  Urs, how the integration approach to diff. forms fits with existance of classes of smooth, $C^1$-only, $L^1$-integrable etc. differential forms and the currents ("differential form-valued distributions"), and it seems it puts n-forms on n-manifolds in special position, than say k-forms on n-manifolds. There is a subject of geometric integration theory where integrability is related to geometric properties like rectifiability (Federer); how this fits with that. And finally with differential forms on singular varieties. It seems to me that this approach has advantages and applicability in some cases, while the easy approach via dualizing vector fields to get 1-forms and then proceeding algebraically in others. One should maybe also compare to Lurie's usage of cotangent bundle in expressing an alternative approach to higher descent. 

  * [[Urs Schreiber]]: there are many aspects to this, but what I wrote lives in the entirely smooth context. The integration map is that from Reyes-Moerdijk section 4 , which integrates "synthetic" forms over "synthetic" simplices. Technique-wise this is really rather conservative, the only new twist to it is that I am saying: its helpful to arrange some objects that people consider in the synthetic context into cosimplicial objects, that reveals some nice underlying structure.

* [[Urs Schreiber]]: 

  *  created [[(infinity,1)-quantity]] -- some comments:

     * this accompanies a blog question [here](http://golem.ph.utexas.edu/category/2009/08/question_on_synthetic_differen.html)

     * among other things this aims to provide the full general nonsense $\infty$-version of the statement at the beginning of [[differential form]]

     * I could move this to my private web. Let me know if you feel that would be better.

* [[Zoran Škoda]]: created [[crossed profunctor]] (of crossed modules) and [[butterfly]] (papillon). First after M. Jibladze (1990) and second after B. Noohi (2005). I did not draw the diagram but wrote equations explicitly.
* [[Eric]]:

  * Gleefully responded to John's gleeful response on [[directed graph]]. Note: I need to learn about this 'resolution' stuff.

* [[Zoran Škoda]]: created [[reconstruction theorem]]. There should eventually be separate entries for each of the main classes and examples, which are listed in the main entry.

* [[John Baez]]: I love the idea of an article full of [[reconstruction theorems]]!  I contributed one, perhaps not quite the sort Zoran was thinking --- but I just happened to have it on hand, and I think with some work one can see that it's part of the big family of Tannaka--Krein-like results.  By the way, I took a course with Kazhdan in which he went through tons of Tannaka--Krein--like theorems, but I've been unable to find my notes from that course!  He started with a very primitive (and thus important) result saying something like this: any $k$-linear abelian category with a faithful functor to $FinVect_k$ is equivalent to the category of finite-dimensional representations of some coalgebra.  Does anyone know a reference to this sort of theorem?  It's crucial that we use _co_algebras here.

* [[Urs Schreiber]]: 

  * added something on the dual Dold-Kan correspondence relating _co_ -chain complexes and co-simplicial abelian groups to [[Dold-Kan correspondence]].

  * renamed differentials at [[chain complex]] from "$d$" to "$\partial$"

  * expanded [[cochain complex]]

  * created [[differential forms in synthetic differential geometry]] with two purposes: it reviews the definition found in the literature and then proposes a -- supposedly nicer -- reformulation

* [[Zoran Škoda]]: added a query in [[compact object]]: the stated characterization of categories of $R$-modules is known at least about 3 decades before Ginzburg's lectures. Maybe we should look into classical sources.
* [[John Baez]]: 

   * Added theorem characterizing categories of $R$-modules to [[compact object]].

   * Added same theorem and also the Mitchell embedding theorem to [[abelian category]].

   * Gleefully shot down an idea of Eric's over at [[directed graph]] --- but this idea can be resuscitated using the concept of 'resolution'.

* [[Sridhar Ramesh]] added a small note that [[Lawvere-Tierney topology|Lawvere-Tierney topologies]] are the same as (internal) closure operators on truth values (Being new here, I'm not exactly sure what the protocols are; in "Please log all your non-trivial changes", does "non-trivial" mean everything above, say, typo-correction?). I also observed, in the article on [[presheaf|presheaves]], that the representable presheaves on a category of presheaves are precisely those which turn colimits into limits (i.e., a functor of type $[C, Set]^{op} \to Set$ is representable just in case it is limit-preserving).

  * [[Urs Schreiber]]: I added a remark to the text above on what "non-trivial" means. Generally, I think you can't log too much of your activity here, just too little. So if in doubt whether anyone else might be interested in your changes or not, drop a note here.

*  [[John Baez]]: Welcome, Sridhar Ramesh!  I'd like to add: we are not trying to force you to do lots of bureaucratic work, so please don't feel we are _demanding_ you to log changes here.  If you make a change and feel too tired to log it here, we won't be mad at you.  We just _like_ to see changes here, even smallish ones.

* [[Eric]]: Asked a question of [[Mike Shulman|Mike]] (or anyone else interested in SDG) at [[synthetic differential geometry]].

## 2009-08-01

*  [[Sridhar Ramesh]] has joined, editing [[module]] and [[Mitchell-Benabou language]] so far.

* [[Urs Schreiber]]: replied and reacted at  [[differential form]]

*  [[Toby Bartels]]:

   *  Archived the [[2009 July changes]].  (Check there if you missed some ... which you did, I promise.)
   *  More discussion with [[Rafael Borowiecki]] at [[category theory]].
   *  Answered one of two un-logged questions by [[Jim Stasheff]] at the bottom of [[Timeline of category theory and related mathematics]].
   *  Asked Urs a question at [[differential form]].


***

[[2008 changes|First list]] &#8212; [[2009 July changes|Previous list]] &#8212; No next list &#8212; **Current list**

***


category: meta

[[!redirects 2009 August changes]]
[[!include all changes]]

A list of all recently edited entries can be seen here:

* [Recently Revised](http://ncatlab.org/nlab/recently_revised).

But that list tends to contain lots of minor changes: it's not easy to spot the important ones.

So, if you feel people's attention should be drawn to some changes you make, please mention them *here*.  That will help [[Contributors|the rest of us]] spot them, so we can learn what you know --- and maybe make further improvements!

These comments should go in _reverse_ chronological order, so that the latest are on top of the list. To keep the list international, use the date in UTC (the date given by the server for your edits).

***


## 2009-07-13

*  [[Toby Bartels]]:
   *  Comments on [[Timeline of category theory and related mathematics]].
   *  Created [[opposite relation]], quite brief.

* [[David Roberts]]: Posted kernel of an idea at [[microbundle]] that has been sitting at the back of mind for a while, in the hope someone might be able to use it or do something interesting with it.

*  [[Toby Bartels]]:  Wrote [[subset collection]] (a [[foundations|foundational]] axiom of [[set theory]] intermediate between [[power set]]s and [[function set]]s, justified by [[type theory]] and strong enough to define the located Dedekind [[real number]]s).


## 2009-07-12

*  [[Toby Bartels]]:  Wrote [[sphere]] and [[pointed space]] to fill some gaps.  The former has a reference to (yet unwritten) [[Whitehead's theorem]] with the provacative claim that this shows that [[generalised (Eilenberg?Steenrod) homotopy theory]] is unnecessary; I don\'t really intend to defend that, but maybe it will interest the people working on that subject?

* [[Andrew Stacey]]: Started a discussion on the n-forum about how to get a snapshot of the n-lab (since this is really an announcement page rather than a discussion page).
Discussion is [here](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=42).

*  [[Toby Bartels]]:  Added some illustrations to [[simplicial set]], based on those at [[cubical set]], as requested by an [[InterestedAnonymousCoward]].

* [[Zoran ?koda]] created [[microbundle]]. Note that classical references do not mention morphisms, just isomorphisms or equivalences of microbundles. Did anybody notice my update downstairs on the issue of export_html (answer to Urs/Toby answers) ? I suggested that once a week an export_html be posted as a file to be downloaded which is not up-to-date with a warning, as I think (maybe I should be corrected) that Jacques stopped serving export_html because of long generation/compilation time, while static file and new cimpilation once a week will do less harm. And leave generation of export_markup as it is, up-to-date. 


## 2009-07-11

* [[Urs Schreiber|Urs]]:

  * branched off [[chain homology and cohomology]] from [[cohomology]], prodded by the blog discussion [here](http://golem.ph.utexas.edu/category/2009/06/cohomology_and_homotopy.html#c025198) -- but left somewhat unfinished as I need to run

*  [[Toby Bartels]]:

   *  Another tip for Zoran:  If $\sqrt{\frac{a}{b}}$ looks bad, then the problem is on your end.  To be sure, it looks bad to me too, but that problem is on my end; it looks good if I use the STIX fonts (as discussed [here](http://golem.ph.utexas.edu/instiki/show/Browsers/)), but I think that those are otherwise pretty ugly, so I don\'t use them.  So the problem is that almost every font doesn\'t know how to do that sort of thing correctly ... but the MathML produced by Instiki is correct.  (Update:  Actually, that example looks just fine in DejaVu Serif too, but I remember that there are other examples that don\'t.)
   *  A question on terminology at [[replete subcategory]].  Possibly the answers should inform [[equivalence]].


## 2009-07-10

* [[Urs Schreiber|Urs]]:

  * added model category version to [[local object]]

  * added remark about relation of Quillen equivalences to the corresponding presented $(\infty,1)$-categories to [[presentable (infinity,1)-category]]

  * created [[combinatorial simplicial model category]]

  * created [[combinatorial model category]]

* [[Tim]]: I have started to reorganise some of the entries on Cech methods since David has started on [[homotopy (as an operation)]] and had an idea about [[Cech homotopy]].  I have encorporated a point made by [[Zoran ?koda|Zoran]] about the history of [[Cech methods]].

* [[Zoran ?koda]]: created a version (to be expanded) of [[Legendre polynomial]] and [[M M Postnikov]] and added references to [[Postnikov system]]. I think historically tower and system differed by inclusion of universal cohomological class representing the fibration into the notion of system (cf. Whitehead's big book, ch.9). This should be still noted: if one does not specify the cohomological class this is I think like missing the choice of isomorphism when the isomorphism exists. Technical issues: I encountered a problem that sqrt{fraction} puts sqrt only such that the numerator is under the root. I do not know how one should write correctly. Toby thank you for the tip for getting the SOURCE of old versions. I sometimes write some items partly motivated by need to have them for my students, and plan to incorporate something close to my version into student scripta. You are very knowledgable about wiki world. :) I was also trying to take the export of the whole nlab and succeeded to get the markupML version but not html: when asking nlab/export_html i get 403 FORBIDDEN message in my browser. 

  * [[Urs Schreiber]]: I also get this error message when trying to export the $n$Lab as html -- I remember the html export was particularly heavy on the server and maybe it was truned off in view of the server being a bit weak -- we are trying to move to a better host eventually

  *  _Toby_:  Yes, Jacques turned that off because it was such a load on the server; I expect that we can turn it on again when we get a better host.  In principle, you can get the HTML by exporting the source and compiling it on a local copy of Instiki, but of course you have to install Instiki to do that.  (Also note that you\'ll need the CSS files if you want the HTML to look the same, including fonts, query boxes, etc.)  And neither of these includes old versions; I think that Urs(?) is backing those up periodically in case the server crashes.

  * _Zoran_: could then somebody make one copy of html zip file 2-3 times a month ? It would not be updated but still it would be useful for browsing math when offline. If I get the zip-file I can put it online on my homepage. Or simply could Jacques put one zip file of export_html weekly with link and warning that it is not up-to-date; and for editing we can anywy use markup version. Then the server does not get heavy with generation, I think that probably generating, compiling all takes time, the shear downloading from time to time would maybe not burden the server ? 

* [[David Corfield|David]]: began an experiment on [[homotopy (as an operation)]] of dualizing the [[cohomology]] page. Began [[generalized (Eilenberg-Steenrod) homotopy]].

* [[Urs Schreiber]]:

  * rewrote the intro to [[Cech cohomology]] (see there) and started adding a list of examples for the abelian case: the standard series line bundles, line bundle gerbes, with connection, etc. -- but not well written at the moment and no effort to get signs straight

  * created [[nerve and realization]] in order to host Kan's general idea of how a functor into a category with colimits induces an adjoint pair of functors 

    * I think I know what I am doing, but I'd like to ask people like [[Tim Porter]] and [[Todd Trimble]] to have a critical look at it (where is [[Mike Shulman]]??) -- in particular at the moment I allowed myself to assume that we are copowered over the enriching category in order to get nice formulas, I wouldn't object if somebody finds the time to give the more general discussion

    * then of course I adjusted links and made some comments accordingly at [[nerve]], [[geometric realization]] and [[Dold-Kan correspondence]]

  * following [[Eric Forgy|Eric]]'s question I typed a quick reply into [[cohomology]] on how the ordinary notion of cohomology in cochain complexes is reproduced. In principle this gives all the necessary information, but I'll try to find the time later to give a long detailed exposition of how this basic important special case arises from the very general perspective

  * added an "Idea" section to the beginning of 
    [[Postnikov system in triangulated category]]

    * in the course of that I noticed that the sub-web of stable higher category links was lacking a bit of coherence.  I tried to improve the link lists at [[stable (infinity,1)-category]] a bit accordingly and also added an "Idea" piece with links to [[enhanced triangulated category]].

*  [[Toby Bartels]]:  A quick note:  I also have been changing `[[apple]]s` to `[[apples]]` but I will not do it now unless I have reason to think that it was written by someone who prefers `[[apples]]`.  In general, I do not edit matters of taste; I didn\'t know that this was a matter of taste, but now I do know that.  (Sometimes if I\'m changing something else, then I will change matters of taste at the same time, but only if I have substantially rewritten the sentence or if helps to standardise the notation and terminology.  And this does not qualify as notation and terminology.)  I\'m sorry if I caused offence, but please understand that I did not know that there was a difference of style.
   *  PS:  If Eric adds `[[!redirects apples]]` to the bottom of `[[apple]]`, then both `http://ncatlab.org/nlab/show/apple` and `http://ncatlab.org/nlab/show/apples` should work.  I will still add such redirects myself, for the benefit of the style preferred by Urs, Eric, and me; but I will no longer change styles in what Zoran has written.
   *  PPS:  To see the source of an old version of a page, hit **Back in time** until you find the right version (or try **History** to get a list of versions), then hit **Rollback** to see the source of that version.  After you\'ve copied the source, hit **Cancel** (or **Submit** if you really want to change it back to the old version).
   *  PPPS:  You can type <code>`[[apple]]s`</code> to get `[[apple]]s` if you find it convenient to do so.


## 2009-07-09

* [[Zoran ?koda|Zoran ?k]]oda: but the plurals are NOT there -- if I write <nowiki>[[apple]]s</nowiki> I did not use the code for plural. Let me clear the issue (I will write round brackets): Eric is doing TWO things 1) he is taking entry ((apple)) and adding the redirection instruction inside to allow for ((apples)). This creates one new version, not too bad, you consider this robust, I can tolerate it. 2) he is changing every occurence of my reference ((apple))s which used to be correct usage from within entries ((banana)), ((pear)), ((ananas)) and ((strawberry)) to new format ((apples)). This amounts to not allowing me to use legitimate ((apple))s from within ((bananas)). This second thing, unlike the first, I can not tolerate, as it has no rational explanation. I do not know if it is [[evil|good :)) ]].  

  * [[Eric]]: The fact that many items appear as <nowiki>[[apple]]s</nowiki> on the nLab is an artifact of the period prior to having redirects. Prior to having redirects, we'd have to write that as <nowiki>[[apple|apples]]</nowiki> to get it to render correctly which gets old after a while, so people naturally gravitated to the easier <nowiki>[[apple]]s</nowiki>. If we'd had redirects from the beginning, there would be a redirect at <nowiki>[[apple]]</nowiki> for <nowiki>[[apples]]</nowiki> and no one in their right mind would ever write <nowiki>[[apple]]s</nowiki> again (which is distracting to look at) if they could just write <nowiki>[[apples]]</nowiki> instead. I'm at a total loss as to why you oppose this. Currently, I am trying to reverse the damage so that we can make things cleaner from here. Whenever, I see "]]s", I instinctively change this to "s]]" and add a redirect if it doesn't exist. In time, this should work itself out and we should have plural redirects for most links that are commonly used. It would work itself even faster if people stopped writing "]]s" and used the plural link form instead.

  * Zoran: I disagree that for example I write <nowiki>[[apple]]s</nowiki> rather than <nowiki>[[apple|apples]]</nowiki> beause it is easier. I write it because the appearance of <nowiki>[[apple]]s</nowiki> I like more: it tells me by the color which part of the name is real URL (as I often type URL), plus I have no dislike for multicolored words. I will continue writing like that. If you like to write your way write, but leave my links the way they are. Otherwise I can not ENJOY writing. It takes sometimes the whole minute to reload the page and I often reload the page is somebody has changes it, and it disappoints if the change is a matter of taste, and is legitimate. Second there may be day when you will have no time to write redirects etc. and one will not memorize which redirects exist and which do not. If I write the way I do, I will never have problem with this. If I want a single-color appearance of the link for some reason, I do not mind writing it long way like <nowiki>[[apple|apples]]</nowiki>, it is about 2 seconds more, rather than spending far more time to check if there is a created redirect and wait half a minute to load the page, specially if in addition to slowness of the server I have my own internet connection problems what is very often.   

* [[Urs Schreiber]]

  * I started going a bit through the [[Timeline of category theory and related mathematics]] and added links to $n$Lab entries wherever I saw a possibility

    * in that context: I like what [[Eric Forgy|Eric]] is doing. It makes the linkage of the Lab more robust. For instance quite a few  of the Timeline's imported links _didn't_ break (while thousands broke) just because Eric had made sure that some plurals etc were recognized. 

* [[Zoran Skoda]] 

  * created [[Postnikov system in triangulated category]]

  * I STRONGLY disagree with creation of spurios PLURAL items when they are of NO use. Namely like Eric just created new version of [[bialgebra cocycle]] to say that it redirects [[bialgebra cocycles]], while it is simpler and better from memory point of view to write [[bialgebra cocycle]]s. Why having whole page archived and one more page to browse in history just to distiguish if s is before or after the brackets ?? Dear Eric we have thousands of items to enter and there will be thousands of new pages in future and why to increase entropy and spend yuor valuable time on this -- please take some book and help us entering something NEW and not messing with plurals and creating new versions for nothing. I have hard time browsing history when something is messed up and if I am going to spend it on such a nonsense than I will leave the idea to enter new items myself.  

    * [[Eric]]: Hi Zoran. By adding a redirect for plurals, we are not creating spurious pages (but we are creating spurious revisions, but I don't see that as a meaningful issue). In fact, my hope is that everyone will stop writing things like <nowiki>[[page]]s</nowiki> in favor of <nowiki>[[pages]]</nowiki> at which point I could stop correcting the links. Please see [[redirect]] for more information. Redirects are a very nice new feature of the nLab (partially motivated by your suggestions wrt symbolic links) and I hope they become a natural part of any contributors arsenal. PS: It is ironic that you complain about creating additional revisions when you just created a THIRD revision by changing my redirect BACK (???). PPS: A good place to discuss this and any other administrative issues is on the [n-forum](http://www.math.ntnu.no/~stacey/Vanilla/nForum/). That is a good place for such discussions and once a decision has been made about any issue, the conclusion will be placed on the brand new [nLab meta](http://ncatlab.org/nlabmeta/show/HomePage) site. We're working on decision making processes now and any feedback is more than welcome.

   * Zoran: look at my explanation few paragraphs above: I accept your creating redirects, but do not accept not allowing me having my own format of calling links within my own text. I changed your redirect back because I want to assert my right to have the link called any possible way I like it. It functions, it correctly displays and it si even more informative: ((apple))s tells you even the information that s is not the name of the page, and I often TYPE the URL name of the page rather than clicking on the link, because often because of slowness of the server working on laptop and desktop simultaneously. Of course this kind of strange usage is useful just for the author, but if I am in process of improving the page which i largely created i think I have the right for the convenience.

      * [[Eric]]: Hi Zoran. The nLab is a group effort, and as such, it has to have some rules and should probably have at least some (loose) sense of uniformity. I don't think it makes sense for Toby and I to be going around correcting links to have you change them back simply because you want assert yourself. The nLab is already MUCH looser than Wikipedia as far as standards and formats and I think that is a good thing, but I also think there should be some agreed upon "Matters of Style". I started a discussion on "Matters of Style" on the n-forum [here](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=41). We should probably discuss it there. Whatever we all decide on, then we can add a "Matters of Style" page to [nLab meta](http://ncatlab.org/nlabmeta/show/HomePage). Anyone reading this is more than welcome to voice their opinion, but once a "quorum" is met, I think we should establish a rule. In a bit, we may also want to remove this discussion from [[latest changes]] since this isn't what the page was intended for.

  * created [[bialgebra cocycle]], [[Drinfel'd twist]]

  * by the way how does one download the source of a previous version ? I sometimes create a page and then there are changes after and I want to have my file for other purposes with what I wrote and I do not know how to access it. 

* [[John Baez|John]] 

  * I did some work on the [[Timeline of category theory and related mathematics]], and proposed some new guidelines for how it should look. 

* [[Urs Schreiber|Urs]]

  * am working at [[Cech cohomology]] on the section "Abelian Cech cohomology" where my aim is to spell out a derivation of the standard Cech double complex from starting with the general definition of cohomology for the case that the coefficient object is in the image of the Dold-Kan map from chain complexes of sheaves to simplicial sheaves -- I am not really satisfied, but this is how far I got -- check critically


## 2009-07-08

* [[Urs Schreiber]]:
 
  * added to [[nerve]] an "Idea" section and a further "examples"-section on nerves for chain complexes and the relation to the Dold-Kan correspondence

  * after a bit of work and with a bit of luck, I found the old reference by Kan where the description of the Dold-Kan correspondence is given in terms of nerves -- this is the nice way to do it -- added that reference to the [[Dold-Kan correspondence]]

    * that reminds me that it would be nice if we eventually had an entry on that verey general nonsense behind nerves (or do we already have that somewhere?)

  * by coincidence I came across the old entry [[crossed module]] and noticed that there were meanwhile plenty of links to add to it -- so I did

  * added two further references, by Birgit Richter, on the ($\infty$-)monoidal structure of the Dold-Kan correspondence  to [[Dold-Kan correspondence]]

  * added a small section on and a link to [[matching family]] at [[sheafification]]

  * reorganized [[Dold-Kan correspondence]] in an attempt to make the material more systematic -- then I started adding a detailed def/lemma/theorem/proof list of the classical statement, but didn't get very far yet

  * made a remark at [[Timeline of category theory and related mathematics]]

  * pasted a blog comment by [[David Ben-Zvi]] into [[n-categorical physics]]

*  [[Zoran ?koda]]: created [[essential image]], added n-category generalization to [[replete subcategory]], additions to [[image]], [[model structure on chain complexes]], remark due Leinster to [[Gray-category]]; created [[matching family]] following mainly conventions in MacLane-Moerdijk. This last item surely overlaps with [[sheafification]] but the approach and exposition is rather different; created micro-entry [[maximal sieve]].  


## 2009-07-07

*  [[Toby Bartels]]:
   *  Gave Tim a link at [[category theory]].
   *  Started [[suspension]] to fill links.  (We already have [[reduced suspension]].  There\'s also a suspension defined at [[delooping]] which doesn\'t seem to be quite the same; what\'s the connection?)

      * [[Urs Schreiber|Urs]]: when passing from topological spaces to spectra, suspension of spaces becomes the suspension mentioned at delooping: that in a [[stable (infinity,1)-category]], I'd say

* [[David Corfield|David]]

  * added to [[co-H-space]]. It's not looking very much like a dual version of [[H-space]].

* [[Urs Schreiber|Urs]]

  * created [[Cech cover]] and [[Cech model structure on simplicial presheaves]]

    * in that context also rewrote and expanded the introduction at [[hypercover]] and included corresponding links at [[model structure on simplicial presheaves]].

  * I notice that [[Timeline of category theory and related mathematics]] is a renamed version of the original Sandbox(!). (As you can see by clicking on its "history" link. But also the current [[Sandbox]]'s very first link claims to lead to the historical Sandbox, but takes on to the Sandbox poage with title "Timeline of category theory-...") I guess that's not intended. 

    *  This came about because [[Rafael Borowiecki]] created the [[Timeline of category theory and related mathematics|Timeline]] by moving the [[Sandbox]] instead of as a new page.  So I was faced with the choice to move it back and then create Rafael\'s page properly or to just recreate the Sandbox instead.  So I recreated the Sandbox but then put a note at the top in case anybody wants to see the history of that page, which is now at the [[Timeline of category theory and related mathematics|Timeline]].  (But now that it\'s been more than half an hour, I can remove that note; anyone looking through the history will still see it.)  ---Toby

  * tried to improve the exposition at [[groupoid object in an (infinity,1)-category]]. More to be done eventually, though.

* [[Eric]]

  * Reminds Urs that he no longer needs to type <nowiki>[[Urs Schreiber|Urs]]</nowiki> because there is now a redirect from [[Urs]] to [[Urs Schreiber]]., i.e. the link <nowiki>[[Urs]]</nowiki> points to [[Urs]]. Try it! :)

  * Along similar lines, after seeing <nowiki>[[internalization|internal to]]</nowiki> about a million times, I just added a redirect so that typing <nowiki>[[internal to]]</nowiki> gets redirected automatically to [[internal to]]. Try it! :)


## 2009-07-06

* [[Urs]]

  * replied to [[Toby Bartels|Toby]] at [[cogroup]] (yes, that wasn't so good) and to [[David Roberts|David R.]] at [[principal infinity-bundle]] (yes, that was a typo)

* [[Toby Bartels]]:

  * I would like to suggest that the appearance of links to nonexistent pages is a *feature* that we should not break.  Thus we should not create blank pages (or pages that are blank except for redirects) but instead create pages only when we have something to put there.  Conversely, we shouldn\'t change links to go to redirected forms (as at [[geometric infinity-function theory]] currently) unless the redirects have actually been created.  If this means that we have things like `[[∞-foo|infinity-foo]]` (when nobody has written about $\infty$-foos yet), then we\'re no worse off than before we had redirects, and the appearance of links to nonexistent pages still tells us something.  (Note: there is some related discussion now hidden under July 3.)

    * [[Eric]]: I agree that appearance of links to nonexistent pages is a **feature** that should not be broken. Currently, one of my self-assigned projects (a.k.a. a labor of love) is to pick a page and systematically "clean it". The last major cleaning was [[geometric ∞-function theory]]. I hope that for the most part (with some minor exceptions) most everyone would agree that it looks a lot better now. The issue that brought up your comment, however, came about as a result of me "cleaning" [[strict ∞-category]]. Part of my system for cleaning pages involves changing things like <nowiki>[[category|categories]]</nowiki> to simply <nowiki>[[categories]]</nowiki> and adding a redirect from [[categories]] to [[category]]. If I do this enough, then most n-Lab pages will have available redirects for plural forms of nouns. In fact, I would encourage everyone to stop including things like <nowiki>[[singular page name|plural page name]]</nowiki> and simply use the plural form <nowiki>[[plural page name]]</nowiki>. Then either leave the nonexistent link there for someone to add the redirect or add the [[redirect]] yourself. What happened on [[strict ∞-category]] was that there was a link <nowiki>[[exchange law|exchange laws]]</nowiki>. My "system" suggests that I change that to <nowiki>[[exchange laws]]</nowiki> and add a redirect from [[exchange laws]] to [[exchange law]]. In this rare case, [[exchange law]] did not exist yet, so I couldn't add a redirect without creating a blank page for [[exchange law]]. In this rare case, given that I am trying to systematically "clean" pages, I thought it was acceptable to break the rule about nonexistent pages. I still think it is justified as long as it doesn't become a habit, which I'm pretty sure it won't be.

  * A question at [[cogroup]] about what we really want there.  (Surely more than just the empty set?)

    * [[Urs Schreiber|Urs]]: we want to say that pointed _spheres_ are co-groups, so that maps out of them, called homotopy groups, are, well, groups. Supposed to be dual to the statement that mapping _into_ a group coefficient object gives [[cohomology group]]s

* [[Urs Schreiber|Urs]] 

  * added to [[principal bundle]] a long detailed section called "the $G$-action from the homotopy pullback" -- this may look like weird overkill, but the point is that this serves as a warmup for an analogous discussion at [[principal infinity-bundle]]

  * rediscovered that we had an entry [[Cech methods]] and added lots of links to that

  * provided explicit details at [[Cech cohomology]] for the general (nonabelian) case in low degree

* [[Zoran ?koda]]: created [[small fibration]], added more general discussion on [[endomorphism monoids]]. 

* [[Urs Schreiber|Urs]] created [[Cech cohomology]]

* [[David Corfield|David]]

  * more suggestions than changes, but it would be good to have entries for [[cogroup]] and [[co-H-space]]. Could [[homotopy group]] and [[cohomology group]] be made to resemble each other more? I.e., must the former be restricted to $n$-spheres as domain? Hmm, is something suboptimal about H-group and H-cogroup, whereas H-space and co-H-space? Perhaps 'co' and 'H' commute.

    * [[Urs Schreiber|Urs]]: it would in principle be good to have expositions at [[cohomology]], [[cohomology group]] and [[homotopy]], [[homotopy group]] be more symmetric -- we just have to beware that we'd be going into untrodden territory and should indicate accordingly: while generalized cohomologies of all sorts are becoming familiar, I can't recall having seen mentioned the corresponding dual notion of generalized homotopy anywhere but in our discussion -- so we should maybe tag the corresponding discussion, if we implrement it, with a box saying "this is research material" or the like -- but I would enjoy it if we did so

* [[Urs Schreiber|Urs]]

  * created [[groupoid object in an (infinity,1)-category]]

    * added a discussion of this at [[delooping]], a brief reference to it at [[quotient object]] and a link to it in the fourth $\inft$-Giraud-axiom at [[(infinity,1)-topos]]


## 2009-07-05

*  [[Toby Bartels]]:
   *  Mentioned [[endomorphism monoids]] too.
   *  Tried to give Tim some comfort at [[pseudofunctor]].

* [[Urs Schreiber]]

  * added a tiny bit of discussion to [[principal infinity-bundle]] about how the homotopy pullback definition gives the $G$-action and vice versa. But need to say more here.

    * By the way has anyone seen [[Mike Shulman|Mike]]? I know that he has thought about this, it's related to his [[michaelshulman:exactness hypothesis|exactness hypothesis]].


## 2009-07-04

*  [[Toby Bartels]]:  Mentioned [[automorphism groups]].

*  [[Tim]]: I have asked a silly question at [[pseudofunctor]], but would appreciate an answer. Can I make a plea to someone to provide a more detailed treatment of the Grothendieck construction as well. (I mean the one which is related to the pseudocolimit. At least a general reference to that should be in the entry.)

*  [[Toby Bartels]]:
   *  Put some stuff at [[equality]], but there is much more that could and should be said there.
   *  Added some pretty broad examples to [[evil]].

*  [[Tim]]: I have added new references to [[distributor]] and [[Grothendieck fibration]].

*  [[Toby Bartels]]:  Added a bit to the scandalously short page [[isomorphism]].


## 2009-07-03

*  [[Eric Forgy]] created [[exchange law]] blank (perhaps by accident?) and [[Toby Bartels]] wrote a very brief stub there.
   *  _Eric_: This was not an accident. I was cleaning some pages and wanted a redirect for [[exchange laws]], but [[exchange law]] did not exist yet, so I created it so I could insert a redirect assuming (correctly) that someone would fill in some content.
   *  _Toby_:  I wouldn\'t agree with your assumption.  What I wrote there is not very useful; if I\'d waited to write it by choice rather than by necessity, then I would have written rather more.

* [[Urs Schreiber|Urs]]

  * edited and expanded the link list at [[generalized smooth space]]

  * created [[smooth infinity-stack]] -- took the liberty of declaring this to be the term for "$\infty$-stacks on CartesianSpaces" 

    * see the example there to see the relevance of this, with an eye towards the discussion at [[principal 2-bundle]] and [[principal infinity-bundle]]

  * created [[smooth space]] -- took the liberty of declaring this to be the term for "sheaves on Diff" = "sheaves on CartesianSpaces". 

    * this way a "diffeological space" is precisely a "concrete smooth space" and I 

      * edited [[diffeological space]]

      * and created [[concrete sheaf]] (but [[concrete site]] still missing, and also maybe not the best definition at [[concrete sheaf]] yet)
  
      to make this statement.

*  [[Toby Bartels]]:  Created [[Cauchy sequence]] and [[complete space]], including brief references at the end of each to the relationship with [[Cauchy complete categories]].


## 2009-07-02

* [[Urs Schreiber|Urs]]

  * started a section "concrete realizations" at [[principal infinity-bundle]]. So far I recall the old result by Quillen on certain "1-categorica topological bundles" and their $\infty$-action groupoids. Then I start making some remarks on Jardine's approach using what he calls "diagrams" and have a remark on how that compares to the Bartels-Bakovi&cacute;-etc-style. This requires eventually much more discussion, but I have to call it quits for today. 

    But the point is that Jardine works in the "petit topos" perspective where all bundles live over the fixed site. So the terminal object in his setup is not the point, but the underlying space over which one works. This means that the simple picture of a principal $\infty$-bundle as the homotopy pullback of the point no longer works and is the reason why he introduces the yoga of what he calls "diagrams".

    On the other hand, when one works with simplicial sheaves in the context of a "gros topos" such as sheaves on $Diff$ or on open subsets of $\mathbb{R}^n$ or equivalent, then the simple conceptual picture remains valid. 

    Notice that placing oneself into the context of $n$-groupoids internal to diffeological spaces or the like is doing precissely this: working with simplicial sheaves on $Diff$.

    Evidently i shouldn't be discussing this here but in some entry. But it's time for me to go to bed now.

* [[Zoran ?koda]] created [[grouplike element]]. It contains few words on Amitsur complex for a coring with a (semi-)grouplike. The aim is to soon (using the setup) introduce entries for connections for corings; and then correpsondence between falt connections and descent data in the comonadic and coring setups (after Menini et al; all coming back to the example which is the correspondence between 1-order costratifications and flat connections in the crystalline setup due Grothendieck). 

* [[Urs Schreiber|Urs]]

  * started adding the discussion of the model given by (pre)sheaves with values in _simplicial groupoids_ to [[model structure on simplicial presheaves]] (contained in a new big diagram containing all Quillen equivalent models for $\infty$-sheaves)

    * in that context created [[model structure on presheaves of simplicial groupoids]]

* [[Zoran ?koda]] created [[coseparable coring]],[[Sweedler coring]], [[two dimensional sheaf theory]]; expanded [[stratifold]] (which was empty, but existing!), added a reference to [[fibration in a 2-category]] and somewhere else. I think that in K-theory delooping has a bit different multiple meanings which are related but are more procedures making from something what can not be delooped strictly in the sense of [[delooping]] to the delooping of something what is the best approximation of deloopable; there are procedures due to Quillen, Waldhausen, Karoubi etc. 

  * [[Urs Schreiber|Urs]]: the entry on [[two dimensional sheaf theory]] is motivated from some behind-the-scenes discussion Zoran and I are having -- Zoran rightly points out that the present characterization of [[derived stack]] may be wanting, as strictly speaking saying "derived stack" should be related to but not be regarded as equivalent to "higher stack on higher categorical site" -- what we really need eventually is more details on the To&#235;n-Vezzosi [work](http://www.math.uiuc.edu/K-theory/0579/) on higher topos theory in the context of SSet-enriched categories, 

* [[Urs Schreiber|Urs]] 

  * replied at [[delooping]]

* _[[Eric]]_: Added a redirect for [[Urs]] so that he no longer has to type <nowiki>[[Urs Schreiber|Urs]]</nowiki> and can simply type <nowiki>[[Urs]]</nowiki> and will be redirected to the correct page.


## 2009-07-01

* [[Urs Schreiber|Urs]]

  * proudly presenting what is now the widest (horizontally speaking) $n$Lab entry as yet: at [[model structure on simplicial presheaves]] I added a section "Map" where I draw a big diagram that indicates at least part of the collection of model structures, their interrelation, definition and authors

    *  Yeah, I was thinking of reworking that map to run vertically ....  ---Toby

    *  Would that really be better, though? Optimally, eventually we'd produce a LaTeXed pdf diagram. Here and elsewhere. That, however, inhibits joint editing a bit. ---Urs

  * replied at [[delooping]], at [[group]], added a bit at [[Notation]]

  * moved the key statement of [[Toby Bartels|Toby]]'s remark to the very beginning of [[group]] 

*  [[Toby Bartels]]:
   *  [[Andrew Stacey]] may be interested to see how I\'ve changed the formatting of the goal box at [[Froelicher space]].
   *  Incorporated Zoran\'s new references at [[principal 2-bundle]] into the text.
   *  Added a note at [[group]] how $Grp$ is a full sub-$2$-category of $Grpd_*$ (even though not of $Grpd$).

* [[Urs Schreiber|Urs]]

  * expanded at [[group]] on the statement that "a group is a groupoid with a single object"

  * added to [[loop space object]] the true definition, added also an "idea" section, links to related entries and an introductory blurb to the original material

  * created [[delooping]] for the matter discussed by [[Eric Forgy|Eric]] and [[Toby Bartels|Toby]] at [[Dijkgraaf-Witten theory]]

  * added Jardine-Luo reference to [[principal 2-bundle]] and [[principal infinity-bundle]]

  * added to [[Froelicher space]] an "Idea" and a "Reference" section, prompoted by the blog entry [here](http://golem.ph.utexas.edu/category/2009/07/laubinger_on_lie_algebras_for.html)

*  [[Toby Bartels]]:
   *  I archived the [[2009 June changes]] by the sneaky method of changing this page\'s name, copying the header and footer text (with appropriate changes) from the previous archive, and then creating this page anew.  Maybe that will keep us from testing Instiki\'s tolerance for pages with thousands of edits in their history.  (^_^)
   *  I\'ve completed migrating all old redirect pages to history pages; all links within the body of the Lab should now take you immediately to the target page.  (There are a few victims of a bug, but I\'ll straighten that out with Jacques.)  I have [more comments](http://www.math.ntnu.no/~stacey/Vanilla/nForum/comments.php?DiscussionID=39) on the Forum.


***

[[2008 changes|First list]] &#8212; [[2009 June changes|Previous list]] &#8212; No next list &#8212; **Current list**

***


category: meta

[[!redirects 2009 July changes]]
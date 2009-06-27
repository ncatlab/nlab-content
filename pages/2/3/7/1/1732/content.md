
This entry is about the book

* [[John Baez]], [[Peter May]], _Approaching [[higher category theory|Higher Category Theory]]_ .

The following reproduces 

* preface

* list of references

from that book, equipped with hyperlinks.

***


**Dedicated to Max Kelly, June 5 1930 to January 26 2007**


#Preface#

This is _not_ a proceedings of the 2004 conference 
"[[n-category|n-Categories]]: Foundations and Applications"
that we organized and ran at the IMA during the two weeks 
June 7--18, 2004!  We thank all the participants for helping make
that a vibrant and inspiring occasion.  There has been a great deal
of work in [[higher category theory]] since then, but we still feel that 
it is not yet time to offer a volume devoted to the main topic of the 
conference.   At that time, we felt that we were at the
beginnings of a large new area of mathematics, but one with many different 
natural approaches in desperate need of integration into a
cohesive field.   We feel that way still.   

So, instead of an introduction to [[higher category theory]], 
we have decided to publish a series of papers that
provide useful _background_ for this subject.  This volume
is aimed towards the wider mathematical community, rather than those
knowledgeable in category theory and especially [[higher category theory]].  
We are particularly sensitive to the paucity of young Americans 
knowledgeable enough in the subject to be potential readers.   

The focus of the conference was on comparing the many approaches to
[[higher category theory]]. These approaches, as they existed at the time
of the conference, have been summarized by Leinster [Lein1] and by
Cheng and Lauda [ChLau].  The earliest was based on [[filtered simplicial set|filtered]]
[[simplicial set]]s.  It is due to Street [Str1, Str3] and is being
developed in detail by Verity [Verity1, Verity2, Verity3], with a
contribution by Gurski [Gur].  Another approach, called "[[opetope|opetopic]]''
since [[operad]]s were used to describe the [[geometric shapes for higher structures|shapes of diagrams]] used in the
theory, is due to Baez and Dolan [BD] and has been developed by
Leinster [Lein2], Cheng [Ch1, Ch2, Ch3, Ch4], and Makkai and his
collaborators [HMP,Makkai].  There is also a topologically motivated [[Trimble n-category|approach using]] [[operad]]s due to Trimble [Trimble], which has been
studied and generalized by Cheng and Gurski [Ch5, ChGur].  There is a
quite different and more extensively developed operadic approach to
[[weak omega-category|weak infinity-categories]] due to Batanin [Bat1, Str2], with a variant
due to Leinster [Lein3].  Penon [Penon] gave a related, very compact
definition of $\infty$-category; a modified version correcting a small
but critical flaw has been proposed by Cheng and Makkai [ChMakkai].
Another highly developed approach, based on [[n-fold Segal space|n-fold]] [[simplicial set]]s
and inspired by work of Segal in infinite loop space theory, is due to
Tamsamani and Simpson [Simpson1, Simpson2, Simpson3, Simpson4, Tam1].
Yet another theory, due to Joyal [Berger1,Joyal], is based on a
[[presheaf]] category called the category of "theta-sets".  Also, Lurie
[Lurie3] has begun making extensive use of [[n-fold complete Segal space|Barwick's approach]] to
[[(infinity,n)-category|(infinity,n)-categories]], which are roughly weak $\infty$-categories
where [[(n,r)-category|all morphisms above dimension $n$ are invertible]].

The theme of the 2004 conference was comparisons among all these
approaches to higher categories --- or at least, those that existed at
the time.  While there are papers that tackle aspects of this immense
unification project [Berger2, Ch3, Ch5, Simpson5], it is still quite
unclear how a unified theory of higher categories will evolve.  In
proposing the conference, we wrote as follows: "It is <i>not</i> to be
expected that a single all embracing definition that is equally suited
for all purposes will emerge.  It is not a question as to whether or
not a good definition exists.  Not one, but many, good definitions
already do exist, although they have been worked out to varying
degrees.  There is growing general agreement on the basic desiderata
of a good definition of [[n-category]], but there does not yet exist an
axiomatization, and there are grounds for believing that only a
partial axiomatization may be in the cards.''

One can make analogies with many other areas where a number of
interrelated definitions exist.  In [[algebraic topology]], there are
various [[symmetric monoidal category|symmetric monoidal]] [[category of spectra|categories of]] [[spectrum|spectra]], and they are related
by a web of [[Quillen equivalence]]s of model categories.  In this
context, all theories are in some sense "the same'', but the
applications require use of different models: many things that can be
proven in one model cannot easily be proven in another [May].
In [[algebraic geometry]], there are many different [[cohomology]] theories,
definitely not all the same, but connected by various comparison
functors.  [[pure motive|Motivic theory]] is in part a search for a universal source
of such comparisons.

In the case of weak $n$-categories, it is unclear whether there is a
useful sense in which all known theories are the same.  We do not have
a complete web of comparison maps relating different theories.  Nor
are we sure what it _means_ for two theories to be "the
same", despite important insights by Grothendieck [Gro]
and Makkai [Makkai2].  The terms in which comparisons should be
made are not yet clear.  Quillen [[model category]] theory should capture
some comparisons, but it may be too coarse to give the complete story.
A smaller related theme of the conference was that there should be a
"baby'' comparison project, for which [[model category]] theory would in
fact be sufficient.  Precisely, the idea was that there should be a
web of Quillen equivalences among the various notions of [[(infinity,1)-category]].  These include topologically or [[simplicially enriched category|simplicially enriched categories]], [[Segal category|Segal categories]], [[complete Segal space]]]s, and
[[quasi-category|quasi-categories]].  In the years since the conference, this comparison
project has been largely completed by Bergner [Be1, Be2] and Joyal and
Tierney [JT].

Another smaller related theme was the [[homotopy hypothesis|higher categorical modelling of]]
[[homotopy n-type|n-types]] of [[topological space]]s.  It was a [[Pursuing Stacks|dream of Grothendieck]]
[Gro] that weak [[n-groupoid]]s should model [[homotopy n-type|n-types]].  The
[[algebraic definition of higher category|algebraic model]] [[homotopy hypothesis|of n-types due to Loday]] [Loday] is one
implementation of this idea.  More recently we are seeing attempts to
implement Grothendieck's idea in various approaches to $n$-categories
[Bat2, Bat3, Tam2, Cisinski].  There is also a large body of work on 
simpler $n$-categorical structures, such as 
[[strict omega-groupoid|"strict" n-groupoids]], that
capture only part of the information in a homotopy $n$-type.  The 
prime mover of this line of work is Brown [BHS].

As mentioned, the goal of this volume is merely to prepare the reader
for more detailed study of these fast-moving topics.  So, we begin
with a light-hearted paper that treats 
[[Pursuing Stacks|Grothendieck's dream]] as a
starting-point for speculations on the relationship between
$n$-categories and [[cohomology]].  It is based on notes that 
[[Mike Shulman|Michael Shulman]] took of [[John Baez]]'s 
[2007 Namboodiri Lectures at Chicago]().
Higher category theory has largely developed from a series of
analogies with and potential applications to other subjects, including
[[algebraic topology]], [[algebraic geometry]], [[physics|mathematical physics]], computer
science, [[logic]], and, of course, [[category theory]].  This paper
illustrates this, and raises the challenge of formalizing the patterns 
that become visible thereby.

The second paper, by Julie Bergner, is a survey of
[[(infinity,1)-category|(infinity,1)-categories]].  She begins by describing four approaches:
[[simplicially enriched category|simplicial categories]], [[complete Segal space]]s, [[Segal category|Segal categories]] and
[[quasi-category|quasi-categories]].  Then she describes the network of [[Quillen equivalence]]s relating these: the "baby comparison project" 
mentioned above.

The third paper, by Simona Paoli, focuses on a number of 
algebraic ways of modelling [[homotopy n-type|n-types]] of [[topological space]]s in terms of strict categorical structures.  Her focus 
is on the role of [[internalization|"internal" structures]] in [[higher category theory]], 
that is, structures that live in categories other than the [[Set|category of sets]].  She surveys the known comparisons among such 
[[algebraic definition of higher category|algebraic models for n-types]].  It is a part of the comparison
project to relate various notions of [[infinity-groupoid|weak n-groupoid]] to these strict
algebraic models for topological $n$-types. 

Logically, we might next delve into various approaches to
$n$-categories and full-fledged [[omega-category|infinity-categories]].  But this seems
premature.  So instead, the rest of the volume goes back to the
beginnings of the subject.  By now every well-educated young
mathematician can be expected to be familiar with [[category|categories]], as
introduced by Eilenberg and Mac Lane in 1945.  It has taken longer to
understand that what they introduced was a [[2-category]]: [[Cat]], with
[[category|categories]] as objects, [[functor]]s as morphisms, and 
[[natural transformation]]s as 2-morphisms.  Ehresmann [Ehresmann] introduced
[[omega-category|strict n-categories]] sometime in the 1960's, and Eilenberg and Kelly
discussed them in 1965 [EK], with [[Cat]] as a key example of a
strict [[2-category]].  B&eacute;nabou introduced the more general weak
$2$-categories or "[[bicategory|bicategories]]" the following year [Benabou].  But
even today, the mathematics of 2-categories is considered somewhat
recondite, even by many mathematicians who implicitly use these
structures all the time.  There is a great deal of basic [[2-category]]
theory that can illuminate everyday mathematics.  The second author
rediscovered a chunk of this while writing a book on parametrized
[[homotopy theory]] [MS], and he was chastened to see how little he knew
of something that was so very basic to his own work.

For this reason, the next paper is the longest in this volume: a 
thorough introduction to the theory of $2$-categories, by Stephen Lack.  
This paper gives a solid grounding for anyone who wants some idea of what
lies beyond mere categories and how to work with higher categorical
notions.  Anybody interested in higher category theory must learn
something of the richness of $2$-categories.

Lawrence Breen's paper, on [[gerbe]]s and [[principal infinity-bundle|2-gerbe]]s, gives an idea of how
naturally $2$-categorical algebra arises in the study of algebraic and
[[differential geometry]].  His paper also illustrates the need for
"[[enriched category theory|enriched]]" higher category theory, in which one deals with hom
objects that have more structure than is seen in merely set-based categories.  Many more such applications could be cited.

Stephen Lack is an Australian, and it is noteworthy that the premier
world center for category theory has long been Sydney.  We have
dedicated this volume to Max Kelly, the founder of the Australian
school of category theory, who died in 2007.  Kelly visited Chicago in
1970-71, just before becoming Chair of the Department of Mathematics
at Sydney.  That was long before e-mail, and Max was considering how
best to build up a department that would necessarily suffer from a
significant degree of isolation.  He decided to focus in large part on
the development of his own subject, and he succeeded admirably.  The
final paper in this volume, by  Kelly's student Ross Street, gives a 
fascinating mathematical and personal account of the development of higher 
category theory in Australia.

We had very much hoped to include a survey by Andr&eacute; Joyal of his
important work on [[quasi-category|quasi-categories]].  As shown in the work of [[Jacob Lurie|Lurie]]
[[Higher Topos Theory|Lurie1]], [[higher algebra|Lurie2]], these give probably the most tractable model of
[[(infinity,1)-category|(infinity,1)-categories]].  Joyal's work showing that one "can do
category theory" in quasi-categories is an essential precursor to
Lurie's work and is unquestionably one of the most important recent
developments in higher category theory.  However, Joyal's survey is
not yet complete: it has grown to hefty proportions and is still
growing.  So, it will appear separately.  

#References#


* [BD1]
  [[John Baez|J. Baez]] and [[James Dolan|J. Dolan]], 
  _Higher-dimensional algebra III: $n$-categories and the   
  algebra of opetopes,
  Adv. Math. **135** (1998), 
  145--206.
  ([arXiv](http://arxiv.org/abs/q-alg/9702014))

* [Bat1]
  M. Batanin, 
  _Monoidal globular categories as natural environment for the theory of weak $n$-categories,_
  Adv. Math. **136** (1998), 39--103.

* [Bat2] 
  M. Batanin, 
  _The Eckmann--Hilton argument, higher 
operads and $E_n$-spaces._  ([arXiv](arXiv:math/0207281))

* [Bat3] 
  M. Batanin, 
  _The combinatorics of iterated
loop spaces._  ([arXiv](http://arxiv.org/abs/math/0301221))

* [Benabou] 
  J. B&eacute;nabou, 
  _Introduction to bicategories,_ 
  in _Reports of the Midwest Category Seminar_ , 
  Springer, Berlin, 1967, pp. 1--77.

* [Berger1] 
  C. Berger, 
  _Iterated wreath product of the simplex
  category and iterated loop spaces_ 
  Adv. Math. **213**
  (2007), 230--270.  
  ([arXiv](http://arxiv.org/abs/math/0512575))

* [Berger2] 
  C. Berger, 
  _A cellular nerve for higher categories, 
  Adv. Math. **169** (2002), 118--175.  
  ([web]("http://math.ucr.edu.fr/~cberger/))

* [Be1] 
  J. Bergner, 
  _A model category structure on the category of 
simplicial categories_, 
  Trans. Amer. Math. Soc. **359**  (2007), 2043-2058.  
  ([arXiv](http://arxiv.org/abs/math/0406507))

* [Be2] 
  J. Bergner, 
  _Three models of the homotopy theory
of homotopy theory_ , 
  Topology **46** (2006), 
1925--1955.  
  ([arXiv](http://arxiv.org/abs/math/0504334))

* [BHS] 
  R. Brown, P. Higgins and R. Sivera, 
  _[[nonabelian algebraic topology|Nonabelian
Algebraic Topology]]: Higher Homotopy Groupoids of Filtered Spaces_
  ([web](http://www.bangor.ac.uk/~mas010/nonab-a-t.html))

...


#Blog discussion#

* [This Book Needs a Title](http://golem.ph.utexas.edu/category/2009/06/this_book_needs_a_title.html)


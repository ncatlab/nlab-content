[[!redirects Bill Lawvere]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Overview

> Talking with Bill, I often feel like a fly buzzing around a cow. (It seems to me I can liken Bill to a cow, if I'm just a fly myself.) On any easy question, I'll probably see the answer first. But his thoughts seem to move on a level where I don't function, I can barely see down there. (From an [interview](http://at.yorku.ca/t/o/p/c/06.htm) with [[John Isbell]].)

F. William Lawvere 

* ([web site](http://www.acsu.buffalo.edu/~wlawvere/), [Wikipedia entry](http://en.wikipedia.org/wiki/William_Lawvere))

is an influential [[category theory|category theorist]].

See 

* {#Interview07} _An interview with F. William Lawvere_, [Bulletin of the International Center for Mathematics](http://www.cim.pt/?q=publications) ([part 1, December 2007](http://www.cim.pt/files/publications/b23www.pdf), [part 2, June 2008](http://www.cim.pt/files/publications/b24www.pdf),  [full pdf](http://www.mat.uc.pt/~picado/lawvere/interview.pdf), [[LawvereInterview.pdf:file]])

for a survey of his academic path and work. See also

* Interview by Felice Cardone, March 2013 ([link](https://dl.dropboxusercontent.com/u/92056191/Archive/temporary_new_material/lawvere-cardone-2000.html))

for an interview on his contributions to [[categorical logic]].

For a (somewhat random) list of further links see also at "[conceptual mathematics](http://conceptualmathematics.wordpress.com/2013/02/09/happy-birthday-professor-f-william-lawvere/)".


## Topics

### Main contributions

Lawvere invented [[categorical logic]] and introduced the eponymous [[Lawvere theories]] as a [[category theory|category-theoretic]] way to describe finitary [[algebraic theories]].  He generalised [[Grothendieck toposes]] to [[elementary toposes]], revolutionising the [[foundations]] of [[mathematics]]; in this vein, he developed the [[foundation]] in [[structural set theory]] called [[ETCS]].  He also introduced and worked on [[synthetic differential geometry]] as a foundation for [[differential geometry]] and [[equations of motion]] in [[continuum physics]]. Later he introduced the notion of _[[cohesive topos]]_ as a more general foundation of [[geometry]]. 




### Mathematics relating to Physics
 {#MotivationFromFoundationsOfPhysics}

A central motivation for Lawvere's work is the search for a good  mathematical [[foundations]] of [[physics]], specifically of ([[classical physics|classical]]) [[continuum mechanics]] (or at least some [[kinematics|kinematical]] aspects thereof, Lawvere does not seem to mention [[Hamiltonians]], [[Lagrangians]] or [[action functionals]]).

In ([interview, p. 8](http://www.mat.uc.pt/~picado/lawvere/interview.pdf)) he recalls:

> I had been a student at Indiana University from 1955 to January 1960. I liked [[experiment|experimental]] [[physics]] but did not appreciate the imprecise reasoning in some theoretical courses. So I decided to study [[mathematics]] first. [[Clifford Truesdell|Truesdell]] was at the Mathematics Department but he had a great knowledge in Engineering Physics. He took charge of my education there. $[...]$ in 1955 (and subsequently) had advised me on pursuing the study of [[continuum mechanics]] and [[kinetic theory]]. 

> In Summer 1958 I studied [[topological dynamics|Topological Dynamics]] with George Whaples, with the agenda of understanding as much as possible in categorical terms.  $[...]$ Categories would clearly be important for simplifying the foundations of [[continuum physics]]. I concluded that I would make category theory a central line of my study. 

Then in ([interview, p. 11](http://www.mat.uc.pt/~picado/lawvere/interview.pdf)) about the early 1960s:

> I felt a strong need to learn more [[set theory]] and [[logic]] from experts in that field, still of course with the aim of clarifying the foundations of [[category theory]] and of [[physics]].

The title of the early text _[[Toposes of laws of motion]]_, which is often cited as the text introducing [[synthetic differential geometry]], clearly witnesses the origin and motivation of these ideas in [[classical mechanics]].


On this, in ([interview, p. 15](http://www.mat.uc.pt/~picado/lawvere/interview.pdf)):


> Q: As an assistant professor in Chicago, in 1967, you taught with Mac Lane a course on [[mechanics|Mechanics]], where you "started to think about the justification of older intuitive methods in geometry" You called it "[[synthetic differential geometry]]". How did you arrive at the program of [[Categorical dynamics|Categorical Dynamics]] and [[synthetic differential geometry|Synthetic Differential Geometry]]?

> A: From January 1967 to August 1967 I was Assistant Professor at the University of Chicago. Mac Lane and I soon organized to teach a joint course based on Mackey's book "Mathematical Foundations of [[quantum mechanics|Quantum Mechanics]]". 

> Q: So, Mackey, a functional analyst from Harvard mainly concerned with the relationship between quantum mechanics and representation theory, had some relation to category theory.

Then ([interview, p. 16](http://www.mat.uc.pt/~picado/lawvere/interview.pdf)):

> Q: Back to the origins of Synthetic Differential Geometry, where did the idea of organizing such a joint course on Mechanics originate ? Apparently, Chandra had suggested that Saunders give some courses relevant to physics, and our joint course was the first of a sequence. Eventually Mac Lane gave a talk about the [[Hamilton-Jacobi equation]] at the Naval Academy in summer 1970 that was published in the American Mathematical Monthly

> A: $[...]$ I began to apply the Grothendieck topos theory that I had learned from Gabriel to the problem of simplied foundations of [[continuum mechanics]] as it had been inspired by [[Clifford Truesdell|Truesdell]]'s teachings, [[Walter Noll|Noll]]'s [[axiom|axiomatizations]], and by my 1958 efforts to render categorical the subject of [[topological dynamics]].

A review of this with more comments on more relations to physics is in the introduction to the book collection _[[Categories in Continuum Physics]]_, which is the proceedings of a meeting organized by Lawvere in 1982.

In the talk _[[Toposes of laws of motion]]_ in 1997, Lawvere starts with the following remark

> I read somewhere recently that the basic program of infinitesimal [[calculus]], [[continuum mechanics]], and [[differential geometry]] is that all the world can be reconstructed from the [[infinitesimal object|infinitely small]]. One may think this is not possible, but nonetheless it's certainly a program that has been very fruitful over the last 300 years. I think we are now finally in a position to actually make more explicit what that program amounts to.

> $[...]$ I think that on the basis of these developments we can focus on this question of making very explicit how [[continuum physics]] etc. can be built up mathematically from very simple ingredients.

In the same talk, a few lines later after discussion of [[infinitesimally thickened points]] $T$, it says:

> The basic [[spaces]] which are needed for [[functional analysis]] and theories of [[physical fields]] are thus in some sense available in any [[topos]] with a suitable [[object]] $T$.


In 2000 in the article _[[Comments on the development of topos theory]]_ Lawvere writes in the closing section 7 titled "From and to continuum physics":

> What was the impetus which demanded the simplification and generalization of [[Grothendieck]]'s concept of [[topos]], if indeed the application to [[logic]] and [[set theory]] were not decisive. $[...]$ My own motivation came from my earlier study of [[physics]]. The [[foundation]] of the [[continuum physics]] of general materials, in the spirit of [[Clifford Truesdell|Truesdell]], [[Walter Noll|Noll]] and others, involves powerful and clear physical ideas, which unfortunately have been submerged under a mathematical apparatus $[...]$. But, as Fichera $[25]$ lamented, all this apparatus gives often a very uncertain fit to the phenomena. The apparatus may well be helpful in the solution of certain problems, but can the problems themselves and the needed axioms be stated in a direct and clear manner? And might this not lead to a simpler, equally rigorous account? These were the questions to which I began to apply the [[topos]] method in my 1967 Chicago lectures $[$ _[[Categorical dynamics]]_ $]$. It was clear that work on the notion of topos itself would be needed to achieve the goal. I had spent 1961-62 with the Berkeley logicians, believing that listening to experts on [[foundations]] might be the road to clarifying foundational questions. 

> $[...]$ Several books treating the simplified [[topos theory]] ([[Sheaves in Geometry and Logic|MacLane-Moerdijk]] being the most recent and readable text), together with the three excellent books on [[synthetic differential geometry]] $[...]$ provide a solid basis on which further treatment of [[functional analysis]] and the needed development of [[continuum physics]] can be based.


The [Wikipedia entry](http://en.wikipedia.org/wiki/William_Lawvere) concludes:

> Lawvere continues to work on his 50-year quest for a rigorous flexible base for physical ideas, free of unnecessary analytic complications. 

See also at _[[higher category theory and physics]]_ for more on this.

### Mathematics relating to Philosophy
 {#RelationToPhilosophy}

Lawvere has proposed formalizations in [[category theory]], [[categorical logic]] and [[topos theory]] of concepts which are motivated from [[philosophy]], notably in [[Georg Hegel]]'s _[[Science of Logic]]_ (see there for more). This includes for instance definitions of concepts found there such as: 

* _[[objective and subjective logic]]_, _[[abstract general]]_, _[[concrete general]]_, _[[concrete particular]]_, _[[unity of opposites]]_, _[[Aufhebung]]_, _[[being]]_, _[[becoming]]_, _[[space and quantity]]_, _[[cohesion]]_, _[[intensive and extensive quantity]]_ 

(see the references in these entries for pointers).

In ([Lawvere 92](#Lawvere92)) it says:

> It is my belief that in the next decade and in the next century the technical advances forged by category theorists will be of value to dialectical philosophy, lending precise form with disputable mathematical models to ancient philosophical distinctions such as general vs. particular, objective vs. subjective, being vs. becoming, space vs. quantity, equality vs. difference, quantitative vs. qualitative etc. In turn the explicit attention by mathematicians to such philosophical questions is necessary to achieve the goal of making mathematics (and hence other sciences) more widely learnable and useable. Of course this will require that philosophers learn mathematics and that mathematicians learn philosophy.

A precursor to this undertaking is [[Hermann Grassmann]] with his _[[Ausdehnungslehre]]_ ([Lawvere 95](#Lawvere95)), see there for more.

## Talks, Lecture notes and Publications
 {#Talks}

The following is a list of texts by Lawvere, equipped with brief comments and hyperlinks to further material on the $n$Lab. See also the 

* [list of publications on Lawvere's website](http://www.acsu.buffalo.edu/~wlawvere/list.html)

and also this 

* [repository of Lawvere's publications](https://github.com/mattearnshaw/lawvere), made available by [[Matt Earnshaw]]. 

(Some of Lawvere's writings don't exist as published articles, but circulate in some form or other. Notably the "[[Archive for Mathematical Sciences & Philosophy]]" run by [[Michael Wright]] has a lot of recordings or lectures by Lawvere, though presently few or none of the files in the archive are available online.)

* _[[Functorial Semantics of Algebraic Theories]]_ Originally published as: Ph.D. thesis, Columbia University, 1963 and
in Reports of the Midwest Category Seminar II, 1968, 41-61, Republished in:
Reprints in Theory and Applications of Categories, No. 5 (2004) pp 1-121 ([tac](http://www.tac.mta.ca/tac/reprints/articles/5/tr5abs.html))

  (on [[algebraic theories]], now also called [[Lawvere theories]])

* _An elementary theory of the category of sets_, 1964, Proceedings of the National Academy of Science of the U.S.A 52, 1506-1511. Expanded version with commentary by [[Colin McLarty]] and the author in:
Reprints in Theory and Applications of Categories, No. 11 (2005) pp. 1-35 ([tac](http://www.tac.mta.ca/tac/reprints/articles/11/tr11abs.html))

   (Axiomatizing the category of sets; a summary is at [[ETCS]])

*  _The Category of Categories as a Foundation for Mathematics_ , pp.1-20 in Eilenberg, Harrison, MacLane, R&#246;hrl (eds.), _Proceedings of the Conference on Categorical Algebra - La Jolla 1965_, Springer Heidelberg 1966.

   (Axiomatizing the category of categories; a summary is at [[ETCC]])

* _[[Categorical dynamics]]_, 1967 Chicago lectures ([pdf](http://www.mat.uc.pt/~ct2011/abstracts/lawvere_w.pdf))

  _Categorical Dynamics Revisited_, talk at _Sets Within Geometry_, Nancy, France 26-29 July 2011 ([recording](https://www.youtube.com/watch?v=sXATg9_6iWE))

  (on [[synthetic differential geometry]] as a context for axiomatizing [[ordinary differential equations]] as they appear in [[classical physics]])


* {#AdjointnessInFoundations} _[[Adjointness in Foundations]]_, ([TAC](http://www.emis.de/journals/TAC/reprints/articles/16/tr16abs.html)), Dialectica 23 (1969), 281-296

  (on the interpretation of [[quantifiers]] in [[categorical logic]] as [[base change]] [[adjoints]])

*  _Equality in hyperdoctrines and comprehension schema as an adjoint functor_.  In A. Heller, ed., _Proc. New York Symp. on Applications of Categorical Algebra_, pp. 1--14.  AMS, 1970. ([[LawvereComprehension.pdf:file]])

    (on [[comprehension]] in [[hyperdoctrines]])

*  _Quantifiers and sheaves_, Actes, Congr&#232;s intern, math., 1970. Tome 1, p. 329 &#224; 334 ([pdf](https://pdfs.semanticscholar.org/6630/846a00261a071b71e264e0f532e29cd9152f.pdf))

    on [[geometric modalities]]/[[Lawvere-Tierney topology]] and [[universal quantifier|universal]]/[[existential quantifier|existential]] [[quantifiers]] related to [[dependent product]]/[[dependent sum]] further developed in:

*  _Equality in hyperdoctrines and
comprehension schema as an adjoint functor_, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970), 1-14.

* _Teoria delle categorie sopra un topos di base_, lecture notes from Perugia (1972--73) -- available online [here](https://github.com/mattearnshaw/lawvere/blob/master/pdfs/1972-perugia-lecture-notes.pdf)

    (on basic category theory, the [[category of sets]] and [[elementary toposes]], and an approach to [[indexed categories]])

* _Metric spaces, generalized logic and closed categories_ Reprints in Theory and Applications of Categories, No. 1 (2002) pp 1-37 ([tac](http://www.tac.mta.ca/tac/reprints/articles/1/tr1abs.html))

     (A classic text from 1973 on [[Cauchy complete categories]] and [[enriched category theory]])

* _Variable sets etendu and variable structure in topoi_ ,
Lecture notes University of Chicago 1975.

    (a review of topos theory: on structural sets, role of [[forcing]] and non-standard analysis and [[étendue]] toposes)

* _Variable quantities and variable structures in topoi_ , pp.101-131 in Heller, Tierney (eds.), Algebra, Topology and Category Theory, Academic Press New York 1976.

    (an important text for the Eilenberg-festschrift, reviews toposes in [[algebraic geometry]], first attention to [[gros topos]])

* _Topos-theoretic methods in geometry_, Aarhus 1997

* _Extensive and intensive quantities_ Workshop on Categorical Methods in Geometry, Aarhus 1983

  (a proposal for a general axiomatization of [[homotopy]]/[[homology]]-like "[[extensive]] quantities" and [[cohomology]]-like "[[intensive]] quantities")

* _State Categories, Closed Categories, and the Existence Semi-Continuous Entropy Functions_ , IMA reprint 86, 1984 ([pdf](http://www.ima.umn.edu/preprints/pp1984/86s.pdf))

* _Functional Remarks on the General Concept of Chaos_ , IMA reprint 87, 1984 ([pdf](http://www.ima.umn.edu/sites/default/files/87s.pdf))

  (on a formalization of the concept of [[chaos]])

* _Toward the description in a smooth topos of the dynamically possible motions and deformations of a continuous body_, Cah.top.g&#233;o.diff.cat, 21 nr.4, 1980, pp.377-392 ([Numdam](http://www.numdam.org/item?id=CTGDC_1980__21_4_377_0))

   (contains a section with some remarks on Lagrangian mechanics)

* with [[Stephen Schanuel]], _[[Categories in Continuum Physics]]_, Lectures given at a Workshop held at SUNY, Buffalo 1982, Lecture Notes in Mathematics 1174, 1986

  (on [[continuum mechanics]], [[variational calculus]] and [[laws of motion]] in [[synthetic differential geometry]] and in [[diffeological spaces]] and [[Frölicher spaces]], and on [[intensive and extensive]] properties in terms of [[ring objects]] and [[modules]] in a [[topos]].)

* {#TakingCategoriesSeriously} _Taking categories seriously_, Reprints in Theory and Applications of Categories, No. 8, 2005, pp. 1&#8211;24. ([pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf))

  (reprint of a 1986 paper on the relevance of fundamental concepts in [[category theory]], such as [[Isbell duality]])
&#8206;

* _Categories of spaces may not be generalized spaces, as exemplified by directed graphs_, preprint, State University of New York at Buffalo, (1986) Reprints in Theory and Applications of Categories, No. 9, 2005, pp. 1&#8211;7 ([tac:tr9](http://www.tac.mta.ca/tac/reprints/articles/9/tr9abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/9/tr9.pdf))

  (on the notion of [[gros topos|gros toposes]], details of his claims are worked out at [[sufficiently cohesive topos]])

*   _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

     (Uses toposes of graphs to introduce his ideas on petit/gros toposes)

* _Display of graphics and their applications, as exemplified by 2-categories and the Hegelian "taco"_, Proceedings of the first international Conference on algebraic methodology and software technology University of Iowa, May 22-24 1989, Iowa City pp. 51-74 

  (on [[Aufhebung]], [[graphic category|graphic categories]], the [[Hegelian taco]]; the most explicit text with Lawvere's ideas on [[Hegel]])

* _More on graphic toposes_, Cah. Top. G&#233;om. Diff. Cat. **XXXII** no. 1 (1991) pp.5-10. ([Numdam](http://www.numdam.org/item?id=CTGDC_1991__32_1_5_0))

  (on [[graphic category|graphic categories]] and their presheaf categories)

* _[[Some Thoughts on the Future of Category Theory]]_ in A. Carboni, M. Pedicchio, G. Rosolini (eds.), _Category Theory_  , [[Como|Proceedings of the International Conference held in Como]], LNM **1488** Springer Heidelberg 1991.

  (on -- implicitly -- [[cohesive topos|cohesive toposes]]);

* with [[Stephen Schanuel]], _Conceptual Mathematics - A first  introduction to categories_ , Cambridge UP 1997.

  (first steps into category theory; the Spanish translation is available [here](http://www.acsu.buffalo.edu/~wlawvere/concep-3.pdf))

* {#Lawvere92} _Categories of space and quantity_ in: J. Echeverria et al (eds.), _The Space of mathematics_ , de Gruyter, Berlin, New York (1992)

  (on [[space and quantity]] and on formalizing concepts from [[philosophy]] as in the _[[Science of Logic]]_ in terms of [[category theory]] and [[categorical logic]])

* _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_ Philosophia Mathematica (3) Vol. 2 (1994), pp. 5-15. ([[LawvereCohesiveToposes.pdf:file]])
  
  (an early version of the notion of [[cohesive topos|cohesive toposes]])

* {#Lawvere94b} _[[Tools for the advancement of objective logic]]: closed categories and toposes_, in J. Macnamara and [[Gonzalo Reyes]] (Eds.), _The Logical Foundations of Cognition_, Oxford University Press 1993 (Proceedings of the Febr. 1991 Vancouver Conference "Logic and Cognition"),
pages 43-56, 1994.

  (on formalizing [[philosophy]] as in the _[[Science of Logic]]_ in terms of [[category theory]] and [[categorical logic]].) 

* {#Lawvere95} _A new branch of mathematics, "The Ausdehnungslehre of 1844," and other works. Open Court (1995), Translated by Lloyd C. Kannenberg, with foreword by Albert C. Lewis_, _Historia Mathematica Volume 32, Issue 1, February 2005, Pages 99&#8211;106_ ([publisher](http://www.sciencedirect.com/science/article/pii/S031508600400059X))

  (on [[Hermann Grassmann]]'s _[[Ausdehnungslehre]]_ and hence also on _[[extensive and intensive quantity]]_)

* _Grassmann's Dialectics and Category Theory_, in _Hermann G&#252;nther Gra&#223;mann (1809&#8211;1877): Visionary Mathematician, Scientist and Neohumanist Scholar_, Boston Studies in the Philosophy of Science Volume 187, 1996, pp 255-264 ([publisher](http://link.springer.com/chapter/10.1007%2F978-94-015-8753-2_21))

* _Volterra's functionals and covariant cohesion of space_ Perugia Studies in Mathematics (Proceedings of the May 1997 Meeting in Perugia) ([pdf](http://www.acsu.buffalo.edu/~wlawvere/Volterra.pdf))

  (with first remarks on [[cohesive topos|cohesion]])

* _[[Toposes of laws of motion]]_ , transcript of a talk in Montreal, Sept. 1997 ([pdf](http://www.acsu.buffalo.edu/~wlawvere/ToposMotion.pdf))

  (on the description of [[differential equations]] in terms of [[synthetic differential geometry]] and the notion of _[[toposes of laws of motion]]_)

* _Outline of synthetic differential geometry_ , seminar notes (1998) ([pdf](http://www.acsu.buffalo.edu/~wlawvere/SDG_Outline.pdf))

  (the origin of the concept of [[synthetic differential geometry]])

* _Kinship and Mathematical Categories_ , pp.411-425 in Jackendoff, Bloom, Wynn (eds.), _Language, Logic, and Concepts_ , MIT Press Cambridge 1999.

   (Lawvere's venture into anthropology; a summary is at [[kinship]]) 

* _[[Comments on the development of topos theory]]_ , pp.715-734 in Jean-Paul Pier (ed.), _Development of mathematics 1950-2000_, Birkh&#228;user Basel 2000.

     (review of the history of topos theory)

* _Linearization of graphic toposes via Coxeter groups_,  JPAA **168** (2002) pp. 425-436. ([pdf](http://www.sciencedirect.com/science/article/pii/S0022404901001074/pdfft?md5=a4ca9bc67df6ae63ddf53c559bd71315&pid=1-s2.0-S0022404901001074-main.pdf))

* _Categorical algebra for continuum micro physics_,  JPAA **175** (2002) pp. 267-287.  ([pdf](http://www.sciencedirect.com/science/article/pii/S002240490200138X/pdfft?md5=ebd435105778d597f25141bf065978e3&pid=1-s2.0-S002240490200138X-main.pdf))

*  _Foundations and Applications: Axiomatization and Education_, Bulletin of Symbolic Logic **9** no.2 (2003) pp.213-224. ([ps-preprint](https://www.math.ucla.edu/~asl/bsl/0902/0902-006.ps))

   (a review of (not only set-theoretic) foundations in mathematics)

* {#LawvereRosebrugh} with [[Robert Rosebrugh]], _[[Sets for Mathematics]]_ , Cambridge UP  2003. ([web](http://books.google.de/books?id=h3_7aZz9ZMoC&pg=PP1&dq=sets+for+mathematics))

  (on [[set theory]] from a practical [[category theory|theoretic]] point of view (informal [[ETCS]]))

* _Axiomatic cohesion_ ,Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

  (a more formal definition of [[cohesive topos|cohesive toposes]], [[sufficiently cohesive topos]] works out details of his claims concerning 'sufficient cohesion')  

* _[[Cohesive Toposes -- Combinatorial and Infinitesimal Cases]]_ , lecture in Como (2008)  

  (on [[cohesive topos|cohesive toposes]])

* _Open problems in topos theory_, April 2009 ([pdf](https://web.archive.org/web/20170421103453/http://cheng.staff.shef.ac.uk/pssl88/lawvere.pdf))

  (problem 7 presented there "The algebra of time", concerns the characterization of _[[Toposes of laws of motion]]_)

* _The Dialectic of the Continuous and the Discrete in the history of the struggle for a usable guide to mathematical thought_, talk at _Sets Within Geometry_, Nancy, France 26-29 July 2011 ([recording](https://www.youtube.com/watch?v=OE-R3565jrs))

* _What are Foundations of Geometry and Algebra_, Keynote lecture at the _[Fifty Years of Functorial Semantics](http://www.math.union.edu/~niefiels/13conference/Web/)_ conference, Union College, October 2013 ([recording](https://www.youtube.com/watch?v=ZYGyEPXu8as))

*  _Alexander Grothendieck and the Concept of Space_, address CT15 Aveiro 2016. ([link](http://www.acsu.buffalo.edu/~wlawvere/GrothendiekAveiro15.htm))

   (a talk given at CT15 reviewing 50 years of developments since the 1965 La Jolla conference)



category: people

[[!redirects William Lawvere]]
[[!redirects Lawvere]]
[[!redirects F. W. Lawvere]]
[[!redirects F.W. Lawvere]]
[[!redirects W. Lawvere]]
[[!redirects F. William Lawvere]] 
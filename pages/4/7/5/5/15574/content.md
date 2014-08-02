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
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

[[!redirects aufhebung]]
[[!redirects Aufhebungs relation]]

##Idea
_Aufhebung_ (sublation) is a central concept in the dialectical logic of the German philosopher G. W. F. Hegel. The German expression has several meanings for which _tollere, elevare, conservare_ would be Latin equivalents.[^fine] 

[^fine]: As this polysemy is important for the concept and difficult to preserve in translation we prefer to use the German term in the following.

In his quest to axiomatize the concepts of space and cohesion, [[F. W. Lawvere]] inspired by [[homotopy theory]] proposed a mathematical rendering of the _Aufhebungs_ relation within [[topos theory]]. It is the mathematical concept that will constitute the primary subject in the following.

##_Aufhebung_ in Hegel's 'Wissenschaft der Logik'

Although the two volumes of _'Wissenschaft der Logik'_ - Science of Logic (1st ed. 1812-1816) can be considered as one of the main texts of Hegel's philosophy they fell into disfavour in the second half of the 19th century and most of the 20th century, and accordingly received much less attention than the 'Ph&#228;nomenologie des Geistes' or the 'Rechtsphilosophie'. They shared this fate with Hegelian philosophy as a whole which apart from the philological interest it generated, was continued only through the political wing of Lefthegelianism which in either its existentialist interpretation by A. Koj&#232;ve or its Marxist interpretation by G. Luk&#225;cs openly rejected the concept of objective dialectics in nature thereby seriously severing the social thought from its broad foundation in ontology and logic, whereas the natural philosophical tradition in the vein of F. Engels petrified to the doctrines of dialectical materialism. 

The 'Wissenschaft der Logik' has to be viewed against the background of philosophy in the early 19th century: **Kant** had embarked on a project of 'refoundation', or rather demolition, of metaphysics from an epistemological perspective and this project had been pushed further by his followers especially Fichte in his _Wissensschaftslehre_. However critical these idealist systems had been to the claims of traditional metaphysics and epistemology they all left the traditional logic untouched and in this respect fell behind Leibniz. It is at this point where Hegel starts: he sets out to extend the critical examination of the foundations of knowledge to logic itself.

Heavily influenced by the transcendental deductions and the chapters on dialectical paralogisms in Kant's 'Kritik der reinen Vernunft' he intends to start from nothing and justify the autonomous development of the system of categories. Here dialectics and Aufhebung enter the picture as Hegel conceives the categories not only as not given apriorily but as actually  becoming: _logic ceases to be an inventory of categories but becomes a system of transformations of categories!_ (Had Eilenberg and MacLane in 1945 intended their terminological loans from philosophy as a kind of joke, Lawvere would 25 years later take this terminological proximity at face value.)

Hegels parts with the traditional conception mainly in two points: the foundations of his logic coalesce with ontology into an **objective logic** as the first part is titled (a 'logic of things' as [[Charles Sanders Peirce|C.S. Peirce]] would later put it), i.e. he rejects the subject as a possible ground for logic, and he reassesses the status of **negativity** or conflict-contradiction in logic. The cornerstone of the edifice is the anti-eleatic unity of being and nothingness in the idea of becoming. It is precisely this 'positively being negative' that finds its expression in the concept of 'Aufhebung'. 

A key passage on Aufhebung in 'Wissenschaft der Logik' comes at the end of the first chapter ([I.1.1Cc, p.113](#WdL)): after a deduction of the categories of 'being', 'nothingness', and their unity in 'becoming' Hegel determines **dialectics** as 'the higher rational movement... in which the precondition of the separatedness (of the seemingly separated) is lifted ( _sich aufhebt_ )' ([p.111](#WdL)).

He goes on ([p.113](#WdL)) to explicate _Aufheben_ as one of the most important concepts in all of philosophy that constantly recurs everywhere. The sublated - _das Aufgehobene_ is not nothing which is an _unmediated_, but is a mediated - _ein Vermitteltes_; it is nothing - _das Nichtseiende_, but as a result that originated from a being and therefore still carries with it the determination from which it derives. We see here how Hegel tries to combine Leibniz' identification of being with being determinate with Spinoza's 'omni determinatio est negatio': **Aufhebung** is the mode of this coexistence of negation-affirmation.

Clearly, these remarks can not do justice to the richness and subtlety of Hegel's logic and should only serve as canvas against which to get a better grasp of Lawvere's conceptual translation. The points to keep in mind from this view are:

* Aufhebung is a _pervasive_ concept: although Lawvere proposes only mathematical definitions for two terms of Hegel's logic, namely _unity of opposites_ and _Aufhebung_, these are in fact the key terms and go already far in a reconstruction of the whole edifice!

* Aufhebung unites _determinatedness_ with annihilation of being. These recur at the mathematical level as the correspondance between being-being a sheave, annihilation -being the adjoint opposite of sheaf (anti-sheaf), and the determination of Aufhebung as being the least (=the Leibnizian best) level of being simultaneously a sheaf and an anti-sheaf.

##Lawvere's path to _Aufhebung_

>In early 1985, while I was studying the foundations of homotopy theory, it occurred to me that the explicit use of a certain simple categorical structure might serve as a link between mathematics and philosophy. ([Lawvere 1996](#Lawvere96), p.167)

##The mathematics of _Aufhebung_

So now let's get down to business and do some mathematics!

### The mathematics of Yin and Yang

In ([Lawvere 2000](#Law00)) a particular simple example of the adjoint cylinder was suggested that we use in the following as a running thread.

Let $N$ be the natural numbers $\{0, 1,\dots\}$ viewed as a category via their usual ordering. Let $L,R:N\to N$ be the two parallel functors '_even_' and '_odd_' defined by $L(n):=2n$ and $R(n):=2n+1$.

Both are full and faithful, hence candidates for an adjoint cylinder, and so we look now for a third functor $N\to N$ which we will call $T$ in a clin d'oeil to [[Charles Sanders Peirce|C. S. Peirce's]] concept of _thirdness_, such that $L\dashv T\dashv R$.

For our simple poset example these adjunctions amount to $L(n)\leq m$ iff $n\leq T(m)$ and $n\leq R(m)$ iff $T(n)\leq m$. When such a $T$ exists it must satisfy $T\circ R \cong id\cong T\circ L$ which in our case just gives $T\circ R = id = T\circ L$, i.e. the thirdness $T$ mediates the _identity_ of $R$ and $S$. Spelled out this says $T(2n)=n$ and $T(2n+1)=n$ which we simply take as definition for $T$.

Here we also see how $T$ mediates the _opposition_ between $L$ and $R$ because in order for such a $T$ to exist the functors $L$ and $R$ must actually correspond to inclusions of _disjoint subcategories_ e.g. for $L(n)=2n$ and $G(n):=3n\quad$ $T$ would have to invert e.g. 6 to 2 and to 3 at the same time, which a function of course cannot do.

The _unity_ of the opposites is finally provided by the encompassing $N$ where they sit as subcategories of even and odd numbers.


##Related pages

* [[Science of Logic]]

* [[graphic category]]

* [[generic interval]]

* [[Pursuing stacks]]

##A Guide to the Literature

The book by [La Palme-Reyes-Zolfaghari (2004)](#RRZ04) provides a good entry to the mathematics of Lawvere from an elementary point of view and contains even a page on the adjoint cylinder.

Lawvere introduced the Hegelian concepts in Lawvere ([1989a](#Lawv89a),[1989b](#Law89b)). They get some attention in Lawvere ([1991](#Lawv91a),[1992](#Law92)) with the latter containing his 'philosophical program'. By all means have a look at [Lawvere (1996)](#Law96), this together with Lawvere ([1989a](#Lawv89a),[1999](#Law99)) exposes his ideas on homotopy theory. The  work on graphic toposes ([1989b](#Law89b),[1991b](#Law91b),[2002](#Law02)) concerns the _Aufhebungs_ relation. [Kelly-Lawvere (1989)](#KL89) provides the technical prerequisites on essential localizations for _Aufhebung_.

The known mathematical results on the Aufhebungs relation are contained in the paper by [Kennett-Riehl-Roy-Zaks (2010)](#KRRZ10) which is based on older phd-works by some of the authors.

Further results on essential localizations can be found in the papers by [Borceux-Korotenski (1991)](#BK91), [Johnstone (1996)](#JS96), [Vitale (2001)](#VT01) and [Lucyshyn-Wright (2011)](#LW11) or in [SGA 4](#SGA4).


##References

* {#SGA4} M.Artin, A.Grothendieck, J. L. Verdier (eds.) , _Th&#233;orie des Topos et Cohomolgie Etale des Sch&#233;mas - SGA 4_ , Springer LNM **269** Heidelberg 1972. (sec. IV 7.6., pp.414-416)

* [[John Baez|J.C. Baez]], [[Mike Shulman|M. Shulman]] , _Lectures on n-categories and cohomology_ , pp.1-68 in: J.C. Baez, P. May (eds.), _Towards Higher Categories_, Springer Heidelberg 2010. ([preprint](http://math.ucr.edu/home/baez/cohomology.pdf))
&#8206;
* {#BK91}[[Francis Borceux|F. Borceux]], M. Korostenski, _Open Localizations_ , JPAA **74** (1991) pp.229-238.

* J. Climent Vidal, J. Soliveres Tur, _Functors of Lindenbaum-Tarski, Schematic Interpretations, and Adjoint Cylinders between Sentential Logics_ , Notre Dame Journal of Formal Logic **49** no.2 (2008) pp.185-202. ([pdf](https://projecteuclid.org/download/pdfview_1/euclid.ndjfl/1210859927))
&#8206;
* {#WdL} G. W. F. Hegel, _Wissenschaft der Logik I_ , Suhrkamp Frankfurt 1986[1812/13; revised 1831].

* {#JS96}[[Peter Johnstone|P. Johnstone]], _Remarks on Quintessential and Persistent Localizations_ , TAC **2** no.8 (1996) pp.90-99. ([pdf](http://www.tac.mta.ca/tac/volumes/1996/n8/n8.pdf))

* {#KL89}[[G. M. Kelly]], F. W. Lawvere, _On the Complete Lattice of Essential Localizations_ , Bull.Soc.Math. de Belgique **XLI** (1989) pp.261-299.

* {#KRRZ10} C. Kennett, [[Emily Riehl|E. Riehl]], M. Roy, M. Zaks, _Levels in the toposes of simplicial sets and cubical sets_ , JPAA **215** no. 5 (2011) pp.949-961. ([preprint](http://arxiv.org/abs/1003.5944))

* {#RRZ04} M. La Palme Reyes, [[Gonzalo E. Reyes|G. E. Reyes]], H. Zolfaghari, _Generic Figures and their Glueings_ , Polimetrica Milano 2004.

* {#Law89a} F. W. Lawvere, _Qualitative Distinctions between some Toposes of Generalized Graphs_ , Cont. Math. **92** (1989) pp.261-299.

* {#Law89b} F. W. Lawvere, _Display of graphics and their applications, as exemplified by 2-categories and the Hegelian "taco"_ , Proceedings of the first international conference on algebraic methodology and software technology University of Iowa, May 22-24 1989, Iowa City, pp.51-74. 

* {#Law91a} F. W. Lawvere, _Some Thoughts on the Future of Category Theory_ , pp.1-13 in Springer LNM **1488** (1991).

* {#Law91b} F. W. Lawvere, _More on Graphic Toposes_ , Cah.Top.G&#233;om.Diff.Cat. **XXXII** no. 1 (1991) pp.5-10. ([pdf](archive.numdam.org/article/CTGDC_1991__32_1_5_0.pdf))
&#8206;
* {#Law92} F. W. Lawvere, _Categories of Space and Quantity_, pp.14-30 in: J. Echeverria et al (eds.), _The Space of mathematics_ , de Gruyter Berlin 1992.

* {#Law94a} F. W. Lawvere, _Cohesive Toposes and Cantor's 'lauter Einsen'_ , Phil. Math. **2** no.3 (1994) pp.5-15.

* {#Law94b} F. W. Lawvere, _Tools for the Advancement of Objective Logic: Closed Categories and Toposes_, pp.43-56 in: J. Macnamara, G. E. Reyes (eds.), _The Logical Foundations of Cognition_ , Oxford UP 1994.

* {#Law96} F. W. Lawvere, _Unity and Identity of Opposites in Calculus and Physics_ , App. Cat. Struc **4** (1996) pp.167-174.

* {#Law99}F. W. Lawvere, _Kinship and Mathematical Categories_ , pp.411-425 in: R. Jackendoff, P. Bloom, K. Wynn (eds), _Language, Logic, and Concepts - Essays in Memory of John Macnamara_, MIT Press 1999.

* {#Law00} F. W. Lawvere , _Adjoint Cylinders_, message to catlist November 2000. ([link](http://permalink.gmane.org/gmane.science.mathematics.categories/1683))

* {#Law02} F. W. Lawvere, _Linearization of graphic toposes via Coxeter groups_ , JPAA **168** (2002) pp.425-436.

* {#Law07} F. W. Lawvere, _Axiomatic cohesion_ , TAC **19** no.3 (2007) pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))

* F. W. Lawvere, _Open Problems in Topos Theory_ , ms. (2009). ([pdf](http://cheng.staff.shef.ac.uk/pssl88/lawvere.pdf))

* {#Law13} F. W. Lawvere, _Combinatorial Topology_, message to catlist November 2013. ([link](http://comments.gmane.org/gmane.science.mathematics.categories/7920))

* {#LW11}[[Rory Lucyshyn-Wright|R. Lucyshyn-Wright]], _Totally Distributive Toposes_ , arXiv.1108.4032 (2011). ([pdf](http://arxiv.org/pdf/1108.4032v3))

* J. Petitot, _La Neige est Blanche ssi... Pr&#233;dication et Perception_ , Math.Inf.Sci.Hum **35** no.140 (1997) pp.35-50. ([pdf](http://archive.numdam.org/article/MSH_197_140_35_0.pdf))

* [[R. Street]], _The petit topos of globular sets_ , JPAA **154** (2000) pp.299-315.

* {#VT01}[[Enrico Vitale|E. M. Vitale]], _Essential Localizations and Infinitary Exact Completions_ , TAC **8** no.17 (2001) pp.465-480. ([pdf](http://www.tac.mta.ca/tac/volumes/8/n17/n17.pdf))

* {#WR93}[[Gavin C. Wraith]], _Using the Generic Interval_ , Cah.Top.G&#233;om.Diff.Cat. **XXXIV** 4 (1993) pp.259-266. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1993__34_4/CTGDC_1993__34_4_259_0/CTGDC_1993__34_4_259_0.pdf))

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Linear type theory_ is the [[linear logic]]-version of [[type theory]]. In the definition of ([Seely 89, prop. 1.5](#Seely89)), following ([Girard 87](#Girard87)), this is the [[internal language]] of/has [[categorical semantics]] in [[star-autonomous categories]]. 

More generally, the term "linear" (as in *linear type theory*) has over time come to connote [[internal languages|internal]] [[type theories]], and related logical frameworks ([[sequent calculus|sequent calculi]], [[natural deduction]]) that correspond to (usually symmetric) monoidal categories, where particularly the monoidal product is not assumed to be the cartesian product (reviews include [Blute-Panangaden-Seely 94](#BlutePanangadenSeely94)). Indeed, this general notion still faithfully follows the original motivation for the term "linear" as introduced in ([Girard 87](#Girard87)), since the non-cartesianness of the [[tensor product]] means the absence of a [[diagonal]] map and hence the impossibility of [[functions]] to depend on more than a single (linear) copy of their [[variables]]. 

In the corresponding logical frameworks, the non-cartesianness means one drops the contraction and weakening rules of inference associated with cartesian structure, but retains the exchange rule corresponding to the symmetry constraint. This general type of "linear logic" takes on many flavors: in addition to the Girard-style language that is naturally interpreted in [[star-autonomous categories]], one has languages for [[closed monoidal category|monoidal biclosed categories]], [[closed monoidal category|symmetric monoidal closed categories]], [[compact closed categories]], and others, collectively representing the "multiplicative" core of linear logic as understood in this general sense. 

In addition to this "multiplicative" core, one also often studies modalities (comonads) which relate these symmetric monoidal products to cartesian products and coproducts (so-called "additive" operations in linear logic). 

Extending these considerations, the [[dependent type theory]]-version of linear type theory should be _[[dependent linear type theory]]_.

Linear (dependent) type theory can be argued to be the proper [[type theory]] for [[quantum logic]]. In this context the linearity of the type theory, hence the absence of [[diagonal maps]] in its [[categorical semantics]], corresponds to the [[no-cloning theorem]] in [[quantum physics]].

## Properties

### Categorical semantics

(...)

In [[star-autonomous categories]].



| Conjunctive operator | $\leftarrow$[[de Morgan duality]] $\rightarrow$ | Disjunctive operator |
| -------------------- | - | -------------------- |
| $\top$               |   | $0$                  |
| $1$                  |   | $\bot$               |
| $\&$                 |   | $\oplus$             |
| $\otimes$            |   | $\parr$              |
| $^\bot$              |   | $^\bot$              |
| $\bigwedge$          |   | $\bigvee$            |
| $!$                  |   | $?$                  |

(...)

### The canonical co-modality

The original axiomatics for [[linear type theory]] in ([Girard 87](#Girard87)) contain in addition to the structures corresponding to a ([[star-autonomous category|star-autonomous]]) [[symmetric monoidal category|symmetric]] [[closed monoidal category]] a certain (co-)[[modality]] traditionally denoted "$!$", the [[exponential modality]]. 
In ([Benton 95](#Benton95), [Bierman 95](#Bierman95))
it is noticed (reviewed in ([Barber 97, p. 21 (26)](#Barber97))) that a natural [[categorical semantics]] for this modality identifies it with the [[comonad]] that is induced from a [[strong monoidal adjunction]]

$$
  (\Sigma \dashv R)
  \;\colon\;
  \mathcal{C}
  \stackrel{\overset{\Sigma}{\leftarrow}}{\underset{R}{\longrightarrow}}
  S
$$

between the [[closed monoidal category|closed]] [[symmetric monoidal category]] $\mathcal{C}$ which interprets the given [[linear type theory]] and a [[cartesian monoidal category]] $S$.

If there is only the [[strong monoidal functor]] $\Sigma \;\colon\; S \longrightarrow \mathcal{C}$ without possibly a [[right adjoint]], then ([Barber 97, p. 21 (27)](#Barber97)) speaks of the _structural [[fragment]]_ of [[linear type theory]].

In ([Ponto-Shulman 12](#PontoShulman12)) it is observed that this in turn is canonically induced if $\mathcal{C} \simeq \mathcal{C}_\ast$ is the linear type theory over the trivial context of a [[dependent linear type theory]]/[[indexed closed monoidal category]] with category of contexts being $S$. See at _[indexed monoidal (infinity,1)-category -- Exponential modality and Fock spaces](https://ncatlab.org/nlab/show/indexed+monoidal+%28infinity%2C1%29-category#TheCanonicalComodality)_ for more on this.

## History of linear categorical semantics
 {#HistoryCategoricalSemantics}
 
There is a long history of logical frameworks of "linear type" and their categorical semantics in various [[doctrines]] of monoidal and closed monoidal categories, even though much of the early history predates Girard's introduction of linear logic (and which therefore do not bear the term "linear"). We give a thumbnail sketch of some of this below. 

The founding father could be said to be [[Joachim Lambek]], who was the first to apply deductive systems and particularly the method of Gentzen cut-elimination to what we would now recognize as [[categorification]]s of various [[fragments]] of propositional logic. It is noteworthy that one of the various first applications of this categorified cut-elimination was to the (*linear*) doctrine of [[monoidal biclosed categories]], in which Lambek was interested in connection with his linguistic research ([Lambek 58](#Lambek58)); see ([Lambek 68](#Lambek68), [Lambek 69](#Lambek69)). A principal goal in these papers was to study (and partially solve) the coherence problem for such structures. 

+-- {: .num_remark} 
###### Remark 
Kelly and Mac Lane then adapted the essential cut-elimination techniques of Lambek to study the (difficult) coherence problem for closed symmetric monoidal categories, in their landmark study [KM](#KM71). Their work cleverly avoided the explicit introduction of logical equipment, presumably in the service of greater self-containment or greater categorical readership, although the debt to Lambek's pioneering work is clear enough (and _is_ made explicit). 
=-- 

By the late 1970's, the connections between [[proof theory]], coherence theory, and the categorical semantics of deductive systems had been well elaborated, and again it is noteworthy that there was especial focus on categorical doctrines of general linear type. A largish batch of various [[fragments]] of classical logic, particularly in sequent calculus form, together with their categorical semantics, was collected in a book-length study ([Szabo 78](#Szabo78)) by Manfred Szabo, who had been Lambek's student. (While the categorical semantics of various deductive systems were carefully spelled out in Szabo's book, this work was unfortunately tainted by overly ambitious claims by Szabo regarding his purported solutions to the relevant coherence problems, in terms of normalization algorithms which turned out not to be Church-Rosser; see [Jay 90a](#Jay90a).)  

Nor were the logical frameworks restricted to those of sequent calculus type. In particular, the Soviet logician Minc and his students had also developed a type theory whose semantics is naturally valued in closed monoidal categories; see [Minc 77](#Minc77). This too was in view of coherence problems. 

Interest in these problems was of course reawakened and reinvigorated in the light of Girard's extraordinarily insightful 1987 paper [Linear Logic](#Girard87). The connection with closed symmetric monoidal categories and $\ast$-autonomous categories was picked up in very short order by the categorical community; an early account of this connection was given by [Seely 89](#Seely89). It was not long before Girard's very fruitful exposition of linear proof theory and [[cut-elimination]] in terms of [[proof net|proof nets]], specifically for the [[multiplicative conjunction|multiplicative]] [[fragment]] MLL which is the basic technical core of Girard's work, was seen as closely related to "extranaturality" graphs (aka KM-graphs) used by Kelly-Mac Lane in their work on the coherence theory for closed symmetric monoidal categories -- as well as by other "Australian category theorists" who had developed Kelly's theory of clubs (which again tended to be most successful for doctrines of linear type). 

These aspects are covered in ([Blute 91](#Blute91)), who treated a number of coherence problems and particularly the method of Lambek/Kelly-Mac Lane as efficiently streamlined through the method of proof nets with connection given to KM-graphs and clubs. Note that all of those applications were towards various [[fragments]] of MLL or doctrines of linear type. 

From approximately the same time period we also have some work of Barry Jay, who had developed a calculus of terms and their normalization to study coherence for closed monoidal categories. See for instance ([Jay 89](#Jay89), [Jay 90b](#Jay90b)). (This does not seem to owe allegiance to Girard's methods particularly, but it does indicate some contemporaneous thinking on linear types, terms, and their categorical semantics.) 

+-- {: .num_remark} 
###### Remark 
It should be noted that the "classical" techniques developed by Lambek, Kelly-Mac Lane, and Blute merely yield _partial_ coherence results, in effect evading the notorious "problem of the unit" which had made the full coherence problem for closed monoidal categories seem fearsomely difficult. However, Trimble in his (unpublished) 1994 thesis showed how to re-interpret Girard's proof nets so that they naturally took the unit into account, and was then able to give a _full_ coherence result for MILL by arranging cut-free nets into a strongly normalizing and confluent rewrite system. Note that while full coherence results for this case had also been proposed by Voreadou and Dole (students of Mac Lane), by Minc and Jay, and also incorrectly by Szabo, none of these earlier approaches were in a position to take advantage of the proof net formalism. For another account of this sort of formalism, specifically for the case of $\ast$-autonomous categories, [[weakly distributive category|weakly distributive categories]], and full coherence thereof, see [Blute-Cockett-Seely-Trimble96](#BluteCockettSeelyTrimble96). 
=-- 

Meanwhile, the type theory and its categorical semantics for _full_ linear logic, going beyond MLL and taking into account the modalities and the "additive" operations of LL, was also advanced during this time period. A comprehensive description is given in [Benton-Bierman-de Paiva-Hyland 92](#BentonBiermanPaivaHyland92), with an important antecedent in de Paiva's work on the Dialectica interpretation [de Paiva 89](#dePaiva89). See also [Hyland-de Paiva 93](#HylandPaiva93), [Bierman 95](#Bierman95), [Barber 97](#Barber97)

See also [Schalk 04](#Schalk04), [Melli&#232;s 09](#Mellies09). Schalk and Melli&#232;s have also worked on game-theoretic semantics of theories of linear type -- which itself has a long and intricate history. 

Finally, in addition to these usual "denotational" categorical semantics, linear logic also has an "operational" categorical semantics, called the Geometry of Interaction, in traced monoidal categories. 

## Related concepts

* [[dependent linear type theory]]

* [[quantum logic]], [[quantum programming]]

* [[propositions as projections]]

* [[modal type theory]]

* [[geometric homotopy type theory]]

* [[stable homotopy type]]


## References

### General

The original article on [[linear logic]] is

* {#Girard87} [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science 50:1, 1987.  ([pdf](http://girard.perso.math.cnrs.fr/linear.pdf))

A review of linear logic is in

* {#Girard11} [[Jean-Yves Girard]], part III of _[[Lectures on Logic]]_, European Mathematical Society 2011

Linear type theory as such is made explicit for instance in 

* Masahito Hasegawa. _Logical predicates for intuitionistic linear type theories_, Typed Lambda Calculi and Applications:
4th International Conference, TLCA '99, ed. J.-Y. Girard, Lecture Notes in Computer Science 1581, Springer, Berlin, 1999 ([pdf](http://www.kurims.kyoto-u.ac.jp/~hassei/papers/tlca99.pdf))

* [pdf](http://www.cs.cmu.edu/~fp/courses/15816-f01/handouts/lintt.pdf)

### Lambek's syntactic calculus

Several decades before Girard's article on linear logic, Lambek introduced a sequent calculus without weakening, contraction, or exchange, and described its applications to modeling aspects of natural language (generalizing previous work by Ajdukiewicz and Bar-Hillel on [[categorial grammar]]):

* {#Lambek58} [[Joachim Lambek]]. _The mathematics of sentence structure_ . American mathematical monthly, 154-170, 1958. [link](http://www.jstor.org/stable/2310058)

Lambek called his system the "syntactic calculus", while nowadays it is often called _Lambek calculus_ in linguistics.

In "Towards a geometry of interaction" (1989), Girard references Lambek's 1958 article, and writes that "this work must be acknowledged as a true ancestor to linear logic; its connection to linguistics can be seen as the first serious evidence against the exclusive focus on mathematics" (p.81).  On the other hand, Lambek later wrote that his original motivations were actually in [[homological algebra]]:

> I would now call this system "bilinear logic", meaning "non-commutative linear logic" or "logic without Gentzen's three structural rules". My original name had been "syntactic calculus", because of its intended application to linguistics; but actually it had been developed in collaboration with George Findlay [1955] in an attempt to understand some basic homological algebra. Alas, our paper was rejected on the grounds that most of our results were to appear in a book by Cartan and Eilenberg [1956], the publication of which had been delayed because of a paper shortage. (Lambek, "Bilinear logic in algebra and linguistics", _Advances in Linear Logic_, CUP, 1995)


### Categorical semantics

The following articles are about "logics of linear type" and their categorical semantics, although they predate the use of the word "linear" in Girard's sense. Most have a view motivated in part by categorical coherence problems. 

* {#Lambek68} [[Joachim Lambek]], _Deductive systems and categories_, Mathematical Systems Theory 2 (1968), 287-318. 
 

* {#Lambek69} [[Joachim Lambek]], _Deductive systems and categories II_, Lecture Notes in Math. 86, Springer-Verlag (1969), 76-122. 

* {#Minc77} G.E. Minc, _Closed categories and the theory of proofs_, translated from an article in Russian in Zapiski Nauchnykh Seminarov Leningradskogo Otdeleniya Mat. Instituta im. V.A. Steklova AN SSSR 68 (1977), 83-114. Republished in Grigorii E. Mints, _Selected Papers in Proof Theory_, Bibliopolis (1992).

* {#Szabo78} M.E. Szabo, _Algebra of Proofs_, Studies in Logic and the Foundations of Mathematics, vol. 88 (1978), North-Holland. 

* {#Jay89} C.B. Jay, _Languages for monoidal categories_, JPAA 59 (1989), 61-85. 

* {#Jay90a} C.B. Jay, _Coherence in category theory and the Church-Rosser property_. Unpublished preprint (1990), cited in the following reference. 

* {#Jay90b} C.B. Jay, _The structure of free closed categories_, JPAA 66 (1990), 271-285. 

The [[categorical semantics]] of linear type theory in [[star-autonomous categories]] was first described in 

* {#Seely89} [[R. A. G. Seely]],  _Linear logic, $\ast$-autonomous categories and cofree coalgebras_, _Contemporary Mathematics_ 92, 1989.  ([[SeelyLinearLogic.pdf:file]], [ps.gz](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz)) 

with the first non-syntactic, mathematical categorical model in the same volume: 

* {#dePaiva89} [[Valeria de Paiva]], _The Dialectica Categories_, _Contemporary Mathematics_ 92, 1989. ([web] (http://www.cs.bham.ac.uk/~vdp/publications/dial87.pdf)) 

As mentioned above, generalization of this semantics, restricted to the "multiplicative fragment" but covering doctrines of more general symmetric monoidal closed type (with specific reference to Girard's work) is given in 

* {#Blute91} [[Richard Blute]], _Linear logic, coherence, and dinaturality_, Dissertation, University of Pennsylvania 1991, published in Theoretical Computer Science archive Volume 115 Issue 1, (July 5, 1993) 3-41.  
  

Blute's thesis derives coherence theorems for various doctrines of "linear type", including a coherence theorem for symmetric monoidal [[closed categories]] due to Kelly and Mac Lane: 

* {#KM71} [[Max Kelly]], [[Saunders MacLane]], _Coherence in closed categories_, JPAA 1 (1971), 97-140 ([web](http://www.sciencedirect.com/science/article/pii/0022404971900132)) 
 

An decent review of some of this is in 

* {#BlutePanangadenSeely94} [[Richard Blute]], [[Prakash Panangaden]], [[R. A. G. Seely]], _Fock Space: A Model of Linear Exponential Types_ (1994) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.27.6825))


Extensions of the coherence-theoretic applications of proof nets in Blute's thesis, to give full solutions to coherence problems, were given in 

* {#Trimble94} [[Todd Trimble]], _Linear Logic, Bimodules, and Full Coherence for Autonomous Categories, Rutgers 1994

* {#BluteCockettSeelyTrimble96} [[Richard Blute]], Cockett, [[R. A. G. Seely]], [[Todd Trimble]], _Natural deduction and coherence for weakly distributive categories_, JPAA 113 (1996), 229-296. ([web](http://www.sciencedirect.com/science/article/pii/002240499500159X)) 

Type theory for full linear logic, together with its categorical interpretation, was developed in 

* {#BentonBiermanPaivaHyland92} [[Nick Benton]], Gavin Bierman, [[Valeria de Paiva]], [[Martin Hyland]], _Term assignments for intuitionistic linear logic_. Technical report 262, Cambridge 1992 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.31.8666))
 

* {#HylandPaiva93} [[Martin Hyland]], [[Valeria de Paiva]], _Full Intuitionistic Linear Logic_ (extended abstract). Annals of Pure and Applied Logic, 64(3), pp.273-291, 1993. ([pdf](http://www.cs.bham.ac.uk/~vdp/publications/fill.pdf))

* {#Barber97} Andrew Graham Barber, _Linear Type Theories, Semantics and Action Calculi_, PhD Thesis, Edinburgh 1997 ([web](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/&#8206;), [pdf](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/ECS-LFCS-97-371.pdf))
 

Further review and discussion is in 

* {#Bierman95} Gavin M. Bierman, _What is a categorical model of intuitionistic linear logic? ([web] (http://research.microsoft.com/en-us/um/people/gmb/papers/tlca95.pdf)) 
 

The more general case of general [[symmetric monoidal categories]] is reviewed and further discussed in 

* {#Schalk04} Andrea Schalk, _What is a categorical model for linear logic?_ ([pdf](http://www.cs.man.ac.uk/&#8764;schalk/notes/llmodel.pdf))

* [[Richard Blute]], Philip Scott, _Category theory for linear logicians_, 2004 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.83.6250))

* {#Mellies09} [[Paul-André Melliès]] , _Categorial Semantics of Linear Logic_, in _Interactive models of computation and program behaviour_, Panoramas et synth&#232;ses 27, 2009 ([pdf](http://www.pps.univ-paris-diderot.fr/~mellies/papers/panorama.pdf))

The interpretation of Girard's $!$-modality as the [[comonad]] induced from a [[monoidal adjunction]] between the closed [[symmetric monoidal category]] and a [[cartesian closed category]] is due to

* {#Bierman95} G. Bierman, _On Intuitionistic Linear Logic_ PhD thesis, Computing
Laboratory, University of Cambridge, 1995 ([pdf](http://research.microsoft.com/~gmb/papers/thesis.pdf))

* {#Benton95} [[Nick Benton]], _A mixed linear and non-linear logic; proofs, terms and
models_, In _Proceedings of Computer Science Logic_ '94, vol. 933 of
Lecture Notes in Computer Science. Verlag, June 1995. 
 

Interpretation of this in [[dependent linear type theory]] is in 

* {#PontoShulman12} [[Kate Ponto]], [[Mike Shulman]], _Duality and traces for indexed monoidal categories_, Theory and Applications of Categories, Vol. 26, 2012, No. 23, pp 582-659 ([arXiv:1211.1555](http://arxiv.org/abs/1211.1555))
 


Further discussion of linear type theory is for instance in

* _Chapter 7, Linear type theory_ [pdf](http://www.cs.cmu.edu/~fp/courses/linear/handouts/lintt.pdf)

* Anders Schack-Nielsen, Carsten Sch&#252;rmann, _Linear contextual modal type theory_ [pdf](http://www.itu.dk/~carsten/papers/lcmtt.pdf)

* Bernardo Toninho, Lu&#237;s Caires, Frank Pfenning, _Dependent Session Types via Intuitionistic Linear Type Theory_ [pdf](http://ctp.di.fct.unl.pt/~lcaires/papers/dstypes.pdf)

* Iliano Cervesato, [[Frank Pfenning]], _A Linear Logical Framework_, 1996, ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.21.1152))

Discussion of application of linear logic to [[quantum logic]], [[quantum computing]] and generally to [[quantum physics]] includes

* [[Vaughan Pratt]], _Linear logic for generalized quantum mechanics_, in Proc. of _Workshop on Physics and Computation (PhysComp'92)_ ([pdf](http://boole.stanford.edu/pub/ql.pdf), [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.137.7817))

* [[Ross Duncan]], _Types for quantum mechanics_, 2006 ([pdf](http://personal.strath.ac.uk/ross.duncan/papers/rduncan-thesis.pdf))

* {#CCGP09} Gianpiero Cattaneo, Maria Luisa Dalla Chiara, Roberto
Giuntini and Francesco Paoli, section 9 of _Quantum Logic and Nonclassical Logics_, p. 127 in  Kurt Engesser, Dov M. Gabbay, Daniel Lehmann (eds.) _Handbook of Quantum Logic and Quantum Structures: Quantum Logic_, 2009 North Holland


* [[Ugo Dal Lago]], Claudia Faggian, _On Multiplicative Linear Logic, Modality and Quantum Circuits_ ([arXiv:1210.0613](http://arxiv.org/abs/1210.0613))


Discussion of linear type theory without [[units]] is in 

* [[Robin Houston]], _Linear Logic without Units_ ([arXiv:1305.2231](http://arxiv.org/abs/1305.2231))

Discussion of [[inductive types]] in the context of linear type theory is in 

* St&#233;phane Gimenez, _Towards Generic Inductive Constructions in
Systems of Nets_ ([pdf](http://www.imn.htwk-leipzig.de/WST2013/papers/paper_16.pdf))


[[!redirects linear type theories]]

[[!redirects linear type]]
[[!redirects linear types]]

[[!redirects linear homotopy type]]
[[!redirects linear homotopy types]]

[[!redirects linear type]]
[[!redirects linear types]]
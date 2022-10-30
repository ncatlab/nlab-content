
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

More generally, the term "linear" (as in *linear type theory*) has over time come to connote [[internal languages|internal]] [[type theories]] that correspond to (usually symmetric) monoidal categories, where particularly the monoidal product is not assumed to be the cartesian product. Indeed, this general notion still faithfully follows the original motivation for the term "linear" as introduced in ([Girard 87](#Girard87)), since the non-cartesianness of the [[tensor product]] means the absence of a [[diagonal]] map and hence the impossibility of [[functions]] to depend on more than a single (linear) copy of their [[variables]]. 

In the corresponding logical presentations, the non-cartesianness means one drops the contraction and weakening rules of inference associated with cartesian structure, but retains the exchange rule corresponding to the symmetry constraint. This general type of "linear logic" takes on many flavors: in addition to the Girard-style language that is naturally interpreted in [[star-autonomous categories]], one has languages for [[closed monoidal category|symmetric monoidal closed categories]], [[compact closed categories]], and others, collectively representing the "multiplicative" core of linear logic in this general sense. 

In addition to this "multiplicative" core, one also often studies modalities (comonads) which relate these symmetric monoidal products to cartesian products and coproducts (so-called "additive" operations in linear logic). 

For the important case of the linear type theory for possibly-non-[[cartesian monoidal category|cartesian]] [[symmetric monoidal category|symmetric]] [[closed monoidal category]], called _multiplicative intuitionistic linear logic_ or MILL for short, see especially ([dePaiva 89](#dePaiva89), [Blute 91](#Blute91), [Benton-Bierman-de Paiva-Hyland 92](#BentonBiermanPaivaHyland92), [Hyland-de Paiva 93](#HylandPaiva93),, [Bierman 95](#Bierman95), [Barber 97](#Barber97), see also [Schalk 04](#Schalk04), [Melli&#232;s 09](#Mellies09)). 

In addition to these usual "denotational" categorical semantica, linear logic also has an "operational" categorical semantics, called the _[[Geometry of Interaction]]_, in [[traced monoidal categories]].

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

The original axiomatics for [[linear type theory]] in ([Girard 87](#Girard87)) contain in addition to the structures corresponding to a ([[star-autonomous category|star-autonomous]]) [[symmetric monoidal category|symmetric]] [[closed monoidal category]] a certain (co-)[[modality]] traditionally denoted "$!$". 
In ([Benton 95](#Benton95), [Bierman 95](#Bierman95))
it is noticed (reviewed in ([Barber 97, p. 21 (26)](#Barber97))) that a natural [[categorical semantics]] for this modality identifies it with the [[comonad]] that is induced from a [[strong monoidal adjunction]]

$$
  (\Sigma \dashv R)
  \;\colon\;
  \mathcal{C}
  \stackrel{\overset{\Sigma}{\leftarrow}}{\underset{R}{\longrightarrow}}
  S
$$

between the [[closed monoidal category|closed]] [[symmetric monoidal category]] $\mathcal{C}$ wich interprets the given [[linear type theory]] and a [[cartesian monoidal category]] $S$.

If there is only the [[strong monoidal functor]] $\Sigma \;\colon\; S \longrightarrow \mathcal{C}$ without possibly a [[right adjoint]], then ([Barber 97, p. 21 (27)](#Barber97)) speaks of the _structural fragment_ of [[linear type theory]].

In ([Ponto-Shulman 12](#PontoShulman12)) it is observed that this in turn is canonically induced if $\mathcal{C} \simeq \mathcal{C}_\ast$ is the linear type theory over the trivial context of a [[dependent linear type theory]]/[[indexed closed monoidal category]] with category of contexts being $S$. See at _[dependent linear type theory -- Properties -- Canonical co-modality](http://ncatlab.org/nlab/show/dependent+linear+type+theory#TheCanonicalComodality)_ for more on this.

## Related concepts

* [[modal type theory]]

* [[geometric homotopy type theory]]

* [[stable homotopy type]]

## History of linear categorical semantics
 {#HistoryCategoricalSemantics}
 
([Blute 91](#Blute91)) is one concrete place where fragments of multiplicative [[linear logic]] and their [[categorical semantics]] are discussed, not because that semantics is the main focus of the work, but because the [[proof theory]] of the fragments is being related to [[coherence]]-theoretic results over on the categorical [[doctrine]] side. This was pretty well-known by anyone working in the area at that time, even if the word "linear" was not always used. 

For example, in ([Szabo 78](#Szabo78)) one finds descriptions of many fragments of classical [[propositional logic]] and their [[sequent calculi]], including quite specifically the fragments that correspond to [[symmetric monoidal categories]] and symmetric [[closed monoidal categories]], discussed in quite some detail. 

Szabo was a student of [[Lambek]], who was perhaps the founding father of the entire area: it was Lambek who first related the [[proof theory]] of various fragments of [[logic]] to [[category theory]] and promoted (categorified, in a sense) the crucial [[cut-elimination]] method of Gentzen to obtain [[coherence]]-theoretic results on the categorical side. This started already back in the 1960's ([Lambek 68](#Lambek68), [Lambek 69](#Lambek69)), basically with monoidal biclosed categories (or what were called _residuated categories_) but dropping the monoidal [[unit]], of which more in a moment. 

Cut-elimination is usually presented in the context of [[sequent calculus]], but workers in the area were also aware of how to translate into other [[logical frameworks]] (e.g., [[types]] and [[terms]]). For example, this is discussed in [Minc 77](#Minc77).


For instance the articles
([Jay 89](#Jay89), [Jay 90a](#Jay90a), [Jay 90b](#Jay90b))
develop a term calculus to give coherence-theoretic results for [[monoidal categories]] and [[symmetric monoidal categories]] in particular. So ideas on categorical semantics of fragments of logic, including famously the case of [[symmetric monoidal categories]], were well "in the air" by the late 80's, and not just in the air but written down, even if not all of them gave a nod to Girard.

Szabo's work has unfortunately been derided in some circles, because he wrongly claimed to have a rewrite system of sequent proofs for a batch of cases including sm and smc categories that was strongly normalizing and Church-Rosser; the claim of being Church-Rosser was refuted in ([Jay 90a](#Jay90a)). Nevertheless Szabo's book quite valuable because it has very concrete details on the sequent calculi themselves and their categorical semantics. 

The founding papers ([Lambek 68](#Lambek68), [Lambek 69](#Lambek69)) were extremely important, although they concentrate mainly on the monoidal biclosed case (which Lambek was interested in for other reasons, having to do with his categorical researches in linguistics). 

Blute, a student of Scedrov at U. Penn., wrote his thesis ([Blute 91](#Blute91)) specifically on Girard's technique of [[proof nets]] as applied to coherence problems. Proof nets, introduced in one form in the original linear logic paper of Girard (cf. the material on "cyclic trips") and developed further by Danos and Regnier, are a very pretty graphical way of visualizing the essential structure of Lambek-equivalence classes of sequent proofs and their cut-elimination specifically for fragments of MLL, including MILL, and some more abstruse cases (involving the so-called MIX rule). They are closely related to Kelly-Mac Lane [[extranaturality]] (or [[dinaturality]]) graphs, and what Blute does is how how to rederive the coherence-theoretic results of Kelly-Mac Lane for smc categories using the technique of proof nets. Actually, he treats a number of [[doctrines]] of monoidal closed type in the same way, indicating which doctrines are amenable to cut-elimination and which are not (e.g., compact closed categories), and I think he relates this also to which of these doctrines are "clubbable" in the sense of Kelly. 

The [[coherence]] problem for [[symmetric monoidal category]] cats was generally regarded as notorious and fearsomely difficult, partly because the techniques of Kelly and Mac Lane (based themselves on a close reading and rewriting of Lambek's work), based as they were on extranaturality graphs which track naturality and dinaturality instances of the variables that appear in morphisms of free structures (in the specifically "linear" cases, even if they didn't call it that), were insufficient to deal with constants such as the monoidal unit $I$. Szabo, Minc, Jay, Kelly, and at least two students of Mac Lane (Voreadou and Dole) all gave their own solutions, and all were difficult if not outright wrong. 

The thesis ([Trimble 94](#Trimble94)) does reinterpret the proof nets so that they would manifestly apply to the units as well. In the *intuitionistic* case (MILL), it was possible to give a very satisfying rewrite system on these unit-extended (cut-free) proof nets that was strongly [[normalization|normalizing]] and [[confluence|confluent]], so that the normalization solves the full [[coherence]] problem in a relatively simple and elegant way. It is probably fair to say that the coherence problem looks far less fearsome as a result of this work. The re-interpreted (i.e., unit-extended) proof nets also apply to MLL, so that the coherence problem for [[star-autonomous categories]] is effectively solved in terms of "rewiring"-equivalence classes of proof nets, although that case is, from the standpoint of writing down a rewrite system, not clean and simple as MLL: there is an input-output directionality for MILL proof nets that is not there for MLL proof nets. This is covered in [Blute-Cockett-Seely-Trimble96](#BluteCockettSeelyTrimble96)


(Weakly distributive categories are very closely related to $\ast$-autonomous categories: they have monoidal products $\otimes$, $\wp$ for the multiplicative conjunction and disjunction, with an appropriate distributivity or strength relating the two, but without linear negation. The paper gives precise details on the relationship.)

## References

### General

The orginal notion of [[linear logic]] was introduced in 

*  [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science 50:1, 1987.  ([pdf](http://iml.univ-mrs.fr/~girard/linear.pdf))
 {#Girard87}


A review is in

* [[Jean-Yves Girard]], part III of _[[Lectures on Logic]]_, European Mathematical Society 2011
 {#Girard11}

Linear type theory as such is made explicit for instance in 

* Masahito Haegawa. _Logical predicates for intuitionistic linear type theories_, Typed Lambda Calculi and Applications:
4th International Conference, TLCA '99, ed. J.-Y. Girard, Lecture Notes in Computer Science 1581, Springer, Berlin, 1999 ([pdf](http://www.kurims.kyoto-u.ac.jp/~hassei/papers/tlca99.pdf))

* [pdf](http://www.cs.cmu.edu/~fp/courses/15816-f01/handouts/lintt.pdf)

### Categorical semantics

* J. Lambek, _Deductive systems and categories_, Mathematical Systems Theory 2 (1968), 287-318. 
 {#Lambek68}

* J. Lambek, _Deductive systems and categories II_, Lecture Notes in Math. 86, Springer-Verlag (1969), 76-122. 
 {#Lambek69}

* G.E. Minc, _Closed categories and the theory of proofs_, translated from an article in Russian in Zapiski Nauchnykh Seminarov Leningradskogo Otdeleniya Mat. Instituta im. V.A. Steklova AN SSSR 68 (1977), 83-114. 
 {#Minc77}


* M.E. Szabo, _Algebra of Proofs_, Studies in Logic and the Foundations of Mathematics, vol. 88 (1978), North-Holland. 
 {#Szabo78}




The [[categorical semantics]] of linear type theory in [[star-autonomous categories]] was first described in 

*  [[R. A. G. Seely]],  _Linear logic, $\ast$-autonomous categories and cofree coalgebras_, _Contemporary Mathematics_ 92, 1989.  ([[SeelyLinearLogic.pdf:file]], [ps.gz](http://www.math.mcgill.ca/rags/nets/llsac.ps.gz))
 {#Seely89}

and the generalization to more general symmetric monoidal categories is considered in

(the first non-syntactic, mathematical categorical model in the same volume:)

* [[Valeria de Paiva]], _The Dialectica Categories_, _Contemporary Mathematics_ 92, 1989. ([web] (http://www.cs.bham.ac.uk/~vdp/publications/dial87.pdf)) 
 {#dePaiva89}


* C.B. Jay, _Languages for monoidal categories_, JPAA 59 (1989), 61-85. 
 {#Jay89}

* C.B. Jay, _Coherence in category theory and the Church-Rosser property_. Unpublished preprint (1990), cited in the following reference. 
 {#Jay90a}

* C.B. Jay, _The structure of free closed categories_, JPAA 66 (1990), 271-285. 
 {#Jay90b}


* [[Richard Blute]], _Linear logic, coherence, and dinaturality_, Dissertation, University of Pennsylvania 1991, published in Theoretical Computer Science archive
Volume 115 Issue 1, July 5, 1993  Pages 3 - 41 
 {#Blute91}

* Nick Benton, Gavin Bierman, [[Valeria de Paiva]], [[Martin Hyland]], _Term assignments for intuitionistic linear logic_. Technical report 262, Cambridge 1992 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.31.8666))
 {#BentonBiermanPaivaHyland92}

* [[Martin Hyland]], [[Valeria de Paiva]], _Full Intuitionistic Linear Logic_ (extended abstract). Annals of Pure and Applied Logic, 64(3), pp.273-291, 1993. ([pdf](http://www.cs.bham.ac.uk/~vdp/publications/fill.pdf))
 {#HylandPaiva93}

* [[Todd Trimble]], _Linear Logic, Bimodules and Full Coherence for Autonomous Categories, Rutgers 1994
 {#Trimble94}

* [[Richard Blute]], Cockett, [[R. A. G. Seely]], [[Todd Trimble]], _Natural deduction and coherence for weakly distributive categories_, JPAA 113 (1996), 229-296. ([web (http://www.sciencedirect.com/science/article/pii/002240499500159X)) 
 {#BluteCockettSeelyTrimble96}


* Andrew Graham Barber, _Linear Type Theories, Semantics and Action Calculi_, PhD Thesis, Edinburgh 1997 ([web](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/&#8206;), [pdf](http://www.lfcs.inf.ed.ac.uk/reports/97/ECS-LFCS-97-371/ECS-LFCS-97-371.pdf))
 {#Barber97}


Further review and discussion is in 

* Gavin M. Bierman, _What is a categorical model of intuitionistic linear logic? ([web] (http://research.microsoft.com/en-us/um/people/gmb/papers/tlca95.pdf))


The more general case of general [[symmetric monoidal categories]] is reviewed and further discussed in 

* Andrea Schalk, _What is a categorical model for linear logic?_ ([pdf](http://www.cs.man.ac.uk/&#8764;schalk/notes/llmodel.pdf))
 {#Schalk04}

* [[Richard Blute]], Philip Scott, _Category theory for linear logicians_, 2004 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.83.6250))


* [[Paul-André Melliès]] , _Categorial Semantics of Linear Logic_, in _Interactive models of computation and program behaviour_, Panoramas et synth&#232;ses 27, 2009 ([pdf](http://www.pps.univ-paris-diderot.fr/~mellies/papers/panorama.pdf))
 {#Mellies09}

The interpretation of Girard's $!$-modality as the [[comonad]] induced from a [[monoidal adjunction]] between the closed [[symmetric monoidal category]] and a [[cartesian closed category]] is due to

* G. Bierman, _On Intuitionistic Linear Logic_ PhD thesis, Computing
Laboratory, University of Cambridge, 1995 ([pdf](http://research.microsoft.com/~gmb/papers/thesis.pdf))
 {#Bierman95}

* N. Benton, _A mixed linear and non-linear logic; proofs, terms and
models_, In _Proceedings of Computer Science Logic_ '94, vol. 933 of
Lecture Notes in Computer Science. Verlag, June 1995. 
 {#Benton95}

Interpretation of this in [[dependent linear type theory]] is in 

* [[Kate Ponto]], [[Mike Shulman]], _Duality and traces for indexed monoidal categories_, Theory and Applications of Categories, Vol. 26, 2012, No. 23, pp 582-659 ([arXiv:1211.1555](http://arxiv.org/abs/1211.1555))
 {#PontoShulman12}


Further discussion of linear type theory is for instance in

* _Capter 7, Linear type theory_ [pdf](http://www.cs.cmu.edu/~fp/courses/linear/handouts/lintt.pdf)

* Anders Schack-Nielsen, Carsten Sch&#252;rmann, _Linear contextual modal type theory_ [pdf](http://www.itu.dk/~carsten/papers/lcmtt.pdf)

* Bernardo Toninho, Lu&#237;s Caires, Frank Pfenning, _Dependent Session Types via Intuitionistic Linear Type Theory_ [pdf](http://ctp.di.fct.unl.pt/~lcaires/papers/dstypes.pdf)

* Iliano Cervesato, [[Frank Pfenning]], _A Linear Logical Framework_, 1996, ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.21.1152))

Discussion of application of linear logic to [[quantum logic]], [[quantum computing]] and generally to [[quantum physics]] includes

* [[Vaughan Pratt]], _Linear logic for generalized quantum mechanics_, in Proc. of _Workshop on Physics and Computation (PhysComp'92)_ ([pdf](http://boole.stanford.edu/pub/ql.pdf), [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.137.7817))

* [[Ross Duncan]], _Types for quantum mechanics_, 2006 ([pdf](http://homepages.ulb.ac.be/~rduncan/papers/rduncan-thesis.pdf))

* Gianpiero Cattaneo, Maria Luisa Dalla Chiara, Roberto
Giuntini and Francesco Paoli, section 9 of _Quantum Logic and Nonclassical Logics_, p. 127 in  Kurt Engesser, Dov M. Gabbay, Daniel Lehmann (eds.) _Handbook of Quantum Logic and Quantum Structures: Quantum Logic_, 2009 North Holland
  {#CCGP09}


* Ugo Dal Lago, Claudia Faggian, _On Multiplicative Linear Logic, Modality and Quantum Circuits_ ([arXiv:1210.0613](http://arxiv.org/abs/1210.0613))


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
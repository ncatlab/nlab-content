[[!redirects Bonn2018]]



This entry records tites and abstracts of the meeting

* **[Types, Homotopy Type Theory, and Verification](https://www.him.uni-bonn.de/programs/past-programs/past-trimester-programs/types-sets-constructions/workshop-types-homotopy-type-theory-and-verification/)**


  June 4-8, 2018

  at the [Hausdorff Institute for Mathematics](https://www.him.uni-bonn.de/), Bonn

  Organizers: [[Steve Awodey]], [[Thierry Coquand]], [[Maria Emilia Maietti]]

on [[homotopy type theory]].

This was part of the:

* **Trimester Program "[Types, Sets and Constructions](https://www.him.uni-bonn.de/programs/past-programs/past-trimester-programs/types-sets-constructions/description/)"**

  May 2 - August 24, 2018

  at the [Hausdorff Institute for Mathematics](https://www.him.uni-bonn.de/), 

  Organizers: Douglas S. Bridges, Michael Rathjen, Peter Schuster, Helmut Schwichtenberg




#Contents#
* table of contents
{:toc}

## Schedule of the Workshop ##

Monday, June 4

11:00 - 12:00	Tutorial 1: Dan Licata: A Fibrational Framework for Modal Simple Type Theories
([slides](http://dlicata.web.wesleyan.edu/pubs/lsr17multi/him-tutorial.pdf))

14:00 - 15:00	Christian Sattler: Do cubical models of type theory also model homotopy types?

15:00 - 16:00	Floris van Doorn: Spectral Sequences in Homotopy Type Theory ([[vanDoorn.pdf:file]])

16:30 - 17:30	Thorsten Altenkirch: Towards higher models and syntax of type theory
([slides](http://www.cs.nott.ac.uk/~psztxa/talks/bonn18.pdf))


Tuesday, June 5

09:30 - 10:30	Klaus Mainzer: Algorithms of Type and Proof Checking

11:00 - 12:00	Tutorial 2: Felix Wellen: The Shape Modality in Real-cohesive HoTT and Covering Spaces

15:00 - 16:00	Kuen-Bang Hou (Favonia): Cartesian cubical computational type theory ([slides](http://favonia.org/files/ccctt-bonn2018-slides.pdf))

16:30 - 17:30	Benno van den Berg: Univalent polymorphism  ([[vdB.pdf:file]])

Wednesday, June 6

09:30 - 10:30	Tutorial 3: Dan Licata: Discrete and Codiscrete Modalities in Cohesive HoTT, I ([slides](http://dlicata.web.wesleyan.edu/pubs/lsr17multi/him-tutorial.pdf))

11:00 - 12:00	Tutorial 4: Felix Wellen: Discrete and Codiscrete Modalities in Cohesive HoTT, II

15:00 - 16:00	Anders Mortberg: Yet Another Cartesian Cubical Type Theory (yacctt)  ([[MortbergBonn.pdf:file]])

16:30 - 17:30	Jacopo Emmenegger: W-types in the setoid model

Thursday, June 7

09:30 - 10:30	Tutorial 5: Dan Licata: A Fibrational Framework for Modal Dependent Type Theories ([slides](http://dlicata.web.wesleyan.edu/pubs/lsr17multi/him-tutorial.pdf))

11:00 - 12:00	Bas Spitters: Modal Dependent Type Theory and the Cubical Model ([PDF](http://www.cs.au.dk/~spitters/bonn-slides.pdf))

14:00 - 15:00	Pino Rosolini: Embedding the effective topos into cubical assemblies

15:00 - 16:00	Fabio Pasquali: Assemblies as an elementary quotient completion

16:30 - 17:30	Hugo Herbelin: Investigations into cubical type theory

Friday, June 8

09:30 - 10:30	Tutorial 6: Felix Wellen: Differential Cohesive HoTT

11:00 - 12:00	Andrej Bauer: Toward an initiality theorem for general type theories

14:00 - 15:00	Nicolai Kraus: The Challenge of Free Groups

15:00 - 16:00	Paul-André Melliès: Refinement type systems and Martin-Lof type theory

##Abstracts##

### Thorsten Altenkirch: Towards higher models and syntax of type theory

We (Ambrus Kaposi and myself) have defined the intrinsic (no preterms) syntax of type theory in type theory using quotient inductive inductive types, that is set truncated higher inductive inductive types. Set truncation is necessary because we want to have decidability which we established using normalisation by evaluation. However, this stops us from defining any interesting semantic models, e.g. interpreting contexts as sets, types as families etc, because sets do not from a set (not for size reason but dimension). I suggest that we can overcome this problem by defining higher models of type theory and a higher syntax. I envisage that the higher syntax does form a set without being explicitly truncated, hence decidability should still hold. In my talk I will describe the first steps towards this programme.


### Andrej Bauer: Toward an initiality theorem for general type theories

I will report on a project of defining carefully and formally what a general type theory is. This is kind of step 1 to a generally applicable initiality theorem. It's not really a big surprise: it's what one would expect, but there's a number of things one has to organize and think through so that the whole thing holds water. We've got large chunks of it formalized. Work in progress with Philipp Haselwarter and Peter Lumsdaine. 

### Benno van den Berg: Univalent polymorphism

We show that Martin Hyland's effective topos can be exhibited as the homotopy category of a path category EFF. Path categories are categories of fibrant objects in the sense of Brown satisfying two additional properties and as such provide a context in which one can interpret many notions from homotopy theory and Homotopy Type Theory. Within the path category EFF one can identify a class of discrete fibrations which is closed under push forward along arbitrary fibrations (in other words, this class is polymorphic or closed under impredicative quantification) and satisfies propositional resizing. This class does not have a univalent representation, but if one restricts to those discrete fibrations whose fibres are propositions in the sense of Homotopy Type Theory, then it does. This means that, modulo the usual coherence problems, it can be seen as a model of the Calculus of Constructions with a univalent type of propositions. We will also build a more complicated path category in which the class of discrete fibrations whose fibres are sets in the sense of Homotopy Type Theory has a univalent representation, which means that this will be a model of the Calculus of Constructions with a univalent type of sets.

### Floris van Doorn: Spectral sequences in Homotopy Type Theory

In algebraic topology, spectral sequences form a powerful tool which can be used to compute homotopy and (co)homology groups of spaces in a wide variety of cases. We have constructed two spectral sequences in homotopy type theory, the Atiyah-Hirzebruch and Serre spectral sequences for cohomology. In this talk, I will introduce the concept of spectral sequences, talk about the spectral sequences we constructed and explore some of the applications and future work. (This is joint work with Jeremy Avigad, Steve Awodey, Ulrik Buchholtz, Egbert Rijke and Mike Shulman.)

### Jacopo Emmenegger: W-types in the setoid model

Current arguments to obtain initial algebras for polynomial endofunctors in categories of equivalence relations rely on assumptions like UIP or on constructions that involve recursion into a universe. We present a new argument, verified in Coq, that instead uses a generalisation of W-types in the underlying type theory. This in turn allows us to both give a direct construction of the initial algebra and to use induction of the underlying W-type to prove initiality.


### Hugo Herbelin: Investigations into cubical type theory

We report on a work in progress in building a variant of cubical type theory based on the following principles:

- equality is primitively attached to types;
- in particular, as in Altenkirch-Kaposi and Polonsky, equality of types is defined to be equivalence (so that univalence holds by construction); equality of proofs of equality of types is defined to be commutative squares of equivalences, etc.;
- type coercion (and thus transport) is direct by projecting the first component of a proof of equivalence;
- on top of type-based equality, a generic transverse level of dependent abstraction and application over a formal interval is provided (as in Section 9 of Cohen-Coquand-Huber-Mörtberg), together with connections and inverses, emphasizing that equality gives to types the structure of a symmetric (Cartesian) cubical structure with connections and reversals;
- a primitive notion of strictly associative composition of equality proofs is added which allows to interpret a function from the formal interval to the universe as a proof of equivalence;
- enforcing that transport computes on reflexivity proofs does not seem to pose problems;
- the theory is intended to be directly justified by an iterated parametricity translation to type theory with identity type, as explored e.g. by Altenkirch-Kaposi.


### Kuen-Bang Hou (Favonia): Cartesian cubical computational type theory

Homotopy type theory (HoTT) equips Martin-Löf type theory with additional features: univalence and higher inductive types. This has led to a fruitful development of synthetic homotopy theory. Unfortunately, those new features stated as axioms disrupt the computational content of type theory and affect the practicality of using HoTT to mechanize proofs. A well-known example is the fourth homotopy group of the 3-sphere, which was shown by Brunerie to be isomorphic to Z/nZ for some number n in HoTT, and the number n could have been automatically evaluated to the number two if the disruption did not happen. Instead, it took Brunerie several more years to prove that the number is indeed two. There have been many attempts to restore computational content while retaining all the additional features. To date, the most promising approach is through cubical structure. Recently, Cohen et al. constructed a type theory based on De Morgan cubes with univalence and higher inductive types. Inspired by their work, we also built a type-theoretic semantics with all the features but instead based on Cartesian cubes. In addition to using a different cubical structure, our semantics is built from computational content directly, following a computation-first methodology which itself is interesting. In this talk, I will compare two different cubical type theories and discuss how the computation-first methodology works.

(Joint work with Carlo Angiuli, Evan Cavallo, Robert Harper and Jonathan Sterling)

### Klaus Mainzer: Algorithms of Type and Proof Checking, Towards Univalent Foundations of Mathematics and Computer Science

Homotopy Type Theory (HoTT) is inspired by the idea of a proof-checking software to guarantee trust and security in mathematics. Since the Curry-Howard interpretation, basic intuitionistic type theory was extended by more advanced type formers (e.g., Martin-Löf). With higher inductive types in HoTT, we get direct, logical descriptions and constructions of advanced mathematical objects (e.g. in homotopy theory) as well as convenient machine implementations. These are not only theoretical insights connecting mathematics and computer science. They are deeply involved in great challenges of our digitalized world: Current AI-technology of machine learning is based on inductive principles of learning algorithms from data. But, although these are data-efficient methods, they need more explainability, verification, and provability of their foundations, in order to improve trust, reliability and security in society. HoTT should serve as a practical aid to working mathematicians as well as to computer scientists.


### Paul-André Melliès: Refinement type systems and Martin-Lof type theory

In this talk, I will review my recent work with Noam Zeilberger on refinement type systems [1,2]. I will then discuss how to equip refinement type systems with various notions of comprehension, in such a way as to connect them with Martin-Lof type theory.

[1] Paul-André Melliès and Noam Zeilberger. Functors are Type Refinement Systems.
[2] Paul-André Melliès and Noam Zeilberger. An Isbell Duality Theorem for Type Refinement Systems. Math. Struct. in Comp. Science (2018), vol. 28, pp. 736-774.
[3] Paul-André Melliès and Noam Zeilberger. A bifibrational reconstruction of Lawvere's presheaf hyperdoctrine. Proceedings of LICS 2016: 555-564


### Anders Mörtberg: Yet Another Cartesian Cubical Type Theory (yacctt)

I will discuss recent work on developing a Cartesian cubical type theory inspired by the computational semantics of Computational Higher Type Theory of Angiuli et. al. This system differs from cubical type theory (à la Coquand et. al.) in that it has an interval with less structure (no reversals or connections) and more general Kan composition operations. Another major difference is that there are no general Glue types, instead there is a special case called V-types which allows an equivalence to be transformed into a line between types. This specialization enables us to give a more direct proof that these "univalence types" are fibrant which in turn should lead to more efficient computations with univalence. If time permits I will sketch two proofs of the univalence theorem in this system.

This is joint work with Carlo Angiuli and we have implemented a primitive proof assistant based on this type theory: https://github.com/mortberg/yacctt.


### Fabio Pasquali: Assemblies as an elementary quotient completion

We characterize the category of assemblies as an elementary quotient completion, a construction introduced by Maietti and Rosolini to axiomatize the category of setoids used to build the Maietti-Sambin's Minimalist Foundation. As an application we link this characterization to the known fact that the effective topos, and related subcategories of it, satisfies Formal Church's Thesis. (This is a joint work with M.E. Maietti and G. Rosolini.)


### Pino Rosolini: Embedding the effective topos into cubical assemblies

The effective topos, introduced by J.M.E. Hyland in a paper in the Proceedings of the L.E.J.Brouwer Centenary Symposium, has proved to be a very useful environment where to test constructive aspects of mathematics, and many different presentations for the topos have been provided since its original appearance. In this line of work, we exhibit the effective topos as a subcategory of the cubical sets in the category of assemblies.
(Joint work with Steve Awodey and Jonas Frey)


### Christian Sattler: Do cubical models of type theory also model homotopy types?

I will give an alternative exposition of Kapulkin and Voevodsky's result about simplicial sets forming a subtopos of certain cubical sets: https://arxiv.org/abs/1805.04126. I will also give a brief summary of my current state of knowledge on which cubical models do or do not model homotopy types.


### Bas Spitters: Modal Dependent Type Theory, and its application to the cubical model

In recent years we have seen several new models of dependent type theory extended with some form of modal necessity operator, including nominal type theory, guarded and clocked type theory, and spatial and cohesive type theory. In this paper we study modal dependent type theory: dependent type theory with an operator satisfying (a dependent version of) the K-axiom of modal logic. We investigate both semantics and syntax. For the semantics, we introduce categories with families with a dependent right adjoint (CwDRA) and show that the examples above can be presented as such. Indeed, we show that any finite limit category with an adjunction of endofunctors gives rise to a CwDRA via the local universe construction. For the syntax, we introduce a dependently typed extension of Fitch-style modal lambda-calculus, show that it can be interpreted in any CwDRA, and build a term model. We extend the syntax and semantics with universes.
[Ranald Clouston, Bassel Mannaa, Rasmus Ejlers Møgelberg, Andrew M. Pitts, Bas Spitters, Modal Dependent Type Theory and Dependent Right Adjoints. https://arxiv.org/abs/1804.05236]
I will also present the related work on the application of modal dependent type theory to the construction of a universe in cubical sets in the internal logic.
[Daniel R. Licata, Ian Orton, Andrew M. Pitts, Bas Spitters, Internal Universes in Models of Homotopy Type Theory FSCD18 https://arxiv.org/abs/1801.07664]


### Tutorial Daniel R. Licata and Felix Wellen: Synthetic Mathematics in Modal Dependent Type Theories

Several [[modal homotopy type theory|modal extensions]] of [[homotopy type theory]] have been or are being developed, with applications to [[synthetic mathematics|synthetic]] formalizations of aspects of topology, differential geometry, and spectra, as well as internal language presentations of cubical models of HoTT. In this tutorial, we will describe some recent work on these type theories, the frameworks we use to design them, and their applications in real-cohesive and differential-cohesive HoTT.

The preliminary lecture schedule is: 

A Fibrational Framework for Modal Simple Type Theories
The Shape Modality in Real-cohesive HoTT and Covering Spaces
Discrete and Codiscrete Modalities in Cohesive HoTT, I
Discrete and Codiscrete Modalities in Cohesive HoTT, II
A Fibrational Framework for Modal Dependent Type Theories
Differential Cohesive HoTT
These talks will describe joint work with and work by Jacob Gross, Max S. New, Ian Orton, Jennifer Paykin, Andrew M. Pitts, Egbert Rijke, Mitchell Riley, Urs Schreiber, Michael Shulman, and Bas Spitters.

* {#LicataWellen18} [[Dan Licata]], [[Felix Wellen]], _Synthetic Mathematics in Modal Dependent Type Theories_, tutorial at *[[HoTT in Bonn2018|Types, Homotopy Theory and Verification]]*, 2018

  Tutorial 1, Dan Licata:  _A Fibrational Framework for Modal Simple Type Theories_
([recording](https://www.youtube.com/watch?v=uLLbSAYd3yI))

  Tutorial 2, Felix Wellen: _The Shape Modality in Real cohesive HoTT and Covering Spaces_ ([recording](https://www.youtube.com/watch?v=ACGjJDarEc4))

  Tutorial 3, Dan Licata: _Discrete and Codiscrete Modalities in Cohesive HoTT_ ([recording](https://www.youtube.com/watch?v=OHN9vEVPBN8))

  Tutorial 4, Felix Wellen, _Discrete and Codiscrete Modalities in Cohesive HoTT, II_ ([recording](https://www.youtube.com/watch?v=KXx9UDQdWPw))

  Tutorial 5, Dan Licata: _A Fibrational Framework for Modal Dependent Type Theories_ ([recording](https://www.youtube.com/watch?v=R4SsxUnIcng))

  Tutorial 6, Felix Wellen: _Differential Cohesive HoTT_, ([recording](https://www.youtube.com/watch?v=uEZXHPdwvJU&t=226s))

* {#Licata18} [[Dan Licata]], _Synthetic Mathematics in Modal Dependent Type Theories_, notes for tutorial at _[Types, Homotopy Theory and Verification](https://www.him.uni-bonn.de/programs/past-programs/past-trimester-programs/types-sets-constructions/workshop-types-homotopy-type-theory-and-verification/)_, 2018 ([pdf](http://dlicata.web.wesleyan.edu/pubs/lsr17multi/him-tutorial.pdf))


## See also

* [[homotopy type theory events]]

category: reference

[[!redirects Bonn18]]

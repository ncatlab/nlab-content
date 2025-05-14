
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

### General idea

In [[type theory]], the paradigm of __propositions as types__ says that [[propositions]] and [[types]] are essentially the same.  A proposition is identified with the type (collection) of all its [[proofs]], and a type is identified with the proposition that it has a [[term]] (so that each of its terms is in turn a proof of the corresponding proposition).  

> ... to show that a proposition is true in type theory corresponds to exhibiting an element $[$ [[term]] $]$ of the type corresponding to that proposition. We regard the elements of this type as _evidence_ or _witnesses_ that the proposition is true. (They are sometimes even called _proofs_... (from [[Homotopy Type Theory -- Univalent Foundations of Mathematics]], section 1.11)

Not all type theories follow this paradigm; among those that do, [[Martin-Löf type theories]] are the most famous. In its variant as [[homotopy type theory]] the paradigm is also central, but receives some refinements, see at [[propositions as some types]].

Even when the paradigm is not adopted, however, there is still a close relationship between logical and type-theoretic operations, called the __Curry--Howard isomorphism__ or (if it is not clear in which category this [[isomorphism]] is supposed to exist) the __Curry--Howard correspondence__. Or maybe better ([Harper](#Harper)) the **[[Brouwer-Heyting-Kolmogorov interpretation]]**. This correspondence is most precise and well-developed for [[intuitionistic logic]], but could also be developed for [[classical logic]]. 

Accordingly, [[logic|logical]] operations on propositions have immediate analogs on [[types]]. For instance logical _[[and]]_ corresponds to forming the [[product type]] $A \times B$ (a [[proof]] of $A$ and a proof of $B$), the [[universal quantifier]] corresponds to [[dependent product]], the [[existential quantifier]] to [[dependent sum]]. In [[classical mathematics]], the [[law of double negation]] corresponds to a [[global choice operator]]. 

Furthermore, most structures traditionally involving [[predicates]] or [[relations]] are defined as type-valued type families. For instance, [[setoids]] or [[Bishop sets]] are usually defined to have a [[pseudo-equivalence relation]] in the propositions as types paradigm, rather than a [[equivalence relation]] as typical in the [[propositions as some types]] paradigm. However, in classical mathematics, the [[global choice operator]] representing the [[law of double negation]] in propositions as types implies that the [[type of booleans]] is the [[type of all propositions]], so predicates or relations can simply be defined as functions into the type of booleans. 

### Propositions as some types
 {#PropositionsAsSomeTypes}

A related paradigm may be called **[[propositions as some types]]**, in which propositions are identified with particular types, but not all types are regarded as propositions.  Generally, the propositions are the "types with at most one [[term]]".  This is the paradigm usually used in the [[internal logic]] of [[categories]] such as [[toposes]], as well as in [[homotopy type theory]].  In this case, the type-theoretic operations on types either restrict to the propositions to give logical operations (for [[conjunction]], [[implication]], and the [[universal quantifier]]), or have to be "reflected" therein (for [[disjunction]] and the [[existential quantifier]]).  The reflector operation is called a [[bracket type]].


### In homotopy type theory

We consider aspects of the interpretation of _propositions as types_ in [[homotopy type theory]], see ([HoTT book, section 1.11](#HoTTBook)).

In [[homotopy type theory]] where types may be thought of as [[homotopy types]] ([[∞-groupoids]]) (or rather [[geometric homotopy types]] ([[∞-stacks]],[[(∞,1)-sheaves]]), more generally), we may think for $A$ any type of

* the [[objects]] of $A$ are [[proofs]] of some proposition;

* the [[morphisms]] of $A$ are equivalences between these proofs;

* the [[2-morphisms]] of $A$ are equivalences between these equivalences, and so on.

So in terms of the notion of [[n-connected object of an (infinity,1)-topos|n-connected]] and [[truncated|n-truncated objects in an (∞,1)-category]] we have 

* if $A$ is [[(-1)-connected]] then the corresponding proposition is [[true]]; 

* if $A$ is [[(-2)-truncated]] (a [[(-2)-groupoid]]) then the corresponding proposition is true by a unique proof which is uniquely equivalent to itself, etc.;

* if $A$ is [[(-1)-truncated]] (a [[(-1)-groupoid]]) then the corresponding proposition may be true or [[false]], but if it is true it is to by a unique proof as above;

* if $A$ is [[0-truncated]] then there may be more than one proof, but none equivalent to itself in an interesting way;

* if $A$ is [[1-truncated]] then there may be proofs of the corresponding proposition that are equivalent to themselves in interesting ways.

We would not say homotopy type theory has propositions as types in the same way that Martin--L&#246;f type theory has; only the $(-1)$-truncated types are propositions as such.  That is, in HoTT we have propositions as *some* types.  In this case the [[bracket types]] can be identified with a particular [[higher inductive type]] called $isInhab$.

### Propositions as sets in set theory

There is an analogue of the "propositions as types" in [[set theory]], called **propositions as sets**. Instead of working in the external logic, one interprets certain set-theoretic operations as representing the predicate logic:

* Any [[set]] represents a proposition

* The [[empty set]] represents [[falsehood]]

* Any [[singleton]] represents [[truth]]

* The binary cartesian product of two sets is [[conjunction]] of propositions

* The function set between two sets is [[implication]] of propositions

* The function set from a set to the empty set is [[negation]] of propositions

* Given a family of sets, the indexed [[cartesian product]] of the family of sets is [[universal quantification]]

* The binary [[disjoint union]] of two sets is the [[disjunction]] of propositions

* The indexed [[disjoint union]] of a family of sets is the [[existential quantifier]]

* Equality is given by the [[diagonal subset]]

Compare with [[propositions as subsingletons]], which is the usual interpretation of the [[internal logic]] of a set theory via set-theoretic operations on sets. 

## Related concepts

* [[proof relevance]]

* [[computational trinitarianism]]

* [[theory]]

* [[proposition]]/[[type]]

* [[definition]]/[[proof]]/[[program]] ([[proofs as programs]])

* [[theorem]], [[axiom]]

* [[propositions as projections]]

* [[propositions as some types]]

* [[propositional logic as a dependent type theory]]



## References

### General

Early account for [[intuitionistic type theory]]:

* [[Per Martin-Löf]] (notes by [[Giovanni Sambin]]), _Intuitionistic type theory_, noted of a Lecture in Padua 1984, Bibliopolis (1984) &lbrack;[pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]]&rbrack;

* {#Girard89} [[Jean-Yves Girard]] (translated and with appendiced by [[Paul Taylor]] and [[Yves Lafont]]), Chapter 3 of: *Proofs and Types*, Cambridge University Press (1989) &lbrack;[ISBN:978-0-521-37181-0](), [webpage](http://www.paultaylor.eu/stable/Proofs+Types.html), [pdf](https://www.paultaylor.eu/stable/prot.pdf)&rbrack;

With a notion of [[propositional truncation]]:

* [[Steve Awodey]], [[Andrej Bauer]], *Propositions as $[$Types$]$*, Journal of Logic and Computation, **14**  (2004) 447-471 &lbrack;[doi:10.1093/logcom/14.4.447](https://doi.org/10.1093/logcom/14.4.447), [pdf](http://andrej.com/papers/brackets_letter.pdf)&rbrack;


Textbook accounts:

* [[Simon Thompson]], *[[Type Theory and Functional Programming]]*, Addison-Wesley (1991) &lbrack;ISBN:0-201-41667-0, [webpage](http://www.cs.kent.ac.uk/people/staff/sjt/TTFP), [pdf](http://www.cs.kent.ac.uk/people/staff/sjt/TTFP/ttfp.pdf), [ISBN:9780444520777](https://www.elsevier.com/books/lectures-on-the-curry-howard-isomorphism/sorensen/978-0-444-52077-7)&rbrack;

* [[Bart Jacobs]], Section 10.2 of *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;


* Morten Heine Sørensen, Pawel Urzyczyn, *Lectures on the Curry-Howard isomorphism*, Studies in Logic **149**, Elsevier (2006) &lbrack;[ISBN:9780444520777](https://www.elsevier.com/books/lectures-on-the-curry-howard-isomorphism/sorensen/978-0-444-52077-7), [pdf](https://disi.unitn.it/~bernardi/RSISE11/Papers/curry-howard.pdf)&rbrack;

Exposition:

* {#Harper} [[Robert Harper]], _Extensionality, Intensionality, and Brouwer's Dictum_ (2012) &lbrack;[blog](http://existentialtype.wordpress.com/2012/08/11/extensionality-intensionality-and-brouwers-dictum/)&rbrack;

* [[Philip Wadler]], *Propositions as Types*, Communications of the ACM **58** 12 (2015) 75–84 &lbrack;[doi:10.1145/2699407](https://doi.org/10.1145/2699407), [pdf](https://homepages.inf.ed.ac.uk/wadler/papers/propositions-as-types/propositions-as-types.pdf), [video](https://www.youtube.com/watch?v=IOiZatlZtGU)&rbrack;

 
See also:

* Wikipedia, *[Curry-Howard correspondence](https://en.wikipedia.org/wiki/Curry%E2%80%93Howard_correspondence)*


Discussion in view of [[homotopy type theory]]:

* {#HoTTBook} [[Univalent Foundations Project]], Section 1.11 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf), [[Planet Math|PM]] [wiki version](http://planetmath.org/node/87534)&rbrack;

 
### History
 {#ReferencesHistory}

An influential original article was 

* [[William Howard]], _The formulae-as-types notion of construction_. In J. Roger Seldin, Jonathan P.; Hindley, (ed.s), _To H.B. Curry: Essays on Combinatory Logic, Lambda Calculus and Formalism_, pages 479&#8211;490. Academic Press, 1980. original paper manuscript from 1969. (Cited
on pages 53, 54, 100, and 430.) ([pdf](http://www.cs.cmu.edu/~crary/819-f09/Howard80.pdf))

The origins of this manuscript and its publication are recounted in a 2014 email from Howard to Philip Wadler:

* [[William Howard]], [email](http://wadler.blogspot.fr/2014/08/howard-on-curry-howard.html).

This influential note brought [[Dana Scott]] to write "Constructive Validity" (a precursor of type theory) and also strongly influenced [[Per Martin-Löf]]. Independently and at about the same time, the idea was also found by [[N.G. de Bruijn]] for the [[Automath]] system.

[[Dana Scott]], [[William Howard]], [[Per Martin-Löf]], and [[William Tait]] were all involved in the late 60s and early 70s, mainly in Chicago.

* [[William Tait]],  _The completeness of intuitionistic first-order logic_. Unpublished manuscript.

Also [[William Lawvere]] was there, lecturing on [[hyperdoctrines]]. Lawvere told [[Steve Awodey]] that the basic example of a morphism of hyperdoctrines from the proof-relevant one to the proof-irrelevant one was influenced by Kreisel, not Howard, who attended Lawvere's Chicago lectures in the 60s. See pages 2 and 3 of 

* [[William Lawvere]] interviewed by Felice Cardone, _The role of Cartesian closed categories in foundations_, March 2000 ([link](https://dl.dropboxusercontent.com/u/92056191/Archive/temporary_new_material/lawvere-cardone-2000/lawvere-cardone-2000.pdf))

But the story started earlier with what has been called the [[BHK interpretation]] of [[intuitionistic logic]], highlighted for instance in ([Troelstra 91](#Troelstra91)), which identifies a proposition with the collection of its proofs. This view goes back to an observation of Kolmogorov that the formalisation of Brouwer's ideas by Heyting in 1930 can be semantically interpreted as a calculus of 'Aufgaben' - problems (and solutions), reported in

* [[Andrey Kolmogorov]], _Zur Deutung der intuitionistischen Logik_, Math. Z. **35** (1932) pp.58-65. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=GDZPPN002373467))

A historical account is in the section on types in

* Hindley J. Roger; Cardone Felice, _History of Lambda-calculus and Combinatory Logic_. Handbook of the History of Logic. Volume 5. Logic from Russell to Church (edited by D. Gabbay and J. Woods), Elsevier, 2009, pp. 723-817 ([pdf](http://www.di.unito.it/~felice/pdf/lambdacomb.pdf), [errata](http://www.di.unito.it/~felice/pdf/erratalist.pdf))

and in section 5 of 

* {#Troelstra91} [[Anne Sjerp Troelstra]], _History of Constructivism in the 20th Century_, 1991 ([preprint](https://www.illc.uva.nl/Research/Publications/Reports/ML-1991-05.text.pdf))
 




[[!redirects propositions as types]]
[[!redirects propositions-as-types]]
[[!redirects propositions as types in type theory]]

[[!redirects propositions as sets]]
[[!redirects propositions-as-sets]]

[[!redirects Curry-Howard correspondence]]
[[!redirects Curry–Howard correspondence]]
[[!redirects Curry--Howard correspondence]]
[[!redirects Curry-Howard isomorphism]]
[[!redirects Curry–Howard isomorphism]]
[[!redirects Curry--Howard isomorphism]]
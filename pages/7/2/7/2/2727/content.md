
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[type theory]], the paradigm of __propositions as types__ says that a [[proposition]] and a [[type]] are the same thing.  A proposition is identified with its type of [[proofs]], and a type is identified with the proposition that it has a [[term]].  

Not all type theories follow this paradigm; among those that do, [[Martin-Löf type theories]] are the most famous.

Even when the paradigm is not adopted, however, there is still a close relationship between logical and type-theoretic operations, called the __Curry--Howard isomorphism__ or (if it is not clear in which category this [[isomorphism]] is supposed to exist) the __Curry--Howard correspondence__. Or maybe better ([Harper](#Harper)) the _[[BHK correspondence]]_. This correspondence is most precise and well-developed for [[intuitionistic logic]].

Accordingly, [[logic|logical]] operations on propositions have immediate analogs on [[types]]. For instance logical _[[and]]_ coresponds to forming the [[product type]] $A \times B$ (a [[proof]] of $A$ and a proof of $B$), the [[universal quantifier]] corresponds to [[dependent product]], the [[existential quantifier]] to [[dependent sum]].

A related paradigm may be called **propositions as some types**, in which propositions are identified with particular types, but not all types are regarded as propositions.  Generally, the propositions are the "types with at most one [[term]]".  This is the paradigm usually used in the [[internal logic]] of [[categories]] such as [[toposes]], as well as in [[homotopy type theory]].  In this case, the type-theoretic operations on types either restrict to the propositions to give logical operations (for [[conjunction]], [[implication]], and the [[universal quantifier]]), or have to be "reflected" therein (for [[disjunction]] and the [[existential quantifier]]).  The reflector operation is called a [[bracket type]].


## Curry--Howard / BHK in homotopy type theory

In [[homotopy type theory]] where types may be thought of as [[∞-groupoid]]s (or rather [[∞-stack]]s, more generally), we may think for $A$ any type of

* the [[object]]s of $A$ are proofs of some proposition;

* the [[morphism]]s of $A$ are equivalences between these proofs;

* the [[2-morphisms]] of $A$ are equivalences between these equivalences, and so on.

So in terms of the notion of [[n-connected object of an (infinity,1)-topos|n-connected]] and [[truncated|n-truncated objects in an (∞,1)-category]] we have 

* if $A$ is [[(-1)-connected]] then the corresponding proposition is [[true]]; 

* if $A$ is [[(-2)-truncated]] (a [[(-2)-groupoid]]) then the corresponding proposition is true by a unique proof which is uniquely equivalent to itself, etc.;

* if $A$ is [[(-1)-truncated]] (a [[(-1)-groupoid]]) then the corresponding proposition may be true or [[false]], but if it is true it is to by a unique proof as above;

* if $A$ is [[0-truncated]] then there may be more than one proof, but none equivalent to itself in an interesting way;

* if $A$ is [[1-truncated]] then there may be proofs of the corresponding proposition that are equivalent to themselves in interesting ways.

We would not say homotopy type theory has propositions as types in the same way that Martin--L&#246;f type theory has; only the $(-1)$-truncated types are propositions as such.  That is, in HoTT we have propositions as *some* types.  In this case the [[bracket types]] can be identified with a particular [[higher inductive type]] called $isInhab$.


## Related concepts

* [[computational trinitarianism]]

* [[theory]]

* [[proposition]]/[[type]] (**propositions as types**) 

* [[definition]]/[[proof]]/[[program]] ([[proofs as programs]])

* [[theorem]], [[axiom]]


## References


### General

* [[Per Martin-Löf]], _Intuitionistic Type Theory_, Notes by Giovanni Sambin of a series of lectures given in Padua, June 1980. Bibliopolis, Napoli, 1984.

* [[William Tait]],  _The completeness of intuitionistic first-order logic_. Unpublished manuscript.

Exposition is in 

* [[Robert Harper]], _Extensionality, Intensionality, and Brouwer's Dictum_ ([blog](http://existentialtype.wordpress.com/2012/08/11/extensionality-intensionality-and-brouwers-dictum/))
 {#Harper}

### History
 {#ReferencesHistory}

An influential original article was 

* [[William Howard]], _The formulae-as-types notion of construction_. In J. Roger Seldin, Jonathan P.; Hindley, (ed.s), _To H.B. Curry: Essays on Combinatory Logic, Lambda Calculus and Formalism_, pages 479&#8211;490. Academic Press, 1980. original paper manuscript from 1969. (Cited
on pages 53, 54, 100, and 430.)

This influential note brought [[Dana Scott]] to write "Constructive
Validity" (a precursor of type theory) and also strongly influenced
[[Per Martin-Löf]]. Independently and at about the same time, the idea was also found by N.G. de Bruijn for the [[Automath]] system.

[[Dana Scott]], [[William Howard]], [[Per Martin-Löf]], and [[William Tait]] were all involved in the late 60s and early 70s, mainly in Chicago.
Also [[William Lawvere]] was there, lecturing on [[hyperdoctrines]]. Lawvere told [[Steve Awodey]] that the basic example of a morphism of hyperdoctrines from the proof-relevant one to the proof-irrelevant one was influenced by Kreisel, not Howard, who attended Lawvere's Chicago lectures in the 60s. See pages 2 and 3 of 

* [[William Lawvere]] interviewed by Felice Cardone, _The role of Cartesian closed categories in foundations_, March 200 ([pdf](http://conceptualmathematics.files.wordpress.com/2013/02/cartesian-closed-categories.pdf))


A historical account is in the section on types in

* Hindley J. Roger; Cardone Felice, _History of Lambda-calculus and Combinatory Logic_. Handbook of the History of Logic. Volume 5. Logic from Russell to Church (edited by D. Gabbay and J. Woods), Elsevier, 2009, pp. 723-817 ([pdf](http://www.di.unito.it/~felice/pdf/lambdacomb.pdf), [errata](http://www.di.unito.it/~felice/pdf/erratalist.pdf) )

and in section 5 of 

* Troelstra, _History of Constructivism in the 20th Century_ ([pdf](http://staff.science.uva.nl/~anne/hhhist.pdf))

[[!redirects propositions as types]]
[[!redirects propositions as types in type theory]]

[[!redirects Curry-Howard correspondence]]
[[!redirects Curry?Howard correspondence]]
[[!redirects Curry--Howard correspondence]]
[[!redirects Curry-Howard isomorphism]]
[[!redirects Curry?Howard isomorphism]]
[[!redirects Curry--Howard isomorphism]]

[[!redirects propositions-as-types]]
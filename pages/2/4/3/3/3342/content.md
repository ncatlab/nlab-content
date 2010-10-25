

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The Haag--Kastler axioms (sometimes also called Araki--Haag--Kastler axioms) try to define in a mathematically precise way the notion of [[quantum field theory]] (QFT), by axiomatizing how its local _algebras of observables_ should behave. 

The approch to quantum field theory based on these axioms is often called [[AQFT]]: _algebraic quantum field theory_ .

Although they are called axioms, one should keep in mind that the Haag--Kastler approach to QFT has not reached its final state, so that different versions of the axioms are used by practitioners of the field.

From the [[nPOV]], the Haag-Kastler axioms descibe a coflabby [[copresheaf|presheaf]] of algebras. This kind of structure is similar to the notion of a [[factorization algebra]], which plays a role in other approaches to formalize local algebras of observables.


## Definition

1. Axiom A: 

   To every "allowed" (e.g. bounded open) region $O$ in spacetime there is associated a [[C*-algebra]]; this association fulfils isotony.
The basic assumption of the Haag--Kastler approach is that everything that can be measured in certain regions of spacetime $O$ (like temperature or particle count) is described by an algebra $A(O)$, so that the theory consists of a [[net]] of [[operator algebras]] and a [[state]] $p$ that describes the physical system. There are different approaches to define what regions are "allowed", one common approach is to take all [[bounded space|bounded]] [[open subspace|open]] subsets of [[Minkowski space|Minkowski]] [[spacetime]].

1. Axiom B: locality

   Locality Algebras assigned to regions that are spacelike separated commute. 

1. Axiom C:  Transformation Properties

   The geometric symmetry operations map the algebra of a region onto the algebra of the transformed region.

   In Minkowski spacetime the geometric symmetry group is usually be taken to be the [[Poincaré group]], but note that some authors consider subgroups of the full Poincar&#233; group, like the subgroup of translations (Borchers: "Translation group and particle representations in quantum field theory").

1. Axiom D: Positivity of Energy

   An axiom is needed to ensure that only nonnegative energies occur -- one possibility is the "spectrum condition", which says that the spectrum (to be more precise: the support of the [[spectral measure]]) of the operator associated with a translation is contained in the closed forward light cone, for all translations. 

## Remarks

Unlike the [[Wightman axioms]], the Haag--Kastler axioms do not need the notion of "[[physical field|field]]": the fields in the Wightman axioms are -- from the Haag--Kastler point of view -- only necessary to describe how the algebras of observables are constructed; any way to consistently construct the net of algebras would suffice.

It is possible to prove both a [[spin-statistics theorem]] and a [[PCT theorem]] in the Haag-Kastler approach. The mathematically precise, model independent statements and their proofs are considered to be a major breakthrough of the theory.

## Example: Causal Nets of Operator Algebras on Minkowski Spacetime
The nLab has a page with a specific choice of axioms and an exposition of some of their consequences here: [[Haag-Kastler vacuum representation]]

## Generalization of the Haag-Kastler Axioms to Curved Spacetimes
See [[AQFT on curved spacetimes]].

## References 

See also [[AQFT]]. 

### References for the physical aspects of the Haag-Kastler approach on Minkowski spacetime

Since on that page there are already some references to sources that stress the mathematical aspects, we will cite some that are more oriented to the physical interpretations:

The classic references are of course:

* Rudolf Haag: _Local quantum physics. Fields, particles, algebras._ 2nd., rev. and enlarged ed. Springer 1996 [ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0857.46057&format=complete).

and:

* Huzihiro Araki: _Mathematical theory of quantum fields._ Oxford University Press 1999 [ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0998.81501&format=complete). 

and

* Bogolyubov, Logunov, Oksak, Todorov: _General principles of quantum field theory._ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0732.46040&format=complete))


An online reference page is here:

* Stephen J. Summers: [AQFT online] (http://www.math.ufl.edu/~sjs/aqft.html)

An expository introduction into the properties of the vacuum state of a vacuum representation and it's physical consequences is this:

* Stephen J. Summers:"Yet More Ado About Nothing: The Remarkable Relativistic Vacuum State" ([arXiv] (http://xxx.uni-augsburg.de/abs/0802.1854))

An expository introduction to scattering theory is here:

* Stephen J. Summers, Detlev Buchholz: "Scattering in Relativistic Quantum Field Theory: Fundamental Concepts and Tools" ([arXiv] (http://xxx.uni-augsburg.de/abs/math-ph/0509047))

An introduction into Tomita-Takesaki modular theory is here:

* Stephen J. Summers: "Tomita-Takesaki Modular Theory" ([arXiv] (http://xxx.uni-augsburg.de/abs/math-ph/0511034))

...while a paper that puts it to serious work is this:

* H.J. Borchers: "On Revolutionizing of Quantum Field Theory
with Tomita's Modular Theory", ([ESI preprint page] (http://www.esi.ac.at/preprints/ESI-Preprints.html))

+-- {: .query}
[[Tim van Beek]]: I have not done an extensive search for pages that I could link to, so there may be some missing (but not on purpose!). Also the links on the [[AQFT]] site could equally well be placed here... 
=--


[[!redirects Haag-Kastler approach]]
[[!redirects Haag-Kastler axioms]]
[[!redirects Haag-Kastler axiom]]
[[!redirects Haag–Kastler axioms]]
[[!redirects Haag–Kastler axiom]]
[[!redirects Haag--Kastler axioms]]
[[!redirects Haag--Kastler axiom]]
[[!redirects Araki-Haag-Kastler axioms]]
[[!redirects Araki-Haag-Kastler axiom]]
[[!redirects Araki–Haag–Kastler axioms]]
[[!redirects Araki–Haag–Kastler axiom]]
[[!redirects Araki--Haag--Kastler axioms]]
[[!redirects Araki--Haag--Kastler axiom]]
[[!redirects Haag–Kastler net]]
[[!redirects Haag-Kastler nets]]


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
* table of contents
{:toc}

## Idea

The Haag--Kastler axioms (sometimes also called Araki--Haag--Kastler axioms) try to define in a mathematically precise way the notion of [[quantum field theory]] (QFT), by axiomatizing how its [[local nets of observables]] should behave. 

The approch to quantum field theory based on these axioms is often called [[AQFT]]: either for _axiomatic quantum field theory_ (since it was among the first attempts to put the edifice of QFT on solid [[axiom]]atic grounds) or _algebraic quantum field theory_ (since it amplifies the algebras of local [[observable]]s over the spaces of [[state]]s). Neither of these terms is very descriptive. First there is  another, dual, axiomatization which does axiomatize the propagation of [[states]] -- see _[[FQFT]]_ -- which, second, is also "algebraic" in some sense, even though algebras of observables to not appear directly.

Although they are called axioms, one should keep in mind that the Haag-Kastler approach to QFT has not reached its final state, so that different versions of the axioms are used by practitioners of the field.


## Formulation

We formulate the ideas of the core axioms of Haag-Kastler, and their intended physical meaning. For more details see [[local net of observables]].

1. **spacetime locality** 

   Since the _fields_ in [[quantum field theory]] (such as the [[electromagnetic field]]) exhibit and are characterized by
their _local excitations_ (for instance the value of the electric/magnetic [[field strength]] at any point) having effects only locally (the field excitations at two points a finite distance apart do not directly influence each other) the fields over any region of [[spacetime]] form a [[subsystem]] of the fields of any larger region and
in particular of the total system.

   If "[[quantum mechanical system]]" is formalized as "[[C-star algebra]]" (of [[observables]]) then "[[subsystem]]" translates to "sub-$C^*$-algebra". Therefore the above sentence translates into: quantum fields form a [[copresheaf]] of [[C-star algebras]] on [[spacetimes]] whose co-restriction morphisms are [[monomorphism]]s. 

   In [[AQFT]] such is called an **[[local net|isotonic net of algebras]]** .

   There are different approaches to define what kind of spacetime regions the algebras of observables are assigned to, hence different approaches as to what exactly the [[site]] is on which the co-presheaf is defined. A common approach is to take all [[bounded space|bounded]] [[open subspace|open]] subsets of [[Minkowski space|Minkowski]] [[spacetime]]. For more general setups see [[AQFT on curved spacetimes]].

1. **causal locality**

   If two regions of [[spacetime]] are [[spacelike]] separated, then there can be no influence between them whatsoever. Not only do the field excitations in one of the two regions not _directly_ influence those in the other region (as per item 1), but they do not even influence _indirectly_ : no [[waves]] of excitations (for instance [[electromagnetic waves]]: [[light]]) can run from one region to a spacelike separated region. Therefore the two [[subsystems]] constituted by these two regions accordording to the first point are even _[[independent subsystems]]_ .

   The formalization of "two [[independent subsystems]]" in [[quantum mechanics]] is: two subalgebras that _commute_ with each other inside the larger [[C-star algebra]]. (And usually one adds: and such that the algebra they generate in the larger algebra is [[isomorphic]] to their [[tensor product]].)

   Therefore this translates into the axiom: quantum fields on a
spacetime form an isotonic copresheaf of algebras such that the
algebras assigned to any two spacelike separated regions commute with
each other inside the algebra assigned to any larger region containing
these two regions.


1. **spacetime covariance**

   The geometric symmetry operations map the algebra of a region onto the algebra of the transformed region.

   (this is not an extra axiom if one defines the [[site]] of spacetime regions general enough...)

   In Minkowski spacetime the geometric symmetry group is usually be taken to be the [[Poincaré group]], but note that some authors consider subgroups of the full Poincar&#233; group, like the subgroup of translations (Borchers: "Translation group and particle representations in quantum field theory").

1. **positivity of energy**

   An axiom is needed to ensure that only nonnegative energies occur -- one possibility is the "spectrum condition", which says that the spectrum (to be more precise: the support of the [[spectral measure]]) of the operator associated with a translation is contained in the closed forward light cone, for all translations. 

## Properties

### Structural theorems

It is possible to prove both a [[spin-statistics theorem]] and a [[PCT theorem]] in the Haag-Kastler approach. The mathematically precise, model independent statements and their proofs are considered to be a major breakthrough of the theory.


### Relation to Wightman axioms

Unlike the [[Wightman axioms]], the Haag--Kastler axioms do not need the notion of "[[physical field|field]]": the fields in the Wightman axioms are -- from the Haag--Kastler point of view -- only necessary to describe how the algebras of observables are constructed; any way to consistently construct the net of algebras would suffice.


## Related concepts

* [[AQFT]]

  * **Haag-Kastler axioms**

  * [[local net of observables]]

## References 

The original article that introduced these axioms is

* [[Rudolf Haag]], [[Daniel Kastler]], _An algebraic approach to quantum field theory_ , Journal of Mathematical Physics, Bd.5, 1964, S.848-861 

See also the references at [[AQFT]]. 

Since on that page there are already some references to sources that stress the mathematical aspects, we will cite some that are more oriented to the physical interpretations:

The classic references are

* [[Rudolf Haag]], _[[Local Quantum Physics -- Fields, Particles, Algebras]]_ 

and

* [[Huzihiro Araki]]: _[[Mathematical Theory of Quantum Fields]]_ Oxford University Press 1999 [ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0998.81501&format=complete). 

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
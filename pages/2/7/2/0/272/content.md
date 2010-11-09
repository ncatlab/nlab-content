
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

**Algebraic Quantum Field Theory** or **Axiomatic Quantum Field Theory** or **AQFT** for short is a formalization of [[quantum field theory]] that axiomatizes the assignment of _algebras of observables_ to patches of parameter space that one expects a quantum field theory to provide.

As such, the approach of AQFT is roughly dual to that of [[FQFT]], where instead _spaces of states_ are assigned to boundaries of [[cobordism]]s and propagation maps between state spaces to cobordisms themselves.

One may roughly think of AQFT as being a formalization of what in basic [[quantum mechanics]] textbooks is called the **Heisenberg picture** of quantum mechanics. On the other hand [[FQFT]] axiomatizes the _Schr&#246;dinger picture_ .

The axioms of traditional AQFT encode the properties of a [[local net]] of observables and are called the [[Haag-Kastler axioms]]. They are one of the oldest systems of axioms that seriously attempt to put [[quantum field theory]] on a solid conceptual footing. 

From the [[nPOV]] we may think of a [[local net]] as a co-flabby [[presheaf|copresheaf]] of [[algebra|algebras]] on spacetime which satisfies a certain _locality_ axiom with respect to the Lorentzian structure of spacetime: 

* locality: algebras assigned to spacelike separated regions commute with each other when embedded into any joint superalgebra.

This is traditionally formulated (implicitly) as a structure in ordinary [[category theory]]. More recently, with the proof of the [[cobordism hypothesis]] and the corresponding [[(∞,n)-category]]-formulation of [[FQFT]] also [[higher category theory|higher categorical]] versions of systems of local algebras of observables are being put forward and studied. Three structures are curently being studied, that are all conceptually very similar and similar to the Haag-Kastler axioms:


* [[factorization algebra]]s

* [[topological chiral homology]]

* [[blob homology]].

On the other hand, all three of these encode what in physics are called _Euclidean_ quantum field theories, whereas only the notion of [[local net]] so far really incorporates crucially the fact that the underlying spacetime of a quantum field theory is a [[smooth Lorentzian space]].

In the context of the Haag-Kastler axioms there is a precise theorem, the [[Osterwalder-Schrader theorem]], relating the Euclidean to the Lorentzian formulation: this is the operation known as [[Wick rotation]].

--- much information to be filled in ---


## Axioms

* [[Wightman axioms]]

* [[Haag-Kastler axioms]]

## Theorems

* [[Reeh-Schlieder theorem]]

* [[Osterwalder-Schrader theorem]]

* [[PCT theorem]]

* [[Bisognano-Wichmann theorem]]

* [[spin-statistics theorem]]


--- much information to be filled in ---

## References

A good account of the mathematical axiomatics of Haag-Kastler AQFT is

* Hans Halvorson, Michael M&#252;ger, _Algebraic Quantum Field Theory_ ([arXiv](http://arxiv.org/abs/math-ph/0602036))

This is, among other things, the ideal starting point for pure mathematicians who have always been left puzzled or otherwise unsatisfied by accounts of quantum field theory, even those tagged as being "for mathematicians". AQFT is truly axiomatic and rigorously formal. 

An account written by mathematicians for mathematicians is this:

* Hellmut Baumg&#228;rtel, Manfred Wollenberg: _Causal nets of operator algebras._ Berlin: Akademie Verlag 1992 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0749.46038&format=complete))

and this:

* Hellmut Baumg&#228;rtel: _Operator algebraic Methods in Quantum Field Theory. A series of lectures._ Akademie Verlag 1995 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0839.46063&format=complete))

There is much more literature one should point to here, eventually. For instance for the connection between the AQFT axioms and the perturbative Feynman-integral techniques much used in [[quantum field theory]], see

* Romeo Brunetti, Michael Duetsch, Klaus Fredenhagen, _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_ ([arXiv](http://arxiv.org/abs/0901.2038))

Out of laziness for the moment I point for further references and more background to the introductory section of 

* [[Urs Schreiber]], _AQFT from $n$-functorial QFT_ , Comm. Math. Phys., ([arXiv](http://arxiv.org/abs/0806.1079))

Recent account of the principle of locality in AQFT from the point of view of traditional school

* Sergio Doplicher, _The principle of locality: Effectiveness, fate, and challenges_, J. Math. Phys. __51__, 015218 (2010), [doi](http://dx.doi.org/10.1063/1.3276100)
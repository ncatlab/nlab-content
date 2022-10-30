
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
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

## Idea

Broadly speaking, _quantum logic_ is meant to be a kind of [[formal logic]] that is to traditional formal logic as [[quantum mechanics]] is to [[classical mechanics]]. In its traditional meaning "quantum logic" refers to the [[orthocomplemented lattice]] of closed linear subspaces of a [[Hilbert space]] [[space of quantum states|of quantum states]]. Later it was proposed that the logic of quantum systems is better captured by [[linear logic]] or by the [[internal logic]] of [[Bohr toposes]].



## History

Typically  in the literature the term "quantum logic" is taken to refer very specifically to the first proposal for such a formalization that was given by ([Birkhoff-vonNeumann 1936](#BirkhoffvonNeumann36)). In this proposal given a [[quantum mechanical system]] with a [[Hilbert space]] [[space of states|of states]], the logical [[propositions]] about the system are taken to correspond to (the [[projections]] to) [[closed subspaces]], with [[implication]] given by inclusion of such subspaces.  Hence Brikhoff-vonNeumann quantum logic is given by the [[lattice]] of closed linear subspaces of Hilbert spaces (regarded as an [[orthocomplemented lattice]]).

This formalization is often understood as being the default meaning of "quantum logic". But the proposal has later been much criticised, for its lack of key properties that one would demand of a [[formal logic]]. 

For instance in ([Heunen-Landsman-Spitters 07, p. 4](#HeunenLandsmanSpitters07)) it says the following.

> Attractive and revolutionary as this spatial quantum "logic" may appear  it faces severe problems. The main logical drawbacks are:

> &#8226; Due to its lack of distributivity, quantum 'logic' is difficult to interpret as a logical structure.
> &#8226; In particular, despite various proposals no satisfactory implication operator has been found (so that there is no deductive system in quantum logic).
> &#8226; Quantum 'logic' is a propositional language; no satisfactory generalization to predicate logic has been found. 

> Quantum logic is also problematic from a physical perspective. Since (by various theorems and wide agreement) quantum probabilities do not admit an ignorance interpretation, $[0, 1]$-valued truth values attributed to propositions by pure states via the Born rule cannot be regarded as sharp (i.e. {0, 1}-valued) truth values muddled by human ignorance. This implies that, if $X = [a \in \Delta]$ represents a quantum-mechanical proposition, it is wrong to say that either $x$ or its negation holds, but we just do not know which of these alternatives applies. However, in quantum logic one has the law of the excluded middle in the form $x \vee x^\perp = 1$ for all $x$. Thus the formalism of quantum logic does not match the probabilistic structure of quantum theory responsible for its empirical content.

In ([Girard 11, page xii](#Girard11)) it says:

>  Among the magisterial mistakes of logic, one will first mention quantum logic, whose ridiculousness can only be ascribed to a feeling of superiority of the language &#8211; and ideas, even bad, as soon as they take a written form &#8211; over the physical world. Quantum logic is indeed a sort of punishment inflicted on nature, guilty of not yielding to the prejudices of logicians... just like Xerxes had the Hellespont &#8211; which had destroyed a boat bridge &#8211; whipped.

For more criticism see ([Girard 11, section 17](#Girard11)).

Therefore later other proposals as to what quantum logic should be have been made, and possibly by "quantum logic" in the general sense one should understand any formal framework which is supposed to be able to _express_ the statements whose [[semantics]] is the totality of all what is verifiable by [[measurement]] in a [[quantum system]].

In particular it can be argued that flavors of _[[linear logic]]_ and more generally _[[linear type theory]]_ faithfully capture the essence of [[quantum mechanics]] ([Abramsky-Duncan 05](#AbramskyDuncan05), [Duncan 06](#Duncan06), see ([Baez-Stay 09](#BaezStay09)) for an introductory exposition) due to its [[categorical semantics]] in [[symmetric monoidal categories]] such as those used in the desctiption of [[finite quantum mechanics in terms of dagger-compact categories]]. In particular the [[category]] of (finite dimensional) [[Hilbert spaces]] that essentially underlies the Birkhoff-vonNeumann quantum logic interprets [[linear logic]].

Another candidate for quantum logic has been argued to be the [[internal logic]] of [[Bohr toposes]] .

In [[quantum computing]] the quantum analog of classical [[logic gates]] are called _quantum logic gates_.

## Approaches

### Birkhoff-von Neumann quantum logic

It is based on the setting the [[Hilbert lattice]] (of closed suspaces of a Hilbert space) to represent the set of propositions of quantum system. 

...

### Linear logic

See at _[[linear logic]]_, _[[linear type theory]]_, _[[quantum computing]]_.

### Topos theoretic approaches to quantum mechanics

See at _[[Bohr topos]]_ for more.


## Related concepts

* [[qbit]]

* [[linear logic]], [[quantum computing]]

* [[quantum mechanics]]

* [[Kochen-Specker theorem]]

* [[Gleason's theorem]]

* [[quantale]], 

* [[Bohr topos]]

## Literature

General introductions ans surveys include

* Wikipedia, _[Quantum logic](http://en.wikipedia.org/wiki/Quantum_logic)_

* Stanford encyclopaedia of philosophy: [quantum logic and probability theory](http://plato.stanford.edu/entries/qt-quantlog), [quantum mechanics](http://plato.stanford.edu/entries/qm) (abbrev. qm), [qm: Kochen-Specker theorem](http://plato.stanford.edu/entries/kochen-specker), [qm: von Neumann vs. Dirac](http://plato.stanford.edu/entries/qt-nvd), [qm: Bohmian mechanics](http://plato.stanford.edu/entries/qm-bohm), [qm:colapse theories](http://plato.stanford.edu/entries/qm-collapse), [Copenhagen interpretation of qm](http://plato.stanford.edu/entries/qm-copenhagen), [many-world interpretation of qm](http://plato.stanford.edu/entries/qm-manyworlds), [modal-interpretations of qm](http://plato.stanford.edu/entries/qm-modal), [Everett's relative-state formulation of qm](http://plato.stanford.edu/entries/qm-everett)

* I. Pitowsky, _Quantum probability &#8212; quantum logic_, Springer Lecture Notes in Physics __321__


The original article on quantum logic is

* [[Garrett Birkhoff]], [[John von Neumann]], _The logic of quantum mechanics_, Annals of Mathematics, 37: 823-843 (1936)
 {#BirkhoffvonNeumann36}

Further discussion of this includes 

* A. Gleason, _Measures on the closed subspaces of a Hilbert space_, Journal of Mathematics and Mechanics __6__: 885-893 (1957)

* Samuel S. Holland Jr., _Orthomodularity in infinite dimensions; a theorem of M. Sol&#232;r_, Bull. Amer. Math. Soc. (N.S.) __32__ (1995) 205-234, [arXiv:math.RA/9504224](http://arxiv.org/abs/math/9504224)

Discussion of [[linear logic]] as quantum logic is in 

* [[Jean-Yves Girard]], _[[Lectures on Logic]]_, European Mathematical Society 2011
 {#Girard11}

* [[Samson Abramsky]], [[Ross Duncan]], _A Categorical Quantum Logic_ ([arXiv:quant-ph/0512114](http://arxiv.org/abs/quant-ph/0512114))
 {#AbramskyDuncan05}

* [[Ross Duncan]], _Types for quantum mechanics_, 2006 ([pdf](http://homepages.ulb.ac.be/~rduncan/papers/rduncan-thesis.pdf), [slides](http://www.cs.ox.ac.uk/people/ross.duncan/talks/2005/pps-22-05-2005.pdf))
 {#Duncan06}

An exposition along these lines is in

* [[John Baez]], [[Mike Stay]], _Physics, topology, logic and computation: a rosetta stone_, [arxiv/0903.0340](http://arxiv.org/abs/0903.0340); in "New Structures for Physics", ed. Bob Coecke, Lecture Notes in Physics __813__, Springer, Berlin, 2011, pp. 95-174
 {#BaezStay09}

The proposal that the [[internal logic]] of [[Bohr toposes]] is a good notion of quantum logic is made in

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], _A topos for algebraic quantum theory_, Comm. Math. Phys. 291:63&#8211;110, 2009, free access [doi](http://dx.doi.org/10.1007/s00220-009-0865-6), [arXiv:0709.4364](http://arxiv.org/abs/0709.4364)
 {#HeunenLandsmanSpitters07}

* [[Steve Vickers]], slides from Midland Grad. School 2010, quantum topos theory, [web](http://www.cs.bham.ac.uk/~sjv/teaching/MGS2010), most relevant part IV: [pdf](http://www.cs.bham.ac.uk/~sjv/teaching/MGS2010/slides4.pdf)


See also

* [[Yuri Manin]], _A course in mathematical logic_, Springer 

*  &#1044;.&#1048;. &#1041;&#1083;&#1086;&#1093;&#1080;&#1085;&#1094;&#1077;&#1074;, &#1055;&#1088;&#1080;&#1085;&#1094;&#1080;&#1087;&#1080;&#1072;&#1083;&#1100;&#1085;&#1099;&#1077; &#1074;&#1086;&#1087;&#1088;&#1086;&#1089;&#1099; &#1082;&#1074;&#1072;&#1085;&#1090;&#1086;&#1074;&#1086;&#1081; &#1084;&#1077;&#1093;&#1072;&#1085;&#1080;&#1082;&#1080;, 1966, 162 &#1089;.


* A. Sudbery, _Quantum mechanics and the particles of nature_, An outline for mathematicians, Camb. Univ. Press 1986


[[!redirects quantum logics]]
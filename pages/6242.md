
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Broadly speaking, _quantum logic_ is meant to be a kind of [[formal logic]] that is to traditional formal logic as [[quantum mechanics]] is to [[classical mechanics]]: a formal framework which is supposed to be able to _express_ the statements whose [[semantics]] is the totality of all what is verifiable by [[measurement]] in a [[quantum system]] ([[quantum measurement]]).

In its traditional and default meaning due to ([Birkhoff-vonNeumann 1936](#BirkhoffvonNeumann36)) "quantum logic" refers specifically to the [[orthocomplemented lattice]] of closed linear subspaces of a [[Hilbert space]] [[space of quantum states|of quantum states]]. Later it was proposed ([Yetter 90](#Yetter90), [Pratt 92](#Pratt92), [Abramsky-Duncan 05](#AbramskyDuncan05), [Girard 11](#Girard11)) that a better way to think of the BvN quantum lattices is as the [[propositions]] in [[linear logic]] ([Girard 87](#Girard)), the [[categorical logic]] of [[symmetric monoidal categories]]. 

There is also the proposal ([Heunen-Landsman-Spitters 07](#HeunenLandsmanSpitters07)) that quantum logic should be understood as being the [[internal logic]] of [[Bohr toposes]].

In [[quantum computing]] the quantum analog of classical [[logic gates]] are called _[[quantum logic gates]]_.


## History and Critique
 {#History}

Typically  in the literature the term "quantum logic" is taken to refer very specifically to the first proposal for such a formalization that was given by ([Birkhoff-von Neumann 1936](#BirkhoffvonNeumann36)). In this proposal given a [[quantum mechanical system]] with a [[Hilbert space]] [[space of states|of states]], the logical [[propositions]] about the system are taken to correspond to (the [[projections]] to) [[closed subspaces]], with [[implication]] given by inclusion of such subspaces.  Hence Birkhoff-von Neumann quantum logic is given by the [[lattice]] of closed linear subspaces of Hilbert spaces (regarded as a [[Hilbert lattice]]).

This formalization is often understood as being the default meaning of "quantum logic". But the proposal has later been much criticised, for its lack of key properties that one would demand of a [[formal logic]]. 

For instance in ([Abramsky 09](#Abramsky09)) it is called a "non-logic"

> The term quantum logic is usually understood in connection with the 1936 Birkhoff-von Neumann proposal to consider the (closed) linear subspaces of a Hilbert space ordered by inclusion as the formal expression of the logical distinction between quantum and classical physics. While in classical logic we have deduction, the linear subspaces of a Hilbert space form a non-distributive lattice and hence there is no obvious notion of implication or deduction. Quantum logic was therefore always seen as logically very weak, or even as a non-logic. In addition, it has never given a satisfactory account of compound systems and entanglement.

Here by "no [[deduction]]" is meant "no [[deduction theorem]]".

And for example in ([Heunen-Landsman-Spitters 07, p. 4](#HeunenLandsmanSpitters07)) it says the following.

> Attractive and revolutionary as this spatial quantum "logic" may appear  it faces severe problems. The main logical drawbacks are:

> 1. Due to its lack of distributivity, quantum 'logic' is difficult to interpret as a logical structure.
> 2. In particular, despite various proposals no satisfactory implication operator has been found (so that there is no deductive system in quantum logic).
> 3. Quantum 'logic' is a propositional language; no satisfactory generalization to predicate logic has been found. 

> Quantum logic is also problematic from a physical perspective. Since (by various theorems and wide agreement) quantum probabilities do not admit an ignorance interpretation, $[0, 1]$-valued truth values attributed to propositions by pure states via the Born rule cannot be regarded as sharp (i.e. {0, 1}-valued) truth values muddled by human ignorance. This implies that, if $X = [a \in \Delta]$ represents a quantum-mechanical proposition, it is wrong to say that either $x$ or its negation holds, but we just do not know which of these alternatives applies. However, in quantum logic one has the law of the excluded middle in the form $x \vee x^\perp = 1$ for all $x$. Thus the formalism of quantum logic does not match the probabilistic structure of quantum theory responsible for its empirical content.

But notice that one may argue that the first three points here are squarely resolved by thinking of BvN-quantum logic as embedded into [[linear logic]], we come back to this in a moment. Concerning the last point one might argue that the propositions in BvN-quantum logic concern the [[quantum measurement]]-outcomes (only), for which, at least in some  [[interpretation of quantum mechanics|interpretations]], it does make sense to speak of a definite result.

In ([Girard 11, page xii](#Girard11)) it says:

>  Among the magisterial mistakes of logic, one will first mention quantum logic, whose ridiculousness can only be ascribed to a feeling of superiority of the language &#8211; and ideas, even bad, as soon as they take a written form &#8211; over the physical world. Quantum logic is indeed a sort of punishment inflicted on nature, guilty of not yielding to the prejudices of logicians... just like Xerxes had the Hellespont &#8211; which had destroyed a boat bridge &#8211; whipped.


For more and more objective criticism see ([Girard 11, section 17](#Girard11)).

Girard had introduced the class of [[formal logic]] systems called _[[linear logic]]_ and it has been argued that [[linear logic]] and more generally _[[linear type theory]]_ does faithfully capture the essence of [[quantum mechanics]] ([Yetter 90](#Yetter90). [Pratt 92](#Pratt92), [Abramsky-Duncan 05](#AbramskyDuncan05), [Duncan 06](#Duncan06)), see ([Baez-Stay 09](#BaezStay09)) for an introductory exposition). This is due to the fact that the [[categorical semantics]] of linear logic is in [[symmetric monoidal categories]] such as those used in the description of [[finite quantum mechanics in terms of dagger-compact categories]]. In particular the [[category]] of (finite dimensional) [[Hilbert spaces]] whose [[subobjects]]/[[propositions]] form the Birkhoff-von Neumann style quantum logic does interpret [[linear logic]].

This is stated explicitly for instance in ([Pratt 92, p.4](#Pratt92)):

> These objections are overcome in the extension of quantum logic to linear logic as a dynamic quantum logic.

Notice that the [[subobjects]] in a category of (finite dimensional) [[Hilbert spaces]], and hence the [[propositions]] in the [[categorical logic]] of Hilbert spaces, are the (closed) linear subspaces. Therefore Birkhoff-von Neumann quantum logic is indeed subsumed as a fragment of linear logic. This (obvious) fact was highlighted in ([Crown 75](#Crown75)) and then later with more of [[categorical logic]] in place and emphasizing [[dagger-category|dagger]]-structures in ([Heunen 08](#Heunen08), [Harding 08](#Harding08) [Heunen-Jacobs 09](#HeunenJacobs09), [Coecke-Heunen-Kissinger 13](#CoeckeHeunenKissinger13)). Also ([CCGP 09, section 9.3](#CCGP09)):

> both orthologic (or weakenings thereof) and linear logic share the failure of lattice distributivity. In particular, the fragment of linear logic that includes just negation and the additive connectives is nothing but a version of the paraconsistent quantum logic PQL.
 
That seems to make much of the above-listed criticism appear in a different light. For instance there is also a natural notion of [[dependent linear type theory]] and that does yield a well-behaved kind of [[predicate logic]] with [[quantifiers]] for linear logic.




## Approaches

### Birkhoff-von Neumann quantum logic

It is based on the setting the [[Hilbert lattice]] (of closed suspaces of a Hilbert space) to represent the set of propositions of quantum system. 

...

[[conjunction]] is given by intersection of two linear subspaces

[[disjunction]] however is given by forming the [[linear space]] of two linear subspaces. Hence [[quantum states]] in the conjunction $A \vee B$ may be [[linear combinations]] of states in $A$ and $B$. This is an incarnation of [[superposition principle]] of [[quantum mechanics]].

as a result, the BvN disjunction does not [[distributivity|distribute]] over conjunction, and hence the BvN lattice is not a [[distributive lattice]].

[[negation]] is given by forming [[orthogonal complement]]

[[Hilbert lattice]]


### Logic of Quantales

On top of the above [[lattice]] of lineat subspaces, take into account that it carries naturally a [[tensor product]]. That makes it a _[[quantale]]_.

### Linear logic

More generally, if we do not just consider the monoidal [[poset]] (quantale) but more generally [[symmetric monoidal categories]] then this is  _[[linear logic]]_, _[[linear type theory]]_

(...)

_[[quantum computing]]_.

(...)

The linearity of the logic, hence the absence of a [[diagonal]] in its [[categorical semantics]], corresponds to the [[no-cloning theorem]] of [[quantum physics]]

### Bohr toposes

See at _[[Bohr topos]]_ for more.


## Related concepts

* [[effect algebra]]

* [[quantum probability]]

* [[interpretation of quantum mechanics]]

* [[order-theoretic structure in quantum mechanics]]

  * [[Kochen-Specker theorem]]

  * [[Alfsen-Shultz theorem]]

  * [[Harding-Döring-Hamhalter theorem]]

* [[Fell's theorem]]

* [[Gleason's theorem]]

* [[Wigner theorem]]

* [[Bell's theorem]]

* [[Bub-Clifton theorem]]

* [[Kadison-Singer problem]]

* [[collapse of the wave function]]

* [[qbit]]

* [[quantum circuit]]

* [[linear logic]], 

* [[quantum mechanics]]

  * [[quantum computing]]

  * [[beable]]

* [[computable physics]]

* [[quantale]], 

* [[Bohr topos]]


## Literature

General introductions and surveys include

* Wikipedia, _[Quantum logic](http://en.wikipedia.org/wiki/Quantum_logic)_

* Stanford encyclopaedia of philosophy, _[Quantum logic and probability theory](http://plato.stanford.edu/entries/qt-quantlog)_

* Kurt Engesser, Dov M. Gabbay, Daniel Lehmann (eds.) _Handbook of Quantum Logic and Quantum Structures: Quantum Logic_, 2009 North Holland

* I. Pitowsky, _Quantum probability &#8212; quantum logic_, Springer Lecture Notes in Physics __321__

* P. Pt&#225;k and S. Pulmannov&#225;, _Orthomodular structures as quantum logics_, ser. Fundamental theories of physics. Kluwer Academic Publishers,
1991.

A bibliography of hundreds of works up to 1992 is

* Mladen Pavi&#269;i&#263;, _Bibliography on quantum logics and related structures_, [pdf](http://www.irb.hr/users/mpavicic/papers-ps-pdf/quantum-logic/1992-int-j-theor-phys-1.pdf).

The original article on quantum logic is

* [[Garrett Birkhoff]], [[John von Neumann]], _The logic of quantum mechanics_, Annals of Mathematics, 37: 823-843 (1936)
 {#BirkhoffvonNeumann36}

Further discussion of this includes 

* A. Gleason, _Measures on the closed subspaces of a Hilbert space_, Journal of Mathematics and Mechanics __6__: 885-893 (1957)

* Samuel S. Holland Jr., _Orthomodularity in infinite dimensions; a theorem of M. Sol&#232;r_, Bull. Amer. Math. Soc. (N.S.) __32__ (1995) 205-234, [arXiv:math.RA/9504224](http://arxiv.org/abs/math/9504224)

Discussion of [[categorical logic]] in [[symmetric monoidal categories]] and hence of [[linear logic]] as quantum logic is in 

* G.D. Crown, _On some orthomodular posets of vector bundles_. Journ. of
Natural Sci. and Math., 15(1-2):11&#8211;25, 1975.
 {#Crown75}

* [[Jean-Yves Girard]], _Linear logic_,   Theoretical Computer Science 50:1, 1987.  ([pdf](http://iml.univ-mrs.fr/~girard/linear.pdf))
 {#Girard}

([Girard 87](#Girard) introduces [[linear logic]] nad suggests a possible relation to [[quantum physics]], but remains undecided on thatM on p. 7 it says: "One of the wild hopes that this suggests is the possibility of a direct connection with quantum mechanics... but let's not dream too much!")

* [[David Yetter]], _Quantales and (noncommutative) linear logic_, Journal of Symbolic Logic 55 (1990), 41-64.
 {#Yetter90}

([Yetter 90](#Yetter90)) observes the the relation of linear logic to [[quantales]], which have otherwise been proposed as providing a quantum logic.)

* [[Vaughan Pratt]], _Linear logic for generalized quantum mechanics_, in Proc. of _Workshop on Physics and Computation (PhysComp'92)_ ([pdf](http://boole.stanford.edu/pub/ql.pdf), [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.137.7817))
 {#Pratt92}

([Pratt 92](#Pratt92) is maybe the first to say fully that linear logic is a good kind of quantum logic.=

* [[Samson Abramsky]], [[Ross Duncan]], _A Categorical Quantum Logic_ ([arXiv:quant-ph/0512114](http://arxiv.org/abs/quant-ph/0512114))
 {#AbramskyDuncan05}

* [[Ross Duncan]], _Types for quantum mechanics_, 2006 ([pdf](http://personal.strath.ac.uk/ross.duncan/papers/rduncan-thesis.pdf), [slides](http://www.cs.ox.ac.uk/people/ross.duncan/talks/2005/pps-22-05-2005.pdf))
 {#Duncan06}

(This highlights more [[linear type theory]] and its use in quantum theory.)

* [[Chris Heunen]], _Quantifiers for quantum logic_ ([arXiv:0811.1457](http://arxiv.org/abs/0811.1457))
 {#Heunen08}

* {#Harding08} [[John Harding]], _A link between quantum logic and categorical quantum mechanics_, Int J Theor Phys (2009) 48: 769&#8211;802

* [[Chris Heunen]], [[Bart Jacobs]], _Quantum Logic in Dagger Kernel Categories_, Order, July 2010, Volume 27, Issue 2, pp 177-212,  ([arXiv:0902.2355](http://arxiv.org/abs/0902.2355))
 {#HeunenJacobs09}

* Gianpiero Cattaneo, Maria Luisa Dalla Chiara, Roberto
Giuntini and Francesco Paoli, section 9 of _Quantum Logic and Nonclassical Logics_, p. 127 in  Kurt Engesser, Dov M. Gabbay, Daniel Lehmann (eds.) _Handbook of Quantum Logic and Quantum Structures: Quantum Logic_, 2009 North Holland
  {#CCGP09}

* [[Samson Abramsky]], _Temperley-Lieb Algebra: From Knot Theory to Logic and Computation via Quantum Mechanics_, In Goong Chen, Louis Kauffman,
and Sam Lomonaco (eds.), _Mathematics of Quantum Computing and Technology_,
pages 415&#8211;458. Taylor and Francis, 2007. ([arXiv:0910.2737](http://arxiv.org/abs/0910.2737))

* [[Jean-Yves Girard]], _[[Lectures on Logic]]_, European Mathematical Society 2011
 {#Girard11}


* Ugo Dal Lago, Claudia Faggian, _On Multiplicative Linear Logic, Modality and Quantum Circuits_ ([arXiv:1210.0613](http://arxiv.org/abs/1210.0613))
 {#LagoFaffian12}

* [[Bob Coecke]], [[Chris Heunen]], [[Aleks Kissinger]], _Compositional Quantum Logic_ ([arXiv:1302.4900](http://arxiv.org/abs/1302.4900))
 {#CoeckeHeunenKissinger13}

That therefore in particular [[categories of cobordisms]] (the domains of [[FQFT|functorial quantum field theory]]) interpret quantum logic qua [[linear logic]] has been highlighted in 

* [[Sergey Slavnov]], _From proof-nets to bordisms: the geometric meaning of
multiplicative connectives_, Mathematical Structures in Computer Science / Volume 15 / Issue 06 / December 2005, pp 1151 - 1178
 {#Slavnov05}

* [[John Baez]], [[Mike Stay]], _Physics, topology, logic and computation: a rosetta stone_, ([arxiv/0903.0340](http://arxiv.org/abs/0903.0340)); in "New Structures for Physics", ed. Bob Coecke, Lecture Notes in Physics __813__, Springer, Berlin, 2011, pp. 95-174
 {#BaezStay09}

Discussion of [[Fock space]]-type free [[quantum field theory]] in [[linear logic]] is in 

*  [[Marcelo Fiore]], _Differential Structure in Models of Multiplicative Biadditive Intuitionistic Linear Logic_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.109.2328))


The proposal that the [[internal logic]] of [[Bohr toposes]] is a good notion of quantum logic is made in

* [[Chris Heunen]], [[Klaas Landsman]], [[Bas Spitters]], _A topos for algebraic quantum theory_, Comm. Math. Phys. 291:63&#8211;110, 2009, free access [doi](http://dx.doi.org/10.1007/s00220-009-0865-6), [arXiv:0709.4364](http://arxiv.org/abs/0709.4364)
 {#HeunenLandsmanSpitters07}

* [[Steve Vickers]], slides from Midland Grad. School 2010, quantum topos theory, [web](http://www.cs.bham.ac.uk/~sjv/teaching/MGS2010), most relevant part IV: [pdf](http://www.cs.bham.ac.uk/~sjv/teaching/MGS2010/slides4.pdf)


See also

* [[Yuri Manin]], _A course in mathematical logic_, Springer 

*  &#1044;.&#1048;. &#1041;&#1083;&#1086;&#1093;&#1080;&#1085;&#1094;&#1077;&#1074;, &#1055;&#1088;&#1080;&#1085;&#1094;&#1080;&#1087;&#1080;&#1072;&#1083;&#1100;&#1085;&#1099;&#1077; &#1074;&#1086;&#1087;&#1088;&#1086;&#1089;&#1099; &#1082;&#1074;&#1072;&#1085;&#1090;&#1086;&#1074;&#1086;&#1081; &#1084;&#1077;&#1093;&#1072;&#1085;&#1080;&#1082;&#1080;, 1966, 162 &#1089;.


* A. Sudbery, _Quantum mechanics and the particles of nature_, An outline for mathematicians, Camb. Univ. Press 1986

* Stanford Encyclopedia of Philosophy, [qm: von Neumann vs. Dirac](http://plato.stanford.edu/entries/qt-nvd), 

[[!redirects quantum logics]]
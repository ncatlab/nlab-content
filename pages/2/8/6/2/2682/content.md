
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

### recalling the context ##

The undertaking called [[string theory]] started out as _perturbative string theory_ where the idea was to encode [[spacetime]] [[physics]] in [[perturbation theory]] by an [[S-matrix]] that is obtained by a sum of the integrals of the [[correlators]] of a fixed 2-dimensional [[conformal field theory]] over the [[moduli space]]s of conformal structures on surfaces of all possible genera -- thought of as the [[second quantization]] of a [[string]] [[sigma-model]].

The [[S-matrix]] elements obtained this way from the [[string perturbation series]] could be seen to be approximated by an ordinary [[effective QFT]] (some flavor of [[supergravity]] coupled to [[gauge theory]] and [[fermion]]s) on [[target space]]. 

Moreover, the precise choice of 2d [[CFT]] also encodes a [[Euler-Lagrange equation|classical solution]] of the effective background QFT, hence a [[vacuum]] of that theory.

The _first superstring revolution_ was given by the realization that this makes sense: the effective background theories obtained this way are indeed free of [[quantum anomaly|quantum anomalies]].

### narrowing in on the issue ##

The _second superstring revolution_ was given by the realization that all these background field theories seem to fit into one single bigger context that seems to exists independently of their perturbatve definitions. 

Aspects of this bigger non-perturbative context are known as [[M-theory]]. While one couldn't figure out what that actually is, the circumstancial evidence suggested that whatever it is, it has a low-energy limit where it also looks like an effective background field theory, this time [[11-dimensional supergravity]].

In a different but similar manner, other background field theories were found whose classical solutions are thought to encode "stable solutions" ("[[vacuum]] solutions") of whatever physical theory this non-perturbative definition of string theory is.

Here, when talking about a "stable solution" one thinks of solutions of these theories of [[gravity]] with plenty of extra fields that look like [[Minkowski space]] times something else, such that all these extra fields are constant in time (using the simple Minkowsi-space-times-internal-part-ansatz to say what "constant in time" means), hence sitting at the bottom of their corresponding effective potentials.

Solutions with this property, in particular for all the scalar fields that appear, are said to have _stabilized moduli_ : the scalar fields that encode various properties of the geometry of the solution are constant in time.

Since these geometric properties determine, in the fashion of [[Kaluza-Klein theory]], the effective physics in the remaining [[Minkowski space]] factor, it is these "moduli-stabilized" solutions that have a first chance of being candidate solutions of whatever that theory is we are talking about, which describe the real world.

### the landscape 

At some point there had been the hope that only very few such solutions exist. When arguments were put forward that this is far from being true, the term **landscape** for the collection of all such solutions was invented.


So, to summarize in a few words, the landscape of string theory vacua is...

## Flux compactifications 

One widely studied class of modli-stabilized solutions to the string-theory background equations is that of **[[flux compactifications]]**.

These are classical solutions to the corresponding [[supergravity]] theory that are of the form $M^4 \times CY$ with $CY$ some [[Calabi-Yau manifold]] of six real dimensions such that the [[RR-field]] in the solution has nontrivial values on $CY$. Its components are called the _[[fluxes]]_ .

The presence of this [[RR-field]] in the solution induces an effective potential for the scalar moduli fields that parameterize the geometry of CY. Hence by choosing the [[RR-field]] suitably one can find classical solutions in which all these moduli have values that are constant in time.

A review of flux compactifications is for instance in ([Gra&#241;a 05](#Grana05))

## Related concepts

> at least one thing missing in the discussion here is the subtlety explained out by [[Jacques Distler]] in blog dicussion [here](http://golem.ph.utexas.edu/category/2009/10/structural_foundations_of_quan.html#c028474)


* [[string theory]]

  * [[heterotic string theory]]

    * [[Green-Schwarz mechanism]]

   * [[dual heterotic string theory]]

  * [[type II string theory]]

* [[vacuum]], [[false vacuum]]

* [[model (in particle physics)]]

  * [[standard model of particle physics]]

  * [[Grand Unified Theory]], [[MSSM]]

* [string theory FAQ - Does string theory make predictions?](string+theory+FAQ#HowDoesStringTheoryMakePredictions)

* [string theory FAQ -- What does it mean to say that string theory has a "landscape of solutions"?](http://ncatlab.org/nlab/show/string+theory+FAQ#WhatDoesItMeanToSayStringTheoryHasALandscapeOfSolutions)

## References

### Moduli space of 2s CFTs

Some general thoughts on what a [[moduli space]] of 2d CFTs should be are in 

* [[Michael Douglas]], _Spaces of Quantum Field Theories_ ([arXiv:1005.2779](http://arxiv.org/abs/1005.2779))

The compactness results mentioned there are discussed in 

* [[Yan Soibelman]], _Collapsing CFTs, spaces with non-negative Ricci curvature and nc geometry_ in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011)

based on conjectures in 

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Homological Mirror Symmetry and
torus fibrations_ , ([math.SG/0011041](http://arxiv.org/abs/math/0011041))

Discussion of aspects of [[effective field theories]] which might rule them out as having a [[UV-completion]] by a [[string theory]] [[vacuum]] has been initiated in 

* [[Cumrun Vafa]], _The String Landscape and the Swampland_ ([arXiv:hepth/0509212](http://arxiv.org/abs/hepth/0509212))

### Phenomenological speculation
 {#ReferencesPhenomenologicalSpeculation}

Early and technical articles that amplified the existence of a finite but very large number of string theory compactifications are

* [[Wolfgang Lerche]], [[Dieter Lüst]], [[Bert Schellekens]], _Ten dimensional heterotic strings from Niemeier lattices_, Physics Letters B, Volume 181, Issues 1-2, 1986 ([pdf](http://cds.cern.ch/record/170910/files/198609340.pdf))

which says on p. 2

> Although the consistenty requirements which string theories have to satisfy are quite restrictive, it has become clear that there are more solutions than one originally expected. [...] Although the possibility of making Lorentz rotations suggests a continuous infinity of new ten dimensional theories, there is actually only a discrete set of theories that makes physical sense, as we will explain below.

and


* [[Wolfgang Lerche]], [[Dieter Lüst]], [[Bert Schellekens]], _Chiral Four-dimensional Heterotic Strings from Self-dual Lattices_  Nucl. Phys. B 287, 477, 1987 ([pdf](http://lerche.web.cern.ch/lerche/papers/4dhetstrings.pdf))

which says in conclusion on page 45-46

> Although the number of chiral theories of this type is finite, our results suggest that there exist very many of them, so that a complete enumeration appears impossible.

A popular account of these observations was given in

* {#Schellekens98} [[Bert Schellekens]], _Naar een waardig slot_, inauguration speech ar University of Nijmegen, September 1998, ISBN 90-9012073-4

a commented translation of which later appeared as

* {#Schellekens06} [[Bert Schellekens]], _The Landscape "avant la lettre"_ ([arXiv:physics/0604134](http://arxiv.org/abs/physics/0604134))

These articles, and this speech, did not cause much of excitement then. Also they did not discuss [[moduli]] stabilization, which could still have been thought to reduce the number of vacua. Excitement was only later caused instead by more vague discussion of flux compactification vacua with moduli stabilization in type IIB string theory:

That there are $10^{hundreds}$ different flux compactifications was maybe first said explicitly in 

* [[Raphael Bousso]], [[Joseph Polchinski]], _Quantization of Four-form Fluxes and Dynamical Neutralization of the Cosmological Constant_ ([arXiv:hep-th/0004134](http://arxiv.org/abs/hep-th/0004134))

The idea became popular with the articles

* [[Leonard Susskind]], _The Anthropic Landscape of String Theory_ ([arXiv:hep-th/0302219](http://arxiv.org/abs/hep-th/0302219))

* [[Shamit Kachru]], [[Renata Kallosh]], [[Andrei Linde]], [[Sandip  Trivedi]], _de Sitter Vacua in String Theory_, Phys. Rev. D68:046005, 2003 ([arXiv:hep-th/0301240](http://arxiv.org/abs/hep-th/0301240))

* [[Joseph Polchinski]], _The Cosmological Constant and the String Landscape_ ([arXiv:hep-th/0603249](http://arxiv.org/abs/hep-th/0603249))

The specific (but arbitrary) value  "$10^{500}$" for the typical number of flux compactification, which became iconic in public discussion of the issue, seems to originate with [[Michael Douglas]]. An early appearance in print is p. 3 of

* [[Ralph Blumenhagen]], [[Florian Gmeiner]], [[Gabriele Honecker]], [[Dieter Lüst]], [[Timo Weigand]], _The Statistics of Supersymmetric D-brane Models_, Nucl.Phys.B713:83-135, 2005 ([arXiv:hep-th/0411173](http://arxiv.org/abs/hep-th/0411173))

A review of the issue of flux compactifications is in

* [[Mariana Graña]], _Flux compactifications in string theory: a comprehensive review_ ([arXiv:hep-th/0509003](http://arxiv.org/abs/hep-th/0509003))
 {#Grana05}

General considerations on this state of affairs are in

* [[Frank Wilczek]], _Multiversality_ ([arXiv:1307.7376](http://arxiv.org/abs/1307.7376))


The fact that in principle all the parameters of the "landscape" of string theory vacua are dynamical (are moduli fields) and the idea that an [[eternal cosmic inflation]] might be something like an [[ergodic process]] in this landscape has led to ideas to connect this to [[phenomenology]] and the [[standard model of cosmology]]/[[standard model of particle physics]] by way of [[statistical mechanics]].

Summaries of this line of thinking include

* [[Raphael Bousso]], _The State of the Multiverse:
The String Landscape, the Cosmological
Constant, and the Arrow of Time_, 2011 ([pdf](http://www.ctc.cam.ac.uk/stephen70/talks/swh70_bousso.pdf))

For more on this see the references at _[[eternal inflation]]_.



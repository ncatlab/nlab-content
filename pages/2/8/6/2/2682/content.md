

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### recalling the context ##

The undertaking called [[string theory]] started out as _perturbative string theory_ where the idea was to encode [[spacetime]] [[physics]] in [[perturbation theory]] by an [[S-matrix]] that is obtained by a sum of the integrals of the [[correlators]] of a fixed [[2d superconformal field theory]] over the [[moduli spaces]] of conformal structures on surfaces of all possible genera -- thought of as the [[second quantization]] of a [[string]] [[sigma-model]].

The [[S-matrix]] elements obtained this way from the [[string perturbation series]] could be seen to be approximated by an ordinary [[effective QFT]] (some flavor of [[supergravity]] coupled to [[gauge theory]] and [[fermion]]s) on [[target space]]. 

(The _first superstring revolution_ was given by the realization that this makes sense: the effective background theories obtained this way are indeed free of [[quantum anomaly|quantum anomalies]].)


Hence it is the chocie of [[worldsheet]] [[2d SCFT]] which in [[perturbative string theory]] translates products of "field insertions" into [[scattering amplitudes]]. In [[perturbative AQFT]] it is the choice of [[vacuum state]] which does this, and therefore [[2d SCFTs]] are the [[perturbative string theory vacua]]. 


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

* [[cosmological constant]]

* [[axionic landscape]]

* [[string theory]]

  * [[heterotic string theory]]

    * [[Green-Schwarz mechanism]]

   * [[dual heterotic string theory]]

  * [[type II string theory]]

* **[[vacuum]]**

  * [[vacuum state]], [[Hadamard state]]

  * [[interacting vacuum]]

  * [[vacuum expectation value]], [[vacuum amplitude]], [[vacuum fluctuation]]

  * [[vacuum energy]]

  * [[vacuum diagram]]

  * [[vacuum stability]]

  * [[false vacuum]], [[tachyon]], [[Coleman-De Luccia instanton]]

  * [[theta vacuum]]

  * [[perturbative string theory vacuum]]

  * [[landscape of string theory vacua]]


* [[moduli field]], [[multiverse]]

* [[model (in particle physics)]]

  * [[standard model of particle physics]]

  * [[Grand Unified Theory]], [[MSSM]]

* [[Brandenberger-Vafa mechanism]]

* [string theory FAQ - Does string theory make predictions?](string+theory+FAQ#HowDoesStringTheoryMakePredictions)

* [string theory FAQ -- What does it mean to say that string theory has a "landscape of solutions"?](http://ncatlab.org/nlab/show/string+theory+FAQ#WhatDoesItMeanToSayStringTheoryHasALandscapeOfSolutions)

## References

### F-theory flux compactification

Surveys of the general story of [[flux compactification]] in [[F-theory]] includes

* {#Denef08} [[Frederik Denef]], _Les Houches Lectures on Constructing String Vacua_, in _[[String theory and the real world]]_ ([arXiv:0803.1194](http://arxiv.org/abs/0803.1194))


### Moduli space of 2d CFTs

Scan of the moduli space of semi-realistic [[type II string theory|type IIB]] CFTs compactfied on [[orbifolds]] of [[Gepner models]] is in 

* T.P.T. Dijkstra, L. R. Huiszoon, [[Bert Schellekens]], _Supersymmetric Standard Model Spectra from RCFT orientifolds_, Nucl. Phys.B 710:3-57,2005 ([arXiv:hep-th/0411129](https://arxiv.org/abs/hep-th/0411129))

Some general thoughts on what a [[moduli space]] of 2d CFTs should be are in 

* [[Michael Douglas]], _Spaces of Quantum Field Theories_ ([arXiv:1005.2779](http://arxiv.org/abs/1005.2779))

The compactness results mentioned there are discussed in 

* {#Soibelman11} [[Yan Soibelman]], _Collapsing CFTs, spaces with non-negative Ricci curvature and nc geometry_ in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011)

based on conjectures in 

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Homological Mirror Symmetry and
torus fibrations_ , ([math.SG/0011041](http://arxiv.org/abs/math/0011041))

Discussion of aspects of [[effective field theories]] which might rule them out as having a [[UV-completion]] by a [[string theory]] [[vacuum]] has been initiated in 

* {#Vafa05} [[Cumrun Vafa]], _The String Landscape and the Swampland_ ([arXiv:hepth/0509212](http://arxiv.org/abs/hepth/0509212))

See also

* {#BrennanCartaVafa17} T. Daniel Brennan, Federico Carta, [[Cumrun Vafa]], _The String Landscape, the Swampland, and the Missing Corner_ ([arXiv:1711.00864](https://arxiv.org/abs/1711.00864))

* Ben Heidenreich, [[Matthew Reece]], Tom Rudelius, _Emergence and the Swampland Conjectures_ ([arXiv:1802.08698](https://arxiv.org/abs/1802.08698))

### Phenomenological speculation
 {#ReferencesPhenomenologicalSpeculation}

Early and technical articles that amplified the existence of a finite but very large number of string theory compactifications are

* {#LercheLustSchellekens86} [[Wolfgang Lerche]], [[Dieter Lüst]], [[Bert Schellekens]], _Ten dimensional heterotic strings from Niemeier lattices_, Physics Letters B, Volume 181, Issues 1-2, 1986 ([pdf](http://cds.cern.ch/record/170910/files/198609340.pdf))

which says on p. 2

> Although the consistency requirements which string theories have to satisfy are quite restrictive, it has become clear that there are more solutions than one originally expected. [...] Although the possibility of making Lorentz rotations suggests a continuous infinity of new ten dimensional theories, there is actually only a discrete set of theories that makes physical sense, as we will explain below.

and

* {#LercheLustSchellekens87} [[Wolfgang Lerche]], [[Dieter Lüst]], [[Bert Schellekens]], _Chiral Four-dimensional Heterotic Strings from Self-dual Lattices_  Nucl. Phys. B 287, 477, 1987 ([pdf](http://lerche.web.cern.ch/lerche/papers/4dhetstrings.pdf))

which says in conclusion on page 45-46

> Although the number of chiral theories of this type is finite, our results suggest that there exist very many of them, so that a complete enumeration appears impossible.

A popular account of these observations was given in

* {#Schellekens98} [[Bert Schellekens]], _Naar een waardig slot_, inauguration speech ar University of Nijmegen, September 1998, ISBN 90-9012073-4

a commented translation of which later appeared as

* {#Schellekens06} [[Bert Schellekens]], _The Landscape "avant la lettre"_ ([arXiv:physics/0604134](http://arxiv.org/abs/physics/0604134))

Similarly

* [[Bert Schellekens]], _Big Numbers in String Theory_ ([arXiv:1601.02462](http://arxiv.org/abs/1601.02462))

The articles [Lerche-L&#252;st-Schellekens 86](#LercheLustSchellekens86), [Lerche-L&#252;st-Schellekens 87](#LercheLustSchellekens87), and the speech [Schellekens 98](#Schellekens98), did not cause much of excitement then. Also they did not discuss [[moduli stabilization]], which could still have been thought to reduce the number of vacua. Excitement was only later caused instead by more vague discussion of flux compactification vacua with moduli stabilization in type IIB string theory:

That there are $10^{hundreds}$ different flux compactifications was maybe first said explicitly in 

* [[Raphael Bousso]], [[Joseph Polchinski]], _Quantization of Four-form Fluxes and Dynamical Neutralization of the Cosmological Constant_ ([arXiv:hep-th/0004134](http://arxiv.org/abs/hep-th/0004134))

The idea became popular in discussion of the [[cosmological constant]] with the alleged construction of a large set of metastable [[de Sitter spacetime]]-vacua in

* {#KKLT03} [[Shamit Kachru]], [[Renata Kallosh]], [[Andrei Linde]], [[Sandip  Trivedi]], _de Sitter Vacua in String Theory_, Phys. Rev. D68:046005, 2003 ([arXiv:hep-th/0301240](http://arxiv.org/abs/hep-th/0301240))

  ("KKLT", a good quick review is in [Danielsson-VanRiet 18 section 2.5.1](#DanielssonVanRiet18), also [Ibanez-Uranga 12, section 15.3.1](#IbanezUranga12))

and the amplification of the complication of the [KKLT 03](#KKLT03)-construction its alleged vastness in

* {#Susskind03} [[Leonard Susskind]], _The Anthropic Landscape of String Theory_, in B. Carr (ed.) _Universe or multiverse_, 247-266 ([arXiv:hep-th/0302219](http://arxiv.org/abs/hep-th/0302219))

  "The vacua in [KKLT 03](#KKLT03) are not at all simple.  They are jury-rigged, [Rube Goldberg contraptions](https://en.wikipedia.org/wiki/Rube_Goldberg_machine) that could hardly have fundamental significance." (p. 5)

* [[Joseph Polchinski]], _The Cosmological Constant and the String Landscape_ ([arXiv:hep-th/0603249](http://arxiv.org/abs/hep-th/0603249))

Review includes

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 15.3 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012

(Beware that the approach of [KKLT 03](#KKLT03) is argued to be false in [DanielssonVanRiet 18](#Danielsson-VanRiet18) and is being abandoned in [Obied-Ooguri-Spodyneiko-Vafa 18](#ObiedOoguriSpodyneikoVafa18), [Danielsson et. al 18](#de+Sitter+spacetime#BDDGS18)).


The specific (but arbitrary) value  "$10^{500}$" for the typical number of flux compactification, which became iconic in public discussion of the issue, originates in 

* {#Douglas04} [[Michael Douglas]], p. 4 of _Basic results in vacuum statistics_, Comptes Rendus Physique, vol. 5, pp. 965&#8211;977, 2004 ([arXiv:hep-th/0409207](http://arxiv.org/abs/hep-th/0409207))

* [[Ralph Blumenhagen]], [[Florian Gmeiner]], [[Gabriele Honecker]], [[Dieter Lüst]], [[Timo Weigand]], p.3 of _The Statistics of Supersymmetric D-brane Models_, Nucl.Phys.B713:83-135, 2005 ([arXiv:hep-th/0411173](http://arxiv.org/abs/hep-th/0411173))

* [[Michael Douglas]], [[Shamit Kachru]], p. 55 of _Flux Compactification_, Rev.Mod.Phys.79:733-796,2007 ([arXiv:hep-th/0610102](https://arxiv.org/abs/hep-th/0610102))


Previously 

* [[Suyay Ashok]], [[Michael Douglas]], _Counting flux vacua_, JHEP, vol. 0401, p. 060, 2004

had considered $10^{120}$ and earlier [Lerche-L&#252;st-Schellekens 87](#LercheLustSchellekens87) had $10^{1500}$.

A review of the issue of flux compactifications is in

* {#Grana05} [[Mariana Graña]], _Flux compactifications in string theory: a comprehensive review_ ([arXiv:hep-th/0509003](http://arxiv.org/abs/hep-th/0509003))
 

General considerations on this state of affairs are in

* [[Frank Wilczek]], _Multiversality_ ([arXiv:1307.7376](http://arxiv.org/abs/1307.7376))


The fact that in principle all the parameters of the "landscape" of string theory vacua are dynamical (are moduli fields) and the idea that an [[eternal cosmic inflation]] might be something like an [[ergodic process]] in this landscape has led to ideas to connect this to [[phenomenology]] and the [[standard model of cosmology]]/[[standard model of particle physics]] by way of [[statistical mechanics]].

Summaries of this line of thinking include

* [[Raphael Bousso]], _The State of the Multiverse:
The String Landscape, the Cosmological
Constant, and the Arrow of Time_, 2011 ([pdf](http://www.ctc.cam.ac.uk/stephen70/talks/swh70_bousso.pdf))

For more on this see the references at _[[multiverse]]_ and _[[eternal inflation]]_.

On the other hand, discussion casting doubt on the existence of a large number of [[de Sitter spacetime]] [[perturbative string theory vacua]] includes the following:

* [[Tom Banks]], _The Top $10^{500}$ Reasons Not to Believe in the Landscape_ ([arXiv:1208.5715](https://arxiv.org/abs/1208.5715))

* [Brennan-Carta-Vafa 17](#BrennanCartaVafa17)

* {#DanielssonVanRiet18} [[Ulf Danielsson]], Thomas Van Riet,  _What if string theory has no de Sitter vacua?_ ([arXiv:1804.01120](https://arxiv.org/abs/1804.01120))

Implications of the possible non-existence of de Sitter vacua in string theory are explored in

* {#ObiedOoguriSpodyneikoVafa18} Georges Obied, [[Hirosi Ooguri]], Lev Spodyneiko, [[Cumrun Vafa]], _De Sitter Space and the Swampland_ ([arXiv:1806.08362](https://arxiv.org/abs/1806.08362))

* {#AgrawalObiedSteinhardtVafa18} Prateek Agrawal, Georges Obied, Paul Steinhardt, [[Cumrun Vafa]], _On the Cosmological Implications of the String Swampland_ ([arXiv:1806.09718](https://arxiv.org/abs/1806.09718))

* {#Vafa18} [[Cumrun Vafa]], _Cosmology and the String Swampland_, talk at _[Strings 2018](https://indico.oist.jp/indico/event/5/)_ ([pdf slides](https://indico.oist.jp/indico/event/5/picture/96.pdf), [recording](https://www.youtube.com/watch?v=fU8sJRCRz24&t=1904s))

But then:

* Jakob Moritz, Ander Retolaza, Alexander Westphal, _Towards de Sitter from 10D_, Phys. Rev. D 97, 046010 (2018) ([arXiv:1707.08678](https://arxiv.org/abs/1707.08678))


See also

* {#Sethi17} [[Savdeep Sethi]], _Supersymmetry Breaking by Fluxes_ ([arXiv:1709.03554](https://arxiv.org/abs/1709.03554))





+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[perturbative string theory]] [[scattering amplitudes]] are defined as in [[quantum field theory]], but with [[n-point functions]] of 1-dimensional [[worldline theories]] ([[Feynman diagrams]]) replaced by those of [[worldsheet]] [[2d CFTs]]. 

<img src="https://ncatlab.org/nlab/files/StringFeynmanDiagrams.png" width="300">

> graphics grabbed from [Penrose 04](https://en.m.wikipedia.org/wiki/The_Road_to_Reality), per [Jurke 10](https://benjaminjurke.com/content/articles/2010/string-theory/) 


## Properties

### Finiteness
 {#Finiteness}

The amplitudes are thought (see the commented [references below](#References)) to come out term-wise (for each "loop order" hence for each [[genus]] and number of punctures of ([[super Riemann surface|super]]-)[[Riemann surfaces]]) finite (at least UV-finite), hence [[renormalization|renormalized]]: the higher string oscillations may be seen as providing canonical counterterms for the massless excitations in the [[effective field theory]]. In this sense string theory provides a [[UV-completion]] of these effective field theories ([[supergravity]] coupled to [[Yang-Mills theory]]).

+-- {: .num_remark}
###### Remark

The full [[perturbation series]] is the [[sum]] of all these (finite) contributions over the [[genus|genera]] of [[Riemann surfaces]] (the "loop orders"). This _sum_ diverges, even if all loop orders are finite. Notice though, that a non-trivial [[perturbation theory|perturbative]] [[QFT]] is not supposed to have a finite [[radius of convergence]] of its scattering amplitudes, since that would imply convergence also for _negative_ [[coupling constant]], which is physically unreasonable. (For the [[bosonic string]] the perturbation series has apparently been explicitly shown not to be [[Borel summation|Borel resummable]].) For more on this see at _[[non-perturbative effect]]_ and _[string theory FAQ -- Is the divergence of the pertubation series fatal?](string+theory+FAQ#NonConvergenceOfPerturbationSeries)_.

=--

+-- {: .num_remark}
###### Remark

A string scattering amplitude is called _UV-finite_ at a given loop order ([[genus]] of a [[Riemann surface]] $\Sigma$ with $n$ marked points/string insertions) if the [[correlation function]] $\langle \phi_1, \cdots, \phi_n\rangle_{\Sigma}$ is finite for every single such [[Riemann surface]]. The actual string amplitude at order $(g,n)$ though is the averaging of this over all possible [[conformal structures]] on $\Sigma$, hence the  [[integration]] of the [[correlation function]], as a function on the conformal structure, over the compactified [[moduli space of conformal structures]] $\mathcal{M}_{g,n}$ (a [[Deligne-Mumford stack]]). 

If also this integral is finite, hence if the total [[measure]] on the [[moduli space of conformal structures]] is finite, then one says the amplitude is _IR-finite_.

This distinction between UV-finiteness and IR-finiteness is not always highlighted in all of the articles below. All authors argue that the string is _UV-finite_ to all order. The IR-finiteness is only discussed much more recently at low loop order.

IR non-finiteness is not physically fatal. For instance if a [[perturbation theory|perturbative]] theory of [[quantum gravity]] develops a [[cosmological constant]] perturbatively, then the perturbation series will be IR-divergent, signifying the fact that background spacetime without cosmological constant is no longer a solution to the quantum-corrected [[equations of motion]]. Nevertheless, these potential IR-divergences seem to be absent for the [[superstring]] perturbation series. For the [[cosmological constant]] case this can already be seen from the fact that the [[effective QFT]] of [[type II supergravity]] etc. does not admit a cosmological constant, for that would violate [[supersymmetry]].

=--

### Open-closed scattering duality and KLT relations

The [[open/closed string duality]] implies certain relations in string scattering amplitudes that in the point-particle limit induces relations between [[scattering amplitudes]] in [[Yang-Mills theory]] and in [[gravity]]. These are the _[[KLT relations]]_ in [[QFT]]. See in particular [Mafra-Schlotterer 18a](#MafraSchlotterer18a), [Mafra-Schlotterer 18b](#MafraSchlotterer18b), [Mafra-Schlotterer 18c](#MafraSchlotterer18c).

### Twistor string amplitudes and MHV amplitudes in Yang-Mills theory

The scattering amplitudes in [[twistor string theory]] induce the MHV amplitudes in ([[super Yang-Mills theory|super]]-)[[Yang-Mills theory]]. See at _[[string theory results applied elsewhere]]_ in the section _[Application to QCD -- Scattering amplitudes](string+theory+results+applied+elsewhere#QCDScatteringAmplitudes)_.

### $p$-Adic formulation

The [[Veneziano amplitude]] (open bosonic string tree-level scattering) has an equivalent formulation as the inverse product over all [[prime numbers]] $p$ of an amplitude computed not by an integral in the real but in the [[p-adic numbers]]. For other open string amplitudes this holds up to some regularization. This is the topic of _[[p-adic string theory]]_, see there for more details.

## Examples

* [[Veneziano amplitude]]

* [[Virasoro-Shapiro amplitude]]

* [[vacuum amplitude]]

## Related entries

* [[scattering amplitude]]

* [[perturbation theory]], [[perturbative string theory]]

* [[non-perturbative effect]], [[M-theory]]

* [[string theory FAQ]], [[string theory results applied elsewhere]]

## References
 {#References}

### General
 {#General}

A comprehensive account of the [[superstring]] [[S-matrix]] may be obtained from combining the general idea presented in

* {#Polchinski01} [[Joseph Polchinski]], section 12.5 of vol 2 of _String theory_, Cambridge Monographs on Mathematical Physics (2001)

with the technical details laid out in

* {#Witten12} [[Edward Witten]], _Superstring Perturbation Theory Revisited_ ([arXiv:1209.5461](https://arxiv.org/abs/1209.5461))

* {#Witten13} [[Edward Witten]], _More On Superstring Perturbation Theory: An Overview Of Superstring Perturbation Theory Via Super Riemann Surfaces_ ([arXiv:1304.2832](https://arxiv.org/abs/1304.2832))

Survey of the tree level string scattering amplitudes includes

* [[Ralph Blumenhagen]], [[Dieter Lüst]], [[Stefan Theisen]], _String Scattering Amplitudes and Low Energy Effective Field Theory_, chapter 16 in _Basic Concepts of String Theory_ Part of the series Theoretical and Mathematical Physics pp 585-639 Springer 2013 ([TOC pdf](https://link.springer.com/content/pdf/bfm%3A978-3-642-29497-6%2F1.pdf), [publisher page](http://www.springer.com/gp/book/9783642294969))

* [[Katrin Becker]], [[Melanie Becker]], Ilarion V. Melnikov, Daniel Robbins, Andrew B. Royston, _Some tree-level string amplitudes in the NSR formalism_, JHEP 12 (2015) 010 ([arXiv:1507.02172](http://arxiv.org/abs/1507.02172))

See also 

* {#Moore93} [[Gregory Moore]], _Symmetries of the Bosonic String S-Matrix_ ([arXiv:hep-th/9310026](https://arxiv.org/abs/hep-th/9310026))

* Gaston Giribet, Nicholas Labranche, Joan La Madrid, *Comments on the two-point string amplitudes* &lbrack;[arXiv:2303.15658](https://arxiv.org/abs/2303.15658)&rbrack;

* [[Nima Arkani-Hamed]], Carolina Figueiredo, [[Grant N. Remmen]]: *Open String Amplitudes: Singularities, Asymptotics, and New Representations* &lbrack;[arXiv:2412.20639](https://arxiv.org/abs/2412.20639)&rbrack;

* Carolina Figueiredo, Marcos Skowronek: *Cuts and Contours* &lbrack;[arXiv:2506.05456](https://arxiv.org/abs/2506.05456)&rbrack;




On string scattering amplitudes in view of the [[S-matrix bootstrap]]:

* Andrea Guerrieri, Joao Penedones, Pedro Vieira, _Where is String Theory?_ ([arXiv:2102.02847](https://arxiv.org/abs/2102.02847))

For more references see also at *[[string theory results applied elsewhere]]*.


### Superstring scattering

A review of superstring scattering amplitudes is in the last section of ([Staessens-Vernocke 10](#StaessensVernocke10)). A general discussion of the problem of superstring amplitudes is in 

* [[Eric D'Hoker]],  [[Duong Phong]]: _Loop amplitudes for the fermionic string_, Nucl. Phys. B 278 (1986) 225;

* [[Greg Moore]], P. Nelson, [[Joseph Polchinski]], _Strings and supermoduli_, Phys. Lett. B 169 (1986) 47-53.

On analycity of the superstring [[S-matrix]]:

* {#dLES18} Corinne de Lacroix, Harold Erbin, [[Ashoke Sen]], _Analyticity and Crossing Symmetry of Superstring Loop Amplitudes_ ([arXiv:1810.07197](https://arxiv.org/abs/1810.07197))

Survey of the presence and role of divergences:

* [[Ashoke Sen]], _Ultraviolet and Infrared Divergences in Superstring Theory_ ([arXiv:1512.00026](http://arxiv.org/abs/1512.00026))

Review of the scattering of massive modes in [[type IIB string theory]]:

* Nicholas Agia, *Massive Type IIB Superstrings Part I: 3- and 4-Point Amplitudes* &lbrack;[arXiv:2309.11538](https://arxiv.org/abs/2309.11538)&rbrack;

See also:

* Sergio Luigi Cacciatori, Samuel Grushevsky, [[Alexander A. Voronov]], *Tree-Level Superstring Amplitudes: The Neveu-Schwarz Sector* &lbrack;[arXiv:2403.09600](https://arxiv.org/abs/2403.09600)&rbrack;


Discussion of superstring scattering amplitudes in terms of [[pure spinors]] ([[Berkovits superstring]]) with emphasis on [[KLT relations]]:

* {#MafraSchlotterer18a} [[Carlos Mafra]], [[Oliver Schlotterer]], _Towards the $n$-point one-loop superstring amplitude I: Pure spinors and superfield kinematics_ ([arXiv:1812.10969](https://arxiv.org/abs/1812.10969))

* {#MafraSchlotterer18b} [[Carlos Mafra]], [[Oliver Schlotterer]], _Towards the $n$-point one-loop superstring amplitude II: Worldsheet functions and their duality to kinematics_ ([arXiv:1812.10970](https://arxiv.org/abs/1812.10970))

* {#MafraSchlotterer18c} [[Carlos Mafra]], [[Oliver Schlotterer]], _Towards the $n$-point one-loop superstring amplitude III: One-loop correlators and their double-copy structure_ ([arXiv:1812.10971](https://arxiv.org/abs/1812.10971))


* [[Carlos R. Mafra]], [[Oliver Schlotterer]], *Tree-level amplitudes from the pure spinor superstring* &lbrack;[arXiv:2210.14241](https://arxiv.org/abs/2210.14241)&rbrack;


For more see also at _[[superstring field theory]]_, such as

* Corinne de Lacroix, [[Harold Erbin]], Sitender Pratap Kashyap, [[Ashoke Sen]], Mritunjay Verma, _Closed Superstring Field Theory and its Applications_,  International Journal of Modern Physics AVol. 32, No. 28n29, 1730021 (2017) ([arXiv:1703.06410](https://arxiv.org/abs/1703.06410))

The [[1-loop]] amplitudes in [[type II string theory]] have been discussed in 

* [[Michael Green]], [[John Schwarz]], _Supersymmetrical string theories_, Phys. Lett. 109 B (1982) 444-448.

and for [[heterotic string theory]] in 

* [[David Gross]], J.A. Harvey, E.J. Martinec and R. Rohm, _Heterotic String Theory (II). The interacting heterotic string_, Nucl. Phys. B267 (1986) 75.

The description of [[2-loop]] amplitudes, including the [[Berezin integral]] over the super-[[moduli space of super Riemann surfaces]] in superstring theory:

* {#DHokerPhong02} [[Eric D'Hoker]], [[Duong Phong]], _Two-Loop Superstrings I, Main Formulas_, Phys. Lett. B529:241-255, 2002 ([arXiv:hep-th/0110247](http://arxiv.org/abs/hep-th/0110247))

* [[Eric D'Hoker]], [[Duong Phong]], _Two-Loop Superstrings II, The Chiral Measure on Moduli Space_, Nucl. Phys. B636:3-60, 2002 ([arXiv:hep-th/0110283](http://arxiv.org/abs/hep-th/0110283))

* [[Eric D'Hoker]], [[Duong Phong]], _Two-Loop Superstrings III, Slice Independence and Absence of Ambiguities_, Nucl. Phys. B636:61-79, 2002 ([arXiv:hep-th/0111016](http://arxiv.org/abs/hep-th/0111016))

* [[Eric D'Hoker]], [[Duong Phong]], _Two-Loop Superstrings IV, The Cosmological Constant and Modular Forms_, Nucl. Phys. B639:129-181, 2002 ([arXiv:hep-th/0111040](http://arxiv.org/abs/hep-th/0111040))

* [[Eric D'Hoker]], [[Duong Phong]], _Two-Loop Superstrings V: Gauge Slice Independence of the N-Point Function_, Nucl. Phys. B715:91-119, 2005 ([arXiv:hep-th/0501196](http://arxiv.org/abs/hep-th/0501196))

* [[Eric D'Hoker]], [[Duong Phong]], _Two-Loop Superstrings VI: Non-Renormalization Theorems and the 4-Point Function_,  	Nucl. Phys. B715:3-90, 2005 ([arXiv:hep-th/0501197](http://arxiv.org/abs/hep-th/0501197))

* [[Eric D'Hoker]], [[Duong Phong]], _Two-Loop Superstrings VII, Cohomology of Chiral Amplitudes_, Nucl. Phys. B804:421-506, 2008 ([arXiv:0711.4314](http://arxiv.org/abs/0711.4314))

Review of this work:

* A.Morozov, _NSR Superstring Measures Revisited_, JHEP0805:086,2008 ([arXiv:0804.3167](http://arxiv.org/abs/0804.3167))

Further developments:

* [[Eric D'Hoker]], [[Carlos Mafra]], [[Boris Pioline]], [[Oliver Schlotterer]], _Two-loop superstring five-point amplitudes I: Construction via chiral splitting and pure spinors_ ([arXiv:2006.05270](https://arxiv.org/abs/2006.05270))

* [[Eric D'Hoker]], [[Carlos Mafra]], [[Boris Pioline]], [[Oliver Schlotterer]], _Two-loop superstring five-point amplitudes II: Low energy expansion and S-duality_ ([doi:2008.08687](https://arxiv.org/abs/2008.08687))


The technical issue of the [[moduli space]] of [[super Riemann surfaces]] of higher genus (for higher loop string scattering amplitudes) is discussed in

* [[Edward Witten]], _Notes On Super Riemann Surfaces And Their Moduli_ ([arXiv:1209.2459](http://arxiv.org/abs/1209.2459))

* [[Ron Donagi]], [[Edward Witten]], _Supermoduli Space Is Not Projected_ ([arXiv:1304.7798](http://arxiv.org/abs/1304.7798))



On the case of [[3-loop]]:

* Petr Dunin-Barkowski, Igor Fedorov, Alexey Sleptsov: *RNS superstring measure for genus 3* &lbrack;[arXiv:2505.02950](https://arxiv.org/abs/2505.02950)&rbrack;




### Higher order corrections

* [[Christopher Pope]],  _Higher-order corrrections in String and M-theory and Generalized Holonomies_, December 2006 ([pdf](http://www.luth.obspm.fr/IHP06/workshops/cosmo/slides/Pope.pdf))

### On finiteness
 {#ReferencesOnFiniteness}

Here is a commented list of references on the degreewise [finiteness of string scattering amplitudes](#Finiteness).

#### Finiteness of bosonic string scattering

Introductory lecture notes:

* {#StaessensVernocke10} Wieland Staessens, Bert Vercnocke, _Lectures on Scattering Amplitudes in String Theory_, Lecture notes based on lectures given at the fifth Modave School on Mathematical Physics (August 2009) ([arXiv:1011.0456](http://arxiv.org/abs/1011.0456))
 

Discussion of the term-wise finiteness of the bosonic string scattering amplitudes is in

* L. Clavelli, S. T. Jones, _Finiteness of the bosonic string in fewer than 26 dimensions_, Phys. Rev. D 39, 3795&#8211;3797 (1989) ([SPIRE](http://inspirehep.net/record/24403))

There are also arguments in 

* Simon Davis, _On the domain of string perturbation theory_, Classical and Quantum Gravity, Volume 6, Issue 12, pp. 1791-1803 (1989) ([web](http://adsabs.harvard.edu/abs/1989CQGra...6.1791D))


#### Finiteness of superstring scattering

Finiteness of heterotic and type II superstring $n$-point functions in flat spacetime is argued for in

* Joseph Atick, [[Gregory Moore]], [[Ashoke Sen]], _Catoptrick tadpoles_, Nucl.Phys. B307 (1988) 221 ([spire](http://inspirehep.net/record/252598?ln=en))

General finiteness of superstring amplitudes is discussed in 

* [[Stanley Mandelstam]], _The $n$ Loop String Amplitude: Explicit Formulas, Finiteness and Absence of Ambiguities_, Phys. Lett. B277 (1992) 82. ([inspire](http://inspirehep.net/record/319501))

which shows that a certain divergence which could appear does not.

Also 

* A. Restuccia, J. Taylor, _Finiteness of type II superstring amplitudes_, Physics Letters B, Volume 187, Issues 3&#8211;4, 26 March 1987, Pages 267&#8211;272

argues finiteness of the superstring amplitudes at each order.

Also:

* [[Eric D'Hoker]], [[Duong Phong]], _Momentum Analyticity and Finiteness of the 1-Loop Superstring Amplitude_,  Phys. Rev. Lett. 70 (1993) 3692-3695 ([arXiv:hep-th/9302003](http://arxiv.org/abs/hep-th/9302003))

* [[Eric D'Hoker]], [[Duong Phong]], _The Box Graph In Superstring Theory_, Nucl.Phys.B440:24-94,1995 ([arXiv:hep-th/9410152](http://arxiv.org/abs/hep-th/9410152))

* [[Eric D'Hoker]], [[Duong Phong]], _Dispersion Relations in String Theory_; Nucl.Phys.B440:24-94,1995 ([arXiv:hep-th/9404128](http://arxiv.org/abs/hep-th/9404128))

Arguments for the finiteness of superstring scattering amplitudes to all loop order based on the [[Berkovits superstring]]-formulation have been promoted in 

* [[Nathan Berkovits]], _Multiloop Amplitudes and Vanishing Theorems using the Pure Spinor Formalism for the Superstring_,  JHEP 0409:047,2004 ([arXiv:hep-th/0406055](http://arxiv.org/abs/hep-th/0406055))

(In footnote 2 this article claims that the claimed proofs of the same statement by G.S Danilov in [hep-th/9801013](http://arxiv.org/abs/hep-th/9801013), [hep-th/0312177](http://arxiv.org/abs/hep-th/0312177) are not in fact proofs.)

Discussion of [[2-loop]] amplitudes from holomorphy arguments:

* [[Edward Witten]], _Notes On Holomorphic String And Superstring Theory Measures Of Low Genus_ ([arXiv:1306.3621](http://arxiv.org/abs/1306.3621))

See also:

* [[Ashoke Sen]], _Supersymmetry Restoration in Superstring Perturbation Theory_ ([arXiv:1508.02481](http://arxiv.org/abs/1508.02481))

### Graviton scattering

Computation of [[graviton]] scattering amplitudes ([[perturbative quantum gravity]]):

* [[Taejin Lee]], _Gravitational Scattering Amplitudes and Closed String Field Theory in the Proper-Time Gauge_, EPJ Web of Conferences 168, 07004 (2018) ([doi:10.1051/epjconf/201816807004](https://doi.org/10.1051/epjconf/201816807004))

* [[Taejin Lee]], _Four-Graviton Scattering and String Path Integral in the Proper-time gauge_ ([arXiv:1806.02702](https://arxiv.org/abs/1806.02702))


### Via AdS/CFT
 {#ReferencesViaAdSCFT}

Discussion via [[AdS/CFT]] beyond the [[SCFT]] [[planar limit]], using the [[conformal bootstrap]]:

* {#ABP18} [[Luis Alday]], [[Agnese Bissi]], [[Eric Perlmutter]], _Genus-One String Amplitudes from Conformal Field Theory_, JHEP06(2019) 010 ([arXiv:1809.10670](https://arxiv.org/abs/1809.10670))


### More

On point-particle limit via [[tropical geometry]]

* Piotr Tourkine, _Tropical Amplitudes_ ([arXiv:1309.3551](http://arxiv.org/abs/1309.3551))

Scattering amplitudes of highly excited strings:

* Dimitri P. Skliros, Edmund J. Copeland, Paul M. Saffin, _Highly Excited Strings I: Generating Function_ ([arxiv:1611.06498](https://arxiv.org/abs/1611.06498))



[[!redirects string scattering amplitudes]]

[[!redirects superstring scattering amplitude]]
[[!redirects superstring scattering amplitudes]]

[[!redirects string scattering]]

[[!redirects string perturbation series]]


[[!redirects string amplitude]]
[[!redirects string amplitudes]]



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[physics]], specifically in [[field theory]], a _Dirac field_ is an [[electromagnetism|electromagentially]] charged and possibly [[mass|massive]] a _[[fermion|fermionic]] [[spinor]] field_.

This includes [[fermions]] in the [[standard model of particle physics]], such as [[electrons]], [[quarks]], [[neutrinos]] and [[muons]], after the [[Higgs mechanism]] has equipped them with [[mass]].

Mathematically, the Dirac field is the [[field (physics)|field]] whose [[field bundle]] is a [[spinor bundle]] with typical [[fiber]] a [[Dirac representation]] in [[supergeometry|odd super-degree]] and whose [[equation of motion]] is a [[Dirac equation]].

Notice that there are other [[spinor]] [[field (physics)|fields]] which would not be called "Dirac fields", such as those transforming in a [[Majorana representation]] or a [[Weyl representation]], or for example the [[gravitino]] field which would be called a _[[Rarita-Schwinger field]]_.

## Properties

### Free Dirac field in Couloumb background
 {#FreeDiracFieldInCoulombBackground}

In [[solid state physics]], the [[electrons]] described by the [[Dirac equation]] are encountered in the [[electromagnetic field|electromagnetic]] [[background field]] that is sourced by [[atomic nuclei]] such as those on the lattice sites of a [[crystal]]. 

In a common approximation used in [[condensed matter theory]] for computing [[ground state]]-properties of [[crystals]], the nuclei are typically treated as motionless (due to their large [[mass]] compared to that of the electrons), hence sourcing a static Coulomb background field, while the electromagnetic interaction of the electrons with each other is neglected. In this approximation one is dealing with a "[[free field|free]] [[Dirac field]] in a static [[electromagnetic field|Coulomb]] [[background field|background]]".


<center>
<img src="https://ncatlab.org/nlab/files/ElectronFieldInCoulombBackground-220509.jpg" width="400">
</center>



The [[vacua]]/[[ground state]] of the [[free field|free]] [[Dirac field]] in such a "classical Coulomb background" (review in [Thaller 92, Sec. 10](#Thaller92)) have been computed in [Klaus & Scharf 77](#KlausScharf77) and found to be characterized by [[Fredholm operators]] (amplified in [Carey, Hurst & O'Brien 82](#CareyHurstOBrien82)) whose [[kernel]]/[[cokernel]] are the [[Hilbert spaces]] of single [[electron]]/[[positron]] [[quantum states]] which are occupied in the charged vacuum, hence whose [[Fredholm index]] is the total [[charge]] in this vacuum.

<center>
<img src="https://ncatlab.org/nlab/files/ChargedDiracVacuumAsFredholmOperator-220509b.jpg" width="640"/>

(graphics from <a href="https://ncatlab.org/schreiber/show/Topological+Quantum+Computation+in+TED-K">SS 22</a>, <a href="https://ncatlab.org/schreiber/show/Anyonic+defect+branes+in+TED-K-theory#ExpositoryTalk">Sc 22</a>)
</center>


## Related concepts

* [[Dirac spinor]]

* [[Dirac conjugate]]

* [[Dirac operator]], [[Dirac equation]]

* [[Dirac current]]

* [[electron propagator]]

## Reference

### General

A concise collection of the Dirac field over [[Minkowski spacetime]] is in

* {#DermisekI9} [[Radovan Dermisek]], _qft I-9_, 2009 ([pdf](http://www.physics.indiana.edu/~dermisek/QFT_09/qft-I-9-4p.pdf), [[DermisekDiracField.pdf:file]])

with background on [[spinor]] [[field (physics)|fields]] in 

* {#DermisekI8} [[Radovan Dermisek]], _qft I-8_, 2009 ([pdf](http://www.physics.indiana.edu/~dermisek/QFT_09/qft-I-8-4p.pdf), [[DermisekSpinorField.pdf:file]])


A textbook account of the interacting Dirac field in the context of [[causal perturbation theory]]:

* {#Scharf95} [[Günter Scharf]], section 2.2 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

* {#Scharf01} [[Günter Scharf]], section 1.8 of _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001


Textbook account of the [[free field|free]] Dirac field but possiblyin an [[electromagnetic field|electromagnetic]] [[background field]]:

* {#Thaller92} [[Bernd Thaller]], Section 10 of: *The Dirac Equation*,  Texts and Monographs in Physics, Springer (1992) ([doi:10.1007/978-3-662-02753-0](https://link.springer.com/book/10.1007/978-3-662-02753-0))
   


### Free Dirac field in Coulomb background

Discussion of the *charged* [[vacua]]/[[ground states]] of the [[free field|free]] Dirac field in a strong [[electromagnetic field|Coulomb]] [[background field]] (such as that sourced by [[atomic nuclei]] on a [[crystal]] lattice):

Identification of the [[vacua]]/[[ground states]] of the [[free field|free]] [[Dirac field]] in a [[electromagnetic field|Coulomb]] [[background field]]:

* {#KlausScharf77} [[Martin Klaus]], [[Günter Scharf]], *The regular external field problem in quantum electrodynamics*, Helv. Phys. Acta **50** (1977) $[$[doi:10.5169/seals-114890](http://doi.org/10.5169/seals-114890)$]$

and the observation that these vacua are characterized by [[Fredholm operators]] whose [[index]] is the total charge in the vacuum:

* {#CareyHurstOBrien82} [[Alan Carey]], [[Charles Angas Hurst]], [[Denis O'Brien]], *Automorphisms of the canonical anticommutation relations and index theory*, Journal of Functional Analysis **48** 3 (1982) 360-393 $[$<a href="https://doi.org/10.1016/0022-1236(82)90092-1">doi:10.1016/0022-1236(82)90092-1</a>$]$

This curious observation seems not to have been followed up on much, but some related references are listed in [Thaller 92, p. 319](#Thaller92).



[[!redirects Dirac fields]]

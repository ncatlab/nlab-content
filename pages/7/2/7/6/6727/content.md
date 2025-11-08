

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

In the construction of the [[NSR string|NSR]] [[superstring]] as a [[2d SCFT]] from a [[supersymmetry|supersymmetric]] [[sigma-model]] one needs to remove one half of the [[sigma-model]]-excitations in order to achieve that the resulting [[2d SCFT]] satisfies [[modular invariance]], hence that it is defined not just on the [[complex plane]] but also on [[tori]]. This halfing of the naive sigma-model spectrum is called the _GSO projection_, after [GSO 77](#GSO77).

Depending on how the GSO projection is chosen, one gets [[type IIA string theory]], [[type IIB string theory]] or [[type 0 string theory]].

A good account is in [Majer, sections 1.3 and 2](#Majer).

<center>
<img src="https://ncatlab.org/nlab/files/GSOProjection.jpg" width="700"/>
</center>


## Properties

### Local spacetime supersymmetry - supergravity

The GSO projection to the [[type II superstring]] together with the [[Goddard-Thorn no-ghost theorem]] implies that the [[effective field theory]] encoded in the [[string scattering amplitudes]] ([[S-matrix]]) is a [[supergravity]] theory ([Green-Schwarz 81](#GreenSchwarz81)).

This way the mere assumption of strings with [[fermions]] in their spectrum (originally just called "[[spinning strings]]") _implies local_ [[supersymmetry]]_ in [[target space|target]] [[spacetime]]. For more on this see [[string theory FAQ]]: _[Does string theory predict supersymmetry?](string+theory+FAQ#DoesSTPredictSupersymmetry)_

### Beyond modular invariance

One should really check that the [[2d SCFT]] is well defined on _all_ [[worldsheet]] [[genus of a surface|genera]], not just on genus 1 as given by [[modular invariance]].

Because [[correlators]] at all the higher genera enter the [[string perturbation series]] at higher [[loop order]]. 

But this is subtle for the [[NSR superstring]], see at _[[super Riemann surface]]_ for more on this. 

A full construction of [[2d CFTs]] at all [[genus of a surface|genera]] has been achieved only for bosonic [[rational 2d CFTs]], see at _[[FRS-theorem on rational 2d CFT]]_.

### The Green-Schwarz string

The [[Green-Schwarz superstring]] [[sigma-model]] gives an alternative description of the [[superstring]], where [[spacetime]] [[supersymmetry]] is manifest throughout the construction. No "GSO projection" is needed here, and no analog of the [[Goddard-Thorn no-ghost theorem]] needs to be proven. The downside is that generalization to higher [[genus of a surface|genera]] and to [[curved spacetimes]] is less immediate or unclear.


## Related entries

* [[Goddard-Thorn no-ghost theorem]]

* [[string theory FAQ]]: _[Does string theory predict supersymmetry?](string+theory+FAQ#DoesSTPredictSupersymmetry)_

## References

The concept is due to 

* {#GSO77} F. Gliozzi, [[Joël Scherk]], D. I. Olive, _Supersymmetry, supergravity theories and the dual spinor model_, Nucl. Phys, B122, 253 (1977)

* {#GSO77} F. Gliozzi, [[Joël Scherk]], D. I. Olive, _Supersymmetry, Supergravity Theories and the Dual Spinor Model_, Nucl. Phys. B 122 (1977), 253 ([spire](http://inspirehep.net/record/111434))



Review includes

* {#Majer} Imre Majer, sections 1.3 and 2 of: _Superstrings_ ([pdf](http://edu.itp.phys.ethz.ch/fs13/cft/SuperS2_Majer.pdf), [[MajerSuperstrings.pdf:file]])

* _String primer_ around p. 43 in ([arXiv:hep-th/9810240](http://arxiv.org/abs/hep-th/9810240))

See also 

* Wikipedia, _[GSO projection](https://en.wikipedia.org/wiki/GSO_projection)_

That the GSO projection implies [[spacetime]] [[supersymmetry]] is due to

* {#GreenSchwarz81} [[Michael Green]], [[John Schwarz]], 

  _Supersymmetrical dual string theory_ , Nucl. Phys. B181 (1981) 502; 

  _Supersymmetrical string theories_ , Phys. Lett. 109B (1982) 444.

Superconformal invariance of the spinning string was discussed in

* {#Howe79} [[Paul Howe]], _Super Weyl transformations in two dimensions_ J. Phys. 12 (1979) 393


A review of the history of these developments is in 

* [[John Schwarz]], _String theory origins of supersymmetry_, Nucl. Phys. Proc. Suppl. 101 (2001) 54-61 ([arXiv:hep-th/0011078](http://arxiv.org/abs/hep-th/0011078))

Interpretation of the [[GSO projection]] as a [[sum]] over [[spin structures]] and discussion of [[type 0 string theory]]:



* [[Nathan Seiberg]], [[Edward Witten]], section 4 of: *Spin Structures in String Theory*, Nucl. Phys. B **276** (1986) 272 \[<a href="https://doi.org/10.1016/0550-3213(86)90297-X">doi:10.1016/0550-3213(86)90297-X</a>\]

* [[Lance J. Dixon]], [[Jeffrey A. Harvey]]: *String Theories in Ten-Dimensions Without Space-Time Supersymmetry*, Nucl. Phys. B **274** (1986) 93-105 \[<a href="https://doi.org/10.1016/0550-3213(86)90619-X">10.1016/0550-3213(86)90619-X</a>\]


* [[Hikaru Kawai]], D. C. Lewellen, S. H. H. Tye: *Classification of Closed Fermionic String Models*, Phys. Rev. D **34** (1986) 3794 &lbrack;[doi:10.1103/PhysRevD.34.3794](https://doi.org/10.1103/PhysRevD.34.3794)&rbrack;



Discussion in the context of [[D-branes]] ([[boundary conformal field theory]]):

* [[Jürgen Fuchs]], [[Christoph Schweigert]], J. Walcher: _Projections in string theory and boundary states for Gepner models_, Nucl.Phys. B588 (2000) 110-148 ([arXiv:hep-th/0003298](https://arxiv.org/abs/hep-th/0003298))

Relation of the GSO projection to the [[symmetry protected topological phase|symmetry protected]] [[invertible field theory|invertible]] [[topological phases of matter]] and the [[K-theory classification of topological phases of matter]]:

* [[Justin Kaidi]], [[Julio Parra-Martinez]], [[Yuji Tachikawa]]: *Classification of String Theories via Topological Phases*, Phys. Rev. Lett. **124** (2020) 121601 &lbrack;[doi:10.1103/PhysRevLett.124.121601](https://doi.org/10.1103/PhysRevLett.124.121601)&rbrack;

* [[Justin Kaidi]], [[Julio Parra-Martinez]], [[Yuji Tachikawa]]: _Topological Superconductors on Superstring Worldsheets_, SciPost Phys. **9** 010 (2020)  &lbrack;[doi:10.21468/SciPostPhys.9.1.010](https://doi.org/10.21468/SciPostPhys.9.1.010), [arXiv:1911.11780](https://arxiv.org/abs/1911.11780)&rbrack;





[[!redirects GSO projections]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The flavour of [[generalized cohomology]] which is both [[twisted cohomology|twisted]] as well as [[differential cohomology|differential]] is called _twisted differential cohomology_ (or: _differential twisted cohomology_).

A key motivation for twisted differential cohomology is its role in [[string theory]] as the type of [[generalized cohomology theory]] that classifies [[higher gauge fields]] (following [[Dirac charge quantization and generalized differential cohomology|Freed 00]]), notably in the example of [[twisted differential K-theory]] classifying the [[RR-field]] twisted by the [[B-field]] (see [below](#TwistedDifferentialKTheory)).

## Definition

Observing that

1. [[differential cohomology]] may be understood as being the intrinsic [[cohomology]] inside an [[(∞,1)-topos]] $\mathbf{H}$ which is [[cohesive (∞,1)-topos|cohesive]] (see at _[[differential cohomology diagram]]_);

1. [[twisted cohomology]] may be understood as being the intrinsic [[cohomology]] inside the [[tangent (∞,1)-topos]] $T \mathbf{H}$ of the given ambient [[(∞,1)-topos]] $\mathbf{H}$

and since 

* the [[tangent (∞,1)-topos]] $T \mathbf{H}$ of an [[cohesive (∞,1)-topos]] $\mathbf{H}$ is itself again cohesive, 

one may define twisted differential cohomology in generality to be the intrinsic [[cohomology]] inside [[cohesive (∞,1)-topos|cohesive]] [[tangent (∞,1)-toposes]] $T \mathbf{H}$ ([Schreiber 13, Sec. 4.1.2](#Schreiber13), [Schreiber 14, slide 16](#Schreiber14)).

The [[objects]] of such a $T \mathbf{H}$ may be understood as [[sheaves of spectra|sheaves of]] [[parametrized spectra]] ([Braunack-Mayer 19, Theorem 3.4](#BraunackMayer19)). For example with $\mathbf{H} =$ [[Smooth∞Grpd]] the objects of $T Smth\infty Grpd$ are [[smooth spectra|smooth]] [[parametrized spectra]]. In this sense the formulation of twisted differential cohomology via [[cohesive (∞,1)-topos|cohesive]] [[tangent (∞,1)-topos]] generalizes the classical [[Brown representability theorem]] (identifying plain [[generalized (Eilenberg-Steenrod) cohomology theories]] with plain [[spectra]]) to twisted and differential cohomology.

By means of a suitable [[model category]] [[presentable (∞,1)-category|presentation]] of [[tangent (∞,1)-toposes]], [Braunack-Mayer 19, Example 3.23](#BraunackMayer19) proves that a more explicit component-based definition of twisted differential cohomology due to [Bunke-Nikolaus 14](#BunkeNikolaus14) is a special case of this general definition from [Schreiber 13, Sec. 4.1.2](#Schreiber13).


## Examples

### Twisted de Rham cohomology

A simple example of twisted cohomology is _[[twisted de Rham cohomology]]_ (see there for more), the [[twisted cohomology|twisted]] generalization of [[de Rham cohomology]].

### Twisted differential K-theory
 {#TwistedDifferentialKTheory}

The archetypical example is [[twisted differential K-theory]], which combines [[twisted K-theory]] with [[differential K-theory]]. To the extent that [[D-brane charge]] is classified by [[K-theory]] (see [there](D-brane#ReferencesKTheoryDescription)), it is [[twisted differential K-theory]] that is relevant: the [[differential K-theory|differential]] aspect captures the [[higher gauge field]] called the [[RR-field]], and the [[twisted K-theory|twisted]] aspects captures the [[higher gauge field]] called the [[B-field]], in [[string theory]].

This example of [[D-brane charge]] used to be one of the main motivations for finding a definition and construction of twisted differential cohomology theories. Earlier account of D-brane charge theory had to assume without a construction that such a theory exists (e.g. [DFM 09](twisted+differential+K-theory#DFM09)).

Other [[higher gauge fields]] in [[string theory]]/[[M-theory]] are expected to be [[cocycles]] in twisted differential cohomology theories for other [[generalized cohomology theories]] apart from K-thery. For instance the hypothesis that the [[M-theory]] [[supergravity C-field|C-field]] is topologically a cocycle in [[twisted cohomotopy]] ([[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation|FSS19b]], [[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization|FSS19c]]) means that with all differential form data added. it is actually a cocycle in _twisted differential cohomotopy_.


## References

The general abstract definition of [[twisted differential cohomology]] as the intrinsic [[cohomology]] of [[cohesive (∞,1)-topos|cohesive]] [[tangent (∞,1)-toposes]] is due to 

* {#Schreiber13} [[Urs Schreiber]], section 4.1.2 of _[[schreiber:Differential cohomology in a cohesive (∞,1)-topos]]_, ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930v1))

* {#Schreiber14} [[Urs Schreiber]], around slide 17 of _[[schreiber:Differential generalized cohomology in Cohesive homotopy type theory]]_ , talk at   IHP trimester on _[Semantics of proofs and certified mathematics](https://ihp2014.pps.univ-paris-diderot.fr/doku.php)_ Workshop 1: _[Formalization of Mathematics](https://ihp2014.pps.univ-paris-diderot.fr/doku.php?id=workshop_1)_, [Institut Henri Poincaré](http://www.ihp.fr/en),  Paris, 5-9 May 2014 ([pdf slides](https://ncatlab.org/schreiber/files/SchreiberParis2014.pdf))

* [[Daniel Grady]], [[Hisham Sati]], *Twisted differential generalized cohomology theories and their Atiyah-Hirzebruch spectral sequence*, Algebr. Geom. Topol. 19 (2019) 2899-2960 ([arXiv:1711.06650](https://arxiv.org/abs/1711.06650), [doi:10.2140/agt.2019.19.2899](https://projecteuclid.org/journals/algebraic-and-geometric-topology/volume-19/issue-6/Twisted-differential-generalized-cohomology-theories-and-their-AtiyahHirzebruch-spectral-sequence/10.2140/agt.2019.19.2899.short))

* {#FSS20} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The character map in (twisted differential) non-abelian cohomology]]_ ([arXiv:2009.11909](https://arxiv.org/abs/2009.11909))



Discussion of [[twisted differential K-theory]] along these lines:

* [[Daniel Grady]], [[Hisham Sati]], _Twisted differential KO-theory_ ([arXiv:1905.09085](https://arxiv.org/abs/1905.09085))

  (specifically: [[KO-theory]])

A more component-based definition was given in

* {#BunkeNikolaus14} [[Ulrich Bunke]], [[Thomas Nikolaus]], _Twisted differential cohomology_, Algebr. Geom. Topol. Volume 19, Number 4 (2019), 1631-1710. ([arXiv:1406.3231](http://arxiv.org/abs/1406.3231), [euclid:euclid.agt/1566439272](https://projecteuclid.org/euclid.agt/1566439272))

A proof that the definition of [Bunke-Nikolaus 14](#BunkeNikolaus14) is a special case of that of [Schreiber 13, Sec. 4.2.1](#Schreiber13) is due to

* {#BraunackMayer19} [[Vincent Braunack-Mayer]], Section 3.1 of _Combinatorial parametrised spectra_, based on the [[schreiber:thesis Braunack-Mayer|PhD thesis]] ([arXiv:1907.08496](https://arxiv.org/abs/1907.08496))

For more discussion of twisted differential cohomology as the intrinsic [[cohomology]] of _[[tangent cohesive (∞,1)-topos|Goodwillie-tangent spaces of cohesive (∞,1)-topos]]_ see there.

[[!redirects differential twisted cohomology]]
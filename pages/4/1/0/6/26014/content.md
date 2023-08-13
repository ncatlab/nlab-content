
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

Traditionally, a *[[global symmetry|global]] [[symmetry]]* is defined as [[invariance]] (e.g. of a physical system) under a [[group action]]. This definition is well-suited for physical systems such as in [[classical mechanics]], where symmetries appear as [[symplectomorphisms]] leaving a [[Hamiltonian]] invariant. 

However, many systems of interest depart, or **generalize**, from this setting in two different ways: as a [[classical field theory]], or as a [[quantum system]] (or as both, as a [[quantum field theory]]). A natural question to ask is what happens to the mathematical objects realizing the notion of symmetry when these generalizations are considered. The former case leads to the [[vertical categorification]] of groups to [[n-groups|$n$-groups]], as observed in [[higher prequantum geometry]]. The latter case leads to a [[ring]] (or [[algebra]]) structure. The concept of **generalized global symmetries** is thought to be the appropriate notion of symmetry when both of these generalizations take place at the same time. 

{#OriginOfTheTerminology} The terminology *generalized global symmetry* for such a situation is due to [Gaiotto, Kapustin, Seiberg & Willett (2014)](#GaiottoKapustinSeibergWillett14). As described therein (at a very in-formal level) classical symmetries (described by a group) that survive the quantization process are thought to become "[[operators]]" that can be "inserted" (namely into the [[integrand]] of a [[path integral]], though this step and its details are left implicit) along [[submanifolds]] (of [[spacetime]]) of non-negative [[codimension]]. 
These operators are supposed to be "topological", in the sense that they should only depend on the homology class of said submanifold. [GKSW14](#GaiottoKapustinSeibergWillett14) propose to regard any quantum operator with the topological property as a symmetry of the quantum system even if they do not have inverses. It is in this sense that the concept of symmetry is regarded as being generalized.

As emphasized by [Freed, Moore & Teleman (2022)](#FMT22), such phenomena should be controlled by [[higher algebra]]. Of course this is not quite a new observation, ideas broadly in this direction date back to [Roberts (1979)](John+Elias+Roberts#Roberts79). Concretly, "non-invertible symmetry insertions" are at least close to what elsewhere has long been known as *[[QFT with defects|defects in QFT]]* which have routinely been described via [[higher algebra|higher]] [[categorical algebra]], cf. [Fuchs, Runkel & Schweigert (2004)](#FRS04); [Fröhlich, Fuchs, Runkel & Schweigert (2007)](#FFRS07); [Lurie (2009) §4.3](QFT+with+defects#Lurie09); [Davydov, Runkel & Kong (2011)](QFT+with+defects#DavydovRunkelKong11); [Fuchs, Schweigert & Valentino (2013)](QFT+with+defects#FuchsSchweigertValentino13). The terms "defects" and "topological operator insertions" are actually often used interchangeably in the Physics literature. Indeed, many of the techniques used to deal with these generalized symmetries come from the literature on defects. A notable example is the gauging procedure of defects in two-dimensional QFT as originally described in [Fuchs, Runkel & Schweigert (2002)](#FRS02I), and directly recasted in the language of generalized symmetries in e.g. [Bhardwaj and Tachikawa (2017)](#BT17).


The upshot is that just as groups correctly describe the symmetries of classical mechanics, higher algebra is thought to describe the "generalized global symmetries" of a quantum field theory.

In this sense, the concept may be better understood as **higher quantum symmetries** (even though the name "quantum symmetries" is already used in the Physics literature for a "dual" symmetry that arises after gauging a symmetry, originating in [Vafa (1989)](#Vafa89)).

A significant part of the current Physics literature on the topic restricts to the study of *finite* generalized symmetries, thus avoiding questions regarding the *[[smooth|smoothness]]* of the corresponding higher algebra (in contrast with the situation of [[n-group|higher groups]], by which one really means a [[smooth infinity-groupoid]]). In such a case, the concrete mathematical objects of study are *bare* [[fusion categories|fusion category]] (and their vertical categorifications as in e.g. [Decoppet and Yu (2023)](#DY23)). These fusion categories are argued to contain information about the quantum operators and their fusion rules but also about any present [['t Hooft anomaly]], all (somehow) encoded in the [[topological quantum field theory]] defined through the [[Turaev-Viro model]] and their would-be higher generalizations.  Unfortunately, not only these expectations but even fundamental questions such as precisely *how* a smooth higher algebra acts on a quantum field theory (beyond the slogan of *a symmetry operator inserted on a codimension $d$ submanifold acts on quantum operators supported on dimension $d-1$ submanifolds*) are still not understood. An accurate description of such an action of a smooth higher algebra should in particular describe how the [[group action]] of the [[quantomorphism group]] on the [[prequantum circle n-bundle]] becomes this after [[motivic quantization]].

## Related concepts

* [[QFT with defects]]

* [[duality in physics]]


## References
 {#References}

Early discussion of "generalized global symmetries" under the name of *[[QFT with defects|defects]]*, in [[2d conformal field theory]] (via the [[FRS theorem on rational 2d CFT]]):

* {#FRS02I} [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], _TFT construction of RCFT correlators I: Partition functions_, Nucl. Phys. B **646**  (2002) 353-497 &lbrack;[arXiv:hep-th/0204148](http://arxiv.org/abs/hep-th/0204148), <a href="https://doi.org/10.1016/S0550-3213(02)00744-7">doi:10.1016/S0550-3213(02)00744-7</a>&rbrack;

* {#FRS04} [[Jürg Fröhlich]], [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], *Kramers-Wannier duality from conformal defects*, Phys. Rev. Lett. **93** (2004) 070601 &lbrack;[doi:10.1103/PhysRevLett.93.070601](https://doi.org/10.1103/PhysRevLett.93.070601), [arXiv:cond-mat/0404051](http://arxiv.org/abs/cond-mat/0404051)&rbrack;

* {#FFRS07} [[Jürg Fröhlich]], [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], *Duality and defects in rational conformal field theory*, Nucl. Phys. B **763** (2007) 354-430 &lbrack;[arXiv:hep-th/0607247](http://arxiv.org/abs/hep-th/0607247), [doi:10.1016/j.nuclphysb.2006.11.017](https://doi.org/10.1016/j.nuclphysb.2006.11.017)&rbrack;



The terminology of *generalized global symmetries* is due to:

* {#GaiottoKapustinSeibergWillett14} [[Davide Gaiotto]], [[Anton Kapustin]], [[Nathan Seiberg]], [[Brian Willett]], *Generalized Global Symmetries*  J. High Energ. Phys. **2015** 172 (2015) &lbrack;[arXiv:1412.5148](https://arxiv.org/abs/1412.5148), <a href="https://doi.org/10.1007/JHEP02(2015)172">doi:10.1007/JHEP02(2015)172</a>&rbrack;

Further suggestion for mathematical formalization of what [GKSW14](#GaiottoKapustinSeibergWillett14) had in mind (purely at the quantum level, with caveats):

* {#FMT22} [[Daniel Freed]], [[Gregory Moore]], [[Constantin Teleman]], *Topological symmetry in quantum field theory* (2022) &lbrack;[arXiv:2209.07471](https://arxiv.org/abs/2209.07471)&rbrack;

See also:

* {#Vafa89} [[Cumrun Vafa]], *Quantum Symmetries of String Vacua* (1989) &lbrack;[doi:10.1142/S0217732389001842](https://doi.org/10.1142/S0217732389001842)&rbrack;

* {#BT17} [[Lakshya Bhardwaj]], [[Yuji Tachikawa]]. *On finite symmetries and their gauging in two dimensions*, J. High Energ. Phys. **2018** 189 (2018) &lbrack;[arXiv:1704.02330](https://arxiv.org/abs/1704.02330), <a href="https://doi.org/10.1007/JHEP03(2018)189">doi:10.1007/JHEP03(2018)189</a>&rbrack;

* {#DY23} [[Thibault Decoppet]], [[Matthew Yu]], *Fiber 2-Functors and Tambara-Yamagami Fusion 2-Categories* (2023) &lbrack;[arXiv:2306.08117](https://arxiv.org/abs/2306.08117)&rbrack;



[[!redirects generalized global symmetries]]

[[!redirects generalized symmetry]]
[[!redirects generalized symmetries]]
[[!redirects non-invertible symmetry]]
[[!redirects non-invertible symmetries]]


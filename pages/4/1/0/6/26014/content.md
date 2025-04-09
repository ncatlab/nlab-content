
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

As emphasized by [Freed, Hopkins, Teleman & Lurie (2009)](#FHTL09), and again in [Freed, Moore & Teleman (2022)](#FMT22), such phenomena should be controlled by [[higher algebra]]. Of course this is not quite a new observation, ideas broadly in this direction date back to [Roberts (1979)](John+Elias+Roberts#Roberts79). Concretly, "non-invertible symmetry insertions" are at least close to what elsewhere has long been known as *[[QFT with defects|defects in QFT]]* which have routinely been described via [[higher algebra|higher]] [[categorical algebra]], cf. [Fuchs, Runkel & Schweigert (2004)](#FRS04); [Fröhlich, Fuchs, Runkel & Schweigert (2007)](#FFRS07); [Lurie (2009) §4.3](QFT+with+defects#Lurie09); [Davydov, Runkel & Kong (2011)](QFT+with+defects#DavydovRunkelKong11); [Fuchs, Schweigert & Valentino (2013)](QFT+with+defects#FuchsSchweigertValentino13). The terms "defects" and "topological operator insertions" are actually often used interchangeably in the Physics literature. Indeed, many of the techniques used to deal with these generalized symmetries come from the literature on defects. A notable example is the gauging procedure of defects in two-dimensional QFT as originally described in [Fuchs, Runkel & Schweigert (2002)](#FRS02I), and directly recasted in the language of generalized symmetries in e.g. [Bhardwaj and Tachikawa (2017)](#BT17).


The upshot is that just as groups correctly describe the symmetries of classical mechanics, higher algebra is thought to describe the "generalized global symmetries" of a quantum field theory.

In this sense, the concept may be better understood as **higher quantum symmetries** (even though the name "quantum symmetries" is already used in the Physics literature for a "dual" symmetry that arises after gauging a symmetry, originating in [Vafa (1989)](#Vafa89)).

A significant part of the current Physics literature on the topic restricts to the study of *finite* generalized symmetries, thus avoiding questions regarding the *[[smooth|smoothness]]* of the corresponding higher algebra (in contrast with the situation of [[n-group|higher groups]], by which one really means a [[smooth infinity-groupoid]]). In such a case, the concrete mathematical objects of study are *bare* [[fusion categories|fusion category]] (and their vertical categorifications as in e.g. [Decoppet and Yu (2023)](#DY23) and [Bhardwaj et al. 2024](#BDSY24) based on [Johnson-Freyd 2020](#JF20nf)). These fusion categories are argued to contain information about the quantum operators and their fusion rules but also about any present [['t Hooft anomaly]], all (somehow) encoded in the [[topological quantum field theory]] defined through the [[Turaev-Viro model]] and their would-be higher generalizations.  Unfortunately, not only these expectations but even fundamental questions such as precisely *how* a smooth higher algebra acts on a quantum field theory (beyond the slogan of *a symmetry operator inserted on a codimension $d$ submanifold acts on quantum operators supported on dimension $d-1$ submanifolds*) are still not fully understood. An accurate description of such an action of a smooth higher algebra should in particular describe how the [[group action]] of the [[quantomorphism group]] on the [[prequantum circle n-bundle]] becomes this after [[motivic quantization]]. In this picture, the action of a higher group makes sense since the prequantum n-bundle also has a higher structure. In this sense, the action of a higher algebra should be defined on an object which has both a higher and a linear structure. This is the case for higher [[vector bundle|vector bundles]] such as [[2-vector bundle|2-vector bundles]] or, in much greater generality, an [[n-vector bundle]] over some [[E-∞ ring]].

## Freed-Moore-Teleman *quiche*

In [Freed, Moore and Teleman (2022)](#FMT22), the authors describe a proposal to make mathematical sense of the heuristics of generalized symmetries. The approach is based on the presentation of Quantum Field Theory as [[extended functorial field theory]], and relies on the idea that any QFT $T$ defines a [[topological field theory]] $Sym(T)$ defined by the generalized symmetries of $T$, called the *Symmetry TFT* and that, in turn, $T$ can be recovered from $Sym(T)$ via manipulations on its boundary.

The main concept is that of a **quiche**, which is a pair $(\sigma,\rho)$ where $\sigma$ is a fully extended $(n+1)$-dimensional TFT, and $\rho$ is a $\sigma$-"module" (where the concept of module is defined only in analogy with a [[domain wall]] between TFT's). Then the statement that an $n$-dimensional QFT $T$ has $\sigma=Sym(T)$ as its symmetry theory consists of another pair $(\tilde{T},\theta)$ where $\tilde{T}$ is a $\sigma$-module and $\theta$ is an "isomorphism"

$$
\theta: \rho\otimes_{\sigma}\tilde{T} \cong T
$$

where $\rho\otimes_{\sigma}\tilde{T}$ is schematically understood as placing $\sigma$ on a spacetime $X^n\times [0,1]$ with $\rho$ on one end and $\tilde{T}$ on the other, such that collapsing the slab gives $T$ on $X^n$.

Some remarks about this proposal are in order. First, the kind of symmetries that are usually dealt with here are of finite character (related to a [[homotopy type with finite homotopy groups]] as explained in Appendix A). This allows to avoid discussions regarding smoothness of categories. However, as highlighted in ([Kang & Kang (2023)](#KK23)), overlooking this fact has led to some inaccurate conclusions obtained from applying techniques that in reality are valid only in the discrete setting but not in the smooth setting. Work aiming towards addressing this issue is in ([Gripaios, Randal-Williams, and Tooby-Smith (2023)](#GRT23)). Second, some statements (which are not necessarily minor points) are still only schematic. This includes the isomorphism $\theta$ mentioned. This is partly due to the following assertion: *"Recall that the cobordism hypothesis enables a calculus of such functors (FTFT's) in terms of duality data inside the codomain category C. Turning to nontopological theories, a similar calculus is not in place and is a subject of wide interest.*" ([FMT22](#FMT22), p. 10). In particular, the work of [Grady and Pavlov (2021)](#GradyPavlov21) on the *geometric* [[cobordism hypothesis]] has clear relevance to these two remarks.



## Related concepts

* [[QFT with defects]]

* [[duality in physics]]


## References
 {#References}

Early discussion of "generalized global symmetries" under the name of *[[QFT with defects|defects]]*, in [[2d conformal field theory]] (via the [[FRS theorem on rational 2d CFT]]):

* {#FRS02I} [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], _TFT construction of RCFT correlators I: Partition functions_, Nucl. Phys. B **646**  (2002) 353-497 &lbrack;[arXiv:hep-th/0204148](http://arxiv.org/abs/hep-th/0204148), <a href="https://doi.org/10.1016/S0550-3213(02)00744-7">doi:10.1016/S0550-3213(02)00744-7</a>&rbrack;

* {#FRS04} [[Jürg Fröhlich]], [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], *Kramers-Wannier duality from conformal defects*, Phys. Rev. Lett. **93** (2004) 070601 &lbrack;[doi:10.1103/PhysRevLett.93.070601](https://doi.org/10.1103/PhysRevLett.93.070601), [arXiv:cond-mat/0404051](http://arxiv.org/abs/cond-mat/0404051)&rbrack;

* {#FFRS07} [[Jürg Fröhlich]], [[Jürgen Fuchs]], [[Ingo Runkel]], [[Christoph Schweigert]], *Duality and defects in rational conformal field theory*, Nucl. Phys. B **763** (2007) 354-430 &lbrack;[arXiv:hep-th/0607247](http://arxiv.org/abs/hep-th/0607247), [doi:10.1016/j.nuclphysb.2006.11.017](https://doi.org/10.1016/j.nuclphysb.2006.11.017)&rbrack;

The terminology "categorical (symmetry)-groups" for *[[2-groups]]* goes back to the origin of the subject in

* {#Solian80} [[Alexandru Solian]], *Coherence in categorical groups*,  Communications in Algebra **9** 10 (1980) 1039-1057 &lbrack;[doi:10.1080/00927878108822631](https://doi.org/10.1080/00927878108822631)&rbrack;

Early appearance of the terminology "categorified symmetries" is in:

* [[Urs Schreiber]], [[Zoran Škoda]], *Categorified symmetries*, 5th Summer School of Modern Mathematical Physics, SFIN XXII Series **A1** (2009) 397-424 &lbrack;[arXiv:1004.2472](https://arxiv.org/abs/1004.2472), [inspire:851901](https://inspirehep.net/literature/851901)&rbrack;

The terminology of *generalized global symmetries* is due to:

* {#GaiottoKapustinSeibergWillett14} [[Davide Gaiotto]], [[Anton Kapustin]], [[Nathan Seiberg]], [[Brian Willett]], *Generalized Global Symmetries*  J. High Energ. Phys. **2015** 172 (2015) &lbrack;[arXiv:1412.5148](https://arxiv.org/abs/1412.5148), <a href="https://doi.org/10.1007/JHEP02(2015)172">doi:10.1007/JHEP02(2015)172</a>&rbrack;

Survey of the "field":

* [[Clay Cordova]], [[Thomas T. Dumitrescu]], [[Kenneth Intriligator]], [[Shu-Heng Shao]], *Snowmass White Paper: Generalized Symmetries in Quantum Field Theory and Beyond* &lbrack;[arXiv:2205.09545](https://arxiv.org/abs/2205.09545)&rbrack;

Lecture notes:

* [[Clay Cordova]], [[Michele Del Zotto]], [[Daniel Freed]], [[David Jordan]], [[Kantaro Ohmori]]. *Simons Lectures on Categorical Symmetries* (2024). ([arXiv:2411.09082](https://arxiv.org/abs/2411.09082)).


Further suggestion for mathematical formalization of what [GKSW14](#GaiottoKapustinSeibergWillett14) had in mind (purely at the quantum level, with caveats):

* {#FMT22} [[Daniel Freed]], [[Gregory Moore]], [[Constantin Teleman]], *Topological symmetry in quantum field theory* (2022) &lbrack;[arXiv:2209.07471](https://arxiv.org/abs/2209.07471)&rbrack;

rooted in

* {#FHTL09} [[Daniel Freed]], [[Mike Hopkins]], [[Constantin Teleman]], [[Jacob Lurie]], *[[Topological Quantum Field Theories from Compact Lie Groups]]*, in: *A celebration of the mathematical legacy of Raoul Bott*, AMS (2010) &lbrack;[arXiv:0905.0731](http://arxiv.org/abs/0905.0731), [ISBN:978-0-8218-4777-0](https://bookstore.ams.org/view?ProductCode=CRMP/50)&rbrack;

Gauging of generalized global symmetries of TQFTs: 

* {#CarquevilleRunkelSchaumann} [[Nils Carqueville]], [[Ingo Runkel]], [[Gregor Schaumann]], _Orbifolds of $n$-dimensional defect TQFTs_, Geom. Topol. **23** (2019) 781-864 *lbrack;[arXiv:1705.06085](https://arxiv.org/abs/1705.06085), [doi:10.2140/gt.2019.23.781](https://doi.org/10.2140/gt.2019.23.781)&rbrack;

* [[Nils Carqueville]], [[Ingo Runkel]], *Orbifold completion of defect bicategories*, ([arXiv:1210.6363](https://arxiv.org/abs/1210.6363))

* [[Nils Carqueville]], *Orbifolds of topological quantum field theories*, in: *[[Encyclopedia of Mathematical Physics 2nd ed]]* &lbrack;[arXiv:2307.16674](https://arxiv.org/abs/2307.16674)&rbrack;



See also:

* {#Vafa89} [[Cumrun Vafa]], *Quantum Symmetries of String Vacua* (1989) &lbrack;[doi:10.1142/S0217732389001842](https://doi.org/10.1142/S0217732389001842)&rbrack;

* {#BT17} [[Lakshya Bhardwaj]], [[Yuji Tachikawa]]. *On finite symmetries and their gauging in two dimensions*, J. High Energ. Phys. **2018** 189 (2018) &lbrack;[arXiv:1704.02330](https://arxiv.org/abs/1704.02330), <a href="https://doi.org/10.1007/JHEP03(2018)189">doi:10.1007/JHEP03(2018)189</a>&rbrack;

* {#GradyPavlov21} [[Daniel Grady]], [[Dmitri Pavlov]], *The geometric cobordism hypothesis* &lbrack;[arXiv:2111.01095](https://arxiv.org/abs/2111.01095)&rbrack;

* {#PutrovWang23} [[Pavel Putrov]], [[Juven Wang]], *Categorical Symmetry of the Standard Model from Gravitational Anomaly* &lbrack;[arXiv:2302.14862](https://arxiv.org/abs/2302.14862)&rbrack;

* Masaki Okada, [[Yuji Tachikawa]]. *Non-invertible symmetries act locally by quantum operations* (2024). ([arXiv:2403.20062](https://arxiv.org/abs/2403.20062)).


In the context of [[fusion 2-categories]]:

* {#DY23} [[Thibault Decoppet]], [[Matthew Yu]], *Fiber 2-Functors and Tambara-Yamagami Fusion 2-Categories* (2023) &lbrack;[arXiv:2306.08117](https://arxiv.org/abs/2306.08117)&rbrack;

* Wenjie Xi, Tian Lan, Longye Wang, Chenjie Wang, Wei-Qiang Chen, *On a class of fusion 2-category symmetry: condensation completion of braided fusion category* &lbrack;[arXiv:2312.15947](https://arxiv.org/abs/2312.15947)&rbrack;

and for $3$-fusion categories

* {#BDSY24} Lakshya Bhardwaj, Thibault Décoppet, Sakura Schäfer-Nameki, Matthew Yu. *Fusion 3-Categories for Duality Defects* (2024). ([arXiv:2408.13302](https://arxiv.org/abs/2408.13302)).

based on the definition of fusion $n$-categories in

* {#JF20nf} Theo Johnson-Freyd. *On the classification of topological orders* (2020). ([arXiv:2003.06663](https://arxiv.org/abs/2003.06663)).

In the context of [[factorization algebra|factorization algebras]], see

* [[Kevin Costello]], [[Owen Gwilliam]]. *Factorization algebra* (2023). ([arXiv:2310.06137](https://arxiv.org/abs/2310.06137)).

in particular Section 6 therein.


Work in the direction of *smooth* generalized symmetries:

* {#GRT23} [[Ben Gripaios]], [[Oscar Randal-Williams]], [[Joseph Tooby-Smith]], *Smooth generalized symmetries of quantum field theories*, J. Geom. Phys.  (2024) &lbrack;[arXiv:2310.16090](https://arxiv.org/abs/2310.16090), <a href="https://doi.org/10.1016/j.geomphys.2024.105212">doi:10.1016/j.geomphys.2024.105212</a>&rbrack;

Notes on a more proper treatment of *smooth* 2-groups in the present context is in:

* {#KK23} Monica Jinwoo Kang, Sungkyung Kang, *Central extensions of higher groups: Green-Schwartz mechanism and 2-connections* ([arXiv:2311.14666](https://arxiv.org/abs/2311.14666))

On the extension of this notion to [[supergroup|fermionic symmetries]] see e.g.

* Federico Ambrosino, Ran Luo, Yi-Nan Wang, Yi Zhang. *Understanding Fermionic Generalized Symmetries* (2024). ([arXiv:2404.12301](https://arxiv.org/abs/2404.12301)).

* P. A. Grassi, S. Penati. *Super-Higher-Form Symmetries* (2025). ([arXiv:2503.16182](https://arxiv.org/abs/2503.16182)).

On conserved currents (of putative global higher symmetries) coming from [[Chern-Weil theory]]

* Ben Heidenreich, Jacob McNamara, Miguel Montero, Matthew Reece, Tom Rudelius, Irene Valenzuela. *Chern-Weil Global Symmetries and How Quantum Gravity Avoids Them* (2020). ([arXiv:2012.00009](https://arxiv.org/abs/2012.00009)).

Via [[factorization algebras]] and [[classifying spaces]]:

* [[Owen Gwilliam]]: *Remarks on the locality of generalized global symmetries* &lbrack;[arXiv:2504.05626](https://arxiv.org/abs/2504.05626)&rbrack;


Further activity:

* {#CategoricalSymmetries23} *Categorical Symmetries in Quantum Field Theory* (28 Aug -1 Sept 2023) &lbrack;[indico:1131193](https://indico.cern.ch/event/1131193)&rbrack;


[[!redirects generalized global symmetries]]

[[!redirects generalized symmetry]]
[[!redirects generalized symmetries]]
[[!redirects non-invertible symmetry]]
[[!redirects non-invertible symmetries]]
[[!redirects noninvertible symmetry]]
[[!redirects noninvertible symmetries]]

[[!redirects higher form symmetry]]
[[!redirects higher form symmetries]]
[[!redirects higher-form symmetry]]
[[!redirects higher-form symmetries]]

[[!redirects categorified symmetry]]
[[!redirects categorified symmetries]]



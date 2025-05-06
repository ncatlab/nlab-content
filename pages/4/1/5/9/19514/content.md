

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[anti de Sitter group]] $SO(2,D-1)$ has "ultra-short" [[unitary representations]] that admit no [[Minkowski spacetime]]-limit (along the [[Lie algebra contraction]]). For $D = 4$ these were first discussed by [Dirac 63](#Dirac63) and named _singletons_. 

More generally, given a (non-[[compact Lie group|compact]]) [[Lie group]] $G$ admitting [[lowest weight representation]] with [[maximal compact subgroup]] of the form $H \times U(1)$ for some other [[compact Lie group]] $H$, the _oscillator method_ is to describe [[unitary representation]] by realizing the generators of $G$ as [[creation and annihilation operators]] on some [[Fock space]], and have them transform in the (anti-)[[fundamental representation]] of $H$. Then a _singleton representation_ is one where the generators are realized as the creators and annihilators of a single oscillator, and there are typically two of these (usually the scalar and spinor representations, in a physical language).

A _doubleton representation_ is one where the generators are realized as two sets of oscillators, and so forth.

## In AdS/CFT

It was observed by  [Fronsdal 81](#Fronsdal81), [Flato & Fronsdal 81](#FlatoFronsdal81), [Angelopoulos, Flato, Fronsdal & Sternheimer 81](#AngelopoulosFlatoFronsdalSternheimer81) that these representations may naturally be understood as arising in [[free field theory]] on the [[asymptotic boundary]] of [[anti de Sitter spacetime]].

Analogous statements hold true for the [[super anti de Sitter group]] (e.g. [Gunyadin 89](#Gunyadin89))

Based on this observation, it was conjectured in [Duff 88, p. 29-30](#Duff88) that the singleton representation of $SO(3,2)$ is realized by the [[field (physics)|field]] content of the [[worldvolume]]-theory of a [[Green-Schwarz sigma model|fundamental]] [[M2-brane]] stretched along the [[asymptotic boundary]] of [[anti de Sitter spacetime]] factor $AdS_{4}$ in a [[Freund-Rubin compactification]] of [[11-dimensional supergravity]]. [^Dirac ]

[^Dirac]: Curiously, also the idea of a fundamental [[membrane]] is due to [[Paul Dirac]] ([Dirac 62](supermembrane#Dirac62))

This conjecture was shown to be true in ... and is a pre-cursor of what is now known as the _[[AdS-CFT correspondence]]_ (see [Duff 98](#Duff98) for review). See also at _[super p-brane -- As part of the AdS-CFT correspondence](Green-Schwarz+action+functional#AsPartOfTheAdSCFTCorrespodence)_.

From [Gunyadin 98, p. 2](#Gunyadin98)

> The ultra-short singleton supermultiplet sits at the bottom of this infinite tower of Kaluza-Klein modes and decouple from the spectrum as local gauge degrees of freedom [25]. However , even though the singleton supermultiplet decouples from the spectrum as local gauge modes, one can generate the entire spectrum of 11-dimensional supergravity over $S^7$ by tensoring the singleton supermultiplets repeatedly and restricting oneself
to "CPT self-conjugate" vacuum supermultiplets.

## References

* {#Dirac63} [[Paul Dirac]], _A remarkable representation of the 3+2 de Sitter group_, Journal of Mathematical Physics, 4(7), 901-909, 1963 ([doi:10.1063/1.1704016](https://aip.scitation.org/doi/pdf/10.1063/1.1704016))

* {#Fronsdal81} [[Christian Fronsdal]], _Dirac supermultiplet_, Phys. Rev. D **26** (1982) 1988 &lbrack;[doi:10.1103/PhysRevD.26.1988](https://doi.org/10.1103/PhysRevD.26.1988)&rbrack;

* {#FlatoFronsdal81} [[Moshé Flato]], [[Christian Fronsdal]], _Quantum field theory of singletons. The rac_, J. Math. Phys. **22** (1981) 1100 &lbrack;[doi:10.1063/1.524993](https://doi.org/10.1063/1.524993)&rbrack;



* {#AngelopoulosFlatoFronsdalSternheimer81} E. Angelopoulos, [[Moshe Flato]], [[Christian Fronsdal]], [[Daniel Sternheimer]], _Massless Particles, Conformal Group, and De Sitter Universe_, Phys. Rev. D23 (1981) 1278

* [[Sergio Ferrara]], [[Christian Fronsdal]], _Conformal Maxwell theory as a singleton field theory on $AdS_5$, IIB three-branes and duality_, Class.Quant.Grav.15:2153-2164, 1998 ([arXiv:hep-th/9712239](https://arxiv.org/abs/hep-th/9712239))

* {#Gunyadin89} [[Murat Günaydin]], _Singleton And Doubleton Supermultiplets Of Space-time Supergroups And Infinite Spin Superalgebras_, 1989 ([spire:282501](http://inspirehep.net/record/282501/))

* {#Duff88} [[Mike Duff]], _Supermembranes: The First Fifteen Weeks_, Class.Quant.Grav. 5 (1988) 189 ([spire:248034](http://inspirehep.net/record/248034))

* [[Eric Bergshoeff]], [[Mike Duff]], [[Christopher Pope]] and [[Ergin Sezgin]], _Supersymmetric supermembrane vacua and singletons_, Phys. Lett. B199, 69 (1988)

* [[Gianguido Dall'Agata]], Davide Fabbri, Christophe Fraser, [[Pietro Fré]], Piet Termonia, Mario Trigiante, _The $Osp(8|4)$ singleton action from the supermembrane_, Nucl.Phys.B542:157-194, 1999 ([arXiv:hep-th/9807115](http://arxiv.org/abs/hep-th/9807115))

* [[Paolo Pasti]], [[Dmitri Sorokin]], Mario Tonin, _Branes in Super-AdS Backgrounds and Superconformal Theories_ ([arXiv:hep-th/9912076](http://arxiv.org/abs/hep-th/9912076))

* {#Duff98} [[Mike Duff]], _Anti-de Sitter space, branes, singletons, superconformal field theories and all that_, Int. J. Mod. Phys. A **14** (1999) 815-844, &lbrack;[arXiv:hep-th/9808100](https://arxiv.org/abs/hep-th/9808100)&rbrack;

* {#Gunyadin98} [[Murat Günaydin]], _Unitary Supermultiplets of $OSp(1 \vert32,\mathbb{R}$) and M-theory_, Nucl. Phys. B **528** (1998) 432-450 &lbrack;[arXiv:hep-th/9803138](https://arxiv.org/abs/hep-th/9803138)&rbrack;

* [[Henning Samtleben]], [[Ergin Sezgin]]: *Singletons in supersymmetric field theories and in supergravity* &lbrack;[arXiv:2409.03000](https://arxiv.org/abs/2409.03000)&rbrack;

* M. A. Vasiliev: *Dirac Singleton as a Relativistic Field Beyond Standard Model* &lbrack;[arXiv:2505.01915](https://arxiv.org/abs/2505.01915)&rbrack;





[[!redirects singleton representations]]



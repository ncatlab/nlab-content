
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _multi trace observable_ in a [[gauge theory]] is a [[polynomial]] in [[single trace operators]] (see there for more background). 





## Properties

### Under AdS/CFT correspondence

Under the [[AdS/CFT correspondence]], [[single trace observables]] in the gauge theory correspond to single particle/string excitations on the [[gravity]]-side, while multi-trace observables correspond to multi-particle/string excitations ([Liu 98, p. 6 (7 of 39)](#Liu98), [Andrianapoli-Ferrara 99, p. 13](#AndrianapoliFerrara99), [Chalmers-Schalm 00, Section 7](#ChalmersSchalm00), [Aharony-Gubser-Maldacena-Ooguri-Oz 99, p. 75](#AharonyGubserMaldacenaOoguriOz9))

The [[asymptotic boundary|asymptotic]] [[boundary conditions]] for [[field (physics)|fields]] $\Phi$ on the AdS-side 

$$
  \Phi(\vec x, r)
  \overset{r \to 0}
  \sum_i
  \alpha_i (\vec x)
  r^{d -\lambda_i}
  + 
  \cdots
$$

that correspond to multi-trace observables $W(\{\mathcal{O}_i\})$ have [[coefficients]] given by the [[derivative]] of the multi-trace [[polynomial]] by its single-trace variables $\mathcal{O}_i$:

$$
  \alpha_i
  =
  \partial_{\mathcal{O}_i}
  W
  (\{\langle\mathcal{O}_i\rangle\})
$$

([Witten 01, Section 3](#Witten01))

## Examples


[[!include chord diagrams as multi-trace observables in BMN matrix model -- example]]

## References

Discussion of [[multi-trace operators]] in [[super Yang-Mills theory]] and of their [[AdS-CFT duality|AdS-CFT dual]] [[gravity]]/[[string theory]] incarnation:

* [[Tom Banks]], [[Michael Douglas]], [[Gary Horowitz]], [[Emil Martinec]], _AdS Dynamics from Conformal Field Theory_ ([arXiv:hep-th/9808016](https://arxiv.org/abs/hep-th/9808016), [spire:474214](http://inspirehep.net/record/474214))

* {#Liu98} [[Hong Liu]], _Scattering in Anti-de Sitter Space and Operator Product Expansion_, Phys. Rev. D 60, 106005 (1999) ([arXiv:hep-th/9811152](https://arxiv.org/abs/hep-th/9811152))

* {#AndrianapoliFerrara99} [[Laura Andrianopoli]], [[Sergio Ferrara]], _On short and long $SU(2,2/4)$ multiplets in the AdS/CFT correspondence_, Lett. Math.Phys. 48 (1999) 145-161 ([arXiv:hep-th/9812067](https://arxiv.org/abs/hep-th/9812067))

* {#ChalmersSchalm00} Gordon Chalmers, Koenraad Schalm, _Holographic Normal Ordering and Multi-particle States in the AdS/CFT Correspondence_, Phys. Rev. D61:046001, 2000 ([arXiv:hep-th/9901144](https://arxiv.org/abs/hep-th/9901144))

* {#AharonyGubserMaldacenaOoguriOz99} [[Ofer Aharony]], [[Steven Gubser]], [[Juan Maldacena]], [[Hirosi Ooguri]], [[Yaron Oz]], _Large $N$ Field Theories, String Theory and Gravity_, Phys. Rept. 323:183-386, 2000 ([arXiv:hep-th/9905111](http://arxiv.org/abs/hep-th/9905111))

* Massimo Bianchi, Stefano Kovacs, Giancarlo Rossi, Yassen S. Stanev, _On the logarithmic behaviour in $\mathcal{N}=4$ SYM theory_, JHEP 9908 (1999) 020 ([arXiv:hep-th/9906188](https://arxiv.org/abs/hep-th/9906188))

* Witold Skiba, _Correlators of Short Multi-Trace Operators in $\mathcal{N}=4$ Supersymmetric Yang-Mills_, Phys. Rev. D 60, 105038 (1999) ([arXiv:hep-th/9907088](https://arxiv.org/abs/hep-th/9907088))

* [[Eric D'Hoker]], [[Daniel Freedman]], [[Samir Mathur]], A. Matusis, [[Leonardo Rastelli]], _Extremal Correlators in the AdS/CFT Correspondence_, in: _[[The many faces of the superworld]]_ ([arXiv:hep-th/9908160](https://arxiv.org/abs/hep-th/9908160))

* [[Gleb Arutyunov]], [[Sergey Frolov]], A. C. Petkou, _Perturbative and instanton corrections to the OPE of CPOs in $\mathcal{N}=4$ $SYM_4$_, Nucl. Phys. B602:238-260, 2001; Erratum-ibid. B609:540, 2001 ([arXiv:hep-th/0010137](https://arxiv.org/abs/hep-th/0010137))


* [[Ofer Aharony]], [[Micha Berkooz]], [[Eva Silverstein]], _Multiple-Trace Operators and Non-Local String Theories_, JHEP 0108:006, 2001 ([arXiv:hep-th/0105309](https://arxiv.org/abs/hep-th/0105309))


* [[Ofer Aharony]], [[Micha Berkooz]], [[Eva Silverstein]], _Non-local string theories on $AdS_3$ times $S^3$ and stable non-supersymmetric backgrounds_, Phys. Rev. D65:106007, 2002 ([arXiv:hep-th/0112178](https://arxiv.org/abs/hep-th/0112178))

* L. Hoffmann, L. Mesref, A. Meziane, W. Rühl, _Multi-trace quasi-primary fields of $\mathcal{N}=4$ $SYM_4$ from AdS $n$-point functions_, Nucl. Phys. B641 (2002) 188-222 ([arXiv:hep-th/0112191](https://arxiv.org/abs/hep-th/0112191))


* {#Witten01} [[Edward Witten]], _Multi-Trace Operators, Boundary Conditions, And AdS/CFT Correspondence_ ([arXiv:hep-th/0112258](https://arxiv.org/abs/hep-th/0112258))

* [[Steven Gubser]], Indrajit Mitra, _Double-trace operators and one-loop vacuum energy in AdS/CFT_, Phys. Rev. D67 (2003) 064018 ([arXiv:hep-th/0210093](https://arxiv.org/abs/hep-th/0210093))

* [[Vijay Balasubramanian]], [[Jan de Boer]], [[Bo Feng]], [[Yang-Hui He]], Min-xin Huang, Vishnu Jejjala, Asad Naqvi, _Multi-Trace Superpotentials vs. Matrix Models_, Commun. Math. Phys. 242:361-392, 2003 ([arXiv:hep-th/0212082](https://arxiv.org/abs/hep-th/0212082))



* [[Steven Gubser]], [[Igor Klebanov]], _A universal result on central charges in the presence of double-trace deformations_, Nucl. Phys. B656 (2003) 23-36 ([arXiv:hep-th/0212138](https://arxiv.org/abs/hep-th/0212138))


* P. J. Heslop, [[Paul Howe]], _Aspects of $\mathcal{N}$=4 SYM_, JHEP 0401 (2004) 058 ([arXiv:hep-th/0307210](https://arxiv.org/abs/hep-th/0307210))

* Thomas Hartman, [[Leonardo Rastelli]], _Double-Trace Deformations, Mixed Boundary Conditions and Functional Determinants in AdS/CFT_, JHEP 0801:019, 2008 ([arXiv:hep-th/0602106](https://arxiv.org/abs/hep-th/0602106))

Textbook account:

* {#HartnollLucasSachdev16} [[Sean Hartnoll]], [[Andrew Lucas]], [[Subir Sachdev]], Section 1.7.3 of: _Holographic quantum matter_, MIT Press 2018 ([arXiv:1612.07324](https://arxiv.org/abs/1612.07324), [publisher](https://mitpress.ublish.com/book/holographic-quantum-matter))

  (with an eye towards [[AdS/CFT in condensed matter physics]])


[[!redirects multi-trace operators]]

[[!redirects multi trace operator]]
[[!redirects multi trace operators]]


[[!redirects multi-trace observable]]
[[!redirects multi-trace observables]]

[[!redirects multi trace observable]]
[[!redirects multi trace observables]]




[[!redirects double-trace operator]]
[[!redirects double-trace operators]]

[[!redirects double trace operator]]
[[!redirects double trace operators]]

[[!redirects double-trace observable]]
[[!redirects double-trace observables]]

[[!redirects double trace observable]]
[[!redirects double trace observables]]



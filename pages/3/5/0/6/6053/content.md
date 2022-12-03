
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Drinfel'd double_- or _quantum double_-construction a sends a [[Hopf algebra]] to a [[quasi-triangular Hopf algebra]] &lbrack;[Drinfeld (1987)](#Drinfeld87)&rbrack;; or more generally, it sends a [[quasi-Hopf algebra]] to a [[quasi-triangulated quasi-Hopf algebra]] &lbrack;[Majid (1994)](#Majid)&rbrack;.

Geometrically, if the given [[Hopf algebra]] is the [[group algebra]] of a [[finite group]] $G$, then the quantum double is the [[groupoid convolution algebra]] of the corresponding [[inertia groupoid]] $\mathcal{L}\mathbf{B}G \simeq G \sslash_{ad} G$ (this is made almost explicit in [Dijkgraaf, Pasquier & Roche (1990), eq. 2.1.10](#DijkgraafPasquierRoche90); the [[categorification|categorified]] version of this statement is highlighted in [Hinich (2007)](#Hinich07)). 

More generally, if the given [[quasi-Hopf algebra]] is the [[twisted groupoid convolution algebra]] of a [[group cohomology]] 3-[[cocycle]] $c \colon \mathbf{B}G \to \mathbf{B}^3 U(1)$, then the corresponding quantum double is the [[twisted groupoid convolution algebra]] of the [[inertia groupoid]] equipped with the [[transgression in group cohomology|transgressed]] 2-cocycle &lbrack;[Willerton (2005)](#Willerton)&rbrack;



## Definition

Given a [[field]] $k$, __Drinfel'd__ (or Drinfeld or quantum) __double__ of a finite dimensional Hopf $k$-algebra $H$ is the tensor product algebra $D(H) = H\otimes H^*$ where $H^* = Hom_k(H, k)$ with induced canonical Hopf algebra structure. It appears that the canonical element in $D(H)$ (the image of the identity under the isomorphism $Hom_k(H,H) \cong H\otimes H^*$) is a universal $R$-element in $D(H)$ making it into a [[quasitriangular Hopf algebra]], which is making it "almost commutative". 

This quasitriangular structure in some infinite-dimensional versions of the construction is related to the quasitriangular structure on some [[quantum groups]]. 


## Properties

### Relation to Yetter-Drinfeld modules


The [[category of modules]] over a quantum double of a Hopf algebra $H$ is equivalent to the category of [[Yetter-Drinfeld modules]] of $H$-

### Relation to Drinfeld center

For $H$ a [[Hopf algebra]] arising as the [[groupoid convolution algebra]] of a finite [[groupoid]], the [[category of modules]] of its Drinfeld double is equivalently the [[Drinfeld center]] of the category of modules of the original algebra.

More generally, the analog of this statement holds for [[orbifolds]] ([Hinich (2007)](#Hinich07)).

[[!include structure on algebras and their module categories - table]]


## Related concepts

* [[inertia orbifold]], [[transgression in group cohomology]]

* [[Drinfeld center]]


## References

The original articles:

* {#Drinfeld87} [[Vladimir Drinfeld]], _Quantum groups_, in: A. Gleason (ed.) *[Proceedings of the](https://archive.org/details/proceedingsofint0002inte_v5c3/mode/2up) [1986 International Congress of Mathematics](https://inspirehep.net/conferences/966215?ui-citation-summary=true)* **1** (1987) 798-820 &lbrack;[pdf](https://www.mathunion.org/fileadmin/ICM/Proceedings/ICM1986.1/ICM1986.1.ocr.pdf)&rbrack;

  expanded version:

  Journal of Soviet Mathematics **41** (1988) 898–915 &lbrack;[doi:10.1007/BF01247086](https://doi.org/10.1007/BF01247086)&rbrack;

* [[Shahn Majid]], _Doubles of quasitriangular Hopf algebras_, Comm. Algebra __19__ 11 (1991) 3061-3073 &lbrack;[MR92k:16052](http://www.ams.org/mathscinet-getitem?mr=1132774) [doi:10.1080/00927879108824306](http://dx.doi.org/10.1080/00927879108824306)&rbrack; 

* [[Shahn Majid]], _Some remarks on the quantum double_, Czechoslovak J. Phys. __44__ 11-12 (1994) 1059-1071 &lbrack;[arXiv:hep-th/9409056](https://arxiv.org/abs/hep-th/9409056), [doi:10.1007/BF01690458](https://doi.org/10.1007/BF01690458)&rbrack;


Survery:

* [[Piotr Hajac]], *On and around the Drinfeld double* (2009) &lbrack;[pdf](http://www.impan.pl/~burgunde/WSBC09/Ddouble_Hajac.pdf), [[Hajac-DrinfeldDouble.pdf:file]]&rbrack;

The generalization of the double construction to [[quasi-Hopf algebras]] motivated by 

* {#DijkgraafPasquierRoche90} [[Robbert Dijkgraaf]], [[Vincent Pasquier]], [[Philippe Roche]], *QuasiHopf algebras, group cohomology and orbifold models*, Nucl. Phys. B Proc. Suppl **18** (1990) 60-72 &lbrack;<a href="https://doi.org/10.1016/0920-5632(91)90123-V">doi:10.1016/0920-5632(91)90123-V</a>&rbrack;

* [[Robbert Dijkgraaf]], [[Vincent Pasquier]], [[Philippe Roche]], _Quasi-quantum groups related to orbifold models_, *International Colloquium on Modern Quantum Field Theory* (Bombay, 1990), 375-383, World Sci. (1991) &lbrack;[cds:206306](https://cds.cern.ch/record/206306?ln=ka), [[DPR-QuasiQuantumGroups.pdf:file]]&rbrack;

which is reviewed in 

*  A. Coste, J-M. Maillard, _Representation Theory of Twisted Group Double_, Annales Fond.Broglie 29 (2004) 681-694, ([arXiv:hep-th/0309257](http://arxiv.org/abs/hep-th/0309257))

was obtained in  

* {#Majid} [[Shahn Majid]], _Quantum double for quasi-Hopf algebras_, Lett. Math. Phys. __45__ (1998), no. 1, 1&#8211;9, [MR2000b:16077](http://www.ams.org/mathscinet-getitem?mr=1631648), [doi](http://dx.doi.org/10.1023/A:1007450123281), [q-alg/9701002](http://arxiv.org/abs/q-alg/9701002) 

* [[Shahn Majid]], _Cross product quantisation, nonabelian cohomology and twisting of Hopf algebras_, [hep-th/9311184](http://arxiv.org/abs/hep-th/9311184)

Interpretation via [[transgression in group cohomology]]:

* {#Willerton08} [[Simon Willerton]], Section 1 of: *The twisted Drinfeld double of a finite group via gerbes and finite groupoids*, Algebr. Geom. Topol. 8 (2008) 1419-1457 &lbrack;[arXiv:math/0503266](https://arxiv.org/abs/math/0503266), [doi:10.2140/agt.2008.8.1419](https://doi.org/10.2140/agt.2008.8.1419)&rbrack;


The special case of the Drinfeld double of a [[finite group]] is discussed further in 

* Hui-Xiang Chen, Gerhard Hiss, _Notes on the Drinfeld double of a finite-dimensional group algebra_ ([pdf](http://www.math.rwth-aachen.de/~Gerhard.Hiss/Preprints/drindouble.pdf))

A characterization of the (quasi-)Hopf algebras arising this way is in 

* Sonia Natale, _On group theoretical Hopf algebras and exact factorization of finite groups_ ([arXiv:math/0208054](http://arxiv.org/abs/math/0208054))

The equivalence of category of modules over the Drinfeld double for the case of [[orbifolds]], hence representations of the [[inertia orbifold]], with the [[Drinfeld center]] of the category of representations of the original orbifold is discussed in

* {#Hinich07} [[Vladimir Hinich]], *Drinfeld double for orbifolds*, in *Quantum Groups*, Contemporary Math **433** AMS (2007) 251-265 &lbrack;[math.QA/0511476](http://arxiv.org/abs/math/0511476), [doi:10.1090/conm/433](http://dx.doi.org/10.1090/conm/433)&rbrack;
 

[[!redirects Drinfel'd doubles]]

[[!redirects Drinfeld double]]
[[!redirects Drinfeld doubles]]

[[!redirects quantum double]]
[[!redirects quantum doubles]]

[[!redirects twisted Drinfeld double]]
[[!redirects twisted Drinfeld doubles]]



 
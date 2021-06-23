
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

The _Drinfel'd double_ or _quantum double_ construction is a construction that sends a [[Hopf algebra]] to a [[quasi-triangular Hopf algebra]] ([Drinfeld 87](#Drinfeld87)). Or more generally, it sends a [[quasi-Hopf algebra]] to a [[quasi-triangulated quasi-Hopf algebra]] ([Majid 94](#Majid)).

Geometrically, if the given [[Hopf algebra]] is the [[group algebra]] of a [[finite group]] $G$, then the quantum double is the [[groupoid convolution algebra]] of the corresponding [[inertia groupoid]] $\mathcal{L}\mathbf{B}G \simeq G//_{ad} G$. More generally, if the given [[quasi-Hopf algebra]] is the [[twisted groupoid convolution algebra]] of a [[group cohomology]] 3-[[cocycle]] $c \colon \mathbf{B}G \to \mathbf{B}^3 U(1)$, then the corresponding quantum double is the [[twisted groupoid convolution algebra]] of the [[inertia groupoid]] equipped with the [[transgression|transgressed]] 2-cocycle ([Willerton 05](#Willerton))



## Definition

Given a [[field]] $k$, __Drinfel'd__ (or Drinfeld or quantum) __double__ of a finite dimensional Hopf $k$-algebra $H$ is the tensor product algebra $D(H) = H\otimes H^*$ where $H^* = Hom_k(H, k)$ with induced canonical Hopf algebra structure. It appears that the canonical element in $D(H)$ (the image of the identity under the isomorphism $Hom_k(H,H) \cong H\otimes H^*$) is a universal $R$-element in $D(H)$ making it into a [[quasitriangular Hopf algebra]], which is making it "almost commutative". 

This quasitriangular structure in some infinite-dimensional versions of the construction is related to the quasitriangular structure on some [[quantum groups]]. 

## Properties

### Relation to Yetter-Drinfeld modules


The [[category of modules]] over a quantum double of a Hopf algebra $H$ is equivalent to the category of [[Yetter-Drinfeld modules]] of $H$-

### Relation to Drinfeld center

For $H$ a [[Hopf algebra]] arising as the [[groupoid convolution algebra]] of a finite [[groupoid]], the [[category of modules]] of its Drinfeld double is equivalently the [[Drinfeld center]] of the category of modules of the original algebra.

More generally, the analog of this statement holds for [[orbifolds]] ([Hinich 05](#Hinich)).

[[!include structure on algebras and their module categories - table]]


## Related concepts

* [[inertia orbifold]]

* [[Drinfeld center]]

## References

The original references are 

* [[Vladimir Drinfeld]], _Quantum groups_ In A. Gleason, editor, Proceedings of the ICM, pages 798&#8211;820, Rhode Island, 1987. AMS
 {#Drinfeld87}

* [[Shahn Majid]], _Doubles of quasitriangular Hopf algebras_, Comm. Algebra __19__:11. (1991), pp. 3061-3073 [MR92k:16052](http://www.ams.org/mathscinet-getitem?mr=1132774) [doi](http://dx.doi.org/10.1080/00927879108824306); _Some remarks on the quantum double_, Quantum groups and physics (Prague, 1994), Czechoslovak J. Phys. __44__ (1994), no. 11-12, 1059&#8211;1071 [doi](http://dx.do.org/10.1007/BF01690458)

A brief survey is in 

* Piotr Hajac, _On and around the Drinfeld double_, ([pdf](http://www.impan.pl/~burgunde/WSBC09/Ddouble_Hajac.pdf))

The generalization of the double construction to [[quasi-Hopf algebras]] motivated by 

* [[Robbert Dijkgraaf]], V. Pasquier, P. Roche, _QuasiHopf algebras, group cohomology and orbifold models_, Nucl. Phys. B Proc. Suppl. __18B__ (1990), 60-72; _Quasi-quantum groups related to orbifold models_, Modern quantum field theory (Bombay, 1990), 375&#8211;383, World Sci. 1991

which is reviewed in 

*  A. Coste, J-M. Maillard, _Representation Theory of Twisted Group Double_, Annales Fond.Broglie 29 (2004) 681-694, ([arXiv:hep-th/0309257](http://arxiv.org/abs/hep-th/0309257))

was obtained in  

* [[Shahn Majid]], _Quantum double for quasi-Hopf algebras_, Lett. Math. Phys. __45__ (1998), no. 1, 1&#8211;9, [MR2000b:16077](http://www.ams.org/mathscinet-getitem?mr=1631648), [doi](http://dx.doi.org/10.1023/A:1007450123281), [q-alg/9701002](http://arxiv.org/abs/q-alg/9701002)
 {#Majid}

* [[Shahn Majid]], _Cross product quantisation, nonabelian cohomology and twisting of Hopf algebras_, [hep-th/9311184](http://arxiv.org/abs/hep-th/9311184)

The geometric interpretation of this was discussed in 

* [[Simon Willerton]], _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv:math/0503266](http://arxiv.org/abs/math/0503266))

The special case of the Drinfeld double of a [[finite group]] is discussed further in 

* Hui-Xiang Chen, Gerhard Hiss, _Notes on the Drinfeld double of a finite-dimensional group algebra_ ([pdf](http://www.math.rwth-aachen.de/~Gerhard.Hiss/Preprints/drindouble.pdf))

A characterization of the (quasi-)Hopf algebras arising this way is in 

* Sonia Natale, _On group theoretical Hopf algebras and exact factorization of finite groups_ ([arXiv:math/0208054](http://arxiv.org/abs/math/0208054))

The equivalence of category of modules over the Drinfeld double for the case of [[orbifolds]], hence representations of the [[inertia orbifold]], with the [[Drinfeld center]] of the category of representations of the original orbifold is discussed in

* [[Vladimir Hinich]], _Drinfeld double for orbifolds_,  Contemporary Math, 433, AMS Providence, 2007, 251-265, [math.QA/0511476](http://arxiv.org/abs/math/0511476)
 {#Hinich}

Essentially the same conclusion (with similar motivation and in terms of equivariant fibres of monoidal fibered categories with orbifolds encoded as internal groupoid objects in the base) was independently obtained by [[Zoran Škoda]] at MPI Bonn in 2004 (unpublished).


[[!redirects Drinfel'd doubles]]

[[!redirects Drinfeld double]]
[[!redirects Drinfeld doubles]]

[[!redirects quantum double]]
[[!redirects quantum doubles]]


 
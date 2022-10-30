Given a $k$-[[bialgebra|bialgebra]] $(H,m_H,\eta,\Delta,\epsilon)$, a left-right **Hopf module** of $H$ is a $k$-[[module]] $M$ with the structure of left $H$-module and right $H$-comodule, where the action $\nu: H\otimes M\to M$ and right $H$-coaction $\rho : M\to M\otimes H$ are compatible in the sense that the coaction is a morphism of left modules (the structure of left module on $M\otimes H$ is the standard tensor product of modules over Hopf algebras, with action given in this case by 
$(\nu\otimes m_H)\circ(H\otimes \tau\otimes H)\circ(\Delta \otimes M\otimes H)$ as $k$-linear map $H\otimes(M\otimes H)\to M\otimes H$ where $\tau=\tau_{H,M}:H\otimes M\to M\otimes H$ is the standard flip of tensor factors in the [[symmetric monoidal category]] of $k$-modules).

An immediate generalization of Hopf modules is for the case where $E$ is a right $H$-comodule algebra (a monoid in the category of $H$-comodules); then one can define the category ${}_E\mathcal{M}^H$ of left $E$- right $H$- relative Hopf modules (less precisely, $(E,H)$-relative Hopf modules, or simply (relative) Hopf modules), which are left $E$-modules that are right $H$-comodules with a natural compatibility condition. There are further generalizations where instead of a bialgebra $H$ and a $H$-comodule algebra $E$ one replaces $E$ by an arbitrary algebra $A$, and $H$ by a coalgebra $C$ and introduces a compatibility in the sense of a mixed [[distributive law]] or [[entwining]] (structure). Then the relative Hopf modules become a special case of so-called entwined modules, see the monograph \[BW 2003\].

The entwined modules are first introduced under the name "bialgebras" by van Osdol (\[van Osdol 1973\]) in the more general case of monads and comonads instead of $k$-algebras and $k$-coalgebras. 

Geometrically, relative Hopf modules are instances of [[equivariant object]]s (equivariant quasicoherent sheaves) in [[noncommutative algebraic geometry]], the statement of which can be made precise, cf. \[&#352;koda 2008\].

Furthermore, in the context of relative Hopf modules there is an analogue of the faithfully flat descent along [[torsor]]s from commutative algebraic geometry, and the Galois descent theorems in algebra. Its main instance is [[Schneider's theorem]], asserting that if $H$ is a Hopf algebra and $U\hookrightarrow E$ a faithfully flat $H$-[[Hopf-Galois extension]] then the natural adjunction between the categories of relative $(E,H)$-Hopf modules and left $U$-modules is an [[equivalence of categories]]. This corresponds to the classical theorem saying that the category of equivariant quasicoherent sheaves over the total space of a torsor is equivalent to the category of the quasicoherent sheaves over the base of the torsor. 

One can also consider Hopf bimodules, and similar categories. The category ${}_H^H\mathcal{M}^H_H$ is related to the category of [[Yetter-Drinfeld module]]s.

# References #

* BW2003: [[T. Brzeziński]], R. Wisbauer, __Corings and comodules__, London Math. Soc. Lec. Note Series 309, Cambridge 2003.
* &#352;koda 2008: [[Z. Škoda]], _Some equivariant constructions in noncommutative algebraic geometry_ [arXiv:0811.4770](http://arxiv.org/abs/0811.4770)
* van Osdol 1973: D. H. van Osdol, _Bicohomology theory_, Trans. Amer. Math. Soc. __183__ (1973), 449--476. 
* Susan Montgomery, _Hopf algebras and their actions on rings_, 
CBMS Lecture Notes __82__, AMS 1993, 240p.
* Peter Schauenburg, _Hopf Modules and Yetter - Drinfel&#8242;d Modules_,
Journal of Algebra __169__:3 (1994) 874-890 [doi](http://dx.doi.org/10.1006/jabr.1994.1314); _Hopf modules and the double of a quasi-Hopf algebra_, Trans. Amer. Math. Soc. 354 (2002), 3349-3378 [doi](http://dx.doi.org/10.1090/S0002-9947-02-02980-X) [pdf](http://www.ams.org/journals/tran/2002-354-08/S0002-9947-02-02980-X/S0002-9947-02-02980-X.pdf); _Actions of monoidal categories, and generalized Hopf smash products_, Journal of Algebra __270__ (2003) 521-563, <a href="http://dx.doi.org/10.1016/S0021-8693(03)00403-4">doi</a> [ps](http://www.mathematik.uni-muenchen.de/%7Eschauen/papers/amcghsp.ps)
* A. Borowiec, G. A. Vazquez Coutino, _Hopf modules and their duals_, [math.QA/0007151](http://arxiv.org/abs/math/0007151)
* H-J. Schneider, _Principal homogeneous spaces for arbitrary Hopf algebras_, 
Israel J. Math. __72__ (1990), no. 1-2, 167&#8211;195 [MR92a:16047](http://www.ams.org/mathscinet-getitem?mr=1098988) [doi](http://dx.doi.org/10.1007/BF02764619)

[[!redirects Hopf modules]]
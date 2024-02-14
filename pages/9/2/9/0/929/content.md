
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

The Hopf modules over bimonoids are modules in the category of comodules 
or viceversa. This notion has many generalizations and variants. Relative Hopf modules
are an algebraic and possibly noncommutative analogue of a notion of an equivariant
sheaf.

## Definition

Given a $k$-[[bialgebra|bialgebra]] $(H,m_H,\eta,\Delta,\epsilon)$, a left-right **Hopf module** of $H$ is a $k$-[[module]] $M$ with the structure of left $H$-module and right $H$-[[comodule]], where the action $\nu: H\otimes M\to M$ and right $H$-coaction $\rho : M\to M\otimes H$ are compatible in the sense that the coaction is a morphism of left modules. In this, the structure of left module on $M\otimes H$ is the standard tensor product of modules over Hopf algebras, with the action given by $(\nu\otimes m_H)\circ(H\otimes \tau\otimes H)\circ(\Delta \otimes M\otimes H)$ as $k$-linear map $H\otimes(M\otimes H)\to M\otimes H$ where $\tau=\tau_{H,M}:H\otimes M\to M\otimes H$ is the standard flip of tensor factors in the [[symmetric monoidal category]] of $k$-modules. 

An immediate generalization of Hopf modules is for the case where $(E,\eho_E)$ is a right $H$-comodule algebra (a monoid in the category of $H$-comodules); then one can define the category ${}_E\mathcal{M}^H$ of left $E$- right $H$- __relative Hopf modules__ (less precisely, $(E,H)$-relative Hopf modules, or simply (relative) Hopf modules), which are left $E$-modules that are right $H$-comodules with a natural compatibility condition. In [[Sweedler notation]] for comodules. where $\rho(m) = \sum m_{(0)}\otimes m_{(1)}$, $\rho_E(e) = \sum e_{(0)}\otimes e_{(1)}$, the compatibility condition for the left-right relative Hopf modules is
$\rho (e m) = \sum e_{(0)} m_{(0)} \otimes e_{(1)} m_{(1)}$ for all $m\in M$ and $e\in E$. 

There are further generalizations where instead of a bialgebra $H$ and a $H$-comodule algebra $E$ one replaces $E$ by an arbitrary algebra $A$, and $H$ by a coalgebra $C$ and introduces a compatibility in the sense of a mixed [[distributive law]] or [[entwining]] (structure). Then the relative Hopf modules become a special case of so-called [[entwined module]]s, see the monograph \[BW 2003\]. 

Geometrically, relative Hopf modules are instances of [[equivariant object]]s (equivariant quasicoherent sheaves) in [[noncommutative algebraic geometry]], the statement of which can be made precise, cf. \[&#352;koda 2008\].

Furthermore, in the context of relative Hopf modules there is an analogue of the faithfully flat descent along [[torsor]]s from commutative algebraic geometry, and the Galois descent theorems in algebra. Its main instance is [[Schneider's theorem]], asserting that if $H$ is a Hopf algebra and $U\hookrightarrow E$ a faithfully flat $H$-[[Hopf-Galois extension]] then the natural adjunction between the categories of relative $(E,H)$-Hopf modules and left $U$-modules is an [[equivalence of categories]]. This corresponds to the classical theorem saying that the category of equivariant quasicoherent sheaves over the total space of a torsor is equivalent to the category of the quasicoherent sheaves over the base of the torsor. 

## Hopf bimodules

One can also consider Hopf bimodules, and similar categories. A Hopf $H$-bimodule is 
left and right $H$-comodule
and left and right $H$-bimodule, where all four
structure are compatible in standard way.  
The category of Hopf bimodules, ${}_H^H\mathcal{M}^H_H$ is monoidally equivalent to the category of [[Yetter-Drinfeld module]]s.

## Fundamental theorem on Hopf modules

If $H$ is a Hopf algebra over a field $k$, then the category of the ordinary Hopf modules ${}_H^H\mathcal{M}$ is equivalent to the category of $k$-vector spaces. See Section 1 of [Montgomery 1993](#Mont93) for more.

The equivalence may be seen as follows. Any vector space $V$ can be endowed with a (left-) Hopf module structure, for $H$ a Hopf algebra, simply by tensoring with $H$. The action of $H$ is given as

$$
\rho: h'\otimes h\otimes v\mapsto h'h\otimes v
$$

and the coaction as

$$
\sigma: h\otimes v\mapsto \Delta(h)\otimes v
$$

for $\Delta:H\to H\otimes H$ the comultiplication. This is known as a **trivial Hopf module**.

The fundamental theorem of Hopf modules states that *any* Hopf module $M$ arises precisely in this way, as one shows that

$$
M\cong H \otimes M^{\text{co} H} 
$$

where $M^{\text{co} H}:= \{m\in M \vert \sigma(m)= 1_H \otimes m\}$ is the space of coinvariant of $M$ under the coaction $\sigma$ of $H$. In fact, the operations 

$$
V \mapsto H\otimes V
$$

$$
M\mapsto M^{\text{co} H}
$$

come as functors realizing an equivalence of categories between vector spaces, and $H$-Hopf modules (see [Vercruysse 2012](#Vercruysse12) for more on this).

## References 

Related entries include [[comodule algebra]], [[Schneider's descent theorem]], [[Yetter-Drinfeld module]], [[entwined module]]

* BW2003: [[T. Brzeziński]], R. Wisbauer, __Corings and comodules__, London Math. Soc. Lec. Note Series 309, Cambridge 2003.
* &#352;koda 2008: [[Z. Škoda]], _Some equivariant constructions in noncommutative algebraic geometry_, Georgian Mathematical Journal __16__ (2009), No. 1, 183&#8211;202, [arXiv:0811.4770](https://arxiv.org/abs/0811.4770) [MR2011b:14004](https://www.ams.org/mathscinet-getitem?mr=2527623)
* {#Mont93} [[Susan Montgomery]], _Hopf algebras and their actions on rings_, CBMS Lecture Notes __82__, AMS 1993, 240p.
* Peter Schauenburg, _Hopf modules and Yetter - Drinfel&#8242;d modules_, J. Algebra __169__:3 (1994) 874-890 [doi](https://doi.org/10.1006/jabr.1994.1314); _Hopf modules and the double of a quasi-Hopf algebra_, Trans. Amer. Math. Soc. __354__ (2002), 3349-3378 [doi](https://doi.org/10.1090/S0002-9947-02-02980-X) [pdf](https://www.ams.org/journals/tran/2002-354-08/S0002-9947-02-02980-X/S0002-9947-02-02980-X.pdf); _Actions of monoidal categories, and generalized Hopf smash products_, Journal of Algebra __270__ (2003) 521-563, <a href="https://doi.org/10.1016/S0021-8693(03)00403-4">doi</a> [ps](http://www.mathematik.uni-muenchen.de/%7Eschauen/papers/amcghsp.ps)
* A. Borowiec, G. A. Vazquez Coutino, _Hopf modules and their duals_, [math.QA/0007151](http://arxiv.org/abs/math/0007151)
* H-J. Schneider, _Principal homogeneous spaces for arbitrary Hopf algebras_, 
Israel J. Math. __72__ (1990), no. 1-2, 167--195 [MR92a:16047](http://www.ams.org/mathscinet-getitem?mr=1098988) [doi](https://doi.org/10.1007/BF02764619)
* Francesco d'Andrea, Alessandro de Paris, _On noncommutative equivariant bundles_, [arXiv:1606.09130](http://arxiv.org/abs/1606.09130)

* {#Vercruysse12} [[Joost Vercruysse]]. *Hopf algebras---Variant notions and reconstruction theorems*. (2012). ([arXiv:1202.3613](https://arxiv.org/abs/1202.3613))


category: algebra
[[!redirects Hopf modules]]
[[!redirects Hopf bimodule]]
[[!redirects Hopf bimodules]]

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


##Definition##

Let $H$ be a $k$-[[bialgebra|bialgebra]] and $E$, say, a right $H$-comodule algebra (i.e. a [[monoid]] in the category of right $H$-[[comodule]]s) with coaction $\rho:E\to E\otimes H$, $e\mapsto \sum e_{(0)}\otimes e_{(1)}$.

The subalgebra $U = E^{\mathrm{co}H}$ of $H$-coinvariants in $E$ consists of all $u\in E$ such that $\rho(u)=u\otimes 1$.

The $k$-algebra **extension** $U\hookrightarrow E$ is __Hopf--Galois__ over $H$ if the natural map $E\otimes_U E\to E\otimes H$ given by the $k$-linear extension of the formula $e\otimes e'\mapsto (e\otimes_k 1)\rho(e') = \sum e e'_{(0)}\otimes e'_{(1)}$ is a bijection (hence a $k$-module isomorphism). 

A **Hopf--Galois object** over a $k$-bialgebra $H$ is any Hopf-Galois extension $k\hookrightarrow E$ over $H$ of the ground field (or ring) $k$. It is a dual (and noncommutative) analogue to a torsor over a point. 


##Classical Galois extensions as a special case##

If $k\subset U=E^G$, $k,E$ are [[field]]s, $G$ a finite group and $H = (k[G])^*$ is the dual [[Hopf algebra]] to the [[group algebra]] of $G$, then $E^G\hookrightarrow E$ is (classically) a [[Galois extension]] iff it is a $H$-Hopf--Galois extension, where the coaction of $H$ is induced by the action of $k[G]$, hence of $G$. One uses the Dedekind lemma on independence of automorphisms to prove this equivalence. It is possible however that $E^G\subset E$ is not (classically) Galois, but it is $K$-Hopf--Galois for some Hopf algebra $K\neq (k[G])^*$. 


##Role in geometry##

In [[algebraic geometry]], given an affine algebraic $k$-group [[scheme]] $G$, the algebra $E$ of regular functions over the total scheme $X$ of an affine $G$-[[torsor]] $X\to Y$, whose base $Y$ also happens to be affine, is a commutative $H$-Hopf--Galois extension of the algebra of regular functions $U$ on the base $Y\cong X/G$, where $H$ is the $k$-Hopf algebra of global regular functions on $G$. In algebraic topology, a generalization to [[spectrum|spectra]] (with the [[smash product]] of spectra in the role of tensor product) was studied by Rognes and others (see ([Rognes 08](#Rognes08))). In [[noncommutative geometry]], Hopf--Galois extensions are studied as affine [[noncommutative principal bundle]]s, with interesting [[descent]] theorems for [[Hopf module|Hopf modules]] like the [[Schneider's descent theorem]]. Given a right $H$-Hopf-Galois extension $U\hookrightarrow E$ and a left $H$-comodule $V$, the cotensor product $k$-module $E\Box^H V$ is interpreted as a space of sections of the associated [[fiber bundle]] with structure group $Spec H$ (in noncommutative sense) and fiber $V$. 


##Literature##

A class of Hopf-Galois extensions admitting a cleaving map   is dedicated a separate entry, [[cleft extension]].

### Early papers

* H. F. Kreimer, [[Mitsuhiro Takeuchi]], _Hopf algebras and Galois extensions of an algebra_, Indiana Univ. Math. J. 30 (1981), 615-692 [web](https://www.iumj.indiana.edu/IUMJ/fulltext.php?year=1981&volume=30&artid=30052) [pdf](https://www.iumj.indiana.edu/IUMJ/FTDLOAD/1981/30/30052/pdf) [djvu](https://www.iumj.indiana.edu/IUMJ/FTDLOAD/1981/30/30052/djvu)

* Y. Doi, M. Takeuchi, _Hopf-Galois extensions of algebras, the Miyashita-Ulbrich action, and Azumaya algebras_, J. Algebra 121 (1989) 488--516

[[Schneider's descent theorem]] for Hopf-Galois extensions is proven in 

* [[Hans-Jürgen Schneider]], _Principal homogeneous spaces for arbitrary Hopf algebras_, Israel J. Math. __72__ (1990) 1-2, 167&#8211;195 [MR92a:16047](http://www.ams.org/mathscinet-getitem?mr=1098988) [doi](http://doi.org/10.1007/BF02764619)

### Surveys

* [[Susan Montgomery]], _Hopf Galois theory: a survey_, Geometry and topology monographs 16 (2009) 367--400; [link](http://www.msp.warwick.ac.uk/gtm/2009/16/p012.xhtml), [doi](https://doi.org/10.2140/gtm.2009.16.367)

### Newer references

* [[Stefaan Caenepeel]], Septimiu Crivei, Andrei Marcus, [[Mitsuhiro Takeuchi]], _Morita equivalences induced by bimodules over Hopf-Galois extensions_, J. Algebra __314__ (2007) 267--302 [pdf](https://core.ac.uk/download/pdf/81180359.pdf)

* [[Peter Schauenburg]], _Hopf bimodules over Hopf-Galois extensions, Miyashita–Ulbrich actions, and monoidal center constructions_, Comm. Algebra 24 (1996) 143--163 [doi](https://doi.org/10.1080/00927879608825559)
* [[Peter Schauenburg]], _Hopf-Galois and bi-Galois extensions_, from: “Galois theory, Hopf
algebras, and semiabelian categories”, (G Janelidze, B Pareigis, W Tholen, editors), Fields Inst. Commun. 43, Amer. Math. Soc. (2004) 469--515 [MR2075600](http://www.ams.org/mathscinet-getitem?mr=2075600)
* Giovanni Landi, Chiara Pagani, _Push-forward of Hopf--Galois extensions: the non central case_, arXiv:[2512.20465](https://arxiv.org/abs/2512.20465)

### Categorifications and homotopifications

* [[Kathryn Hess]], _Homotopic Hopf-Galois extensions: foundations and examples_, Geometry & Topology Monographs 16 (2009) 79--132 [pdf](https://msp.org/gtm/2009/16/gtm-2009-16-005s.pdf) [arXiv:0902.3393](https://arxiv.org/abs/0902.3393)

Discussion for [[ring spectra]]:

* {#Rognes08} [[John Rognes]], _Galois extensions of structured ring spectra/Stably dualizable groups_, Memoirs of the American Mathematical Society, 192(898), 2008,  ([partial pdf](https://folk.uio.no/rognes/papers/galois.pdf), [doi:10.1090/memo/0898](https://doi.org/10.1090/memo/0898))

category: algebraic geometry
[[!redirects Hopf-Galois extensions]]
[[!redirects Hopf–Galois extension]]
[[!redirects Hopf–Galois extensions]]
[[!redirects Hopf--Galois extension]]
[[!redirects Hopf--Galois extensions]]
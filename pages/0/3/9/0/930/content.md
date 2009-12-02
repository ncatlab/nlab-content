##Definition##

Let $H$ be a $k$-[[bialgebra|bialgebra]] and $E$, say, a right $H$-comodule algebra (i.e. a [[monoid]] in the category of right $H$-[[comodule]]s) with coaction $\rho:E\to E\otimes H$.

The subalgebra $U = E^{\mathrm{co}H}$ of $H$-coinvariants in $E$ consists of all $u\in E$ such that $\rho(u)=u\otimes 1$.

The $k$-algebra extension $U\hookrightarrow E$ is __Hopf--Galois__ over $H$ if the natural map $E\otimes_U E\to E\otimes H$ given by the $k$-linear extension of the formula $e\otimes e'\mapsto (e\otimes_k 1)\rho(e')$ is a bijection (hence a $k$-module isomorphism). 


##Classical Galois extensions as a special case##

If $k\subset U=E^G$, $E$ is a [[field]], $G$ a finite group and $H = (k[G])^*$ is the dual [[Hopf algebra]] to the [[group algebra]] of $G$, then $E^G\hookrightarrow E$ is (classically) a [[Galois extension]] iff it is a $H$-Hopf--Galois extension, where the coaction of $H$ is induced by the action of $k[G]$, hence of $G$. One uses the Dedekind lemma on independence of automorphisms to prove this equivalence. It is possible however that $E^G\subset E$ is not (classically) Galois, but it is $K$-Hopf--Galois for some Hopf algebra $K\neq (k[G])^*$. 


##Role in geometry##

In [[algebraic geometry]], given an affine algebraic $k$-group [[scheme]] $G$, the algebra $E$ of regular functions over the total scheme $X$ of an affine $G$-[[torsor]] $X\to Y$, whose base $Y$ also happens to be affine, is a commutative $H$-Hopf--Galois extension of the algebra of regular functions $U$ on the base $Y\cong X/G$, where $H$ is the $k$-Hopf algebra of global regular functions on $G$. In algebraic topology, a generalization to [[spectrum|spectra]] (with the [[smash product]] of spectra in the role of tensor product) was studied by Rognes and others. In [[noncommutative geometry]], Hopf--Galois extensions are studied as noncommutative affine torsors, with interesting theorems involving [[descent]] theorems for [[Hopf module|Hopf modules]] generalizing [[Schneider's theorem]]. Given a right $H$-Hopf-Galois extension $U\hookrightarrow E$ and a left $H$-comodule $V$ the cotensor product $k$-module $E\Box^H V$ is interpreted as a space of sections of the associated [[fiber bundle]] with structure group $Spec H$ (in noncommutative sense) and fiber $V$. 

##Literature##

* Susan Montgomery, Hopf Galois theory: a survey, Geometry and topology monographs 16 (2009) 367&#8211;400 [link](http://www.msp.warwick.ac.uk/gtm/2009/16/p012.xhtml); [doi](http://dx.doi.org/10.2140/gtm.2009.16.367).

[[!redirects Hopf-Galois extensions]]
[[!redirects Hopf–Galois extension]]
[[!redirects Hopf–Galois extensions]]
[[!redirects Hopf--Galois extension]]
[[!redirects Hopf--Galois extensions]]
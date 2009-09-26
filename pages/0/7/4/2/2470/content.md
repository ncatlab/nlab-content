In [[noncommutative algebraic geometry]] one represents a scheme by an abelian category of quasicoherent sheaves on the scheme. This looses a bit of information but sometimes the information is sufficient. In _derived noncommutative (algebraic) geometry_ one instead considers the derived category of quasicoherent sheaves, or more precisely its [[enhanced triangulated category|dg-enhancement]] or A-infinity-enhancement; dg-enhancements for the derived categories of quasiprojective smooth varieties are essentially unique. 

In general one represents complex noncommutative spaces by pretriangulated dg-categories. This is well into homotopy theory area. Quillen [[model category]] structures and homotopy limits in this context were studied by a number of people (including impressive thesis by Tabuada). On the other hand, over a mixed characteristics, the meaning of such representations is less well understood.

The derived noncommutative geometry has been introduced by Kapranov-Bondal and later Orlov around 1990; contemporary main works belong also to [[Kontsevich]], Lunts, van den Bergh, Katzarkov, Kuznetsov and Kaledin. Some of the works of Toen, Vaquie, Keller  are properly in this area as well. 

* L. Katzarkov, M. Kontsevich, T. Pantev, _Hodge theoretic aspects of mirror symmetry), [arxiv:0806.0107](http://arxiv.org/abs/math/0806.0107).

formulate the following

__Definition__ A __graded complex nc-space__ is a $\mathbb{C}$-linear differential graded category $C$ which is homotopy complete and cocomplete. 

The derived categories of qcoh sheaves on a scheme over $Spec(\mathbb{C})$ is one of the examples; another example is the category of dg-modules over a fixed dg-algebra $A$, which are such that $A$ admits an exhaustive filtration
such that the associated graded is a sum of shifts of $A$.
Call that category $A$-$Mod$. 

Kontsevich calls a complex differential $\mathbb{Z}/2$-graded algebra 

* __smooth__ if $A$ is a perfect object in the category of $A$-$A$-dg-bimodules (perfect object here means that $Hom(A,-)$ preserves small homotopy colimits); 

* __compact__ if the total complex dimension of its cohomology $H^\bullet(A,d_A)$ is finite

The category $A$-$Mod$ is a smooth (resp. compact) nc space if the underlying dg-algebras $A$ is; this notion depends on the category and not on the underlying dg-algebra. 

The above definition implies that a category $C$ which represents a nc-space in the sense above is triangulated and Karoubi closed. Sometimes this are requirements in another variant of the definition.

* (M. Kontsevich) A __noncommutative space__ $X$ is a small triangulated category $C_X$ which is Karoubi closed (=every projector splits) and appropriately enriched over either

  * by spectra $Hom_{C_X}(E,F[i])=\pi_{-i}\mathbf{Hom}_{C_X}(E,F)$

  * by complexes of $k$-vector spaces: $Hom(E,F[i])= H^i(\mathbf{Hom}_{C_X}(E,F))$. $C_X$ is $k$-linear over a field $k$ and one writes $X/k$. If instead $k$ is replaced by a ring $R$ then one enriches over complexes of $R$-modules which are cofibrant. 



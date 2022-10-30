
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[noncommutative algebraic geometry]] one represents a [[scheme]] by an [[abelian category]] of [[quasicoherent sheaf|quasicoherent sheaves]] on the [[scheme]]. 

In _derived (higher) noncommutative (algebraic) geometry_ one instead considers the [[derived category]] of [[quasicoherent sheaf|quasicoherent sheaves]], or more precisely its [[enhanced triangulated category|dg-enhancement]] or [[A-infinity-category|A-infinity-enhancement]]; dg-enhancements for the derived categories of quasiprojective smooth varieties are essentially unique. Taking the derived category instead of the abelian loses a bit of information but sometimes the information is sufficient.

In general one represents complex noncommutative spaces by [[pretriangulated dg-category|pretriangulated dg-categories]]. This is well into [[homotopy theory]] area. Quillen [[model category]] structures and [[homotopy limit]]s in this context were studied by a number of people (including the impressive thesis by Tabuada). On the other hand, over a mixed characteristics, the meaning of such representations is less well understood.

Derived noncommutative geometry has been introduced by Kapranov-Bondal and later Orlov around 1990; contemporary main works belong also to [[Kontsevich]], [[Valery Lunts|Lunts]], van den Bergh, Katzarkov, Kuznetsov and Kaledin. Some of the works of [[Bertrand Toen|Toen]], Vaquie, Keller  are properly in this area as well. 

## Definitions

In 

* L. Katzarkov, M. Kontsevich, T. Pantev, _Hodge theoretic aspects of mirror symmetry_, [arxiv:0806.0107](http://arxiv.org/abs/math/0806.0107).

the following definition is given.

+-- {: .un_definition}
###### Definition (graded complex noncommutative space)

A __graded complex nc-space__ is a $\mathbb{C}$-linear [[dg-category|differential graded category]] $C$ which is homotopy complete and cocomplete (has all [[homotopy limit]]s and colimits). 

=--

The [[derived category|derived categories]] of [[quasicoherent sheaf|quasicoherent sheaves]] on a [[scheme]] over $Spec(\mathbb{C})$ is one of the examples; another example is the category of dg-modules over a fixed [[dg-algebra]] $A$, which are such that $A$ admits an exhaustive filtration
such that the associated graded is a sum of shifts of $A$.
Call that category $A$-$Mod$. 

Kontsevich calls a complex differential $\mathbb{Z}/2$-graded algebra 

* __smooth__ if $A$ is a perfect object in the category of $A$-$A$-dg-bimodules (perfect object here means that $Hom(A,-)$ preserves small homotopy colimits); 

* __compact__ if the total complex dimension of its cohomology $H^\bullet(A,d_A)$ is finite

The category $A$-$Mod$ is a smooth (resp. compact) nc space if the underlying dg-algebras $A$ is; this notion depends on the category and not on the underlying dg-algebra. 

The above definition implies that a category $C$ which represents a nc-space in the sense above is [[triangulated category|triangulated]] and [[Karoubi envelope|Karoubi closed]]. Sometimes this are requirements in another variant of the definition.

+-- {: .un_definition}
###### Definition (noncommutative space (M. Kontsevich))

A __noncommutative space__ $X$ is a small [[triangulated category]] $C_X$ which is [[Karoubi envelope|Karoubi closed]] (=every [[idempotent]] is a [[split idempotent]]) and appropriately [[enriched category|enriched]] over either

* [[spectrum|spectra]] $Hom_{C_X}(E,F[i])=\pi_{-i}\mathbf{Hom}_{C_X}(E,F)$

* [[chain complex|complexes]] of $k$-vector spaces (i.e. is a [[dg-category]]): $Hom(E,F[i])= H^i(\mathbf{Hom}_{C_X}(E,F))$. $C_X$ is $k$-linear over a field $k$ and one writes $X/k$. If instead $k$ is replaced by a ring $R$ then one enriches over complexes of $R$-modules which are [[model structure on chain complexes|cofibrant]]. 

=--

## Some history 

In the early works of the Moscow school ([[Kapranov]], [[Alexei Bondal|Bondal]], [[Dmitri Orlov|Orlov]], [[Kontsevich]]) one replaces a [[variety]] by the [[derived category]] of [[coherent sheaves]] (or [[quasicoherent sheaves]] on that variety, or [[dg-category]] (or [[A-infinity category]]) [[enhanced triangulated category|enhancements]] thereof. There are also noncommutative deformations of such derived categories and analogues like the categories corresponding to the so-called [[Landau-Ginzburg model]]s. Therefore [[noncommutative derived algebraic geometry]] (and even noncommutative motives). 

Notice that the [[derived category]] of coherent sheaves on a variety does _not_ remember all the structure of the original variety hence derived geometry loses often some information (sometimes not); thus derived algebraic geometry is sometimes easier than nonderived. 

## References

* L.Katzarkov, M.Kontsevich, T.Pantev, _Hodge theoretic aspects of mirror symmetry_, [arxiv:0806.0107](http://arxiv.org/abs/0806.0107)
{#KatzarkovKontsevichPantev}

and a bit earlier treatise on formal (infinitesimal in the sense of [[formal schemes]]) aspect as used in the [[deformation theory]] is in

* M. Kontsevich, Y. Soibelman, _Notes on A-infinity algebras, A-infinity categories and non-commutative geometry. I_, [math.AG/0606241](http://arxiv.org/abs/math/0606241)
 {#KontsevichSoibelman}

* [[Dmitry Kaledin]], _Homological methods in non-commutative geometry_  (2008) ([pdf](http://imperium.lenin.ru/~kaledin/math/tokyo/final.pdf))

The relations to tropical and symplectic geometry are in recent Kontsevich's talk at 2009 Arbeitstagung:

* M. Kontsevich, Mathematische Arbeitstagung 2009, _Symplectic geometry of homological algebra_, preprint MPIM2009-40a, [pdf](http://www.mpim-bonn.mpg.de/preprints/send?bid=4024)

Homological mirror symmetry is one of the main motivations and statements of the derived noncommutative algebraic geometry 

* Maxim Kontsevich, _Homological algebra of mirror symmetry_,   Proceedings of the International Congress of Mathematicians, Vol. 1, 2 (Z&#252;rich, 1994),  120--139, Birkh&#228;user, Basel, 1995.

* Maxim Kontsevich, Yan Soibelman, _Homological mirror symmetry and torus fibrations_, in Symplectic geometry and mirror symmetry (Seoul, 2000),  203--263, World Sci. Publ., River Edge, NJ, 2001. 


[[!redirects derived noncommutative algebraic geometry]] 
[[!redirects noncommutative derived algebraic geometry]]

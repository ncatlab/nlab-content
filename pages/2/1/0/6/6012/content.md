
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

A __torsion theory__ in an [[abelian category]] $A$ is a [[pair]] $(T,F)$ of [[additive category|additive]] [[subcategories]], called the __torsion class__ $T$ and the __torsion free class__ $F$, such that the following conditions hold:

* $Hom(T,F) = 0$

(in other words, $A(X,Y) = 0$ if $X \in Ob T$ and $Y\in Ob F$).

* $Hom(T,Y) = 0 \Rightarrow Y\in Ob F$

* $Hom(X,F) = 0 \Rightarrow X\in Ob T$

* for all $X\in Ob A$, there exists $Y\subset X$, $Y\in Ob T$ and $X/Y\in Ob F$

Equivalently, a torsion theory in $A$ is a pair $(T,F)$ of [[strictly full subcategories]] of $A$ such that the first and last conditions in the above list hold. Alternatively, we can require the last condition
and the following 3: $T\cap F=\{0\}$, $T$ is closed under quotients
and $F$ under subobjects.  It follows also that $T$ and $F$ are stable under extensions. 

### Torsion part of an object

If the [[abelian category]] $A$ satisfies [[Pierre Gabriel|Gabriel]]'s [[property (sup)]] then for every [[object]] $X$ there exists the largest [[subobject]] $t(X)\subset X$ which is in $T$, which is called the _torsion part_ of $X$ (sometimes written as $X_T$). Under the [[axiom of choice]], $t: X\to t(X)$ can be extended to a functor. 

### Hereditary torsion theories

A torsion theory is called __hereditary__ if $T$ is closed under [[subobjects]], or equivalently, $t$ is [[left exact functor]]. 
For some authors (e.g. Golan) torsion theory is assumed to
be hereditary. 

## Properties

If $(T,F)$ is a torsion class then $T$ and $F$ both contain the [[zero object]] and are closed under [[biproducts]] ([Borceux II 1.12.3](ncatlab.org/nlab/show/Handbook+of+Categorical+Algebra)). Presentation of an object $X$ in $Ob A$ as an [[extension]] $0\to Y\to X\to X/Y\to 0$,  $Y$ in $Ob T$ by $X/Y$ in $Ob F$ is unique up to an [[isomorphism]] of [[short exact sequences]] ([Borceux II 1.12.4](ncatlab.org/nlab/show/Handbook+of+Categorical+Algebra)). 

Given an [[abelian category]] $A$ there is a [[bijection]] between universal [[closure operator|closure operations]] on $A$, hereditary torsion theories in $A$ ([Borceux II 1.12.8](ncatlab.org/nlab/show/Handbook+of+Categorical+Algebra)) and, if $A$ is a [[locally finitely presentable category]] also with [[left exact functor|left exact]] [[localizations]] of $A$ admitting a [[right adjoint]] and with [[localizing subcategories]] of $A$ ([Borceux II 1.13.15](ncatlab.org/nlab/show/Handbook+of+Categorical+Algebra)). 

## Examples

The basic example of a torsion class is the class of [[torsion subgroup|torsion]] [[abelian groups]] within the [[category]] $A =$ [[Ab]] of all [[abelian groups]]. The torsion theories are often used as a means to formulate [[localization]] theory in [[abelian categories]]. 


## Literature

The notion originates with:

* {#Dickson63} [[Spencer Ernst Dickson]], _Torsion theories for abelian categories_, Thesis, New Mexico State University (1963) ([ProQuest](https://www.proquest.com/openview/0c7793e99ae9368bd940699a03d70132/1))
 
* {#Dickson66} [[Spencer Ernst Dickson]], *A Torsion Theory for Abelian Categories*, Transactions of the American Mathematical Society **121** 1 (1966) 223-235 ([doi:10.2307/1994341](https://doi.org/10.2307/1994341), [jstor:1994341](https://www.jstor.org/stable/1994341))


Comprehensive accounts:

* [[Francis Borceux]], _[[Handbook of Categorical Algebra]]_, vol. 2

* N. Popescu, _Abelian categories with applications to rings and modules_, London Math. Soc. Monographs 3, Academic Press 1973. xii+467 pp. [MR0340375](http://www.ams.org/mathscinet-getitem?mr=0340375)

* [[Joachim Lambek]], _Torsion theories, additive semantics, and rings of quotients_, with app. by H. H. Storrer on torsion theories and dominant dimensions. Lecture Notes in Mathematics __177__, Springer-Verlag 1971, vi+94 pp. [MR284459](http://www.ams.org/mathscinet-getitem?mr=284459)
 

For a unified treatment in abelian and in [[triangulated categories]] see

* Apostolos Beligiannis, Idun Reiten, _Homological and homotopical aspects of torsion theories_,  Mem. Amer. Math. Soc. 188 (2007), no. 883, viii+207 pp. [pdf](http://www.math.uoi.gr/~abeligia/torsion.pdf)

As explained there, in triangulated context, torsion pairs are in 1-1 correspondence with [[t-structures]]. One could
also study a relation between torsion theories on an abelian
category with tilting theory and $t$-structures on the derived category:

* Dieter Happel, Idun Reiten, Sverre O. Smal&#248;, _Tilting in abelian categories and quasitilted algebras_, Mem. Amer. Math. Soc. 120 (1996), no. 575, viii+ 88

* Riccardo Colpi, Luisa Fiorot, Francesco Mattiello, _On tilted Giraud subcategories_, [arxiv/1307.1987](http://arxiv.org/abs/1307.1987) 

Other references in abelian context include

* Lia Va&#353;, _Differentiability of torsion theories_, ([pdf](http://www.usciences.edu/~lvas/homepage_sa_umdja/difftt_single.pdf))

For analogues in nonadditive contexts see

* [[Michael Barr]], _Non-abelian torsion theories_, Canad. J. Math. 25 (1973) 1224--1237

* Basil A. Rattray, _Torsion theories in non-additive categories_, Manuscripta Math. __12__ (1974), 285&#8211;305 [MR340360](http://www.ams.org/mathscinet-getitem?mr=340360) [doi](http://dx.doi.org/10.1007/BF01155518)

* [[Jiří Rosický ]], [[Walter Tholen]], _Factorization, fibration and torsion_, [arxiv/0801.0063](http://arxiv.org/abs/0801.0063), Journal of homotopy and Related Structures

* M. M. Clementino, D. Dikranjan, [[Walter Tholen]], _Torsion theories and radicals in normal categories_, J. of Algebra __305__ (2006) 92-129 

* [[Dominique Bourn]], [[Marino Gran]], _Torsion theories in homological categories_, J. of Algebra __305__ (2006) 18&#8211;47 [MR2007k:18018](http://www.ams.org/mathscinet-getitem?mr=2262518) [doi](http://dx.doi.org/10.1016/j.jalgebra.2006.07.011)

[[!redirects torsion theories]]

# Yetter--Drinfeld modules
* table of contents
{: toc}

## Definition

A __Yetter--Drinfeld module__ over a $k$-[[bialgebra]] $B=(B,\Delta,\epsilon)$, (with [[Sweedler notation]] $\Delta(b) = \sum b_{(1)}\otimes b_{(2)}$), is a $k$-module which is simultaneously a $B$-module and a $B$-[[comodule]] with certain compatibility between the $B$-action and $B$-coaction. 

+-- {: .un_defn}
###### Compatibility for left-right YD Modules

The compatibility for a left $B$-module $B\otimes M\to M$, $b\otimes m\mapsto b\blacktriangleright m$, which is a right $B$-comodule 
with respect to the coaction $\rho:M\to M\otimes B$, $\rho(m) = \sum m_{[0]}\otimes m_{[1]}$,
is the following
$$
\sum (b_{(1)}\blacktriangleright m_{[0]})\otimes b_{(2)} m_{[1]}
= \sum (b_{(2)}\blacktriangleright m)_{[0]}
\otimes (b_{(2)}\blacktriangleright m)_{[1]} b_{(1)}
$$
or equivalently, if $B$ is a Hopf algebra with invertible antipode $S$ (or instead just with the
[[skew-antipode]] denoted $S^{-1}$)
$$
\sum (b_{(2)}\blacktriangleright m_{[0]})\otimes b_{(3)} m_{[1]} S^{-1}(b_{(1)})
= \sum (b\blacktriangleright m)_{[0]}
\otimes (b\blacktriangleright m)_{[1]}
$$
=--

+-- {: .un_defn}
###### Compatibility for left-left YD Modules

$$
b_{(1)} m_{[-1]}\otimes (b_{(2)}\blacktriangleright m_{[0]})
=
(b_{(1)}\blacktriangleright m)_{[-1]} b_{(2)}  \otimes 
(b_{(1)}\blacktriangleright m)_{[0]}
$$
=--

+-- {: .un_defn}
###### Compatibility for right-left YD Modules


$$
m_{[-1]}b_{(1)}\otimes (m_{[0]}\blacktriangleleft b_{(2)})
=
b_{(2)} (m\blacktriangleleft b_{(1)})_{[-1]}  \otimes (m\blacktriangleleft b_{(1)})_{[0]}
$$
=--

+-- {: .un_defn}
###### Compatibility for right-right YD Modules
$$
m_{[0]}\blacktriangleleft b_{(1)}\otimes m_{[1]} b_{(2)}
=
(m\blacktriangleleft b_{(2)})_{[0]}\otimes 
b_{(1)} (m\blacktriangleleft b_{(2)})_{[1]} 
$$
=--


## The category of Yetter--Drinfeld modules

The _category of left-right YD modules_, i.e. Yetter--Drinfeld modules which are left $B$-modules and
right $B$-comodules, is denoted by ${}_B \mathcal{Y D}^B$; the category is rarely alternatively called the (left-right) Yetter--Drinfeld category
and it can be presented as the category of entwined modules for certain  special entwining structure. 

${}_B \mathcal{Y D}^B$ is a monoidal category equipped 
with "pre-braiding" morphisms, which make it into a 
[[braided monoidal category]] iff $B$ is a Hopf
algebra with a bijective antipode. If $A$ is a commutative algebra in
${}_B\mathcal{Y D}^B$ then the [[smash product algebra]] $A\sharp B$
is an associative [[bialgebroid]], said to be the extension of scalars
from the bialgebra $B$ along $k\hookrightarrow A$. If $B=H$ 
is a Hopf algebra with bijective antipode then this bialgebroid is in fact 
a [[Hopf algebroid]], both in the sense of Lu and in the sense of Bohm.

If $B=H$ is a finite-dimensional [[Hopf algebra]], then the category
${}_H \mathcal{Y D}^H$ is equivalent to the category of ${}_{D(H)}\mathcal{M}$ of left $D(H)$-modules, where $D(H)$ is the [[Drinfeld double]] of $H$, which in turn is equivalent to the center
of the monoidal category ${}_H\mathcal{H}$ of left $H$-modules. 

The commutative algebras in the center of a monoidal category, play
role in the [[dynamical extension of a monoidal category]]. Hence the commutative algebras in ${}_H\mathcal{Y D}^H$ provide such examples. An important example, is the dual $H^*$ when $H$ is finite-dimensional. 
The smash product algebra is in that case the [[Heisenberg double]], hence 
it inherits a Hopf algebroid structure. 


## Anti Yetter--Drinfeld modules

The most general coefficients for Hopf cyclic cohomology is called stable-anti-Yetter--Drinfled modules. These kind of modules appeared for the first time  in  different name  in B. Rangipour's PhD thesis under supervision of M. Khalkhali. Later on it was generalized by 
P.M. Hajac, M. Khalkhali, B. Rangipour, and Y. Sommerhaeuser. The category of AYD modules is not monodical but product of an AYD module   with a YD module results in an AYD module.  By the work of Rangipour--Sutlu one knows that there is such category over Lie algebras and there is a one-to-one correspondence between AYD modules over a Lie algebra and those over the universal enveloping algebra of the Lie algebra. This correspondence is extended by the same authors for bicrossed product Hopf algebras. 
The true  meaning of the AYD modules in non commutative geometry is not known yet. There are some  attempts by   A. Kaygun--M. Khalkhali to relate them to the curvature of flat  connections similar to the work of T. Brzezi&#324;ski on YD modules, however their identification   are not restricted to AYD and  works for a wide variety of YD type modules. 


## Literature

* Susan Montgomery, _Hopf algebras and their actions on rings_, 
CBMS Lecture Notes __82__, AMS 1993, 240p.

* A.M. Semikhatov, _Yetter--Drinfeld structures on Heisenberg doubles and chains_, [arXiv:0908.3105](http://arxiv.org/abs/0908.3105)

* wikipedia [Yetter--Drinfeld category](http://en.wikipedia.org/wiki/Yetter%E2%80%93Drinfeld_category)

* Peter Schauenburg, _Hopf Modules and Yetter--Drinfel&#8242;d Modules_,
Journal of Algebra __169__:3 (1994) 874--890 [doi](http://dx.doi.org/10.1006/jabr.1994.1314); _Hopf modules and the double of a quasi-Hopf algebra_, Trans. Amer. Math. Soc. 354 (2002), 3349--3378 [doi](http://dx.doi.org/10.1090/S0002-9947-02-02980-X) [pdf](http://www.ams.org/journals/tran/2002-354-08/S0002-9947-02-02980-X/S0002-9947-02-02980-X.pdf); _Actions of monoidal categories, and generalized Hopf smash products_, Journal of Algebra __270__ (2003) 521--563, [doi](http://dx.doi.org/10.1016/S0021-8693%2803%2900403-4) [ps](http://www.mathematik.uni-muenchen.de/%7Eschauen/papers/amcghsp.ps)

* V. G. Drinfel'd, _Quantum groups_, Proceedings of the International Congress of Mathematicians 1986, Vol. 1, 798--820, AMS 1987, [djvu:1.3M](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0798.0820.ocr.djvu), [pdf:2.5M](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0798.0820.ocr.pdf)

* David N. Yetter, _Quantum groups and representations of monoidal categories_, 
Math. Proc. Cambridge Philos. Soc. 108 (1990), no. 2, 261--290 [MR91k:16028](http://www.ams.org/mathscinet-getitem?mr=1074714) [doi](http://dx.doi.org/10.1017/S0305004100069139)

* [[Gabriella Bohm|Gabriella B&#246;hm]], Dragos Stefan, _(Co)cyclic (co)homology of bialgebroids: An approach via (co)monads_, Comm. Math. Phys. 282 (2008), no.1, 239--286, [arxiv/0705.3190](http://arxiv.org/abs/0705.3190); _A categorical approach to cyclic duality_, J. Noncommutative Geometry __6__ (2012), no. 3, 481--538, [arxiv/0910.4622](http://arxiv.org/abs/0910.4622) 

* Atabey Kaygun, Masoud Khalkhali, _Hopf modules and noncommutative differential geometry_, Lett. in Math. Physics __76:1__, pp 77--91 (2006) [arxiv/math.QA/0512031](http://arxiv.org/abs/math/0512031), [doi](http://dx.doi.org/10.1007/s11005-006-0062-x)

* [[T. Brzeziński]], _Flat connections and (co)modules_, [in:] New Techniques in Hopf Algebras and Graded Ring Theory, S Caenepeel and F Van Oystaeyen (eds), Universa Press, Wetteren, 2007 pp. 35--52   [arxiv:math.QA/0608170](http://arxiv.org/abs/math.QA/0608170)

* P.M. Hajac, M. Khalkhali, B. Rangipour, Y. Sommerhaeuser, _Hopf-cyclic homology and cohomology with coefficients_, C. R. Math. Acad. Sci. Paris __338__(9), 667--672 (2004) [math.KT/0306288](http://arxiv.org/abs/math/0306288); _Stable anti-Yetter--Drinfeld modules_. C. R. Math Acad. Sci. Paris __338__(8), 587--590 (2004)

* B. Rangipour, Serkan S&#252;tl&#252;, _Characteristic classes of foliations via SAYD-twisted cocycles_, [arxiv/1210.5969](http://arxiv.org/abs/1210.5969);
_SAYD modules over Lie--Hopf algebras_, [http://arxiv.org/abs/1108.6101](http://arxiv.org/abs/1108.6101); _Cyclic cohomology of Lie algebras_, [arxiv/1108.2806](http://arxiv.org/abs/1108.2806)

* Florin Panaite, Mihai D. Staic, _Generalized (anti) Yetter--Drinfeld modules as components of a braided T-category_, [math.QA/0503413](http://arxiv.org/abs/math/0503413) 

* D. Bulacu, S. Caenepeel, F. Panaite, _Doi--Hopf modules and Yetter--Drinfeld categories for quasi-Hopf algebras_, Communications in Algebra, 34 (9), 3413--3449 (2006) [math.QA/0311379](http://arxiv.org/abs/math/0311379)

* Florin Panaite, Dragos Stefan, _Deformation cohomology for Yetter--Drinfel'd modules and Hopf (bi)modules_, [math.QA/0006048](http://arxiv.org/abs/math/0006048)

* Nicol&#225;s Andruskiewitsch, Istv&#225;n Heckenberger, Hans-J&#252;rgen Schneider, _The Nichols algebra of a semisimple Yetter--Drinfeld module_,  American J. of Math. __132__:6, (2010) 1493--1547 [doi](http://dx.doi.org/10.1353/ajm.2010.0019)

* M. Cohen, D. Fischman, S. Montgomery, _On Yetter&#8211;Drinfeld categories and $H$-commutativity_, Commun. Algebra __27__ (1999) 1321--1345

* Yukio Doi, _Hopf modules in Yetter--Drinfeld categories_, Commun. Alg. __26__:9, 3057--3070 (1998) [doi](http://dx.doi.org/10.1080/00927879808826327)

* I. Heckenberger, H.-J. Schneider, _Yetter--Drinfeld modules over bosonizations of dually paired Hopf algebras_, [arxiv/1111.4673](http://arxiv.org/abs/1111.4673)

* V. Ulm, _Actions of Hopf algebras in categories of Yetter--Drinfeld modules_, Comm. Alg. __31__:6, 2719--2743

* D.E. Radford, J. Towber, _Yetter--Drinfel'd categories associated to an arbitrary bialgebra_, J. Pure Appl. Algebra __87__ (1993), 259--279 [MR94f:16060](http://www.ams.org/mathscinet-getitem?mr=1228157) [doi](http://dx.doi.org/10.1016/0022-4049%2893%2990114-9)

* Georgia Benkart, Mariana Pereira, Sarah Witherspoon, _Yetter--Drinfeld modules under cocycle twists_, [arxiv/0908.1563](http://arxiv.org/abs/0908.1563)

* [[Shahn Majid]], Robert Oeckl, _Twisting of quantum differentials and
the Planck scale Hopf algebra_, Commun. Math. Phys. __205__, 617--655 (1999)


[[!redirects Yetter-Drinfeld module]]
[[!redirects Yetter-Drinfeld modules]]
[[!redirects Yetter–Drinfeld module]]
[[!redirects Yetter–Drinfeld modules]]
[[!redirects Yetter--Drinfeld module]]
[[!redirects Yetter--Drinfeld modules]]

[[!redirects Yetter-Drinfeld category]]
[[!redirects Yetter-Drinfeld categories]]
[[!redirects Yetter–Drinfeld category]]
[[!redirects Yetter–Drinfeld categories]]
[[!redirects Yetter--Drinfeld category]]
[[!redirects Yetter--Drinfeld categories]]


# Yetter--Drinfeld modules
* table of contents
{: toc}

## Definition

A __Yetter--Drinfeld module__ over a $k$-[[bialgebra]] $B=(B,\Delta,\epsilon)$, (with [[Sweedler notation]] $\Delta(b) = \sum b_{(1)}\otimes b_{(2)}$), is a $k$-module which is simultaneously a $B$-module and a $B$-[[comodule]] with certain compatibility -- also called Yetter-Drinfeld condition -- between the $B$-action and $B$-coaction. 

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

Morphisms of YD $B$-modules are morphisms of underlying $B$-modules which are also the morphisms of underlying
$B$-comodules.
The _category of left-right YD modules_ over a bialgebra $B$ is denoted by ${}_B \mathcal{Y D}^B$; the category is rarely alternatively called the (left-right) Yetter--Drinfeld category
and it can be presented as the category of entwined modules for certain  special entwining structure. 

${}_B \mathcal{Y D}^B$ is a monoidal category: if $V$ and $W$ are left-right YD modules, $V\otimes W$ is the tensor product of underlying vector spaces equipped with left $B$-action
$$
b\blacktriangleright (v\otimes w) = (b_{(1)}\blacktriangleright v)\otimes (b_{(2)}\blacktriangleright w)
$$
and right $B$-coaction
$$
v\otimes w\mapsto v_{[0]}\otimes w_{[0]}\otimes w_{[1]}v_{[1]}
$$
Note the order within the rightmost tensor factor! One checks directly that this tensor product indeed satisfies the Yetter-Drinfeld condition.
Radford and Towber prefer slightly different monoidal structure: in above formulas use the opposite product and coopposite coproduct on $B$. (They mention, however, both structures.)

Monoidal category ${}_B \mathcal{Y D}^B$ is equipped 
with "pre-braiding" morphisms
$$ 
R_{V,W}: V\otimes W\to W\otimes V,\,\,\,\,\,\,\,\,
v\otimes w\mapsto w_{[0]} \otimes (w_{[1]}\blacktriangleright v).
$$
In Radford-Towber convention the pre-braiding is $v\otimes w\mapsto (v_{[1]}\blacktriangleright w)\otimes v_{[0]}$.
Prebraidings satisfy all conditions for a [[braided monoidal category|braiding]] except for invertibility
of $R_{V,W}$
which is fullfilled for all $V,W$ iff $B$ is a Hopf algebra. $R_{V,W}$ is always fullfilled if both $V$ and $W$ are finite dimensional. In particular, $R_{V,V}$ satisfies the Yang-Baxter equation.
If $A$ is a commutative algebra in
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

If $F$ is a counital 2-cocycle for a bialgebra $H$, the Drinfeld twist $H^F$ of $F$ is also a bialgebra and there is a monoidal equivalence ${}_H\mathcal{M}\cong {}_{H^F}\mathcal{M}$. In Section 2 of [Škoda-Stojić2023](#Škoda-Stojić2023) it is shown how this monoidal equivalence lifts to a braided monoidal equivalence between the categories of Yetter-Drinfeld modules
${}_H\mathcal{M}^H\cong {}_{H^F}\mathcal{M}^{H^F}$.

* [[Zoran Škoda]], Martina Stojić, _Comment on "Twisted bialgebroids versus bialgebroids from Drinfeld twist"_, [arXiv:2308.05083](https://arxiv.org/abs/2308.05083)

## Yetter-Drinfeld module algebras

A __left-right Yetter-Drinfeld module algebra__ is a monoid $(A,\mu)$ in ${}_B\mathcal{Y D}^B$. Let its multiplication map be denoted $\mu:a\otimes c\mapsto a\cdot c$. Let us unwind the requirements that $\mu:A\otimes A\to A$ is a morphism in ${}_B\mathcal{Y D}^B$.

Requirement that $\mu$ is a map of $B$-modules is, for $a,c\in A$
$$
b\blacktriangleright (a\cdot c) = (b_{(1)}\blacktriangleright a)\cdot (b_{(2)}\blacktriangleright c),
$$
which, together with compatibility of unit $b\blacktriangleright 1 = \epsilon(b) 1$, means that the action is Hopf ($A$ is a left $B$-module algebra).
Requirement that $\mu$ is a map of $B$-comodules is
$$\rho\circ\mu = (\mu\otimes id)\rho_{A\otimes A}$$
$$
\rho(a\cdot c)
= (\mu\otimes id)(a_{[0]}\otimes c_{[0]}\otimes c_{[1]} a_{[1]})
= a_{[0]}\cdot c_{[0]}\otimes c_{[1]} a_{[1]},
$$
that is (along with the counit condition), $A$ is right $B^\op$-comodule algebra.
A left-right Yetter-Drinfeld module algebra $A$ is __braided-commutative__ if
$$
\mu\circ R_{A,A} = \mu.
$$
In explicit terms, for all $a,c\in A$,
$$
c_{[0]}\cdot (c_{[1]}\blacktriangleright a) = a\cdot c.
$$

## Anti Yetter--Drinfeld modules

The most general coefficients for Hopf cyclic cohomology are called stable anti-Yetter-Drinfeld modules; the definition of [[anti-Yetter-Drinfeld module]]s is very similar.  

## Nichols algebras

To every YD module one assigns a [[Nichols algebra]], see there.

## Literature

### YD modules over Hopf/bi-algebras

* Susan Montgomery, _Hopf algebras and their actions on rings_, CBMS Lecture Notes __82__, AMS 1993, 240p.

* A.M. Semikhatov, _Yetter--Drinfeld structures on Heisenberg doubles and chains_, [arXiv:0908.3105](https://arxiv.org/abs/0908.3105)

* wikipedia [Yetter--Drinfeld category](http://en.wikipedia.org/wiki/Yetter%E2%80%93Drinfeld_category)

* Peter Schauenburg, _Hopf Modules and Yetter--Drinfel&#8242;d Modules_,
Journal of Algebra __169__:3 (1994) 874--890 [doi](https://doi.org/10.1006/jabr.1994.1314); _Hopf modules and the double of a quasi-Hopf algebra_, Trans. Amer. Math. Soc. 354 (2002), 3349--3378 [doi](https://doi.org/10.1090/S0002-9947-02-02980-X) [pdf](http://www.ams.org/journals/tran/2002-354-08/S0002-9947-02-02980-X/S0002-9947-02-02980-X.pdf); _Actions of monoidal categories, and generalized Hopf smash products_, Journal of Algebra __270__ (2003) 521--563, [doi](http://dx.doi.org/10.1016/S0021-8693%2803%2900403-4) [ps](http://www.mathematik.uni-muenchen.de/%7Eschauen/papers/amcghsp.ps)

* V. G. Drinfel'd, _Quantum groups_, Proceedings of the International Congress of Mathematicians 1986, Vol. 1, 798--820, AMS 1987, [djvu:1.3M](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0798.0820.ocr.djvu), [pdf:2.5M](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0798.0820.ocr.pdf)

* David N. Yetter, _Quantum groups and representations of monoidal categories_, Math. Proc. Cambridge Philos. Soc. 108 (1990), no. 2, 261--290 [MR91k:16028](https://www.ams.org/mathscinet-getitem?mr=1074714) [doi](http://dx.doi.org/10.1017/S0305004100069139)

* [[T. Brzeziński]], _Flat connections and (co)modules_, [in:] New Techniques in Hopf Algebras and Graded Ring Theory, S Caenepeel and F Van Oystaeyen (eds), Universa Press, Wetteren, 2007 pp. 35--52   [arXiv:math.QA/0608170](https://arxiv.org/abs/math.QA/0608170)


* Florin Panaite, Mihai D. Staic, _Generalized (anti) Yetter--Drinfeld modules as components of a braided T-category_, arXiv:[math.QA/0503413](https://arxiv.org/abs/math/0503413) 

* D. Bulacu, S. Caenepeel, F. Panaite, _Doi--Hopf modules and Yetter--Drinfeld categories for quasi-Hopf algebras_, Communications in Algebra, 34 (9), 3413--3449 (2006) [math.QA/0311379](https://arxiv.org/abs/math/0311379)

* Florin Panaite, Dragos Stefan, _Deformation cohomology for Yetter--Drinfel'd modules and Hopf (bi)modules_, [math.QA/0006048](https://arxiv.org/abs/math/0006048)

* M. Cohen, D. Fischman, [[Susan Montgomery|S. Montgomery]], _On Yetter--Drinfeld categories and $H$-commutativity_, Commun. Algebra __27__ (1999) 1321--1345

* [[Yukio Doi]], _Hopf modules in Yetter--Drinfeld categories_, Commun. Alg. __26__:9, 3057--3070 (1998) [doi](https://doi.org/10.1080/00927879808826327)

* I. Heckenberger, H.-J. Schneider, _Yetter--Drinfeld modules over bosonizations of dually paired Hopf algebras_, [arXiv:1111.4673](https://arxiv.org/abs/1111.4673)

* V. Ulm, _Actions of Hopf algebras in categories of Yetter--Drinfeld modules_, Comm. Alg. __31__:6, 2719--2743

* L. A. Lambe, D. E. Radford, _Algebraic aspects of the quantum Yang–Baxter equation_, J. Algebra 154 (1992) 228--288 [doi](https://doi.org/10.1006/jabr.1993.1014)

* D.E. Radford, [[Jacob Towber]], _Yetter--Drinfel'd categories associated to an arbitrary bialgebra_, J. Pure Appl. Algebra __87__ (1993), 259--279 [MR94f:16060](http://www.ams.org/mathscinet-getitem?mr=1228157) [doi](https://doi.org/10.1016/0022-4049%2893%2990114-9)

* [[Georgia Benkart]], Mariana Pereira, Sarah Witherspoon, _Yetter--Drinfeld modules under cocycle twists_, J. Algebra 324:11 (2010) 2990--3006 [arxiv:0908.1563](https://arxiv.org/abs/0908.1563)

* [[Shahn Majid]], Robert Oeckl, _Twisting of quantum differentials and the Planck scale Hopf algebra_, Commun. Math. Phys. __205__, 617--655 (1999)

* Huixiang Chen, Yinhuo Zhang, _Cocycle deformations and Brauer groups_, Comm. Alg. 35:2 (2007) 399--433 [doi](https://doi.org/10.1080/00927870601052422); arXiv v. Cocycle deformation and Brauer group isomorphisms, [arXiv:math/0505003](https://arxiv.org/abs/math/0505003)

### YD modules over Hopf/bi-algebroids

* [[Peter Schauenburg]], _Duals and doubles of quantum groupoids ($\times_R$-Hopf algebras)_, New Trends in Hopf Algebra Theory (La Falda, 1999), Contemp. Math. __267__, Amer. Math. Soc. (2000) 273--299

* Imre Bálint, [[Kornél Szlachányi]], _Finitary Galois extensions over noncommutative bases_, Journal of Algebra
__296__:2 (2006) 520--560 [doi](https://doi.org/10.1016/j.jalgebra.2005.09.023)

* Xiao Han, _Hopf bimodules and Yetter-Drinfeld modules of Hopf algebroids_, [arXiv:2312.03595](https://arxiv.org/abs/2312.03595)

category: algebra

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

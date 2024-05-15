
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents


## Idea

Stable anti-Yetter--Drinfeld modules are natural [[coefficients]] for [[Hopf algebra|Hopf-algebraic]] [[cyclic homology]].

Their definition is a slight variant of that of [[Yetter-Drinfeld modules]].  

## Definition

Given a [[commutative ring]] $k$ and a [[Hopf algebra]] $H$ over $k$ with an invertible [[antipode]] $S$, a $k$-[[module]] $M$ is called a *left-left anti-Yetter--Drinfeld module* if 

(i) $M$ is a left $H$-module

(ii) $M$ is a left $H$-[[comodule]] via a [[coaction]] $m\mapsto \sum m_{(-1)}\otimes m_{(0)}$

(iii) The anti-Yetter--Drinfeld compatibility condition between the $H$-module and $H$-comodule structure
is satisfied

$$
\sum (h m)_{(-1)} \otimes (h m)_{(0)} 
= \sum h_{(1)}m_{(-1)} S^{-1}(h_{(3)})\otimes h_{(2)}m_{(0)}
$$

## Properties

The category of AYD modules is not [[monoidal category|monoidal]] but the [[tensor product]] of an AYD module  with a YD module results in an AYD module.  

By the work of Rangipour--Sutlu one knows that there is such category over Lie algebras and there is a one-to-one correspondence between AYD modules over a Lie algebra and those over the universal enveloping algebra of the Lie algebra. This correspondence is extended by the same authors for bicrossed product Hopf algebras. 

The true  meaning of the AYD modules in [[noncommutative geometry]] is not known yet. There are some  attempts by [Kaygun & Khalkhali 2006](#KaygunKhalkhali06) to relate them to the curvature of flat  connections similar to the work of T. Brzezi&#324;ski on YD modules, however their identification  are not restricted to AYD and  works for a wide variety of YD type modules. 


## Related entries

* [[Yetter-Drinfeld module]]

* [[Hopf module]]

* [[cyclic homology]]


## Literature

AYD modules appeared for the first time  in  different name  in B. Rangipour's PhD thesis under supervision of M. Khalkhali. 

The notion was generalized in:

* P. M. Hajac, M. Khalkhali, B. Rangipour, Y. Sommerhaeuser: _Hopf-cyclic homology and cohomology with coefficients_, C. R. Math. Acad. Sci. Paris __338__(9), 667--672 (2004) [math.KT/0306288](https://arxiv.org/abs/math/0306288); 

* P. M. Hajac, M. Khalkhali, B. Rangipour, Y. Sommerhaeuser: _Stable anti-Yetter--Drinfeld modules_. C. R. Math Acad. Sci. Paris __338__(8), 587--590 (2004)

See also:

* [[Gabriella Böhm]], Dragos Stefan, _(Co)cyclic (co)homology of bialgebroids: An approach via (co)monads_, Comm. Math. Phys. 282 (2008), no.1, 239--286, [arxiv/0705.3190](http://arxiv.org/abs/0705.3190); _A categorical approach to cyclic duality_, J. Noncommutative Geometry __6__ (2012), no. 3, 481--538, [arxiv/0910.4622](http://arxiv.org/abs/0910.4622) 

* {#KaygunKhalkhali06} [[Atabey Kaygun]], [[Masoud Khalkhali]], _Hopf modules and noncommutative differential geometry_, Lett. Math. Phys. __76__ (2006) 77--91 [doi](https://doi.org/10.1007/s11005-006-0062-x)

> We define a new algebra of noncommutative differential forms for any Hopf algebra with an invertible antipode. We prove that there is a one-to-one correspondence
between anti-Yetter--Drinfeld modules, which serve as coefficients for the Hopf cyclic (co)homology, and modules which admit a flat connection with respect to our differential calculus. Thus, we show that these coefficient modules can be regarded as “flat bundles”
in the sense of Connes’ noncommutative differential geometry.

* B. Rangipour, Serkan S&#252;tl&#252;, _Characteristic classes of foliations via SAYD-twisted cocycles_, [arXiv:1210.5969](https://arxiv.org/abs/1210.5969);
_SAYD modules over Lie--Hopf algebras_, [arXiv:1108.6101](https://arXiv.org/abs/1108.6101); _Cyclic cohomology of Lie algebras_, [arXiv:1108.2806](https://arxiv.org/abs/1108.2806)

* Florin Panaite, Mihai D. Staic, _Generalized (anti) Yetter--Drinfeld modules as components of a braided T-category_, arXiv:[math.QA/0503413](https://arxiv.org/abs/math/0503413) 

category: algebra

[[!redirects anti-Yetter--Drinfeld module]]
[[!redirects anti-Yetter-Drinfeld modules]]
## Definition

Given a [[bialgebra]] $H$, a __Drinfel'd twist__ is an invertible element $\chi\in H\otimes H$ satisfying

$$
(1\otimes\chi)(id\otimes\Delta)\chi = (\chi\otimes 1)(\Delta\otimes id)\chi,
$$
satisfying $(\epsilon\otimes id)\chi = (id\otimes\epsilon)\chi = 1$ (in fact it is enough to require one out of these two counitality conditions). 

In [[Shahn Majid|Majid]]'s formalism of [[bialgebra cocycle]]s, this is the same as a counital 2-cocycle in $H$. 

## Application to twisting

Vladimir Drinfel'd introduced $\chi$ in order to suggest a procedure of twisting [[Hopf algebra]]s. Given a bialgebra, Hopf algebra or quasitriangular Hopf algebra, one gets another such structure twisting it with a Drinfel'd twist. Let $H$ be a quasi-triangular Hopf algebra with comultiplication $\Delta$, antipode $S$, universal R-element $R$ and let $\chi$ be a Drinfel'd twist. Then the same algebra becomes another quasitriangular Hopf algebra with formulas for comultiplication $\Delta_\chi b = \chi (\Delta b)\chi^{-1}$, universal R-element $R_\chi = \chi_{21} R\chi$ and antipode $S_\chi b = 
\sum \chi^{(1)} S(\chi^{(2)}) (S b)(\sum \chi^{(1)}S(\chi^{(2)}))^{-1}$. The counit is not changed. Here $\chi_{21}=\tau(\chi)$ where $\tau$ is the flip of tensor factors, and $\chi = \sum \chi^{(1)}\otimes\chi^{(2)}$ is a notation similar to Sweedler's convention.

## Generalizations

In the original Drinfel'd's work 2-cocycles for twisting quasi-Hopf algebras were also considered. 

There is also a subtle generalization for bialgebroids over nonassociative base due Ping Xu. 

## Literature

The original references are

* [[Vladimir Drinfeld|V. G. Drinfeld]], _Quasi-Hopf algebras and Knizhnik-Zanolodchikov equations_, Acad. Sci. Ukrainian SSR, Institute for Theoretical Physics, Preprint ITP-89-43B (Kiev 1989) [pdf](https://inis.iaea.org/collection/NCLCollectionStore/_Public/23/037/23037492.pdf)
* V. G. Drinfel'd, _Quasi-Hopf algebras_, Algebra i Analiz, 1:6 (1989) 114-148; Leningrad Math. J., 1:6 (1990) 1419-1457 ([pdf](https://www.mathnet.ru/php/getFT.phtml?jrnid=aa&paperid=53&what=fullt&option_lang=eng) in Russian)
* V. G. Drinfel'd, _Almost commutative Hopf algebras_, Algebra i Analiz, 1:2 (1989) 30-46; Leningrad Math. J., 1:2 (1990) 321-342 [mathnet.ru](https://www.mathnet.ru/eng/aa1)

Drinfeld twist and Drinfeld associator have been reproduced as special cases of higher bialgebra cocycles in works of Majid,

* [[Shahn Majid]], _Cross product quantisation, nonabelian cohomology and twisting of Hopf algebras_, in H.-D. Doebner, V.K. Dobrev, A.G. Ushveridze, eds., Generalized symmetries in Physics. World Sci. (1994) 13-41; ([arXiv:hep.th/9311184](http://front.math.ucdavis.edu/9311.3184))
* [[Shahn Majid]], _Foundations of quantum group theory_, Cambridge UP

The bialgebroid generalization is described in

* [[Ping Xu]], _Quantum groupoids_, Commun. Math. Phys. __216__ (2001) 539--581 arXiv:[q-alg/9905192](https://arxiv.org/abs/math/9905192)

category: algebra

[[!redirects Drinfeld twist]]
[[!redirects Drinfel'd twist]]
[[!redirects Drinfelʹd twist]]
[[!redirects Дринфельд twist]]
[[!redirects Drinfeld 2-cocycle]]
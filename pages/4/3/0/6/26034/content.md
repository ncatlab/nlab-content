
#Contents#
* table of contents
{:toc}

## Motivation and historical appearance

Given a finite-dimensional Hopf algebra $H$ and a $D(H)$-module algebra $A$ (where $D(H)$ is the Drinfeld double of $H$), [Lu1996](#Lu1996) has introduced the structure of a left $A$-[[associative bialgebroid|bialgebroid]] on the [[smash product algebra]] $A\sharp H$ as a noncommutative generalization of the algebra of functions on an [[action groupoid]]. In this finite-dimensional case, the category of left-right Yetter-Drinfeld modules is equivalent to the category of [[Yetter-Drinfeld module|Yetter-Drinfeld]] $H$-modules. In this new context of Yetter-Drinfeld module algebras, the construction has been generalized 
by the so called Brzeziński-Militaru construction or scalar extension bialgebroid in [BrzezinskiMilitaru2002](#BrzezinskiMilitaru). They also proved a converse, roughly that the formulas given for the scalar extension bialgebroid for an arbitrary smash product satisfy the axioms of a bialgebroid only if the module algebra which is also a comodule is in fact a braided commutative Yetter-Drinfeld algebra.

## Definition

If $(H,\Delta,\epsilon)$ (where $\Delta(h) = \sum h_{(1)}\otimes h_{(2)}$ is a bialgebra and $A$ a left-right Yetter-Drinfeld $H$-module algebra with Hopf action $\triangleright:H\otimes A\to A$ and a coaction $\rho: A\to A\otimes H$, then the smash product $A\sharp H$ inherits the left $A$-bialgebroid structure $(A\sharp H,\alpha,\beta,\Delta^{A\sharp H},\epsilon^{A\sharp H})$ where source $\alpha(a) = a\sharp 1$, target $\beta$ is $\rho$ followed by the identification of vector spaces $A\sharp H\cong A\otimes H$ and the coproduct $\Delta^{A\sharp H}$ is obtained by extending $\Delta$ along inclusion $H\to A\sharp H$, that is,
$$
\Delta^{A\sharp H} : A\sharp H\to (A\sharp H)\otimes_A (A\sharp H), \,\,\,\,a\sharp h\mapsto a\sharp h_{(1)}\otimes 1\sharp h_{(2)},
$$
which is an extension of $\Delta$ along the canonical embedding $H\to A\sharp H$. The counit is
$$
\epsilon^{A\sharp H}:A\sharp H\to A,\,\,\,\,
\epsilon^{A\sharp H}(a\sharp h) = a\epsilon(h).
$$

## Scalar extension Hopf algebroid

If $H$ is a Hopf algebra the Brzeziński-Militaru construction gives a Lu-Hopf bialgebroid and if the 
antipode $S$ of $H$ is
invertible then it gives also a
Böhm-Szlachányi symmetric Hopf algebroid. 
If the antipode $S$ is not invertible
then the data of a Yetter-Drinfeld module algebra has to be replaced by a compatible pair of a left-right Yetter-Drinfeld module algebra and a right-left Yetter-Drinfeld module algebra yielding again a symmetric Hopf algebroid [Stojic2023](#Stojic2023).

## Special case: Heisenberg double

Heisenberg double $H^*\sharp H$ of a finite-dimensional Hopf algebra is a specific example of a Hopf algebroid. There are many infinite-dimensional cases of Heisenberg double which can be cast into bialgebroids, but most often
complicated issues with completions are involved (e.g. in
[MSSncphasespace2017](#MSSncphasespace2017))

## Twists of scalar extension bialgebroids

## Literature

* {#Lu1996} [[Jiang-Hua Lu]], _Hopf algebroids and quantum groupoids_, Int. J. Math. __7__, 1 (1996) pp. 47-70, [q-alg/9505024](https://arxiv.org/abs/q-alg/9505024), [MR95e:16037](https://mathscinet.ams.org/mathscinet-getitem?mr=95e:16037), [doi](https://doi.org/10.1142/S0129167X96000050); _On the Drinfeld double and the Heisenberg double of a Hopf algebra_, Duke Math. J. __7__:3 (1994) 763-776, [MR1277953](https://www.ams.org/mathscinet-getitem?mr=1277953), [doi](https://doi.org/10.1215/S0012-7094-94-07428-0)

* {#BrzezinskiMilitaru} [[Tomasz Brzeziński]], [[Gigel Militaru]], *Bialgebroids, $\times_A$-bialgebras and duality*,  J. Algebra __251__ (2002) 279-294 &lbrack;[math.QA/0012164](https://arxiv.org/abs/math.QA/0012164), [doi:10.1006/jabr.2001.9101](https://doi.org/10.1006/jabr.2001.9101)&rbrack;


Standard reference is now

* [[G. Böhm]], _Hopf algebroids_, in Handbook of algebra, vol. 6, ed. M. Hazewinkel, arXiv:[math.RA/0805.3806](https://arxiv.org/abs/0805.3806)

Remaining issues about the antipode are settled in 

* {#Stojic2023} M. Stojić, _Scalar extension Hopf algebroids_, Journal of algebra and applications 2023 [doi](https://doi.org/10.1142/S0219498824501147) [arXiv:2208.11696](https://arxiv.org/abs/2208.11696)

Every invertible counital 2-cocycle $F = \sum F^1\otimes F^2$  (Drinfeld twist) for a bialgebra $H$, with inverse $F^{-1} = G^1\otimes G^2$, induces a Drinfeld-Xu 2-cocycle $\mathcal{G}=\sum 1\sharp G^1\otimes_A 1\sharp G^2$ for the scalar extension bialgebroid $A\sharp H$. The scalar extension for the $F$-twisted data $A_F\sharp H^F$ is isomorphic as a $A_F$-bialgebroid to the $\mathcal{G}$-twist of $A\sharp H$. 

* Andrzej Borowiec, Anna Pachoł, _Twisted bialgebroids versus bialgebroids from Drinfeld twist_, J. Phys. A50:5 (2017) [arXiv:1603.09280](https://arxiv.org/abs/1603.09280)

Some corrections and a slight generalization are given in 

* [[Zoran Škoda]], Martina Stojić, _Comment on "Twisted bialgebroids versus bialgebroids from Drinfeld twists"_, [arXiv:2308.05083](https://arxiv.org/abs/2308.05083)

An infinite-dimensional case of a Heisenberg double of a universal enveloping algebra $U(g)$ of a finite dimensional Lie algebra over a field of characteristic zero is described as a version of a completed Hopf algebroid in

* {#MSSncphasespace2017} S. Meljanac, Z. Škoda, M. Stojić, _Lie algebra type noncommutative phase spaces are Hopf algebroids_, Lett. Math. Phys. 107:3, 475–503 (2017) [doi](https://doi.org/10.1007/s11005-016-0908-9)  [arXiv:1409.8188](https://arxiv.org/abs/1409.8188)

While all the statements in the above article are rigorous, the axioms are not the most natural. A natural version where the Heisenberg double of $U(g)$ has been described as an internal Hopf algebroid (of an internal scalar extension type) in a symmetric monoidal category of (countably cofinite) filtered-cofiltered vector spaces in

* Martina Stojić, _Completed Hopf algebroids_ (in Croatian: Upotpunjeni Hopfovi algebroidi), Ph. D. thesis, University of Zagreb, 2017, 306 pp. [pdf](https://web.math.pmf.unizg.hr/~stojic/Stojic-disertacija.pdf)

Other articles include

* X. Han, [[Shahn Majid]], _Bisections and cocycles on action Hopf algebroids_, [arXiv:2305.12465](https://arxiv.org/abs/2305.12465)

Scalar extension Hopf algebroids can be recast also in the form fitting the axioms of the Hopf algebroid with a balancing subalgebra, see Sec. 4 in

* [[Zoran Škoda]], Martina Stojić, _Hopf algebroids with balancing subalgebra_, J. Alg. __598__ (2022) 445--469 [arXiv:1610.03837](https://arxiv.org/abs/1610.03837) [doi](https://doi.org/10.1016/j.jalgebra.2022.01.027)

category: algebra
[[!redirects Brzeziński-Militaru construction]]
[[!redirects scalar extension Hopf algebroid]]
[[!redirects action Hopf algebroid]]


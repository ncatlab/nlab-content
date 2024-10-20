## Definition

Given a field $k$ and two $k$-[[bialgebra]]s $A$ and $B$ with [[Hopf pairing]] $\lt, \gt : A\otimes B\to k$, one defines a left [[Hopf action]] $\blacktriangleright$ of $B$ on $A$ by formulas
$$
b\blacktriangleright a = \sum \lt b, a_{(2)}\gt a_{(1)}= (\lt,\gt \otimes \id)(b\otimes \tau\Delta_A(a))
$$
The __Heisenberg double__ corresponding to these data is the [[crossed product algebra]] (Hopf algebraic "smash product") $A\sharp B$ associated to the Hopf action $\blacktriangleright$. 

## Examples

The motivating example is the following: when $A = S(V)$ is the symmetric (Hopf) algebra on a finite-dimensional vector space $V$, and $B$ its algebraic dual $(S(V))^*\cong \hat{S}(V^*)$, considered as its dual topological Hopf algebra, the result is the [[Weyl algebra]] of [[regular differential operators]], completed with respect to the filtration corresponding to the degree of differential operator. If $B$ is just the finite dual of $S(V)$ which is a usual Hopf algebra, then there is no completion, of course. 

## Properties

If $H$ is finite-dimensional then the Heisenberg double has a structure of a [[scalar extension bialgebroid]].

## Literature

* [[Jiang-Hua Lu]], _On the Drinfeld double and the Heisenberg double of a Hopf algebra_, Duke Math. J. __74__ (1994) 763&#8211;776.

In the following paper there is an example showing that the Heisenberg double $A^*\sharp A$ has a structure of a Hopf algebroid over $A^*$; moreover $A^*$ can be replaced by any module algebra over the [[Drinfel'd double]] $D(A)$:  

* [[Jiang-Hua Lu]], _Hopf algebroids and quantum groupoids_, Int. J. Math. __7__, 1 (1996) pp. 47-70, [q-alg/9505024](http://arxiv.org/abs/q-alg/9505024), [MR95e:16037](http://www.ams.org/mathscinet-getitem?mr=95e:16037), [doi](https://doi.org/10.1142/S0129167X96000050)

An example of an infinite dimensional analogue coming from Lie algebras is treated in 

* S. Meljanac, [[Z. Škoda]], _Lie algebra type noncommutative phase spaces are Hopf algebroids_, [arxiv:1409.8188](https://arxiv.org/abs/1409.8188)

which partly refers to the following earlier paper (which however neglects the issues related to completions, and has some expositional errors)

* [[Zoran Škoda]], _Heisenberg double versus deformed derivatives_, Int. J. of Modern Physics A __26__, Nos. 27 & 28 (2011) 4845--4854, [arXiv:0909.3769](https://arxiv.org/abs/0909.3769), [doi](https://doi.org/10.1142/S0217751X11054772) 

The canonical element in the Heisenberg double satisfies a [[pentagon relation]], which is a version of pentagon relation for [[multiplicative unitaries]] of Baaj-Skandalis.  Kashaev has explained the pentagon relations for quantum [[dilogarithm]] as coming from the pentagon for the canonical element in the double.

* R.M. Kashaev, _Heisenberg double and the pentagon relation_, St. Petersburg Math. J. 8 (1997) 585--592 [q-alg/9503005](https://arxiv.org/abs/q-alg/9503005).
* [[Gigel Militaru]], _Heisenberg double, pentagon equation, structure and classification of finite-dimensional Hopf algebras_, J. London Math. Soc. (2) 69 (2004) 44--64 ([doi](https://doi.org/10.1112/S0024610703004897)).

Miscellaneous articles on Heisenberg doubles

* F. Panaite, _Doubles of (quasi) Hopf algebras and some examples of quantum groupoids and vertex groups related to them_, [math.QA/0101039](https://arxiv.org/abs/math/0101039)

* [[A. M. Semikhatov]], _A Heisenberg double addition to the logarithmic Kazhdan--Lusztig duality_, Lett. Math. Phys. __92__ (2010) 81--98 [arXiv:0905.2215](https://arxiv.org/abs/0905.2215).

* [[A. M. Semikhatov]], _Yetter--Drinfeld structures on Heisenberg doubles and chains_, [arXiv:0908.3105](https://arxiv.org/abs/0908.3105)

There are some generalizations or Heisenberg doubles in different setups

* [[Mikhail Kapranov]], _Heisenberg doubles and derived categories_, J. Alg. 202, 712--744 (1998), arXiv:[q-alg/9701009](https://arxiv.org/abs/q-alg/9701009).

* Daniele Rosso, Alistair Savage, _Twisted Heisenberg doubles_, [arxiv/1405.7889](http://arxiv.org/abs/1405.7889)

* Robert Laugwitz, _Braided Drinfeld and Heisenberg doubles_, J. Pure Appl. Alg. __219__:10 (2015) 4541-4596 [doi](https://doi.org/10.1016/j.jpaa.2015.02.031)

category: algebra
[[!redirects Heisenberg doubles]]
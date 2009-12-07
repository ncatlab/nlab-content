Eckmann and Hilton noticed that a number of notions and theorems in the [[homotopy theory]] of [[pointed spaces]] can be dualized in the sense of certain expanding dictionary:

* [[homotopy]] -- [[cohomology]]

* [[fibration]]  -- [[cofibration]]

* [[mapping cylinder]] -- [[mapping cocylinder]]

* [[suspension]] $\Sigma X$ -- [[loop space]] $\Omega X$

The "duality" in their work has been just a heuristic rather than a systematic algorithm to [[duality|dualize]] constructions and theorems. It has a little flavour of working with [[adjoint functors]], though it does not reduce to Kan adjointness. 

Later some versions have been made rigorous, the most well-known being Fuks duality in homotopy theory.

D. B. Fuks considers the category $End(k Top_*)$ of [[endofunctors]] on the category $k Top_*$ of pointed [[compactly generated space|compactly generated]] Hausdorff spaces. He enriches this category in $k Top_*$ as follows: Let $S,T$ be two endofunctors, then the set $\{S\to T\}$ of isomorphism classes of natural transformations $S\to T$ is equipped with the weakest topology in which all maps $\alpha_X$, $X\in k Top_*$, of taking components $\{S\to T\}\mapsto Map(S(X),T(X))\in kTop_*$ are [[continuous map|continuous]]. Recall that the topology on the set of maps $S(X)\to T(X)$ in $k Top_*$ is obatined by first taking the [[compact-open topology]] and then performing the [[kaonization]] of the space so obtained. 

A **Fuks duality** is any functor $D: End(kTop_*)\to End(kTop_*)$ such that 

1. for any two functors $S,T\in End(kTop_*)$, $\{S\to D T\}$ is binaturally homeomorphic to
$\{D S\to T\}$ 

2. $D\Sigma =\Omega$, $D\Omega = \Sigma$.

+-- {: .un_theorem}
###### Theorem (D. B. Fuks)
There exists a unique Fuks duality functor. 
=--

Notice that $D^2 = D\circ D$ is not isomorphic to the [[identity functor|identity]] in general, though it is identical when applied to a number of natural endofunctors in homotopy theory. Fuks duality can be extended suitably to functors of many arguments. 

* D. B. Fuks, On duality in homotopy theory, Soviet Math. Dokl. 2 (1961), 1575--1578.

* D. B. Fuks, Eckmann--Hilton duality and the theory of functors in the category of topological spaces, 1966 Russ. Math. Surv. 21 1--33 [doi](http://dx.doi.org/10.1070/RM1966v021n02ABEH004149), [free Russian original pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=rm&paperid=5847&what=fullt&option_lang=rus)

* R. Nakagawa, On Fuks homotopy duality, Sci. Rep. Tokyo Kyoiku Daigaku Sect. A 8 (1963), 93--98. 


[[!redirects Fuks duality]]
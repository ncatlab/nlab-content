## Idea

The __Schneider's descent theorem__ is a noncommutative affine analogue of the [[descent along a torsor]] where the structure group is also replaced by a Hopf algebra.  

## The theorem

### Preliminaries

Let $H$ be a Hopf algebra with comultiplication $\Delta$ and $E = (E,\rho_E:E\to E\otimes H)$ a right $H$-comodule algebra. Consider the subalgebra $U = E^{co H}\subset E$ of coinvariants. Consider the category ${}_E\mathcal{M}^H$ of relative [[Hopf modules]] and the category ${}_U\mathcal{M}$ of left $U$-modules. There is a pair of adjoint functors between these two categories: 

Taking coinvariants extends to a functor $()^{co H}:{}_E\mathcal{M}^H\to {}_U\mathcal{M}$. Scalar extension of a $U$-module $M$, $E\otimes_U M$ is canonically a relative Hopf module via coaction $e\otimes_U m\mapsto (e_{(0)}\otimes_U m)\otimes e_{(1)}$ and the map $M\mapsto E\otimes_U M$ extends to a functor $E\otimes_U -:{}_U\mathcal{M}\to {}_E\mathcal{M}^H$ which is adjoint to $()^{co H}$. The unit of the adjunction has components $\eta_N : N\mapsto (E\otimes_U N)^{co H}$, $n\mapsto 1\otimes_U n$ and the counit is $\epsilon_M:E\otimes_U M^{co H}\to M$, $e\otimes_U m\mapsto e m$.

### Statement

In the left-right version, it says that given a Hopf algebra $H$ and a faithfully flat right [[Hopf-Galois extension]] $U\hookrightarrow E$ which is faithfully flat from the left, the category of left-right relative Hopf modules ${}_E\mathcal{M}^H$ is equivalent to the category of left $U$-modules ${}_U \mathcal{M}$ via the adjoint equivalence described above. 

Schneider proves the equivalence for left-left Hopf modules, hence he needs an additional assumption that $H$ has a bijective antipode. 

### Modern proofs

Schneider's original proof is rather involved. Modern proofs begin by rephrasing the category of relative Hopf modules in different terms, either as modules over certain
cosimplicial algebra ("coBorel construction" by Lunts-Škoda 2002, see [ŠkodaGMJ2009](#ŠkodaGMJ2009)), or as comodules over related comonad $G$ on the category of $E$-modules, or comodules over an $E$-coring (Brzezinski 2002). Then the Hopf-Galois condition $E\otimes_U E\cong E\otimes H$ directly gives the equivalence of any of the three constructions with the analogue in the descent theory for extension of rings; for example the Sweedler coring $E\otimes_U E$ is isomorphic to the mentioned coring. Hence the categories of comodules are equivalent and the theorem hence boils down to the standard faithfully flat descent (for noncommutative rings) or comonadicity criterium in comonadic version. 

Let us describe the comonad $G$ on the category of left $E$-modules, ${}_E\mathcal{M}$. As an endofunctor, $G$ sends a left $E$-modules $M$ to $M\otimes H$ with $H$-coaction $\id_M\otimes\Delta:M\otimes H\to (M\otimes H)\otimes H$ and left $E$-action, 
$$e\otimes (m\otimes h) = \sum e_{(0)} m\otimes e_{(1)} h.$$
(Remark: This action is induced by a distributive law.) The [[Eilenberg-Moore category]] of this comonad is equivalent to ${}_E\mathcal{M}^H$.

## Literature

* [[Hans-Jürgen Schneider]], _Principal homogeneous spaces for arbitrary Hopf algebras_, 
Israel J. Math. __72__ (1990), no. 1-2, 167--195 [MR92a:16047](http://www.ams.org/mathscinet-getitem?mr=1098988) [doi](https://doi.org/10.1007/BF02764619)
* {#ŠkodaGMJ2009} [[Z. Škoda]], _Some equivariant constructions in noncommutative algebraic geometry_, Georgian Mathematical Journal __16__ (2009), No. 1, 183--202, [arXiv:0811.4770](https://arxiv.org/abs/0811.4770) [MR2011b:14004](http://www.ams.org/mathscinet-getitem?mr=2527623)

A generalization to Hopf algebroids is proven in 

* A. Ardizzoni, [[G. Böhm]], C. Menini, _A Schneider type theorem for Hopf algebroids_, J. Algebra __318__ (2007), no. 1, 225&#8211;269 [MR2008j:16103](http://www.ams.org/mathscinet-getitem?mr=2363132) [doi](https://doi.org/10.1016/j.jalgebra.2007.05.017) [math.QA/0612633](http://arxiv.org/abs/math/0612633) (arXiv version is unified, corrected); _Corrigendum_, J. Algebra __321__:6 (2009) 1786-1796 [MR2010b:16060](http://www.ams.org/mathscinet-getitem?mr=2498268) [doi](https://doi.org/10.1016/j.jalgebra.2008.11.040)

[[!redirects Schneider's descent theorem]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The __associative Yang-Baxter equation__ (AYBE) is an [[associativity|associative]] analogue of the [[classical Yang-Baxter equation]]. 

## Definition

If $A$ is a $k$-algebra then, in Leningrad notation, the AYBE for a matrix $r\in A\otimes A$ is the condition

$$
r_{1 3} r_{1 2} - r_{1 2} r_{2 3} + r_{2 3} r_{1 3} = 0
$$

If $r = \sum a_i\otimes b_i$, then the operator $P:A\to A$ given by

$$
P(x) = \sum a_i x b_i
$$

is a Rota-Baxter operator of weight $0$, i.e. $(A,P)$ is a [[Rota-Baxter algebra]] of weight $\lambda = 0$. 

The skew-symmetric solutions ($r_{1 2} = - r_{2 1}$) of AYBE give rise to 

* an algebra with the trace quadratic Poisson bracket

* double Poisson structures on a free associative algebra

* an anti-Frobenius associative subalgebra of a matrix algebra

## Related concepts

[[!include Yang-Baxter equations -- contents]]


## References

* V.N. Zhelyabin, _Jordan bialgebras of symmetric elements and Lie bialgebras_, Siberian Mathematical Journal __39__ (1998, 261-276, [open access pdf in Russian](http://www.mathnet.ru/links/da921ffaf25317abe8ca0e15e9c91eda/smj275.pdf)) 

* [[Marcelo Aguiar]], _Infinitesimal Hopf algebras_,  Contemporary Mathematics, 267 (2000) 1-29; _Pre-Poisson algebras_, Lett. Math. Phys. 54 (2000) 263-277, [doi](http://dx.doi.org/10.1023/A:1010818119040); _On the associative analog of Lie bialgebras_,  Journal of Algebra __244__ (2001, 492-532, [open access pdf](http://www.sciencedirect.com/science/article/pii/S0021869301988775/pdf?md5=322e83568195266edf53989698f3ae78&pid=1-s2.0-S0021869301988775-main.pdf)

* A. Polishchuk, _Classical  Yang-Baxter equation  and the $A_\infty$-constraint_, Adv. Math. __168__ (2002, 56-95) [open access pdf](http://ac.els-cdn.com/S000187080192047X/1-s2.0-S000187080192047X-main.pdf?_tid=39dd1e78-93f8-11e7-9f5c-00000aab0f01&acdnat=1504808179_dfd4e9b508ad159abe651d8258654b58)

* Chengming Bai, Li Guo, Xiang Ni, _$\mathcal{O}$-operators on associative algebras and associative Yang-Baxter equations_, Pacific J. Math. __256__ (2012) 257-289, [arxiv/0910.3261](http://arxiv.org/abs/0910.3261)

* Travis Schedler, _Poisson algebras and Yang-Baxter equations_, in: Advances in quantum computation (Tyler, TX, 2007) (Providence, RI) (K. Mahdavi and D. Koslover, eds.), Contemp. Math. __482__ (2009) 91--106
arXiv:[math.QA/0612493](https://arxiv.org/abs/math.QA/0612493)

* V. Sokolov, _Classification of constant solutions for associative Yang-Baxter on $gl(3)$_, [arxiv/1212.6421](http://arxiv.org/abs/1212.6421)

* [[A. Odesskii]], [[V. Rubtsov]], V. Sokolov, _Double Poisson brackets on free associative algebras_, in: Noncommutative Birational Geometry, Representations and Combinatorics, Contemp. Math. __592__, Amer. Math. Soc. (2013) 225--239 [doi](https://arxiv.org/abs/1208.2935) [arxiv/1208.2935](https://arxiv.org/abs/1208.2935)
*  [[A. Odesskii]], [[V. Rubtsov]], V. Sokolov, _Parameter-dependent associative Yang–Baxter equations and Poisson brackets_, Int. J. Geom. Meth. Mod. Phys. __11__:09, 1460036 (2014) Proc. XXII IFWGP, Univ. of Évora, Portugal, 2013 [doi](https://doi.org/10.1142/S0219887814600366)

category: algebra, physics

[[!redirects AYBE]]
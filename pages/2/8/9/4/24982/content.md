# Contents
* table of contents
{: toc}

## Idea

_Hida theory_ is an approach to p-adic interpolation of [[modular forms]] in the ordinary case.

## Definitions

This section follows chapter 8 of [DarmonRotgerAWS](#DarmonRotgerAWS).

Let $\Lambda$ be the [[Iwasawa algebra]] $\mathbb{Z}_{p}[[\Gamma]]$ where $\Gamma=(1+p\mathbb{Z}_{p})^{\times}$. We have that $\Lambda\cong \mathbb{Z}_{p}[[T]]$. We can further identify $\Lambda$ as the ring of rigid analytic functions on the _weight space_

$$\mathcal{X}:=\Hom_{cts}(\Gamma,\mathbb{C}^{\times}).$$

A point $\nu\in \mathcal{X}$ is called an _arithmetic point_ if there exists and integer $k$ (called the _weight_) and a [[Dirichlet character]] $\chi$ of p-power order and values in $\mathbb{C}_{p}^{\times}$ such that

$$\nu(x)=\chi(x)x^{k}$$

for all $x\in (1+p\mathbb{Z}_{p})$.

More generally a finite extension $\widetilde{\Lambda}$ of $\Lambda$ can be identified with the ring of rigid analytic functions on an etale cover $\widetilde{\mathcal{X}}$ of $\mathcal{X}$.

A _$\Lambda$-adic modular form_ of tame level $N$ and tame character $\chi$ is a pair $(\widetilde{\Lambda},\underline{g})$ where $\widetilde{\Lambda}$ is a finite extension of $\Lambda$ and

$$\underline{g}:=\sum \underline{a}_{n}q^{n}$$

where $\underline{a}_{n}\in \widetilde{\Lambda}$, such that for almost all $\nu\in\widetilde{X}$ of weight $k\in\mathbb{Z}\geq 2$, the power series

$$\underline{g}:=\sum \underline{a}_{n}(\nu)q^{n}$$

is the q-expansion of a classical normalized ordinary eigenform of weight $k$ and level $N$.

## Related concepts

* [[eigenvariety]]

* [[p-adic modular form]]

## References

* Chris Williams, _An Introduction to Hida Theory_ ([pdf](http://www.im.ufrj.br/~aftab/An%20Introduction%20to%20Hida%20Theory.pdf))

* Cameron Franc, _Hida Theory_ ([pdf](http://virtualmath1.stanford.edu/~conrad/DarmonCM/2011Notes/hida_theory.pdf))

A discussion may also be found in chapter 8 of

* {#DarmonRotgerAWS} Henri Darmon and Victor Rotger, _Algebraic Cycles and Stark-Heegner Points_, ([pdf](http://virtualmath1.stanford.edu/~conrad/DarmonCM/2011Notes/hida_theory.pdf))
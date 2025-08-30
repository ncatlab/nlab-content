
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

The _Verity-Gray tensor product_ or _lax Gray tensor product of [[stratified simplicial sets]]_ is a [[tensor product]] on the [[category]] $Strat$ of [[stratified simplicial sets]] which, when restricted to [[complicial sets]], i.e. to [[oriental|omega-nerves]] of [[strict omega-category|strict omega-categories]], reproduces the [[Crans-Gray tensor product]] on strict $\omega$-categories.

## Definition

Let $(X, t X)$ and $(Y, t Y)$ be [[stratified simplicial sets]]. Then their **Verity-Gray tensor product** $(X, t X) \otimes (Y, t Y)$ is given by

$$
  (X, t X) \otimes (Y, t Y)
  \coloneqq
  \big(X \times Y, q(t X, t Y)\big)
  \,,
$$

where $X \times Y$ is the [[cartesian product]] of [[simplicial sets]] (hence the standard monoidal structure on [[SSet]], cf. at *[[product of simplices]]*), while $q(t X, t Y)$, the set of thin cells, is $t X \times t Y$ for the [[Gray tensor product]], and for the lax-Gray product  is enlarged as described in the paper.



## References

* {#Verity08} [[Dominic Verity]], §7.2 & §11.4 in: *Complicial Sets Characterising the Simplicial Nerves of Strict $\omega$-Categories*, Memoirs of the AMS, **193** 905 (2008) &lbrack;[arXiv:math/0410412](http://arxiv.org/abs/math/0410412), [ams:memo-193-905](https://bookstore.ams.org/memo-193-905/)&rbrack;

* {#Verity08b} [[Dominic Verity]], def 59 (p. 32) of: *Weak complicial sets I: Basic homotopy theory*, Advances in Mathematics **219** 4 (2008) 1081-1149 &lbrack;[arXiv:math/0604414](http://arxiv.org/abs/math/0604414), [doi:10.1016/j.aim.2008.06.003](https://doi.org/10.1016/j.aim.2008.06.003)&rbrack;

* [[Dominic Verity]], around slide 60 of:: _Weak complicial sets and internal quasi-categories_, talk at *[[Category Theory conference|Category Theory 2007]]* &lbrack;[pdf](http://www.mat.uc.pt/~categ/ct2007/slides/verity.pdf), [[Verity-WeakComplicialAndQuasi.pdf:file]]&rbrack;




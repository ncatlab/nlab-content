# Accessible model categories

* table of contents
{: toc}

## Definition

An **accessible model category** is a [[model structure]] on a [[locally presentable category]] whose two [[weak factorization systems]] can be realized by [[functorial factorizations]] that are [[accessible functors]], that is that they are [[accessible weak factorization systems]].

This implies that in fact its weak factorization systems can be enhanced to [[algebraic weak factorization systems]] that are also accessible (see [[accessible wfs]]).  However, such algebraic structure is not given as data in the notion of accessible model category: for that, see [[algebraic model category]].

## Properties

### Left and right lifting

Accessible model structures can be both left- and right-lifted along adjunctions as long as the relevant "acyclicity condition" holds.  That is, let $U:A\to B$ be a functor between locally presentable categories and suppose $B$ is an accessible model category.  Then:

1. If $U$ is a right adjoint, then there is a model structure on $A$ in which the weak equivalences and fibrations are created by $U$ (i.e. $W_A = U^{-1}(W_B)$ and $F_A = U^{-1}(F_B)$) if and only if every map having the left lifting property with respect to $F_A$ lies in $W_A$.

1. If $U$ is a left adjoint, then there is a model structure on $A$ in which the weak equivalences and cofibrations are created by $U$ (i.e. $W_A = U^{-1}(W_B)$ and $C_A = U^{-1}(C_B)$) if and only if every map having the right lifting property with respect to $C_A$ lies in $W_A$.

Both of the lifted model structures are then again accessible.  See [[transferred model structure]].  For proofs, see [HKRS](#HKRS15) and its correction in [GKR](#GKR18).

## Related concepts

* [[accessible weak factorization system]]
* [[algebraic model category]]

[[!include algebraic model structures - table]]

## References

* {#Rosicky17} [[Jiri Rosicky]], *Accessible model categories*,  Appl Categor Struct (2017) 25: 187. [doi](https://doi.org/10.1007/s10485-015-9419-6), [arxiv](https://arxiv.org/abs/1503.05010)

* {#HKRS15} [[Kathryn Hess]], Magdalena K&#281;dziorek, [[Emily Riehl]], [[Brooke Shipley]], _A necessary and sufficient condition for induced model structures_ ([arXiv:1509.08154](http://arxiv.org/abs/1509.08154)).  This paper contains an error, corrected by:

* {#GKR18} [[Richard Garner]], Magdalena Kedziorek, [[Emily Riehl]], _Lifting accessible model structures_, [arXiv:1802.09889](https://arxiv.org/abs/1802.09889)

* [[John Bourke]], *Equipping weak equivalences with algebraic structure*, [arxiv:1712.02523](https://arxiv.org/abs/1712.02523)

[[!redirects accessible model categories]]
[[!redirects accessible model structure]]
[[!redirects accessible model structures]]

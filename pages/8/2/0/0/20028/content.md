# Accessible model categories

* table of contents
{: toc}

## Definition

An **accessible model category** is a [[model structure]] on a [[locally presentable category]] whose two [[weak factorization systems]] can be realized by [[functorial factorizations]] that are [[accessible functors]].  This implies that in fact its weak factorization systems can be enhanced to [[algebraic weak factorization systems]] that are also accessible.

## Properties

The following, which shows that the two definitions of accessible model category agree, is Remark 3.1.8 of [HKRS15](#HKRS15), which relies on Theorem 4.3 of [Rosicky17](#Rosicky17).

\begin{theorem}
Suppose $E$ is an accessible functorial factorization on a locally presentable category $M$, realizing a weak factorization system.  Then there is an accessible algebraic weak factorization system realizing the same weak factorization system.
\end{theorem}
\begin{proof}
Let $Coalg(L)$ be the category of [[algebra over an endofunctor|coalgebras]] for the [[pointed endofunctor|copointed endofunctor]] of the [[arrow category]] $M^\to$ induced by $E$, i.e. morphisms equipped with a section of their $E$-factorization exhibiting them as a retract of the first factor.  Then $Coalg(L)$ is locally presentable (being complete and a [[PIE limit]] construction from $M$).  Thus, it has a small dense subcategory $X$.  We can then apply [[Garner's small object argument]] to generate an algebraically-free algebraic weak factorization system from $X$.  The algebraic right-maps in this awfs are the morphisms with coherent lifting functions against $X$, which by density is the same as having a coherent lifting function against all of $Coalg(L)$, which is the same as being an algebra for the pointed endofunctor of $M^\to$ corresponding to $E$.  Thus this is an awfs with the same right-maps, hence the same underlying weak factorization system.
\end{proof}

## References

* {#Rosicky17} [[Jiri Rosicky]], *Accessible model categories*,  Appl Categor Struct (2017) 25: 187. [doi](https://doi.org/10.1007/s10485-015-9419-6), [arxiv](https://arxiv.org/abs/1503.05010)

* {#HKRS15} [[Kathryn Hess]], Magdalena K&#281;dziorek, [[Emily Riehl]], [[Brooke Shipley]], _A necessary and sufficient condition for induced model structures_ ([arXiv:1509.08154](http://arxiv.org/abs/1509.08154)).  This paper contains an error, corrected by:

* {#GKR18} [[Richard Garner]], Magdalena Kedziorek, [[Emily Riehl]], _Lifting accessible model structures_, [arXiv:1802.09889](https://arxiv.org/abs/1802.09889)

* [[John Bourke]], *Equipping weak equivalences with algebraic structure*, [arxiv:1712.02523](https://arxiv.org/abs/1712.02523)

[[!redirects accessible model categories]]
[[!redirects accessible model structure]]
[[!redirects accessible model structures]]

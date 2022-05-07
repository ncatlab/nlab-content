
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[homotopy 2-category]] $Ho_2\big((\infty,1)Cat\big)$ of the [[(∞,2)-category]] [[(∞,1)Cat]] of [[(∞,1)-categories]] has been argued ([Riehl & Verity 13](#RiehlVerity13), following [Joyal 08](#Joyal08) [p. 158](https://ncatlab.org/nlab/files/JoyalTheoryOfQuasiCategories.pdf#page=10)) to provide a useful context for [[(∞,1)-category theory]] (in the spirit of [[John Gray]]'s "[[Adjointness for 2-Categories|formal category theory]]" in the [[2-category]] [[Cat]] of plain [[categories]]). 

For example, the notion of [[adjoint (∞,1)-functors]] turns out to equivalently reduce to plain [[adjunctions]] in this homotopy 2-category ([Joyal 08](#Joyal08) [p. 159](https://ncatlab.org/nlab/files/JoyalTheoryOfQuasiCategories.pdf#page=11), [Riehl & Verity 13, Sec 4](#RiehlVerity13), see [below](#AdjunctionsAndAdjointInfinityFunctors).

## Properties

### Adjunctions and adjoint $(\infty,1)$-functors
 {#AdjunctionsAndAdjointInfinityFunctors}

\begin{proposition}
\label{AdjointInfinityFunctorsInHomotopy2Category}
  An adjunction in the [[homotopy 2-category of (infinity,1)-categories|homotopy 2-category of $(\infty,1)$-categories]] is equivalently a pair of [[adjoint (infinity,1)-functors|adjoint $(\infty,1)$-functors]].
\end{proposition}
([Riehl & Verity 2015, Rem. 4.4.5](adjoint+infinity1-functor#RiehlVerity15); [Riehl & Verity 2022, Prop. F.5.6](adjoint+infinity1-functor#RVElements); see [there](adjoint+infinity1-functor#InTheHomotopy2Category) for more).


\begin{remark}
  In view of its classical analog ([this Prop.](adjunction#AdjunctionsInCatAreAdjointFunctors)),
  the remarkable aspect of Prop. \ref{AdjointInfinityFunctorsInHomotopy2Category} is that the [[homotopy 2-category of (infinity,1)-categories|homotopy 2-category of $\infty$-categories]] is sufficient to detect adjointness of [[(infinity,1)-functors|$\infty$-functors]], which would, *a priori*, be defined as a kind of homotopy-coherent adjointness in the full [[(infinity,2)-category|$(\infty,2)$-category]] [[(infinity,1)Cat|$Cat_{(\infty,1)}$]]. For more on this reduction of homotopy-coherent adjunctions to plain adjunctions see [Riehl & Verity 2016, Thm. 4.3.11, 4.4.11](adjoint+infinity1-functor#RiehlVerity16).
\end{remark}


### Relation to homotopy 2-category of model categories?
 {#RelationToHomotopy2CategoryOfCombinatorialModelCategories}

One might expect (by the discussion [there](locally+presentable+infinity-category#PresentedByCombinatorialSimplicialModelCategories)) that the [[homotopy 2-category]] of [[locally presentable (∞,1)-categories]] 
([Joyal 08](#Joyal08) [p. 348](https://ncatlab.org/nlab/files/JoyalTheoryOfQuasiCategories.pdf#page=40))
is [[equivalence of 2-categories|equivalent]] to the [[localization of a 2-category|localization of the 2-category]] of [[combinatorial model categories]] at the [[Quillen equivalences]], [[Ho(CombModCat)]]. 

At least for the homotopy $(2,1)$-categories this is proven in [Pavlov 2021](HoCombModCat#Pavlov21)
and for presentable [[derivators]] it is proven in [Renaudin 2006](HoCombModCat#Renaudin06).



## Related concepts

* [[adjoint (∞,1)-functor]]

* [[Ho(CombModCat)]]


## References

With [[(∞,1)-categories]] modeled as [[quasi-categories]], their homotopy 2-category was considered first in

* {#Joyal08} [[André Joyal]], p. 158 (10 of 348) in: _The theory of quasicategories and its applications_, lectures at: _[Advanced Course on Simplicial Methods in Higher Categories](https://lists.lehigh.edu/pipermail/algtop-l/2007q4/000017.html)_, Quadern **45** 2, Centre de Recerca Matemàtica, Barcelona 2008 ([[JoyalTheoryOfQuasiCategories.pdf:file]])

and then developed further (in terms of [[∞-cosmoi]]) in:

* {#RiehlVerity13} [[Emily Riehl]], [[Dominic Verity]], _The 2-category theory of quasi-categories_, Advances in Mathematics Volume 280, 6 August 2015, Pages 549-642 ([arXiv:1306.5144](http://arxiv.org/abs/1306.5144), [doi:10.1016/j.aim.2015.04.021](https://doi.org/10.1016/j.aim.2015.04.021))

Review and further discussion in:

* {#Riehl14} [[Emily Riehl]], Chapter 18 of: _[[Categorical Homotopy Theory]]_, Cambridge University Press, 2014 ([pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf), [doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457))

* {#RiehlVerity15} [[Emily Riehl]], [[Dominic Verity]], Section 3 of: _Fibrations and Yoneda's lemma in an $\infty$-cosmos_, Journal of Pure and Applied Algebra Volume 221, Issue 3, March 2017, Pages 499-564 ([arXiv:1506.05500](https://arxiv.org/abs/1506.05500), [doi:10.1016/j.jpaa.2016.07.003](https://doi.org/10.1016/j.jpaa.2016.07.003))

* {#RiehlVerity16} [[Emily Riehl]], [[Dominic Verity]], Section 1.3 in: _Infinity category theory from scratch_, Higher Structures Vol 4, No 1 (2020) ([arXiv:1608.05314](https://arxiv.org/abs/1608.05314), [pdf](http://www.math.jhu.edu/~eriehl/scratch.pdf))

* {#RiehlVerity21} [[Emily Riehl]], [[Dominic Verity]], Chapter 1 of: *Elements of $\infty$-Category Theory*, 2021 ([pdf](https://emilyriehl.github.io/files/elements.pdf))

[[!redirects homotopy 2-category of (infinity,1)-categories]]

[[!redirects homotopy 2-category of infinity-categories]]
[[!redirects homotopy 2-category of infinity1-categories]]


[[!redirects homotopy 2-category of quasi-categories]]
[[!redirects homotopy 2-category of quasicategories]]




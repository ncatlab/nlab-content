
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* toc
{: toc}

[[Barr]] proved a theorem about [[embedding of categories|embedding]] [[regular categories]] into [[presheaf category|categories of]] [[small presheaves]], and also a strengthening for [[Barr exact categories]].

## Idea  

Barr's embedding theorem has the classical form of many embedding[^note] theorems in mathematics: if a structure $\mathcal{C}$ has certain good properties, then it admits an embedding with certain other good properties into another structure $\mathcal{D}$ which is somehow more explicit than $\mathcal{C}$.


For example, 


* by Tychonoff's embedding theorem, if a $T_0$ space $X$ is [[completely regular]], then there exists an embedding of $X$ into a product of [[metric space]]s

* by the [[Whitney embedding theorem]], if an abstract $d$-dimensional real manifold $M$ is smooth, then there exists an embedding, which is an [[embedding of smooth manifolds]], of $M$ into the explicit real manifold that is $\mathbb{R}^{2d}$

* by the [[Freyd-Mitchell embedding theorem]], if a category is [[small]] and [[abelian category|abelian]], then there exist an embedding, which is [[exact functor|exact]], into the category of modules of a (not necessarily commutative) [[ring]]. 

and, 

* by Barr's embedding theorem, if a category is [[small]] and [[regular category|regular]], then there exists an [[embedding]], which is a full, faithful and [[regular functor|regular]], into a category of [[presheaves]] over some [[small category]]. 


## A proof of Makkai

The proof of (a version of) Barr's theorem given by Makkai in [Makkai1980](#Makkai80) is a nice example of a non-trivial application of [[ultraproduct]]s in category theory.

## References

It has been proved in 

* [[Michael Barr|M. Barr]], _Exact categories_, Lecture Notes in Math. __236__, (Springer, Berlin, 1971), 1-120.

and, in a different way, in 

* M. Barr, _Representation of categories_, J. Pure Appl. Alg. __41__ (1986) 113-137 (this article has supposedly some fixable errors).

* F. Borceux, _A propos d'un th&#233;or&#232;me de Barr_, S&#233;minaire de math&#233;matique (nouvelle s&#233;rie) Rapport 28 - Mai 1983, Institute de Mathematique Pure et Appliqee, Univ. Cath. de Louvain.

* M. Makkai, _A theorem on Barr-exact categories, with an infinitary generalization_, Ann. Pure Appl. Logic __47__ (1990), no. 3, 225-268.

[[Michael Barr]]'s full exact embedding theorem for [[Barr exact categories]], proved in (?)

* Michael Barr, _Embedding of categories_, Proc. Amer. Math. Soc. __37__, No. 1 (Jan., 1973), pp. 42-46 ([jstor](http://www.jstor.org/stable/2038702), [pdf](http://www.math.mcgill.ca/barr/papers/embed.pdf))

generalizes the Lubkin-Freyd-Mitchell embedding theorems for abelian categories. The Giraud's theorem for topoi is not much more than a special case of that theorem. 

* {#Makkai80} M. Makkai, _On full embeddings I_, Journal of Pure and Applied Algebra __16__, (1980), pp. 183-195

* M. Makkai, _Full continuous embeddings of toposes_, Trans. Amer. Math. Soc. __269__, No. 1 (Jan., 1982), pp. 167-196 [jstor](http://www.jstor.org/stable/1998599)

One can also consider categories enriched over a locally finitely presentable closed symmetric monoidal category $V$. Such a $V$-category $C$ is regular if it is finitely complete, admits the coequalizers of kernel pairs all [[regular epimorphism]]s are universal (i.e. stable under pullbacks) and stable under cotensors with the finite objects. A $V$-functor is regular if it preserves finite limits and regular epimorphisms. The following generalizes the Barr's embedding theorem for regular categories to the regular enriched categories:

* Dimitri Chikhladze, _Barr's embedding theorem for enriched categories_, J. Pure Appl. Alg. __215__, n. 9 (2011) 2148-2153, [arxiv/0903.1173](http://arxiv.org/abs/0903.1173), [doi](http://dx.doi.org/10.1016/j.jpaa.2010.12.004)

Its main result is 

> Theorem 10. For a small regular $V$-category $C$ there exists a small category $T$ and a regular fully faithful functor $E : C \longrightarrow [T, V]$.

[[!redirects Barr's embedding theorem]]
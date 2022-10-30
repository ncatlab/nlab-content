
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Supercompact cardinals are among the [[large cardinal]]s.


## Definition

For $S$ a [[set]] and $\kappa$ a [[cardinal]], let $P_\kappa(S)$ be the set of [[subset]]s of $S$ of cardinality less than $\kappa$.

For $\lambda$ an [[ordinal]] a cardinal $\kappa$ is called **$\lambda$-supercompact** if $P_\kappa(\lambda)$ admits a [[normal measure]]. It is **supercompact** if it is $\lambda$-supercompact for every $\lambda$.

$\kappa$ being $\lambda$-supercompact is equivalent to there being an [[elementary embedding]]  $j : V \to M$ such that $j(\alpha) = \alpha$ for all $\alpha \lt \kappa$ and $j(\kappa) \gt \lambda$, where $M$ is an [[inner model]] such that $\{f | f : \lambda \to M\} \subset M$, i.e. every $\lambda$-sequence of elements of $M$ is an element of $M$.  


## Properties

By invoking [[Vopěnka's principle]] one can make strong statements about the existence of [[reflective subcategories]].  The assumption of supercompact cardinals is much weaker, and accordingly they similarly imply existence of reflective subcategories only under some more additional assumptions.  The following theorems are all from ([BCMR](#BagariaCasacubertaMathiasRosicky)).

+-- {: .num_theorem}
###### Theorem
Suppose there are arbitrarily large supercompact cardinals.  Then if $L$ is a reflection on an accessible category $C$ and the class of $L$-equivalences is $\Sigma_2$-[[Levy hierarchy|definable]], then the $L$-local objects are a small-orthogonality class (so that $L$ is a localization with respect to some [[set]] of morphisms).
=--

+-- {: .num_theorem}
###### Theorem
Suppose there are arbitrarily large supercompact cardinals.  Then any full subcategory of a locally presentable category which is closed under limits and $\Sigma_2$-[[Levy hierarchy|definable]] is reflective.
=--

There is also a generalization to $\Sigma_n$-definability involving [[C(n)-extendible cardinals]]; see [[Vopenka's principle]].


## References

Supercompact cardinals are discussed for instance in

* T. Jech _Set Theory_ The Third Millenium Edition, Revised and Expanded.
Springer Monographs in Mathematics. Springer-Verlag, Berlin, Heidelberg (2003)

* A. Kanamori, _The Higher Infinite: Large Cardinals in Set Theory from Their
Beginnings_ Perspectives in Mathematical Logic. Springer-Verlag, Berlin, Heidelberg (1994)

The relation to refelctive subcategories is discusssed in

* Joan Bagaria, [[Carles Casacuberta]], Adrian Mathias, _Epireflections and supercompact cardinals_  Journal of Pure and Applied Algebra 213 (2009), 1208-1215 ([pdf](http://atlas.mat.ub.es/personals/casac/articles/bcm.pdf))
{#BagariaCasacubertaMathias}

* Joan Bagaria, [[Carles Casacuberta]], Adrian Mathias, [[Jiri Rosicky]] _Definable orthogonality classes in accessible categories are small_, [arXiv](http://arxiv.org/abs/1101.2792)
{#BagariaCasacubertaMathiasRosicky}

[[!redirects supercompact cardinal]]
[[!redirects supercompact cardinals]]
[[!redirects supercompact cardinal number]]
[[!redirects supercompact cardinal numbers]]

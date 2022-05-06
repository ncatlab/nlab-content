
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[mathematics]] typically by default the term "configuration space" of a [[topological space]] $X$ refers to the topological space of pairwise distinct points in $X$, also called _[[Fadell's configuration space]]_, for emphasis.

In principle many other kinds of configurations and the spaces these form may be referred to by "configuration space", notably in [[physics]] the usage is in a broader sense, see at _[[configuration space (physics)]]_.

## Definition

(...)

([Bödigheimer 87, 1](#Boedigheimer87))

(...)

## Properties

### Cocycle spaces and the Scanning map
 {#CocycleSpacesAndScanningMap}


For $X$ a [[compact topological space|compact]] [[manifold]] and $A$ a [[pointed topological space]] ("[[charge]] [[coefficients]]"), there is the [[scanning map]]

$$
  Conf(X, A)
  \longrightarrow
  \Gamma( S_X(T X)\wedge_X A  )
$$

from the configuration space of points in $X$ with charge in $A$ and [[continuous function|continuous]] [[sections]] of the [[spherical fibration]] induced by the [[tangent bundle]] of $X$ [[fiber]]-wise [[smash product|smashed]] with the [[coefficients]] $A$.

Under mild conditions, this is a [[homotopy equivalence]].

This is due to ([McDuff 75](#McDuff75)), for review see ([Bödigheimer 87, Prop. 2](#Boedigheimer87), [Francis Lecture 17, Theorem 1.1](#FrancisLect17)).

If here $A = S^n$ is an [[n-sphere]]  regarded as [[coefficients]] for [[non-abelian cohomology]], then this equivalence identifies the configuration space with the [[cocycle]] space/[[infinity-groupoid]] of $\tau_X$-[[twisted cohomology|twisted]] [[cohomotopy]] in degree $\tau + n$, where $\tau_X \coloneqq [S_X(T X)]$ is the class of the [[spherical fibration]] of the tangent bundle.

In particular if $X$ is a [[parallelizable manifold]]/[[framed manifold]], then $\tau_X = dim(X)$ and the equivalence identifies the configuration space with the plain [[cohomotopy]] of $X$ in degree $dim(X) + n$:

$$
  Conf(X,S^n)
  \;\simeq\;
  Maps( X, S^{dim(X) + n} )
  \,.
$$


## Examples

### Classifying space of the symmetric group

Let $X= \mathbb{R}^\infty$. Then 

* the _unordered_ configuration space of $n$ points in $\mathbb{R}^\infty$ is a model for the [[classifying space]] $B \Sigma(n)$ of the [[symmetric group]] $\Sigma(n)$;

  (e.g. [Bödigheimer 87, Example 10](#Boedigheimer87))


* the _ordered_ configuration space of $n$ points, equipped with the canonical $\Sigma(n)$-[[action]], is a model for the $\Sigma(n)$-[[universal principal bundle]].

### James construction

The [[James construction]] of $X$ is [[homotopy equivalence|homotopy equivalent]] to the [[configuration space (mathematics)|configuration space]] $C(\mathbb{R}^1, X)$ of points in the [[real line]] with "[[charges]]" taking values in $X$.

(e.g. [Bödigheimer 87, Example 9](#Boedigheimer87))


## References

### General

Review includes 

* {#FrancisLect17} [[John Francis]], _The H-Principle Lecture 17: The sheaf oof configuration spaces and the scanning map_ ([pdf](http://math.northwestern.edu/~jnkf/classes/hprin/17configmapping.pdf))


* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf))


See also

* Edward Fadell, Lee Neuwirth, _Configuration spaces_
Math. Scand. __10__ (1962) 111-118, [MR141126](http://www.ams.org/mathscinet-getitem?mr=141126), [pdf](http://www.mscand.dk/article.php?id=1623)

* [[Graeme Segal]], _Configuration-spaces and iterated loop-spaces_, Invent. Math. __21__ (1973), 213&#8211;221. MR 0331377 ([pdf](http://dodo.pdmi.ras.ru/~topology/books/segal.pdf))


* {#McDuff75} [[Dusa McDuff]], _Configuration spaces of positive and negative particles_, Topology Volume 14, Issue 1, March 1975, Pages 91-107 (<a href="https://doi.org/10.1016/0040-9383(75)90038-5">doi:10.1016/0040-9383(75)90038-5</a>)


* [[Craig Westerland]], _Configuration spaces in geometry and topology_, 2011, [pdf](https://www.austms.org.au/Publ/Gazette/2011/Nov11/TechPaperWesterland.pdf)


* Edward R. Fadell, Sufian Y. Husseini, _Geometry and topology of configuration spaces_, Springer Monographs in Mathematics (2001), [MR2002k:55038](http://www.ams.org/mathscinet-getitem?mr=2002k:55038), xvi+313 pp.

* F. R. Cohen, [[Sam Gitler|S. Gitler]], _On loop spaces of configuration spaces_, Trans. Amer. Math. Soc. __354__ (2002), no. 5, 1705&#8211;1748, [MR2002m:55020](http://www.ams.org/mathscinet-getitem?mr=1881013)

### In Goodwillie-calculus
 {#ReferencesInGoodwillieCalculus}

The configuration spaces of a space $X$ appear as the [[Goodwillie derivatives]] of its [[mapping space]]/[[nonabelian cohomology]]-[[functor]] $Maps(X,-)$:


* {#Arone99} [[Greg Arone]], _A generalization of Snaith-type filtration_, Transactions of the American Mathematical Society 351.3 (1999): 1123-1150. ([pdf](https://www.ams.org/journals/tran/1999-351-03/S0002-9947-99-02405-8/S0002-9947-99-02405-8.pdf))

* {#Ching05} [[Michael Ching]], _Calculus of Functors and Configuration Spaces_, Conference on Pure and Applied Topology Isle of Skye, Scotland, 21-25 June, 2005 ([pdf](https://www3.amherst.edu/~mching/Work/skye.pdf))


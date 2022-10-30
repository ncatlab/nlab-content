# Contents #
* table of contents 
{: toc}

## Idea 

__Matroid__ is one of the basic structures of combinatorics with several different ways of encoding/defining and presenting a general notion of "independence", e.g., linear independence in a vector space, algebraic independence in a field extension. There is also a similar concept of an [[oriented matroid]]; every oriented matroid has an underlying matroid. 

## Definitions 

+-- {: .num_defn} 
###### Definition 
A **matroid** on a set $X$ is a [[Moore closure|closure operator]] $C: P(X) \to P(X)$ satisfying the _exchange axiom_: if $a \in C(S \cup\{b\}) \cap \neg C(S)$, then $b \in C(S \cup\{a\}) \cap \neg C(S)$. 
=-- 

Usually when speaking of matroids, $X$ is taken to be a finite set. A typical example is $X$ some finite subset of a vector space $V$, taking $C(S) \coloneqq X \cap Span(S)$ for any $S \subseteq X$. 

Under this definition, a subset $S \subseteq X$ is _independent_ if there is a strict inclusion $C(T) \subset C(S)$ for every strict inclusion $T \subset S$. Again under this definition, $S$ is a _basis_ if $C(S) = X$ and $S$ is independent. A _hyperplane_ is a closed subset $S$ (meaning $C(S) = S$) that is maximal among proper closed subsets of $X$. It is possible to axiomatize the notion of matroid by taking bases as the primitive notion, or independent sets as the primitive notion, or hyperplanes as the primitive notion, etc. -- Rota speaks of _cryptomorphism_ between these differing presentations. 

## Mnev's theorem 

Mn&#235;v's universality theorem says that any [[semialgebraic set]] in $\mathbb{R}^n$ defined over integers is stably equivalent to the realization space of some oriented matroid.

* wikipedia [matroid](http://en.wikipedia.org/wiki/Matroid), [Mn&#235;v's universality theorem](http://en.wikipedia.org/wiki/Mnev%27s_universality_theorem), [oriented matroid](http://en.wikipedia.org/wiki/Oriented_matroid)
* Hassler Whitney, _On the abstract properties of linear dependence_, American Journal of Mathematics (The Johns Hopkins University Press) 57 (3): 509&#8211;533, 1935, [jstor](http://jstor.org/stable/2371182), [MR1507091](http://www.ams.org/mathscinet-getitem?mr=1507091)
* J. Oxley, _What is a matroid_, [pdf](http://www.math.lsu.edu/~oxley/survey4.pdf)
* James G. Oxley, _Matroid theory_, Oxford Grad. Texts in Math. 1992, 2010
* some papers on Coxeter matroids [html](http://www.math.ufl.edu/~white/cox.html)
* MathOverflow question [Mn&#235;v's universality corollaries, quantitative versions](http://mathoverflow.net/questions/72154/mnevs-universality-corollaries-quantitative-versions) 
* Eric Katz, Sam Payne, _Realization space for [[tropical geometry|tropical]] fans_, [pdf](http://users.math.yale.edu/~sp547/pdf/Realization-spaces.pdf)
* Nikolai E. Mnev, _The universality theorems on the classification problem of configuration varieties and convex polytopes varieties_, pp. 527-543, in "Topology and geometry: Rohlin Seminar." Edited by O. Ya. Viro. Lecture Notes in Mathematics, __1346__, Springer 1988; _A lecture on universality theorem_ (in Russian) [pdf](http://club.pdmi.ras.ru/~panina/9.pdf)
* Talal Ali Al-Hawary, _Free objects in the category of geometries_, [pdf](http://www.emis.de/journals/HOA/IJMMS/Volume26_12/770.pdf)
* Talal Ali Al-Hawary, D. George McRae, _Toward an elementary axiomatic theory of the category of LP-matroids_, Applied Categorical Structures __11__: 157&#8211;169, 2003, [doi](http://dx.doi.org/10.1023/A:1023557229668)
* Hirokazu Nishimura, Susumu Kuroda, _A lost mathematician, Takeo Nakasawa: the forgotten father of matroid theory_ 1996, 2009
* William H. Cunningham, _Matching, matroids, and extensions_, Math. Program., Ser. B __91__: 515&#8211;542 (2002) [doi](http://dx.doi.org/10.1007/s101070100256)
* L. Lov&#225;sz, _Matroid matching and some applications_, J. Combinatorial Theory B __28__, 208&#8211;236 (1980)
* A. Bj&#246;rner, M. Las Vergnas, B. Sturmfels, N. White, G.M. Ziegler,  _Oriented matroids_, Cambridge Univ. Press 1993, 2000, [view at reslib.com](http://reslib.com/book/Oriented_Matroids)
[[!redirects matroids]]
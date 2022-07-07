
#Contents#
* table of contents
{:toc}

## Idea

The _Chow groups_ of a [[noetherian scheme]] $X$ are the analogs of the [[singular homology]] groups of a [[topological space]].

## Definition

Let $X$ be a [[noetherian scheme]].  One defines the **$k$-th Chow group** of $X$ as the [[quotient]] of the group $Z_k(X)$ of [[algebraic cycles]] of [[dimension]] $k$ by the [[subgroup]] of [[algebraic cycles]] [[rational equivalence|rationally equivalent]] to zero:

$$ CH_k(X) \coloneqq Z_k(X) / \sim_{\rat} $$

The **Chow ring** is the [[graded ring]] which is the [[direct sum]] of the Chow groups, with multiplication being the [[intersection product]].

More generally one can use any [[adequate equivalence relation]] $\sim$ (e.g. $\sim_{num}, \sim_{hom}, \sim_{alg}$) in place of rational equivalence, to get groups

$$ CH^{\sim}_k(X) = Z_k(X) / \sim $$

## Cohomological interpretation

Chow groups appear as the [[cohomology groups]] of [[motivic cohomology]] (see there for details) with [[coefficients]] in suitable [[Eilenberg-MacLane objects]].  

## Related concepts

* [[arithmetic Chow group]]
* [[adequate equivalence relation]]
* [[Chow motive]]


## References

Named after [[Wei-Liang Chow]].

The canonical reference is

* [[William Fulton]], _Intersection theory_, 1998.  Ergebnisse der Mathematik und ihrer Grenzgebiete. 3. Folge. A Series of Modern Surveys in Mathematics, 2, Berlin, New York: Springer-Verlag

The original references are

* [[Pierre Samuel]], _Rational Equivalence of Arbitrary Cycles_. American Journal of Mathematics, Vol. 78, No. 2 (Apr., 1956), pp. 383-400

* [[Claude Chevalley]], _Les classes d'equivalence rationnelles I_. S&#233;minaire Claude Chevalley, 3 (1958), Exp. No. 2, 14 (on [NUMDAM](http://www.numdam.org/item?id=SCC_1958__3__A2_0))

* [[Claude Chevalley]], _Les classes d'&#233;quivalence rationnelle, II_. S&#233;minaire Claude Chevalley, 3 (1958), Exp. No. 3, 18 (on [NUMDAM](http://www.numdam.org/numdam-bin/item?id=SCC_1958__3__A3_0))


The most general treatment can be found in the [[The Stacks Project]]:

* [[Aise Johan de Jong]] et. al., [[The Stacks Project]], chapter 38, _Chow Homology and Chern Classes_ ([URL](https://stacks.math.columbia.edu/tag/02P3))

See also

* Wikipedia, *[Chow group](https://en.wikipedia.org/wiki/Chow_group)*

Informal lecture notes by [[Jacob Murre]]:

* [[Jacob Murre]], _Lectures on algebraic cycles and Chow groups_.  Summer school on Hodge theory and related topics, ICTP, 2010.  [PDF](http://jfresan.files.wordpress.com/2010/11/lectures-murre.pdf)

A concise definition of the notion of Chow group and related concepts is in 

* [this pdf](http://www.math.utah.edu/vigre/minicourses/algebra/spiroff3.pdf) from some [Vigre minicours](http://www.math.utah.edu/vigre/minicourses/) (???) 

[[!redirects Chow groups]]
[[!redirects Chow ring]]
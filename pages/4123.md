
> This page is about a property of [[Cech nerves]] in [[homotopy theory]]. For the "nerve theorem" in [[category theory]] see at _[[Segal conditions]]_. For the "nerve theorem" for [[monads with arities]] see [there](monad+with+arities#NerveTheorem).

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **nerve theorem** asserts that the [[homotopy type]] of a sufficiently nice [[topological space]] is encoded in the [[Cech nerve]] of a [[good cover]].

This can be seen as a special case of some aspects of [[étale homotopy]] as the &#233;tale homotopy type of nice spaces coincides with the homotopy type of its Cech nerve.

## Statement

+-- {: .num_theorem}
###### Theorem

Let $X$ be a [[paracompact space]] and $\{U_i \to X\}$ a [[good open cover]]. Write $C(\{U_i\})$ for the [[Cech nerve]] of this cover

$$
  C(\{U_i\}) = \left(
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}\coprod_{i,j} U_i \cap U_j \stackrel{\longrightarrow}{\longrightarrow} \coprod_{i} U_i
  \right)
  \,,
$$

(a [[simplicial object|simplicial]] [[space]]) and write 

$$
  \tilde C(\{U_i\}) = \left(
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}\coprod_{i,j} * \stackrel{\longrightarrow}{\longrightarrow} \coprod_{i} *
  \right)
$$

for the [[simplicial set]] obtained by replacing in $C(\{U_i\})$ each [[direct sum]]mand space by the [[point]]. Let $|\tilde C(\{U_i\})|$ be the [[geometric realization]]. 

This is [[homotopy equivalence|homotopy equivalent]] to $X$.

=--

The proof relies on the existence of [[partitions of unity]].

This is usually attributed to ([Borsuk 1948](#Borsuk48)). It appears more explicitly as [Weil 52, p. 141](#Weil52) [McCord 67, Thm. 2](#McCord67), review in [Hatcher, prop. 4G.3](#Hatcher).

+-- {: .num_remark}
###### Remark

This statement implies that in the [[cohesive (∞,1)-topos]] [[ETop∞Grpd]] the intrinsic [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] coincides with the ordinary [[fundamental ∞-groupoid]] functor of [[paracompact topological spaces]]. See <a href="http://ncatlab.org/nlab/show/Euclidean-topological+infinity-groupoid#GeometricHomotopy">Euclidean-topological ∞-groupoid : Geometric homotopy</a> for details.

=--

## References

Original references:

* {#Borsuk48} [[Karol Borsuk]], _On the imbedding of systems of compacta in simplicial complexes_ , Fund. Math. 35, (1948) 217&#8211;234 ([dml:213158](https://eudml.org/doc/213158))

* [[Jean Leray]], _L'anneau spectral et l'anneau filtr&#233; d'homologie d'un espace localement compact et d'une application continue_, J. Math. Pures Appl. (9) 29 (1950), 1&#8211;139.

* {#Weil52} [[André Weil]], &#167;6. in: _Sur les theoremes de de Rham_, Comment. Math. Helv. 26 (1952), 119&#8211;145 ([dml:139040](https://eudml.org/doc/139040))


* {#McCord67} [[Michael C. McCord]], _Homotopy type comparison of a space with complexes associated with its  open covers_, Proc. Amer. Math. Soc. 18 (1967), 705&#8211;708 ([jstor:2035443](https://www.jstor.org/stable/2035443))

* [[Graeme Segal]],  &#167;4 in: _Classifying spaces and spectral sequences_, Inst. Hautes &#201;tudes Sci. Publ. Math. 34 (1968), 105&#8211;112. 

* [[Armand Borel]] and [[Jean-Pierre Serre]], Theorem&#160;8.2.1. in: _Corners and arithmetic groups_,
Comment. Math. Helv. 48 (1973), 436&#8211;491.

A version for hypercovers is discussed in

* [[Daniel Dugger]], [[Daniel C. Isaksen]], _Topological hypercovers and $\mathbb{A}^1$-realizations_, Math. Z. 246 (2004), no. 4, 667&#8211;689

A review appears as corollary 4G.3 in the textbook

* {#Hatcher} [[Allen Hatcher]], _Algebraic topology_ ([web](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)) .


Some slightly stronger statements are discussed in

* Anders Bj&#246;rner, _Nerves, fibers and homotopy groups_, Journal of combinatorial theory, series A, 102 (2003), 88-93

* Andrzej Nag&#243;rko, _Carrier and nerve theorems in the extension theory_, Proc. Amer. Math. Soc.  135  (2007), 551-558.  ([web](http://www.ams.org/journals/proc/2007-135-02/S0002-9939-06-08477-2/home.html))

A nerve theorem for categories:

* Kohei Tanaka, _Cech complexes for covers of small categories_, Homology, Homotopy and Applications 19(1), (2017), pp. 281-291. [arXiv:1508.03688](https://arxiv.org/abs/1508.03688)

[[!redirects nerve theorems]]

[[!redirects Borsuk's nerve theorem]]

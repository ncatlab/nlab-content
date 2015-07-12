
This page is about a property of [[?ech nerves]] in [[homotopy theory]]. For the "nerve theorem" in [[category theory]] see at _[[Segal conditions]]_.

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
    \stackrel{\to}{\stackrel{\to}{\to}}\coprod_{i,j} U_i \cap U_j \stackrel{\to}{\to} \coprod_{i} U_i
  \right)
  \,,
$$

(a [[simplicial object|simplicial]] [[space]]) and write 

$$
  \tilde C(\{U_i\}) = \left(
    \stackrel{\to}{\stackrel{\to}{\to}}\coprod_{i,j} * \stackrel{\to}{\to} \coprod_{i} *
  \right)
$$

for the [[simplicial set]] obtained by replacing in $C(\{U_i\})$ each [[direct sum]]mand space by the [[point]]. Let $|\tilde C(\{U_i\})|$ be the [[geometric realization]]. 

This is [[homotopy equivalence|homotopy equivalent]] to $X$.

=--

This is usually attributed to ([Borsuk1948](#Borsuk)). The proof relies on the existence of [[partitions of unity]] (see for instance the review [Hatcher, prop. 4G.2](#Hatcher)).

+-- {: .num_remark}
###### Remark

This statement implies that in the [[cohesive (∞,1)-topos]] [[ETop∞Grpd]] the intrinsic [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] coincides with the ordinary [[fundamental ∞-groupoid]] functor of [[paracompact topological spaces]]. See <a href="http://ncatlab.org/nlab/show/Euclidean-topological+infinity-groupoid#GeometricHomotopy">Euclidean-topological ∞-groupoid : Geometric homotopy</a> for details.

=--

## References

Some earlier references on the nerve theorem include

* [[K. Borsuk]], _On the imbedding of systems of compacta in simplicial complexes_ , Fund. Math. 35, (1948) 217&#8211;234
{#Borsuk}

* [[Jean Leray]], _L'anneau spectral et l'anneau filtr&#233; d'homologie d'un espace localement compact et d'une application continue_, J. Math. Pures Appl. (9) 29 (1950), 1&#8211;139.

* [[André Weil]], _Sur les theoremes de de Rham_, Comment. Math. Helv. 26 (1952), 119&#8211;145.
(See &#167;6.)

* [[Michael C. McCord]], _Homotopy type comparison of a space with complexes associated with its  open covers_, Proc. Amer. Math. Soc. 18 (1967), 705&#8211;708.

* [[Graeme Segal]], _Classifying spaces and spectral sequences_, Inst. Hautes &#201;tudes Sci. Publ. Math. 34 (1968), 105&#8211;112.  (See &#167;4.)

* [[Armand Borel]] and [[Jean-Pierre Serre]],
_Corners and arithmetic groups_,
Comment. Math. Helv. 48 (1973), 436&#8211;491.
(See Theorem&#160;8.2.1.)

A version for hypercovers is discussed in

* [[Daniel Dugger]], [[Daniel C. Isaksen]],
_Topological hypercovers and $\mathbb{A}^1$-realizations_,
Math. Z. 246 (2004), no. 4, 667&#8211;689.

A review appears as corollary 4G.3 in the textbook

* [[Allen Hatcher]], _Algebraic topology_ ([web](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)) .
{#Hatcher}

Some slightly stronger statements are discussed in

* Anders Bj&#246;rner, _Nerves, fibers and homotopy groups_ , Journal of combinatorial theory, series A, 102 (2003), 88-93

* Andrzej Nag&#243;rko, _Carrier and nerve theorems in the extension theory_ Proc. Amer. Math. Soc.  135  (2007), 551-558.  ([web](http://www.ams.org/journals/proc/2007-135-02/S0002-9939-06-08477-2/home.html))

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
* automatic table of contents goes here
{:toc}

## Idea

The **nerve theorem** asserts that the [[homotopy type]] of a sufficiently nice [[topological space]] is encoded in the [[Cech nerve]] of a [[good cover]].

## Statement

+-- {: .un_theorem}
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

This is usually attributed to ([Borsuk1948](#Borsuk)).

+-- {: .un_remark}
###### Remark

This statement implies that in the [[cohesive (∞,1)-topos]] [[ETop∞Grpd]] the intrinsic [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] coincides with the ordinary [[fundamental ∞-groupoid]] functor of [[paracompact topological spaces]]. See <a href="http://ncatlab.org/nlab/show/Euclidean-topological+infinity-groupoid#GeometricHomotopy">Euclidean-topological ∞-groupoid : Geometric homotopy</a> for details.

=--

## References

The nerve theorem is usually attributed to

* K. Borsuk, _On the imbedding of systems of compacta in simplicial complexes_ , Fund. Math 35, (1948) 217-234
{#Borsuk}

A review appears as corollary 4G.3 in the texbook

* [[Allen Hatcher]], _Algebraic topology_ ([web](http://www.math.cornell.edu/~hatcher/AT/ATpage.html)) .

Some slightly stronger statements are discussed in

* Anders Bj&#246;rner, _Nerves, fibers and homotopy groups_ , Journal of combinatorial theory, series A, 102 (2003), 88-93



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

The relative version of a locally compact topological space is a continuous map that behaves like a 'family of locally compact spaces'.

## Definition

+-- {: .num_defn #ProperContinuous}
###### Definition

A [[continuous function]] $f  \colon X \to Y$ is called _locally proper_ if for any $x \in X$ and [[neighbourhood]] $V \ni x$ there is a neighbourhood $A\ni x$ with $A \subset V$ and a neighbourhood $U \ni f(x)$ such that $A \to U$ is a [[proper map]].

=--

## Examples

* The inclusion map of a locally closed subset $C\hookrightarrow X$ in a topological space $X$ is locally proper.

* A topological space $X$ is a [[locally compact space]] if and only if $X\to \ast$ is locally proper.

## Properties

+-- {: .num_prop }
###### Proposition

Let $f\colon X\to Y$ and $g\colon Y\to Z$ be locally proper. Then $g\circ f$ is locally proper. If $W\to Y$ is any continuous function then $W\times_Y Z \to W$ is locally proper. (ie locally proper maps are closed under composition and stable under pullback. Hence they form a singleton [[coverage]])

=--

As a corollary, one has that for a locally compact space $X$, every locally closed
subspace of $X$ is locally compact.

+-- {: .num_prop }
###### Proposition

Let $f\colon X\to Y$ be a continuous function. Then if

* there is an open covering $\mathcal{U} = \{U_i\}$ of $X$ such that $f\big|_{U_i} \colon U_i \to Y$ is locally proper for all $i$,

or

* there is an open covering $\mathcal{V} = \{V_j\}$ of $Y$ such that $f^{-1}(V_j) \to V_j$ is locally proper for all $j$,

then $f$ is locally proper. The converse implications also hold

=--




Recall that a continuous map $g\colon Y \to Z$ of topological spaces is called _separated_ if $Y\to Y\times_Z Y$ is a closed embedding.

+-- {: .num_prop }
###### Proposition

If $f\colon X\to Y$ and $g\colon Y\to Z$ are continuous maps, $g$ is separated and $g\circ f$ is locally proper, then $f$ is locally proper

=--

+-- {: .num_prop }
###### Corollary

Every continuous map from a [[locally compact]] [[Hausdorff space]] to a Hausdorff space is separated and locally proper.

=--

The following proposition generalises the well-known result that compact Hausdorff spaces are locally compact.

+-- {: .num_prop }
###### Proposition

Every ([[separated map|separated]]) [[proper map]] is locally proper

=--

The [[proper base change theorem]] also holds for locally proper maps if one uses [[direct image with compact support]] instead of ordinary [[direct image]]

## Related Entries

* [[proper map]]

* [[locally compact space]]

* [[direct image with compact support]]

## References

* Olaf M. Schnürer and Wolfgang Soergel, _Proper base change for separated locally proper maps_,  Rend. Sem. Mat. Univ. Padova **135** (2016) pp 223-250. doi:[10.4171/RSMUP/135-13](https://doi.org/10.4171/RSMUP/135-13), arXiv:[1404.7630](https://arxiv.org/abs/1404.7630)
* Günther Richter and Alexander Vauth, _Fibrewise sobriety_, in: Categorical structures and their applications. Proceedings of the North-West European category seminar, Berlin, Germany, March 28--29, 2003. River Edge, NJ: World Scientific. 265--283 (2004; Zbl 1065.18003). doi:[10.1142/9789812702418_0020](https://doi.org/10.1142/9789812702418_0020)

[[!redirects locally proper]]

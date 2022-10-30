
#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

Let $\mathcal{T}$ be a [[triangulated category]] with [[coproducts]]. Then $\mathcal{T}$ is **compactly generated** if there is a set $\mathcal{G}$ of objects of $\mathcal{T}$ such that

1. Whenever $X$ is an object such that $\mathcal{T}(\Sigma^m G, X) = 0$ for all $G \in \mathcal{G}$ and $m \in \mathbb{Z}$, then $X = 0$.

1. All objects in $\mathcal{G}$ are [[compact object|compact]] i.e. for all $G \in \mathcal{G}$ and for every family $\{ X_i \mid i \in I\}$ of objects of $\mathcal{T}$
$$
\coprod_{i \in I} \mathcal{T}(G, X_i) \to \mathcal{T}(C,\coprod_{i \in I} X_i)
$$
is an isomorphism.

=--

## Properties

+-- {: .num_prop}
###### Proposition

If $\mathcal{T}$ is a triangulated category with coproducts, then a set of objects $\mathcal{G}$ satisfies the two above conditions if and only if the smallest [[localizing subcategory]] of $\mathcal{T}$ that contains $\mathcal{G}$ is $\mathcal{T}$ itself.

=--

+-- {: .proof}
###### Proof

Lemma 2.1.1. of

* Schwede, Stefan; Shipley, Brooke _Stable model categories are categories of modules._

=--

## Examples

* The [[sphere spectrum]] is a compact generator for the [[stable homotopy category]].

=--

## Related concepts

* [[well-generated triangulated category]]

=--

## References

* Schwede, Stefan; Shipley, Brooke _Stable model categories are categories of modules._ Topology 42 (2003), no. 1, 103&#8211;153.
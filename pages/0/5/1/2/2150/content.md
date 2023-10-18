
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition 

Let $X$ be a [[paracompact space|paracompact]] [[Hausdorff space]]. A [[sheaf]] $F$ of [[groups]] over $X$ is __fine__ if for every two disjoint closed subsets $A,B\subset X$, $A\cap B = \emptyset$, there is an [[endomorphism]] of the sheaf of groups $F\to F$ which restricts to the identity in a neighborhood of $A$ and to the $0$ endomorphism in a neighborhood of $B$. Every fine sheaf is [[soft sheaf|soft]].

A slightly different definition is given in Voisin, in _Hodge Theory and Complex Algebraic Geometry I_ (Definition 4.35):

A __fine sheaf__ $\mathcal{F}$ over $X$ is a sheaf of $\mathcal{A}$-[[modules]], where $\mathcal{A}$ is a sheaf of [[rings]] such that, for every [[open cover]] $U_i$ of $X$, there is a [[partition of unity]] $1 = \sum f_i$ (where the sum is locally finite) subordinate to this covering.

Another definition is given by [Godement 1958](#Godement58)
(the paragraph after Theorem II.3.7.2):
a sheaf $F$ is __fine__ if the [[internal hom]] $Hom(F,F)$ is a [[soft sheaf]].

## Properties

* For any fine sheaf $J$ over a paracompact Hausdorff space $M$, the [[sheaf cohomology]] groups of positive degree $j$ are all trivial

$$
H^j(M,J) = 0.
$$

* Any sheaf $S$ [[abelian sheaf|of abelian groups]] admits a [[resolution]] by fine sheaves $\{J_i\}$

$$
0\to S\to J_0\to J_1\to \cdots
$$

These resolutions can be used to compute the sheaf cohomology groups of $S$ in terms of the induced maps of sections

$$
d_i^*: \Gamma(M,J_i)\to\Gamma(M,J_{i+1}).
$$

as

$$
H^q(M,S) \cong (\text{ker}d^*_{q})/(\text{im}d^*_{q-1})
$$

(see Section 3 of [Gunning (1966)](#Gun66).).

## Related concepts

* [[sheaf]]

* [[abelian sheaf cohomology]]

  * [[soft sheaf]]

  * [[flabby sheaf]]

## References


* {#Godement58} [[Roger Godement]], *Topologie algébrique et theorie des faisceaux*, Actualités Sci. Ind. **1252**, Hermann, Paris (1958) &lbrack;[webpage](https://www.editions-hermann.fr/livre/topologie-algebrique-et-theorie-des-faisceaux-roger-godement), [[Godement-TopologieAlgebrique.pdf:file]]&rbrack;

* {#Gun66} Robert C. Gunning. *Lectures on Riemann Surfaces*. Princeton University Press (1966).

category: sheaf theory
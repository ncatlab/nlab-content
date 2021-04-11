
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A common condition on [[subgroups]] of a [[topological group]] is that they be [[closed subspaces|closed]]. 

This is typically required in [[equivariant differential topology]]/[[equivariant homotopy theory]], for instance in the definition of the [[orbit category]].

## Definition

\begin{defn}\label{ClosedSubgroup}
**(closed subgroup)**\linebreak

A [[topological group|topological]] [[subgroup]] $H \subset G$ of a [[topological group]] $G$ is called a _closed subgroup_ if as a [[topological subspace]] it is a [[closed subspace]].

\end{defn}

+-- {: .num_lemma #OpenSubgroupOfTopologicalGroupIsClosed}
###### Lemma
**(open subgroups of topological groups are closed)**

Every [[open subset|open]] [[subgroup]] $H \subset G$ of a topological group is [[closed subset|closed]], hence a [[closed subgroup]].

=--

(e.g [Arhangel'skii-Tkachenko 08, theorem 1.3.5](#ArhangelskiiTkachenko08))

+-- {: .proof}
###### Proof

The [[set]] of $H$-[[cosets]] is a [[cover]] of $G$ by [[disjoint subsets|disjoint]] [[open subsets]]. One of these cosets is $H$ itself and hence it is the [[complement]] of the [[union]] of the other cosets, hence the complement of an open subspace, hence closed.

=--



## Examples

### Stabilizer subgroup

\begin{prop}\label{StabilizerSubgroupsOfContinuousActionsOnT1SpacesAreClosed}
**([[stabilizer subgroups]] of [[topological G-space|continuous actions]] on [[T1-spaces]] are closed)**
  Let $G$ be a [[topological group]] and let $X \in G Actions(TopologicalSpaces)$ a [[topological G-space]] whose underlying [[topological space]] is a [[T1-space]], e.g. a [[Hausdorff space]].

Then for all [[points]] $x \in X$  their [[isotropy groups]], hence their [[stabilizer subgroup]]

  $$
    G_x 
    \;\coloneqq\;
    Stab_G(x)
    \;\subset\;
    G
    \,,
  $$

  is a closed subgroup (Def. \ref{ClosedSubgroup}).

\end{prop}
\begin{proof}
  We may understand $G_x$ as the [[pre-image]] 

$$
  G_x 
  \;\simeq\;
  \big(
    \rho(-)(x)
  \big)^{-1}
  \big(
    \{x\}
  \big)
$$

of the [[singleton set|singleton]] [[subset]] $\{x\} \subset X$ under the [[continuous function]] which sends $x$ to its [[image]] under the given $G$-[[action]]:

$$
  \array{
    G 
    &\overset{\rho(-)(x)}{\longrightarrow}&
    X
    \\
    g &\mapsto& g \cdot x
    \,.
  }
$$

Since this is a [[continuous function]], and since $x \in X$ is a [[closed point]] by assumption that $X$ is [[T1 topological space|T1]], hence since $\{x\} \subset X$ is a [[closed subset]], it follows that $G_x \subset G$ is a closed subset, since [continuous preimages of closed subsets are closed](continuous+map#PropertiesPreservedByAContinuousFunction).


\end{proof}


### Localic subgroups

Any localic subgroup of a [[localic group]] is closed (see [this Theorem](https://ncatlab.org/nlab/show/localic+group#LocalicSubgroupsAreClosed)).


## Properties

### Local sections over coset space


\begin{prop}\label{CosetSpaceCoprojectionsWithLocalSections}
**([[coset space coprojections with local sections]])**\linebreak
Let $G$ be a [[topological group]] and $H \subset G$ a [[subgroup]].

Sufficient conditions for the [[coset space]] [[coprojection]] $G \overset{q}{\to} G/H$ to admit [[local sections]], in that there is an [[open cover]] $\underset{i \in I}{\sqcup}U_i \to G/H$ and a [[continuous section]] $\sigma_{\mathcal{U}}$ of the [[pullback]] of $q$ to the cover,

$$
  \array{
    &&
    G_{\vert \mathcal{U}}
    &\longrightarrow&
    G
    \\
    &
    {}^{\mathllap{
      \exists \sigma
    }}
    \nearrow
    &
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow 
    \\
    \mathllap{ \exists \; } 
    \underset{i \in I}{\sqcup} U_i    
    &=&
    \underset{i \in I}{\sqcup} U_i
    &\longrightarrow&
    G/H
    \mathrlap{\,,}
  }
$$

include the following:

* $G$ is any [[topological group]] 

  and $H$ is a [[compact Lie group]]

  (in particular for $H$ a [[closed subgroup]] if $G$ itself is a [[compact Lie group]], since [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]).

  ([Gleason 50, Thm. 4.1](#Gleason50))


or:

* The underlying [[topological space]] of $G$ is

  1. [[locally compact topological space|locally compact]];

  1. [[separable metric space]];

  1. of [[finite number|finite]] [[dimension of a separable metric space]]

  (e.g. if $G$ is a [[Lie group]])

  and $H \subset G$ is a [[closed subgroup]].

  ([Mostert 53, Theorem 3](#Mostert53))


\end{prop}




## Related concepts

* [[maximal compact subgroup]]

* [[locally compact topological group]]

* [[compact Lie group]]

## References

* {#Gleason50} [[Andrew Gleason]], _Spaces With a Compact Lie Group of Transformations_, Proceedings of the American Mathematical Society Vol. 1, No. 1 (Feb., 1950), pp. 35-43 ([jstor:2032430](https://www.jstor.org/stable/2032430), [doi:10.2307/2032430](https://doi.org/10.2307/2032430))

* {#Mostert53} [[Paul Mostert]], _Local Cross Sections in Locally Compact Groups_, Proceedings of the American Mathematical Society, Vol. 4, No. 4 (Aug., 1953), pp.645-649 ([jstor:2032540](https://www.jstor.org/stable/2032540), [doi:10.2307/2032540](https://doi.org/10.2307/2032540))

* {#ArhangelskiiTkachenko08} Alexander Arhangel'skii, Mikhail Tkachenko, _Topological Groups and Related Structures_, Atlantis Press 2008 ([doi:10.2991/978-94-91216-35-0](https://doi.org/10.2991/978-94-91216-35-0))


[[!redirects closed subgroups]]
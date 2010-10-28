
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition

Suppose $X$ is a [[set]], $\{ (X_i, T_i) \}_{i \in I}$ a [[family]] of [[topological space]]s and $\{ f_i \}_{i \in I}$ a family of [[function]]s from $X$ to the family $\{ X_i \}_{i \in I}$. That is, for each index $i \in I$, $f_i\colon X \to X_i$. Let $\Gamma$ be the set of all topologies $\tau$ on $X$ such that $f_i$ is a [[continuous map]] for every $i \in I$. Then the [[intersection]] $\bigcap_{\tau \in \Gamma} \tau$ is again a topology and also belongs to $\Gamma$. Clearly, it is the coarsest/weakest topology $\tau_0$ on $X$ such that each function $f_i: X \to X_i$ is a [[continuous map]].

We call $\tau_0$ the **weak/coarse/initial topology induced** on $X$ by the family of mappings $\{ f_i \}_{i \in I}$.  Note that all terms 'weak topology', 'initial topology', and 'induced topology' are used.  The [[subspace topology]] is a special case, where $I$ is a [[singleton]] and the unique function $f_i$ is an [[injection]].


## Generalisations

We can perform the above construction in any [[topological concrete category]], where it is a special case of an [[initial structure]] for a [[source|sink]].

The dual situtation is forming the [[strong topology]] on $X$ when equipped with a family of functions *to* $X$ from topological spaces.  (This generalises to forming a [[final structure]] for a [[sink]].)


## References

The original version of this article was posted by [[Vishal Lama]] at [[nlabmeta:induced topology]].


[[!redirects weak topology]]
[[!redirects weak topologies]]
[[!redirects coarse topology]]
[[!redirects coarse topologies]]
[[!redirects initial topology]]
[[!redirects initial topologies]]

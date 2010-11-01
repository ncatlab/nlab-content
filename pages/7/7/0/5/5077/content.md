
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


## In functional analysis

In [[functional analysis]], the term 'weak topology' is used in a special way.  If $V$ is a [[topological vector space]] over the [[ground field]] $K$, then we may consider the continuous linear [[functional]]s on $V$, that is the [[continuous map|continuous]] [[linear maps]] from $V$ to $K$.  Taking $V$ to be the set $X$ in the general definition above, taking each $T_i$ to be $K$, and taking the continuous linear functionals on $V$ to comprise the family of functions, then we get the __weak topology__ on $V$.

The [[weak-star topology]] is another special case of a weak topology.


## References

The original version of this article was posted by [[Vishal Lama]] at [[nlabmeta:induced topology]].


[[!redirects weak topology]]
[[!redirects weak topologies]]
[[!redirects coarse topology]]
[[!redirects coarse topologies]]
[[!redirects initial topology]]
[[!redirects initial topologies]]


> For the strong topology in functional analysis, see at [[strong operator topology]].


***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Induced topologies
* table of contents
{:toc}

## Definitions

Suppose 

1. $S$ is a [[set]], 

1. $\{ (X_i, T_i) \}_{i \in I}$ is a [[family]] of [[topological spaces]] 

1. $\{ f_i \}_{i \in I}$ a family of [[functions]] from $S$ to the family $\{ X_i \}_{i \in I}$. 

That is, for each index $i \in I$, $f_i\colon S \to X_i$. Let $\Gamma$ be the set of all topologies $\tau$ on $S$ such that $f_i$ is a [[continuous map]] for every $i \in I$. Then the [[intersection]] $\bigcap_{\tau \in \Gamma} \tau$ is again a topology and also belongs to $\Gamma$. Clearly, it is the coarsest/weakest topology $\tau_0$ on $X$ such that each function $f_i\colon S \to X_i$ is a [[continuous map]].

We call $\tau_0$ the **weak/coarse/initial topology induced** on $S$ by the family of mappings $\{ f_i \}_{i \in I}$.  Note that all terms 'weak topology', 'initial topology', and 'induced topology' are used.  The [[subspace topology]] is a special case, where $I$ is a [[singleton]] and the unique function $f_i$ is an [[injection]].

Dually, suppose $S$ is a [[set]], $\{ (X_i, T_i) \}_{i \in I}$ a [[family]] of [[topological spaces]] and $\{ f_i \}_{i \in I}$ a family of [[functions]] to $S$ from the family $\{ X_i \}_{i \in I}$. That is, for each index $i \in I$, $f_i\colon X_i \to S$. Let $\Gamma$ be the set of all topologies $\tau$ on $S$ such that $f_i$ is a [[continuous map]] for every $i \in I$. Then the [[intersection]] $\bigcap_{\tau \in \Gamma} \tau$ is again a topology and also belongs to $\Gamma$. Clearly, it is the finest/strongest topology $\tau_0$ on $S$ such that each function $f_i\colon X_i \to S$ is a [[continuous map]].

We call $\tau_0$ the **strong/fine/final topology induced** on $S$ by the family of mappings $\{ f_i \}_{i \in I}$.  Note that all terms 'strong topology', 'final topology', and 'induced topology' are used.  The [[quotient topology]] is a special case, where $I$ is a [[singleton]] and the unique function $f_i$ is a [[surjection]].


## Generalisations

We can perform the first construction in any [[topological concrete category]], where it is a special case of an [[initial structure]] for a [[sink|source or cosink]].

We can also perform the second construction in any [[topological concrete category]], where it is a special case of an [[final structure]] for a [[sink]].


## In functional analysis

In [[functional analysis]], the term 'weak topology' is used in a special way.  If $V$ is a [[topological vector space]] over the [[ground field]] $K$, then we may consider the [[continuous linear functional]]s on $V$, that is the [[continuous map|continuous]] [[linear maps]] from $V$ to $K$.  Taking $V$ to be the set $X$ in the general definition above, taking each $T_i$ to be $K$, and taking the continuous linear functionals on $V$ to comprise the family of functions, then we get the __weak topology__ on $V$.

The _weak-star topology_ on the dual space $V^*$ of continuous linear functionals on $V$ is precisely the weak topology induced by the dual (evaluation) functionals on $V^*$

$$
\left\{V^* \overset{\operatorname{ev}_v}{\to} K, \text{ by } f \mapsto f(v)\right\}_{v \in V}.
$$

For the strong topology in functional analysis, see the [[strong operator topology]].

## Related entries

* [Category of topological spaces -- Universal constructions](Top#UniversalConstructions)

## References

The original version of this article was posted by [[Vishal Lama]] at [[nlabmeta:induced topology]].

See also

* Wikipedia, _[Initial topology](https://en.wikipedia.org/wiki/Initial_topology)_, _[Final topology](https://en.wikipedia.org/wiki/Final_topology)_, 


[[!redirects weak topology]]
[[!redirects weak topologies]]
[[!redirects coarse topology]]
[[!redirects coarse topologies]]
[[!redirects initial topology]]
[[!redirects initial topologies]]

[[!redirects strong topology]]
[[!redirects strong topologies]]
[[!redirects fine topology]]
[[!redirects fine topologies]]
[[!redirects final topology]]
[[!redirects final topologies]]
[[!redirects weak-star topology]]
[[!redirects induced topology]]
[[!redirects induced topologies]]

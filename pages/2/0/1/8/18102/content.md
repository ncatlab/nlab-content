
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

## Definition

+-- {: .num_defn #TopologyFinerCoarser}
###### Definition
**(finer/coarser topologies)**

Let $X$ be a [[set]], and let $\tau_1, \tau_2 \subset P(X)$ be two [[topological space|topologies]] on $X$,
hence two choices of [[open subsets]] for $X$, making it a [[topological space]]. If

$$
  \tau_1 \subset \tau_2
$$

hence if every open subset of $X$ with respect to $\tau_1$ is also regarded as open by $\tau_2$, then 
one says that

* the topology $\tau_2$ is _finer_ than the topology $\tau_1$

* the topology $\tau_1$ is _coarser_ than the topology $\tau_2$.

=--

## Examples

+-- {: .num_example #CoDiscreteTopology}
###### Example
**(discrete and co-discrete topology)**

Let $X$ be any [[set]]. Then there are always the following two extreme
possibilities of equipping $X$ with a topology $\tau \subset P(X)$, and hence making it a [[topological space]]:

1. $\tau \coloneqq P(X)$ the set of _all_ subsets; 

   this is called the _[[discrete topology]]_ on $X$, it is the [[finer topology|finest topology]] (def. \ref{TopologyFinerCoarser}) on $X$,
   
   we write $Disc(X)$ for the resulting topological space;

1. $\tau \coloneqq \{ \emptyset, X \}$ the set contaning only the [[empty set|empty]] subset of $X$ and all of $X$ itself;

   this is called the _[[codiscrete topology]]_ on $X$, it is the [[coarser topology|coarsest topology]] (def. \ref{TopologyFinerCoarser}) on $X$
   
   we write $CoDisc(X)$ for the resulting topological space.
   

=--


## References

* Wikipedia, _[Comparison of topologies](https://en.wikipedia.org/wiki/Comparison_of_topologies)_

[[!redirects finer topologies]]

[[!redirects coarser topology]]
[[!redirects coarser topologies]]


[[!redirects comparison of topologies]]
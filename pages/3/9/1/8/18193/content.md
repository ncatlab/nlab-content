
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

Given a [[set]] $\{X_i\}_{i \in I}$ of [[topological spaces]], then the _box topology_ on the [[Cartesian product]] $\underset{i \in I}{\prod} X_i$ of the underlying sets of these spaces is the [[topological space|topology]] which is generated from the [[topological base]] whose elements are the [[Cartesian products]] 

$$
  \underset{i \in I}{\prod} U_i
  \;\subset\;
  \underset{i\in I}{\prod} X_i
$$


of [[open subsets]] $U_i \subset X_i$ of each of the factor spaces. 


## Properties

### Relation to Tychonoff topology

If the index set $I$ is a [[finite set]], then this box topology coincides with the [[Tychonoff topology]] on the Cartesian product. For general $I$ however the Tychnoff topology has as base open subsets only those products $\underset{i \in I}{\prod} U_i$ for which all but a finite number of factors are in fact the corresponding total space $X_i$.


Hence for non-finite index set $I$ the box topology is strictly [[finer topology|finer]] that the Tychonoff topology. Beware that it is the Tychonoff toopology which yields the actual [[Cartesian product]] in the [[category]] [[Top]] of [[topological spaces]]. Accordingly, for non-finite $I$ the box topology _fails_ to possess the properties that one expects from a categorical product.

For example, there may be a family of continuous functions, $f_i: X \to X_i$, for which the associated map by components, $X \to \underset{i\in I}{\prod} X_i$, is not continuous for the box topology.


## References

* Wikipedia, _[Box topology](https://en.wikipedia.org/wiki/Box_topology)_

[[!redirects box topologies]] 

[[!redirects box product]]
[[!redirects box products]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

Given a [[linearly ordered set]] $(S, \lt)$, its __order topology__ is the [[topological structure|topology]] on $S$ generated from the [[subbase of a topology|sub-basis]] $\beta \subset P(S)$ 

$$
  \beta 
    \coloneqq
  \left\{
    (a,\infty),
    (-\infty,a)
  \right\}_{a \in S}
  \,.
$$ 


whose elements are the "open half rays"

$$
  (a, \infty)
  \coloneqq
  \left\{
    s \in S \,\vert\, a \lt s
  \right\}
    \phantom{AAAA}
  (-\infty, a)
  \coloneqq
  \left\{
    s \in S \,\vert\, s \lt a
  \right\}
  \,.
$$


## Examples

* The usual [[Euclidean space]] [[metric topology]] on the [[real numbers]] is equal to the order topology with respect to the canonical ordering of the real numbers. The analogous statement then holds for the [[rational numbers]] $\mathbb{Q} \subset \mathbb{R}$ equipped with their [[subspace topology]].


## Related concepts

* [[specialization topology]],

* [[Scott topology]]


## References

* Wikipedia, _[Order topology](https://en.wikipedia.org/wiki/Order_topology)_


[[!redirects order topology]]
[[!redirects order topologies]]

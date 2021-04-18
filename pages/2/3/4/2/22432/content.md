

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $n \in \mathbb{N}$, with $Sym(n)$ denoting the [[symmetric group]] on $n$ elements, consider a [[permutation]] $\sigma \;\in\; Sym(n)$ of $n$ elements.

Write 

$$
  \langle \sigma \rangle
  \;\coloneqq\;
  \big\{
    e, 
    \sigma,
    \sigma^2,
    \cdots
    ,
    \sigma^{order(\sigma)-1}
  \big\}
  \;\subset\;
  Sym(n)
$$

for the [[cyclic group]] [[finitely generated group|generated]] by $\sigma$. This cyclic group (whose [[order of a group|order]] is the [[order of a group element|order]] of $\sigma$) canonically [[action|acts]] on the [[set]] $\{1, \cdots, n\}$ through the defining [[group action]] of $Sym(n)$ on this set. 

Then a *cycle* of the [[permutation]] $\sigma$ is an [[orbit]] of $\langle \sigma \rangle$ with respect to this canonical [[group action]] on $\{1, \cdots, n\}$.

More explicitly, this means that a cycle of $\sigma$ is a [[subset]] of the form

$$
  \big\{
    k, \sigma(k), \sigma(\sigma(k)), \cdots 
  \big\}
  \;\subset\;
  \{1,\cdots, n\}
$$

for any $1 \leq k \leq n$. 

Beware that this is really meant as a [[subset]], not as a [[tuple]]. So for instance 

$$
  \big\{
    \sigma(k), \sigma(\sigma(k)), \sigma^3(k)), \cdots 
  \big\}
  \;\subset\;
  \{1,\cdots, n\}
$$

is the same cycle.

The permutation action restricted to the cycle is a [[cyclic permutation]].



## Related concepts

* [[Cayley distance]], [[Kendall distance]]

* [[cyclic permutation]]

* [[orbit]]

## References

See also 

* Wikipedia, *[Cyclic permutation](https://en.wikipedia.org/wiki/Cyclic_permutation)*

* MathWorld, *[Permutation Cycle](https://mathworld.wolfram.com/PermutationCycle.html)*


[[!redirects cycles of a permutation]]

[[!redirects permutation cycle]]
[[!redirects permutation cycles]]



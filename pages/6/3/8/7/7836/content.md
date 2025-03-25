
> This entry is about the concept in [[group theory]]. See at _[[order]]_ for the concept in [[order theory]].

***

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

### Order of a group
 {#OrderOfAGroup}

For $G$ a [[discrete group]], its **order** is the [[cardinality]] of the underlying [[set]].

Hence for $G$ a [[finite group]], its order $\vert G\vert \in \mathbb{N}$ is a [[natural number]], the number of its group elements.

### Order of an element of a group
 {#OrderOfAnElementOfAGroup}

For $G$ a [[group]] and $g \in G$ an [[element]], the **order** of $g$ is the smallest [[positive number|positive]] [[natural number]] $n$ such that the $n$-fold group product of $g$ with itself is the [[neutral element]]:

$$
  order(g) \coloneqq min \{ n \in \mathbb{N}^+ | g^n = e\}
  \,.
$$

The _[[exponent of a group]]_ is the [[least common multiple]] of the order of all elements of the group.

### Order of a group scheme

Sometimes the term ''order'' refers to the [[height of a group scheme|height]] of a ([[group scheme|group]]) [[scheme]] $X$ over a [[field]] (of [[characteristic]] $p$) which is defined to be the dimension of the associated ring of functions $O(X)$ as a $k$-[[vector space]]. Another term for this notion is ''rank''. If this group scheme is moreover [[p-divisible group|p-divisible]] - which means that is is in fact a codirected diagram of [[group scheme|group schemes]] of order $p^{v h}$; in this case $h$ is called the order or height of $X$.

## Properties

For $G$ a [[finite group]] and $g \in G$ an element, there is a close relation between 

1. the order $\vert G\vert$ of $G$ in the sense [above](#OrderOfAGroup);

1. the order $order(g)$ of $g$ the sense [above](#OrderOfAnElementOfAGroup)


### Orders of cyclic subgroups

The element $g$ [[generators and relations|generates]] a [[cyclic group|cyclic]] [[subgroup]] $C_g \subset G$. Evidently, the order of the element $g$ equals the order $\vert C_g \vert$ of this cyclic subgroup that it generates:

\[
  \label{OrderOfElementIsOrderOfGeneratedCyclicGroup}
  order(g) =\vert C_g\vert
  \,.
\]

### Lagrange's theorem

By [[Lagrange's theorem]], if $G$ a [[finite group]] and $H \subset G$ a [[subgroup]], then the order $\vert G\vert$ of $G$ is divisible by the order $\vert H\vert$ of $H$. The multiple is called the [[index of a subgroup|subgroup index]] $[G : H] \in \mathbb{N}$:

$$
  {\vert G\vert}
  \;=\;
  [G : H] \, {\vert H\vert}
  \,.
$$

Hence with (eq:OrderOfElementIsOrderOfGeneratedCyclicGroup) it follows that with $g \in G$ any element, the order of $g$ divides the order of $G$:

$$
  {\vert G\vert}/ order(g)
  \;=\;
  [G : C_g]
  \,.
$$





## Related concepts

* [[exponent of a group]]

* [[p-group]]

## References

See also 

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Order_(group_theory)">Order (group theory)</a>_

[[!redirects order of an element]]

[[!redirects order of a group element]]

[[!redirects group order]]

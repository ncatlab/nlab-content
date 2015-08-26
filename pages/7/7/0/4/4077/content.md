
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

### Standard definition

A **simple group** is a [[group]] $G$ with exactly two [[quotient group]]s: the [[trivial quotient group]] $\{1\} \cong G/G$ and the group $G \cong G/\{1\}$ itself. 

Equivalently, a simple group is a group possessing exactly two [[normal subgroup|normal subgroups]]: the [[trivial subgroup]] $\{1\}$ and the group $G$ itself. One can also say that a normal subgroup is trivial iff it is not $G$, or trivial iff proper (compare the definition in constructive mathematics below).

Note that the [[trivial group]] does not itself count as simple, on the grounds that it has only *one* quotient group (or only one normal subgroup).  It may be possible to find authors that use "at most" in place of "exactly", thereby allowing the trivial group to be simple.  (Compare [[too simple to be simple]].)


### In constructive algebra

In [[constructive mathematics]], we consider a group $G$ equipped with a [[tight apartness]] $\ne$ such that the group operations are [[strongly extensional function|strongly extensional]] and use the theory of [[antisubgroups]] (which classically are the complements of subgroups).  Then $G$ is __simple__ if, given any [[normal antisubgroup]] $N$ of $G$, $N$ is trivial iff it is proper.  Explicitly, this says $N$ owns every nonidentity element (every $x$ such that $x \ne 1$) iff $N$ is [[inhabited subset|inhabited]] (with some $x$ such that necessarily $x \ne 1$).  Replacing 'iff' with 'if' here would allow the trival group to be simple.


## Examples

### Finite simple groups

Simple groups are most commonly encountered in the theory of [[finite group]]s. Every finite group $G$ admits a [[composition series]], i.e., a finite filtration of subgroups 

$$1 = G_0 \subseteq G_1 \subseteq \ldots \subseteq G_n = G$$ 

where each inclusion $G_i \subseteq G_{i+1}$ is a [[normal subgroup]] and the quotient $G_{i+1}/G_i$ (called a **composition factor**) is simple. The condition of simplicity means that that the filtration cannot be further refined by addition of strict inclusions of normal subgroups. Furthermore, the [[Jordan-Hölder theorem]] ensures that any two composition series have the same length and the same composition factors (up to permutation). 

Thus finite simple groups are in some sense the primitive building blocks of finite groups generally. The massive program of classifying all finite simple groups was announced as completed by Daniel Gorenstein in 1983, although some doubts remained because there were some gaps in proofs. Most if not all the gaps are considered by experts in the area to have been filled, but there remain some notable skeptics, including for example [[Jean-Pierre Serre]] and [[John H. Conway]] (verification needed here). See [[classification of finite simple groups]]. 


### Infinite simple groups

There are simple groups of any [[cardinality]] $\kappa$; take for example the smallest normal subgroup of the [[automorphism group]] $Aut(\kappa)$ containing all 3-cycles (this is the infinite version of the [[alternating group]]).


[[!redirects simple group]]
[[!redirects simple groups]]

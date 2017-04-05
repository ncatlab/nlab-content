
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

The [[forgetful functor]] $\Gamma : Top \to Set$ from [[Top]] to [[Set]] that sends any [[topological space]] to its underlying [[set]] has a [[left adjoint]] $Disc : Set \to Top$ and a [[right adjoint]] $Codisc : Set \to Top$.

$$
  (Disc \dashv \Gamma \dashv Codisc) : 
  Top
    \stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
  Set
  \,.
$$


For $S \in Set$

* $Disc(S)$ is the [[topological space]] on $S$ in which every subset is an [[open set]]

  this is called the **discrete topology** on $S$, it is the [[finer topology|finest topology]] on $S$; $Disc(S)$ is called a [[discrete space]];

* $Codisc(S)$ is the topological space on $S$ whose only open sets are the [[empty set]] and $S$ itself

  this is called the **codiscrete topology** on $S$ (also _indiscrete topology_ or _trivial topology_), it is the [[coarser topology|coarsest topology]] on $S$; $Codisc(S)$ is called a _[[codiscrete space]]_ .

For an axiomatization of this situation see _[[codiscrete object]]_.

## Properties


+-- {: .num_example}
###### Example

Let $S$ be a [[set]] and let $(X,\tau)$ be a [[topological space]]. Then 

1. every [[continuous function]] $(X,\tau) \longrightarrow Disc(S)$ is [[locally constant function|locally constant]];

1. every [[function]] (of sets) $X \longrightarrow CoDisc(S)$ is [[continuous function|continuous]].

=--


[[!redirects discrete topology]]

[[!redirects discrete topologies]]
[[!redirects discrete topological structure]]
[[!redirects discrete topological structures]]
[[!redirects discrete topological space]]
[[!redirects discrete topological spaces]]

[[!redirects codiscrete topology]]
[[!redirects codiscrete topologies]]
[[!redirects codiscrete topological structure]]
[[!redirects codiscrete topological structures]]

[[!redirects codiscrete topological space]]
[[!redirects codiscrete topological spaces]]

[[!redirects co-discrete topological space]]
[[!redirects co-discrete topological spaces]]


[[!redirects indiscrete topology]]

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

  this is caled the **discrete topology** on $S$, $Disc(S)$ is called a [[discrete space]];

* $Codisc(S)$ is the topological space on $S$ whose only open sets are the [[empty set]] and $S$ itself

  this is called the **codiscrete topology** on $S$ (also _indiscrete topology_ or _trivial topology_), $Codisc(S)$ is called a _[[codiscrete space]]_ .

## Properties

For an axiomatization of this situation see [[cohesive topos]].

[[!redirects codiscrete topology]]
[[!redirects discrete topology]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A more general concept of [[metric space]]. 

## Definition ##

A __premetric space__ is a [[set]] $S$ with a ternary [[relation]] $(-)\sim_{(-)}(-)\colon S \times \mathbb{R}_+ \times S \to \Omega$, where $\mathbb{R}_+$ represent the positive [[real numbers]] in $\mathbb{R}$ and $\Omega$ is the set of [[truth values]]. 

A premetric is __reflexive__ if for every $a \in S$ and $\epsilon \in \mathbb{R}_+$, $a \sim_\epsilon a$, and a set with a reflexive premetric is called a **reflexive premetric space**. 

## Properties ##

### Premetric topology ###

+-- {: .num_defn #OpenBalls}
###### Definition

Let $(X,\sim^X)$, be a reflexive premetric space. Then for every element $x \in X$ and every  $\epsilon \in \mathbb{R}_+$ a [[positive number|positive]] [[real number]], write

$$
  B^\circ_x(\epsilon) 
    \;\coloneqq\;
  \left\{
    y \in X \;\vert\; x \sim_\epsilon y
  \right\}
$$

for the [[open ball]] of [[radius]] $\epsilon$ around $x$.

=--

+-- {: .num_defn #OpenSubsetsOfAMetricSpace}
###### Definition

Let $(X,\sim^X)$ be a reflexive premetric space. Say that

1. A _[[neighbourhood]]_ of a point $x \in X$ is a [[subset]] $x \in U \subset X$ which contains some [[open ball]] $B_x^\circ(\epsilon)$ around $x$ (def. \ref{OpenBalls}).

1. An _[[open subset]]_ of $X$ is a [[subset]] $U \subset X$ such that for every for $x \in U$ it also contains a [[neighbourhood]] of $x$.

=--

+-- {: .num_remark}
###### Remark

The collection of open subsets in def. \ref{OpenSubsetsOfAMetricSpace} constitutes a _[[topological space|topology]]_ on the set $X$, making it a _[[topological space]]_. This is called the __premetric topology__. Stated more concisely: the [[open balls]] in a reflexive premetric space constitute the [[basis of a topology]] for the premetric topology.

=--

### Premetric uniformity ###

* Every reflexive premetric space is a [[uniform space]]. 

## Rational premetric spaces ##

Sometimes the positive [[rational numbers]] $\mathbb{Q}_{+}$ are used instead of $(0, \infty)$, such as in the construction of the [[Cauchy real numbers]] and the [[HoTT book real numbers]]. These premetrics are called **rational premetrics**, and the associated spaces **rational premetric spaces**, and they also come with a topology and a uniformity. 

## See also ##

* [[Cauchy structure]]

* [[metric space]]

## References ##

* Auke B. Booij, Analysis in univalent type theory ([pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf))

[[!redirects premetric]]
[[!redirects premetrics]]
[[!redirects premetric spaces]]
[[!redirects premetric topology]]
[[!redirects premetric topologies]]

[[!redirects reflexive premetric]]
[[!redirects reflexive premetrics]]
[[!redirects reflexive premetric space]]
[[!redirects reflexive premetric spaces]]

[[!redirects rational premetric]]
[[!redirects rational premetrics]]
[[!redirects rational premetric space]]
[[!redirects rational premetric spaces]]
[[!redirects rational premetric topology]]
[[!redirects rational premetric topologies]]
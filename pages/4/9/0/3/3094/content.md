
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

Given a [[topological space]] $X$ in the sense of [[Bourbaki]] (that is, a set $X$ and a topology $\tau_X$) and a [[subset]] $Y$ of $X$, a topology $\tau_Y$ on $Y$ is said to be the topology **induced** from $\tau_X$ by the [[inclusion function|set inclusion]] $Y \hookrightarrow X$ if $\tau_Y = \tau_X \cap_{pw} \{Y\} \coloneqq \{ U \cap Y | U\in\tau_X\}$. The pair $(Y,\tau_Y)$ is then said to be a *topological [[subspace]]* of $(X,\tau_X)$. The induced topology is for that reason sometimes called the **subspace topology** on $Y$. 

A property of topological spaces is said to be **hereditary** if its satisfaction for a topological space $X$ implies its satisfaction for all topological subspaces of $X$. 


## Variations

There is also a notion of a [[Grothendieck topology]] induced along a [[functor]] from a Grothendieck topology on another category (actually the input can be a somewhat more general [[coverage]], then the topology induced along the [[identity functor]] will serve as a sort of a completion). (this will be explained later).

A topology may be induced by more than a [[function]] other than a subset inclusion, or indeed by a family of functions out of $Y$ (not necessarily all with the same [[target]]). However, the term 'induced topology' is often (usually?) restricted to subspaces; the general concept is called a [[weak topology]].  (This construction can be done in any [[topological concrete category]]; in this generality it is often called an [[initial structure]] for a [[sink|source]].)  The dual construction (involving functions to $Y$) is a [[strong topology]] (or [[final structure]] for a [[sink]]); an example is the [[quotient topology]] on a [[quotient space]].


[[!redirects subspace topology]]
[[!redirects induced topology]]

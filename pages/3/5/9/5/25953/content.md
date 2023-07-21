
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

\tableofcontents

\section{Definition}

Recall that a [[simple graph]] is a [[set]] $V$ of [[vertices]] equipped with 

* a [[family]] of [[subsingletons]] $x \in V, y \in V \vdash E(x, y)$ whose elements are called [[edges]], 

* a family of bijections $x \in V \vdash i(x, y):E(x, x) \cong \emptyset$, 

* a family of [[bijections]] $x \in V, y \in V \vdash s(x, y):E(x, y) \cong E(y, x)$. 

A **weighted graph** is a simple graph equipped with a family of functions $x \in V, y \in V \vdash w(x, y):E(x, y) \to R$ from the edge subsingleton to a [[rig]] of [[numbers]] $R$. Usually $R$ is the [[natural numbers]] $\mathbb{N}$ or the [[real numbers]] $\mathbb{R}$. 

\section{References}

* Wikipedia, [Weighted graph](https://en.wikipedia.org/wiki/Weighted_graph)

* Wikipedia, <a href="https://en.wikipedia.org/wiki/Graph_(discrete_mathematics)#Weighted_graph">Graph (discrete mathematics)</a>

[[!redirects weighted graph]]
[[!redirects weighted graphs]]
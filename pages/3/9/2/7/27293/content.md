
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Idea

A pretopological space is a [[convergence space]] which has all intersections of convergent filters to an element also converge to that element. Thus, a $\sigma$-pretopological space should be a convergence space which should have countable intersections of convergent filters to an element converge to that element. 

## Definition

A $\sigma$-pretopological space $S$ is a set $S$ with a relation $F \to x$ from the set of [[filters]] on $S$ to $S$ itself, satisfying the following properties 

*  Centred:  The free ultrafilter at $x$ (the collection of all sets that $x$ belongs to) converges to $x$:
   $$ \{ A \;|\; x \in A \} \to x .$$
*  Isotone:  If $F$ converges to $x$ and $G$ refines $F$, then $G$ converges to $x$:
   $$ F \to x \;\Rightarrow\; F \subseteq G \;\Rightarrow\; G \to x .$$
*  Countably directed:  The intersection of a [[countable]] [[family]] of filters that converge to $x$ itself converges to $x$:
   $$ \forall n \in \mathbb{N}.(F_n \to x) \; \Rightarrow \; \left(\bigcap_{n \in \mathbb{N}} F_n\right) \to x .$$

## Related concepts

* [[convergence space]]

* [[pretopological space]]

[[!redirects sigma-pretopological space]]
[[!redirects sigma-pretopological spaces]]

> This entry is about a notion in [[general topology]], unrelated to [[derived geometry]].

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


\tableofcontents


## Idea

In the context of [[general topology]], given a [[subset]] of a [[topological space]], its *derived set* consists of all [[elements]] of the space that are [[limit point|accumulation points]] of the subset. 

In other words, if we consider every point of the [[topological closure|closure]] of the set as either isolated or non-isolated, then the derived set consists of the non-isolated points in the closure. 

Another name for the derived set is the *Cantor-Bendixson derivative*. 

## Properties 

Derived sets are [[closed set|closed]], since the set of isolated points in the closure is open in the closure under the [[subspace topology]]. 

Given a [[topological space]] $X$, the assignment that takes a closed [[subset]] $A$ of $X$ to its derived set $A'$ defines an operator 

$$\delta: Cl(X) \to Cl(X)$$ 

on the set of closed subsets of $X$. It has the following easily established properties: 

* $\delta(A) \subseteq A$; 

* If $A \subseteq B$, then $\delta(A) \subseteq \delta(B)$; 

* $\delta$ preserves finite unions.

Recall that a subset $A$ of a space $X$ is *[[perfect set|perfect]]* if $A' = A$. For [[closed sets]] $C$, define a closed set $C^\alpha$ for each [[ordinal]] $\alpha$ by transfinite [[recursion]]: 

* $C^0 \coloneqq C$; 

* $C^{\alpha + 1} \coloneqq \delta(C^\alpha)$; 

* For [[limit ordinals]] $\beta$, $C^\beta \coloneqq \bigcap_{\alpha \lt \beta} C^\alpha$. 

The decreasing chain $C^\alpha$ eventually terminates in a perfect set. The least ordinal for which $C^{\alpha + 1} = C^\alpha$ is called the *Cantor-Bendixson rank* of $C$. 

\begin{proposition} 
In a [[second-countable space]], every closed set has countable Cantor-Bendixson rank, and is the union of a perfect set and a countable set. 
\end{proposition} 

\begin{proof} 
Let $U_i$ be a [[countable set|countable]] [[topological base|basis]] of $X$. For each $\beta \lt \alpha$, each point $x \in C^\beta \setminus C^{\beta + 1}$ is an isolated point, so we can find an $U_{i(x)}$ in the basis such that $U_{i(x)} \cap (C^\beta \setminus C^{\beta + 1}) = \{x\}$. It is then clear that $x \mapsto i(x)$ is injective, so each $C^\beta \setminus C^{\beta + 1}$ is countable. Similarly, whenever $C^\beta \setminus C^{\beta + 1}$ is [[inhabited set|nonempty]], we can find a basis element $U_{j(\beta)}$ that isolates one of its points (say $x$), and this same $U_j$ cannot isolate any point of an earlier $C^\gamma \setminus C^{\gamma + 1}$ since $x$ is a limit point of $C^\gamma$. It follows that $\beta \mapsto j(\beta)$ is an injective map, so that $\alpha$ must be a countable ordinal, and the collection $F \coloneqq C \setminus C^\alpha = \bigcup_{\beta \lt \alpha} C^\beta \setminus C^{\beta + 1}$ is (at most) countable. 
\end{proof} 

\begin{proposition} 
In a [[Polish space]], perfect sets have continuum [[cardinality]] $c = 2^{\aleph_0}$. 
\end{proposition} 

The proof is given [there](Polish+space#cantor). It follows that infinite closed sets in a Polish space have cardinality either $\aleph_0$ or $2^{\aleph_0}$ (compare the *[[continuum hypothesis]]*). 

## Related concepts 

* [[Polish space]] 

* [[limit point]] 

## References 

* {#Kechris} Alexander S. Kechris, _Classical descriptive set theory_, Springer (1994) &lbrack;[doi:10.1007/978-1-4612-4190-4](https://doi.org/10.1007/978-1-4612-4190-4)&rbrack;

See also:

* Wikipedia: *<a href="https://en.wikipedia.org/wiki/Derived_set_(mathematics)">Derived set (mathematics)</a>*

[[!redirects derived sets]]


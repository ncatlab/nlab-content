
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--

\tableofcontents

## Definition

A (binary) [[relation]] $\sim$ on a set $A$ is __asymmetric__ if no two elements are related in both orders:
$$\forall (x, y: A),\; x \sim y \;\Rightarrow\; y \nsim x$$

This is equivalently 

$$\forall (x, y: A),\; (x \sim y \wedge y \sim x) \;\Rightarrow\; \bot$$ 

In the language of the $2$-poset-with-duals [[Rel]] of sets and relations, a relation $R: A \to A$ is __asymmetric__ if it is disjoint from its dual:
$$R \cap R^{op} \subseteq \empty$$
Of course, this containment is in fact an equality.

An asymmetric relation is necessarily [[irreflexive relation|irreflexive]].

That $x \sim y \;\Rightarrow\; y \nsim x$ implies that $x \nsim y \vee y \nsim x$ holds. As a result, the [[disjunction]] of $x \sim y$ and $y \sim x$ is equivalent to the [[exclusive disjunction]] of $x \sim y$ and $y \sim x$, and is an [[inequality relation]] $x \# y$:

$$x \# y \iff (x \sim y \vee y \sim x) \iff (x \sim y \underline{\vee} y \sim x)$$

If $x \sim y$ is also [[cotransitive relation|cotransitive]] then $x \# y$ is an [[apartness relation]], and if $x \sim y$ is [[connected relation|connected]] then $x \# y$ is [[tight relation|tight]]. 

## Related concepts

* [[pseudo-order]]

[[!redirects asymmetric]]
[[!redirects asymmetric relation]]
[[!redirects asymmetric relations]]
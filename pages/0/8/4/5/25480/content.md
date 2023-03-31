
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The **reflexive completion** (also called the **Isbell completion**) of a category $A$ is the [[fixed point of an adjunction|fixed point]] of the [[Isbell duality]] adjunction for $A$.

## Properties

* The reflexive completion is idempotent: $\mathcal{R}(\mathcal{R}(A)) \simeq \mathcal{R}(A)$.

* The reflexive completion is [[Cauchy complete]]. The Cauchy completion $\bar A$ of a small category $A$ is a full subcategory of the reflexive completion $\mathcal{R}(A)$. We have that $\mathcal{R}(\bar A) \simeq \mathcal{R}(A)$. Hence [[Morita equivalent]] categories have equivalent reflexive completions. See §10 of [Avery and Leinster](#AveryLeinster).

* $A \to \mathcal{R}(A)$ [[created limit|creates]] limits and colimits. $\mathcal{R}(A) \to \hat{A}$ preserves limits and [[reflected limit|reflects]] limits and colimits. See §11 of [Avery and Leinster](#AveryLeinster).

* The reflexive completion of a small category has an [[initial object]] and a [[terminal object]].

* The reflexive completion is a full subcategory of the [[Isbell envelope]], and can be concretely described as a [[2-pullback]]:
\begin{tikzcd}
	{\mathcal R(A)} & {[A^{\mathrm{op}}, \mathrm{Set}]} \\
	{[A, \mathrm{Set}]^{\mathrm{op}}} & {\mathcal I(A)}
	\arrow[hook, from=1-1, to=1-2]
	\arrow[hook, from=1-1, to=2-1]
	\arrow[hook, from=1-2, to=2-2]
	\arrow[hook, from=2-1, to=2-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=1-1, to=2-2]
\end{tikzcd}
See [[envelope of an adjunction]].

## Related concepts

* [[Isbell duality]]

* [[Isbell envelope]]

* [[fixed point of an adjunction]]

* [[MacNeille completion]]

## References

* {#AveryLeinster} [[Tom Avery]], [[Tom Leinster]]. _Isbell conjugacy and the reflexive completion_. Theory and Applications of Categories, **36** 12 (2021) 306-347 &lbrack;[tac:36-12](http://www.tac.mta.ca/tac/volumes/36/12/36-12abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/36/12/36-12.pdf)&rbrack;


[[!redirects reflexive completions]]

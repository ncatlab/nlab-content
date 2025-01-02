
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[constructive mathematics]], a generalisation of the notion of an [[ring with apartness]] which also allows for the [[denial inequality]] of [[rings]] to be used for the inequality relation. 

## Definition

A [[ring]] $R$ is an **inequality ring** or a **ring with inequality** if it comes with an [[irreflexive relation|irreflexive]] [[symmetric relation]] $a \nsim b$ such that

* for all $a, b, c, d \in R$, $a + b \nsim c + d$ implies that $a \nsim c$ or $b \nsim d$

* for all $a, b \in R$, $-a \nsim -b$ implies that $a \nsim b$

* for all $a, b, c, d \in R$, $a \cdot b \nsim c \cdot d$ implies that $a \nsim c$ or $b \nsim d$

## Related concepts

* [[apartness ring]]

* [[antithesis interpretation]]

* [[antithesis ideal]]

## References

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

Some discussion about rings with inequality occurred in:

* *One universe as a foundation & friends*, Category Theory Zulip ([web](https://categorytheory.zulipchat.com/#narrow/channel/229136-theory.3A-category-theory/topic/One.20universe.20as.20a.20foundation.20.26.20friends/near/468013130))

[[!redirects inequality ring]]
[[!redirects inequality rings]]

[[!redirects ring with inequality]]
[[!redirects rings with inequality]]
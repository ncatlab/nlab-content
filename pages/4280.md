
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}


## Idea

This page collects a few notions and facts about [[representations]] of [[C-star-algebras]] with an eye towards their use in [[AQFT]]. 

In [[AQFT]] the observables are given by a [[causal net of algebras]], usually $C^*$-algebras. A concrete physical system corresponds to a [[state]] of the algebra of all observables, which leads, via the [[GNS construction]], to a representation of this algebra on a concrete Hilbert space. In this way the familiar picture of [[quantum mechanics]] reappears. The interpretation of states and their representation as modelling concrete physical systems means that a systematic study of all representation of a given algebra of observables is central to [[AQFT]].

## Definition

+-- {: .num_defn}
###### Definition

A **representation** $\pi$ of a $C^*$-algebra $A$ is a [[star-representation]] on a [[Hilbert space]] $H$, hence a $*$-homomorphism from $A$ to the algebra of [[bounded operators]] on $H$.

=--

+-- {: .num_remark}
###### Remark

The _[[continuous function|continuity]]_ of the representation is implied by the [[star-representation]]-property.

=--

+-- {: .num_defn}
###### Definition

A representation is **faithful** if its [[kernel]] is trivial.

=--

+-- {: .num_defn}
###### Definition

Given two representations $\pi_1$ on $H_1$ and $\pi_2$ on $H_2$, if there is a [[unitary operator]] $U: H_1 \to H_2$ such that $U \pi_1 = \pi_2 U$ then the representations are **unitarily equivalent**. A linear map $U$ (not necessarily unitary) having this property is called an **[[intertwiner]]** or an **intertwining map**. If there is no nontrivial intertwiner the two representations $\pi_1$ and $\pi_2$ are called **disjoint** (or totally / completley different).

=--

In the context of [[AQFT]] the term 'intertwiner' is mostly used in the specific sense defined here.

From the physical viewpoint unitarily equivalent representations describe the same system, so that the classification of not unitarily equivalent representations is an important topic.

+-- {: .num_defn}
###### Definition
If there is a subspace $H_1$ of the Hilbert space $H$ which is invariant under $\pi(A)$, that is $\pi(A)(H_1) \subseteq H_1$, then the restriction of the representation to $H_1$ is again a representation of $A$, it is called a **subrepresentation** of $\pi$. 
=--

+-- {: .num_defn}
###### Definition
Given a family $(\pi_i, H_i)$ of representations, we can form the direct sum $H := \oplus H_i$ of the Hilbert spaces and define a new representation $\pi := \oplus \pi$ via $\pi(A) | H_i := \pi_i$. This is the **direct sum of representations**.
=--


## Related concepts

* [[cyclic vector]]

* [[GNS construction]]


## References

See at _[[operator algebras]]_.


[[!redirects representation of a C-star-algebra]]
[[!redirects representations of a C-star-algebra]]
[[!redirects representations of C-star-algebras]]
[[!redirects representation of a C-star algebra]]
[[!redirects representations of a C-star algebra]]
[[!redirects representations of C-star algebras]]

[[!redirects C-star representation]]
[[!redirects C-star representations]]

[[!redirects C*-representation]]
[[!redirects C*-representations]]

[[!redirects representation of a C*-algebra]]
[[!redirects representations of a C*-algebra]]
[[!redirects representation of C*-algebras]]
[[!redirects representations of C*-algebra]]

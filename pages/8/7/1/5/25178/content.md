
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[material set theory]], a [[subset]] $S$ of a [[set]] $A$ with a [[apartness relation]] $\#$ is an apartness-[[open subset]] $S \subseteq A$ if for all $x \in A$ and $y \in A$,

$$(x \in S) \implies (y \in S) \vee (x \# y)$$

In [[dependently sorted set theory]], where membership $x \in S$ is not a [[relation]], the above statement that $x \in S$ for every element $x \in A$ in material set theory is equivalently a predicate in the logic $x \in A \vdash P_S(x)$. The given apartness-open subset $S$ is then defined by [[restricted separation]] as the set $S \coloneqq \{x \in A \vert P_S(x)\}$, which in structural set theory automatically comes with an [[injection]] 
$$i:\{x \in A \vert P_S(x)\} \hookrightarrow A$$
such that
$$\exists y \in \{x \in A \vert P_S(x)\}.x = i(y) \iff P_S(x)$$
Hence, the notion of apartness-open predicate, a formulation of the notion of apartness-open as a predicate rather than a subset. 

## Definition

Given a set $A$ with an [[apartness relation]] $\#$, an $\#$-open predicate is a predicate $x \in A \vdash P_S(x)$ which satisfies

$$x \in A, y \in A \vdash P_S(x) \implies P_S(y) \vee (x \# y)$$

The $\#$-open subset $S$ is then defined by [[restricted separation]] as
$S \coloneqq \{x \in R \vert P_S(x)\}$

## See also

* [[apartness relation]]
* [[predicate]]
* [[anti-ideal predicate]]
* [[restricted separation]]

[[!redirects apartness-open predicate]]
[[!redirects apartness-open predicates]]
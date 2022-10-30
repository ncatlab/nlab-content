
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# The L&#233;vy hierarchy
* table of contents
{: toc}

## Idea

In [[logic]], [[model theory]], and [[set theory]], the **L&#233;vy hierarchy** is a stratification of [[formulas]], [[definable sets]], and (definable) [[classes]] according to the complexity of the unbounded [[quantifiers]].

## Definition

We define classes of formulas $\Sigma_n$, $\Pi_n$, and $\Delta_n$ by [[induction]] on $n$.

* A formula is $\Sigma_0$ iff it is $\Pi_0$ iff it is $\Delta_0$, by definition if it is equivalent to a formula all of whose quantifiers are [[bounded quantifier|bounded]], i.e. of the form $\forall x\in A$ or $\exists x\in A$.

* A formula is $\Sigma_{n+1}$ if it is equivalent to one of the form $\exists \vec{x}. \phi$, where $\vec{x}$ is a list of variables and $\phi$ is $\Pi_n$.

* A formula is $\Pi_{n+1}$ if it is equivalent to one of the form $\forall \vec{x}. \phi$, where $\vec{x}$ is a list of variables and $\phi$ is $\Sigma_n$.

* A formula is $\Delta_n$ if it is both $\Sigma_n$ and $\Pi_n$.

A class is given one of these labels if it can be defined by a formula which has that label.

These definitions are most useful in [[classical mathematics]], in which every formula is equivalent to one all of whose unbounded quantifiers are in the front, so that every formula belongs to some $\Sigma_n$ or $\Pi_n$.

[[!redirects Levy hierarchy]]
[[!redirects Sigma-n formula]]
[[!redirects Pi-n formula]]
[[!redirects Delta-n formula]]
[[!redirects ∞-n formula]]
[[!redirects ∞-n formula]]
[[!redirects ∞-n formula]]
[[!redirects Sigma-0 formula]]
[[!redirects Pi-0 formula]]
[[!redirects Delta-0 formula]]
[[!redirects ∞-0 formula]]
[[!redirects ∞-0 formula]]
[[!redirects ∞-0 formula]]
[[!redirects Sigma-1 formula]]
[[!redirects Pi-1 formula]]
[[!redirects Delta-1 formula]]
[[!redirects ∞-1 formula]]
[[!redirects ∞-1 formula]]
[[!redirects ∞-1 formula]]

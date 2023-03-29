
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A pointed topological pair is a [[pointed topological space]] $X=(X,x_0)\in Top_*$ equipped with a [[topological subspace]] $A\subset X$ containing the [[base point]] $x_0$.

Let $I=[0,1]$ be the unit [[closed interval]] and for $N\in\mathbb{N}$ let $J^N \coloneqq \partial I^N-\{0\}\times I^{N-1}$. 

\begin{definition}
  The *relative loop space* of a pointed topological pair $(X,A)$ is the [[compact-open topology|space of]] [[continuous maps]] of the form $(I^N,\partial I^N,J^N)\rightarrow (X,A,x_0)$, denoted $\Omega^N(X,A)$. 
\end{definition}

For $A = \{x_0\}$ this reduces to the ordinary notion of ([[iterated loop space|iterated]]) *[[loop space]]*. 

The relative loop spaces allow us to define the relative homotopy groups of topological pairs.

\begin{definition}
For $N\geq 1$ the $N$-th relative homotopy set of a topological pair $(X,A)$, denoted $\pi_N(X,A)$ is defined as the set of connected components of the associated relative loop space, ie $\pi_N(X,A)\coloneqq \pi_0\Omega^N(X,A)$.

If $N\geq 2$ then $\pi_N(X,A)$ is a group, which is abelian if $N\geq 3$.
\end{definition}



## Homotopy theory of relative loop spaces

If we are interested in the [[homotopy theory]] of relative loop spaces (as in *[[recognition of relative loop spaces]]*) the above definition is not appropriate since there is no [[model category]]-[[structure]] on the category of topological pairs, as explained in [this mathoverflow discussion](https://mathoverflow.net/questions/128976/can-one-make-the-category-of-pairs-of-topological-spaces-a-model-category).

The solution here is to work in the category $Top^\to_*$ of continuous pointed maps equipped with the [[projective model structure on functors]]. If we start with the [[classical model structure on topological spaces|Quillen model structure]] on $Top$, the [[cofibrant objects]] in $Top^\to_*$ are the inclusions of CW-pairs, and if we start with the [[mixed model structure]] we get the maps homotopy equivalent to those.

We can then define relative loop spaces as loop spaces of homotopy fibers.

\begin{definition}
  For $N\geq 1$ the relative $N$-loop space functor is the right derivable functor
$$
\Omega^N_{rel}:Top_*^\to \to Top_*, \qquad \Omega^N_{rel}(\iota:A\rightarrow X)\coloneqq (A\times_X X^I)^{\mathbb{S}^{N-1}}.
$$
\end{definition}

For inclusions of topological pairs the two definitions of relative loop spaces are [[natural transformation|naturally]] [[homeomorphism|homeomorphic]].

## Related concepts

* [[loop space]]

* [[CW-pair]]

[[!redirects relative loop spaces]]



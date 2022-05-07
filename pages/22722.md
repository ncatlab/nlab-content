# Axiom of stack completion

\tableofcontents

## Definition

An [[internal category]] $\mathbb{A}$ in an [[elementary topos]] $\mathcal{E}$ is called an **(intrinsic) stack** if the [[indexed category]] that it represents, $(X\in \mathcal{E}) \mapsto \mathcal{E}(X,\mathbb{A}) \in Cat$, is a [[stack]] for the [[regular topology]] of $\mathcal{E}$.  An internal functor is called a **weak equivalence** if it is internally [[essentially surjective]] and [[fully faithful]]; this is strictly weaker than being an internal equivalence if the [[axiom of choice]] does not hold in $\mathcal{E}$.  However, if $f:\mathbb{A} \to \mathbb{B}$ is a weak equivalence and $\mathbb{C}$ is a stack, then the induced functor $\mathrm{Cat}(\mathcal{E})(\mathbb{B},\mathbb {C})\to \mathrm{Cat}(\mathcal{E})(\mathbb{A},\mathbb{C})$ is an equivalence.

We say that $\mathcal{E}$ satisfies the **axiom of stack completions (ASC)** if every internal category admits a weak equivalence to an internal category that is a stack (see [Bunge-Hermida](#BH)).

## Examples

* If $\mathcal{E}$ satisfies the [[axiom of choice]], then every internal category is a stack, so ASC holds trivially.

* If $\mathcal{E}$ is a [[Grothendieck topos]], then internal stack completions can be constructed using the [[small object argument]], as [[fibrant replacements]] in the [[model structure]] on $\mathrm{Cat}(\mathcal{E})$ constructed by [Joyal and Tierney](#JT), so it satisfies ASC.

## References

* {#BH} Bunge and Hermida, "Pseudomonadicity and 2-stack completions"

* {#JT} Joyal and Tierney, "Strong stacks and classifying spaces"

[[!redirects axiom of stack completion]]
[[!redirects ASC]]

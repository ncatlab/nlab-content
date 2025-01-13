
> For [[affine functions]] in [[linear algebra]] and [[geometry]], see [[affine map]]. 

-----

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Definition

Given two [[A-set|$\mathcal{A}$-sets]] $A$ and $B$, an **affine function** or **antithesis function** or **$\mathcal{A}$-function** is a function $f:A \to B$ which preserves the [[equivalence relation]] and reflects the [[irreflexive symmetric relation]]:

$$(x \sim_A y) \to (f(x) \sim_B f(y) \; \mathrm{and} \; (f(x) \nsim_B f(y)) \to (x \nsim_A y)$$

In [[dependent type theory]], if the $\mathcal{A}$-sets are [[univalent setoid|univalent]], then the $\mathcal{A}$-functions are precisely the [[strongly extensional functions]] with respect to the [[irreflexive symmetric relation]]. In addition, if the univalent $\mathcal{A}$-sets are [[affirmative A-set|affirmative]], then every function is an affine function. 

## Related concepts

* [[affine set]]

* [[extensional function]]

* [[strongly extensional function]]

## References

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

[[!redirects A-function]]
[[!redirects A-functions]]

[[!redirects antithesis function]]
[[!redirects antithesis functions]]
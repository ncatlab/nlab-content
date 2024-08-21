
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Definition

### In cohesive type theory

In [[cohesive type theory]], the axiom of **real cohesion** states that there is a [[terminal object|terminal]] [[Archimedean ordered field]] $\mathbb{R}$ such that the [[shape]] of $\mathbb{R}$ is a [[contractible type]]. Note that if the type theory has [[quotient sets]], as in type theory with [[coequalizer types]] and [[set truncations]], then the terminal Archimedean ordered field $\mathbb{R}$ is sequentially Cauchy complete, and if the type theory is [[impredicative type theory|impredicative]] or otherwise contains the [[Dedekind real numbers]], then $\mathbb{R}$ is equivalent to the Dedekind real numbers and thus Dedekind complete. 

This is equivalent in strength to **axiom $\mathbb{R} \flat$**, which says that there is a [[terminal object|terminal]] [[Archimedean ordered field]] $\mathbb{R}$ such that every crisp type $T$ is discrete if and only if every function from $\mathbb{R}$ into $\mathrm{Disc}(T)$ is a [[constant function]]. $\mathrm{Disc}$ is a [[modality]] which takes types in the crisp mode to its corresponding discrete type in the cohesive mode, and a discrete type $A$ in the cohesive mode is one for which the canonical function $\flat(-):A \to \flat A$ is an [[equivalence of types]]. 

Since in the terminal Archimedean ordered field, $\neg (0 =_{\mathbb{R}} 1)$, the proofs of the equivalence of [[sufficient cohesion]] and [[axiom C2]] also applies for real cohesion and axiom $\mathbb{R} \flat$. Thus, by adapting [Shulman 2018](#Shulman18)'s proof for axiom C2 to axiom $\mathbb{R} \flat$, we have that Axiom $\mathbb{R} \flat$ implies that every function from $\mathbb{R}$ into a discrete type $A$ is a constant function; conversely, if every function from $\mathbb{R}$ to a discrete type $A$ is constant, then it holds for the discrete types which are in the image of the $\mathrm{Disc}$ modality. Finally, by adapting [Aberlé 2024](#Aberle24)'s proof for sufficient cohesion to real cohesion, we have that the axiom of real cohesion holds if and only if every function from $\mathbb{R}$ into a discrete type $A$ is a constant function. 

## Properties

\begin{definition}
The [[shape modality]] of a type $A$ is defined to be the [[localization of a type|localization]] of $A$ at the type $\mathbb{R}$

$$\esh A \coloneqq L_\mathbb{R}(A)$$
\end{definition}

## Related concepts

* [[axiom of cohesion]]

* [[axiom of sufficient cohesion]]

## References

* {#Shulman18} [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Shulman17} [[Mike Shulman]], *Homotopy type theory: the logic of space*, New Spaces in Mathematics: Formal and Conceptual Reflections, ed. Gabriel Catren and Mathieu Anel, Cambridge University Press, 2021 ([arXiv:1703.03007](https://arxiv.org/abs/1703.03007), [doi:10.1017/9781108854429](https://doi.org/10.1017/9781108854429))

* {#Aberle24} [[C.B. Aberlé]], *Parametricity via Cohesion* &lbrack;[arXiv:2404.03825](https://arxiv.org/abs/2404.03825)&rbrack; 

[[!redirects real cohesion]]
[[!redirects axiom of real cohesion]]
[[!redirects axioms of real cohesion]]

[[!redirects real-cohesion]]
[[!redirects axiom of real-cohesion]]
[[!redirects axioms of real-cohesion]]

[[!redirects Dedekind real cohesion]]
[[!redirects axiom of Dedekind real cohesion]]
[[!redirects axioms of Dedekind real cohesion]]

[[!redirects axiom Rb]]
[[!redirects axiom R-flat]]
[[!redirects axiom R flat]]
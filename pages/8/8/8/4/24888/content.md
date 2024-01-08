
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

## Idea
 {#Idea}

Axioms of [[cohesion]] are certain [[axioms]] added to any [[spatial type theory]] in order to define the [[shape modality]] for [[cohesive homotopy type theory]]. In particular, the *axiom of real cohesion* plays a role in defining [[real-cohesive homotopy type theory]] (the setting for [[classical homotopy theory]] and [[algebraic topology]]), and the *axiom of affine cohesion* plays a role in defining [[A1-cohesive homotopy type theory|$\mathbb{A}^1$-cohesive homotopy type theory]] (the setting for [[A1-homotopy theory|$\mathbb{A}^1$-homotopy theory]]), where the [[affine line]] $\mathbb{A}^1$ plays the role that $\mathbb{R}$ does in real-cohesive homotopy type theory. Affine cohesion could hypothetically also be used in defining a cohesive version of [[Mitchell Riley]]'s [[bunched logic|bunched]] [[linear homotopy type theory]] (the setting for [[stable homotopy theory]]) for the purposes of doing [[motivic homotopy theory]]. 

## Definition

We assume the presentation of [[spatial type theory]] using crisp term judgments $a::A$ in addition to the usual (cohesive) type and term judgments $A \; \mathrm{type}$ and $a:A$, as well as context judgments $\Xi \vert \Gamma \; \mathrm{ctx}$ where $\Xi$ is a list of crisp term judgments, and $\Gamma$ is a list of cohesive term judgments. A crisp type is a type in the context $\Xi \vert ()$, where $()$ is the empty list of cohesive term judgments. We also assume [[identity types]], the [[sharp modality]], and the [[flat modality]].

Given a type $A$, let us define $\mathrm{const}_{A, R}:A \to (R \to A)$ to be the type of all constant functions in $R$:
$$\delta_{\mathrm{const}_{A, R}}(a, r):\mathrm{const}_{A, R}(a)(r) =_A a$$
There is an equivalence $\mathrm{const}_{A, 1}:A \simeq (1 \to A)$ between the type $A$ and the type of functions from the [[unit type]] $1$ to $A$. 
Given types $B$ and $C$ and a function $F:(B \to A) \to (C \to A)$, type $A$ is **$F$-[[localization of a type at a family of functions|local]]** if the function $F:(B \to A) \to (C \to A)$ is an [[equivalence of types]]. 

A crisp type $\Xi \vert () \vdash A$ is **discrete** if the function $(-)_\flat:\flat A \to A$ is an [[equivalence of types]]. 

The **axiom of cohesion** for type $R$ states that there is a crisp type $\Xi \vert () \vdash R \; \mathrm{type}$ such that given any crisp type $\Xi \vert () \vdash A \; \mathrm{type}$, $A$ is discrete if and only if $A$ is $(\mathrm{const}_{A, 1}^{-1} \circ \mathrm{const}_{A, R})$-local, or equivalently, if $\mathrm{const}_{A, R}$ is an [[equivalence of types]]. 

$$\frac{\Xi \vert () \vdash A \; \mathrm{type}}{\Xi \vert () \vdash R \flat\mathrm{ax}_A:\mathrm{isEquiv}(\mathrm{const}_{A, R}) \simeq \mathrm{isEquiv}(\lambda x:\flat A.x_\flat)}$$

This allows us to define discreteness for non-crisp types: a type $A$ is **discrete** if $A$ is $(\mathrm{const}_{A, 1}^{-1} \circ \mathrm{const}_{A, R})$-local, or equivalently, if $\mathrm{const}_{A, R}$ is an [[equivalence of types]]. 

Another consequence is that the [[shape]] of $R$ is [[contractible]]. 

\begin{theorem}
Assuming a type $R$ and the axiom of $R$-cohesion, the shape of $R$ is contractible. 
\end{theorem}

\begin{proof}
The type $R$ is inhabited by $\kappa_R(\sigma_R)$, so it remains to show that for all $x:\esh R$, $x =_{\esh R} \kappa_R(\sigma_R)$. Since $\esh R$ is discrete, so is the identity type $x =_{\esh R} \kappa_R(\sigma_R)$, which means by $\esh$-induction, it suffices to prove $\sigma_R(x) =_{\esh R} \kappa_R(\sigma_R)$ for all $x:\esh R$. But this is true from the third introduction rule for $\esh R$. 
\end{proof}

In addition, if the [[type of booleans]] $\mathbb{2}$ is discrete, then $R$ is [[compact connected]]:

\begin{theorem}
Assuming a type $R$, a [[type of all propositions]] $\Omega$ with type reflector $T$, and the axiom of $R$-cohesion, if the function $\mathrm{const}_{2, R}$ is an equivalence of types, then for all functions $P:R \to \Omega$, if for all $x:R$, $T(P(x)) \vee \neg T(P(x))$ is contractible, then either for all $x:R$, $T(P(x))$ is contractible, or for all $x:R$, $\neg T(P(x))$ is contractible. 
\end{theorem}

\begin{proof}
If $P:R \to \Omega$ is such that for all $x:R$, $T(P(x)) \vee \neg T(P(x))$ is contractible, then there is a function $P':R \to \mathbb{2}$ into the [[booleans type]] $\mathbb{2}$ with $\delta_{P'}^{1_2}(x):(P'(x) = 1_2)) \simeq T(P(x))$ and $\delta_{P'}^{0_2}(x):(P'(x) = 0_2)) \simeq \neg T(P(x))$. But if $\mathbb{2}$ is discrete, then by $R$-cohesion $P'$ is constant, which implies that either for all $x:R$, $T(P(x))$ is contractible, or for all $x:R$, $\neg T(P(x))$ is contractible. Thus, $R$ is compact connected if $\mathbb{2}$ is discrete. 
\end{proof} 

## Examples

There are a number of axioms which in general could be called an axiom of cohesion for type $R$. The most general such axiom of cohesion is called **stable local connectedness** or **axiom C0**, which imposes no other restrictions on $R$. If we additionally assume that the type $R$ is pointed with point $0:R$, then the axiom becomes **punctual local connectedness** or **axiom C1**, and if we additionally assume that the type $R$ is a non-trivial bi-pointed set, with points $0:R$, $1:R$, and witnesses $\tau_0:\mathrm{isSet}(R)$ and $\mathrm{nontriv}:(0 =_{R} 1) \to \emptyset$, then the axiom becomes **contractible codiscreteness** or **axiom C2**. If we additionally assume that the type $R$ is a [[Dedekind complete]] [[Archimedean field|Archimedean]] [[ordered field|ordered]] [[lattice]] [[field]] (and usually written as $\mathbb{R}$), then the axiom becomes **real cohesion** or **axiom $\mathbb{R}$-flat**. 

| number/symbol | name | associated [[shape modality]] | additional requirements |
|--------|------|------|-----------|
| $C_0$ | cohesion/stable [[locally ∞-connected (∞,1)-topos|local connectedness]] | [[localization of a type|localization]] at a [[type]] $R$ |  |
| $C_1$ | punctual cohesion/punctual [[locally ∞-connected (∞,1)-topos|local connectedness]] | [[localization of a type|localization]] at a [[pointed type]] $R$ |  |
| $C_2$ | contractible codiscreteness | [[localization of a type|localization]] at a non-trivial [[bi-pointed type|bi-pointed]] [[h-set]] $R$ |  |
|  | discrete cohesion | [[localization of a type|localization]] at a [[contractible type]] $R$ |  |
|  | affine cohesion/algebraic cohesion/$\mathbb{A}^1$-cohesion | [[localization of a type|localization]] at an [[affine line]] $\mathbb{A}^1$ |  |
|  | [[compact connectedness]] | [[localization of a type|localization]] at a [[type]] $R$ | the [[type of booleans]] $\mathbb{2}$ is discrete |
|  | [[continuum]] cohesion | [[localization of a type|localization]] at a [[Hausdorff space]] $R$ | $\mathbb{2}$ is discrete. |
|  | [[metric continuum]] cohesion | [[localization of a type|localization]] at a [[metric space]] $R$ | $\mathbb{2}$ is discrete. |
| $\mathbb{R} \flat$ | [[real number|real]] cohesion | [[localization of a type|localization]] at the [[real numbers]] $\mathbb{R}$ | A higher [[coinductive type]] representing the [[homotopy]] [[terminal]] [[Archimedean ordered field]] $\mathbb{R}$ |
| $\mathbb{R} \flat$ | [[Dedekind real number|real]] cohesion ([[impredicative mathematics|impredicative]]) | [[localization of a type|localization]] at the impredicative [[Dedekind real numbers]] or [[generalized Cauchy real numbers]] $\mathbb{R}$ | A [[type of all propositions]] $\Omega$ |
| $\mathbb{R}_{U} \flat$ | locally $U$-small real cohesion | [[localization of a type|localization]] at the $U$-[[Dedekind real numbers]] or $U$-[[generalized Cauchy real numbers]] $\mathbb{R}_U$ | A [[Tarski universe]] $(U, T)$ |
|  | [[unit interval]] cohesion | [[localization of a type|localization]] at the [[unit interval]] $[0, 1]$ | a higher [[coinductive type]] representing the [[homotopy]] [[terminal]] [[dyadic interval coalgebra]]. |
|  | $U$-small unit interval cohesion | [[localization of a type|localization]] at the $U$-small [[unit interval]] $[0, 1]_\mathbb{U}$ | A [[Tarski universe]] $(U, T)$. |
|  | smooth cohesion | [[localization of a type|localization]] at a [[local Artin algebra|local Artin $\mathbb{R}$-algebra]] | A [[local Artin algebra|local Artin $\mathbb{R}$-algebra]] $R$ |
| $S^1 \flat$ | [[circle type cohesion]] | [[localization of a type|localization]] at the circle type | The [[circle type]] $S^1$ |

## See also

* [[shape modality]]

* [[localization of a type at a family of functions]]

## References

* [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* [[Mike Shulman]], *Homotopy type theory: the logic of space*, New Spaces in Mathematics: Formal and Conceptual Reflections, ed. Gabriel Catren and Mathieu Anel, Cambridge University Press, 2021 ([arXiv:1703.03007](https://arxiv.org/abs/1703.03007), [doi:10.1017/9781108854429](https://doi.org/10.1017/9781108854429))

[[!redirects axiom of cohesion]]
[[!redirects axioms of cohesion]]

[[!redirects axiom of stable local connectedness]]
[[!redirects axioms of stable local connectedness]]

[[!redirects axiom of punctual local connectedness]]
[[!redirects axioms of punctual local connectedness]]

[[!redirects axiom of contractible codiscreteness]]
[[!redirects axioms of contractible codiscreteness]]

[[!redirects real cohesion]]
[[!redirects axiom of real cohesion]]
[[!redirects axioms of real cohesion]]

[[!redirects real-cohesion]]
[[!redirects axiom of real-cohesion]]
[[!redirects axioms of real-cohesion]]

[[!redirects Dedekind real cohesion]]
[[!redirects axiom of Dedekind real cohesion]]
[[!redirects axioms of Dedekind real cohesion]]

[[!redirects localic real cohesion]]
[[!redirects axiom of localic real cohesion]]
[[!redirects axioms of localic real cohesion]]

[[!redirects unit interval cohesion]]
[[!redirects axiom of unit interval cohesion]]
[[!redirects axioms of unit interval cohesion]]

[[!redirects A1-cohesion]]
[[!redirects axiom of A1-cohesion]]
[[!redirects axioms of A1-cohesion]]

[[!redirects affine cohesion]]
[[!redirects axiom of affine cohesion]]
[[!redirects axioms of affine cohesion]]

[[!redirects algebraic cohesion]]
[[!redirects axiom of algebraic cohesion]]
[[!redirects axioms of algebraic cohesion]]

[[!redirects smooth cohesion]]
[[!redirects axiom of smooth cohesion]]
[[!redirects axioms of smooth cohesion]]

[[!redirects axiom C0]]
[[!redirects axiom C1]]
[[!redirects axiom C2]]
[[!redirects axiom R-flat]]
[[!redirects axiom R flat]]
[[!redirects axiom A1-flat]]
[[!redirects axiom A1 flat]]
[[!redirects axiom [0, 1]-flat]]
[[!redirects axiom [0, 1] flat]]

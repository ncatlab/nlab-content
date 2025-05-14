
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

Axioms of [[cohesion]] are certain [[axioms]] added to any [[spatial type theory]] in order to define the [[shape modality]] for [[cohesive homotopy type theory]]. In particular, the *axiom of real cohesion* plays a role in defining [[real-cohesive homotopy type theory]] (the setting for [[classical homotopy theory]] and [[algebraic topology]]). 

## Definition

Given a type $I$, the **axiom of $I$-cohesion** or **axiom C0** such that every crisp type $T$ is discrete if and only if every function from $I$ into $\mathrm{Disc}(T)$ is a [[constant function]]. $\mathrm{Disc}$ is a [[modality]] which takes types in the crisp mode to its corresponding discrete type in the cohesive mode, and a discrete type $A$ in the cohesive mode is one for which the canonical function $\flat(-):A \to \flat A$ is an [[equivalence of types]]. 

The axiom of $I$-cohesion allows us to define discreteness for non-crisp types. Given a type $A$, let us define $\mathrm{const}_{A, I}:A \to (I \to A)$ to be the type of all constant functions in $I$:
$$\delta_{\mathrm{const}_{A, I}}(a, r):\mathrm{const}_{A, I}(a)(r) =_A a$$
Type $A$ is $I$-[[null type|null]] if the function $\mathrm{const}_{A, I}$ is an [[equivalence of types]]. 

\begin{definition}
Assuming the axiom of $I$-cohesion, type $A$ is **discrete** if $A$ is $I$-null. 
\end{definition}

Another consequence is that the [[shape]] of $I$ is [[contractible]], i.e. the **axiom of strong connectedness**

\begin{theorem}
Assuming a type $I$ and the axiom of $I$-cohesion, the shape of $I$ is contractible. 
\end{theorem}

\begin{proof}
The type $I$ is inhabited by $\kappa_I(\sigma_I)$, so it remains to show that for all $x:\esh I$, $x =_{\esh I} \kappa_I(\sigma_I)$. Since $\esh I$ is discrete, so is the identity type $x =_{\esh I} \kappa_I(\sigma_I)$, which means by $\esh$-induction, it suffices to prove $\sigma_I(x) =_{\esh I} \kappa_R(\sigma_I)$ for all $x:\esh I$. But this is true from the third introduction rule for $\esh I$. 
\end{proof}

[Shulman 2018](#Shulman18) showed that axiom C0 implies that every function from $I$ into a discrete type $A$ is a constant function; conversely, if every function from $I$ to a discrete type $A$ is constant, then it holds for the discrete types which are in the image of the $\mathrm{Disc}$ modality. Finally, [Aberlé 2024](#Aberle24) proved that the axiom of strong connectedness holds if and only if every function from $I$ into a discrete type $A$ is a constant function

## Properties

\begin{theorem}
The [[type of booleans]] $\mathbb{2}$ is discrete.
\end{theorem}

\begin{proof}
Theorem 6.19 of [Shulman 18](#Shulman18) says that the [[unit type]] is crisply discrete, and theorem 6.21 of [Shulman 18](#Shulman18) says that the [[sum type]] of two crisply discrete types is itself crisply discrete. Since the type of booleans is the [[sum type]] of two copies of the unit type, the type of booleans is crisply discrete, thus discrete.  
\end{proof}

Since the [[type of booleans]] is discrete, then the type $R$ is [[compact connected]]:

\begin{theorem}
Assuming the axiom of $R$-cohesion, if the function $\mathrm{const}_{\mathbb{2}, R}$ is an equivalence of types, then for all $R$-indexed families of [[mere propositions]] $x:R \vdash P(x)$, if for all $x:R$, $P(x) \vee \neg P(x)$ is contractible, then either for all $x:R$, $P(x)$ is contractible, or for all $x:R$, $\neg P(x)$ is contractible. 
\end{theorem}

\begin{proof}
If the family of mere propositions $x:R \vdash P(x)$ is such that for all $x:R$, $P(x) \vee \neg P(x)$ is contractible, then there is a function $P':R \to \mathbb{2}$ into the [[type of booleans]] $\mathbb{2}$ with $\delta_{P'}^{1_2}(x):(P'(x) = 1_2)) \simeq P(x)$ and $\delta_{P'}^{0_2}(x):(P'(x) = 0_2)) \simeq \neg P(x)$. But since $\mathbb{2}$ is discrete, then by $R$-cohesion $P'$ is constant, which implies that either for all $x:R$, $P'(x) = 1_2$ and thus $P(x)$ is contractible, or for all $x:R$, $P'(x) = 0_2$ and thus $\neg P(x)$ is contractible. Thus, $R$ is compact connected. 
\end{proof}

## Examples

There are a number of axioms which in general could be called an axiom of cohesion for type $R$. The most general such axiom of cohesion is called **stable local connectedness** or **axiom C0**, which imposes no other restrictions on $R$. If we additionally assume that the type $R$ is pointed with point $0:R$, then the axiom becomes **punctual local connectedness** or **axiom C1**, and if we additionally assume that the type $R$ is a non-trivial bi-pointed set, with points $0:R$, $1:R$, and witnesses $\tau_0:\mathrm{isSet}(R)$ and $\mathrm{nontriv}:(0 =_{R} 1) \to \emptyset$, then the axiom becomes **contractible codiscreteness** or **axiom C2**. If we additionally assume that the type $R$ is a [[Dedekind complete]] [[Archimedean field|Archimedean]] [[ordered field|ordered]] [[lattice]] [[field]] (and usually written as $\mathbb{R}$), then the axiom becomes **real cohesion** or **axiom $\mathbb{R}$-flat**. 

| number/symbol | name | associated [[shape modality]] | additional requirements |
|--------|------|------|-----------|
| $C_0$ | cohesion/stable [[locally ∞-connected (∞,1)-topos|local connectedness]] | [[localization of a type|localization]] at a [[type]] $R$ |  |
| $C_1$ | punctual cohesion/punctual [[locally ∞-connected (∞,1)-topos|local connectedness]] | [[localization of a type|localization]] at a [[pointed type]] $R$ |  |
| $C_2$ | contractible codiscreteness | [[localization of a type|localization]] at a non-trivial [[bi-pointed type|bi-pointed]] [[h-set]] $R$ |  |
|  | discrete cohesion | [[localization of a type|localization]] at a [[contractible type]] $R$ |  |
| $\mathbb{R} \flat$ | [[real number|real]] cohesion | [[localization of a type|localization]] at the [[real numbers]] $\mathbb{R}$ | A higher [[coinductive type]] representing the [[homotopy]] [[terminal]] [[Archimedean ordered field]] $\mathbb{R}$ |
| $\mathbb{R} \flat$ | [[Dedekind real number|real]] cohesion ([[impredicative mathematics|impredicative]]) | [[localization of a type|localization]] at the impredicative [[Dedekind real numbers]] or [[generalized Cauchy real numbers]] $\mathbb{R}$ | A [[type of all propositions]] $\Omega$ |
| $\mathbb{R}_{U} \flat$ | locally $U$-small real cohesion | [[localization of a type|localization]] at the $U$-[[Dedekind real numbers]] or $U$-[[generalized Cauchy real numbers]] $\mathbb{R}_U$ | A [[Tarski universe]] $(U, T)$ |
|  | [[unit interval]] cohesion | [[localization of a type|localization]] at the [[unit interval]] $[0, 1]$ | a higher [[coinductive type]] representing the [[homotopy]] [[terminal]] [[dyadic interval coalgebra]]. |
|  | $U$-small unit interval cohesion | [[localization of a type|localization]] at the $U$-small [[unit interval]] $[0, 1]_\mathbb{U}$ | A [[Tarski universe]] $(U, T)$. |
| $S^1 \flat$ | [[circle type cohesion]] | [[localization of a type|localization]] at the circle type | The [[circle type]] $S^1$ |

## See also

* [[shape modality]]

* [[localization of a type at a family of functions]]

* [[axiom of punctual cohesion]]

* [[axiom of sufficient cohesion]]

* [[axiom of simplicial cohesion]]

* [[axiom of real cohesion]]

## References

* {#Shulman18} [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Shulman17} [[Mike Shulman]], *Homotopy type theory: the logic of space*, New Spaces in Mathematics: Formal and Conceptual Reflections, ed. Gabriel Catren and Mathieu Anel, Cambridge University Press, 2021 ([arXiv:1703.03007](https://arxiv.org/abs/1703.03007), [doi:10.1017/9781108854429](https://doi.org/10.1017/9781108854429))

* {#Aberle24} [[C.B. Aberlé]], *Parametricity via Cohesion* &lbrack;[arXiv:2404.03825](https://arxiv.org/abs/2404.03825)&rbrack; 

[[!redirects axiom of cohesion]]
[[!redirects axioms of cohesion]]

[[!redirects axiom of strong connectedness]]
[[!redirects axioms of strong connectedness]]

[[!redirects axiom of stable local connectedness]]
[[!redirects axioms of stable local connectedness]]

[[!redirects unit interval cohesion]]
[[!redirects axiom of unit interval cohesion]]
[[!redirects axioms of unit interval cohesion]]

[[!redirects axiom C0]]
[[!redirects axiom [0, 1]-flat]]
[[!redirects axiom [0, 1] flat]]

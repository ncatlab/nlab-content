+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundational axiom
+-- {: .hide}
[[!include foundational axiom - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]], the [[0-truncation]] [[modality]] of a type $A$ can be defined by [[localization of a type]] $A$ at the [[circle type]] $S^1$. This means that a type $A$ is 0-truncated, i.e. a set, if it is $S^1$-local, which means that, in addition to [[axiom K]] and [[uniqueness of identity proofs]], there is another way to make the [[dependent type theory]] into a [[set-level type theory]]: by stipulating that every type is $S^1$-local, or that the canonical [[function]] $\mathrm{const}_{A, S^1}:A \to (S^1 \to A)$, which takes elements of $A$ to [[constant functions]] in $S^1 \to A$, is an [[equivalence of types]]. This is (tentatively) called the **axiom of circle type localization** or the axiom of $S^1$-localization. 

Assuming that one has the function $\mathrm{const}_{A, S^1}:A \to (S^1 \to A)$ defined in the [[dependent type theory]], the syntactic rules for the axiom of $S^1$-localization is given by:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A}{\Gamma \vdash \epsilon_A(f):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A}{\Gamma \vdash \eta_A(f):\mathrm{Id}_{S^1 \to A}(\mathrm{const}_{A, S^1}(\epsilon_A(f)), f)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A \quad \Gamma \vdash x:A \quad \Gamma \vdash y:\mathrm{Id}_{S^1 \to A}(\mathrm{const}_{A, S^1}(x), f)}{\Gamma \vdash c_{\epsilon_A}(f, x, y):\mathrm{Id}_{A}(\epsilon_A(f), x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A \quad \Gamma \vdash x:A \quad \Gamma \vdash y:\mathrm{Id}_{S^1 \to A}(\mathrm{const}_{A, S^1}(x), f)}{\Gamma \vdash c_{\eta_A}(f, x, y):\mathrm{hId}_{z:A.\mathrm{Id}_{S^1 \to A}(\mathrm{const}_{A, S^1}(z), f)}(\epsilon_A(f), x, c_{\epsilon_A}(f, x, y), \eta_A(f), y)}$$

In the context of [[function extensionality]], this is equivalent to

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A}{\Gamma \vdash \epsilon_A(f):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A \quad \Gamma \vdash y:S^1}{\Gamma \vdash \eta_A(f, y):\mathrm{Id}_{A}(\mathrm{const}_{A, S^1}(\epsilon_A(f)), y), f(y))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A \quad \Gamma \vdash x:A \quad \Gamma \vdash z:\prod_{y:S^1} \mathrm{Id}_{A}(\mathrm{const}_{A, S^1}(x, y), f(y))}{\Gamma \vdash c_{\epsilon_A}(f, x, z):\mathrm{Id}_{A}(\epsilon_A(f), x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash f:S^1 \to A \quad \Gamma \vdash x:A \quad \Gamma \vdash z:\prod_{y:S^1} \mathrm{Id}_{A}(\mathrm{const}_{A, S^1}(x, y), f(y))}{\Gamma \vdash c_{\eta_A}(f, x, z):\mathrm{hId}_{w:A.\prod_{y:S^1} \mathrm{Id}_{A}(\mathrm{const}_{A, S^1}(w, y), f(y))}(\epsilon_A(f), x, c_{\epsilon_A}(f, x, z), \eta_A(f), z)}$$

## Consequences
 
Since the [[boolean domain]] $\mathbb{2}$ is $S^1$-local, the axiom of $S^1$-localization implies that $S^1$ is [[compact connected]]:

\begin{theorem}
Assuming a [[type of all propositions]] $\Omega$ with type reflector $T$ and the axiom of $S^1$-localization, if the function $\mathrm{const}_{2, S^1}$ is an equivalence of types, then for all functions $P:S^1 \to \Omega$, if for all $x:S^1$, $T(P(x)) \vee \neg T(P(x))$ is contractible, then either for all $x:S^1$, $T(P(x))$ is contractible, or for all $x:S^1$, $\neg T(P(x))$ is contractible. 
\end{theorem}

\begin{proof}
If $P:S^1 \to \Omega$ is such that for all $x:S^1$, $T(P(x)) \vee \neg T(P(x))$ is contractible, then there is a function $P':S^1 \to \mathbb{2}$ into the [[booleans type]] $\mathbb{2}$ with $\delta_{P'}^{1_2}(x):(P'(x) = 1_2)) \simeq T(P(x))$ and $\delta_{P'}^{0_2}(x):(P'(x) = 0_2)) \simeq \neg T(P(x))$. Since $\mathbb{2}$ is $S^1$-local, then, by the axiom of $S^1$-localization, $P'$ is constant, which implies that either for all $x:S^1$, $T(P(x))$ is contractible, or for all $x:S^1$, $\neg T(P(x))$ is contractible. Thus, $S^1$ is compact connected 
\end{proof} 

## In spatial type theory

In [[spatial type theory]], a crisp type $\Xi \vert () \vdash A$ is discrete if the function $(-)_\flat:\flat A \to A$ is an [[equivalence of types]]. There is a variant of the above axiom called the **axiom of circle type cohesion** or **axiom $S^1 \flat$**, which states that given any crisp type $\Xi \vert () \vdash A \; \mathrm{type}$, $A$ is discrete if and only if $A$ is $S^1$-local, or if $\mathrm{const}_{A, S^1}$ is an [[equivalence of types]]. 

$$\frac{\Xi \vert () \vdash A \; \mathrm{type}}{\Xi \vert () \vdash S^1 \flat\mathrm{ax}_A:\mathrm{isEquiv}(\lambda x:\flat A.x_\flat) \simeq \mathrm{isEquiv}(\mathrm{const}_{A, S^1})}$$

This allows us to define discreteness for non-crisp types: a type $A$ is **discrete** if $A$ is $S^1$-local, resulting in a flavor of [[cohesive homotopy type theory]] where the [[shape modality]] is the [[0-truncation]] [[modality]]. This rule is equivalent to the axiom of circle type localization if every type is discrete. 

## See also

* [[set-level type theory]]

* [[axiom of set truncation]]

* [[axiom K]]

* [[uniqueness of identity proofs]]

* [[axiom of cohesion]]

[[!redirects axiom of circle type localization]]
[[!redirects axiom of S1 localization]]
[[!redirects axiom of S1-localization]]

[[!redirects axiom of circle type cohesion]]
[[!redirects axiom of S1 cohesion]]
[[!redirects axiom of S1-cohesion]]

[[!redirects axiom circle type flat]]
[[!redirects axiom S1 flat]]
[[!redirects axiom S1-flat]]

[[!redirects circle type cohesion]]
[[!redirects S1 cohesion]]
[[!redirects S1-cohesion]]

[[!redirects circle type flat]]
[[!redirects S1-flat]]
[[!redirects S1 flat]]
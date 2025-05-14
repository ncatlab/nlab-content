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

In [[dependent type theory]], the [[0-truncation]] [[modality]] of a type $A$ can be defined by [[localization of a type]] $A$ at the [[circle type]] $S^1$. This means that a type $A$ is 0-truncated, i.e. a set, if it is $S^1$-local, which means that, in addition to [[axiom K]] and [[uniqueness of identity proofs]], there is another way to make the types of a universe into sets: by stipulating that every type is $S^1$-local, or that the canonical [[function]] 
$$\mathrm{const}_{A, S^1} \equiv \lambda x:A.\lambda i:S^1.x:A \to (S^1 \to A)$$ 
which takes elements of $A$ to [[constant functions]] in $S^1 \to A$, is an [[equivalence of types]]. This is (tentatively) called the **axiom of circle type localization** or the axiom of $S^1$-localization. 

Assuming that one has the function $\mathrm{const}_{A, S^1}:A \to (S^1 \to A)$ defined in the [[dependent type theory]], the syntactic rules for the axiom of $S^1$-localization in a universe $\mathcal{U}$ is given by:

$$\frac{\Gamma \vdash A:\mathcal{U} \quad \Gamma \vdash f:S^1 \to A}{\Gamma \vdash \mathrm{circlocal}_{A}:\mathrm{isEquiv}(\mathrm{const}_{A, S^1})}$$

There is also a definitional version of $S^1$-localization which says that $\mathrm{const}_{A, S^1}$ is a definitional [[isomorphism]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:S^1 \to A \vdash \mathrm{const}_{A, S^1}^{-1}(p):A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash \mathrm{const}_{A, S^1}^{-1}(\lambda i:S^1.x) \equiv x:A}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, p:S^1 \to A \vdash \lambda i:S^1.\mathrm{const}_{A, S^1}^{-1}(p) \equiv p:S^1 \to A}$$

### Relation to axiom K

One can prove axiom K (positive copy induction rules) from the axiom of circle type localization (negative copy inference rules):

\begin{theorem}
Suppose that every type $A$ is definitionally $S^1$-local.

Then definitional [[axiom K (type theory)|axiom K]] holds: given any type $A$, and any type family $C(p)$ indexed by loops $p:S^1 \to A$ in $A$, and given any dependent function $t:\prod_{x:A} C(\lambda i:S^1.x)$ which says that for all elements $x:A$, there is an element of the type defined by substituting the constant loop of $x:A$ into $C$, $C(\lambda i:S^1.x)$, one can construct a dependent function $K_A(t):\prod_{z:S^1 \to A} C(z)$ such that for all $x:A$, $K_A(t, \lambda i:S^1.x) \equiv t(x):C(\lambda i:S^1.x)$. 
\end{theorem}

\begin{proof}
$K_A(t)$ is defined to be

$$K_A(t) \equiv \lambda p:S^1 \to A.t(\mathrm{const}_{A, S^1}^{-1}(p))$$

and by the computation rules of loop types as negative copies, one has that for all $x:A$, 

$$\mathrm{const}_{A, S^1}^{-1}(\lambda i:\mathbb{I}.x) \equiv x$$

and so by definition of $\mathrm{ind}_{S^1 \to A}(t)$ and the judgmental congruence rules for substitution, one has

$$K_A(t, \lambda i:S^1.x) \equiv t(\mathrm{const}_{A, S^1}^{-1}(\lambda i:S^1.x)) \equiv t(x)$$
\end{proof}

One has the following analogies between localization at a specific type and the type theoretic letter rule that it proves:

| localization rule | type theoretic letter rule |
|-------------------|----------------------------|
| [[I-localization|$\mathbb{I}$-localization]] | [[J-rule]] |
| [[S1-localization|$S^1$-localization]] | [[K-rule]] |


## Consequences
 
Since the [[type of booleans]] $\mathbb{2}$ is $S^1$-local, the axiom of $S^1$-localization implies that $S^1$ is [[compact connected]]:

\begin{theorem}
Assuming [[propositional truncation]], where $\Omega$ is the type of all $\mathcal{U}$-small propositions with type reflector $T$, and the axiom of $S^1$-localization, if the function $\mathrm{const}_{2, S^1}$ is an equivalence of types, then for all functions $P:S^1 \to \Omega$, if for all $x:S^1$, $T(P(x)) \vee \neg T(P(x))$ is contractible, then either for all $x:S^1$, $T(P(x))$ is contractible, or for all $x:S^1$, $\neg T(P(x))$ is contractible. 
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

* [[interval type localization]]

* [[axiom of cohesion]]

[[!redirects axiom of circle type localization]]
[[!redirects axiom of S1 localization]]
[[!redirects axiom of S1-localization]]

[[!redirects circle type localization]]
[[!redirects S1 localization]]
[[!redirects S1-localization]]

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
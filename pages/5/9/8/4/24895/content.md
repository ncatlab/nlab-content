
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
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

**$\mathbb{A}^1$-cohesive homotopy type theory**,  **affine-cohesive homotopy type theory**, or **algebraic-cohesive homotopy type theory** is a version of [[cohesive homotopy type theory]] which has an [[affine line]] [[type]] $\mathbb{A}^1$ and the [[axiom of A1-cohesion|axiom of $\mathbb{A}^1$-cohesion]]. $\mathbb{A}^1$-cohesive homotopy type theory provides a [[synthetic mathematics|synthetic]] [[foundation]] for [[A1-homotopy theory|$\mathbb{A}^1$-homotopy theory]], where the affine line is the standard [[affine line]] in the [[Nisnevich site]] of [[smooth schemes]] of [[finite type]] over a [[Noetherian scheme]]. 

### Motivic homotopy type theory

[[Mitchell Riley]]'s [[bunched logic|bunched]] [[linear homotopy type theory]] is a synthetic foundations for [[stable homotopy theory]]. This means that there should be an $\mathbb{A}^1$-cohesive [[bunched logic|bunched]] [[linear homotopy type theory]] which behaves as a synthetic foundations for [[motivic homotopy theory]]. 

## Presentation

Similarly to [[real-cohesive homotopy type theory]], we assume a [[spatial type theory]] presented with crisp term judgments $a::A$. In addition, we also assume the spatial type theory has an [[affine line]] [[type]] $\mathbb{A}^1$, and $\mathbb{A}^1$-[[localization of a type at a family of functions|localizations]] $\mathcal{L}_{\mathbb{A}^1}(-)$. 

Given a type $A$, let us define $\mathrm{const}_{A, \mathbb{A}^1}:A \to (\mathbb{A}^1 \to A)$ to be the type of all constant functions in the [[affine line]] $\mathbb{A}^1$:
$$\delta_{\mathrm{const}_{A, \mathbb{A}^1}}(a, r):\mathrm{const}_{A, \mathbb{A}^1}(a)(r) =_A a$$
There is an equivalence $\mathrm{const}_{A, 1}:A \simeq (1 \to A)$ between the type $A$ and the type of functions from the [[unit type]] $1$ to $A$. 
Given types $B$ and $C$ and a function $F:(B \to A) \to (C \to A)$, type $A$ is **$F$-[[localization of a type at a family of functions|local]]** if the function $F:(B \to A) \to (C \to A)$ is an [[equivalence of types]]. 

A crisp type $\Xi \vert () \vdash A$ is **discrete** if the function $(-)_\flat:\flat A \to A$ is an [[equivalence of types]]. 

The **axiom of $\mathbb{A}^1$-cohesion** states that for the crisp affine line $\Xi \vert () \vdash \mathbb{A}^1 \; \mathrm{type}$, given any crisp type $\Xi \vert () \vdash A \; \mathrm{type}$, $A$ is discrete if and only if $A$ is $(\mathrm{const}_{A, 1}^{-1} \circ \mathrm{const}_{A, \mathbb{A}^1})$-local. 

This allows us to define discreteness for non-crisp types: a type $A$ is **discrete** if $A$ is $(\mathrm{const}_{A, 1}^{-1} \circ \mathrm{const}_{A, \mathbb{A}^1})$-local. 

The [[shape modality]] in $\mathbb{A}^1$-cohesive homotopy type theory is then defined as the $\mathbb{A}^1$-localization $\esh(A) \coloneqq \mathcal{L}_{\mathbb{A}^1}(A)$, which ensures that the shape of $\mathbb{A}^1$ itself is a [[contractible type]]. 

## See also

* [[cohesive homotopy type theory]]
* [[A1-homotopy theory|$\mathbb{A}^1$-homotopy theory]]
* [[axiom of A1-cohesion|axiom of $\mathbb{A}^1$-cohesion]]

## References

For the presentation of the underlying [[spatial type theory]] used for $\mathbb{A}^1$-cohesive homotopy type theory, see:

* [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

[[!redirects A1-cohesive homotopy type theory]]
[[!redirects A1 cohesive homotopy type theory]]

[[!redirects affine-cohesive homotopy type theory]]
[[!redirects affine cohesive homotopy type theory]]

[[!redirects algebraic-cohesive homotopy type theory]]
[[!redirects algebraic cohesive homotopy type theory]]
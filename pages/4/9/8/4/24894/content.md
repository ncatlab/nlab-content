
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
=--
=--

\tableofcontents

## Idea

**$\mathbb{R}$-cohesive homotopy type theory** or **real-cohesive homotopy type theory** is a version of [[cohesive homotopy type theory]] which has the [[axiom of real cohesion]]. It provides a [[synthetic mathematics|synthetic]] [[foundation]] for [[topology]], [[real analysis]], [[classical homotopy theory]], and [[algebraic topology]]. A model of real-cohesive homotopy type theory is the [[Euclidean-topological infinity-groupoids]]. 

## Presentation

We assume a [[spatial type theory]] presented with crisp term judgments $a::A$. In addition, we also assume the spatial type theory has a [[Dedekind real numbers]] [[type]] $\mathbb{R}$, and $\mathbb{R}$-[[localization of a type at a family of functions|localizations]] $\mathcal{L}_{\mathbb{R}}(-)$. 

Given a type $A$, let us define $\mathrm{const}_{A, \mathbb{R}}:A \to (\mathbb{R} \to A)$ to be the type of all constant functions in the [[Dedekind real numbers]] $\mathbb{R}$:
$$\delta_{\mathrm{const}_{A, \mathbb{R}}}(a, r):\mathrm{const}_{A, \mathbb{R}}(a)(r) =_A a$$
There is an equivalence $\mathrm{const}_{A, 1}:A \simeq (1 \to A)$ between the type $A$ and the type of functions from the [[unit type]] $1$ to $A$. 
Given types $B$ and $C$ and a function $F:(B \to A) \to (C \to A)$, type $A$ is **$F$-[[localization of a type at a family of functions|local]]** if the function $F:(B \to A) \to (C \to A)$ is an [[equivalence of types]]. 

A crisp type $\Xi \vert () \vdash A$ is **discrete** if the function $(-)_\flat:\flat A \to A$ is an [[equivalence of types]]. 

The **axiom of $\mathbb{R}$-cohesion** states that for the crisp affine line $\Xi \vert () \vdash \mathbb{R} \; \mathrm{type}$, given any crisp type $\Xi \vert () \vdash A \; \mathrm{type}$, $A$ is discrete if and only if $A$ is $(\mathrm{const}_{A, 1}^{-1} \circ \mathrm{const}_{A, \mathbb{R}})$-local. 

This allows us to define discreteness for non-crisp types: a type $A$ is **discrete** if $A$ is $(\mathrm{const}_{A, 1}^{-1} \circ \mathrm{const}_{A, \mathbb{R}})$-local. 

The [[shape modality]] in $\mathbb{R}$-cohesive homotopy type theory is then defined as the $\mathbb{R}$-localization $\esh(A) \coloneqq \mathcal{L}_{\mathbb{R}}(A)$, which ensures that the shape of $\mathbb{R}$ itself is a [[contractible type]]. 

## See also

* [[cohesive homotopy type theory]]
* [[axiom of real cohesion]]
* [[Euclidean-topological infinity-groupoid]]

## References

* [[Mike Shulman]]: *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science **28** 6 (2018) 856-941 &lbrack;[arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147)&rbrack;

[[!redirects real-cohesive homotopy type theory]]
[[!redirects real cohesive homotopy type theory]]
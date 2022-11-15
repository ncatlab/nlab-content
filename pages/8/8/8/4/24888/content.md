\tableofcontents

## Idea
 {#Idea}

Axioms of [[cohesion]] are certain [[axioms]] added to any [[dependent type theory]] with the [[sharp modality]] and [[flat modality]] in order to define the [[shape modality]] for [[cohesive homotopy type theory]]. In particular, the *axiom of real cohesion* plays a role in defining [[real-cohesive homotopy type theory]] (the setting for [[classical homotopy theory]] and [[algebraic topology]]), and the *axiom of motivic cohesion* would play a role in defining a hypothetical unstable motivic homotopy type theory (the setting for unstable [[motivic homotopy theory]]). 

## Definition

We assume a [[dependent type theory]] with crisp term judgments $a::A$ in addition to the usual (cohesive) type and term judgments $A \; \mathrm{type}$ and $a:A$, as well as context judgments $\Xi \vert \Gamma \; \mathrm{ctx}$ where $\Xi$ is a list of crisp term judgments, and $\Gamma$ is a list of cohesive term judgments. A crisp type is a type in the context $\Xi \vert ()$, where $()$ is the empty list of cohesive term judgments. In addition, we also assume the dependent type theory has [[typal equality]] and [[judgmental equality]]. 

### Axioms of cohesion for single types

Given a type $A$, let us define $\mathrm{const}_{A, R}:A \to (R \to A)$ to be the type of all constant functions in $R$:
$$\delta_{\mathrm{const}_{A, R}}(a, r):\mathrm{const}_{A, R}(a)(r) =_A a$$
There is an equivalence $\mathrm{const}_{A, 1}:A \simeq (1 \to A)$ between the type $A$ and the type of functions from the [[unit type]] $1$ to $A$. 
Given types $B$ and $C$ and a function $F:(B \to A) \to (C \to A)$, type $A$ is **$F$-[[localization of a type at a family of functions|local]]** if the function $F:(B \to A) \to (C \to A)$ is an [[equivalence of types]]. 

A crisp type $\Xi \vert () \vdash A$ is **discrete** if the function $(-)_\flat:\flat A \to A$ is an [[equivalence of types]]. 

The **axiom of cohesion** for type $R$ states that there is a crisp type $\Xi \vert () \vdash R \; \mathrm{type}$ such that given any crisp type $\Xi \vert () \vdash A \; \mathrm{type}$, $A$ is discrete if and only if $A$ is $(\mathrm{const}_{A, 1}^{-1} \circ \mathrm{const}_{A, R})$-local. 

This allows us to define discreteness for non-crisp types: a type $A$ is **discrete** if $A$ is $(\mathrm{const}_{A, 1}^{-1} \circ \mathrm{const}_{A, R})$-local. Another consequence is that the [[shape]] of $R$ is [[contractible]].

### Axioms of cohesion for families of types

Given a type $A$ and type family $R(i)$ indexed by index type $I$, let us define $\mathrm{const}_{A, R}:\prod_{i:I} A \to (R(i) \to A)$ to be the type of all constant functions in each $R(i)$:
$$\delta_{\mathrm{const}_{A, R}}(i, a, r):\mathrm{const}_{A, R}(i)(a)(r) =_A a$$
There is an equivalence $\mathrm{const}_{A, 1}:A \simeq (1 \to A)$ between the type $A$ and the type of functions from the [[unit type]] $1$ to $A$. 
Given type families $B(i)$ and $C(i)$ and a function $F:\prod_{i:I} (B(i) \to A) \to (C(i) \to A)$, type $A$ is **$F$-[[localization of a type at a family of functions|local]]** if for all $i:I$ the function $F:(B(i) \to A) \to (C(i) \to A)$ is an [[equivalence of types]]. 

A crisp type $\Xi \vert () \vdash A$ is **discrete** if the function $(-)_\flat:\flat A \to A$ is an [[equivalence of types]]. 

The **axiom of cohesion** for the family of types $R(i)$ states that there is an index type $\Xi \vert () \vdash I \; \mathrm{type}$ and a crisp type family $\Xi, i::I \vert () \vdash R \; \mathrm{type}$ such that given any crisp type $\Xi \vert () \vdash A \; \mathrm{type}$, $A$ is discrete if and only if $A$ is $(\mathrm{const}_{A, 1}^{-1} \circ \mathrm{const}_{A, R})$-local. 

This allows us to define discreteness for non-crisp types: a type $A$ is **discrete** if $A$ is $(\mathrm{const}_{A, 1}^{-1} \circ \mathrm{const}_{A, R})$-local. Another consequence is that the [[shape]] of each $R(i)$ is [[contractible]].

## Examples

There are a number of axioms which in general could be called an axiom of cohesion for families of types $R(i)$. The most general such axiom of cohesion is called **stable local connectedness** or **axiom C0**, which imposes no other restrictions on each $R(i)$. If we additionally assume that the each type $R(i)$ is pointed with point $0(i):R(i)$, then the axiom becomes **punctual local connectedness** or **axiom C1**, and if we additionally assume that each type $R(i)$ is a non-trivial bi-pointed set, with points $0(i):R(i)$, $1(i):R(i)$, and witnesses $\tau_0(i):\mathrm{isSet}(R(i))$ and $\mathrm{nontriv}(i):(0 =_{R(i)} 1) \to \emptyset$, then the axiom becomes **contractible codiscreteness** or **axiom C2**. 

If we additionally assume that $I$ is contractible and the type $R$ up to equivalence is a [[Dedekind complete]] [[Archimedean field|Archimedean]] [[ordered field|ordered]] [[lattice]] [[field]] (and usually written as $\mathbb{R}$), then the axiom becomes **real cohesion** or **axiom $\mathbb{R}$-flat**. Alternatively, if we assume that $I$ is contractible and the type $R$ up to equivalence is a [[homotopy]] [[terminal object|terminal]] [[dyadic interval coalgebra]], then the axiom becomes **unit interval cohesion** or **axiom $[0, 1]$-flat**, where $[0, 1]$ is the Dedekind real [[unit interval]]; this implies real cohesion, as proven in [[continuum]]. 

| number/symbol | name | requirement |
|--------|------|-----------|
| $C_0$ | stable local connectedness | each $R(i)$ is a [[type]] for all $i:I$ |
| $C_1$ | punctual local connectedness | each $R(i)$ is a [[pointed type]] for all $i:I$ |
| $C_2$ | contractible codiscreteness | each $R(i)$ is a non-trivial [[bi-pointed type|bi-pointed]] [[h-set]] for all $i:I$ |
| $\mathbb{R} \flat$ | [[Dedekind real number|real]] cohesion | Assuming the type theory has a [[type of all propositions]] $\Omega$, $R$ is a [[Dedekind complete]] or [[Cauchy complete]] (by [[Cauchy filters]]) [[Archimedean field|Archimedean]] [[ordered field|ordered]] [[lattice]] [[field]] |
| $\mathbb{R}_U \flat$ | locally $U$-small real cohesion | Given [[type universe]] $U$, $R$ is a $U$-[[Dedekind complete]] or $U$-[[Cauchy complete]] (by [[Cauchy filters]] or [[Cauchy nets]] in $U$) [[Archimedean field|Archimedean]] [[ordered field|ordered]] [[lattice]] [[field]] |
| $\mathbb{R}^\mathrm{loc} \flat$ | [[locale of real numbers|localic real]] cohesion | Assuming the type theory has a [[type of all propositions]] $\Omega$, $R$ is a [[localic completion]] of an [[Archimedean field|Archimedean]] [[ordered field|ordered]] [[lattice]] [[field]]. Same as real cohesion in the presence of [[excluded middle]]. |
| $\mathbb{R}_U^\mathrm{loc} \flat$ | locally $U$-small [[locale of real numbers|localic real]] cohesion | Given [[type universe]] $U$, $R$ is a $U$-[[localic completion]] of an [[Archimedean field|Archimedean]] [[ordered field|ordered]] [[lattice]] [[field]] |
| $[0, 1] \flat$ | [[unit interval]] cohesion | $R$ is a higher [[coinductive type]] representing the [[homotopy]] [[terminal]] [[dyadic interval coalgebra]] |
| $[0, 1]_U \flat$ | $U$-small unit interval cohesion | Given [[type universe]] $U$, $R$ is a [[homotopy]] [[terminal]] [[dyadic interval coalgebra]] in $U$ |
| $\mathbb{A}^1 \flat$ | unstable [[motivic homotopy theory|motivic]] cohesion/ $\mathbb{A}^1$-cohesion | $R$ is an [[affine line]] |

## See also

* [[shape modality]]

* [[localization of a type at a family of functions]]

## References

* [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

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

[[!redirects unit interval cohesion]]
[[!redirects axiom of unit interval cohesion]]
[[!redirects axioms of unit interval cohesion]]

[[!redirects motivic cohesion]]
[[!redirects axiom of motivic cohesion]]
[[!redirects axioms of motivic cohesion]]

[[!redirects axiom C0]]
[[!redirects axiom C1]]
[[!redirects axiom C2]]
[[!redirects axiom R-flat]]
[[!redirects axiom R flat]]
[[!redirects axiom [0, 1]-flat]]
[[!redirects axiom [0, 1] flat]]
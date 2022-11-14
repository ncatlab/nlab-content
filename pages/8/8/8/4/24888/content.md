\tableofcontents

## Definition

We assume a [[dependent type theory]] with crisp term judgments $a::A$ in addition to the usual (cohesive) type and term judgments $A \; \mathrm{type}$ and $a:A$, as well as context judgments $\Xi \vert \Gamma \; \mathrm{ctx}$ where $\Xi$ is a list of crisp term judgments, and $\Gamma$ is a list of cohesive term judgments. A crisp type is a type in the context $\Xi \vert ()$, where $()$ is the empty list of cohesive term judgments. In addition, we also assume the dependent type theory has [[typal equality]] and [[judgmental equality]]. 

**Axiom C0** states that there is a crisp type family $\Xi, i::I \vert () \vdash R \; \mathrm{type}$ such that given any crisp type $\Xi \vert () \vdash A \; \mathrm{type}$, $A$ is discrete if and only if for all $i:I$ the function $\mathrm{const}_{A, R}(i):A \to (R_i \to A)$ is an equivalence of types. 

$$\frac{\Xi \vert () \; \mathrm{ctx}}{\Xi, i::I \vert () \vdash R \; \mathrm{type}}$$
$$\frac{\Xi \vert () \vdash A \; \mathrm{type}}{\Xi, i::I \vert () \vdash \mathrm{const}_{A, R}(i):A \to (R_i \to A)}$$
$$\frac{\Xi \vert () \vdash A \; \mathrm{type}}{\Xi, i::I \vert () \vdash C0_A:\mathrm{isEquiv}(\mathrm{const}_{A, R}(i))}$$

## See also

* [[axiom R-flat]]
* [[shape modality]]

## References

* [[Mike Shulman]], *Brouwer's fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))
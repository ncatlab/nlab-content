\tableofcontents

## Definition 

A [[double category]] $\mathbb{D} = (D_{0}, D_{1})$ is *right-connected* if its [[identity morphisms|identity]]-assigning map $id \colon D_{0} \rightarrow D_{1}$ is [[right adjoint]] to its [[codomain]]-assigning map $cod \colon D_{1} \rightarrow D_{0}$. 

Dually, a double category $\mathbb{D} = (D_{0}, D_{1})$ is *left-connected* if its [[identity morphisms|identity]]-assigning map $id \colon D_{0} \rightarrow D_{1}$ is [[left adjoint]] to its [[domain]]-assigning map $dom \colon D_{1} \rightarrow D_{0}$. 

We can unpack the definition of right-connectedness as follows. 
Let $\rho \colon 1_{D_{1}} \Rightarrow id \circ cod$ denote the [[unit of an adjunction|unit]] of the adjunction $cod \dashv id$, and let the [[counit of an adjunction|counit]] be the identity natural transformation by the axioms of an [[internal category]]. 
Given a vertical morphism $f \colon A \nrightarrow B$ in $\mathbb{D}$, the component of the unit may be depicted as follows: 
\begin{tikzcd}
A 
\arrow[rd, phantom, "\rho_{f}"]
\arrow[d, "f"', "\bullet"{anchor=center}]
\arrow[r, "Uf"]
& B
\arrow[d, "id_{B}", "\bullet"{anchor=center}]
\\
B
\arrow[r, "1_{B}"']
& B
\end{tikzcd}
The [[triangle identities]] of an adjunction imply that: 

1. the bottom boundary of $\rho_{f}$ is an identity morphism;
2. the component of $\rho$ at an identity vertical morphism $id_{A} \colon A \nrightarrow A$ is the identity cell on $A$.

Given a cell $\alpha$ in $\mathbb{D}$, naturality of $\rho$ states that the cells 
  \begin{tikzcd}
    A
    \arrow[r, "h"]
    \arrow[d, "\bullet"{anchor=center}, "f"']
    \arrow[rd, phantom, "\alpha"]
    & C
    \arrow[d, "\bullet"{anchor=center}, "g"]
    \arrow[r, "Ug"]
    \arrow[rd, phantom, "\rho_{g}"]
    & D
    \arrow[d, "\bullet"{anchor=center}, "id_{D}"]
    \\
    B
    \arrow[r, "k"']
    & D
    \arrow[r, "1_{D}"']
    & D
    \end{tikzcd}
and 
    \begin{tikzcd}
    A
    \arrow[r, "Uf"]
    \arrow[d, "\bullet"{anchor=center}, "f"']
    \arrow[rd, phantom, "\rho_{f}"]
    & B
    \arrow[d, "\bullet"{anchor=center}, "id_{B}"]
    \arrow[r, "k"]
    \arrow[rd, phantom, "id_{k}"]
    & D
    \arrow[d, "\bullet"{anchor=center}, "id_{D}"]
    \\
    B
    \arrow[r, "1_{B}"']
    & B
    \arrow[r, "k"']
    & D
    \end{tikzcd}
are equal. 

## Examples

\begin{example}
For each category $C$, the [[double category of squares]] $\mathbb{S}q(C)$ is right-connected. 
\end{example}

\begin{example}
For each [[algebraic weak factorization system]] $(K, R, L)$ on a category $K$, the double category of $R$-algebras is right-connected. 
\end{example}

## References

The notion was first defined in Section 3.5 of the paper:

 * {#BourkeGarner2016a} [[John Bourke]], [[Richard Garner]], _Algebraic weak factorisation systems I: Accessible AWFS_, Journal of Pure and Applied Algebra, **220**, 2016 ([arXiv:1412.6559](https://arxiv.org/abs/1412.6559), [doi:10.1016/j.jpaa.2015.06.002](https://doi.org/10.1016/j.jpaa.2015.06.002))

Further discussion of right-connected double categories appears in Section 2.5 of the paper: 

 * {#BourkeGarner2016b} [[John Bourke]], [[Richard Garner]], _Algebraic weak factorisation systems II: Categories of weak maps_, Journal of Pure and Applied Algebra, **220**, 2016 ([arXiv:1412.6560](https://arxiv.org/abs/1412.6560), [doi:10.1016/j.jpaa.2015.06.003](https://doi.org/10.1016/j.jpaa.2015.06.003))

[[!redirects right-connected double categories]]
[[!redirects left-connected double category]]
[[!redirects left-connected double categories]]
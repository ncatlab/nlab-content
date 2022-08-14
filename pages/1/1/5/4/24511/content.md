+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of algebra modality is used to define [[differential categories|codifferential categories]]. However, it could be use in other types of [[doctrines|categorical doctrines]].

## Definition

\begin{definition}
An [[algebra modality]] in a [[symmetric monoidal category]] $(\mathcal{C}, \otimes, I)$ is given by a [[monad]] $(S,m,u)$ and two [[natural transformations]] $\eta:I \rightarrow S(A)$ and $\nabla:S(A) \otimes S(A) \rightarrow S(A)$ such that for every $A \in \mathcal{C}$, $(S(A), \nabla, \eta)$ is a [[commutative monoid]] in $(\mathcal{C},\otimes,I)$ and this diagram commutes:
\begin{tikzcd}
S(S(A)) \otimes S(S(A)) \arrow[dd, "m \otimes m"'] \arrow[rr, "\nabla"] &  & S(S(A)) \arrow[dd, "m"] \\
                                                                            &  &                           \\
S(A) \otimes S(A) \arrow[rr, "\nabla"']                                   &  & S(A)                    
\end{tikzcd}
\end{definition}

## Properties

\begin{proposition}
If $R$ is a commutative rig, then the symmetric algebra defines an algebra modality in $Mod_{R}$.

* $Sym(A)$ is the [[symmetric algebra]] of the module $A$.
* We have $\nabla_{A}:Sym(A) \otimes Sym(A) \rightarrow Sym(A)$.
* We have $\eta_{A}:A \rightarrow Sym(A)$.
* The unit $A \rightarrow Sym(A)$ of the monad is just the injection $x \mapsto x$.
* The multiplication $Sym(Sym(A)) \rightarrow Sym(A)$ of the monad is given on pure tensors by $(x_{1}^{(1)} \otimes_{s} ... \otimes_{s} x_{n_{1}}^{(1)}) \boxtimes_{s} ... \boxtimes_{s}  (x_{1}^{(p)} \otimes_{s} ... \otimes_{s} x_{n_{p}}^{(p)}) \mapsto x_{1}^{(1)} \otimes_{s} ... \otimes_{s} x_{n_{1}}^{(1)} \otimes ... \otimes x_{1}^{(p)} \otimes_{s} ... \otimes_{s} x_{n_{p}}^{(p)}$.  It is a kind of composition of polynomials.

\end{proposition}

\begin{proposition}
[[rigs|Commutative rigs]] are exactly the [[algebra over a monad|algebras]] over the algebra modality $Sym$ in the category of commutative monoids.
\end{proposition}

## References

Algebra modalities are part of the definition of a codifferential category ie. a category $\mathcal{C}$ such that $\mathcal{C}^{op}$ is a differential category.

Differential categories were introduced in:

*  {#BluteCocketSeely06} [[R. F. Blute]], [[J. R. B. Cockett]], and [[R. A. G. Seely]]: _Differential categories_. Math. Struct. Comput. Sci. 16(06), 1049–1083 (2006) ([doi:10.1017/S0960129506005676](https://doi.org/10.1017/S0960129506005676))

and revised in:

* [[Richard Blute]], [[Robin Cockett]], [[Jean-Simon Lemay]] and [[Robert Seely]], _Differential categories revisited,_ Appl. Categ. Struct. 28, 171-235 (2020). ([arXiv:1806.04804](https://arxiv.org/abs/1806.04804), [doi:10.1007/s10485-019-09572-y](https://doi.org/10.1007/s10485-019-09572-y))
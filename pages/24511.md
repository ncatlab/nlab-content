+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
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

The notion of algebra modality is used to define [[differential categories]]. However, it could be use in other types of [[doctrines|categorical doctrines]].

## Definition

\begin{definition}
An [[algebra modality]] in a [[symmetric monoidal category]] $(\mathcal{C}, \otimes, I)$ is given by a [[monad]] $(S,m,u)$ and two [[natural transformations]] $\eta:I \rightarrow S(A)$ and $\nabla:S(A) \otimes S(A) \rightarrow S(A)$ such that for every $A \in \mathcal{C}$, $(S(A), \nabla, \eta)$ is a [[commutative monoid]] in $(\mathcal{C},\otimes,I)$ and this diagram commutes:
\begin{tikzcd}
S(S(A)) \otimes S(S(A)) \arrow[dd, "m \otimes m"'] \arrow[rr, "\nabla"] &  & S(S(A)) \arrow[dd, "m"] \\
                                                                            &  &                           \\
S(A) \otimes S(A) \arrow[rr, "\nabla"']                                   &  & S(A)                    
\end{tikzcd}
\end{definition}

## References

Algebra modalities are part of the definition of a codifferential category ie. a category $\mathcal{C}$ such that $\mathcal{C}^{op}$ is a differential category.

Differential categories were introduced in:

*  {#BluteCocketSeely06} [[R. F. Blute]], [[J. R. B. Cockett]], and [[R. A. G. Seely]]: _Differential categories_. Math. Struct. Comput. Sci. 16(06), 1049–1083 (2006) ([doi:10.1017/S0960129506005676](https://doi.org/10.1017/S0960129506005676))

and revised in:

* [[Richard Blute]], [[Robin Cockett]], [[Jean-Simon Lemay]] and [[Robert Seely]], _Differential categories revisited,_ Appl. Categ. Struct. 28, 171-235 (2020). ([arXiv:1806.04804](https://arxiv.org/abs/1806.04804), [doi:10.1007/s10485-019-09572-y](https://doi.org/10.1007/s10485-019-09572-y))
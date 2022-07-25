
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

The notion of *differential categories* ([Blute, Cocket & Seely 2006](#BluteCocketSeely06) is meant to provide [[categorical semantics]] for 
[[differential linear logic]] ([Ehrhardt & Regnier 2009](#EhrhardtRegnier09)) which in turn is meant to be a [[syntax|syntactic]] [[proof theory|proof-theoretic]] approach to [[differential calculus]].

## Definition and example

We give the definition of a codifferential category which is the dual of a differential category in the sense that a codifferential category is a category $\mathcal{C}$ such that $\mathcal{C}^{op}$ is a differential category and a differential category is a category $\mathcal{C}$ such that $\mathcal{C}^{op}$ is a codifferential category. Codifferential categories are more intuitive mathematically because they involve monoids and monads instead of comonoids and monads, while differential categories are closer to [[linear logic]] where we have comonads and [[differential linear logic]] where we have comonads and comonoids.

In the following sequence of definitions, the object $!A$ must be interpreted as if it was a space of smooth functions with variables in $A$. 

\begin{definition}
A CMon-enriched [[symmetric monoidal category]] is a [[symmetric monoidal category]] $\mathcal{C}$ such that each hom-set $\mathcal{C}[A,B]$ is a [[commutative monoid]] (in Set) and $- \otimes -$ as well as $-;-$ are bilinear ie. preserve sums and the zero in each variable.
\end{definition}

\begin{definition}
An algebra modality in a [[symmetric monoidal category]] $(\mathcal{C}, \otimes, I)$ is given by a [[monad]] $(!,m,u)$ and two [[natural transformations]] $\eta:I \rightarrow !A$ and $\nabla:!A \otimes !A \rightarrow !A$ such that for every $A \in \mathcal{C}$, $(!A, \nabla, \eta)$ is a [[commutative monoid]] in $(\mathcal{C},\otimes,I)$ and this diagram commutes:
\begin{tikzcd}
!!A \otimes !!A \arrow[dd, "m \otimes m"'] \arrow[rr, "\nabla"] &  & !!A \arrow[dd, "m"] \\
                                                                            &  &                           \\
!A \otimes !A \arrow[rr, "\nabla"']                                   &  & !A                    
\end{tikzcd}
\end{definition}

The multiplication of the monad must be interpreted as the composition of smooth functions.

\begin{definition}
A codifferential category is a CMon-enriched [[symmetric monoidal category]] together with an algebra modality and a deriving transformation ie. a [[natural transformation]] $d:!A \rightarrow !A \otimes A$ such that the following diagrams commute:

* [[Leibniz rule]]:
\begin{tikzcd}
!A \arrow[rrrrr, "d"]                                                                                &  &  &  &  & !A \otimes A                                               \\
                                                                                                        &  &  &  &  &                                                               \\
!A \otimes !A \arrow[uu, "\nabla"] \arrow[rrrrr, "(d \otimes 1)(1\otimes \gamma) + 1 \otimes d"'] &  &  &  &  & !A \otimes \!A \otimes A \arrow[uu, "\nabla \otimes 1"']
\end{tikzcd}
It expresses that the differential of a product of two functions is the sum of the differential of the first function multiplied by the second one and the first function multiplied by the differential of the second one. 

* [[chain rule|Chain rule]]:
\begin{tikzcd}
!!A \otimes !A \arrow[rrr, "m \otimes d"] &  &  & !A \otimes !A \otimes A \arrow[rrd, "\nabla \otimes 1"] &  &                 \\
                                                   &  &  &                                                               &  & !A \otimes A \\
!!A \arrow[rrr, "m"'] \arrow[uu, "d"]        &  &  & !A \arrow[rru, "d"']                                       &  &                
\end{tikzcd}

This diagram is the most tricky one. It expresses that the differential of the composition of two smooth functions is equal to the differential of the external function applied to the internal function multiplied by the differential of the internal function.

* Linear rule:
\begin{tikzcd}
A \arrow[dd, "u"'] \arrow[rrdd, "\eta \otimes 1"] &  &                 \\
                                                  &  &                 \\
!A \arrow[rr, "d"']                            &  & !A \otimes A
\end{tikzcd}

It expresses that the differential of a vector, as a formal homogeneous polynomial of degree $1$ is more or less this vector.

* Schwarz rule:
\begin{tikzcd}
!A \otimes A \arrow[rrrr, "d \otimes 1"] &  &                                            &  & !A \otimes A \otimes A \arrow[dd, "1 \otimes \gamma"] \\
                                            &  &                                            &  &                                                          \\
!A \arrow[uu, "d"] \arrow[rr, "d"']      &  & !A \otimes A \arrow[rr, "d \otimes 1"'] &  & !A \otimes A \otimes A                               
\end{tikzcd}

It expresses that the second differential of a function is invariant by permutation of the two variables with respect to we differentiate successively.

\end{definition}

\begin{example}
If $\mathbb{K}$ is a field, then $Vect_{\mathbb{K}}$ is a codifferential category.

* We define $!A = S(A)$, the symmetric algebra on the vector space $A$.
* It is a commutative algebra as usual.
* The unit $A \rightarrow S(A)$ of the monad is just the injection $x \mapsto x$.
* The multiplication $S(S(A)) \rightarrow S(A)$ of the monad is given on pure tensors by $(x_{1}^{(1)} \otimes_{s} ... \otimes_{s} x_{n_{1}}^{(1)}) \boxtimes_{s} ... \boxtimes_{s}  (x_{1}^{(p)} \otimes_{s} ... \otimes_{s} x_{n_{p}}^{(p)}) \mapsto x_{1}^{(1)} \otimes_{s} ... \otimes_{s} x_{n_{1}}^{(1)} \otimes ... \otimes x_{1}^{(p)} \otimes_{s} ... \otimes_{s} x_{n_{p}}^{(p)}$. It is a kind of composition of polynomials.
* The deriving transformation $S(A) \rightarrow S(A) \otimes A$ is defined on pure tensors by $x_{1} \otimes_{s} ... \otimes_{s} x_{n} \mapsto \underset{1 \le k \le n}{\sum}(x_{1} \otimes_{s} ... \otimes_{s} x_{k-1} \otimes_{s} x_{k+1} \otimes_{s} ... \otimes_{s} x_{n}) \otimes x_{k}$. For instance, if $X,Y,Z$ is a basis of $A$, then $d(X^{2}+YZ) = 2X \otimes X + Y \otimes Z + Z \otimes Y$.

\end{example}

## Related concepts

* [[cartesian differential category]]

* [[differential cohesion]]

* [[tangent category]], [[tangent (∞,1)-category]]


## References

The notion is due to:

*  {#BluteCocketSeely06} [[R. F. Blute]], [[J. R. B. Cockett]], and [[R. A. G. Seely]]: _Differential categories_. Math. Struct. Comput. Sci. 16(06), 1049–1083 (2006) ([doi:10.1017/S0960129506005676](https://doi.org/10.1017/S0960129506005676))

* [[Richard Blute]], [[Robin Cockett]], [[Jean-Simon Lemay]] and [[Robert Seely]], _Differential categories revisited,_ Appl. Categ. Struct. 28, 171-235 (2020). ([arXiv:1806.04804](https://arxiv.org/abs/1806.04804), [doi:10.1007/s10485-019-09572-y](https://doi.org/10.1007/s10485-019-09572-y))

following discussion of [[differential linear logic]] in:

* {#EhrhardtRegnier09} [[Thomas Ehrhard]], [[Laurent Regnier]]: _The differential lambda-calculus_, Theor. Comput. Sci. **309** 1 (2003) 1–41  (<a href="https://doi.org/10.1016/S0304-3975(03)00392-X">doi:10.1016/S0304-3975(03)00392-X</a>)

* [[Thomas Ehrhard]], [[Laurent Regnier]]: _Differential interaction nets,_ Theor. Comput. Sci. **364** 2 (2006) 166–195 ([doi:10.1016/j.tcs.2006.08.003](https://doi.org/10.1016/j.tcs.2006.08.003))

[[!redirects differential categories]]
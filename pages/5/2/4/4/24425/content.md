## Idea

A graded codifferential category is like a [[codifferential category]] but where the algebra modality is replaced by a graded algebra modality. Whereas $FVec_{\mathbb{K}}$ is only a trivial codifferential category, with all the structure equal to zero, $FVec_{\mathbb{K}}$ is a non-trivial codifferential category.

## Definition

We will use [[graded monads]] with grading in the multiplicative monoid of a commutative [[rig]]. Also, the term rig must be read as "commutative rig" below.
\begin{definition}
Let $R$ be a rig. A $R$-graded monad in a category $\mathcal{C}$ is given by a family $(S_{r}:\mathcal{C} \rightarrow \mathcal{C})_{r \in R}$ of endofunctors, a family $(m_{r,s}A:S_{r}(S_{s}(A)) \rightarrow S_{rs}(A))_{r,s \in R}$ of natural transformations and a natural transformation $u:A \rightarrow S_{1}(A)$ such that:

\begin{tikzcd}
S_{r}(S_{s}(S_{t}(A))) \arrow[dd, "{S(m)}"'] \arrow[rr, "{m}"] &  & S_{rs}(S_{t}(A)) \arrow[dd, "{m}"] \\
                                                                                      &  &                                           \\
S_{r}(S_{st}(A)) \arrow[rr, "{m}"']                                            &  & S_{rst}(A)                               
\end{tikzcd}

and

\begin{tikzcd}
S_{r}(A) \arrow[d, "S(u)"'] \arrow[rrd, "="] &  &          & S_{r}(A) \arrow[rrd, "="] \arrow[d, "u"'] &  &          \\
S_{r}(S_{1}(A)) \arrow[rr, "{m}"']         &  & S_{r}(A) & S_{1}(S_{r}(A)) \arrow[rr, "{m}"']  &  & S_{r}(A)
\end{tikzcd}

\end{definition}

\begin{definition}
Let $R$ be a rig. A $R$-graded algebra modality is a $R$-graded monad with a family of natural transformations $\nabla_{r,s}A:S_{r}(A) \otimes S_{s}(A) \rightarrow S_{r+s}(A)$ and a natural transformation $\eta_{A}:I \rightarrow S_{0}(A)$ such that for every object $A$, we have that $((S_{r}(A))_{r \in R},(\nabla_{r,s})_{r,s \in R}, \eta)$ is a $(R,+,0)$-commutative [[graded monoid]] and this diagram commutes:

\begin{tikzcd}
S_{r}(S_{t}(A)) \otimes S_{s}(S_{t}(A)) \arrow[dd, "\nabla"'] \arrow[rr, "m \otimes m"] &  & S_{rt}(A) \otimes S_{st}(A) \arrow[dd, "\nabla"] \\
                                                                                        &  &                                                  \\
S_{r+s}(S_{t}(A)) \arrow[rr, "m"']                                                      &  & S_{(r+s)t}(A)                                   
\end{tikzcd}
\end{definition}

## Related concepts

[[symmetric powers in symmetric monoidal categories enriched over modules over a (Q plus)-algebra]]

[[differential category]]

[[!redirects graded codifferential categories]]


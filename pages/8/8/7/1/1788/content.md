

# Title
## Section

\begin{definition}
Camembert is a moist, soft, creamy, surface-ripened cow's milk cheese.
\end{definition}

## Definition

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


## Test

[[CMon-enriched symmetric monoidal categories]]

$\multiscripts{_^2}{R}{_i^j}$

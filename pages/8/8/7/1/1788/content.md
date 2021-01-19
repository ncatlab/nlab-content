
Write 

\[  
  \label{SmashMonoidalCategoryOfPointedTopologicalSpaces}
  \big( PointedTopologicalSpaces, S^0, \wedge \big)
  \;\;\in\;
  SymmetricMonoidalCategories
\] 

* for the [[category]] of [[pointed topological spaces]] (with respect to some [[convenient category of topological spaces]] such as [[compactly generated topological spaces]] or [[D-topological spaces]]) 

* regarded as a [[symmetric monoidal category]] with tensor product the [[smash product]] and unit the [[0-sphere]] $S^0 \,=\, \ast_+$.

This category also has a [[Cartesian product]], given on pointed spaces $X_i = (\mathcal{X}_i, x_i)$ with underlying $\mathcal{X}_i \in TopologicalSpaces$ by

\[
  \label{CartesianProductOfPointedTopologicalSpaces}
  X_1 \times X_2
  \;=\;
  (\mathcal{X}_1, x_1) \times (\mathcal{X}_2, x_2)
  \;\coloneqq\;
  \big(
    \mathcal{X}_1 \times \mathcal{X}_2
    ,
    (x_1, x_2)
  \big)
  \,.
\]

But since this [[smash product]] is a non-trivial [[quotient topological space|quotient]] of the Cartesian product

\[
  \label{SmashProductOfPointedSpacesQuotientDefinition}
  X_1 \wedge X_1 
    \,\coloneqq\, 
  \frac{X_1 \times X_2}{ X_1 \vee X_2 }
\]

it is not itself [[cartesian monoidal category|cartesian]], but just a [[symmetric monoidal category|symmetric monoidal]]. 

However, via the quotienting (eq:SmashProductOfPointedSpacesQuotientDefinition), it still inherits, from the [[diagonal morphisms]] on underlying topological spaces

\[
  \label{CartesianDiagonalOnTopologicalSpaces}
  \array{
    \mathcal{X}
    &\overset{ \Delta_{\mathcal{X}} }{\longrightarrow}&
    \mathcal{X} \times \mathcal{X}
    \\
    x &\mapsto& (x,x)
  }
\]

a suitable notion of [[monoidal category with diagonals|monoidal diagonals]]:

\begin{definition}\label{SmashMonoidalDiagonal}
  [Smash monoidal diagonals]

For $X \,\in\, PointedTopologicalSpaces$, let $D_X \;\colon\; X \longrightarrow X \wedge X$ be the [[composition|composite]] 

\begin{xymatrix@C=7pt}
    X 
    \ar@/_1.6pc/[rrrrr]|-{ \;D_X\; }
    \ar[rr]^-{\Delta_X}
    &&
    X \times X 
    \ar[rr]
    &&
    \frac{X \times X}{ X \vee X}
    \ar@{}[r]|-{ =: }
    &
    X \wedge X
\end{xymatrix}

of the Cartesian [[diagonal morphism]] (eq:CartesianProductOfPointedTopologicalSpaces) with the [[coprojection]] onto the defining [[quotient space]] (eq:SmashProductOfPointedSpacesQuotientDefinition).

\end{definition}

It is immediate that:

\begin{proposition}
  \label{SmashMonoidalDiaginalsAreMonoidalDiagonals}
  The smash monoidal diagonal $D$ (Def. \ref{SmashMonoidalDiagonal})
  makes the [[symmetric monoidal category]] $\big( PointedTopologicalSpaces, S^0, \wedge \big)$ of [[pointed topological spaces]] with [[smash product]] a [[monoidal category with diagonals]], in that

1. $D$ is a [[natural transformation]];

1. $S^0 \overset{\;\;D_{S^0}\;\;}{\longrightarrow} S^0 \wedge S^0$ is an [[isomorphism]].
  
\end{proposition}

While elementary in itself, this has the following profound consequence:

\begin{remark}[Suspension spectra have diagonals]

Since the [[suspension spectrum]]-[[functor]] 

$$
  \Sigma^\infty
  \;\colon\;
  PointedTopologicalSpaces
   \longrightarrow
  HighlyStructuredSpectra
$$

is a [[strong monoidal functor]] from [[pointed topological spaces]] (eq:SmashMonoidalCategoryOfPointedTopologicalSpaces) to any standard category of [[highly structured spectra]] (by [this Prop.](Introduction+to+Stable+homotopy+theory+--+1-2#SmashProductOfFreeSpectra)) it follows that _[[suspension spectra]] have [[monoidal category with diagonals|monoidal diagonals]]_, in the form of [[natural transformations]]

\[
  \label{SmashMonoidalDiagonalOnSuspensionSpectra}
  \Sigma^\infty X
  \overset{
    \;\;
    \Sigma^\infty(D_X)
    \;\;
  }{\longrightarrow}
  \big(
    \Sigma^\infty X
  \big)
    \wedge
  \big(
    \Sigma^\infty X
  \big)  
\]

to their respective [[symmetric smash product of spectra]].

For example, given a [[Whitehead-generalized cohomology theory]] $\widetilde E$ [[Brown representability theorem|represented]] by a  [[ring spectrum]]  

$$
  \big(E, 1^E, \bullet^E \big)
  \;\;
  \in
  \;
  SymmetricMonoids
  \big(
    Ho(Spectra), \mathbb{S}, \wedge 
  \big)
$$

the smash-monoidal diagonal structure (eq:SmashMonoidalDiagonalOnSuspensionSpectra) on suspension spectra serves to define the [[cup product]] $(-)\cup (-)$ on the corresponding [[multiplicative cohomology theory|multiplicative cohomology theory structure]]:

$$
  \begin{aligned}
  &
  \big[
    \Sigma^\infty X
    \overset{c_i}{\longrightarrow}
    \Sigma^{n_i} E
  \big] 
  \,\in\, {\widetilde E}{}^{n_i}(X) 
  \\
  &
  \Rightarrow
  [c_1] \cup [c_2]
  \;\;
    \coloneqq
  \Big[
    \Sigma^\infty X
    \overset{
      \Sigma^\infty(D_X)
    }{\longrightarrow}
    \big(
      \Sigma^\infty X
    \big)
      \wedge
    \big(
      \Sigma^\infty X
    \big)
    \overset{
      ( c_1 \wedge c_2 )
    }{\longrightarrow}
    \big(
      \Sigma^{n_1} E
    \big)
      \wedge
    \big(
      \Sigma^{n_2} E
    \big)  
    \overset{
      \bullet^E
    }{\longrightarrow}
    \Sigma^{n_1 + n_2}E
  \Big]
  \;\;\;
  \in
  \widetilde E^{n_1+n+2}(X)
  \,.
  \end{aligned}
$$




\end{remark}



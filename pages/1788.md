
\[ 1 = 1 \label{a-b} \]
\[ 2 = 2 \label{AbC} \]
Equation \ref{a-b}; equation \ref{AbC}; equation \eqref{a-b}; equation \eqref{AbC}.

Instead of <nowiki>\label{foo-bar}</nowiki>, consider <nowiki>\label{FooBar}</nowiki>.

$$
  G Act(kTop)_{/ B_G \Gamma}
  \underoverset
    {
      \underset{
        (-)
        \times_{ B_G \Gamma } 
        E_G \Gamma 
      }{\longrightarrow}
    }
    {
      \overset{
        (-)/\Gamma
      }{\longleftarrow}
    }
    {\;\;\bot\;\;}
   Im
   \big(
     (-)
     \times_{ B_G \Gamma } 
     E_G \Gamma 
   \big)
   \hookrightarrow
  (\Gamma \rtimes G)Act(kTop)
$$

\begin{tikzcd}
  P \times \Gamma
  \ar[d]
  \ar[rr, shift left=2pt]
  \ar[rr, shift right=2pt]
  &&
  \big(
    A \times E_G \Gamma
  \big)
  \times 
  \Gamma
  \ar[d]
  \\
  P
  \ar[dd]
  \ar[rr]
  \ar[dr]
  &&
  A \times E_G \Gamma
  \ar[dd]
  \ar[dl]
  \\
  &
  E_G \Gamma
  \\
  X
  \ar[rr]
  \ar[dr]
  &&
  A \times_{\Gamma} E_G \Gamma
  \ar[dl]
  \\
  &
  B_G \Gamma
  \ar[from=uu, crossing over]
\end{tikzcd}
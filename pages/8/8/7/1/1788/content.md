
$$
   \stackrel{
      \overset{(\alpha,\phi)_!}{\leftarrow}
   }{
     \underset{(\alpha,\phi)^*}{\to}
   } 
$$

$$
  \underoverset
    {\;\;(\alpha,\phi)^*\;\;}
    {\;\;(\alpha,\phi)_!\;\;}
    {\leftrightarrows}
$$

$$
  \Big\langle
    \big(
      v_1(\sigma)
    \big)_{\sigma \in Sym(n)},
    \;
    \big(
      v_2(\sigma')
    \big)_{\sigma' \in Sym(n)},
  \Big\rangle
  \;\;
    \coloneqq
  \;\;
  \underset{\sigma \in Sym(n)}{\sum}
  \bar v_1(\sigma) \cdot v_2(\sigma)
  \,.
$$

\linebreak

$$
  \begin{aligned}
    \big\langle
      \lambda_1, (i_1, j_1)
    \big\vert
      \lambda_2, (i_2, j_2)
    \big\rangle
    & 
    \;=\;
    \frac{ \chi^{(\lambda_1)}(e) }{ n! }
    \underset{\sigma \in Sym(n)}{\sum}
    \chi^{(\lambda_1)}(\sigma)_{j_1 1_1}
    \bar 
    \chi^{(\lambda_2)}(\sigma)_{i_2 j_2}
    \\
    & \;=\;
    \frac{ \chi^{(\lambda_1)}(e) }{ n! }
    \underset{\sigma \in Sym(n)}{\sum}
    \chi^{(\lambda_1)}(\sigma)_{j_1 i_1}
    \chi^{(\lambda_2)}(\sigma^{-1})_{j_2 i_2}
    \\
    & \;=\;
    \delta^{\lambda_1 \lambda_2}
    \delta_{i_1 i_2} \delta_{j_1 j_2}
  \end{aligned}
$$

Here the first step unwinds the definitions, and the second step uses that the representation matrixes are [[unitary matrices]] in that
$$
  \rho^{(\lambda)}(\sigma^{-1})_{i j}
  \;=\;
  \bar \rho^{(\lambda)}(\sigma)_{j i}  
  \,.
$$
Finally the last step is [[Schur orthogonality]] 
for irreps ([this equation](Schur+orthogonality+relation#eq:SchurOrthogonalityForIrreps)).

\linebreak

\linebreak

\linebreak


$$
  \begin{aligned}
    & 
    \underset{
      \lambda
      \in Part(n)
    }{\sum}
    \big(
      \chi^{(\lambda)}(e)
    \big)^2
    \cdot
    EigVals[e^{- \beta \cdot d_C}]_\lambda
    \\
    &
    \;=\; 
    \underset{
      \lambda \in Part(n)
    }{\sum}
    \big(
      \chi^{(\lambda)}(e)
    \big)^2
    \cdot
    \left(
       \frac{
         1
       }{
         \chi^{(\lambda)}(e)
       }
       \underset{\sigma \in Sym(n)}{\sum}
       e^{ \beta \cdot (\left\vert Cycles(\sigma) \right\vert - n  ) }
       \cdot
       \chi^{(\lambda)}(\sigma)
    \right)
    \\
    & \;=\;
    \underset{
      \sigma \in Sym(n)
    }{\sum}
    e^{ \beta \cdot (\left\vert Cycles(\sigma) \right\vert - n  ) }
    \underset{
      = \delta_{e,\sigma} n!
    }{
    \underbrace{
    \underset{
      \lambda \in Part(n)
    }{\sum}
    \chi^{(\lambda)}(e)
      \cdot
    \chi^{(\lambda)}(\sigma)
    }
    }
    \\
    & \;=\;
    n!
  \end{aligned}
$$


in

\begin{imagefromfile}
    "file_name": "ChordDiagramEntanglementEntropy.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [JGPE 19](#JGPE19)"
\end{imagefromfile}

in

\begin{imagefromfile}
    "file_name": "HanUniversalHolographicCode.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Yan 20](#Yan20)"
\end{imagefromfile}


\begin{prop}
  For $e^\beta = N \in \{1,2, \cdots, n-1\}$
  the Cayley distance kernel $e^{- \beta \cdot d_C}$
  is positive semi-definite.

  For $e^{\beta} = n$  it is not indefinite (i.e. positive semi-definite or positive definite).
\end{prop}
\begin{proof}
  By Lemma \ref{EigenvaluesNonNegativeAtNBetween1Andn} the
  eigenvalues at all these values are non-negative,  
  and by Lemma ... they contain 0 except possibly in the case
  $e^{\beta} = n$
\end{proof}


\begin{lemma}\label{EigenvaluesNonNegativeAtNBetween1Andn}
  For $e^\beta = N \in \{1, 2, \cdots, n\}$
  all the eigenvalues of the Cayley distance kernel 
  $e^{- \beta \cdot d_C}$ on $Sym(n)$
  are non-negative.
\end{lemma}
\begin{proof}
  We observe that the eigenvalues at these particular 
  values of $\beta$ appear, up to a positive multiple, as coefficients of [[monomials]] in [[Schur polynomials]], and all such coefficients are non-negative integers ([this Prop.](Schur+function#CoefficientsOfMonomialsAreNaturalNumbers)). 

  Concretely, for $\lambda$ any [[partition]] of $n$, with corresponding [[Schur polynomial]] $\s_\lambda$  and [[irreducible character|irreducible]] [[Specht module|Specht]] [[character of a linear representation|character]] $\chi^{(\lambda)}$, consider the following computation:

$$
  \begin{aligned}
  s_{\lambda}
  \big(
    \underset{
      N \; args
    }{
      \underbrace{
        x, x, \cdots, x
      }
    }
    ,
    \underset{
      n - N \; args
    }{ 
      \underbrace{
        0, 0, \cdots, 0 
      }
    }
  \big)
  & \;=\;
  \frac{1}{n!}
  \underset{ \sigma \in Sym(n) }{\sum}
    \chi^{(\lambda)}(\sigma)
    \cdot
    \big(
      N x^{l_1} 
    \big)
    \big(
      N x^{l_2} 
    \big)
    \cdots
    \big(
      N x^{l_{\left\vert Cycles(\sigma)\right\vert}} 
    \big)
  \\
  & \;=\;
  \left(
    \frac{1}{n!}
    \underset{ \sigma \in Sym(n) }{\sum}
      \chi^{(\lambda)}(\sigma)
      \cdot
      N^{ \left\vert Cycles(\sigma) \right\vert }
  \right)
  \cdot
  x^n
  \\
  &
  \;=\;\;
  \underset{
    \in \, \mathbb{N}
  }{
  \underbrace{
  \left(
    \tfrac
      {\chi^{(\lambda)}(1)}
      {n!}
    e^{ln(N) \cdot n}
    \cdot
    EV_\lambda (e^{- ln(N) \cdot d_C})
  \right)
  }
  }
  \cdot
  x^n
  \end{aligned}
$$

Here we used:

1. the Frobenius formula for Schur functions ([this Prop.](Schur+function#FrobeniusFormula));

1. some evident re-arrangements;

1. the character formula for the eigenvalues ([this Prop](Cayley+distance+kernel#CharacterFormulaForEigenvalues)).

\end{proof}

$\underoverset
      {k = -s}
      {n -s -1}
      {\prod}\big(N + k \big)
    = \frac{1}{N} \underoverset
      {k = -s}
      {0}
      {\prod}\big(N + k \big) \cdot \underoverset{k = 0}{n -s -1}{\prod}\big(N + k \big) = \frac{1}{N} s_{(s)}(1, 1, \ldots, 1, 0, \ldots 0) \cdot s_{1^{(n-s-1)}}(1, 1, \ldots, 1, 0, \ldots 0)$.

[[quantum information -- contents]]

[[quantum systems -- contents]]

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

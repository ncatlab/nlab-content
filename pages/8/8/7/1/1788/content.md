
$\bigstar$

\begin{proposition}
  \label{MixedUnitaryChannelsOnSIngleQBitAreUnistochastic}
  On a single [[qbit]], every [[mixed unitary quantum channel]]  is a unistochastic channel.
\end{proposition}
([Müller-Hermes & Perry 2019, Cor 1.4](#Müller-HermesPerry19))
\begin{proof}
By Exp. \ref{UniformlyMixedUnitaryChannelsAreUnistochastic} one is reduced to showing that on QBits every mixed unitary quantum channel equals one with uniformly distributed unitaries (this is [M-H & P 19, Thm. 1.2](#Müller-HermesPerry19)). We further spell out the case where there are two unitaries to start with ([M-H & P 19, Lem. 1.1](#Müller-HermesPerry19)):

So let the mixed unitary channel be given by
$$
  \rho
  \;\mapsto\;
  p_1 \, U_1 \cdot \rho \cdot U_1^\dagger
  \;+\;
  p_2 \, U_2 \cdot \rho \cdot U_2^\dagger
$$
then we want to find $U'_i$ with
$$
  p_1 \, U_1 \cdot (\text{-}) \cdot U_1^\dagger
  \;+\;
  p_2 \, U_2 \cdot (\text{-}) \cdot U_2^\dagger
  \;\;
  =
  \;\;
  \tfrac{1}{2}
  \,
  U'_1 \cdot (\text{-}) \cdot U'_1^\dagger
  \;+\;
  \tfrac{1}{2}
  \,
  U'_2 \cdot (\text{-}) \cdot U'_2^\dagger
  \,.
$$
First, by replacing $(\text{-}) \mapsto S \cdot (\text{-}) S^\dagger$ --- for a unitary $S$ to be specified in a moment ---, this is equivalent to
$$
  \begin{array}{r}
  p_1 \, U_1 \cdot S \cdot (\text{-}) \cdot S^\dagger \cdot U_1^\dagger
  \\
  +\;
  p_2 \, U_2 \cdot S \cdot (\text{-}) \cdot S^\dagger \cdot U_2^\dagger
  \end{array}
  \;\;
  =
  \;\;
  \begin{array}{r}
  \tfrac{1}{2}
  \,
  U'_1 \cdot S \cdot (\text{-}) \cdot S^\dagger \cdot U'_1^\dagger
  \\
  +
  \;
  \tfrac{1}{2}
  \,
  U'_2 \cdot S \cdot (\text{-}) \cdot S^\dagger \cdot U'_2^\dagger
  \mathrlap{\,.}
  \end{array}
$$
and then conjugating both sides by $S^\dagger \cdot U^\dagger_1$  gives that this is equivalent to
\[
  \label{IntermediateStepInQBitArgument}
  p_1 \, (\text{-})
  \;+\;
  p_2 \, 
  \underset{D}{
  \underbrace{
    S^\dagger U_1^\dagger \cdot U_2 \cdot S
  } }
  \cdot 
  (\text{-}) 
  \cdot 
  \underset{D^\dagger}{
  \underbrace{
    S^\dagger \cdot U_2^\dagger \cdot U_1 \cdot S
  }
  }
  \;\;
  =
  \;\;  
  \begin{array}{r}
  \tfrac{1}{2}
  \,
  \underset{ W_1 }{
  \underbrace{
    S^\dagger \cdot U_1^\dagger \cdot U'_1 \cdot S 
  }
  }
  \cdot 
    (\text{-}) 
  \cdot 
  \underset{
    W_1^\dagger
  }{
  \underbrace{
    S^\dagger \cdot U'_1^\dagger \cdot U_1 \cdot S
  }
  }
  \\
  +
  \;
  \tfrac{1}{2}
  \,
  \underset{
    W_2
  }{
    \underbrace{
      S^\dagger \cdot U_1^\dagger \cdot U'_2 \cdot S 
    }
  }
  \cdot 
  (\text{-}) 
  \cdot 
  \underset{W_2^\dagger}{
    \underbrace{
      S^\dagger \cdot U'_2^\dagger \cdot U_1 \cdot S
    }
  }
  \end{array}
\]
At this point we fix $S$: Since $U_1^\dagger \cdot U_2$ is evidently a [[normal operator]], the [[spectral theorem]] applies to show that we may find $S$ such that $D$ above is a [[diagonal matrix]]:
\[
  \label{DiagonalizingOperatorInQBitArgument}
  S \cdot U_1^\dagger \cdot U_2 \cdot S^\dagger
  \;\;=\;\;
  diag\big( D_{11}, \, D_{22} \big)
  \,=\,
  D
  \,.
\]

This way we are now reduced to finding unitary operators $W_i$, such that
$$
  p_1 \, (\text{-})
  \;+\;
  p_2
  \,
  D \cdot (\text{-}) \cdot D^\dagger
  \;\;
  =
  \;\;
  \tfrac{1}{2}
  \,
  W_1 \cdot (\text{-}) \cdot W_1^\dagger
  \;+\;
  \tfrac{1}{2}
  \,
  W_2 \cdot (\text{-}) \cdot W_2^\dagger
  \,.
$$
Plugging in the simple ansatz
$$
  W_i 
  \;\coloneqq\;
  \left[
  \array{
    e^{2 \pi \mathrm{i} \phi_i } & 0
    \\
    0 & 1
  }
  \right]
$$
shows that this works for
\[
  \label{PhaseConditionForQBitArgument}
  \tfrac{1}{2}
  \big(
    e^{2 \pi \mathrm{i} \phi_1}
    +
    e^{2 \pi \mathrm{i} \phi_2}
  \big)
  \;\;
  =
  \;\;
  p_1 
  \,+\, 
  p_2 
  \,
  D_11 \overline{D_22}
  \mathrlap{\,.}
\]
which always has a solution for the $\phi_i$ ([M-H & P 19, p. 3](#Müller-HermesPerry19)).

Finally plugging back into (eq:IntermediateStepInQBitArgument) shows that the desired uniformly distributed unitaries may be taken to be:
$$
  \label{UniformUnitariesInQBitCase}
  U'_i
  \;\;\coloneqq\;\;
  U_1
  \cdot
  S
  \cdot
  \left[
  \array{
    e^{2 \pi \mathrm{i} \phi_i} & 0
    \\
    0 & 1
  }
  \right]
  \cdot
  S^\dagger
  \,.
$$
\end{proof}

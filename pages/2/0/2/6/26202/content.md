

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[quantum information theory]], a *mixed unitary quantum channel* is a [[quantum channel]] 

$$
  chan \,\colon\,
  \mathscr{H} \otimes \mathscr{H}^\ast
  \longrightarrow
  \mathscr{H} \otimes \mathscr{H}^\ast
$$

which admits an [operator-sum decomosition](quantum+channel#InTermsOfKrausDecompositions) all whose Kraus operators are multiples of [[unitary operators]] 

$$
  s \,\colon\, S 
  \;\;\;\;
    \vdash
  \;\;\;\;
  U \,\colon\, \mathscr{H} \to \mathscr{H}
$$

as 

$$
  chan
  \;\colon\;
  \rho
  \;\mapsto\;
  \underset{s}{\sum}
  \,
  p_s \, U_s \cdot \rho \cdot U^\dagger
  \,,
$$

where the [[coefficients]] 

$$
  p_{(-)} \,\colon\, S \to [0,1]
$$

necessarily form a [[probability distribution]] over the index [[set]] $S$.


## Examples

\begin{example}
  Of course, all [[unitary quantum channels]] are examples of mixed unitary quantum channels, this being the case (in particular) where the index set $S = \ast$ is the [[singleton set]].
\end{example}

\begin{example}
  A [[bit-flip quantum channel]]
  $$  
    \array{
      QBit \otimes QBit^\ast
      &\xrightarrow{\phantom{-------}}&
      QBit \otimes QBit^\ast
      \\
      \rho 
        &\mapsto& 
      (1-p)\,\rho 
       + 
      p \, X \cdot \rho \cdot X
    }
  $$
  is a mixed unitary quantum channel, where the two unitary operators are the [[identity matrix]] on [[qbits]] and the $X$-[[Pauli gate]]-operator, respectively.
\end{example}


## References

See most references on *[[quantum channels]]*.


[[!redirects mixed unitary quantum channels]]


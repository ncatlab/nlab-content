

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

necessarily form a [[probability distribution]] over the [[finite set|finite]] index [[set]] $S$.


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

In fact:
\begin{example}\label{UnitalChannelOnSingleQBitIsMixedUnitary}
  Every [[unital quantum channel|unital]] quantum channel on a single [[qbit]] is a mixed unitary quantum channel.
\end{example}
This is attributed by [Müller-Hermes & Perry 2019](#Müller-HermesPerry19) (inside the proof of Cor. 1.4) to [Ruskai, Szarek & Werner 2002](#RuskaiSzarekWerner02), where it may be gleaned from combining Thm. 14 (every channel on qbits is the convex combination of two channels in the closure of extremal channels) there and the remark on p. 163 (that the extremal unital channels are the unitary channels).


## References

See most references on *[[quantum channels]]*.

Discussion of mixed unitary quantum channels specifically on single [[qbits]] (cf. *[[DQC1]]*):

* {#RuskaiSzarekWerner02} Mary Beth Ruskai, Stanislaw Szarek, Elizabeth Werner, *An analysis of completely-positive trace-preserving maps on $M_2$*, Linear Algebra and its Applications **347** 1–3 (2002) 159-187 &lbrack;<a href="https://doi.org/10.1016/S0024-3795(01)00547-X">doi:10.1016/S0024-3795(01)00547-X</a>&rbrack;

* {#Müller-HermesPerry19} Alexander Müller-Hermes, Christopher Perry, *All unital qubit channels are 4-noisy operations*, Letters in Mathematical Physics **109** (2019) 1–9 &lbrack;[doi:10.1007/s11005-018-1104-x](https://doi.org/10.1007/s11005-018-1104-x), [arXiv:1802.01337](https://arxiv.org/abs/1802.01337)&rbrack;


[[!redirects mixed unitary quantum channels]]



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

In [[quantum probability theory]]/[[open quantum systems]],
a *unitary quantum channel* is a [[quantum channel]] whose restriction to [[pure states]] acts by a [[unitary transformation]] just as a loss-less [[quantum gate]] does.

Concretely, in terms of [Kraus decomposition](quantum+channel#InTermsOfKrausDecompositions), a quantum channel 

$$
  \array{
    \mathscr{H}_1
    \otimes
    \mathscr{H}_1^\ast
    &
    \longrightarrow
    &
    \mathscr{H}_2
    \otimes
    \mathscr{H}_2^\ast
    \\
    \rho
    &\mapsto&
    ch(\rho)
  }
$$

is unitary iff there exists a [[unitary operator]] $U \,\colon\, \mathscr{H}_1 \longrightarrow \mathscr{H}_2$ such that $ch$ is given by [[conjugation]] with this operator:

$$
  ch(\rho) \;=\; U \cdot \rho \cdot U^\dagger
  \,.  
$$

## Properties

\begin{proposition}
**([[quantum channels]] and [[decoherence]])**

Every [[quantum channel]]

$$
  ch 
  \;\;\colon\;\;
  \mathscr{H} \otimes \mathscr{H}^\ast
  \longrightarrow
  \mathscr{H} \otimes \mathscr{H}^\ast
$$

may be written as 

1. a [[unitary quantum channel]] $U_{tot}$ 

1. on a [[compound system]] with some $\mathscr{B}$ (the "bath"), yielding a *total system* $\mathscr{H} \otimes \mathscr{B}$ ([[tensor product of Hilbert spaces|tensor product]])

1. acting on the given [[mixed state]] $\rho$ coupled (tensored) with a fixed [[mixed state]] $env \,\colon\, \mathscr{B} \otimes \mathscr{B}^\ast$ of the bath system,

1. followed by [[partial trace]] (averaging) over $\mathscr{B}$ (leading to [[decoherence]] in the remaining state)

in that

\[
  \label{QuantumChannelVieDecoherence}
  ch(\rho)
  \;\;=\;\;
  Tr_{\mathscr{B}}
  \big(
    U_{tot}
    \cdot
    (\rho \otimes env)
    \cdot
    U_{tot}^\dagger
  \big)
  \,.
\]

Conversely, every operation of the form (eq:QuantumChannelVieDecoherence) is a quantum channel.
\end{proposition}
(eg. [Attal, Thm. 6.5 & 6.7](#Attal))

## References

See the references at *[[quantum channel]]*, for instance:


* {#Attal} [[Stéphane Attal]], *Quantum Channels*, Lecture 6 in:  *Lectures on Quantum Noises* &lbrack;[pdf](http://math.univ-lyon1.fr/~attal/Quantum_Channels.pdf), [[Attal-QuantumChannels.pdf:file]], [webpage](http://math.univ-lyon1.fr/~attal/chapters.html)&rbrack;



[[!redirects unitary quantum channels]]


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



[[!include quantum channels and decoherence -- section]]




## References

See the references at *[[quantum channel]]*, for instance:


* {#Attal} [[Stéphane Attal]], *Quantum Channels*, Lecture 6 in:  *Lectures on Quantum Noises* &lbrack;[pdf](http://math.univ-lyon1.fr/~attal/Quantum_Channels.pdf), [[Attal-QuantumChannels.pdf:file]], [webpage](http://math.univ-lyon1.fr/~attal/chapters.html)&rbrack;



[[!redirects unitary quantum channels]]

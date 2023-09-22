
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


### General

\begin{proposition}
\label{UnitaryChannelsAreTheReversibleChannels}
**(unitary channels are the reversible channels)**
\linebreak
  Unitary channels are clearly [[invertible map|invertible]]. In fact, every invertible [[quantum channel]] must be a unitary quantum channel.
\end{proposition}
(eg. [Preskill](#PreskillRev04) [pp. 13](http://theory.caltech.edu/~preskill/ph219/chap3_15.pdf#page=13))

[[!include quantum channels and decoherence -- section]]


## Related concepts

* [[quantum channel]]

  * [[quantum measurement channel]]


## References

> (For more see the references at *[[quantum channel]]*.)

* [[Teiko Heinosaari]], [[Mário Ziman]], Exp. 4.6 in: *The Mathematical Language of Quantum Theory -- From Uncertainty to Entanglement*, Cambridge University Press  (2011) &lbrack;[doi:10.1017/CBO9781139031103]( https://doi.org/10.1017/CBO9781139031103)&rbrack;

* {#PreskillRev04} [[John Preskill]], *Reversibility*, Section 3.2.2 &lbrack;[pdf](http://theory.caltech.edu/~preskill/ph219/chap3_15.pdf#page=13)&rbrack; in: *Quantum Computation*, lecture notes, since 2004 &lbrack;[web](http://theory.caltech.edu/~preskill/ph229/)&rbrack;


* {#Attal} [[Stéphane Attal]], *Quantum Channels*, Lecture 6 in:  *Lectures on Quantum Noises* &lbrack;[pdf](http://math.univ-lyon1.fr/~attal/Quantum_Channels.pdf), [[Attal-QuantumChannels.pdf:file]], [webpage](http://math.univ-lyon1.fr/~attal/chapters.html)&rbrack;



[[!redirects unitary quantum channels]]

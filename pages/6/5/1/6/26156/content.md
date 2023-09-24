
### Quantum channels and decoherence
 {#QuantumChannelsAndDecoherence}

The crux of dynamical [[quantum decoherence]] is that *fundamentally* the (time-)evolution of any [[quantum system]] $\mathscr{H}$ may be assumed [[unitary quantum channel|unitary]] (say via a [[Schrödinger equation]]) *when taking the whole evolution of its environment* $\mathscr{B}$ (the "bath", ultimately the whole [[observable universe]]) into account, too, in that the evolution of the total system $\mathscr{H} \otimes \mathscr{B}$  is given by a [[unitary operator]]

$$
  \array{
    \mathllap{
      evolve
      \;\colon\;
    }
    \mathscr{H} \otimes \mathscr{B}
    &\longrightarrow&
    \mathscr{H} \otimes \mathscr{B}
    \\
    \left\vert \psi, \beta \right\rangle
    &\mapsto&
    U_{tot}
    \left\vert \psi, \beta \right\rangle
    \mathrlap{\,,}
  }
$$

after understanding the [[mixed states]] $\rho \,\colon\, \mathscr{H} \otimes \mathscr{H}^\ast$ ([[density matrices]]) of the given [[quantum system]] as coupled to any given mixed state $env \,\colon\, \mathscr{B} \otimes \mathscr{B}^\ast$ of the bath (via [[tensor product]])

$$
  \array{
    \mathllap{
      couple
      \;\colon\;
    }
    \mathscr{H} \otimes \mathscr{H}^\ast
    &
    \longrightarrow
    &
    (\mathscr{H} \otimes \mathscr{B})
    \otimes
    (\mathscr{H} \otimes \mathscr{B})^\ast
    \\
    \rho &\mapsto&
    \rho \otimes env
    \mathrlap{\,;}
  }
$$

...the only catch being that one cannot --- and in any case does not (want or need to) ---  keep track of the precise [[quantum state]] of the environment/bath, instead only of its *average* effect on the given [[quantum system]], which by the rule of [[quantum probability]] is the [[mixed state]] that remains after the [[partial trace quantum channel|partial trace]] over the environment: 
\[
  \label{PartialTraceOverBathTowardsQuantumChannels}
  \array{
    \mathllap{
    average
    \;\colon\;
    }
    (\mathscr{H} \otimes \mathscr{B})
    \otimes
    (\mathscr{H} \otimes \mathscr{B})^\ast
    &\longrightarrow&
    \mathscr{H} \otimes \mathscr{H}^\ast
    \\
    \widehat{\rho}
      &\mapsto&
    Tr_{\mathscr{B}}\big(\widehat{\rho}\big)
    \mathrlap{\,.}
  }
\]

In summary this means *for practical purposes* that the probabilistic evolution of quantum systems $\mathscr{H}$ is always of the composite form

$$
  \array{ 
    \mathscr{H}
    \otimes
    \mathscr{H}^\ast
    & 
    \xrightarrow{    
      \array{
        \text{couple to}
        \\
        \text{environment}
      }
    } 
    &
    \left(
    \array{
      \mathscr{H}
      \\
      \otimes
      \\
      \mathscr{B}
    }
    \right)
    \otimes
    \left(
    \array{
      \mathscr{H}
      \\
      \otimes
      \\
      \mathscr{B}
    }
    \right)^\ast
    &
    \xrightarrow{    
      \array{
        \text{total unitary}
        \\
        \text{evolution}
      }
    } 
    &
    \left(
    \array{
      \mathscr{H}
      \\
      \otimes
      \\
      \mathscr{B}
    }
    \right)
    \otimes
    \left(
    \array{
      \mathscr{H}
      \\
      \otimes
      \\
      \mathscr{B}
    }
    \right)^\ast    
    &
    \xrightarrow{    
      \array{
        \text{average over}
        \\
        \text{environment}
      }
    } 
    &
    \;\;\;\;
    \mathscr{H} \otimes \mathscr{H}^\ast
    \\
    \rho
    &\mapsto&
    \rho \otimes env
    &\mapsto&
    \mathclap{
    U_{tot} 
      \cdot  
    (\rho \otimes env) 
      \cdot
    U_{tot}^\dagger 
    }
    &\mapsto&
    \;\;\;\;\;\;\;\;\;\;\;\;
    \mathclap{
    Tr_{\mathscr{B}}
    \big(
      U_{tot} 
        \cdot  
      (\rho \otimes env) 
        \cdot
      U_{tot}^\dagger 
   \big)
   }
  }
$$

This composite turns out to be a "*[[quantum channel]]*" and in fact all quantum channels arise this way:

\begin{proposition}
\label{QuantumChannelsAsPartialTracesOfUnitariesOnTensors}
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

1. a [[unitary quantum channel]], induced by a [[unitary operator]] $U_{tot} \,\colon\, \mathscr{H} \otimes \mathscr{B} \to \mathscr{H} \otimes \mathscr{B} $ 

1. on a [[compound system]] with some $\mathscr{B}$ (the "bath"), yielding a *total system* [[Hilbert space]] $\mathscr{H} \otimes \mathscr{B}$ ([[tensor product of Hilbert spaces|tensor product]]),

1. and acting on the given [[mixed state]] $\rho$ coupled (tensored) with a fixed [[mixed state]] $env \,\colon\, \mathscr{B} \otimes \mathscr{B}^\ast$ of the bath system,

1. followed by [[partial trace quantum channel|partial trace]] (averaging) over $\mathscr{B}$ (leading to [[decoherence]] in the remaining state)

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

The **original proof** is due to [Lindblad 1975 ](quantum+channel#Lindblad75) (see top of p. 149 and inside the proof of Lem. 5).

For exposition see: [Nielsen & Chuang 2000 §8.2.2-8.2.3](quantum+channel#NielsenChuang00)

For detailed **proof**, including the infinite-dimensional case: [Attal, Thm. 6.5 & 6.7](quantum+channel#AttalLectureNotes).

The realization of a quantum channel in the form (eq:QuantumChannelVieDecoherence) is also called an *environmental representation* (eg. [Życzkowski & Bengtsson 2004 (3.5)](quantum+channel#ŻyczkowskiBengtsson04)).



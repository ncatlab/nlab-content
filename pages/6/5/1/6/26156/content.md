
### Environmental representation of quantum channels
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

This composite turns out to be a "*[[quantum channel]]*" 

The realization of a quantum channel in the form (eq:QuantumChannelVieDecoherence) is also called an *environmental representation* (eg. [Życzkowski & Bengtsson 2004 (3.5)](quantum+channel#ŻyczkowskiBengtsson04)).


In fact all quantum channels on a fixed Hilbert space have such an evironmental representation:

\begin{proposition}
\label{QuantumChannelsAsPartialTracesOfUnitariesOnTensors}
**(environmental representation of quantum channels)**

Every [[quantum channel]]

$$
  chan 
  \;\;\colon\;\;
  \mathscr{H} \otimes \mathscr{H}^\ast
  \longrightarrow
  \mathscr{H} \otimes \mathscr{H}^\ast
$$

may be written as 

1. a [[unitary quantum channel]], induced by a [[unitary operator]] $U_{tot} \,\colon\, \mathscr{H} \otimes \mathscr{B} \to \mathscr{H} \otimes \mathscr{B} $ 

1. on a [[compound system]] with some $\mathscr{B}$ (the "bath"), yielding a *total system* [[Hilbert space]] $\mathscr{H} \otimes \mathscr{B}$ ([[tensor product of Hilbert spaces|tensor product]]),

1. and acting on the given [[mixed state]] $\rho$ coupled (tensored) with any [[pure state]] of the bath system,

1. followed by [[partial trace quantum channel|partial trace]] (averaging) over $\mathscr{B}$ (leading to [[decoherence]] in the remaining state)

in that

\[
  \label{QuantumChannelVieDecoherence}
  chan(\rho)
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

This is originally due to [Lindblad 1975 ](quantum+channel#Lindblad75) (see top of p. 149 and inside the proof of Lem. 5). For exposition and review see: [Nielsen & Chuang 2000 §8.2.2-8.2.3](quantum+channel#NielsenChuang00).
An account of the infinite-dimensional case is in [Attal, Thm. 6.5 & 6.7](quantum+channel#AttalLectureNotes). These authors focus on the case that the environment is in a [[pure state]], the (parital) generalization to [[mixed state|mixed]] environment states is discussed in [Bengtsson & Życzkowski  2006 pp. 258](quantum+channel#BengtssonŻyczkowski06).

\begin{proof}
\label{ProofOfEnvironmentalRepresentationOfQuantumChannels}
We spell out the proof assuming [[finite-dimensional Hilbert spaces]]. (The general case follows the same idea, supplemented by arguments that the following [[sums]] [[convergence|converge]].)

Now given a [[completely positive map]]:

$$
  chan 
    \,\colon\,
  \mathscr{H} \otimes \mathscr{H}^\ast
  \longrightarrow
  \mathscr{H} \otimes \mathscr{H}^\ast 
  \,,
$$

then by  [operator-sum decomposition](quantum+channel#OperatorSumDecompositionOfQuantumChannels) there exists a [[set]] ([[finite set|finite]], under our assumptions) [[inhabited set|inhabited]] by at least one element
$$
  s_{ini} \,\colon\, S
  \,,
$$
and an $S$-[[indexed set]] of [[linear operators]]
\[
  \label{KrausDecompositionInConstructionOfEnvRep}
  s \,\colon\, S
  \;\;\;
    \vdash
  \;\;\;
  E_s 
  \;\colon\;
  \mathscr{H} 
  \longrightarrow
  \mathscr{H}
  \,,\;\;\;\;
  \text{with}
  \;\;\;\;
  \underset{s}{\sum}
  E_s^\dagger \cdot E_s \,=\, Id
  \mathrlap{\,,}
\]

such that 

$$
  chan(\rho)
  \;=\;
  \underset{s}{\sum}
  \,
  E_s \cdot \rho \cdot E_s^\dagger
  \,.
$$

Now take

$$
  \mathscr{B}
  \,\equiv\,
  \underset{S}{\oplus} \mathbb{C}
$$

with its canonical [[Hermitian form|Hermitian]] [[inner product]]-structure with [[orthonormal linear basis]] $\big(\left\vert s \right\rangle\big)_{s \colon S}$ and consider the linear map

$$
  \array{
    \mathllap{
      V
      \;\colon\;\;
    }
    \mathscr{H} 
    &\longrightarrow&
    \mathscr{H}
    \otimes
    \mathscr{B}
    \\
    \left\vert \psi \right\rangle
    &\mapsto&
    \underset{s}{\sum}
    \,
    E_s
    \left\vert
      \psi
    \right\rangle
    \otimes
    \left\vert s \right\rangle
    \mathrlap{\,.}
  }
$$

Observe that this is a [[linear isometry]]

$$
  \begin{array}{ll}
    \left\langle \psi \right\vert
      V^\dagger
      V 
    \left\vert \psi \right\rangle
    \\
    \;=\;
    \underset{s,s'}{\sum}
    \left\langle \psi \right\vert
      E_{s'}^\dagger
      E_s
    \left\vert \psi \right\rangle
    \underset{
      \delta_s^{s'}
    }{
      \underbrace{
        \left\langle s' \vert s \right\rangle
      }
    }
    \\
    \;=\;
    \left\langle \psi \right\vert
    \underset{
      Id
    }{
      \underbrace{
        \underset{s}{\sum}
        E_{s}^\dagger
        E_s
      }
    }
    \left\vert \psi \right\rangle
    \\
    \;=\;
    \left\langle \psi \vert \psi \right\rangle
    \mathrlap{\,.}
  \end{array}
$$

This [implies](linear+isometryLinearIsometriesAreInjective) that $V$ is [[injective map|injective]] so that we have a [[direct sum]]-decomposition of its [[codomain]] into its [[image]] and its [[cokernel]] [[orthogonal complement]], which is unitarily isomorphic to $dim(\mathscr{B})-1$ summands of $\mathscr{H}$ that we may identify as follows:

$$
  \mathscr{H} \otimes \mathscr{B}
  \;\simeq\;
  V\big( \mathscr{H} \big)
  \oplus
  \Big(
    \mathscr{H}
    \otimes
    \big( 
      \mathscr{B} 
        \ominus 
      \mathbb{C}\left\vert s_0 \right\rangle   
    \big)
  \Big)
  \,.
$$

In total this yields a unitary operator

$$
  U
  \;\colon\;
  \mathscr{H} \otimes \mathscr{B}
  \,\simeq\,
  \mathscr{H} 
  \oplus
  \Big(
    \mathscr{H} 
      \otimes 
    \big(
      \mathscr{B} 
        \ominus 
      \mathbb{C}\left\vert s_{ini} \right\rangle
    \big)
  \Big)
  \underoverset{}{}{\longrightarrow}
  V\big(
    \mathscr{H}
  \big) 
  \oplus
  \Big(
    \mathscr{H} 
      \otimes 
    \big(
      \mathscr{B} 
        \ominus 
      \mathbb{C}\left\vert s_{ini} \right\rangle
    \big)
  \Big)
  \;\simeq\;
  \mathscr{H} \otimes \mathscr{B}
$$

and we claim that this has the desired action on couplings of the $\mathscr{H}$-system to the pure bath state $\left\vert s_{ini} \right\rangle$:

$$
  \begin{array}{l}
    trace^{\mathscr{B}}
    \Big(
      U
      \big(
        \left\vert s_{ini} \right\rangle
          \rho 
        \left\langle s_{ini} \right\vert
      \big)
      U^\dagger
    \Big)
    \\
    \;=\;
    \underset{s,s'}{\sum}
    trace^{\mathscr{B}}
    \big(
        \left\vert s \right\rangle
          E_s \cdot \rho \cdot E_{s'}^\dagger
        \left\langle s' \right\vert
    \big)
    \\
    \;=\;
    \underset{s,s'}{\sum}
    \underset{
      \delta_{s}^{s'}
    }{
      \underbrace{
        \left\langle s' \vert s \right\rangle
      }
    }
    E_s \cdot \rho \cdot E_{s'}^\dagger
    \\
    \;=\;
    \underset{s}{\sum}
    E_s \cdot \rho \cdot E_{s}^\dagger
    \\
    \;=\;
    chan(\rho)
    \,.
  \end{array}
$$
This concludes the construction of an environmental representation where the environment is in a pure state.
\end{proof}

\begin{remark}
  The above theorem is often phrased as "... and the environment can be assumed to be in a pure state". But in fact the proof crucially uses the assumption that the environment is in a pure state. It is not clear that there is a proof that works more generally.

In fact, if the environment is taken to be in the maximally mixed state, then the resulting quantum channels are called *noisy operations* or *[[unistochastic quantum channel|unistochastic quantum channels]]* and are not expected to exhaust all quantum channels.
\end{remark}




A [[quantum operation]]/[[quantum channel]] $chan \,\colon\, \mathscr{H} \otimes \mathscr{H}^\ast \to \mathscr{H} \otimes \mathscr{H}^\ast$ is called a *noisy operation* &lbrack;[Horodecki, Horodecki & Oppenheim 2003](#HorodeckiHorodeckiOppenheim03)&rbrack; or a *unistochastic channel* &lbrack;[Życzkowski & Bengtsson 2004](#ŻyczkowskiBengtsson04)&rbrack; if it has an [environmental representation](quantum channel#QuantumChannelsAndDecoherence) where the environment/bath system $\mathscr{B}$ is in its maximally mixed state:


$$
  chan(\rho)
  \;\;=\;\;
  \frac{1}{dim(\mathscr{B})}
  \mathrm{tr}^{\mathscr{B}}
  \Big(
    U
    \big(
      \rho \otimes id_{\mathscr{B}}
    \big)
    U^\dagger
  \Big)
  \,.
$$

\begin{remark}
  The theorem ([here](quantum +channel#QuantumChannelsAsPartialTracesOfUnitariesOnTensors)) that every endo-[[quantum channel]] has an environmental representation is often advertized with the addendum that "... and such the environment may be chose to be in a pure state", but in fact this is assumption is what the existing proofs rely on. For environments in non-pure states it is not clear that they can environmentally represent all quantum channels, and for noisy/unistochastic channels it is not to be expected that they exhaust all quantum channels.

But [Müller-Hermes & Perry 2019](#Müller-HermesPerry19) show that all *[[unital quantum channels]]* on [[qbits]]  can be realized as noisy/unistochastic channels (with a bath of size at least 4).
\end{remark}


## References

Precursor discussion of the concept is due to:

* [[Michal Horodecki]], [[Pawel Horodecki]], [[Jonathan Oppenheim]], *Reversible transformations from pure to mixed states, and the unique measure of information*, Phys. Rev. A 67 062104 (2003) &lbrack;[doi:10.1103/PhysRevA.67.062104](https://doi.org/10.1103/PhysRevA.67.062104), [arXiv;quant-ph/0212019](https://arxiv.org/abs/quant-ph/0212019)&rbrack;

  > (who speak of "noisy operations")

* [[David Poulin]], Robin Blume-Kohout, [[Raymond Laflamme]], Harold Ollivier, around (2) of:  *Exponential speed-up with a single bit of quantum information: Testing the quantum butterfly effect*, Phys. Rev. Lett. **92** 177906 (2004) &lbrack;[arXiv:quant-ph/0310038](https://arxiv.org/abs/quant-ph/0310038), [doi:10.1103/PhysRevLett.92.177906](https://doi.org/10.1103/PhysRevLett.92.177906)&rbrack;


The terminology "unistochastic channels" was introduced in:

* {#ŻyczkowskiBengtsson04} [[Karol Życzkowski]], [[Ingemar Bengtsson]], p. 13 of: *On Duality between Quantum Maps and Quantum States*, Open Systems & Information Dynamics **11** 01 (2004) 3-42 &lbrack;[doi:10.1023/B:OPSY.0000024753.05661.c2](https://doi.org/10.1023/B:OPSY.0000024753.05661.c2)&rbrack;

* {#BengtssonŻyczkowski06} [[Ingemar Bengtsson]], [[Karol Życzkowski]], p. 259 of: *Geometry of Quantum States --- An Introduction to Quantum Entanglement*, Cambridge University Press (2006) &lbrack;[doi:10.1017/CBO9780511535048](https://doi.org/10.1017/CBO9780511535048), [ResearchGate](https://www.researchgate.net/publication/266435541_Geometry_of_Quantum_States_An_Introduction_to_Quantum_Entanglement)&rbrack;

* Marcin Musz, Marek Kuś, [[Karol Życzkowski]], *Unitary quantum gates, perfect entanglers, and unistochastic maps*, Phys. Rev. A **87** 022111 &lbrack;[doi:10.1103/PhysRevA.87.022111](https://doi.org/10.1103/PhysRevA.87.022111)&rbrack;

Proof that all [[unital quantum channels]] on [[qubits]] are unistochastic (noisy operations) for a bath of size at least 4:

* Alexander Müller-Hermes, Christopher Perry, *All unital qubit channels are 4-noisy operations*, Letters in Mathematical Physics **109** (2019) 1–9 &lbrack;[doi:10.1007/s11005-018-1104-x](https://doi.org/10.1007/s11005-018-1104-x), [arXiv:1802.01337](https://arxiv.org/abs/1802.01337)&rbrack;


***

In one direction, assume that 

$$
  chan \,\colon\,
  \mathscr{H} \otimes \mathscr{H}^\ast
  \longrightarrow
  \mathscr{H} \otimes \mathscr{H}^\ast 
$$

is a [[completely positive map]]. Then by  [operator-sum decomposition](quantum+channel#OperatorSumDecompositionOfQuantumChannels) there exists a [[set]] ([[finite set|finite]], under our assumptions) [[inhabited set|inhabited]] by at least one element
$$
  s_{ini} \,\colon\, S
  \,,
$$
and an $S$-[[indexed set]] of [[linear operators]]
$$
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
$$

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

and we claim that this has the desired action if we couple the system to the pure bath state: $\left\vert s_0 \right\rangle$:

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


#Contents#
* table of contents
{:toc}

## Idea

A *linear isometry* is a [[linear map]] 

$$
  \phi
  \,\colon\,
  \mathscr{H}_1
  \longrightarrow
  \mathscr{H}_2
$$

between [[vector spaces]] equipped with ([[Hermitian form|Hermitian]]) [[inner products]] ${\langle \cdot \vert \cdot \rangle}_{i}$ (often: [[Hilbert spaces]]) which preserves these inner products, in that 

$$
  \left\langle \phi(-) \vert \phi(-) \right\rangle_2
  \;=\;
  \left\langle - \vert - \right\rangle_2
$$

or equivalently in terms of [[adjoint operators]]:

$$
  \phi^\dagger \cdot \phi \,=\, Id_{\mathscr{H}_1}
  \,.
$$

If also the reverse condition $\phi \cdot \phi^\dagger$ holds, then $\phi$ is called a [[unitary operator]], which is the case iff $\phi$ is [[surjective map]]. 

## References




### Environmental representation of measurement channels

By the general theorem about [environmental representations](quantum+channel#QuantumChannelsAndDecoherence) of quantum channels, every [[quantum measurement channel]] on a [[quantum system]] $\mathscr{H}$ may be decomposed as 

1. coupling of $\mathscr{H}$ to an environment/bath system $\mathscr{B}$,

1. [[unitary quantum channel|unitary evolution]] of the [[composite system]] $\mathscr{H} \otimes \mathscr{B}$,

1. [[averaging quantum channel|averaging]] the result over the environment states.

The way this works specifically for [[quantum measurement channels]] has precursor discussion [von Neumann 1932 §VI.3 ](quantum+measurement#vonNeumann32) and received much attention in discussion of *[[quantum decoherence]]* following [Zurek 1981](quantum+decoherence#Zurek81) and [Joos & Zeh 1985](quantum+decoherence#JoosZeh85).

> (independently and apparently unkowingly of the general discussion of [environmental representations](quantum+channel#QuantumChannelsAndDecoherence) in [Lindblad 1975](quantum+channel#Lindblad75)) 


Concretely,

> (we shall restrict attention to [[finite-dimensional Hilbert spaces]] not to get distracted by technicalities that are irrelevant to the point we are after)

if $\left\vert b_{\mathrm{init}} \right\rangle \,\colon\, \mathscr{B}$ denotes the initial state of a "device" [[quantum system]] then any notion of this device measuring the given [[quantum system]] $\mathscr{H}$ (in its measurement basis $W$, $\mathscr{H} \simeq \underset{W}{\oplus}\mathbb{C}$) under their joint [[unitary quantum channel|unitary quantum evolution]]  should be reflected in a [[unitary operator]] under which &lbrack;[Zurek 1981 (1.1)](quantum+decoherence#Zurek81), [Joos & Zeh 1985 (1.1.)](quantum+decoherence#JoosZeh85), following [von Neumann 1932 §VI.3 ](quantum+measurement#vonNeumann32), review includes [Schlosshauer 2007 (2.51)](quantum+decoherence#Schlosshauer07)&rbrack;:

1. the system $\mathscr{H}$ remains invariant *if* it is purely in any eigenstate $\left\vert w \right\rangle$ of the measurement basis, 

1. while in this case the measuring system evolves to a corresponding "pointer state" $\left\vert b_w \right\rangle$: 


\[
  \label{UnitaryMeasurementProcess}
  \array{
    &\mathclap{
      \color{green}
      \array{
        \text{unitary}
        \\
        \text{measurement interaction}
      }
   }&
    \\
    \mathllap{
      U_W
      \;\colon\;\;
    }
    \mathscr{H} \otimes \mathscr{B}
    &\longrightarrow&
    \mathscr{H} \otimes \mathscr{B}
    \\
    \left\vert w, b_{ini} \right\rangle
    &\mapsto&
    \left\vert w, b_w \right\rangle
  }
\]


for $b_{\mathrm{ini}}$ and $b_w$ distinct elements of an (in practice: approximately-)[[orthonormal basis]] for $\mathscr{B}$. (There is always a unitary operator with this mapping property (eq:UnitaryMeasurementProcess), for instance the one which moreover maps $\left\vert w, b_{w}\right\rangle \mapsto \left\vert w, b_{\mathrm{ini}}\right\rangle$ and is the [[identity map|identity]] on all remaining basis elements.)

But then the composition of the corresponding [[unitary quantum channel]] with the [[averaging quantum channel|averaging channel]] over $\mathscr{B}$ is indeed equal to the $W$-[[measurement quantum channel]] on $\mathscr{H}$ (cf. eg. [Schlosshauer 2007 (2.117)](quantum+decoherence#Schlosshauer07), going back to [Zeh 1970 (7)](quantum+decoherence#Zeh70)), as follows:

\begin{imagefromfile}
    "file_name": "EnvRepOfQuantumMeasurementChannel-230924b.jpg",
    "width": 920,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}




### Environmental representation of measurement channels

By the general theorem about [environmental representations](quantum+channel#QuantumChannelsAndDecoherence) of quantum channels, every [[quantum channel]] on a [[quantum system]] $\mathscr{H}$ may be decomposed as 

1. coupling of $\mathscr{H}$ to an environment/bath system $\mathscr{B}$,

1. [[unitary quantum channel|unitary evolution]] of the [[composite system]] $\mathscr{H} \otimes \mathscr{B}$,

1. [[averaging quantum channel|averaging]] the result over the environment states.

The way this works specifically for [[quantum measurement channels]] has precursor discussion [von Neumann 1932 §VI.3 ](quantum+measurement#vonNeumann32) and received much attention in discussion of *[[quantum decoherence]]* following [Zurek 1981](quantum+decoherence#Zurek81) and [Joos & Zeh 1985](quantum+decoherence#JoosZeh85) (independently and apparently unkowingly of the general discussion of [environmental representations](quantum+channel#QuantumChannelsAndDecoherence) in [Lindblad 1975](quantum+channel#Lindblad75)).


Concretely,

> (we shall restrict attention to [[finite-dimensional Hilbert spaces]] not to get distracted by technicalities that are irrelevant to the point we are after)

if $\left\vert b_{\mathrm{ini}} \right\rangle \,\colon\, \mathscr{B}$ (we use [[bra-ket notation]]) denotes the initial state of a "device" [[quantum system]] then any notion of this device measuring the given [[quantum system]] $\mathscr{H}$ (in its measurement basis $W$, $\mathscr{H} \simeq \underset{W}{\oplus}\mathbb{C}$) under their joint [[unitary quantum channel|unitary quantum evolution]]  should be reflected in a [[unitary operator]] under $[$[Zurek 1981 (1.1)](quantum+decoherence#Zurek81), [Joos & Zeh 1985 (1.1.)](quantum+decoherence#JoosZeh85), following [von Neumann 1932 §VI.3 ](quantum+measurement#vonNeumann32), review includes [Schlosshauer 2007 (2.51)](quantum+decoherence#Schlosshauer07)$]$:

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
    "width": 940,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


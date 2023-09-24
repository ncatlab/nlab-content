
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

By *quantum measurement channels* one means [[quantum channels]] which express the process of [[quantum measurement]] with its [[quantum state collapse]] *together* with classical uncertainty about which measurement result is obtained. Hence a quantum measurement channel applied to a (normed) [[pure state]] $\left\vert \psi \right\rangle$ produces the [[mixed state]] in which each of the possible [[quantum state collapse|collapsed states]] $P_w \left\vert \psi \right\rangle$ appears with classical [[probability]] $\left\vert\left\langle \psi \vert w \right\rangle\right\vert^2$

More in detail, consider 

$$
  \mathscr{H} 
     \,\equiv\, 
  \underset{w \colon W}{\oplus} \mathscr{H}_w
$$ 

a [[Hilbert space]] exhibited as the [[direct sum]] of subspaces $\mathscr{H}_w$ [[indexed set|indexed]] by a [[finite set]] $W \,\colon\, FinSet$, 
and write

$$
  P_w 
  \,\colon\,
  \mathscr{H}
  \twoheadrightarrow
  \mathscr{H}_w
  \hookrightarrow
  \mathscr{H}
$$

for the corresponding [[projection operator]].

By construction this is such that

$$
  \underset{w}{\sum} P_w
  \;=\;
  \mathrm{id}_{\mathscr{H}}
  \,,
$$

whence one also refers to the [[tuple]] $( w \mapsto P_w )$ aas  *[[projection valued measure]]* (here: on the [[finite set]] $W$).

If now $W$ is a [[quantum measurement]]-[[linear basis|basis]] on $\mathscr{H}$, then the [[quantum state collapse|collapse postulate]] of [[quantum mechanics]] says that after measuring $w \,\colon\, W$ for a quantum system previously in [[pure state]] $\left\vert \psi \right\rangle\,\colon\, \mathscr{H}$, the state will have collapsed (up to normalization) according to
$$
  \left\vert \psi \right\rangle
  \;\mapsto \;
  P_w \left\vert \psi \right\rangle
  \,,
$$

hence any [[mixed state]] ([[density matrix]]) will have evolved according to 

$$
  \rho \;\mapsto\; P_w \cdot \rho \cdot P_w
  \,.
$$

But if one now in addition considers classical [[probability theory|probabilistic]] uncertainty* as to which measurement result $w$ was actually found (say due to ignorance of the experimentor or imperfection of the measurement device) then all of the resulting pure states $P_w \left\vert \psi \right\rangle$ above are equivally likely and as such constitute the [[mixed state]] which is represented by the [[density matrix]]

$$
  \left\vert \psi \right\rangle
  \left\langle \psi \right\vert
  \;\;\mapsto\;\;
  \underset{w}{\sum}
  \,
  P_w \left\vert \psi \right\rangle
 \left\langle \psi \right\vert P_w
  \,.
$$

In general, if the initial state was [[mixed state|mixed]] to start with, then the stochastic quantum measurement process will be represented by

$$
  \array{
    \mathscr{H}
      \otimes
    \mathscr{H}^\ast
    &\overset{meas_W}{\longrightarrow}&
    \mathscr{H}
      \otimes
    \mathscr{H}^\ast
    \\
    \rho
    &\mapsto&
    \;\;\;\;\;
    \mathclap{
    \underset{w}{\sum}
    \,
    P_w \cdot \rho \cdot P_w
    \mathrlap{\,.}
    }
  }
$$

This is a quantum channel, and quantum channels of this form are called *quantum measurement channels*.

## Properties


[[!include environment rep of quantum measurement channel - section]]




## Related concepts

* [[quantum measurement]]

* [[positive operator valued measure]]

* [[quantum channel]]

  * [[unitary quantum channel]]

  * [[partial trace quantum channel]]


## References

The operation of quantum measurement channels on mixed states first appears (before the general concept of "[[quantum channels]]" was formulated) in:

* {#Lüders51} [[Gerhart Lüders]], equation (8) in:

  *Über die Zustandsänderung durch den Meßprozeß*, Ann. Phys. **8** (1951) 322–328  &lbrack;[doi:10.1002/andp.19504430510](https://doi.org/10.1002/andp.19504430510)&rbrack;

  *Concerning the state-change due to the measurement process*, Ann. Phys. **15** 9 (2006) 663-670 &lbrack;[pdf](http://myweb.rz.uni-augsburg.de/~eckern/adp/history/historic-papers/2006_518_663-670.pdf), [[Lueders-StateChange.pdf:file]]&rbrack;


\begin{imagefromfile}
    "file_name": "Lueders-QuantumMeasurementChannel.jpg",
    "width": 540,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

(In generalization of the formula restricted to [[pure state]] that was previously given by [von Neumann 1932](density+matrix#vonNeumann32)).




[[!redirects quantum measurement channels]]

[[!redirects measurement quantum channel]]
[[!redirects measurement quantum channels]]

[[!redirects generalized quantum measurement channel]]
[[!redirects generalized quantum measurement channels]]



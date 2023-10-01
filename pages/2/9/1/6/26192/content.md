
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

A [[quantum operation]]/[[quantum channel]] $chan \,\colon\, \mathscr{H} \otimes \mathscr{H}^\ast \to \mathscr{H} \otimes \mathscr{H}^\ast$ is called a *noisy operation* &lbrack;by [Horodecki, Horodecki & Oppenheim 2003](#HorodeckiHorodeckiOppenheim03), but beware that this can be ambiguous&rbrack; or a *unistochastic channel* &lbrack;[Życzkowski & Bengtsson 2004](#ŻyczkowskiBengtsson04)&rbrack; if it has an [environmental representation](quantum+channel#QuantumChannelsAndDecoherence) where the environment/bath system $\mathscr{B}$ is in its *[[maximally mixed state|maximally]]* [[mixed quantum state]]:

$$
  chan(\rho)
  \;\;=\;\;
  \mathrm{tr}^{\mathscr{B}}
  \Big(
    U
    \big(
      \rho 
        \otimes 
      \underset{
        \mathclap{
          {maximally \; mixed}
          \atop
          environment    
        }
      }{
        \underbrace{
          \frac{1}{dim(\mathscr{B})}
          id_{\mathscr{B}}
        }
      }
    \big)
    U^\dagger
  \Big)
  \,.
$$

\begin{remark}
  The theorem ([here](quantum+channel#QuantumChannelsAsPartialTracesOfUnitariesOnTensors)) that every endo-[[quantum channel]] has an environmental representation is sometimes advertized with the addendum that "... and such that the environment may be chosen to be in a pure state". But existing general proofs actually produce *only* such environmental representations. For environments in non-pure states it is not clear that they can environmentally represent all quantum channels, and for noisy/unistochastic channels it is not to be expected that they exhaust all quantum channels.

But [Müller-Hermes & Perry 2019](#Müller-HermesPerry19) show that at least all *[[unital quantum channels]]* on single [[qbits]] can be realized as noisy/unistochastic channels (with a bath of size at least 4).
\end{remark}

\begin{remark}
**(DQC1 model)**
\linebreak
But the idea of exploring [[quantum computation]]/[[quantum information theory]] on (a few or just single) clean [[qbits]] coupled to an environment in a maximally [[mixed state]] goes back already to [Knill & Laflamme 1998](#KnillLaflamme98), who referred to this model of computation as *deterministic quantum computation with one quantum bit* (abbreviated "*DQC1*", now also used for the corresponding [[quantum complexity theory|quantum complexity ]] [[complexity class|class]], first studied by [Shor 2008](#Shor08), and often referred as the "one clean qbit"-model). 

> The DQC1 model is believed to be a very restricted, but still genuinely quantum, computing model -- a sub-universal quantum computing model whose power is something between classical computation and universal quantum computation. &lbrack;[FKMNTT18, p. 2](#FKMNTT18)&rbrack;

The communities using these different terminologies for closely related ideas may have been somewhat disconnected. A proposal to look at DQC1 in terms of [[quantum channels]] seems to not appear not before [Xuereb, Campbell, Goold & Xuereb 2023](#XuerebCampbellGooldXuereb23); [Fu, He, Li & Luo 2023](#FuHeLiLuo23) (and the "unistochastic" terminology is not used there).
\end{remark}


## Examples

\begin{example}
\label{UniformlyMixedUnitaryChannelsAreUnistochastic}
Any [[mixed unitary quantum channel]] for a *uniform* [[probability distribution]], i.e. one of the form
$$
  \rho
  \;\mapsto\;
  \tfrac{1}{Card(S)}
  \underset{s \colon S}{\sum}
  \,
  U_s \cdot \rho \cdot U_s^\dagger,
  \;\;\;\;
  \,,
$$
for unitaries
$$
  s\,\colon\, S
  \;\;\;\;\;\;
  \vdash
  \;\;\;\;\;\;
  U_s \,\colon\, \mathscr{H}_1 \to \mathscr{H}_2
$$
is unistochastic, as evidently exhibited by the following coupling unitary
$$
  U_tot
  \;\colon\;
  \mathscr{H}_1 \otimes \underset{S}{\oplus} \mathbb{C}
  \to
  \mathscr{H}_2 \otimes \underset{S}{\oplus} \mathbb{C}
$$
\[
  \label{CouplingMatrixForUniformMixedUnitaryChannel}
  U_{tot}
  \;\;\coloneqq\;\;
  \tfrac{1}{Card(S)}
  \underset{s \colon S}{\sum}
  \,
  U_s 
    \otimes 
  \left\vert s \right\rangle 
  \left\langle s \right\vert
  \mathrlap{\,.}
\]
\end{example}
(cf. [Müller-Hermes & Perry 2019, proof of Cor. 1.4](#Müller-HermesPerry19))

\begin{proposition}
  \label{MixedUnitaryChannelsOnSIngleQBitAreUnistochastic}
  On a single [[qbit]], every [[mixed unitary quantum channel]]  is a unistochastic channel.
\end{proposition}
([Müller-Hermes & Perry 2019, Cor 1.4](#Müller-HermesPerry19))
\begin{proof}
By Exp. \ref{UniformlyMixedUnitaryChannelsAreUnistochastic} one is reduced to showing that on QBits every mixed unitary quantum channel equals one with uniformly distributed unitaries (this is [M-H & P 19, Thm. 1.2](#Müller-HermesPerry19)). We further spell out the case where there are two unitaries to start with ([M-H & P 19, Lem. 1.1](#Müller-HermesPerry19)):

So let the mixed unitary channel be given by
$$
  \rho
  \;\mapsto\;
  p_1 \, U_1 \cdot \rho \cdot U_1^\dagger
  \;+\;
  p_2 \, U_2 \cdot \rho \cdot U_2^\dagger
$$
then we want to find $U'_i$ with
$$
  p_1 \, U_1 \cdot (\text{-}) \cdot U_1^\dagger
  \;+\;
  p_2 \, U_2 \cdot (\text{-}) \cdot U_2^\dagger
  \;\;
  =
  \;\;
  \tfrac{1}{2}
  \,
  U'_1 \cdot (\text{-}) \cdot U'_1^\dagger
  \;+\;
  \tfrac{1}{2}
  \,
  U'_2 \cdot (\text{-}) \cdot U'_2^\dagger
  \,.
$$
First, by replacing $(\text{-}) \mapsto S \cdot (\text{-}) S^\dagger$ --- for a unitary $S$ to be specified in a moment ---, this is equivalent to
$$
  \begin{array}{r}
  p_1 \, U_1 \cdot S \cdot (\text{-}) \cdot S^\dagger \cdot U_1^\dagger
  \\
  +\;
  p_2 \, U_2 \cdot S \cdot (\text{-}) \cdot S^\dagger \cdot U_2^\dagger
  \end{array}
  \;\;
  =
  \;\;
  \begin{array}{r}
  \tfrac{1}{2}
  \,
  U'_1 \cdot S \cdot (\text{-}) \cdot S^\dagger \cdot U'_1^\dagger
  \\
  +
  \;
  \tfrac{1}{2}
  \,
  U'_2 \cdot S \cdot (\text{-}) \cdot S^\dagger \cdot U'_2^\dagger
  \mathrlap{\,.}
  \end{array}
$$
and then conjugating both sides by $S^\dagger \cdot U^\dagger_1$  gives that this is equivalent to
\[
  \label{IntermediateStepInQBitArgument}
  p_1 \, (\text{-})
  \;+\;
  p_2 \, 
  \underset{D}{
  \underbrace{
    S^\dagger U_1^\dagger \cdot U_2 \cdot S
  } }
  \cdot 
  (\text{-}) 
  \cdot 
  \underset{D^\dagger}{
  \underbrace{
    S^\dagger \cdot U_2^\dagger \cdot U_1 \cdot S
  }
  }
  \;\;
  =
  \;\;  
  \begin{array}{r}
  \tfrac{1}{2}
  \,
  \underset{ W_1 }{
  \underbrace{
    S^\dagger \cdot U_1^\dagger \cdot U'_1 \cdot S 
  }
  }
  \cdot 
    (\text{-}) 
  \cdot 
  \underset{
    W_1^\dagger
  }{
  \underbrace{
    S^\dagger \cdot U'_1^\dagger \cdot U_1 \cdot S
  }
  }
  \\
  +
  \;
  \tfrac{1}{2}
  \,
  \underset{
    W_2
  }{
    \underbrace{
      S^\dagger \cdot U_1^\dagger \cdot U'_2 \cdot S 
    }
  }
  \cdot 
  (\text{-}) 
  \cdot 
  \underset{W_2^\dagger}{
    \underbrace{
      S^\dagger \cdot U'_2^\dagger \cdot U_1 \cdot S
    }
  }
  \end{array}
\]
At this point we fix $S$: Since $U_1^\dagger \cdot U_2$ is evidently a [[normal operator]], the [[spectral theorem]] applies to show that we may find $S$ such that $D$ above is a [[diagonal matrix]]:
\[
  \label{DiagonalizingOperatorInQBitArgument}
  S \cdot U_1^\dagger \cdot U_2 \cdot S^\dagger
  \;\;=\;\;
  diag\big( D_{11}, \, D_{22} \big)
  \,=\,
  D
  \,.
\]

This way we are now reduced to finding unitary operators $W_i$, such that
$$
  p_1 \, (\text{-})
  \;+\;
  p_2
  \,
  D \cdot (\text{-}) \cdot D^\dagger
  \;\;
  =
  \;\;
  \tfrac{1}{2}
  \,
  W_1 \cdot (\text{-}) \cdot W_1^\dagger
  \;+\;
  \tfrac{1}{2}
  \,
  W_2 \cdot (\text{-}) \cdot W_2^\dagger
  \,.
$$
Plugging in the simple ansatz
$$
  W_i 
  \;\coloneqq\;
  \left[
  \array{
    e^{2 \pi \mathrm{i} \phi_i } & 0
    \\
    0 & 1
  }
  \right]
$$
shows that this works for
\[
  \label{PhaseConditionForQBitArgument}
  \tfrac{1}{2}
  \big(
    e^{2 \pi \mathrm{i} \phi_1}
    +
    e^{2 \pi \mathrm{i} \phi_2}
  \big)
  \;\;
  =
  \;\;
  p_1 
  \,+\, 
  p_2 
  \,
  D_11 \overline{D_22}
  \mathrlap{\,.}
\]
which always has a solution for the $\phi_i$ ([M-H & P 19, p. 3](#Müller-HermesPerry19)).

Finally plugging back into (eq:IntermediateStepInQBitArgument) shows that the desired uniformly distributed unitaries may be taken to be:
$$
  \label{UniformUnitariesInQBitCase}
  U'_i
  \;\;\coloneqq\;\;
  U_1
  \cdot
  S
  \cdot
  \left[
  \array{
    e^{2 \pi \mathrm{i} \phi_i} & 0
    \\
    0 & 1
  }
  \right]
  \cdot
  S^\dagger
  \,.
$$
\end{proof}




\begin{example}
\label{BitFlipAsUnistochasticChannel}
The [[bit-flip quantum channel]] 
\[
  \label{OrdinaryBitFlipChannel}
  \array{
    \mathllap{ 
      flip_p 
      \;\colon\; 
    }
    QBit \otimes QBit^\ast
    &\longrightarrow&
    QBit \otimes QBit^\ast
    \\
    \rho &\mapsto&
    (1-p)\,\rho
    \;+\;
    p \, X \cdot \rho \cdot X
  }
\]
is unistochastic, by Exp. \ref{MixedUnitaryChannelsOnSIngleQBitAreUnistochastic}, since it is manifestly [[mixed unitary quantum channel|mixed unitary]].

Explicitly, the unitary $S$ (eq:DiagonalizingOperatorInQBitArgument) in this case may be taken to be
$$
  S 
  \;=\;
  \tfrac{1}{\sqrt{2}}
  \left[
  \array{
    1 & 1 
    \\
    -1 & 1
  }
  \right]
$$
which gives
$$
  D
  \;\;
  =
  \;\;
  \tfrac{1}{\sqrt{2}}
  \left[
  \array{
    1 & 1 
    \\
    -1 & 1
  }
  \right]
  \cdot
  \underset{
    X
  }{
  \underbrace{
  \left[
  \array{
    0 & 1 
    \\
    1 & 0
  }
  \right]
  }
  }
  \cdot
  \tfrac{1}{\sqrt{2}}
  \left[
  \array{
    1 & -1 
    \\
    1 & 1
  }
  \right]
  \;\;
  =
  \;\;
  \left[
  \array{
    1 & 0 
    \\
    0 & -1
  }
  \right]
  \mathrlap{\,,}
$$
and the condition (eq:PhaseConditionForQBitArgument) in this case is
$$
  \tfrac{1}{2}
  \big(
    e^{2 \pi \mathrm{i} \phi_1}
    +
    e^{2 \pi \mathrm{i} \phi_2}
  \big)
  \;\;
  =
  \;\;
  (1 - 2 p)
  \,.
$$
This is solved for 
$$
  \phi_1 = -\phi_2 = arccos(1-2p)
  \,,
$$
so that the desired unitary operators as obtained from formula (eq:UniformUnitariesInQBitCase) are:
$$
  \begin{array}{l}
  U_{1/2}
  \\
  \;=\;
  \tfrac{1}{\sqrt{2}}
  \left[
  \array{
    1 & 1 
    \\
    -1 & 1
  }
  \right]
  \cdot
  \left[
  \array{
    e^{ \pm \mathrm{i} \phi }
    & 0
    \\
    0 & 1
  }
  \right]
  \cdot   
  \tfrac{1}{\sqrt{2}}
  \left[
  \array{
    1 & -1 
    \\
    1 & 1
  }
  \right] 
  \\
  \;=\;
  \tfrac{1}{2}
  \left[
  \array{
    1 + e^{ \pm \mathrm{i} \phi } 
    & 
    1 - e^{ \pm \mathrm{i} \phi }
    \\
    1 - e^{ \pm \mathrm{i} \phi } 
    & 
    1 + e^{ \pm \mathrm{i} \phi } 
  }
  \right]
  \\
  \;=\;
  \tfrac{1}{2}
  e^{ \pm \mathrm{i} \phi/2 }
  \left[
  \array{
    e^{ \mp \mathrm{i} \phi/2 } + e^{ \pm \mathrm{i} \phi/2 } 
    & 
    e^{ \mp \mathrm{i} \phi/2 } - e^{ \pm \mathrm{i} \phi/2 }
    \\
    e^{ \mp \mathrm{i} \phi/2 } - e^{ \pm \mathrm{i} \phi/2 } 
    & 
    e^{ \mp \mathrm{i} \phi/2 } + e^{ \pm \mathrm{i} \phi/2 } 
  }
  \right]
  \\  
  \;=\;
  e^{ \pm \mathrm{i} \phi/2 }
  \left[
  \array{
    cos(\phi/2) & \pm\mathrm{i}\,sin(\phi/2)
    \\
    \pm\mathrm{i}\,sin(\phi/2) & cos(\phi/2)
  }
  \right]
  \mathrlap{\,.}
  \end{array}
$$
for 
$$
  \phi
  \,\coloneqq\,
  arccos(1-2p)
  \,.
$$

Hence a uniformly mixed unitary channel representation of the [[bit-flip quantum channel]] (eq:OrdinaryBitFlipChannel) is:
\[
  \label{UniformlyMixedUnitaryFormOfBitFliChannel}
  \begin{array}{rcl}
  flip_p(\rho)
  &=&
  \tfrac{1}{2}
  \,
  \left[
  \array{
    cos(\phi/2) & -\mathrm{i}\,sin(\phi/2)
    \\
    -\mathrm{i}\,sin(\phi/2) & cos(\phi/2)
  }
  \right]
  \cdot 
  \rho
  \cdot
  \left[
  \array{
    cos(\phi/2) & +\mathrm{i}\,sin(\phi/2)
    \\
    +\mathrm{i}\,sin(\phi/2) & cos(\phi/2)
  }
  \right]
  \\
  &+&
  \tfrac{1}{2}
  \,
  \left[
  \array{
    cos(\phi/2) & +\mathrm{i}\,sin(\phi/2)
    \\
    +\mathrm{i}\,sin(\phi/2) & cos(\phi/2)
  }
  \right]
  \cdot 
  \rho
  \cdot
  \left[
  \array{
    cos(\phi/2) & -\mathrm{i}\,sin(\phi/2)
    \\
    -\mathrm{i}\,sin(\phi/2) & cos(\phi/2)
  }
  \right]
  \mathrlap{\,,}
  \\
  &&
  \text{where}\;
  \phi
  \,\equiv\,
  arccos(1-2p)
  \text{.}
  \end{array}
\]
With (eq:CouplingMatrixForUniformMixedUnitaryChannel) this uniformly mixed unitary presentation immediately gives the unistochastic presentation of the bit-flip channel. 
\end{example}

## References

### DQC1 computation

The exploration of the possibilities of [[quantum computing]]/[[quantum information theory]] with (a few or even just single) "clean" [[qubits]] coupled to a [[maximally mixed state]] environment goes back to

* {#KnillLaflamme98} [[Emanuel Knill]], [[Raymond Laflamme]], *On the Power of One Bit of Quantum Information*, Phys. Rev. Lett. **81** (1998) 5672-5675 &lbrack;[arXiv:quant-ph/9802037](https://arxiv.org/abs/quant-ph/9802037), [doi:10.1103/PhysRevLett.81.5672](https://doi.org/10.1103/PhysRevLett.81.5672)&rbrack;

(motivated by the practical reality of [[NMR]] [[spin resonance qbits]]) who called this model of computation *deterministic quantum computation with one quantum bit (DQC1)*.

The model was further discussed in:

* [[David Poulin]], [[Raymond Laflamme]], [[Gerard J. Milburn]], [[Juan Pablo Paz]], *Testing integrability with a single bit of quantum information*, Phys. Rev. A **68** 22302 (2003) &lbrack;[arXiv:quant-ph/0303042](https://arxiv.org/abs/quant-ph/0303042), [doi:10.1103/PhysRevA.68.022302](https://doi.org/10.1103/PhysRevA.68.022302)&rbrack;

* [[David Poulin]], Robin Blume-Kohout, [[Raymond Laflamme]], Harold Ollivier, around (2) of:  *Exponential speed-up with a single bit of quantum information: Testing the quantum butterfly effect*, Phys. Rev. Lett. **92** 177906 (2004) &lbrack;[arXiv:quant-ph/0310038](https://arxiv.org/abs/quant-ph/0310038), [doi:10.1103/PhysRevLett.92.177906](https://doi.org/10.1103/PhysRevLett.92.177906)&rbrack;

* {#Shor08} [[Peter W. Shor]], Stephen P. Jordan, *Estimating Jones polynomials is a complete problem for one clean qubit*, Quantum Information and Computation **8** (2008) 681 &lbrack;[arXiv:0707.2831](https://arxiv.org/abs/0707.2831), [doi:10.5555/2017011.2017012](https://dl.acm.org/doi/10.5555/2017011.2017012)&rbrack;

* Dan Shepherd, *Computation with Unitaries and One Pure Qubit* &lbrack;[arXiv:quant-ph/0608132](https://arxiv.org/abs/quant-ph/0608132)&rbrack;

* Chris Cade, Ashley Montanaro, *The Quantum Complexity of Computing Schatten $p$-norms* &lbrack;[arXiv:1706.09279](https://arxiv.org/abs/1706.09279)&rbrack;

See also:

* Wikipedia, *[One Clean QBit](https://en.wikipedia.org/wiki/One_Clean_Qubit)*.

Discussion where even the single system qbit is not fully coherent, either:

* Tomoyuki Morimae, Keisuke Fujii, Harumichi Nishimura, *Power of one non-clean qubit*, Phys. Rev. A *95* 042336 (2017) &lbrack;[arXiv:1610.07244](https://arxiv.org/abs/1610.07244), [doi:10.1103/PhysRevA.95.042336](https://doi.org/10.1103/PhysRevA.95.042336)&rbrack;

Proof that all [[unital quantum channels]] on single [[qubits]] are unistochastic (noisy operations) for a bath of size at least 4:

* {#Müller-HermesPerry19} Alexander Müller-Hermes, Christopher Perry, *All unital qubit channels are 4-noisy operations*, Letters in Mathematical Physics **109** (2019) 1–9 &lbrack;[doi:10.1007/s11005-018-1104-x](https://doi.org/10.1007/s11005-018-1104-x), [arXiv:1802.01337](https://arxiv.org/abs/1802.01337)&rbrack;


Discussion of DQC1 in the language of [[quantum channels]]:

* {#XuerebCampbellGooldXuereb23} Jake Xuereb, Steve Campbell, John Goold, André Xuereb, *DQC1 as an Open Quantum System*, Phys. Rev. A **107** 042222 (2023) &lbrack;[arXiv:2209.03947](https://arxiv.org/abs/2209.03947), [doi:10.1103/PhysRevA.107.042222](https://doi.org/10.1103/PhysRevA.107.042222)&rbrack;

* {#FuHeLiLuo23} Shuangshuang Fu, Jiayu He, Xiaohui Li and Shunlong Luo, *Uncertainties and coherence in DQC1*, Physica Scripta, **98** 4 (2023) &lbrack;[doi:10.1088/1402-4896/acc5ba](https://iopscience.iop.org/article/10.1088/1402-4896/acc5ba)&rbrack;

Discussion of classical simulation (or not) of the DQC1 model

* {#FKMNTT18} Keisuke Fujii, Hirotada Kobayashi, Tomoyuki Morimae, Harumichi Nishimura, Shuhei Tamate, Seiichiro Tani, *Impossibility of Classically Simulating One-Clean-Qubit Computation*,  	Phys. Rev. Lett. **120** 200502 (2018) &lbrack;[arXiv:1409.6777](https://arxiv.org/abs/1409.6777), [doi:10.1103/PhysRevLett.120.200502](https://doi.org/10.1103/PhysRevLett.120.200502)&rbrack;


### Noisy operations/unistochastic channels

The terminology of "noisy operations" is due to  

* {#HorodeckiHorodeckiOppenheim03} [[Michal Horodecki]], [[Pawel Horodecki]], [[Jonathan Oppenheim]], *Reversible transformations from pure to mixed states, and the unique measure of information*, Phys. Rev. A 67 062104 (2003) &lbrack;[doi:10.1103/PhysRevA.67.062104](https://doi.org/10.1103/PhysRevA.67.062104), [arXiv;quant-ph/0212019](https://arxiv.org/abs/quant-ph/0212019)&rbrack;

* picked up by [Müller-Hermes & Perry 2019](#Müller-HermesPerry19)

and the terminology "unistochastic channels" was introduced in:

* {#ŻyczkowskiBengtsson04} [[Karol Życzkowski]], [[Ingemar Bengtsson]], p. 13 of: *On Duality between Quantum Maps and Quantum States*, Open Systems & Information Dynamics **11** 01 (2004) 3-42 &lbrack;[doi:10.1023/B:OPSY.0000024753.05661.c2](https://doi.org/10.1023/B:OPSY.0000024753.05661.c2)&rbrack;

* {#BengtssonŻyczkowski06} [[Ingemar Bengtsson]], [[Karol Życzkowski]], p. 259 of: *Geometry of Quantum States --- An Introduction to Quantum Entanglement*, Cambridge University Press (2006) &lbrack;[doi:10.1017/CBO9780511535048](https://doi.org/10.1017/CBO9780511535048), [ResearchGate](https://www.researchgate.net/publication/266435541_Geometry_of_Quantum_States_An_Introduction_to_Quantum_Entanglement)&rbrack;

* Marcin Musz, Marek Kuś, [[Karol Życzkowski]], *Unitary quantum gates, perfect entanglers, and unistochastic maps*, Phys. Rev. A **87** (2013) 022111 &lbrack;[doi:10.1103/PhysRevA.87.022111](https://doi.org/10.1103/PhysRevA.87.022111)&rbrack;






[[!redirects unistochastic quantum channels]]

[[!redirects noisy quantum operation]]
[[!redirects noisy quantum operations]]

[[!redirects DQC1]]
[[!redirects one clean qbit]]





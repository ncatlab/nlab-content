
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--

#Contemts#
* table of contents
{:toc}

## Idea

A [[quantum operation]]/[[quantum channel]] $chan \,\colon\, \mathscr{H} \otimes \mathscr{H}^\ast \to \mathscr{H} \otimes \mathscr{H}^\ast$ is called a *noisy operation* &lbrack;[Horodecki, Horodecki & Oppenheim 2003](#HorodeckiHorodeckiOppenheim03) but beware that this can be ambiguous&rbrack; or a *unistochastic channel* &lbrack;[Życzkowski & Bengtsson 2004](#ŻyczkowskiBengtsson04)&rbrack; if it has an [environmental representation](quantum+channel#QuantumChannelsAndDecoherence) where the environment/bath system $\mathscr{B}$ is in its *maximally* [[mixed quantum state]]:

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
  The theorem ([here](quantum+channel#QuantumChannelsAsPartialTracesOfUnitariesOnTensors)) that every endo-[[quantum channel]] has an environmental representation is often advertized with the addendum that "... and such that the environment may be chosen to be in a pure state". But existing general proofs actually produce *only* such environmental representations. For environments in non-pure states it is not clear that they can environmentally represent all quantum channels, and for noisy/unistochastic channels it is not to be expected that they exhaust all quantum channels.

But [Müller-Hermes & Perry 2019](#Müller-HermesPerry19) show that at least all *[[unital quantum channels]]* on [[qbits]]  can be realized as noisy/unistochastic channels (with a bath of size at least 4).
\end{remark}

## References

Precursor discussion of the concept is due to:

* {#HorodeckiHorodeckiOppenheim03} [[Michal Horodecki]], [[Pawel Horodecki]], [[Jonathan Oppenheim]], *Reversible transformations from pure to mixed states, and the unique measure of information*, Phys. Rev. A 67 062104 (2003) &lbrack;[doi:10.1103/PhysRevA.67.062104](https://doi.org/10.1103/PhysRevA.67.062104), [arXiv;quant-ph/0212019](https://arxiv.org/abs/quant-ph/0212019)&rbrack;

  > (who speak of "noisy operations")

* [[David Poulin]], Robin Blume-Kohout, [[Raymond Laflamme]], Harold Ollivier, around (2) of:  *Exponential speed-up with a single bit of quantum information: Testing the quantum butterfly effect*, Phys. Rev. Lett. **92** 177906 (2004) &lbrack;[arXiv:quant-ph/0310038](https://arxiv.org/abs/quant-ph/0310038), [doi:10.1103/PhysRevLett.92.177906](https://doi.org/10.1103/PhysRevLett.92.177906)&rbrack;


The terminology "unistochastic channels" was introduced in:

* {#ŻyczkowskiBengtsson04} [[Karol Życzkowski]], [[Ingemar Bengtsson]], p. 13 of: *On Duality between Quantum Maps and Quantum States*, Open Systems & Information Dynamics **11** 01 (2004) 3-42 &lbrack;[doi:10.1023/B:OPSY.0000024753.05661.c2](https://doi.org/10.1023/B:OPSY.0000024753.05661.c2)&rbrack;

* {#BengtssonŻyczkowski06} [[Ingemar Bengtsson]], [[Karol Życzkowski]], p. 259 of: *Geometry of Quantum States --- An Introduction to Quantum Entanglement*, Cambridge University Press (2006) &lbrack;[doi:10.1017/CBO9780511535048](https://doi.org/10.1017/CBO9780511535048), [ResearchGate](https://www.researchgate.net/publication/266435541_Geometry_of_Quantum_States_An_Introduction_to_Quantum_Entanglement)&rbrack;

* Marcin Musz, Marek Kuś, [[Karol Życzkowski]], *Unitary quantum gates, perfect entanglers, and unistochastic maps*, Phys. Rev. A **87** (2013) 022111 &lbrack;[doi:10.1103/PhysRevA.87.022111](https://doi.org/10.1103/PhysRevA.87.022111)&rbrack;

Proof that all [[unital quantum channels]] on [[qubits]] are unistochastic (noisy operations) for a bath of size at least 4:

* {#Müller-HermesPerry19} Alexander Müller-Hermes, Christopher Perry, *All unital qubit channels are 4-noisy operations*, Letters in Mathematical Physics **109** (2019) 1–9 &lbrack;[doi:10.1007/s11005-018-1104-x](https://doi.org/10.1007/s11005-018-1104-x), [arXiv:1802.01337](https://arxiv.org/abs/1802.01337)&rbrack;


[[!redirects unistochastic quantum channels]]

[[!redirects noisy quantum operation]]
[[!redirects noisy quantum operations]]







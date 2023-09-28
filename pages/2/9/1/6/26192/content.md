
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

A [[quantum operation]]/[[quantum channel]] $chan \,\colon\, \mathscr{H} \otimes \mathscr{H}^\ast \to \mathscr{H} \otimes \mathscr{H}^\ast$ is called a *noisy operation* &lbrack;by [Horodecki, Horodecki & Oppenheim 2003](#HorodeckiHorodeckiOppenheim03), but beware that this can be ambiguous&rbrack; or a *unistochastic channel* &lbrack;[Życzkowski & Bengtsson 2004](#ŻyczkowskiBengtsson04)&rbrack; if it has an [environmental representation](quantum+channel#QuantumChannelsAndDecoherence) where the environment/bath system $\mathscr{B}$ is in its *maximally* [[mixed quantum state]]:

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
But the idea of exploring [[quantum computation]]/[[quantum information theory]] on (a few or just single) clean [[qbits]] coupled to an environment in a maximally [[mixed state]] goes back already to [Knill & Laflamme 1998](#KnillLaflamme98), who referred to this model of computation as *deterministic quantum computation with one quantum bit* (abbreviated "*DQC1*", now also used for the corresponding [[quantum complexity theory|quantum complexity ]] [[complexity class|class]], first studied by [Shor 2008](#Shor08), and often referred to by the phrase "one clean qbit"). 

The communities using these different terminologies for closely related ideas may have been somewhat disconnected. A proposal to look at DQC1 in terms of [[quantum channels]] seems to not appear not before [Xuereb, Campbell, Goold & Xuereb 2023](#XuerebCampbellGooldXuereb23); [Fu, He, Li & Luo 2023](#FuHeLiLuo23) (and the "unistochastic" terminology is not used there).
\end{remark}


## References

### DQC1 computation

The exploration of the possibilities of [[quantum computing]]/[[quantum information theory]] with (a few or even just single) "clean" [[qubits]] coupled to a maximally mixed environment goes back to

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





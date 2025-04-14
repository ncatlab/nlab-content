

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion that for certain tasks the power of [[quantum computation]] potentially drastically surpasses that of [[classical physics|classical]] [[computation]] (e.g. via [[quantum algorithms]] such as [[Shor's algorithm]]) has been called *quantum supremacy* ([Preskill 2013](#Preskill13), there related to the computational resource of [[quantum entanglement]]) or *quantum advantage*.

## Related concepts

* [[quantum complexity theory]]

## References
 {#References}

### General

The term "quantum supremacy" is due to:

* {#Preskill13} [[John Preskill]]: *Quantum computing and the entanglement frontier*: pp. 63-80 in: *The Theory of the Quantum World -- Proceedings of the 25th Solvay Conference on Physics*, World Scientific (2013) &lbrack;[arXiv:1203.5813](https://arxiv.org/abs/1203.5813), [doi:10.1142/8674](https://doi.org/10.1142/8674), slides: [pdf](https://simons.berkeley.edu/sites/default/files/docs/394/preskilljohn.pdf)&rbrack;

See also:

* Rønnow et al. *Defining and detecting quantum speedup*, Science **345** 6195 (2014) 420-424 &lbrack;[doi:10.1126/science.1252319](https://doi.org/10.1126/science.1252319)&rbrack;


* Wikipedia, *[Quantum supremacy](https://en.wikipedia.org/wiki/Quantum_supremacy)*

Review and outlook:

> see also at *[quantum computation -- References - Limits of NISQ](quantum+computation#NISQLimitations)*

* [[Scott Aaronson]], *How Much Structure Is Needed for Huge Quantum Speedups?*, talk at: *28th Solvay Physics Conference* in Brussels on May 21, 2022 &lbrack;[arXiv:2209.06930](https://arxiv.org/abs/2209.06930), slides: [ppt](https://www.scottaaronson.com/talks/aar-solvay.ppt)&rbrack;

* Torsten Hoefler, Thomas Haener, [[Matthias Troyer]], *Disentangling Hype from Practicality: On Realistically Achieving Quantum Advantage*, Communications of the ACM **66**  5 (May 2023) 82-87 &lbrack;[arXiv:2307.00523](https://arxiv.org/abs/2307.00523), [acm pdf](https://dl.acm.org/doi/pdf/10.1145/3571725), [doi:10.1145/3571725](https://doi.org/10.1145/3571725)&rbrack;

  > "A large range of problem areas with quadratic quantum speedups, such as many current machine learning training approaches, accelerating drug design and protein folding with Grover’s algorithm, speeding up Monte Carlo simulations through quantum walks, as well as more traditional scientific computing simulations including the solution of many non-linear systems of equations, such as fluid dynamics in the turbulent regime, weather, and climate simulations will not achieve quantum advantage with current quantum algorithms in the foreseeable future."

* Ryan Babbush, Jarrod R. McClean, Michael Newman, [[Craig Gidney]], Sergio Boixo, Hartmut Neven, *Focus beyond Quadratic Speedups for Error-Corrected Quantum Advantage*, PRX Quantum **2** 010103 (2021) &lbrack;[doi:10.1103/PRXQuantum.2.010103](https://doi.org/10.1103/PRXQuantum.2.010103)&rbrack;


* {#LaRose24} Ryan LaRose: *A brief history of quantum vs classical computational advantage* &lbrack;[arXiv:2412.14703](https://arxiv.org/abs/2412.14703)&rbrack;



Emphasis of the need of [[topological quantum computation|topological stabilization]]:

* {#DasSarma22} [[Sankar Das Sarma]], *Quantum computing has a hype problem*, [MIT Technology Review (March 2022)](https://www.technologyreview.com/2022/03/28/1048355/quantum-computing-has-a-hype-problem/)

  > The [[qubit]] systems we have today are a tremendous scientific achievement, but they take us no closer to having a quantum computer that can solve a problem that anybody cares about. $[\cdots]$ What is missing is the breakthrough \[...\] bypassing [[quantum error correction]] by using far-more-stable qubits, in an approach called [[topological quantum computing]].

See also:

* Takashi Yamakawa, Mark Zhandry, *Verifiable Quantum Advantage without Structure* &lbrack;[arXiv:2204.02063](https://arxiv.org/abs/2204.02063)&rbrack;


### Experimental realizations

Claimed experimental demonstration of "quantum supremacy" ("quantum advantage") in (very) special purpose applications:

* F. Arute et al. *Quantum supremacy using a programmable superconducting processor*, Nature **574** (2019) 505–510 ([doi:10.1038/s41586-019-1666-5](https://doi.org/10.1038/s41586-019-1666-5))

* Han-Sen Zhong et al., *Quantum computational advantage using photons*, Science  **370** 6523 (2020) 1460-1463 ([doi:10.1126/science.abe8770](https://science.sciencemag.org/content/370/6523/1460))

Critical analysis:

* [[Gil Kalai]], Yosef Rinott, Tomer Shoham, *Google's 2019 "Quantum Supremacy" Claims: Data, Documentation, and Discussion* &lbrack;[arXiv:2210.12753](https://arxiv.org/abs/2210.12753)&rbrack;

Classical computations competing with these claims:

* Zhao et al.: *Leapfrogging Sycamore: Harnessing 1432 GPUs for 7× Faster Quantum Random Circuit Sampling* &lbrack;[arXiv:2406.18889](https://arxiv.org/abs/2406.18889)&rbrack;

  > "Here we report an energy-efficient classical simulation algorithm, using 1432 GPUs &lbrack;which is&rbrack; 7 times faster than *Sycamore* 53 qubits experiment."

  > arXiv Comments: "This work was completed on August 2023. A further 50x improvement has been achieved and will be posted on arXiv shortly"


{#ExperimentalReview} Review and status reports:

* Adrian Cho, *Google claims quantum computing milestone*, Science **365** 6460 (2019) 1364 ([doi:10.1126/science.365.6460.1364](https://science.sciencemag.org/content/365/6460/1364))

* [[Philip Ball]], *Physicists in China challenge Google’s "quantum advantage"*, Nature **588** 380 (2020) &lbrack;[doi:10.1038/d41586-020-03434-7](https://doi.org/10.1038/d41586-020-03434-7)&rbrack;

* Barry C. Sanders, *[Quantum Leap for Quantum Primacy](https://physics.aps.org/articles/v14/147)*, Physics **14** 147 (2021)

Quantum advantage for [[Grover's algorithm]]:

* Bibek Pokharel, Daniel Lidar, *Better-than-classical Grover search via quantum error detection and suppression* &lbrack;[arXiv:2211.04543](https://arxiv.org/abs/2211.04543)&rbrack;

See also:

* Réouven Assouly, Rémy Dassonneville, Théau Peronnin, Audrey Bienfait, Benjamin Huard, *Demonstration of Quantum Advantage in Microwave Quantum Radar* &lbrack;[arXiv:2211.05684](https://arxiv.org/abs/2211.05684)&rbrack;

    

### Potential applications

Discussion of [[algorithms]] for which quantum computers are expected to outperform classical computers:

The case of [[Shor's algorithm]], relevant for [[quantum cryptography]]:

* [[Peter W. Shor]], *Algorithms for quantum computation: discrete logarithms and factoring*,  Proceedings 35th Annual Symposium on Foundations of Computer Science, IEEE Comput. Soc. Press: 124-134 (1994) &lbrack;[doi:10.1109/SFCS.1994.365700](https://doi.org/10.1109/SFCS.1994.365700)&rbrack;

* [[Daniel R. Simon]], *On the power of quantum computation*, SIAM Journal on Computing **26** 5 (1997) &lbrack;[doi:10.1137/S0097539796298637](https://doi.org/10.1137/S0097539796298637), [pdf](https://courses.cs.washington.edu/courses/cse599/01wi/papers/simon_qc.pdf)&rbrack;

The case of [[Grover's algorithm]], for database searches:

* [[Lov K. Grover]], *A fast quantum mechanical algorithm for database search*, STOC '96: Proceedings of the twenty-eighth annual ACM symposium on Theory of Computing (1996) 212-219 &lbrack;[arXiv:quant-ph/9605043](https://arxiv.org/abs/quant-ph/9605043), [doi:10.1145/237814.237866](https://doi.org/10.1145/237814.237866)&rbrack;

The case of the [[Deutsch-Jozsa algorithm]]:

* [[David Deutsch]], [[Richard Jozsa]], *Rapid solution of problems by quantum computation*. Proc. R. Soc. Lond. A **439** 1907 (1992) 553-558 &lbrack;[pdf](https://www.isical.ac.in/~rcbose/internship/lectures2016/rt08deutschjozsa.pdf), [doi:10.1098/rspa.1992.0167](https://doi.org/10.1098/rspa.1992.0167)&rbrack;


For [[integral transforms]]:

* Doğa Veske et al., *Quantum Advantage for Integral Transforms* &lbrack;[arXiv:2204.04159](https://arxiv.org/abs/2204.04159)&rbrack;

Survey:

* Andrew M. Childs, Wim van Dam, *Quantum algorithms for algebraic problems*, Rev. Mod. Phys. **82** 1 (2010) &lbrack;[arXiv:0812.0380](https://arxiv.org/abs/0812.0380), [doi:10.1103/RevModPhys.82.1](https://doi.org/10.1103/RevModPhys.82.1)&rbrack;



Application of quantum computing to [[quantum chemistry]]:

* [[Seth Lloyd]], *Universal Quantum Simulators*, Science New Series **273** 5278 (1996) 1073-1078 &lbrack;[jstor:2899535](https://www.jstor.org/stable/2899535), [doi:10.1126/science.273.5278.1073](https://doi.org/10.1126/science.273.5278.1073)&rbrack;

* Yudong Cao et al.: *Quantum Chemistry in the Age of Quantum Computing*, Chem. Rev. (2019) **119** 19 (2019) 10856–10915 &lbrack;[doi:10.1021/acs.chemrev.8b00803](https://doi.org/10.1021/acs.chemrev.8b00803)&rbrack;

Argument that quantum supremacy in quantum chemistry is elusive:

* [[Garnet Kin-Lic Chan]] et al., *Is there evidence for exponential quantum advantage in quantum chemistry?* &lbrack;[arXiv:2208.02199](https://arxiv.org/abs/2208.02199), [talk video](https://youtu.be/DZPH7ENcRLU)&rbrack;

Application to [[solid state physics]]:

* Nobuyuki Yoshioka, Tsuyoshi Okubo, Yasunari Suzuki, Yuki Koizumi, Wataru Mizukami, *Hunting for quantum-classical crossover in condensed matter problems* &lbrack;[arXiv:2210.14109](https://arxiv.org/abs/2210.14109)&rbrack;

In [[quantum simulation]] of the [[Schrödinger equation]]:

* Andrew D. King et al.: *Beyond-classical computation in quantum simulation*, Science
(Mar 2025) &lbrack;[doi:10.1126/science.ad6285](https://doi.org/10.1126/science.ado6285)&rbrack;






### Quantum complexity theory

Discussion of [[complexity theory|complexity-theoretic]] aspects:

* [[Scott Aaronson]], [[Lijie Chen]], *Complexity-Theoretic Foundations of Quantum Supremacy Experiments*, CCC '17: Proceedings of the 32nd Computational Complexity Conference (2017) **22** 1–67 &lbrack;[arXiv:1612.05903](https://arxiv.org/abs/1612.05903), [doi;10.5555/3135595.3135617](https://dl.acm.org/doi/10.5555/3135595.3135617)&rbrack;

[[!redirects quantum advantages]]

[[!redirects quantum supremacy]]



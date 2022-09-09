
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

The notion that for certain tasks the power of [[quantum computation]] potentially drastically surpasses that of [[classical physics|classical]] [[computation]] (e.g. via [[Shor's algorithm]]) has been called *quantum supremacy* ([Preskill 2013](#Preskill13), there related to the computational resource of [[quantum entanglement]]) or *quantum advantage*.

## Related concepts

* [[quantum complexity theory]]

## References

### General

The term "qantum supremacy" is due to:

* {#Preskill13} [[John Preskill]]: *Quantum computing and the entanglement frontier*: pp. 63-80 in: *The Theory of the Quantum World -- Proceedings of the 25th Solvay Conference on Physics*, World Scientific (2013) &lbrack;[arXiv:1203.5813](https://arxiv.org/abs/1203.5813), [doi:10.1142/8674](https://doi.org/10.1142/8674), slides: [pdf](https://simons.berkeley.edu/sites/default/files/docs/394/preskilljohn.pdf)&rbrack;

See also:

* Wikipedia, *[Quantum supremacy](https://en.wikipedia.org/wiki/Quantum_supremacy)*

Emphasis of the need of [[topological quantum computation|topological stabilization]]:

* {#DasSarma22} [[Sankar Das Sarma]], *Quantum computing has a hype problem*, [MIT Technology Review (March 2022)](https://www.technologyreview.com/2022/03/28/1048355/quantum-computing-has-a-hype-problem/)

  > The [[qubit]] systems we have today are a tremendous scientific achievement, but they take us no closer to having a quantum computer that can solve a problem that anybody cares about. $[\cdots]$ What is missing is the breakthrough $[\cdots]$ bypassing [[quantum error correction]] by using far-more-stable qubits, in an approach called [[topological quantum computing]].

See also:

* Takashi Yamakawa, Mark Zhandry, *Verifiable Quantum Advantage without Structure* &lbrack;[arXiv:2204.02063](https://arxiv.org/abs/2204.02063)&rbrack;


### Experimental realizations

Claimed experimental demonstration of "quantum supremacy" ("quantum advantage") in (very) special purpose applications:

* F. Arute et al. *Quantum supremacy using a programmable superconducting processor*, Nature **574** (2019) 505–510 ([doi:10.1038/s41586-019-1666-5](https://doi.org/10.1038/s41586-019-1666-5))

* Han-Sen Zhong et al., *Quantum computational advantage using photons*, Science  **370** 6523 (2020) 1460-1463 ([doi:10.1126/science.abe8770](https://science.sciencemag.org/content/370/6523/1460))

{#ExperimentalReview} Review and status reports:

* Adrian Cho, *Google claims quantum computing milestone*, Science **365** 6460 (2019) 1364 ([doi:10.1126/science.365.6460.1364](https://science.sciencemag.org/content/365/6460/1364))

* [[Philip Ball]], *Physicists in China challenge Google’s "quantum advantage"*, Nature **588** 380 (2020) &lbrack;[doi:10.1038/d41586-020-03434-7](https://doi.org/10.1038/d41586-020-03434-7)&rbrack;

* Barry C. Sanders, *[Quantum Leap for Quantum Primacy](https://physics.aps.org/articles/v14/147)*, Physics **14** 147 (2021)

    

### Potential applications

Discussion of [[algorithms]] for which quantum computers are expected to outperform classical computers:

The case of [[Shor's algorithm]], relevant for [[quantum cryptography]]:

* [[Peter W. Shor]], *Algorithms for quantum computation: discrete logarithms and factoring*,  Proceedings 35th Annual Symposium on Foundations of Computer Science, IEEE Comput. Soc. Press: 124-134 (1994) &lbrack;[doi:10.1109/SFCS.1994.365700](https://doi.org/10.1109/SFCS.1994.365700)&rbrack;

* [[Daniel R. Simon]], *On the power of quantum computation*, SIAM Journal on Computing **26** 5 (1997) &lbrack;[doi:10.1137/S0097539796298637](https://doi.org/10.1137/S0097539796298637), [pdf](https://courses.cs.washington.edu/courses/cse599/01wi/papers/simon_qc.pdf)&rbrack;

The case of [[Grover's algorithm]], for database searches:

* [[Lov K. Grover]], *A fast quantum mechanical algorithm for database search*, STOC '96: Proceedings of the twenty-eighth annual ACM symposium on Theory of Computing (1996) 212-219 &lbrack;[arXiv:quant-ph/9605043](https://arxiv.org/abs/quant-ph/9605043), [doi:10.1145/237814.237866](https://doi.org/10.1145/237814.237866)&rbrack;

The case of the [[Deutsch-Jozsa algorithm]]:

* [[David Deutsch]], [[Richard Jozsa]], *Rapid solution of problems by quantum computation*. Proc. R. Soc. Lond. A **439** 1907 (1992) 553-558 &lbrack;[pdf](https://www.isical.ac.in/~rcbose/internship/lectures2016/rt08deutschjozsa.pdf), [doi:10.1098/rspa.1992.0167](https://doi.org/10.1098/rspa.1992.0167)&rbrack;

Application of quantum computing to [[quantum chemistry]]:

* [[Seth Lloyd]], *Universal Quantum Simulators*, Science New Series **273** 5278 (1996) 1073-1078 &lbrack;[jstor:2899535](https://www.jstor.org/stable/2899535), [doi:10.1126/science.273.5278.1073](https://doi.org/10.1126/science.273.5278.1073)&rbrack;

* *Quantum Chemistry in the Age of Quantum Computing*, Chem. Rev. (2019) **119** 19 (2019) 10856–10915 &lbrack;[doi:10.1021/acs.chemrev.8b00803](https://doi.org/10.1021/acs.chemrev.8b00803)&rbrack;

Argument that quantum supremacy in quantum chemistry is elusive:

* [[Garnet Kin-Lic Chan]] et al., *Is there evidence for exponential quantum advantage in quantum chemistry?* &lbrack;[arXiv:2208.02199](https://arxiv.org/abs/2208.02199), [talk video](https://youtu.be/DZPH7ENcRLU)&rbrack;

Survey:

* Andrew M. Childs, Wim van Dam, *Quantum algorithms for algebraic problems*, Rev. Mod. Phys. **82** 1 (2010) &lbrack;[arXiv:0812.0380](https://arxiv.org/abs/0812.0380), [doi:10.1103/RevModPhys.82.1](https://doi.org/10.1103/RevModPhys.82.1)&rbrack;


### Quantum complexity theory

Discussion of [[complexity theory|complexity-theoretic]] aspects:

* [[Scott Aaronson]], [[Lijie Chen]], *Complexity-Theoretic Foundations of Quantum Supremacy Experiments*, CCC '17: Proceedings of the 32nd Computational Complexity Conference (2017) **22** 1–67 &lbrack;[arXiv:1612.05903](https://arxiv.org/abs/1612.05903), [doi;10.5555/3135595.3135617](https://dl.acm.org/doi/10.5555/3135595.3135617)&rbrack;


[[!redirects quantum advantage]]


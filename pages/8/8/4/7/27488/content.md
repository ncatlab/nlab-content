
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


\tableofcontents


## Idea

The *quantum Fourier transform* (QFT) is an analog of the [[discrete Fourier transform]], acting on [[quantum states]].


The QFT is a crucial ingredient in several [[quantum algorithms]], notably in [[Shor's algorithm]]. 

Nominally, the QFT on an [[finite-dimensional Hilbert space|$n$-dimensional Hilbert space]] requires only $\mathcal{O}(n^2)$ [[quantum gates]], as opposed to the $\mathcal{O}(n 2^n)$ [[logic gates]] for the classical [[discrete Fourier transform]] on $n$-dimensional vectors. However, this nominal speedup is not practically extractable for computation of [[Fourier transforms]], since classical en- and de-coding of the data for the QFT is impractical: the Fourier transformed vector is in the *[[complex phases]]* of the [[coefficients]] of the output [[quantum state]], which are not directly [[quantum measurement|measurable]]. &lbrack;[Nielsen & Chuang 2000 p 220](#NielsenChuang00)&rbrack;.

However there are practically accessible [[quantum algorithms]] with [[quantum advantage]] which rely the QFT as a sub-routine, notably "quantum phase estimation" &lbrack;[NC00 §5.2](#NielsenChuang00)&rbrack; (used, in turn, in [[Shor's algorithm]]).



## Related concepts

* [[Fourier transform]]

* [[Shor's algorithm]]

* [[rotation gate]]

## References

Textbook account:

* {#NielsenChuang00} [[Michael A. Nielsen]], [[Isaac L. Chuang]], chapter 5 in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

See also: 

* Wikipedia: *[Quantum Fourier Transform](https://en.wikipedia.org/wiki/Quantum_Fourier_transform)*

Generalization of the QFT algorithm from [[qbits]] to a platform of *[[qdits]]*:

* Ashok Muthukrishnan, C. R. Stroud Jr: *Quantum fast Fourier transform using multilevel atoms*, Journal of Modern Optics **49** 13 (2002) &lbrack;[arXiv:quant-ph/0112017](https://arxiv.org/abs/quant-ph/0112017), [doi:10.1080/09500340210123947](https://doi.org/10.1080/09500340210123947)&rbrack;


* Zeljko Zilic, Katarzyna Radecka: *Scaling and better approximating quantum Fourier transform by higher radices*, IEEE Transactions on Computers **56** 2 (2007) 202-207 &lbrack;[arXiv:quant-ph/0702195](https://arxiv.org/abs/quant-ph/0702195), [doi:10.1109/TC.2007.35](https://doi.org/10.1109/TC.2007.35)&rbrack;

* Cao Ye et al.: *Quantum Fourier Transform and Phase Estimation in Qudit System*, Commun. Theor. Phys. **55** 790 (2011) &lbrack;[doi:10.1088/0253-6102/55/5/11](https://iopscience.iop.org/article/10.1088/0253-6102/55/5/11)&rbrack;

Review of the qdit formulation:

* Yuchen Wang, Zixuan Hu, Barry C. Sanders, Sabre Kais, section 3.2.1 of: *Qudits and high-dimensional quantum computing*, Front. Phys. **8** 479 (2020) &lbrack;[arXiv:2008.00959](https://arxiv.org/abs/2008.00959), [doi:10.3389/fphy.2020.589504](https://doi.org/10.3389/fphy.2020.589504)&rbrack;





[[!redirects quantum Fourier transforms]]

[[!redirects quantum phase estimation]]
[[!redirects quantum phase estimations]]


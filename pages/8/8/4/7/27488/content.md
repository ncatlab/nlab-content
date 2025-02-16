
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

The *quantum Fourier transform* (QFT) is an analog of the [[discrete Fourier transform]] acting on [[quantum states]].


The QFT is a crucial ingredient in several [[quantum algorithms]], notably in [[Shor's algorithm]] for integer factoring. In itself it is not more efficient than classical [[discrete Fourier transform]], but what these algorithms make use of is the efficient "*phase estimation*" that is a side-effect of the QFT.

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



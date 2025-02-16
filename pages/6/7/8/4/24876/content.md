
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
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

In [[quantum information theory]] and [[quantum computing]], by a *qdit* (or *qudit*) one means a [[quantum state]] in a $d$-[[dimension of a vector space|dimensional]] [[Hilbert space]], for any [[natural number]] $d$.

Hence for fixed $d\in \mathbb{N}$, the quantum [[data type]] of qdits is the $d$-[[dimension of a vector space|dimensional]] [[complex vector space]] equipped with a [[quantum measurement]]-[[linear basis|basis]] 

$$
  \mathbb{C}^d
  \;\simeq\;
  \underset{n \in \{1, \cdots, d\}}{\bigoplus} \mathbb{C} \cdot \vert n \rangle
  \,.
$$


* For $d = 2$ one speaks of *[[qbits]]*, this is the original terminology;

* For $d = 3$ one also speaks of *qtrits*.

## Examples

### Anyon states
 {#AnyonStates}

A key example of [[quantum gates]] which naturally act on qdits for $d \gt 2$ are [[anyon]] [[braid representation|braid]]-gates in [[topological quantum computation]]: 

For the potentially realistic case of [[Chern-Simons theory]]/[[WZW-model]]-controled [[anyons]] (such as [[su(2)-anyons]]), the elementary [[quantum logic gates]] act by the [[monodromy]] of the [[Knizhnik-Zamolodchikov connection]] on [[Hilbert spaces]] of [[conformal blocks]], whose [[dimension of a vector space|dimension]] $d$ is given by a [[Verlinde formula]].

References which make this point explicit include [Kolganov, Mironov & Morozov (2023)](#KolganovMironovMorozov23).

## Related concepts

* [[data type]]

* [[qbit]]

* [[quantum gate]], [[quantum circuit]]

## References
 {#References}

General:

* IEEE Spectrum *[Qudits: The Real Future of Quantum Computing?](https://spectrum.ieee.org/qudits-the-real-future-of-quantum-computing)* (June 2017)

* Yuchen Wang, Zixuan Hu, Barry C. Sanders, Sabre Kais, section 3.2.1 of: *Qudits and high-dimensional quantum computing*, Front. Phys. **8** 479 (2020) &lbrack;[arXiv:2008.00959](https://arxiv.org/abs/2008.00959), [doi:10.3389/fphy.2020.589504](https://doi.org/10.3389/fphy.2020.589504)&rbrack;


See also: 

* Wikipedia, *[Qutrit](https://en.wikipedia.org/wiki/Qutrit)*

On the [[quantum Fourier transform]] with qdits:

* Ashok Muthukrishnan, C. R. Stroud Jr: *Quantum fast Fourier transform using multilevel atoms*, Journal of Modern Optics **49** 13 (2002) &lbrack;[arXiv:quant-ph/0112017](https://arxiv.org/abs/quant-ph/0112017), [doi:10.1080/09500340210123947](https://doi.org/10.1080/09500340210123947)&rbrack;

* Zeljko Zilic, Katarzyna Radecka: *Scaling and better approximating quantum Fourier transform by higher radices*, IEEE Transactions on Computers **56** 2 (2007) 202-207 &lbrack;[arXiv:quant-ph/0702195](https://arxiv.org/abs/quant-ph/0702195), [doi:10.1109/TC.2007.35](https://doi.org/10.1109/TC.2007.35)&rbrack;

* Cao Ye et al.: *Quantum Fourier Transform and Phase Estimation in Qudit System*, Commun. Theor. Phys. **55** 790 (2011) &lbrack;[doi:10.1088/0253-6102/55/5/11](https://iopscience.iop.org/article/10.1088/0253-6102/55/5/11)&rbrack;





Explicit mentioning of the qdit-nature of the elementary gates in [[topological quantum computation]]:

* {#KolganovMironovMorozov23}  [[Nikita Kolganov]], [[Sergey Mironov]], [[Andrey Morozov]], *Large $k$ topological quantum computer*, Nuclear Physics B
**987** (2023) 116072 &lbrack;[arXiv:2105.03980](https://arxiv.org/abs/2105.03980), [doi:10.1016/j.nuclphysb.2023.116072](https://doi.org/10.1016/j.nuclphysb.2023.116072)&rbrack;



[[!redirects qudits]]

[[!redirects qdit]]
[[!redirects qdits]]


[[!redirects qtrit]]
[[!redirects qtrits]]

[[!redirects qutrit]]
[[!redirects qutrits]]



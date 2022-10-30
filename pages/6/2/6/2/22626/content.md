
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In the context of [[quantum computation]], a *quantum circuit diagram* (originally: "quantum computational network", [Deutsch 1989](#Deutsch89)) is a kind of [[string diagram]] ([Abramsky & Coecke 2004](#AbramskyCoecke04)) in [[finite-dimensional vector spaces|finite-dimensional]] [[Hilbert spaces]], typically used to express a sequence of low-level [[quantum logic gate|quantum gates]] mapping between [[space of quantum states|spaces of]] [[pure quantum state|pure]] [[quantum states]].

A generic quantum circuit might look as follows:

\begin{imagefromfile}
    "file_name": "QuantumCircuitScheme-221025c.jpg",
    "width": "600",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 10,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

Here, for instance, the "[[quantum gate]]" $U_{34}$ is a [[linear operator]] on the [[tensor product]] [[Hilbert space]] $\mathscr{H} \oplus \mathscr{H}$.

Notice that the quantum circuit is understood to be the actual [[string diagram]], up to the usual admissible topological deformations, not just the [[composition|composite]] [[linear transformation]] which it encodes: The compositeness of the diagram encodes how (e.g. in which order) available [[quantum gate]]-operations would be operated on an actual [[quantum computer]], and the composite linear map only encodes the inpute-to-output-specification of the resulting [[quantum computation]]. In this sense, quantum circuits constitute a [[quantum programming language]] and one also speaks of the "quantum circuit model of quantum computation" (e.g. [Nielsen & Chuang 2000, §II.4.6](#NielsenChuang00); [Miszczak 2011, §3](#Miszczak11), [2012, §4.3](#Miszczak12); [Beneti & Casati 2018, §3.2](#BenetiCasati18)).


Often the basic Hilbert space building block here is taken to be [[complex vector space|complex]] 2-[[dimension of a vector space|dimensional]], $\mathscr{H} \,\coloneqq\, \mathbb{C}^2$, in which case one speaks of a quantum circuit on *[[q-bits]]*.

Sometimes all [[quantum gates]] involved, and hence also the resulting [[composition|composite]] [[linear maps]], are assumed to be [[invertible]], as befits [[reversible computation]] by [[unitary operator|unitary]] quantum state evolution in [[quantum mechanics]].

But more generally and certainly in the broader context of [[quantum information theory]] (such as in formulating the [[quantum teleportation protocol]] and similar), quantum circuits are admitted to also contain:

1. *[[quantum measurement]]-gates*,  

1. *[[quantum state preparation]]-gates*,

1. *classically controlled quantum gates*.

Here [[quantum measurement]], in particular, is not only non-[[reversible computation|reversible]] (due to the [[quantum state collapse]] involved) but also non-deterministic, meaning that it is not immediately represented by a fixed linear map at all -- at least not between the original Hilbert spaces. 

One may model the $B$-[[tuple]] of [[projection operators]] corresponding to the possible set $B$ of measurement outcomes as a [[linear map]] between the original [[Hilbert space]] $\mathscr{H}$ and its $B$-[[indexed set|indexed]] [[direct sum]] (one rare place where this is made explicit, albeit without comment, is [Selinger 2004](#Selinger04), [p. 39](https://www.mathstat.dal.ca/~selinger/papers/qpl.pdf#page=39)):

$$
  \array{
    meas 
    &
      \colon
    &
    \mathcal{H}
    &
      \xrightarrow{\phantom{--}}
    &
    \underset{
      b \colon B
    }{\oplus}
    \mathcal{H}
    \\
    &&
    \vert \psi \rangle
    &\mapsto&
    \underset{b \colon B}{\oplus}
    \,
    P_{b} \vert \psi \rangle 
  }
  \,.
$$


Therefore, as soon as these three operations crossing the [[classical physics|classical]]/[[quantum physics]]-boundary are involved (and made explicit), quantum circuits are no longer just [[string diagrams]] in [[finite-dimensional vector space|finite-dimensional]] [[HilbertSpaces]], but something richer, involving bsides [[tensor products]] also some kind of reflection of [[direct sums]] of [[spaces of quantum states]].

One approach for handling these more general quantum circuits is ([Aharonov, Kitaev & Nisan 1998](#AharonovKitaevNisan98), [Selinger 2004](#Selinger04)) to understand them, in the tradition on [[quantum probability theory]], as diagrams of "[[quantum operations]]" on [[space of quantum states|spaces of]] [[mixed quantum states]], namely as a kind of [[string diagrams]] of [[completely positive maps]] between [[convex spaces]] of [[density matrices]].

Other approaches for giving [[categorical semantics]] for quantum circuits in this general sense have been proposed (and implemented) in the discussion of the [[quantum programming language]] *[[Quipper]]* (see the references [there](Quipper#ReferencesDependentLinearTypesAndCategoricalSemantics)). A natural formulation in terms of [Quantum Modal Logic](necessity+and+possibility#ModalQuantumLogic) in terms of [[dependent linear type theory]] is discussed at:

* *[[quantum circuits via dependent linear types]]*.

These turn out to be related: From a suitably rich formulation of quantum circuits of pure states with measurement and classical control, the [[density matrix]]-formulation may be recovered (...).

 
At the time of writing (2021) most of the actual programming of [[experiment|experimental]] [[quantum computers]] is conceived through quantum circuit diagrams, while more high-level [[quantum programming languages]] are are awaiting the rise of more powerful quantum hardware.

## Examples
 {#Examples}

### Bell state preparation

In [[qbit]]-based [[quantum computation]], the elementary [[Bell state]] is usually prepared via the following small quantum circuit consisting of a [[Hadamard gate]] followed by a [[quantum CNOT gate]]:

\begin{imagefromfile}
    "file_name": "BellStatePreparationCircuit-221026.jpg",
    "width": "680",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


## Related concepts

* [[quantum computation]], [[quantum error correction]]

* [[string diagram]], [[proof net]]

* [[DisCoPy]]


## References

### Quantum circuit diagrams

The notion of [[quantum gates]] and quantum circuits acting on [[pure quantum states]] originates with:

* {#Deutsch89} [[David E. Deutsch]], *Quantum computational networks*, Proceedings of the Royal Society A, **425** 1868 (1989) 73-90 &lbrack;[doi:10.1098/rspa.1989.0099](https://doi.org/10.1098/rspa.1989.0099), [jstor:2398494](https://www.jstor.org/stable/2398494)&rbrack;

On quantum circuits for [[mixed quantum states]] (with [[density matrices]]):

* {#AharonovKitaevNisan98} [[Dorit Aharonov]], [[Alexei Kitaev]], [[Noam Nisan]], *Quantum Circuits with Mixed States*, *Proceedings of the Thirtieth Annual ACM Symposium on Theory of Computation (STOC)* (1998) 20-30 &lbrack;[arXiv:quant-ph/9806029](https://arxiv.org/abs/quant-ph/9806029), [doi:10.1145/276698.276708](https://doi.org/10.1145/276698.276708)&rbrack;

* {#Selinger04} [[Peter Selinger]], _Towards a quantum programming language_, Mathematical Structures in Computer Science **14** 4 (2004) 527–586 &lbrack;[doi:10.1017/S0960129504004256](https://doi.org/10.1017/S0960129504004256), [pdf](https://www.mathstat.dal.ca/~selinger/papers/qpl.pdf),  [web](https://www.mathstat.dal.ca/~selinger/papers.html#qpl)&rbrack;


Standard textbook accounts:

* {#NielsenChuang00} [[Michael A. Nielsen]], [[Isaac L. Chuang]], Section II.4 in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

*  {#Miszczak11} [[Jarosław Adam Miszczak]], Sec. 3 of: *Models of quantum computation and quantum programming languages*, Bull. Pol. Acad. Sci.-Tech. Sci., **59** 3 (2011)305-324 &lbrack;[arXiv:1012.6035](https://arxiv.org/abs/1012.6035), [doi:10.2478/v10175-011-0039-5](https://doi.org/10.2478/v10175-011-0039-5)&rbrack;

* {#Miszczak12} [[Jarosław Adam Miszczak]], Section 4.3 in: *High-level Structures for Quantum Computing*, Morgan&Claypool (2012) &lbrack;[doi:10.2200/S00422ED1V01Y201205QMC006](https://doi.org/10.2200/S00422ED1V01Y201205QMC006), [pdf](https://www.morganclaypool.com/doi/pdf/10.2200/S00422ED1V01Y201205QMC006)&rbrack;

* *Quantum Circuit Model of Computation*, 2015 ([pdf](https://ipgold.epfl.ch/_media/en/courses/2015-2016/calculquant/chapter3corrected.pdf))

* {#BenetiCasati18} [[Giuliano Benenti]], [[Giulio Casati]], [[Davide Rossini]], Chapter 3 of: *Principles of Quantum Computation and Information*, World Scientific 2018  ([doi:10.1142/10909](https://doi.org/10.1142/10909), [2004 pdf](http://mmrc.amss.cas.cn/tlb/201702/W020170224608149307696.pdf))

Standard lecture notes:

* [[John Preskill]], *Classical and quantum circuits* ([pdf](http://theory.caltech.edu/~preskill/ph219/chap5_13.pdf)), Chapter 5 in: *Quantum Computation*, lecture notes ([web](http://theory.caltech.edu/~preskill/ph229/))

* Ryan O’Donnell, *Introduction to the Quantum Circuit Model* (2015) ([pdf](https://www.cs.cmu.edu/~odonnell/quantum15/lecture01.pdf))

* [[Scott Aaronson]], §4.2 in: *Introduction to Quantum Information Science* (2018) &lbrack;[pdf](https://www.scottaaronson.com/qclec.pdf), [webpage](https://www.scottaaronson.com/cs378/)&rbrack;


The ([[dagger-compact category|dagger-compact]] [[monoidal category|monoidal]])  [[category|category theoretic]] formulation is due to:

* {#AbramskyCoecke04} [[Samson Abramsky]], [[Bob Coecke]], *A categorical semantics of quantum protocols*, Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04). IEEE Computer Science Press (2004) &lbrack;[arXiv:quant-ph/0402130](https://arxiv.org/abs/quant-ph/0402130), [doi:10.1109/LICS.2004.1319636](https://doi.org/10.1109/LICS.2004.1319636)&rbrack;

with exposition and further development in:

* {#Coecke05} [[Bob Coecke]], *Kindergarten Quantum Mechanics*, in *Quantum Theory: Reconsideration of Foundations* (QTRF 3) Vaxjo, Sweden, June 6-11, 2005, AIP Conf. Proc. **810** (2006) &lbrack;[arXiv:quant-ph/0510032](https://arxiv.org/abs/quant-ph/0510032), [doi:10.1063/1.2158713](https://doi.org/10.1063/1.2158713)&rbrack;

* {#Coecke10} [[Bob Coecke]], *Quantum Picturalism*, Contemporary Physics **51** (2010) 59-83 &lbrack;[arXiv:0908.1787](https://arxiv.org/abs/0908.1787), [doi:10.1080/00107510903257624](https://doi.org/10.1080/00107510903257624)&rbrack;

For more on this see at *[[finite quantum mechanics in terms of dagger-compact categories]]*.

See also:

* Wikipedia, _[Quantum circuit](http://en.wikipedia.org/wiki/Quantum_circuit)_

* Stephen P. Jordan, Sec. 1.2 in: *Quantum Computation Beyond the Circuit Model* ([arXiv:0809.2307](https://arxiv.org/abs/0809.2307))

Survey, examples, and implementations:

* Michal Charemza, *Examples of Quantum Circuit Diagrams*, 2006 ([pdf](https://warwick.ac.uk/fac/sci/physics/research/cfsa/people/pastmembers/charemzam/pastprojects/mcharemza_quant_circ.pdf))

* Qiskit, *[Defining Quantum Circuits](https://qiskit.org/textbook/ch-algorithms/defining-quantum-circuits.html)*

* {#SKQHackathon20} [South Korea Qiskit Hackathon'20 - Qiskit Metal exercise](https://qiskit.org/documentation/metal/circuit-examples/full-design-flow-examples/Exercise-for-the-South-Korea-Hackathon'20.html)

  > (tutorial for a 2-[[qbit]] quantum chip using Qiskit)

* Microsof Build, *[Quantum circuit diagrams](https://docs.microsoft.com/en-us/azure/quantum/concepts-circuits)*

* Vladimir P. Gerdt, Alexander N. Prokopenya, *The Circuit Model of Quantum Computation and Its Simulation with Mathematica*, In: Adam G., Buša J., Hnatič M. (eds.) *Mathematical Modeling and Computational Science* MMCP 2011. Lecture Notes in Computer Science, vol 7125. Springer 2011 ([doi:10.1007/978-3-642-28212-6_4](https://doi.org/10.1007/978-3-642-28212-6_4))


With an eye towards [[quantum complexity theory]]:

* Richard Cleve, Section 1.2 in: *An Introduction to Quantum Complexity Theory* ([pdf](https://cds.cern.ch/record/392006/files/9906111.pdf))

[[!include quantum programming languages -- references]]


[[!redirects quantum circuit diagrams]]

[[!redirects quantum circuit]]
[[!redirects quantum circuits]]


[[!redirects quantum circuit model]]
[[!redirects quantum circuit models]]

[[!redirects quantum protocol]]
[[!redirects quantum protocols]]





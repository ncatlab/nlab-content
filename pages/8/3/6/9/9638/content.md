
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

### General
 {#IdeaGeneral}

_Quantum computation_ is [[computation]] in terms of [[quantum information theory]], possibly implemented on _quantum computers_, hence on [[physical systems]] for which phenomena of [[quantum mechanics]] are not negligible: [[quantum systems]] such as consisting of [[fundamental particles]] like [[photons]] or [[electrons]] but also often of quantum-[[quasiparticles]] such as [[Cooper pairs]] in [[superconductors]]. 

In terms of the [[computational trilogy]], quantum computation is the computation corresponding to (some kind of) [[quantum logic]]/([[dependent linear type theory|dependent]]) [[linear type theory]].

To the extent that quantum computation involves [[quantum measurement]] (generally to read out results, but often also as a kind of [[quantum logic gate]] in its own right) it is a form of [[nondeterministic computation]], due to the intrinsic [[probability theory|stochastic]] nature of the [[quantum state collapse]] during [[quantum measurement]].

However, away from [[quantum measurement]], [[quantum gates]] are understood to implement [[unitary operators]] on a given [[Hilbert space]] [[space of quantum states|of quantum states]] (fundamentally due to the unitary nature of time-evolution as given by the [[Schrödinger equation]]), for which quantum computation is hence not only deterministic but in fact a form of *[[reversible computation]]*. This relates to its susceptibility to noise and the practical need for [[quantum error correction]] and/or [[topological quantum computation|topological quantum stabilization]].

Specifically, _[[topological quantum computation]]_ is (or is meant to be) quantum computation implemented on [[physical systems]] governed by [[topological quantum field theory]], such as [[Chern-Simons theory]], thought to describe for instance [[anyon]] [[defects]] in [[topological order|topologically ordered]] [[mass gap|gapped]] [[ground states]] of [[quantum materials]] in [[topological phases of matter]].


### Classical control, quantum data
 {#ClassicalControlQuantumData}

Any practical quantum computer will be *[[classically controlled quantum computation|classically controlled]]* (an idea that may be traced back to [Knill 96](#Knill96), [Ömer 03](#Omer03), for more pronounced discussion see [Devitt 14](#Devitt14)).

\begin{imagefromfile}
    "file_name": "ClassicallyControlledQuantumComputation.jpg",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from  [Miszczak 11, Fig. 9](#Miszczak11))"
\end{imagefromfile}

Already for presently available [NISQ](#ReferencesNISQ) machines, classically-[[parameterized quantum systems]] have been considered in contexts such as [[quantum machine learning]] &lbrack;[BLSF 19](#BenedettiLloydSackFiorentini19)&rbrack;:

\begin{imagefromfile}
    "file_name": "HybridQuantumComputing.jpg",
    "width": 350,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [BLSF 19, Fig. 1](#BenedettiLloydSackFiorentini19))"
\end{imagefromfile}

{#DynamicLifting} Here the classical control itself is generally conditioned on [[quantum measurement]]-outcomes --- notably syndrome-measurements for [[quantum error correction]] --- available only during runtime, a mechanism that in the [[quantum programming languages]]-community ([[Quipper]]) has come to be called "[[dynamic lifting]]":

\begin{imagefromfile}
    "file_name": "SQRAMschema-WithDynLifting.jpg",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": -10,
        "right": 0, 
        "left": 10
    },
    "caption": "(SQRAM model adapted from [Nagarajan, Papanikolaou and Williams 2007, Fig 1](#NagarajanPapanikolaouWilliams07))"
\end{imagefromfile}

{#NeedForClassicalControl} $\,$

&lbrack;[Devitt 14](#Devitt14), [p. 2](https://arxiv.org/pdf/1405.4943#page=2):&rbrack;

> Irrespective of the actual quantum code chosen to protect a quantum computer, it is well known that operating such as system requires extensive classical control infrastructure. This is not simply related to the control of the physical device hardware needed to operate a qubit (lasers, signal generators etc...), but it is also required to decode [[quantum error correction|error correction]] information produced by the computer. 

&lbrack;[KESWDSC 23](#KESWDSC23), [p. 2](https://arxiv.org/pdf/2311.07121#page=2):&rbrack;

> Apart from the requirements on the quantum hardware, the successful execution of [[quantum error correction|QEC codes]] depends on the classical control system. The classical control system is responsible for all classical aspects of quantum computing and includes executing the quantum control and
measurement signals, acquiring the readout signals, andperforming classical processing operations, all in a synchronized manner. In QEC, the control system is also responsible for mapping the local physical measurements into logical measurement results or logical Pauli frame updates through an algorithmic procedure called decoding. To reach
useful quantum computation with QEC, i.e., perform faultolerant non-Clifford gates, the control unit is required to perform quantum gates that depend on the decoding output. Moreover, to prevent a diverging classical calculation latency, it is crucial for the control system to close a tight loop, with ultra-low latency, from the physical quantum measurement through the classical decoding procedure to a conditional feed-forward quantum operation. Thus, the success of fault-tolerant quantum computation depends on minimizing the QEC feed-forward latency. 

\begin{imagefromfile}
    "file_name": "CRKAW-QECCP.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(QECCP schematics fom [KESWDSC 23, Fig. 2](#KESWDSC23))"
\end{imagefromfile}


For more on technical details of classical control requirements see also [CRKAW 24](#CRKAW24).

Generally, see the list of references [below](#ReferencesClassicallyControlledQuantumComputing).




### Quantum languages and quantum circuits

A natural way to understand (via [[computational trilogism]]) [[quantum programming languages]] is as  [[linear logic]]/[[linear type theory]] ([Pratt 92](#Pratt92), for more see at *[[quantum logic]]*) with [[categorical semantics]] in non-[[Cartesian monoidal category|cartesian]] [[symmetric monoidal categories]] ([Abramsky & Coecke 04](#AbramskyCoecke04), [Abramsky & Duncan 05](#AbramskyDuncan05), [Duncan 06](#Duncan06), [Lago-Faffian 12](#LagoFaffian12)).  .

The corresponding [[string diagrams]] are known as *[[quantum circuit diagrams]]*.

In fact, languages for [classically controlled quantum computation](#ClassicalControlQuantumData)  should be based on [[dependent linear type theory]] ([Vakar 14](dependent+linear+type+theory#Vakar14), [Vakar 15](dependent+linear+type+theory#Vakar15), [Vakar 17, Sec. 3](dependent+linear+type+theory#Vakar17), [Lundfall 17](dependent+linear+type+theory#Lundfall17), [Lundfall 18](dependent+linear+type+theory#Lundfall18), following [Schreiber 14](dependent+linear+type+theory#Schreiber14)) with [[categorical semantics]] in [[indexed monoidal categories]]:

| classical control | quantum data | 
|-------------------|--------------|
| [[intuitionistic type theory|intuitionistic types]] | [[dependent linear type theory|dependent linear types]]

This idea of classically controlled quantum programming via [[dependent linear type theory]] has been implemented in [[QML]] and in *[[Quipper]]* in [FKS 20](#FKS20), [FKRS 20](#FKRS20).

## Examples

* [[QML]]

* [[Quipper]]


## Related entries

* [[quantum algorithm]]

* [[quantum simulation]]

* [[quantum sensing]]

* [[quantum parallelism]], [[parallel computing]]

* [[Bloch region]], [[quantum operation]]

* [[Grover's algorithm]], [[Shor's algorithm]]

* [[Solovay-Kitaev theorem]]

* [[quantum information theory]]

* [[quantum communication]]

* [[quantum sensing]]

* [[qbit]], [[qtrit]], [[qdit]]

* [[quantum logic gate]], [[quantum circuit]]

* [[quantum error correction]]

* [[quantum logic]], [[linear logic]]

* [[adiabatic quantum computation]]

* [[topological quantum computation]]

* [[measurement-based quantum computation]]

* [[trapped-ion quantum computing]]

* [[quantum Hall effect]], [[Chern-Simons theory]].

* [[superoperator]]

* [[computable physics]]

* [[quantum probability]]



## References

### General

The idea of quantum computation was first expressed in:

* {#Manin1980} [[Yuri I. Manin]], Introduction to: *Computable and Uncomputable*, Sov. Radio (1980) &lbrack;Russian original: [[Manin-1980.pdf:file]]&rbrack;, Enlish translation on p. 69-77 of *Mathematics as Metaphor: Selected essays of Yuri I. Manin*, Collected Works **20**, AMS (2007) &lbrack;[ISBN:978-0-8218-4331-4](https://bookstore.ams.org/cworks-20/)&rbrack;

  > Perhaps, for a better understanding of &lbrack;molecular biology&rbrack;, we need a mathematical theory of quantum automata.

* [[Paul Benioff]], *The computer as a physical system: A microscopic quantum mechanical Hamiltonian model of computers as represented by Turing machines*, J Stat Phys 22, 563–591 (1980) &lbrack;[doi:10.1007/BF01011339](https://doi.org/10.1007/BF01011339)&rbrack;

* [[Paul Benioff]], *Quantum Mechanical Models of Turing Machines That Dissipate No Energy*, Phys. Rev. Lett. **48** 1581  (1982) &lbrack;[doi:10.1103/PhysRevLett.48.1581](https://doi.org/10.1103/PhysRevLett.48.1581)&rbrack;

* {#Feynman82} [[Richard Feynman]], *Simulating physics with computers*,  Int J Theor Phys **21** (1982) 467–488 &lbrack;[doi:10.1007/BF02650179](https://doi.org/10.1007/BF02650179)&rbrack;

  > "because nature isn't classical, dammit, if you want to make a simulation of nature, you'd better make it quantum mechanical"

First ideas of a [[quantum Turing machine]]:

* David Z. Albert, *On quantum-mechanical automata*, Physics Letters A **98** 5–6 (1983) 249-252 &lbrack;<a href="https://doi.org/10.1016/0375-9601(83)90863-0">doi:10.1016/0375-9601(83)90863-0</a>&rbrack;

* [[David Deutsch]], *Quantum theory, the Church–Turing principle and the universal quantum computer*, Proceedings of the Royal Society of London A **400** 1818 (1985) 97-117 &lbrack;[doi:10.1098/rspa.1985.0070](https://doi.org/10.1098/rspa.1985.0070), [pdf](https://www.daviddeutsch.org.uk/wp-content/deutsch85.pdf)&rbrack;


The notion of ([[controlled quantum gate|controlled]]) [[quantum logic gates]] and [[quantum circuits]] was first made explicit in:

* [[Richard Feynman]], *Quantum mechanical computers*, Foundations of Physics **16** (1986) 507–531 &lbrack;[doi:10.1007/BF01886518](https://doi.org/10.1007/BF01886518)&rbrack;

* [[David E. Deutsch]], *Quantum computational networks*, Proceedings of the Royal Society A, **425** 1868 (1989) 73-90 &lbrack;[doi:10.1098/rspa.1989.0099](https://doi.org/10.1098/rspa.1989.0099), [jstor:2398494](https://www.jstor.org/stable/2398494)&rbrack;

The terminology *[[q-bit]]* goes back to:

* [[Benjamin Schumacher]], *Quantum coding*, Phys. Rev. A **51** (1995) 2738 &lbrack;[doi:10.1103/PhysRevA.51.2738](https://doi.org/10.1103/PhysRevA.51.2738)&rbrack;


The potential practical relevance of quantum computation was highlighted early on via toy examples

such as the [[Deutsch-Jozsa algorithm]]:

* [[David Deutsch]], [[Richard Jozsa]], *Rapid solution of problems by quantum computation*. Proc. R. Soc. Lond. A **439** 1907 (1992) 553-558 &lbrack;[pdf](https://www.isical.ac.in/~rcbose/internship/lectures2016/rt08deutschjozsa.pdf), [doi:10.1098/rspa.1992.0167](https://doi.org/10.1098/rspa.1992.0167)&rbrack;

and became widely appreciated in 1996/1997 with the discovery of several practically interesting [[algorithms]] exhibiting "[[quantum supremacy]]", such as:

in [[quantum chemistry]]

* [[Seth Lloyd]], *Universal Quantum Simulators*, Science New Series **273** 5278 (1996) 1073-1078 &lbrack;[jstor:2899535](https://www.jstor.org/stable/2899535), [doi:10.1126/science.273.5278.1073](https://doi.org/10.1126/science.273.5278.1073)&rbrack;

in search algorithms ([[Grover's algorithm]])

* [[Lov K. Grover]], *A fast quantum mechanical algorithm for database search*, STOC '96: Proceedings of the twenty-eighth annual ACM symposium on Theory of Computing (1996) 212-219 &lbrack;[arXiv:quant-ph/9605043](https://arxiv.org/abs/quant-ph/9605043), [doi:10.1145/237814.237866](https://doi.org/10.1145/237814.237866)&rbrack;


and in ([[quantum cryptography|quantum]]) [[cryptography]] ([[Shor's algorithm]])

* [[Daniel R. Simon]], *On the power of quantum computation*, SIAM Journal on Computing **26** 5 (1997) &lbrack;[doi:10.1137/S0097539796298637](https://doi.org/10.1137/S0097539796298637), [pdf](https://courses.cs.washington.edu/courses/cse599/01wi/papers/simon_qc.pdf)&rbrack;

* [[Peter W. Shor]], *Algorithms for quantum computation: discrete logarithms and factoring*,  Proceedings 35th Annual Symposium on Foundations of Computer Science, IEEE Comput. Soc. Press: 124-134 (1994) &lbrack;[doi:10.1109/SFCS.1994.365700](https://doi.org/10.1109/SFCS.1994.365700)&rbrack;

The first realistic proposal for actually building a [[quantum gate]] (namely on [[trapped-ion quantum computing|trapped ions]]):

* {#CiracZoller95} [[J. Ignacio Cirac]], [[Peter Zoller]]: *Quantum Computations with Cold Trapped Ions*, Phys. Rev. Lett. **74** (1995) 4091 &lbrack;[doi:10.1103/PhysRevLett.74.4091](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.74.4091)&rbrack;

Quantum computation became widely thought to be not just a theoretical but a plausible practical possibility with the theoretical understanding of [[quantum error correction]] (which however remains to be implemented scalably):

* {#Shor95} [[Peter W. Shor]], *Scheme for reducing decoherence in quantum computer memory*, Phys. Rev. A 52, R2493(R) 1995 ([doi:10.1103/PhysRevA.52.R2493](https://doi.org/10.1103/PhysRevA.52.R2493))

* {#Steane96} [[Andrew M. Steane]], *Error Correcting Codes in Quantum Theory*, Phys. Rev. Lett. 77, 793 1996 ([doi:10.1103/PhysRevLett.77.793](https://doi.org/10.1103/PhysRevLett.77.793))

* {#CalderbankShor96} [[Robert Calderbank]], [[Peter W. Shor]], *Good Quantum Error-Correcting Codes Exist*, Phys. Rev. A, Vol. 54, No. 2, pp. 1098-1106, 1996 ([doi:10.1103/PhysRevA.54.1098](https://doi.org/10.1103/PhysRevA.54.1098))

Early review:

* [[Adriano Barenco]], *Quantum Physics and Computers*,  Contemp. Phys. **37** (1996) 375-389 &lbrack;[arXiv:quant-ph/9612014](https://arxiv.org/abs/quant-ph/9612014), [doi:10.1080/00107519608217543](https://doi.org/10.1080/00107519608217543)&rbrack;

* [[Yuri I. Manin]], *Classical computing, quantum computing, and Shor's factoring algorithm*, Astérisque, **266** Séminaire Bourbaki 862 (2000) 375-404 &lbrack;[arXiv:quant-ph/9903008](https://arxiv.org/abs/quant-ph/9903008), [numdam:SB_1998-1999__41__375_0](http://www.numdam.org/item/?id=SB_1998-1999__41__375_0)&rbrack;

Monograph on experimental realizations of [[quantum gates]]/[[quantum computers]]:

* {#CCEHRSZ07} Chen, Church, Englert, Henkel, Rohwedder, Scully, Zubairy:  *Quantum Computing Devices -- Principles, Designs, and Analysis*, Routledge (2007) &lbrack;[ISBN:9780367390372](https://www.routledge.com/Quantum-Computing-Devices-Principles-Designs-and-Analysis/Chen-Church-Englert-Henkel-Rohwedder-Scully-Zubairy/p/book/9780367390372?srsltid=AfmBOooGiSmyK4mzxjmR1LBJz4zU9cgCpp_z4cPiCzEhM6SJo4b2GxRp)&rbrack;

Review of [[quantum algorithms]]:

* Ashley Montanaro, *Quantum algorithms: an overview*, npj Quantum Information **2** 15023 (2016) &lbrack;[doi:10.1038/npjqi.2015.23](https://doi.org/10.1038/npjqi.2015.23)&rbrack;

* Renato Portugal: *Basic Quantum Algorithms* &lbrack;[arXiv:2201.10574](https://arxiv.org/abs/2201.10574)&rbrack;

* Kamil Khadiev: *Lecture Notes on Quantum Algorithms* &lbrack;[arXiv:2212.14205](https://arxiv.org/abs/2212.14205)&rbrack;

* [[Alessandro Luongo]]: *[Quantum algorithms for data analysis](https://quantumalgorithms.org)*


An alternative/parallel approach to avoiding errors due to [[decoherence]] is [[topological quantum computation]], see [there](topological+quantum+computation#References) for references.

Influential list of criteria necessary for physical realization of quantum computation:

* {#DiVincenzo00} [[David P. DiVincenzo]], *The Physical Implementation of Quantum Computation*, Fortschr. Phys. **48** 9-11 (2000) 771-783 &lbrack;[arXiv:quant-ph/0002077](https://arxiv.org/abs/quant-ph/0002077), <a href="https://doi.org/10.1002/1521-3978(200009)48:9/11%3C771::AID-PROP771%3E3.0.CO;2-E">doi:10.1002/1521-3978(200009)48:9/11%3C771::AID-PROP771%3E3.0.CO;2-E</a>&rbrack;

Simple quantum computers have been realized (first with [[NMR]] technology, see [references below](#SpinResonanceQBitsReferences), then with [[superconductor]] technology, see [references further below](#SuperconductingQBitsReferences)) and have been argued to demonstrate *[[quantum supremacy]]* (see [there](quantum+supremacy#References) for references) but existing machines remain "noisy and intermediate scale" (see the references [below](#ReferencesNISQ)).

Textbook accounts on quantum computation:

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

* [[Samuel J. Lomonaco]] (ed.), *Quantum Computation: A Grand Mathematical Challenge for the Twenty-First Century and the Millennium*, Proceedings of Symposia in Applied Mathematics **58**, AMS (2002) &lbrack;[doi:10.1090/psapm/058](https://doi.org/10.1090/psapm/058)&rbrack;

* [[Alexei Y. Kitaev]], A. H. Shen, M. N. Vyalyi, *Classical and Quantum Computation*, Graduate Studies in Mathematics **47** (2002) &lbrack;[doi:10.1090/gsm/047](http://dx.doi.org/10.1090/gsm/047)&rbrack;

* [[Ranee K. Brylinski]], [[Goong Chen]] (eds.), *Mathematics of Quantum Computation*, Chapman and Hall/CRC 2002 ([doi:10.1201/9781420035377](https://doi.org/10.1201/9781420035377))

* [[Giuliano Benenti]], [[Giulio Casati]], [[Davide Rossini]], *Principles of Quantum Computation and Information*, World Scientific (2004, 2018)  ([doi:10.1142/10909](https://doi.org/10.1142/10909), [2004 pdf](http://mmrc.amss.cas.cn/tlb/201702/W020170224608149307696.pdf))

* [[Goong Chen]], [[Louis Kauffman]], [[Samuel J. Lomonaco]] (eds.), *Mathematics of Quantum Computation and Quantum Technology*, Chapman and Hall/CRC (2007) (ISBN:9780367388614, [doi:10.1201/9781584889007](https://doi.org/10.1201/9781584889007))

* [[Eleanor Rieffel]], [[Wolfgang Polak]], *Quantum Computing -- A gentle introduction*, MIT Press (2011) &lbrack;[ISBN:9780262526678](https://mitpress.mit.edu/9780262526678/quantum-computing/), [pdf](http://mmrc.amss.cas.cn/tlb/201702/W020170224608150244118.pdf)&rbrack;

* [[Dirk Bouwmeester]], [[Artur Ekert]], [[Anton Zeilinger]] (eds.), *The Physics of Quantum Information -- Quantum Cryptography, Quantum Teleportation, Quantum Computation*, Springer (2020) &lbrack;[doi:10.1007/978-3-662-04209-0](https://doi.org/10.1007/978-3-662-04209-0)&rbrack;

* [[Steven Duplij]], [[Raimund Vogl]], *Innovative Quantum Computing*, IOP (2023) &lbrack;[ISBN:978-0-7503-5281-9](https://iopscience.iop.org/book/mono/978-0-7503-5281-9)&rbrack; 

* Thomas Wong: *Intoduction to Classical and Quantum Computing* (2024) &lbrack;[pdf](https://thomaswong.net/introduction-to-classical-and-quantum-computing-1e4p.pdf), [webpage](https://thomaswong.net/)&rbrack;

Introducing the notion of [[quantum supremacy]] and highlighting its relation to [[quantum entanglement]]:

* [[John Preskill]]: *Quantum computing and the entanglement frontier*: pp. 63-80 in: *The Theory of the Quantum World -- Proceedings of the 25th Solvay Conference on Physics*, World Scientific (2013) &lbrack;[arXiv:1203.5813](https://arxiv.org/abs/1203.5813), [doi:10.1142/8674](https://doi.org/10.1142/8674), slides: [pdf](https://simons.berkeley.edu/sites/default/files/docs/394/preskilljohn.pdf)&rbrack;

   
Further introduction and survey:

* [[Alexei Kitaev]],  *Quantum computations: algorithms and error correction*, Russian Mathematical Surveys, **52** 6 (1997) &lbrack;[doi:10.1070/RM1997v052n06ABEH002155](https://iopscience.iop.org/article/10.1070/RM1997v052n06ABEH002155), <a href="https://ochicken.top/Library/Physics/Quantum_Computation_and_Quantum_Information/1997.06%20A.Yu.Kitaev_%20Quantum%20computations_%20algorithms%20and%20error%20correction%20(kitaev1997).pdf">pdf</a>&rbrack;


* [[Eleanor Rieffel]], [[Wolfgang Polak]],  *An Introduction to Quantum Computing for Non-Physicists*, ACM Comput. Surveys **32** (2000) 300-335 &lbrack;[arXiv:quant-ph/9809016](https://arxiv.org/abs/quant-ph/9809016), [doi:10.1145/367701.367709](https://dl.acm.org/doi/10.1145/367701.367709)&rbrack;


* [[John Preskill]], *Quantum Computation*, lecture notes, since 2004 &lbrack;[web](http://theory.caltech.edu/~preskill/ph229/)&rbrack;

* {#Kuperberg05} [[Greg Kuperberg]], _A concise introduction to quantum probability, quantum mechanics, and quantum computation_ (2005) &lbrack;[pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf), [[Kuperberg-ConciseQuantum.pdf:file]]&rbrack;


* [[Jens Eisert]], M. M. Wolf, _Quantum computing_, In: _Handbook of Nature-Inspired and Innovative Computing_, Springer 2006 ([arXiv:quant-ph/0401019](https://arxiv.org/abs/quant-ph/0401019))

* [[Scott Aaronson]], _Quantum Computing Since Democritus_, Lecture notes (2006) &lbrack;[web](http://www.scottaaronson.com/democritus/)&rbrack;

* [[Phillip Kaye]], [[Raymond Laflamme]], [[Michele Mosca]], *An Introduction to Quantum Computing*, Oxford University Press (2007) &lbrack;[pdf](http://mmrc.amss.cas.cn/tlb/201702/W020170224608149125645.pdf), [ISBN:9780198570493](https://global.oup.com/academic/product/an-introduction-to-quantum-computing-9780198570493?cc=at&lang=en&)&rbrack;
 
* {#Loceff13} Michael Loceff, _A course in quantum computing_, 2013 ([pdf](https://www.fgamedia.org/faculty/loceff/cs_courses/cs_83a/Intro_to_QC_Vol_1_Loceff.pdf))

* [[Scott Aaronson]], *Introduction to Quantum Information Science* (2018) &lbrack;[pdf](https://www.scottaaronson.com/qclec.pdf), [webpage](https://www.scottaaronson.com/cs378/)&rbrack;

  *Introduction to Quantum Information Science II* (2022) &lbrack;[pdf](https://www.scottaaronson.com/qisii.pdf)&rbrack;

* Emily Grumbling, Mark Horowitz (eds.): *Quantum Computing: Progress and Prospects*, National Academies of Sciences (2019) &lbrack;[ISBN:9780309479691](https://nap.nationalacademies.org/catalog/25196/quantum-computing-progress-and-prospects), [doi:10.17226/25196](https://doi.org/10.17226/25196)&rbrack;

* Qiang Zhang, Feihu Xu, Li Li, Nai-Le Liu, Jian-Wei Pan, *Quantum information research in China*, Quantum Sci. Technol. 4 040503 ([doi:10.1088/2058-9565/ab4bea](https://iopscience.iop.org/article/10.1088/2058-9565/ab4bea))

* Farzan Jazaeri, Arnout Beckers, Armin Tajalli, Jean-Michel Sallese, *A Review on Quantum Computing: Qubits, Cryogenic Electronics and Cryogenic MOSFET Physics*, 2019 MIXDES - 26th International Conference "Mixed Design of Integrated Circuits and Systems" (2019) 15-25 &lbrack;[arXiv:1908.02656](https://arxiv.org/abs/1908.02656), [doi:10.23919/MIXDES.2019.8787164](https://doi.org/10.23919/MIXDES.2019.8787164)&rbrack;


* [[Melanie Swan]], [[Renato P dos Santos]], [[Frank Witte]], Between Science and Economics, Volume 2: *Quantum Computing Physics, Blockchains, and Deep Learning Smart Networks*, World Scientific 2020 ([doi:10.1142/q0243](https://doi.org/10.1142/q0243))

* Jiajun Chen, *Review on Quantum Communication and Quantum Computation*,  Journal of Physics: Conference Series, Volume 1865, 2021 International Conference on Advances in Optics and Computational Sciences (ICAOCS) 2021 21-23 January 2021, Ottawa, Canada ([doi:10.1088/1742-6596/1865/2/022008](https://iopscience.iop.org/article/10.1088/1742-6596/1865/2/022008))

* David Matthews,  *How to get started in quantum computing*, Nature **591** March  2021 ([nature:d41586-021-00533-x](https://www.nature.com/articles/d41586-021-00533-x), [pdf](https://media.nature.com/original/magazine-assets/d41586-021-00533-x/d41586-021-00533-x.pdf))

* Christine Middleton, *What’s under the hood of a quantum computer?*, Physics Today, March 2021 ([doi:10.1063/PT.6.1.20210305a](https://physicstoday.scitation.org/do/10.1063/PT.6.1.20210305a))

* [[John Preskill]], *The Physics of Quantum Information*, talk at *The Physics of Quantum Information*, 28th Solvay Conference on Physics (2022) &lbrack;[arXiv:2208.08064](https://arxiv.org/abs/2208.08064)&rbrack;

* Oswaldo Zapata, *A Short Introduction to Quantum Computing for Physicists* &lbrack;[arXiv:2306.09388](https://arxiv.org/abs/2306.09388)&rbrack;

* [[Peter Shor]], *Quantum Computation*, Lecture notes (2022) &lbrack;[web](https://math.mit.edu/~shor/435-LN/)&rbrack;

* Anton Frisk et al., *Lecture notes on quantum computing* &lbrack;[arXiv:2311.08445](https://arxiv.org/abs/2311.08445)&rbrack;

* I. I. Beterov: *Progress and Prospects in the Field of Quantum Computing*, Optoelectron. Instrument. Proc. **60** (2024) 74–83 &lbrack;[doi:10.3103/S8756699024700043](https://doi.org/10.3103/S8756699024700043)&rbrack;


On "continuous variable" analog quantum computation:

* Sophie Choe, *Quantum computing overview: discrete vs. continuous variable models* &lbrack;[arXiv:2206.07246](https://arxiv.org/abs/2206.07246)&rbrack;

* [[Vivien M. Kendon]], [[Kae Nemoto]], [[William J. Munro]], *Quantum Analogue Computing*, Phil. Trans. R. Soc. A **368** 1924 (2010) 3621-3632 &lbrack;[arXiv:1001.2215](https://arxiv.org/abs/1001.2215), [doi:10.1098/rsta.2010.0017](https://doi.org/10.1098/rsta.2010.0017)&rbrack;


See also:

* Wikipedia, _[Quantum computation](http://en.wikipedia.org/wiki/Quantum_computation)_

* [The Net Advance of Physics](http://web.mit.edu/redingtn/www/netadv/): *[Quantum Computation](http://web.mit.edu/redingtn/www/netadv/Xqucomputa.html)*

* [Quantiki](https://www.quantiki.org/) -- Quantum Information Portal and Wiki

* idquantique, *Quantum Computing Review*:

  * [q2 2020](https://www.idquantique.com/quantum-computing-review-q2-2020/)

  * [q3 2020](https://www.idquantique.com/quantum-computing-review-q3-2020/)

  * [q4 2020](https://www.idquantique.com/quantum-computing-review-q4-2020/)

  * [q2 2021](https://www.idquantique.com/quantum-computing-review-q2-2021/)

  * [q3 2021](https://www.idquantique.com/quantum-computing-review-q3-2021/)

  * [q4 2021](https://www.idquantique.com/quantum-computing-review-q4-2021/)

  * [q1 2022](https://www.idquantique.com/quantum-computing-review-q1-2022/)




Experimental demonstration of "[[quantum supremacy]]" ("quantum advantage"):

* F. Arute et al. *Quantum supremacy using a programmable superconducting processor*, Nature **574** (2019) 505–510 ([doi:10.1038/s41586-019-1666-5](https://doi.org/10.1038/s41586-019-1666-5))

* Han-Sen Zhong et al., *Quantum computational advantage using photons*, Science  **370** 6523 (2020) 1460-1463 ([doi:10.1126/science.abe8770](https://science.sciencemag.org/content/370/6523/1460))

Review:

* Adrian Cho, *Google claims quantum computing milestone*, Science **365** 6460 (2019) 1364 ([doi:10.1126/science.365.6460.1364](https://science.sciencemag.org/content/365/6460/1364))

* Philip Ball, *Physicists in China challenge Google’s "quantum advantage"*, Nature **588** 380 (2020) ([doi:10.1038/d41586-020-03434-7](https://doi.org/10.1038/d41586-020-03434-7))

* {#DasSarma22} [[Sankar Das Sarma]], *Quantum computing has a hype problem*, [MIT Technology Review (March 2022)](https://www.technologyreview.com/2022/03/28/1048355/quantum-computing-has-a-hype-problem/)

  > The [[qubit]] systems we have today are a tremendous scientific achievement, but they take us no closer to having a quantum computer that can solve a problem that anybody cares about. $[\cdots]$ What is missing is the breakthrough $[\cdots]$ bypassing [[quantum error correction]] by using far-more-stable qubits, in an approach called [[topological quantum computing]].

Potential relation to the [[Unruh effect]]:

* Eric W. Aspling, John A. Marohn, Michael J. Lawler, *Design Constraints for Unruh-DeWitt Quantum Computers* &lbrack;[arXiv:2210.12552](https://arxiv.org/abs/2210.12552)&rbrack;




[[!include quantum programming languages -- references]]


### Classically controlled quantum computing 
 {#ReferencesClassicallyControlledQuantumComputing}

Theory of [[classically controlled quantum computing]] and [[parameterized quantum circuits]]:

* {#Knill96} [[Emanuel Knill]], *Conventions for quantum pseudocode*, Los Alamos Technical Report (1996) &lbrack;[LA-UR-96-2724](https://www.osti.gov/biblio/366453-conventions-quantum-pseudocode), [doi:10.2172/366453](https://doi.org/10.2172/366453), [pdf](https://www.osti.gov/servlets/purl/366453)&rbrack;


* {#Omer03} [[Bernhard Ömer]], *Structured Quantum Programming*, 2003/2009 ([pdf](http://www.itp.tuwien.ac.at/~oemer/doc/structquprog.pdf))

* Simon Perdrix, Philippe Jorrand, *Classically-Controlled Quantum Computation*, Math. Struct. in Comp. Science, 16:601-620, 2006 ([arXiv:quant-ph/0407008](https://arxiv.org/abs/quant-ph/0407008))


* {#NagarajanPapanikolaouWilliams07} Rajagopal Nagarajan, Nikolaos Papanikolaou, David Williams, *Simulating and Compiling Code for the Sequential Quantum Random Access Machine*, Electronic Notes in Theoretical Computer Science Volume 170, 6 March 2007, Pages 101-124 ([doi:10.1016/j.entcs.2006.12.014](https://doi.org/10.1016/j.entcs.2006.12.014))

* {#Miszczak11} [[Jarosław Adam Miszczak]], *Models of quantum computation and quantum programming languages*, Bull. Pol. Acad. Sci.-Tech. Sci., Vol. 59, No. 3 (2011), pp. 305-324 ([arXiv:1012.6035](https://arxiv.org/abs/1012.6035))

* {#Devitt14} [[Simon J. Devitt]], *Classical Control of Large-Scale Quantum Computers*, In: S. Yamashita, S. Minato  (eds.) *Reversible Computation* Lecture Notes in Computer Science **8507**, Springer (2014) &lbrack;[arXiv:1405.4943](https://arxiv.org/abs/1405.4943), [doi:10.1007/978-3-319-08494-7_3](https://doi.org/10.1007/978-3-319-08494-7_3)&rbrack;

* Jarrod R McClean, Jonathan Romero, Ryan Babbush and Alán Aspuru-Guzik, *The theory of variational hybrid quantum-classical algorithms*, New Journal of Physics, Volume 18, February 2016 ([doi:10.1088/1367-2630/18/2/023023](https://iopscience.iop.org/article/10.1088/1367-2630/18/2/023023))

* Murray Thom (D-Wave), *[Three Truths and the Advent of Hybrid Quantum Computing](https://medium.com/d-wave/three-truths-and-the-advent-of-hybrid-quantum-computing-1941ba46ff8c)* (Jun 25, 2019)

* {#KESWDSC23} Yaniv Kurman, Lior Ella, Ramon Szmuk, Oded Wertheim, Benedikt Dorschner, Sam Stanwyck, Yonatan Cohen: *Control Requirements and Benchmarks for Quantum Error Correction* &lbrack;[arXiv:2311.07121](https://arxiv.org/abs/2311.07121)&rbrack;


* {#CRKAW24} Daan Camps, Ermal Rrapaj, Katherine Klymko, Brian Austin, Nicholas J. Wright: *Evaluation of the Classical Hardware Requirements for Large-Scale Quantum Computations*, ISC High Performance 2024 Research Paper Proceedings (39th International Conference), Hamburg, Germany (2024) 1-12 &lbrack;[doi:10.23919/ISC.2024.10528937](https://doi.org/10.23919/ISC.2024.10528937)&rbrack;

Application of classically controlled quantum computation:

* {#KimSwingle17} Isaac H. Kim, [[Brian Swingle]], *Robust entanglement renormalization on a noisy quantum computer* ([arXiv:1711.07500](https://arxiv.org/abs/1711.07500))

  > (in terms of [[holographic entanglement entropy|holographic]] [[tensor network]] states)


* Sukin Sim, Peter D. Johnson, Alan Aspuru-Guzik, *Expressibility and entangling capability of parameterized quantum circuits for hybrid quantum-classical algorithms*, Adv. Quantum Technol. 2 (2019) 1900070 ([arXiv:1905.10876](https://arxiv.org/abs/1905.10876))

* Mateusz Ostaszewski, Edward Grant, Marcello Benedetti, *Structure optimization for parameterized quantum circuits*, Quantum 5, 391 (2021) ([arXiv:1905.09692](https://arxiv.org/abs/1905.09692))


* {#ShaydulinEtAl19} Ruslan Shaydulin et al., *A Hybrid Approach for Solving Optimization Problems on Small Quantum Computers* ([doi:10.1109/MC.2019.2908942](https://doi.ieeecomputersociety.org/10.1109/MC.2019.2908942))

* Eneko Osaba, Esther Villar-Rodriguez, Izaskun Oregi, Aitor Moreno-Fernandez-de-Leceta, *Focusing on the Hybrid Quantum Computing -- Tabu Search Algorithm: new results on the Asymmetric Salesman Problem* ([arXiv:2102.05919](https://arxiv.org/abs/2102.05919))


in particular in [[quantum machine learning]]:

* {#BenedettiLloydSackFiorentini19} Marcello Benedetti, Erika Lloyd, Stefan Sack, Mattia Fiorentini, *Parameterized quantum circuits as machine learning models*, Quantum Science and Technology **4** 043001 (2019) &lbrack;[arXiv:1906.07682](https://arxiv.org/abs/1906.07682)&rbrack;

* D. Zhu et al. *Training of quantum circuits on a hybrid quantum computer*, Science Advances, 18 Oct 2019: Vol. 5, no. 10, eaaw9918 ([doi: 10.1126/sciadv.aaw9918](https://advances.sciencemag.org/content/5/10/eaaw9918))


* {#MariBromleyIzaacSchuldKilloran20} Andrea Mari, Thomas R. Bromley, Josh Izaac, Maria Schuld, Nathan Killoran,  *Transfer learning in hybrid classical-quantum neural networks*, Quantum 4, 340 (2020) ([arXiv:1912.08278](https://arxiv.org/abs/1912.08278))

* Thomas Hubregtsen, Josef Pichlmeier, Patrick Stecher, Koen Bertels, *Evaluation of Parameterized Quantum Circuits: on the relation between classification accuracy, expressibility and entangling capability*, Quantum Machine Intelligence volume 3, Article number: 9 (2021) ([arXiv:2003.09887](https://arxiv.org/abs/2003.09887), [doi:10.1007/s42484-021-00038-w](https://doi.org/10.1007/s42484-021-00038-w))

* {#TensorFlow} [TensorFlow.org](https://www.tensorflow.org/) (Google), *[Hybrid quantum classical models](https://www.tensorflow.org/quantum/concepts#hybrid_quantum-classical_models)*



### Noisy intermediate-scale quantum (NISQ) computing
 {#ReferencesNISQ}

The origin of the notion:

* Nikolaj Moll et al., *Quantum optimization using variational algorithms on near-term quantum devices*, Quantum Science and Technology **3** 3 (2018) &lbrack[arXiv:1710.01022](https://arxiv.org/abs/1710.01022), [doi:10.1088/2058-9565/aab822](https://doi.org/10.1088/2058-9565/aab822)&rbrack;

* {#Preskill18} [[John Preskill]], *Quantum Computing in the NISQ era and beyond*, Quantum **2** 79 (2018) &lbrack;[arXiv:1801.00862](https://arxiv.org/abs/1801.00862), [doi:10.22331/q-2018-08-06-79](https://doi.org/10.22331/q-2018-08-06-79)&rbrack;



{#NISQLimitations} On the limitations of ([[quantum error correction|quantum error-corrected]]) NISQ machines in achieving any [[quantum advantage]]:

* Subhash Kak: *Prospects for Quantum Computing*, talk at CIFAR Nanotechnology program meeting, Halifax (November 2008) &lbrack;[arXiv:0902.4884](https://arxiv.org/abs/0902.4884)&rbrack;

* Mikhail Dyakonov: *Prospects for quantum computing: extremely doubtful*, Int. J. of Modern Physics: Conf. Series **33** (2014) 1460357 &lbrack;[arXiv:1401.3629](https://arxiv.org/abs/1401.3629), [doi:10.1142/S2010194514603573](https://doi.org/10.1142/S2010194514603573)&rbrack;

* Daniel Koch, Brett Martin, Saahil Patel, Laura Wessing, and Paul M. Alsing, *Demonstrating NISQ era challenges in algorithm design on IBM's 20 qubit quantum computer*, AIP Advances **10** 095101 (2020) &lbrack;[doi:10.1063/5.0015526](https://doi.org/10.1063/5.0015526)&rbrack;

* {#LeymannBarzen20} Frank Leymann, Johanna Barzen, *The bitter truth about gate-based quantum algorithms in the NISQ era*, Quantum Sci. Technol. **5** 044007 (2020) &lbrack;[doi:10.1088/2058-9565/abae7d](https://iopscience.iop.org/article/10.1088/2058-9565/abae7d)&rbrack;

* Mikhail Dyakonov: *Will We Ever Have a Quantum Computer*, Springer Briefs in Physics, Springer (2020) &lbrack;[doi:10.1007/978-3-030-42019-2](https://doi.org/10.1007/978-3-030-42019-2), [pdf](https://link.springer.com/content/pdf/10.1007/978-3-030-42019-2.pdf)&rbrack;
  > (the author's conclusion is: "No.")


* {#Ezratty} [[Olivier Ezratty]], *Where are we heading with NISQ?* &lbrack;[arXiv:2305.09518](https://arxiv.org/abs/2305.09518), [InSpire:2660378](https://inspirehep.net/literature/2660378)&rbrack;
  > "no one has yet successfully implemented a use case matching the original definition of the NISQ regime."

  > "Totally outside the NISQ relevant algorithms class are integer and discrete log factoring algorithms &lbrack;[[Shor's algorithm]]&rbrack;, oracle based search algorithms &lbrack;[[Grover's algorithm]]&rbrack;, and all algorithms relying on a quantum Fourier transform"

  > "most NISQ experiments have been run with fewer than 30 qubits and should therefore better be labelled as “pre-NISQ”. While they are elegant proofs of concepts, they do not yet demonstrate any speed up over classical computing"

* [[Olivier Ezratty]], *Where are we heading with NISQ?*, blog post (2023) &lbrack;[web](https://www.oezratty.net/wordpress/2023/where-are-we-heading-with-nisq/), [pdf](https://www.oezratty.net/wordpress/2023/where-are-we-heading-with-nisq/?output=pdf)&rbrack;
  > NISQ is not at all ready for prime time quantum computing despite all the fuss about “quantum computing being business ready”. Not only have we not yet reached any quantum computing advantage, but in many cases, even if it worked, the most common NISQ algorithms using a variational approach, have prohibitively long execution times particularly in the promising chemical simulations domain.

* Jonathan Wei Zhong Lau, Kian Hwee Lim, Harshank Shrotriya, Leong Chuan Kwek, *NISQ computing: where are we and where do we go?*, AAPPS Bull. **32** 27 (2022) &lbrack;[doi:10.1007/s43673-022-00058-z](https://doi.org/10.1007/s43673-022-00058-z)&rbrack;
  > However, quantum computers are still far from achieving all that they have promised. While early-stage quantum computers have been developed, the problems of noisy calculations and scalability of quantum computers still plague the field. As opposed to the far future, where quantum computers can be as big as we wish them to be and are capable of performing fully controllable operations (termed as the fault-tolerant era), we are currently working in the *Noisy Intermediate-Scale Quantum* (NISQ) era, which is an operational definition that implies that the quantum computers available to us now are subject to substantial error rates and they are constrained in size (in terms of the number of qubits). While it is already a scientific achievement to get to this stage, such quantum computers are still incapable of showing any significant advantages over classical computers. As such, some people in the community have already expressed fear that there will be a ‘Quantum winter’, or a scenario where quantum computing devices remain noisy and are unable to scale up in terms of qubit size, preventing us from ever achieving a meaningful advantage over classical computers.

* {#Preskill23} [[John Preskill]], *Crossing the Quantum Chasm: From NISQ to Fault Tolerance*, talk at Q2B 2023 Silicon Valley (2023) &lbrack;[pdf](http://theory.caltech.edu/~preskill/talks/Preskill-Q2B-2023), [[Preskill-Crossing.pdf:file]]&rbrack;
  > "there is no proposed application of NISQ computing with commercial value for which quantum advantage has been demonstrated"

  > "Nor are there persuasive theoretical arguments indicating that commercially viable applications will be found that do not use quantum error-correcting codes and fault-tolerant quantum computing."

* {#HHT23} Torsten Hoefler, Thomas Haener, [[Matthias Troyer]], *Disentangling Hype from Practicality: On Realistically Achieving Quantum Advantage*, Communications of the ACM **66**  5 (May 2023) 82-87 &lbrack;[arXiv:2307.00523](https://arxiv.org/abs/2307.00523), [acm pdf](https://dl.acm.org/doi/pdf/10.1145/3571725), [doi:10.1145/3571725](https://doi.org/10.1145/3571725)&rbrack;
  > "A large range of problem areas with quadratic quantum speedups, such as many current machine learning training approaches, accelerating drug design and protein folding with Grover’s algorithm, speeding up Monte Carlo simulations through quantum walks, as well as more traditional scientific computing simulations including the solution of many non-linear systems of equations, such as fluid dynamics in the turbulent regime, weather, and climate simulations will not achieve quantum advantage with current quantum algorithms in the foreseeable future."

* Edd Gent: *Quantum Computing’s Hard, Cold Reality Check*, IEEE Spectrum (Dec. 2023) &lbrack;[webpage](https://spectrum.ieee.org/quantum-computing-skeptics)&rbrack;

* Xavier Waintal: *The Quantum House Of Cards*, PNAS **121** 1 (2024) e2313269120 \[<a href="https://doi.org/10.1073/pnas.2313269120">doi:10.1073/pnas.2313269120</a>, [arXiv:2312.17570](https://arxiv.org/abs/2312.17570)\]


On the resulting drop in investment:

* {#McKenzie2024} James McKenzie: *Quantum winter? No chance!*,  Physics World, **37** 5 (2024) 41 &lbrack;[doi:10.1088/2058-7058/37/05/32](https://iopscience.iop.org/article/10.1088/2058-7058/37/05/32)&rbrack;

More optimistic outlook:

* S. G. Gill et al.: *Quantum Computing: Vision and Challenges* &lbrack;[arXiv:2403.02240](https://arxiv.org/abs/2403.02240)&rbrack;

* [[John Preskill]]: *Beyond NISQ: The Megaquop Machine*, talk at *[Q2B 2024 Silicon Valley](https://q2b.qcware.com/2024-conferences/silicon-valley/)* (Dec. 2024) &lbrack;[pdf](https://www.preskill.caltech.edu/talks/Preskill-Q2B-2024.pdf), [webpage](https://quantumfrontiers.com/2024/12/14/beyond-nisq-the-megaquop-machine/)&rbrack;



More concerned outlook:

  > <div style="float:right;margin:-15px 0px 00px 20px;"><a href="https://youtu.be/E98zLxB7EQs?t=85"><img src="/nlab/files/DARPA-QBI-IFItTurnsOutNotPossible.jpg" width="230"></a></div>

* {#DarpaQBI} DARPA: *[Quantum Benchmarjing Initiative](https://www.darpa.mil/work-with-us/quantum-benchmarking-initiative)*
  > "to determine if it’s possible to build an industrially useful quantum computer much faster than conventional predictions. Specifically, QBI is designed to rigorously verify and validate if any quantum computing approach can achieve utility-scale operation — meaning its computational value exceeds its cost — by the year 2033."

  > The [accompanying video](https://youtu.be/E98zLxB7EQs) says at [1:25](https://youtu.be/E98zLxB7EQs?t=85): 

  > "If it turns out, as a lot of us suspect, that that's really not possible, and it really won't do something useful, or there isn't a path, we need to know that, too."




### Quantum programming via monads
 {#ReferencesInTermsOfMonads}

Discussion of aspects of quantum programming in terms of [[monad (in computer science)|monads]] in [[functional programming]] are in 

* [[Thorsten Altenkirch]], Alexander Green, _The quantum IO monad_, in _Semantic Techniques in Quantum Computation_, January 2009, appeared in 2010 ([pdf](http://www.cs.nott.ac.uk/~txa/publ/qio-chapter.pdf), [talk slides](http://www.cs.nott.ac.uk/~txa/talks/qnet06.pdf))


* J. K. Vizzotto, [[Thorsten Altenkirch]], A. Sabry, _Structuring quantum effects: superoperators as arrows_ ([arXiv:quant-ph/0501151](http://arxiv.org/abs/quant-ph/0501151))

### As linear logic
 {#ReferencesAsLinearLogic}

Discussion of quantum computation as the [[internal logic|internal]] [[linear logic]]/[[linear type theory]] of [[compact closed categories]] is in

* {#AbramskyDuncan05} [[Samson Abramsky]], [[Ross Duncan]], _A Categorical Quantum Logic_, Mathematical Structures in Computer Science, 2006 ([arXiv:quant-ph/0512114](http://arxiv.org/abs/quant-ph/0512114))
 
* {#Duncan06} [[Ross Duncan]], _Types for quantum mechanics_, 2006 ([pdf](http://personal.strath.ac.uk/ross.duncan/papers/rduncan-thesis.pdf), [slides](http://www.cs.ox.ac.uk/people/ross.duncan/talks/2005/pps-22-05-2005.pdf))
 

* {#LagoFaffian12} [[Ugo Dal Lago]], [[Claudia Faggian]], _On Multiplicative Linear Logic, Modality and Quantum Circuits_, EPTCS 95, 2012, pp. 55-66 ([arXiv:1210.0613](http://arxiv.org/abs/1210.0613))
 

An exposition along these lines is in

* [[John Baez]], [[Mike Stay]], _Physics, topology, logic and computation: a rosetta stone_, [arxiv/0903.0340](http://arxiv.org/abs/0903.0340); in "New Structures for Physics", ed. Bob Coecke, Lecture Notes in Physics __813__, Springer, Berlin, 2011, pp. 95-174




[[!include quantum information theory via string diagrams -- references]]






### Topological quantum computing

[[topological quantum computation]] is discussed in

* [[Michael Freedman]], [[Alexei Kitaev]], Michael J. Larsen, Zhenghan Wang, _Topological Quantum Computation_ ([arXiv:quant-ph/0101025](http://arxiv.org/abs/quant-ph/0101025))

* Zhenghan Wang, _Topologization of electron liquids with Chern-Simons theory and quantum computation_ ([arXiv:cond-mat/0601285](http://arxiv.org/abs/cond-mat/0601285))

* {#FreedmanLarsenWang00} [[Michael Freedman]], [[Michael Larsen]], [[Zhenghan Wang]], _A modular functor which is universal for quantum computation_, Communications in Mathematical Physics **227** (2002) 605–622 &lbrack;[arXiv:quant-ph/0001108](http://arxiv.org/abs/quant-ph/0001108), [doi:10.1007/s002200200645](https://doi.org/10.1007/s002200200645)&rbrack;

* [[Alexei Kitaev]], _Fault-tolerant quantum computation by anyons_, Annals Phys. 303 (2003) 2-30 ([arXiv:quant-ph/9707021](http://arxiv.org/abs/quant-ph/9707021))


### Relation to tensor networks

Relation to [[tensor networks]], specifically [[matrix product states]]:

* Yiqing Zhou, E. Miles Stoudenmire, Xavier Waintal, _What limits the simulation of quantum computers?_, [arXiv:2002.07730](https://arxiv.org/abs/2002.07730)





[[!include spin resonance qbits -- references]]




[[!include superconducting qbits -- references]]




### Photonic qbits

Realization in photonics:

* Han-Shen Zhong et al. _Quantum computational advantage using photons_, Science 370, n. 6523 (2020) 1460-1463 [doi](https://doi.org/10.1126/science.abe8770)





### Commercial quantum computers
 {#CommercialQuantumComputers}

Since 2019, NISQ quantum computers can be accessed through cloud services:

* New Scientist, *[IBM unveils its first commercial quantum computer](https://www.newscientist.com/article/2189909-ibm-unveils-its-first-commercial-quantum-computer/)* (Jan 2019)

* [IBM Quantum](https://quantum-computing.ibm.com/) (Cloud service) 

  [IBM Quantum compute resources](https://quantum-computing.ibm.com/lab/docs/iql/manage/systems/)

  [Build and deploy quantum programs with Qiskit Runtime](https://cloud.ibm.com/quantum)

There exist toy desktop quantum computers for educational purposes, operating on a couple of [[nuclear magnetic resonance]] [[qbits]] at room temperature :

* [CIQTEK](https://en.ciqtek.com/): *[Diamond Quantum Computer for Education](https://en.ciqtek.com/products/detail/diamond-quantum-computer-for-education.html?id=644102ee-942e-4568-aacd-20241a1a2469&id=644102ee-942e-4568-aacd-20241a1a2469)*

* [SpinQ](https://www.spinquanta.com/): *SpinQ Triangulum: a commercial three-qubit desktop quantum computer* &lbrack;[arXiv:2202.02983](https://arxiv.org/abs/2202.02983)&rbrack;



category: computer science, physics


[[!redirects quantum computing]]
[[!redirects quantum computations]]

[[!redirects quantum computer]]
[[!redirects quantum computers]]


[[!redirects classically controlled quantum computation]]
[[!redirects parameterized quantum computation]]



[[!redirects NISQ]]
[[!redirects noisy intermediate-scale quantum computer]]
[[!redirects noisy intermediate-scale quantum computer]]
[[!redirects noisy intermediate-scale quantum computing]]


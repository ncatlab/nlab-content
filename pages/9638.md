
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

_Quantum computation_ is [[computation]] in terms of [[quantum information theory]], possibly implemented on _quantum computers_, hence on [[physical systems]] for which phenomena of [[quantum mechanics]] are not negligible. In terms of the [[computational trilogy]], quantum computation is the computation corresponding to (some kind of) [[quantum logic]]/[[linear type theory]].

Usually [[quantum gates]] are understood/required to implement [[unitary operators]] on a given [[Hilbert space]] [[space of quantum states|of quantum states]], which implies that quantum comptuation is a form of [[reversible computation]]. This implies its susceptibility to noise and the practical need for [[quantum error correction]] and/or [[topological quantum computation|topological quantum stabilization]].

Specifically, _[[topological quantum computation]]_ is (or is meant to be) quantum computation implemented on [[physical systems]] governed by [[topological quantum field theory]], such as [[Chern-Simons theory]]. A prominent example of this is the (fractional) [[quantum Hall effect]] in [[solid state physics]].

### Classical control, quantum data
 {#ClassicalControlQuantumData}

Any practical quantum computer will be *[[classically controlled quantum computation|classically controlled]]* ([Knill 96](#Knill96), [Ömer 03](#Omer03), [Nagarajan, Papanikolaou & Williams 07](#NagarajanPapanikolaouWilliams07), [Devitt 14](#Devitt14), in line with the general idea of *[[parameterized quantum systems]]*):

\begin{imagefromfile}
    "file_name": "ClassicallyControlledQuantumComputation.jpg",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Miszczak 11](#Miszczak11)"
\end{imagefromfile}

\linebreak

\begin{imagefromfile}
    "file_name": "SQRAMPrinciple.jpg",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Nagarajan, Papanikolaou & Williams 07](#NagarajanPapanikolaouWilliams07)"
\end{imagefromfile}

See the list of references [below](#ReferencesClassicallyControlledQuantumComputing).

The paradigm of [[classically controlled quantum computation]] applies in particular ([Kim & Swingle 17](#KimSwingle17)) to the currently and near-term available noisy intermediate-scale quantum (NISQ) computers ([Preskill 18](#Preskill18), see the references [below](#ReferencesNISQ)), which are useful for highly specialized tasks (only) and need to be emdedded in and called from a more comprehensive classical computing environment. 

This, in turn, applies particularly to applications like [[quantum machine learning]] ([Benedetti, Lloyd, Sack & Fiorentini 19](#BenedettiLloydSackFiorentini19), [TensorFlow Quantum](#TensorFlow), for more see the references [there](machine+learning#ReferencesQuantumMachineLearning)).






### Quantum languages and quantum circuits

A natural way (via [[computational trinitarianism]]) to understand [[quantum programming languages]] is as  [[linear logic]]/[[linear type theory]] ([Pratt 92](#Pratt92), for more see at *[[quantum logic]]*) with [[categorical semantics]] in non-[[Cartesian monoidal category|cartesian]] [[symmetric monoidal categories]] ([Abramsky & Coecke 04](#AbramskyCoecke04), [Abramsky & Duncan 05](#AbramskyDuncan05), [Duncan 06](#Duncan06), [Lago-Faffian 12](#LagoFaffian12)).  .

The corresponding [[string diagrams]] are known as *[[quantum circuit diagrams]]*.

In fact, languages for [classically controlled quantum computation](#ClassicalControlQuantumData)  should be based on [[dependent linear type theory]] ([Vakar 14](dependent+linear+type+theory#Vakar14), [Vakar 15](dependent+linear+type+theory#Vakar15), [Vakar 17, Sec. 3](dependent+linear+type+theory#Vakar17), [Lundfall 17](dependent+linear+type+theory#Lundfall17), [Lundfall 18](dependent+linear+type+theory#Lundfall18), following [Schreiber 14](dependent+linear+type+theory#Schreiber14)) with [[categorical semantics]] in [[indexed monoidal categories]]:

| classical control | quantum data | 
|-------------------|--------------|
| [[intuitionistic type theory|intuitionistic types]] | [[dependent linear type theory|dependent linear types]]

This idea of classically controlled quantum programming via [[dependent linear type theory]] has been implemented for the *[[Quipper]]* language in [FKS 20](#FKS20), [FKRS 20](#FKRS20).




## Related entries

* [[Bloch region]], [[quantum operation]]

* [[Grover's algorithm]]

* [[Shor's algorithm]]

* [[quantum error correction]]

* [[quantum information theory]]

* [[quantum circuit]]

* [[quantum logic]], [[linear logic]]

* [[adiabatic quantum computation]]

* [[topological quantum computation]]

* [[quantum Hall effect]], [[Chern-Simons theory]].

* [[superoperator]]

* [[computable physics]]

* [[quantum probability]]


## References

### General

The idea of quantum computation was first expressed in:

* {#Manin1980} [[Yuri I. Manin]], Introduction to: *Computable and Uncomputable*, Sov. Radio (1980) &lbrack;Russian original: [[Manin-1980.pdf:file]]&rbrack;, Enlish translation on p. 69-77 of *Mathematics as Metaphor: Selected essays of Yuri I. Manin*, Collected Works **20**, AMS (2007) &lbrack;[ISBN:978-0-8218-4331-4](https://bookstore.ams.org/cworks-20/)&rbrack;

  > Perhaps, for a better understanding of &lbrack;molecular bilogy&rbrack;, we need a mathematical theory of quantum automata.

* Paul Benioff, *The computer as a physical system: A microscopic quantum mechanical Hamiltonian model of computers as represented by Turing machines*, J Stat Phys 22, 563–591 (1980) &lbrack;[doi:10.1007/BF01011339](https://doi.org/10.1007/BF01011339)&rbrack;

* {#Feynman82} [[Richard Feynman]], *Simulating physics with computers*,  Int J Theor Phys 21, 467–488 (1982) ([doi:10.1007/BF02650179](https://doi.org/10.1007/BF02650179))

  > because nature isn't classical, dammit, if you want to make a simulation of nature, you'd better make it quantum mechanical



The terminology *[[q-bit]]* goes back to:

* [[Benjamin Schumacher]], *Quantum coding*, Phys. Rev. A **51** (1995) 2738 $[$[doi:10.1103/PhysRevA.51.2738](https://doi.org/10.1103/PhysRevA.51.2738)$]$


The potential practical relevanc ()e of quantum computation was highlighted early on via toy examples

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

Quantum computation became widely thought to be not just a theoretical but a plausible practical possibility with the understanding of [[quantum error correction]]:

* {#Shor95} [[Peter W. Shor]], *Scheme for reducing decoherence in quantum computer memory*, Phys. Rev. A 52, R2493(R) 1995 ([doi:10.1103/PhysRevA.52.R2493](https://doi.org/10.1103/PhysRevA.52.R2493))

* {#Steane96} [[Andrew M. Steane]], *Error Correcting Codes in Quantum Theory*, Phys. Rev. Lett. 77, 793 1996 ([doi:10.1103/PhysRevLett.77.793](https://doi.org/10.1103/PhysRevLett.77.793))

* {#CalderbankShor96} [[Robert Calderbank]], [[Peter W. Shor]], *Good Quantum Error-Correcting Codes Exist*, Phys. Rev. A, Vol. 54, No. 2, pp. 1098-1106, 1996 ([doi:10.1103/PhysRevA.54.1098](https://doi.org/10.1103/PhysRevA.54.1098))

Early review:

* [[Yuri I. Manin]], *Classical computing, quantum computing, and Shor's factoring algorithm*, Astérisque, **266** Séminaire Bourbaki 862 (2000) 375-404 &lbrack;[arXiv:quant-ph/9903008](https://arxiv.org/abs/quant-ph/9903008), [numdam:SB_1998-1999__41__375_0](http://www.numdam.org/item/?id=SB_1998-1999__41__375_0)&rbrack;


Textbook accounts:

* [[Ranee K. Brylinski]], [[Goong Chen]] (eds.), *Mathematics of Quantum Computation*, Chapman and Hall/CRC 2002 ([doi:10.1201/9781420035377](https://doi.org/10.1201/9781420035377))

* [[Goong Chen]], [[Louis Kauffman]], [[Samuel J. Lomonaco]] (eds.), *Mathematics of Quantum Computation and Quantum Technology*, Chapman and Hall/CRC (2007) (ISBN:9780367388614, [doi:10.1201/9781584889007](https://doi.org/10.1201/9781584889007))

Introducing the notion of [[quantum supremacy]] and highlighting its relation to [[quantum entanglement]]:

* [[John Preskill]]: *Quantum computing and the entanglement frontier*: pp. 63-80 in: *The Theory of the Quantum World -- Proceedings of the 25th Solvay Conference on Physics*, World Scientific (2013) &lbrack;[arXiv:1203.5813](https://arxiv.org/abs/1203.5813), [doi:10.1142/8674](https://doi.org/10.1142/8674), slides: [pdf](https://simons.berkeley.edu/sites/default/files/docs/394/preskilljohn.pdf)&rbrack;

   
Further introduction and survey:

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], *Quantum computation and quantum information*, Cambridge University Press (2000) $[$[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]$]$

* [[Giuliano Benenti]], [[Giulio Casati]], [[Davide Rossini]], *Principles of Quantum Computation and Information*, World Scientific (2004, 2018)  ([doi:10.1142/10909](https://doi.org/10.1142/10909), [2004 pdf](http://mmrc.amss.cas.cn/tlb/201702/W020170224608149307696.pdf))


* [[John Preskill]], *Quantum Computation* lecture notes, since 2004 ([web](http://theory.caltech.edu/~preskill/ph229/))

* {#Kuperberg05} [[Greg Kuperberg]], _A concise introduction to quantum probability, quantum mechanics, and quantum computation_ (2005) &lbrack;[pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf), [[Kuperberg-ConciseQuantum.pdf:file]]&rbrack;


* [[Jens Eisert]], M. M. Wolf, _Quantum computing_, In: _Handbook of Nature-Inspired and Innovative Computing_, Springer 2006 ([arXiv:quant-ph/0401019](https://arxiv.org/abs/quant-ph/0401019))

* [[Scott Aaronson]], Lecture notes _Quantum Computing Since Democritus_ 2006 ([web](http://www.scottaaronson.com/democritus/))

* [[Phillip Kaye]], [[Raymond Laflamme]], [[Michele Mosca]], *An Introduction to Quantum Computing*, Oxford University Press (2007) &lbrack;[pdf](http://mmrc.amss.cas.cn/tlb/201702/W020170224608149125645.pdf), [ISBN:9780198570493](https://global.oup.com/academic/product/an-introduction-to-quantum-computing-9780198570493?cc=at&lang=en&)&rbrack;
 
* {#Loceff13} Michael Loceff, _A course in quantum computing_, 2013 ([pdf](https://www.fgamedia.org/faculty/loceff/cs_courses/cs_83a/Intro_to_QC_Vol_1_Loceff.pdf))

* [[Scott Aaronson]], *Introduction to Quantum Information Science* (2018) &lbrack;[pdf](https://www.scottaaronson.com/qclec.pdf), [webpage](https://www.scottaaronson.com/cs378/)&rbrack;

  *Introduction to Quantum Information Science II* (2022) &lbrack;[pdf](https://www.scottaaronson.com/qisii.pdf)&rbrack;


* National Academies of Sciences, Engineering, and Medicine, _Quantum Computing: Progress and Prospects_, The National Academies Press 2019 ([doi:10.17226/25196](https://doi.org/10.17226/25196))

* Qiang Zhang, Feihu Xu, Li Li, Nai-Le Liu, Jian-Wei Pan, *Quantum information research in China*, Quantum Sci. Technol. 4 040503 ([doi:10.1088/2058-9565/ab4bea](https://iopscience.iop.org/article/10.1088/2058-9565/ab4bea))

* Farzan Jazaeri, Arnout Beckers, Armin Tajalli, Jean-Michel Sallese, *A Review on Quantum Computing: Qubits, Cryogenic Electronics and Cryogenic MOSFET Physics*, 2019 MIXDES - 26th International Conference "Mixed Design of Integrated Circuits and Systems", 2019, pp. 15-25, ([arXiv:1908.02656](https://arxiv.org/abs/1908.02656), [doi:10.23919/MIXDES.2019.8787164](https://doi.org/10.23919/MIXDES.2019.8787164))

 

* [[Melanie Swan]], [[Renato P dos Santos]], [[Frank Witte]], Between Science and Economics, Volume 2: *Quantum Computing Physics, Blockchains, and Deep Learning Smart Networks*, World Scientific 2020 ([doi:10.1142/q0243](https://doi.org/10.1142/q0243))

* Jiajun Chen, *Review on Quantum Communication and Quantum Computation*,  Journal of Physics: Conference Series, Volume 1865, 2021 International Conference on Advances in Optics and Computational Sciences (ICAOCS) 2021 21-23 January 2021, Ottawa, Canada ([doi:10.1088/1742-6596/1865/2/022008](https://iopscience.iop.org/article/10.1088/1742-6596/1865/2/022008))

* David Matthews,  *How to get started in quantum computing*, Nature **591** March  2021 ([nature:d41586-021-00533-x](https://www.nature.com/articles/d41586-021-00533-x), [pdf](https://media.nature.com/original/magazine-assets/d41586-021-00533-x/d41586-021-00533-x.pdf))

* Christine Middleton, *What’s under the hood of a quantum computer?*, Physics Today, March 2021 ([doi:10.1063/PT.6.1.20210305a](https://physicstoday.scitation.org/do/10.1063/PT.6.1.20210305a))

* Sophie Choe, *Quantum computing overview: discrete vs. continuous variable models* $[$[arXiv:2206.07246](https://arxiv.org/abs/2206.07246)$]$

* [[John Preskill]], *The Physics of Quantum Information*, talk at
*The Physics of Quantum Information*, 28th Solvay Conference on Physics (2022) &lbrack;[arXiv:2208.08064](https://arxiv.org/abs/2208.08064)&rbrack;



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



Discussion in terms of [[monoidal category]]-theory and [[finite quantum mechanics in terms of dagger-compact categories]]:

* {#HeunenVicary19} [[Chris Heunen]], [[Jamie Vicary]], *Categories for Quantum Theory*, Oxford University Press 2019 ([ISBN:9780198739616](https://global.oup.com/academic/product/categories-for-quantum-theory-9780198739616))


Experimental demonstration of "[[quantum supremacy]]" ("quantum advantage"):

* F. Arute et al. *Quantum supremacy using a programmable superconducting processor*, Nature **574** (2019) 505–510 ([doi:10.1038/s41586-019-1666-5](https://doi.org/10.1038/s41586-019-1666-5))

* Han-Sen Zhong et al., *Quantum computational advantage using photons*, Science  **370** 6523 (2020) 1460-1463 ([doi:10.1126/science.abe8770](https://science.sciencemag.org/content/370/6523/1460))

Review:

* Adrian Cho, *Google claims quantum computing milestone*, Science **365** 6460 (2019) 1364 ([doi:10.1126/science.365.6460.1364](https://science.sciencemag.org/content/365/6460/1364))

* Philip Ball, *Physicists in China challenge Google’s "quantum advantage"*, Nature **588** 380 (2020) ([doi:10.1038/d41586-020-03434-7](https://doi.org/10.1038/d41586-020-03434-7))

* {#DasSarma22} [[Sankar Das Sarma]], *Quantum computing has a hype problem*, [MIT Technology Review (March 2022)](https://www.technologyreview.com/2022/03/28/1048355/quantum-computing-has-a-hype-problem/)

  > The [[qubit]] systems we have today are a tremendous scientific achievement, but they take us no closer to having a quantum computer that can solve a problem that anybody cares about. $[\cdots]$ What is missing is the breakthrough $[\cdots]$ bypassing [[quantum error correction]] by using far-more-stable qubits, in an approach called [[topological quantum computing]].



[[!include quantum programming languages -- references]]


### Classically controlled quantum computing 
 {#ReferencesClassicallyControlledQuantumComputing}

Theory of [[classically controlled quantum computing]] and [[parameterized quantum circuits]]:

* {#Knill96} [[Emanuel Knill]], *Conventions for quantum pseudocode*, 1996 ([LA-UR-96-2724](https://www.osti.gov/biblio/366453-conventions-quantum-pseudocode), [pdf](https://www.osti.gov/servlets/purl/366453))

* {#Omer03} [[Bernhard Ömer]], *Structured Quantum Programming*, 2003/2009 ([pdf](http://www.itp.tuwien.ac.at/~oemer/doc/structquprog.pdf))

* Simon Perdrix, Philippe Jorrand, *Classically-Controlled Quantum Computation*, Math. Struct. in Comp. Science, 16:601-620, 2006 ([arXiv:quant-ph/0407008](https://arxiv.org/abs/quant-ph/0407008))


* {#NagarajanPapanikolaouWilliams07} Rajagopal Nagarajan, Nikolaos Papanikolaou, David Williams, *Simulating and Compiling Code for the Sequential Quantum Random Access Machine*, Electronic Notes in Theoretical Computer Science Volume 170, 6 March 2007, Pages 101-124 ([doi:10.1016/j.entcs.2006.12.014](https://doi.org/10.1016/j.entcs.2006.12.014))

* {#Miszczak11} [[Jarosław Adam Miszczak]], *Models of quantum computation and quantum programming languages*, Bull. Pol. Acad. Sci.-Tech. Sci., Vol. 59, No. 3 (2011), pp. 305-324 ([arXiv:1012.6035](https://arxiv.org/abs/1012.6035))

* {#Devitt14} [[Simon J. Devitt]], *Classical Control of Large-Scale Quantum Computers*, In: S. Yamashita, S. Minato  (eds.) *Reversible Computation* Lecture Notes in Computer Science, vol 8507. Springer 2014 ([arXiv:1405.4943](https://arxiv.org/abs/1405.4943), [doi:10.1007/978-3-319-08494-7_3](https://doi.org/10.1007/978-3-319-08494-7_3))

* Jarrod R McClean, Jonathan Romero, Ryan Babbush and Alán Aspuru-Guzik, *The theory of variational hybrid quantum-classical algorithms*, New Journal of Physics, Volume 18, February 2016 ([doi:10.1088/1367-2630/18/2/023023](https://iopscience.iop.org/article/10.1088/1367-2630/18/2/023023))

* Murray Thom (D-Wave), *[Three Truths and the Advent of Hybrid Quantum Computing](https://medium.com/d-wave/three-truths-and-the-advent-of-hybrid-quantum-computing-1941ba46ff8c)*, Jun 25, 2019

Application of classically controlled quantum computation:

* {#KimSwingle17} Isaac H. Kim, [[Brian Swingle]], *Robust entanglement renormalization on a noisy quantum computer* ([arXiv:1711.07500](https://arxiv.org/abs/1711.07500))

  > (in terms of [[holographic entanglement entropy|holographic]] [[tensor network]] states)


* Sukin Sim, Peter D. Johnson, Alan Aspuru-Guzik, *Expressibility and entangling capability of parameterized quantum circuits for hybrid quantum-classical algorithms*, Adv. Quantum Technol. 2 (2019) 1900070 ([arXiv:1905.10876](https://arxiv.org/abs/1905.10876))

* Mateusz Ostaszewski, Edward Grant, Marcello Benedetti, *Structure optimization for parameterized quantum circuits*, Quantum 5, 391 (2021) ([arXiv:1905.09692](https://arxiv.org/abs/1905.09692))


* {#ShaydulinEtAl19} Ruslan Shaydulin et al., *A Hybrid Approach for Solving Optimization Problems on Small Quantum Computers* ([doi:10.1109/MC.2019.2908942](https://doi.ieeecomputersociety.org/10.1109/MC.2019.2908942))

* Eneko Osaba, Esther Villar-Rodriguez, Izaskun Oregi, Aitor Moreno-Fernandez-de-Leceta, *Focusing on the Hybrid Quantum Computing -- Tabu Search Algorithm: new results on the Asymmetric Salesman Problem* ([arXiv:2102.05919](https://arxiv.org/abs/2102.05919))


in particular in [[quantum machine learning]]:

* {#BenedettiLloydSackFiorentini19} Marcello Benedetti, Erika Lloyd, Stefan Sack, Mattia Fiorentini, *Parameterized quantum circuits as machine learning models*, Quantum Science and Technology 4, 043001 (2019) ([arXiv:1906.07682](https://arxiv.org/abs/1906.07682))

* D. Zhu et al. *Training of quantum circuits on a hybrid quantum computer*, Science Advances, 18 Oct 2019: Vol. 5, no. 10, eaaw9918 ([doi: 10.1126/sciadv.aaw9918](https://advances.sciencemag.org/content/5/10/eaaw9918))


* {#MariBromleyIzaacSchuldKilloran20} Andrea Mari, Thomas R. Bromley, Josh Izaac, Maria Schuld, Nathan Killoran,  *Transfer learning in hybrid classical-quantum neural networks*, Quantum 4, 340 (2020) ([arXiv:1912.08278](https://arxiv.org/abs/1912.08278))

* Thomas Hubregtsen, Josef Pichlmeier, Patrick Stecher, Koen Bertels, *Evaluation of Parameterized Quantum Circuits: on the relation between classification accuracy, expressibility and entangling capability*, Quantum Machine Intelligence volume 3, Article number: 9 (2021) ([arXiv:2003.09887](https://arxiv.org/abs/2003.09887), [doi:10.1007/s42484-021-00038-w](https://doi.org/10.1007/s42484-021-00038-w))

* {#TensorFlow} [TensorFlow.org](https://www.tensorflow.org/) (Google), *[Hybrid quantum classical models](https://www.tensorflow.org/quantum/concepts#hybrid_quantum-classical_models)*



### Noisy intermediate-scale quantum computing
 {#ReferencesNISQ}

* Nikolaj Moll et al., *Quantum optimization using variational algorithms on near-term quantum devices*, Quantum Science and Technology, Volume 3, Number 3 2018 ([arXiv:1710.01022](https://arxiv.org/abs/1710.01022))

* {#Preskill18} [[John Preskill]], *Quantum Computing in the NISQ era and beyond*, Quantum  2018-08-06, volume 2, page 79 ([arXiv:1801.00862](https://arxiv.org/abs/1801.00862), [doi:10.22331/q-2018-08-06-79](https://doi.org/10.22331/q-2018-08-06-79))

* Daniel Koch, Brett Martin, Saahil Patel, Laura Wessing, and Paul M. Alsing, *Demonstrating NISQ era challenges in algorithm design on IBM's 20 qubit quantum computer*, AIP Advances 10, 095101 (2020) ([doi:10.1063/5.0015526](https://doi.org/10.1063/5.0015526))

* Frank Leymann, Johanna Barzen, *The bitter truth about gate-based quantum algorithms in the NISQ era*, Quantum Sci. Technol. 5 044007 (2020) ([doi:10.1088/2058-9565/abae7d](https://iopscience.iop.org/article/10.1088/2058-9565/abae7d))


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



### In terms of dagger-compact categories

Discussion in terms of [[finite quantum mechanics in terms of dagger-compact categories]]:

* [[Jamie Vicary]], Section 3 of: _The Topology of Quantum Algorithms_, (LICS 2013) Proceedings of 28th Annual ACM/IEEE Symposium on Logic in Computer Science, pages 93-102 ([arXiv:1209.3917](https://arxiv.org/abs/1209.3917))






### Topological quantum computing

[[topological quantum computation]] is discussed in

* [[Michael Freedman]], [[Alexei Kitaev]], Michael J. Larsen, Zhenghan Wang, _Topological Quantum Computation_ ([arXiv:quant-ph/0101025](http://arxiv.org/abs/quant-ph/0101025))

* Zhenghan Wang, _Topologization of electron liquids with Chern-Simons theory and quantum computation_ ([arXiv:cond-mat/0601285](http://arxiv.org/abs/cond-mat/0601285))

* {#FreedmanLarsenWang00} [[Michael Freedman]], [[Michael Larsen]], [[Zhenghan Wang]], _A modular functor which is universal for quantum computation_, Communications in Mathematical Physics **227** (2002) 605–622 &lbrack;[arXiv:quant-ph/0001108](http://arxiv.org/abs/quant-ph/0001108), [doi:10.1007/s002200200645](https://doi.org/10.1007/s002200200645)&rbrack;

* [[Alexei Kitaev]], _Fault-tolerant quantum computation by anyons_, Annals Phys. 303 (2003) 2-30 ([arXiv:quant-ph/9707021](http://arxiv.org/abs/quant-ph/9707021))


### Relation to tensor networks

Relation to [[tensor networks]], specifically [[matrix product states]]:

* Yiqing Zhou, E. Miles Stoudenmire, Xavier Waintal, _What limits the simulation of quantum computers?_, [arXiv:2002.07730](https://arxiv.org/abs/2002.07730)

### Experimental realization

* Han-Shen Zhong et al. _Quantum computational advantage using photons_, Science 370, n. 6523 (2020) 1460-1463 [doi](https://doi.org/10.1126/science.abe8770)




category: computer science, physics


[[!redirects quantum computing]]
[[!redirects quantum computations]]

[[!redirects quantum computer]]
[[!redirects quantum computers]]


[[!redirects QML]]

[[!redirects classically controlled quantum computation]]
[[!redirects parameterized quantum computation]]



[[!redirects NISQ]]
[[!redirects noisy intermediate-scale quantum computer]]
[[!redirects noisy intermediate-scale quantum computer]]
[[!redirects noisy intermediate-scale quantum computing]]


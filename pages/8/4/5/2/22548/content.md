

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

Shor's algorithm is [[prime factorization]] [[algorithm]] for [[quantum computers]] (cf. *[[quantum algorithm]]*) making crucial use of the *phase estimation* provided by the [[quantum Fourier transform]].

## Related concepts

* [[Grover's algorithm]]

* [[Deutsch-Jozsa algorithm]]

* [[quantum complexity theory]]

* [[quantum supremacy]]

## References
 {#References}

Due to:

* {#Shor97} [[Peter W. Shor]], *Algorithms for quantum computation: discrete logarithms and factoring*,  Proceedings 35th Annual Symposium on Foundations of Computer Science, IEEE Comput. Soc. Press: 124-134 (1994) &lbrack;[doi:10.1109/SFCS.1994.365700](https://doi.org/10.1109/SFCS.1994.365700)&rbrack;

* {#Simon97} [[Daniel R. Simon]], *On the power of quantum computation*, SIAM Journal on Computing **26** 5 (1997) &lbrack;[doi:10.1137/S0097539796298637](https://doi.org/10.1137/S0097539796298637), [pdf](https://courses.cs.washington.edu/courses/cse599/01wi/papers/simon_qc.pdf)&rbrack;

Early review:

* [[Yuri I. Manin]], *Classical computing, quantum computing, and Shor's factoring algorithm*, Astérisque, **266** Séminaire Bourbaki 862 (2000) 375-404 &lbrack;[arXiv:quant-ph/9903008](https://arxiv.org/abs/quant-ph/9903008), [numdam:SB_1998-1999__41__375_0](http://www.numdam.org/item/?id=SB_1998-1999__41__375_0)&rbrack;

Further review:

* [[Daniel Simon]], *[Exploring Simon’s Algorithm with Daniel Simon](https://aws.amazon.com/blogs/quantum-computing/simons-algorithm/)* (Oct 2021)

  > A bit of amusing history: I submitted my algorithm to a theoretical computer science conference (STOC 1993), but it was rejected. However, Peter Shor was on the program committee for that conference, and immediately saw the potential (that I had had absolutely no inkling of, to be honest) for applying the same general algorithm structure to concrete problems like factoring and discrete logarithms. After trying unsuccessfully to persuade the committee to accept my paper, he got to work on his own, and submitted it to the next major theoretical computer science conference (FOCS 1993)—in parallel with mine, resubmitted. We had in fact agreed to merge the papers if only his was accepted, but the committee fortunately agreed to accept them both, giving us each credit for our respective portions of the resulting achievement.”

* Renato Portugal, *Basic Quantum Algorithms* &lbrack;[arXiv:2201.10574](https://arxiv.org/abs/2201.10574)&rbrack;

Textbook account:

* [[Giuliano Benenti]], [[Giulio Casati]], [[Davide Rossini]], Section 3.14 of: *Principles of Quantum Computation and Information*, World Scientific 2018  ([doi:10.1142/10909](https://doi.org/10.1142/10909), [2004 pdf](http://mmrc.amss.cas.cn/tlb/201702/W020170224608149307696.pdf))

Lecture notes:

* [[Scott Aaronson]], Chapters 18-21 of: *Introduction to Quantum Information Science* (2018) &lbrack;[pdf](https://www.scottaaronson.com/qclec.pdf), [webpage](https://www.scottaaronson.com/cs378/)&rbrack;

Formulation in [[Quipper]]:

* Safat Siddiqui, Mohammed Jahirul Islam, Omar Shehab, §4.3, §4.5 in: *Five Quantum Algorithms Using Quipper* &lbrack;[arXiv:1406.4481](https://arxiv.org/abs/1406.4481)&rbrack;


See also: 

* Wikipedia, *[Shor's algorithm](https://en.wikipedia.org/wiki/Shor%27s_algorithm)*

* Wikipedia, *[Simon's problem](https://en.wikipedia.org/wiki/Simon's_problem)*

On compiling Shor's algorithm to [[su(2)-anyon]] [[braid representation|braid]] [[quantum gates]] (i.e. implementation in [[topological quantum computation]]):

* M. Baraban, Nicholas E. Bonesteel, Steven H. Simon, *Resources required for topological quantum factoring*, Phys. Rev. A **81** 062317 (2010) &lbrack;[doi:10.1103/PhysRevA.81.062317](https://doi.org/10.1103/PhysRevA.81.062317), [arXiv:1002.0537](https://arxiv.org/abs/1002.0537)&rbrack;

On (requirements for) actual implementation of Shor's algorithm on a [[quantum computer]]:

* Austin G. Fowler, Lloyd C. L. Hollenberg: *Scalability of Shor’s algorithm with a limited set of rotation gates*, Phys. Rev. A **70** (2007) 032329 &lbrack;[doi:10.1103/PhysRevA.70.032329](https://doi.org/10.1103/PhysRevA.70.032329)&rbrack;

* {#GidneyEkerå21} [[Craig Gidney]], Martin Ekerå, *How to factor 2048 bit RSA integers in 8 hours using 20 million noisy qubits*, Quantum **5** (2021) 433 &lbrack;[doi:10.22331/q-2021-04-15-433](https://doi.org/10.22331/q-2021-04-15-433), [pdf](https://quantum-journal.org/papers/q-2021-04-15-433/pdf/), video:[YT](https://youtu.be/upTipX9yXNg)&rbrack;
  > &lbrack;[p. 2](https://quantum-journal.org/papers/q-2021-04-15-433/pdf#page=2):&rbrack; Although Shor’s algorithms run in polynomial time, and although there has been significant historical work focusing on reducing the cost of Shor’s algorithms and large scale quantum computing architectures, the constant factors hidden by the asymptotic notation remain substantial. These constant factors must be overcome, by heavy optimization at all levels, in order to make the algorithms practical.
  > Current quantum computers are far from being capable of executing Shor’s algorithms for cryptographically relevant problem sizes."

* Dennis Willsch et al.: *The State of Factoring on Quantum Computers* &lbrack;[arXiv:2410.14397](https://arxiv.org/abs/2410.14397)&rbrack;



[[!redirects Shor algorithm]]


[[!redirects Simon's algorithm]]
[[!redirects Simon algorithm]]

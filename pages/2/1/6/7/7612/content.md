+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

### General

A _certification_ or _formal verification_ of a computer program is a formalized guarantee -- a [[proof]] -- that the program has given specified properties.  For instance, it could be guaranteed to compute a given output based on a given input, or to always terminate, or to not include a certain kind of security hole.

Certifications often take the form of a [[formal proof]] (whence "formal methods" [WLBF09](#WLBF09)) that a program, regarded as a [[term]] of some sort (under _[[programs as proofs]]_), has a specified [[type]].  Thus, [[programming languages]] based on highly expressive [[type theories]] (including [[dependent types]]) are a natural place to do certified programming "natively".  Examples are _[[Coq]]_ and _[[Agda]]_. In this case, the program is written at the same time as a proof of its certification.  One often then wants to "extract" the executable code or "ignore" the proof part of the terms when actually running the code, for performance reasons; Coq and Agda include mechanisms designed for this.

It is also possible to write a program in some less strongly typed language and provide an "external" certification for it, rather than one built into the program itself.  Computer proof assistants like [[Coq]] and [[Agda]] are also used for this, using a formal representation of some other programming language.  There are also other program analysis tools which can produce automated proofs of certain aspects of a computer program, such as safety and termination (although of course a *complete* solution to termination-checking is impossible, being the [[halting problem]]).

### Via homotopy type theory

From [Ghani et al. 15](#GhaniEtAl15):

> The cost of software failure is truly staggering. Well known individual cases include the Mars Climate Orbiter failure (&#163;80 million), Ariane Rocket disaster (&#163;350 million), Pentium Chip Division failure (&#163;300 million), and more recently the heartbleed bug (est. &#163;400 million). There are many, many more examples. Even worse,  failures such as one in the Patriot Missile System and another  in the Therac-25 radiation system have cost lives. More generally, a  2008 study by the US government estimated that faulty software costs the US economy &#163;100 billion annually. 

> There are many successful approaches to software verification (testing, model checking etc). One approach is to find mathematical [[proofs]] that guarantees of software correctness. However, the complexity of modern software means that hand-written mathematical proofs can be untrustworthy and this has led to a growing desire for computer-checked proofs of software correctness.  Programming languages and interactive proof systems like [[Coq]], [[Agda]], [[NuPRL]] and Idris have been developed based on a formal system called [[Martin-Löf type theory]]. In these systems, we can not only write programs, but we can also express properties of programs using [[types]], and write programs to express proofs that our programs are correct.

> In this way, both large mathematical [[theorems]] such as the [[four color theorem|Four Colour Theorem]], and large software systems such as the CompCert C compiler have been formally verified. However, in such large projects, the issue of scalability arises: how can we use these systems to build large libraries of verified software in an effective way?

> This is related to the problem of reusability and modularity: a component in a software system should be replaceable by another which behaves the same way even though it may be constructed in a completely different way. That is, we need an "[[identity type|extensional equality]]" which is computationally well behaved (that is, we want to run programs using this equality). Finding such an equality is a fundamental and difficult problem which has remained unresolved for over 40 years.

> {#WeMightHaveASolution} But now it looks like we might have a solution! Fields medalist [[Vladimir Voevodsky]] has come up with a completely different take on the problem by thinking of equalities as paths such as those which occur in one of the most abstract branches of mathematics, namely [[homotopy theory]], leading to [[homotopy type theory|Homotopy Type Theory]] (HoTT). In HoTT, two objects are completely interchangeable if they behave the same way. However, most presentations of HoTT involve [[axioms]] which lack computational justification and, as a result, we do not have programming languages or verification systems based upon HoTT. The goal of our project is to fix that, thereby develop the first of a new breed of HoTT-based programming languages and verification systems, and develop case studies which demonstrate the power of HoTT to programmers and those interested in formal verification.


## Examples

* The [[completion monad]] has been used to produce code for [[real number]] computations with certified approximation bounds. See at _[[completion monad]]_ for more.

(...)

## Related concept

* [[Hoare logic]]


## References

### General

Introduction:

* {#WLBF09} Jim Woodcock, Peter Gorm Larsen, Juan Bicarregui, John Fitzgerald, *Formal methods: Practice and experience*, ACM Computing Surveys **41**  19  (2009) 1–36 &lbrack;[doi:10.1145/1592434.1592436](https://doi.org/10.1145/1592434.1592436)&rbrack;

* Patrick Cousot, Radhia Cousot, *A gentle introduction to formal verification of computer systems by abstract interpretation*, NATO Science for Peace and Security Series - D: Information and Communication Security, **25** Logics and Languages for Reliability and Security (2009)&lbrack;[doi:10.3233/978-1-60750-100-8-1](https://dx.doi.org/10.3233/978-1-60750-100-8-1), [pdf](https://www.di.ens.fr/~cousot/publications.www/CousotCousot-Marktoberdorf-2009.pdf), [[CousotCousot-FormalVerification.pdf:file]]&rbrack;

* [[John Harrison]], *Formal Verification*, Lecture notes Marktoberdorf 2010 &lbrack;[web](https://www.cl.cam.ac.uk/~jrh13/papers/mark10.html), [pdf](https://www.cl.cam.ac.uk/~jrh13/papers/mark10.pdf), [[Harrison-FormalVerification.pdf:file]]&rbrack;

* Catherine Meadows, *Program Verification and Security* ([doi:10.1007/978-1-4419-5906-5_863](https://doi.org/10.1007/978-1-4419-5906-5_863)), In:  Henk C. A. van Tilborg, Sushil Jajodia (ed.) *[Encyclopedia of Cryptography and Security](https://link.springer.com/referencework/10.1007/978-1-4419-5906-5)* Springer (2011)

* {#SpittersKrebbersvdWeegen} [[Bas Spitters]], Robberts Krebbers, Eelis van der Weegen, _From computational analysis to thoughts about analysis in HoTT_, MAP International spring school on formalization of Mathematics (2012) ([pdf](http://www.cs.ru.nl/~spitters/MapSpringSchool.pdf))

See also:

* Wikipedia, *[Formal verification](https://en.wikipedia.org/wiki/Formal_verification)*

Sources listing real-world issues programming issues that might motivate verification of software include

* Thomas Huckle, Tobias Neckel, *Bits and Bugs: A Scientific and Historical Review on Software Failures in Computational Science*, SIAM 2019 ([doi:10.1137/1.9781611975567](https://doi.org/10.1137/1.9781611975567))

* _[Some disasters caused by numerical errors](https://web.archive.org/web/20200117070005/http://ta.twi.tudelft.nl/nw/users/vuik/wi211/disasters.html)_

* Computerworld, *[Top software failures in recent history](https://www.computerworld.com/article/3412197/top-software-failures-in-recent-history.html#slide1)*, Feb 17, 2020

* Wikipedia, _[List of software bugs](https://en.wikipedia.org/wiki/List_of_software_bugs)_


### For cryptography

Software verification for [[cryptography]]:

* [[Mihhail Aizatulin]], Franccois Dupressoir, Andrew D. Gordon, Jan Jürjens, *Verifying Cryptographic Code in C: Some Experience and the Csec Challenge* ([pdf](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/MSR-TR-2011-118.pdf)) 

* [[Mihhail Aizatulin]], Andy Gordon, Jan Jürjens, *Extracting and Verifying Cryptographic Models from C Protocol Code by Symbolic Execution*, CCS '11 Proceedings of the 18th ACM Conference on Computer and Communications Security 2011 ([pdf](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/11/extracting.pdf))

* Matthias Berg, *Formal Verification of Cryptographic Security Proofs*, 2013 ([pdf](https://publikationen.sulb.uni-saarland.de/bitstream/20.500.11880/26584/1/thesis_berg.pdf), [doi:10.22028/D291-26528](http://dx.doi.org/10.22028/D291-26528))

* [[Adam Petcher]], *A Foundational Proof Framework for Cryptography*, 2014 ([pdf](https://dash.harvard.edu/bitstream/handle/1/17463136/PETCHER-DISSERTATION-2015.pdf), [harvard:17463136](https://dash.harvard.edu/handle/1/17463136))

* [[Adam Petcher]], Greg Morrisett, *The Foundational Cryptography Framework*,  In: R. Focardi, A. Myers (eds.) *Principles of Security and Trust* POST 2015. Lecture Notes in Computer Science **9036**, Springer (2015) &lbrack;[doi:10.1007/978-3-662-46666-7_4](https://doi.org/10.1007/978-3-662-46666-7_4)&rbrack;

* Andrew W. Appel, *Verification of a Cryptographic Primitive: SHA-256*, ACM Transactions on Programming Languages and SystemsApril 2015 Article No.: 7 ([doi:10.1145/2701415](https://doi.org/10.1145/2701415), [pdf](https://www.cs.princeton.edu/~appel/papers/verif-sha.pdf))


* Andres Erbsen, Jade Philipoom, Jason Gross, Robert Sloan, [[Adam Chlipala]], *Simple High-Level Code for Cryptographic Arithmetic - With Proofs, Without Compromises*, [2019 IEEE Symposium on Security and Privacy (SP)](https://ieeexplore.ieee.org/xpl/conhome/8826229/proceeding) ([doi:10.1109/SP.2019.00005](https://doi.org/10.1109/SP.2019.00005))

* [[Mihhail Aizatulin]], *Verifying Cryptographic Security Implementations in C Using Automated Model Extraction* ([arXiv:2001.00806](https://arxiv.org/abs/2001.00806))

Verification of [[cryptography]] via [[type theory]]:

* Cédric Fournet, Karthikeyan Bhargavan, Andrew D. Gordon, *Cryptographic Verification by Typing for a Sample Protocol Implementation*, In: Aldini A., Gorrieri R. (eds) Foundations of Security Analysis and Design VI. FOSAD 2011. Lecture Notes in Computer Science, vol 6858. Springer (2011) ([doi:10.1007/978-3-642-23082-0_3]( https://doi.org/10.1007/978-3-642-23082-0_3))

* Cédric Fournet, Markulf Kohlweiss, Pierre-Yves Strub, *Modular code-based cryptographic verification*, CCS '11: Proceedings of the 18th ACM conference on Computer and communications securityOctober 2011 Pages 341–350 ([doi:10.1145/2046707.2046746](https://doi.org/10.1145/2046707.2046746))

### Via Hoare calculus

Program verification via [[Hoare calculus]]:

* {#Hoare69} [[C. A. R. Hoare]], *An axiomatic basis for computer programming*, Communications of the ACM **12** 10 (1969) 576–580 &lbrack;[doi:10.1145/363235.363259](https://doi.org/10.1145/363235.363259)&rbrack;

For [[quantum programming languages]]:

* [Wu (2019)](#Wu2019)


### Via (dependent) type theory
 {#ViaDependentTypeTheoryReferences}

The general idea of verified programming via [[dependent type theory|dependent]] [[type theory]]:

* [[Per Martin-Löf]], *Constructive Mathematics and Computer Programming*, Studies in Logic and the Foundations of Mathematics Volume 104, 1982, Pages 153-175 (<a href="https://doi.org/10.1016/S0049-237X(09)70189-2">doi:10.1016/S0049-237X(09)70189-2</a>)

* {#Streicher93} [[Thomas Streicher]], p. 1-2 of: *Investigations into Intensional Type Theory*, Habilitation Thesis, Darmstadt (1993) &lbrack;[pdf](https://www2.mathematik.tu-darmstadt.de/~streicher/HabilStreicher.pdf), [[Streicher-IntensionalTT.pdf:file]]&rbrack;



Exposition:

* [[Harley Eades]], *Type Theory and Applications*, 2012 ([pdf](https://metatheorem.org/includes/pubs/comp.pdf), [[EadesTypeTheoryAndApplications.pdf:file]])



Software verification via [[dependent type theory]] (such as in [[Coq]] or [[Agda]]):

* [[Adam Chlipala]], *Implementing Certified Programming Language Tools in Dependent Type Theory*, Berkeley (2007) &lbrack;[UCB/EECS-2007-113](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2007/EECS-2007-113.html), [pdf](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2007/EECS-2007-113.pdf),  [web](http://adam.chlipala.net/papers/ChlipalaPhD/)&rbrack;

* [[Adam Chlipala]], _Certified programming with dependent types_, MIT Press 2013 &lbrack;[ISBN:9780262026659 ](https://mitpress.mit.edu/books/certified-programming-dependent-types), [pdf](http://adam.chlipala.net/cpdt/cpdt.pdf),  [book webpage](http://adam.chlipala.net/cpdt/)&rbrack;

* Aleksandar Nanevski, Anindya Banerjee, Deepak Garg, *Dependent Type Theory for Verification of Information Flow and Access Control Policies*,  ACM Transactions on Programming Languages and Systems July 2013 Article No.: 6 ([doi:10.1145/2491522.2491523](https://doi.org/10.1145/2491522.2491523))

On [[Agda]] as a dependently typed certification language:

* [[Aaron Stump]], *Verified Functional Programming in Agda*, Association for Computing Machinery and Morgan & Claypool (2016) &lbrack;[doi:10.1145/2841316](https://doi.org/10.1145/2841316), ISBN:978-1-970001-27-3&rbrack;

#### Application to consensus algorithms

Verification of ([[blockchain]]-like) hashgraph consensus algorithms:

Background:

* Pierre Tholoniat, Vincent Gramoli, *Formal Verification of Blockchain Byzantine Fault Tolerance*, in *Handbook on Blockchain*, Optimization and Its Applications **194**, Springer (2022) &lbrack;[arXiv:1909.07453](https://arxiv.org/abs/1909.07453), [doi:10.1007/978-3-031-07535-3_12](https://doi.org/10.1007/978-3-031-07535-3_12)&rbrack;

* Leemon Baird, Mance Harmon, and Paul Madsen, *Hedera: A Public Hashgraph Network & Governing Council*, (last update 2020) &lbrack;[pdf](https://hedera.com/hh_whitepaper_v2.1-20200815.pdf)&rbrack;


With [[Coq]]:

* [Hedera](https://hedera.com) blog: *[Coq Proof Completed By Carnegie Mellon Professor Confirms Hashgraph Consensus Algorithm Is Asynchronous Byzantine Fault Tolerant](https://hedera.com/blog/coq-proof-completed-by-carnegie-mellon-professor-confirms-hashgraph-consensus-algorithm-is-asynchronous-byzantine-fault-tolerant)* (Oct 2018)

* [Hedera](https://hedera.com) blog: *[Formal Methods: The Importance of Being Fault Tolerant in a World with Bad Actors](https://medium.com/hedera/formal-methods-the-importance-of-being-abft-in-a-world-with-bad-actors-7308a4997fdd)* (2018)

* {#Baird18} Leemon Baird: *Formal Methods: A Deep Dive Using the Coq Proof Assistant -- Hedera18* (2018) &lbrack;video: [YT](https://youtu.be/6q15ytIOE3U?list=RDCMUCIhE4NYpaX9E9SssFnwrjww)&rbrack;

* Matthew Salazar, *Consensus, Blockchain and Proof Assistants* (2018) &lbrack;[pdf](http://matthew-salazar-1.s3.amazonaws.com/static/analyze/pdf/Consensus_Blockchain_and_Proof_Assistants.pdf), [[Salazar-ConsensusProof.pdf:file]]&rbrack;

* Karl Crary, *Formalizing the Hashgraph gossip protocol*, talk at *CyLab Partners Conference* (2019) &lbrack;[pdf](https://www.cylab.cmu.edu/_files/documents/formal-methods-3-kcrary-formalizing-the-hashgraph-gossip-protocol.pdf)&rbrack;

* Karl Crary, *Verifying the Hashgraph Consensus Algorithm* &lbrack;[arXiv:2102.01167](https://arxiv.org/abs/2102.01167), [pdf](https://www.cs.cmu.edu/~crary/papers/2021/hashgraph.pdf)&rbrack;

* Musab A. Alturki, Jing Chen, Victor Luchangco, Brandon Moore, Karl Palmskog, Lucas Peña, Grigore Roşu, *Towards a Verified Model of the Algorand Consensus Protocol in Coq*, Formal Methods. FM 2019 International Workshops. Lecture Notes in Computer Science **12232** (2019) 362-367 &lbrack;[arXiv:1907.05523](https://arxiv.org/abs/1907.05523), [doi:10.1007/978-3-030-54994-7_27](https://doi.org/10.1007/978-3-030-54994-7_27)&rbrack;



With [[Agda]]:

* Harold Carr, Christopher Jenkins, Mark Moir, Victor Cacciari Miraldo, Lisandra Silva, *Towards Formal Verification of HotStuff-based Byzantine Fault Tolerant Consensus in Agda: Extended Version*, in: *NASA Formal Methods: 14th International Symposium, NFM 2022* Proceedings  (2022) 616–635 &lbrack;[doi:10.1007/978-3-031-06773-0_33](https://doi.org/10.1007/978-3-031-06773-0_33), [arXiv:2203.14711](https://arxiv.org/abs/2203.14711)&rbrack;


See also:

* {#SpittersConcordium} [[Bas Spitters]], *[Formal verificaton](https://cs.au.dk/research/centers/concordium/research-areas/formal-verification)* at *[Concordium Blockchain Research Center](https://cs.au.dk/research/centers/concordium/)*

* {#ThomsenSpitters20} Søren Eller Thomsen, [[Bas Spitters]], *Formalizing Nakamoto-Style Proof of Stake* &lbrack;[eprint:2020/917](https://eprint.iacr.org/2020/917)&rbrack;

* *[1st Workshop on Formal Methods for Blockchains](https://sites.google.com/view/fmbc/)*(October 2019)

* [Quantstamp](https://quantstamp.com/) blog: *[Formally Verifying Hedera Hashgraph's Stablecoin Framework](https://quantstamp.com/blog/quantstamp-stablecoin-case-study-formally-verifying-hedera-hashgraphs-stablecoin-framework)* (2020)

* Sudhani Verma; Divakar Yadav; Girish Chandra, *Introduction of Formal Methods in Blockchain Consensus Mechanism and Its Associated Protocols*, IEEE Access **10** (2022) &lbrack;[doi:10.1109/ACCESS.2022.3184799](https://doi.org/10.1109/ACCESS.2022.3184799), [pdf](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9801830)&rbrack;

* [Quantstamp](https://quantstamp.com/) blog: *[Applying lightweight formal methods and SAT solvers to build better blockchain applications](https://quantstamp.com/blog/towards-satisfactory-web3-software-engineering)* (July 2023)


#### Via homotopy type theory

Proposals for verification specifically via [[homotopy type theory]]:

* {#GhaniEtAl15} [[Neil Ghani]], [[Conor McBride]], EPSRC research grant _[Homotopy Type Theory: Programming and Verification](https://gow.epsrc.ukri.org/NGBOViewGrant.aspx?GrantRef=EP/M016951/1)_, 2015 

* [[Klaus Mainzer]], *From Proof Theory to Proof Assistants -- Challenges of Responsible Software and AI*, talk at *[Arbeitstagung Bern-München, ABM Spring 2019](https://cj-xu.github.io/abm19/)* ([pdf](https://cj-xu.github.io/abm19/mainzer.pdf), [[MainzerResponsibleSoftware2019.pdf:file]])

* [[Klaus Mainzer]], *Proof and Computation. Perspectives for Mathematics, Computer Science, and Philosophy*, Chapter 1 in: Klaus Mainzer, Peter Schuster, Helmut Schwichtenberg (eds.), *Proof and Computation II -- From Proof Theory and Univalent Mathematics to Program Extraction and Verification*, World Scientific 2021 ([doi:10.1142/12263](https://doi.org/10.1142/12263))

and here again specifically for [[cryptography]]:

* [[Paventhan Vivekanandan]], *A Homotopical Approach to Cryptography*, talk at [FCS 2018](https://www.andrew.cmu.edu/user/liminjia/events/fcs2018/papers/s33.pdf) ([pdf](https://www.andrew.cmu.edu/user/liminjia/events/fcs2018/papers/s33.pdf), [easychair:GLtQ#](https://easychair.org/smart-slide/slide/GLtQ#)), In: Charles Morisset and Limin Jia (eds.) FCS Informal Proceedings  **[55](http://t-news.cn/Floc2018/FLoC2018-pages/volume55.html)** (2018) 

* [[Paventhan Vivekanandan]], *HoTT-Crypt: A Study in Homotopy Type Theory based on Cryptography*, Kalpa Publications in Computing Volume 9, 2018, Pages 75-90 ([doi:10.29007/tvpp](https://doi.org/10.29007/tvpp), [web slides](https://easychair.org/smart-slide/slide/WSST#), [[VivekanandanHoTTCryptography.pdf:file]])

Explicitly using [[type equivalences]]:

* [[Talia Ringer]], *Proof repair along type equivalences*, §4 in: *Proof Repair*, Univ. Washington (2021) &lbrack;[proquest:2568297410](https://www.proquest.com/docview/2568297410), [video](https://www.youtube.com/watch?v=_BkTrp44uBU)&rbrack;


### For quantum programming languages
 {#ReferencesForQuantumProgrammingLanguages}


First, on the problem of debugging quantum programs, as maybe first highlighted by [VRSAS 2015](#VRSAS15), [Rand (2018)](#Rand18) and [Ying & Feng (2018)](#YingFeng18):

* {#VRSAS15} [[Benoît Valiron]], [[Neil J. Ross]], [[Peter Selinger]], [[D. Scott Alexander]], [[Jonathan M. Smith]], *Programming the quantum future*, Communications of the ACM **58** 8 (2015) 52–61 &lbrack;[doi:10.1145/2699415](https://doi.org/10.1145/2699415), [pdf](https://www.iro.umontreal.ca/~brassard/cours/6155/Langages%20de%20programmation%20quantique/Programming%20the%20Quantum%20Future.pdf),  [web](https://cacm.acm.org/magazines/2015/8/189851-programming-the-quantum-future/abstract), promo vid:[YT](https://youtu.be/mzce69oFdH0?list=PLn0nrSd4xjjbIHhktZoVlZuj2MbrBBC_f)&rbrack;

  > &lbrack;p 6:&rbrack; "In quantum computation, the cost of debugging is likely to be quite high. To begin with, observing a quantum system can change its state. A debugger for a quantum program would therefore necessarily give incomplete information about its state when run on actual quantum hardware. The alternative is to use a quantum simulator for debugging. But this is not practical due to the exponential cost of simulating quantum systems. Moreover, it can be expected that the initial quantum computers will be rare and expensive to run and therefore that the cost of runtime errors in quantum code will initially be much higher than in classical computing. This shifts the cost-benefit analysis for quantum programming toward strong compile-time correctness guarantees, as well as formal specification and verification."

  > (with an eye towards [[Quipper]])


* Andriy Miranskyy, Lei Zhang, Javad Doliskani, *Is Your Quantum Program Bug-Free?*, in *ICSE-NIER '20: Proceedings of the ACM/IEEE 42nd International Conference on Software Engineering: New Ideas and Emerging Results* (2020) 29–32 &lbrack;[arXiv:2001.10870](https://arxiv.org/abs/2001.10870), [doi:10.1145/3377816.3381731](https://doi.org/10.1145/3377816.3381731)&rbrack;

  > "The classical parts of a quantum program can be debugged using traditional methods. The quantum parts, however, can not be treated in the same way because of the properties of a QC -- such as superposition, entanglement, and no-cloning -- which are governed by the laws of quantum mechanics. The purpose of debugging a program is to present the user with human readable, i.e., classical, information about the runtime state of the system. Extracting classical information from a quantum state is done using measurement which is usually a non-unitary operation and results in collapse of the state, and hence an unintended behavior of the program."


On formal verification of [[quantum computing]] with/of [[quantum programming languages]]:

general:

* {#YingFeng18} [[Mingsheng Ying]], [[Yuan Feng]], *Model Checking Quantum Systems --- A Survey* &lbrack;[arXiv:1807.09466](https://arxiv.org/abs/1807.09466)&rbrack;

  > "But to check whether a quantum system satisfies a certain property at a time point, one has to perform a quantum-measurement on the system, which can change the state of the system. This makes studies of the long-term behaviours of quantum systems much harder than that of classical system."

  > "The state spaces of the classical systems that model-checking algorithms can be applied to are usually finite or countably infinite. However, the state spaces of quantum systems are inherently continuous even when they are finite-dimensional. In order to develop algorithms for model-checking quantum systems, we have to exploit some deep mathematical properties of the systems so that it suffices to examine only a finite number of (or at most countably infinitely many) representative elements, e.g. those in an orthonormal basis, of their state spaces."

> (repeated in [Ying & Feng (2021, Sec. 1.3)](#YingFeng21))

* Ji Guan, [[Yuan Feng]], Andrea Turrini, [[Mingsheng Ying]], *Model Checking Applied to Quantum Physics* &lbrack;[arXiv:1902.03218](https://arxiv.org/abs/1902.03218)&rbrack;

* {#YingFeng21} [[Mingsheng Ying]], [[Yuan Feng]], *Model Checking Quantum Systems -- Principles and Algorithms*, Cambridge University Press (2021) &lbrack;[ISBN:9781108484305](https://www.cambridge.org/ae/academic/subjects/computer-science/programming-languages-and-applied-logic/model-checking-quantum-systems-principles-and-algorithms?format=HB)&rbrack;

* [[Christophe Chareton]], [[Sébastien Bardin]], [[Dongho Lee]], [[Benoît Valiron]], Renaud Vilmart, Zhaowei Xu, *Formal Methods for Quantum Programs: A Survey*, in: *Handbook of Formal Analysis and Verification in Cryptography*, CRC (2023) &lbrack;[arXiv:2109.06493](https://arxiv.org/abs/2109.06493), [doi:10.1201/9781003090052](https://doi.org/10.1201/9781003090052)&rbrack;

* Marco Lewis, Sadegh Soudjani, Paolo Zuliani, *Formal Verification of Quantum Programs: Theory, Tools and Challenges* &lbrack;[arXiv:2110.01320](https://arxiv.org/abs/2110.01320)&rbrack;

  > "Verifying programs is especially important in the quantum setting due to how difficult it is to program complex algorithms correctly on resource-constrained and error-prone quantum hardware."

* Carmelo R. Cartiere, *Formal Methods for Quantum Software Engineering*, in: *Quantum Software Engineering*, Springer (2022) &lbrack;[doi:10.1007/978-3-031-05324-5_5](https://doi.org/10.1007/978-3-031-05324-5_5)&rbrack;

  > "The characteristic difficulty in creating pure quantum software is mainly due to the inaccessibility to intermediate states, which makes debugging practically impossible. However, the use of formal methods, which apply rigorous mathematical models to ensure error-free software, can overcome this barrier and enable the production of reliable quantum algorithms and applications right out of the box."


with [[QML]]:

* [[Alexander Green]], *Towards a formally verified functional quantum programming language* (2010) &lbrack;[eprints:11457](http://eprints.nottingham.ac.uk/11457)&rbrack;

with [[QPMC]]:

* [[Yuan Feng]], Ernst Moritz Hahn, Andrea Turrini, Lijun Zhang, *`QPMC`: A Model Checker for Quantum Programs and Protocols*, in *Formal Methods. FM 2015*, Lecture Notes in Computer Science **9109**, Springer (2015)  &lbrack;[doi:10.1007/978-3-319-19249-9_17](https://doi.org/10.1007/978-3-319-19249-9_17)&rbrack;

  > "In practice, however, security analysis of [[quantum cryptography|quantum cryptographic]] protocols is notoriously difficult; for example, the manual proof of BB84 in &lbrack;15&rbrack; contains about 50 pages. It is hard to imagine such an analysis being carried out for more sophisticated quantum protocols. Thus, techniques for automated or semi-automated verification of these protocols will be indispensable."


for [[Quipper]] with [[QPMC]]:

* Linda Anticoli, Carla Piazza, Leonardo Taglialegne, Paolo Zuliani, _Towards Quantum Programs Verification: From Quipper Circuits to QPMC_, In: Devitt S., Lanese I. (eds.) *Reversible Computation. RC 2016*, Lecture Notes in Computer Science **9720** Springer (2016) &lbrack;[arXiv:1708.06312](https://arxiv.org/abs/1708.06312), [doi:10.1007/978-3-319-40578-0_16](https://doi.org/10.1007/978-3-319-40578-0_16)&rbrack;


with [[QWIRE]] (in [[Coq]]):

* [[Robert Rand]], [[Jennifer Paykin]], [[Steve Zdancewic]], *QWIRE Practice: Formal Verification of Quantum Circuits in Coq*, EPTCS 266, 2018, pp. 119-132 ([arXiv:1803.00699](https://arxiv.org/abs/1803.00699))

* {#Rand18} [[Robert Rand]], *Formally Verified Quantum Programming*, UPenn (2018) &lbrack;[ediss:3175](https://repository.upenn.edu/edissertations/3175)&rbrack;

  > &lbrack;p. iv:&rbrack; "We argue that [[quantum programs]] demand [[proof assistant|machine-checkable proofs]] of correctness. We justify this on the basis of the complexity of programs manipulating [[quantum states]], the expense of running [[quantum programs]], and the inapplicability of traditional debugging techniques to programs whose states cannot be examined."

  > &lbrack;p. 3:&rbrack; "Quantum programs are tremendously difficult to understand and implement, almost guaranteeing that they will have bugs. And traditional approaches to debugging will not help us: We cannot set breakpoints and look at our qubits without [[quantum state collapse|collapsing the quantum state]]. Even techniques like unit tests and random testing will be impossible to run on classical machines and too expensive to run on quantum computers – and failed tests are unlikely to be informative"

  > &lbrack;p. 4:&rbrack; "Thesis Statement: *[[quantum programming|Quantum programming]] is not only amenable to [[software verification|formal verification]]: it demands it.*"

  > "The overarching goal of this thesis is to write and verify quantum programs together. Towards that end, we introduce a quantum programming language called [[Qwire]] and embed it inside the [[Coq]] [[proof assistant]]. We give it a [[linear type system]] to ensure that it obeys the laws of [[quantum mechanics]] and a [[denotational semantics]] to prove that programs behave as desired." 



Further development [[SQIR]]:


* [[Kesha Hietala]], [[Robert Rand]], [[Shih-Han Hung]], Xiaodi Wu, [[Michael Hicks]], *A verified optimizer for Quantum circuits*, Proceedings of the ACM on Programming Languages **5** Issue POPL 37 (2021) 1–29 &lbrack;[doi:10.1145/3434318](https://doi.org/10.1145/3434318)&rbrack;

* [[Kesha Hietala]], [[Robert Rand]], [[Shih-Han Hung]], Liyi Li, [[Michael Hicks]], *Proving Quantum Programs Correct*, in *12th International Conference on Interactive Theorem Proving (ITP 2021)*, Leibniz International Proceedings in Informatics (LIPIcs) **193** (2021) &lbrack;[arXiv:2010.01240](https://arxiv.org/abs/2010.01240)&rbrack;

* [[Kesha Hietala]], *A verified software toolchain for quantum programming* (2022) &lbrack;[pdf](https://khieta.github.io/files/drafts/khieta-dissertation.pdf), [blog](https://blog.sigplan.org/2021/06/02/verifying-a-quantum-compiler/)&rbrack;


See also:

* Jaap Boender, Florian Kammüller, Rajagopal Nagarajan, *Formalization of Quantum Protocols using Coq*, EPTCS **195** (2015) 71-83 &lbrack;[doi:10.4204/EPTCS.195.6](https://doi.org/10.4204/EPTCS.195.6), [doi:10.4204/EPTCS.195.6](https://doi.org/10.4204/EPTCS.195.6)&rbrack;

  > (via [[Coq]])


* Wenjun Shi, Qinxiang Cao, Yuxin Deng, Hanru Jiang, [[Yuan Feng]], *Symbolic Reasoning about Quantum Circuits in Coq*, Journal of Computer Science and Technology (JCST), **36** 6 (2021) 1291-1306 $[$[arXiv:2005.11023](https://arxiv.org/abs/2005.11023), [doi:10.1007/s11390-021-1637-9](https://doi.org/10.1007/s11390-021-1637-9)$]$

* [[Mingsheng Ying]], *Model Checking for Verification of Quantum Circuits*, in: *Formal Methods. FM 2021*, Lecture Notes in Computer Science **13047**, Springer (2021) $[$[arXiv:2104.11359](https://arxiv.org/abs/2104.11359), [doi:10.1007/978-3-030-90870-6_2](https://doi.org/10.1007/978-3-030-90870-6_2)$]$

* [[Mingsheng Ying]], Zhengfeng Ji, *Symbolic Verification of Quantum Circuits*,  $[$[arXiv:2010.03032](https://arxiv.org/abs/2010.03032)$]$

* [[Li Zhou]], [[Gilles Barthe]], [[Pierre-Yves Strub]], Junyi Liu, [[Mingsheng Ying]], *CoqQ: Foundational Verification of Quantum Programs*, Proceedings of the ACM on Programming Languages **7** POPL 09 (2023) 29 833–865 &lbrack;[arXiv:2207.11350](https://arxiv.org/abs/2207.11350), [doi:10.1145/3554343]( https://doi.org/10.1145/3554343)&rbrack;

  > (in [[Coq]])

Via [[Hoare logic]]:

* {#Wu2019} Xiaodi Wu, *Toward Automatic Verification of Quantum Programs* (2019) &lbrack;[pdf](https://www.cs.umd.edu/class/fall2019/cmsc657/note/qhoare.pdf)&rbrack;

Projects:

* *[VeriqTAS -- Verification of Quantum Technologies, Applications and Systems](https://veriqtas.cft.edu.pl/index.html)*

See also

* [[Anne Broadbent]], Arthur Mehta, Yuming Zhao, *Quantum delegation with an off-the-shelf device* &lbrack;[arXiv:2304.03448](https://arxiv.org/abs/2304.03448)&rbrack;



### Hardware verification
 {#HardwareVerification}

* J. Pau Roth, *Hardware Verification*,  IEEE Transactions on Computers C **26** 12 (1977) &lbrack;[doi:10.1109/TC.1977.1674795](https://doi.org/10.1109/TC.1977.1674795)&rbrack;

* Paolo Camurati, Paolo Prinetto, *Formal Verification of Hardware Correctness: Introductions and Survey of Current Research*, ComputerVolume **21** 7 (1988)  &lbrack;[doi:10.1109/2.65](https://doi.org/10.1109/2.65), [Computer-doi:10.1109/2.65](https://doi.ieeecomputersociety.org/10.1109/2.65),  [pdf](https://www.cerc.utexas.edu/~jay/fv_surveys/camurati_fvsurvey_computer1988.pdf)&rbrack;

* Aarti Gupta, *Formal Hardware Verification Methods: A survey*, Formal Methods in System Design **1** (1992) 151-238 &lbrack;[doi:10.1007/BF00121125](https://doi.org/10.1007/BF00121125), [pdf](https://link.springer.com/content/pdf/10.1007/978-1-4615-3556-0_2.pdf)&rbrack;

* Sharad Malik, *Hardware Verification: Techniques, Methodology and Solutions*, in *Tools and Algorithms for the Construction and Analysis of Systems. TACAS 2008*, Lecture Notes in Computer Science **4963** &lbrack;[doi:10.1007/978-3-540-78800-3_1](https://doi.org/10.1007/978-3-540-78800-3_1)&rbrack;

See also:

* Wikipedia, *[Hardware verification language](https://en.wikipedia.org/wiki/Hardware_verification_language)*

* Oxford University CS Department: *[Hardware verification](https://www.cs.ox.ac.uk/activities/hardwareverification/)*

On [[hardware verification]] using [[proof assistants]]:

* Mark Aagaard, Miriam Leeser, *A methodology for efficient hardware verification*, Formal Methods in System Design **5** (1994) 95-117 &lbrack;[doi:10.1007/BF01384235](https://doi.org/10.1007/BF01384235)&rbrack;

    

{#QuantumHardwareVerification} On [[hardware verification]] of [[quantum computing]]-[[quantum systems|systems]]:

* [[Martin Kliesch]], [[Ingo Roth]], *Theory of Quantum System Certification*, PRX Quantum **2** (2021) 010201 &lbrack;[doi:10.1103/PRXQuantum.2.010201](https://doi.org/10.1103/PRXQuantum.2.010201), [arXiv:2010.05925](https://arxiv.org/abs/2010.05925)&rbrack;



    


[[!redirects verified software]]
[[!redirects software verification]]
[[!redirects formal software verification]]

[[!redirects program verification]]
[[!redirects formal program verification]]


[[!redirects verified programming]]

[[!redirects certification language]]
[[!redirects certification languages]]

[[!redirects hardware verification]]
[[!redirects hardware verifications]]

[[!redirects formal method]]
[[!redirects formal methods]]


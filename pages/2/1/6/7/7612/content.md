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

A _certification_ or _formal verification_ of a computer program is a formalized guarantee -- a [[proof]] -- that the program has given specified properties.  For instance, it could be guaranteed to compute a given output based on a given input, or to always terminate, or to not include a certain kind of security hole.

Certifications often take the form of a [[proof]] that a program, regarded as a [[term]] of some sort (under _[[programs as proofs]]_), has a specified [[type]].  Thus, [[programming languages]] based on highly expressive [[type theories]] (including [[dependent types]]) are a natural place to do certified programming "natively".  Examples are _[[Coq]]_ and _[[Agda]]_. In this case, the program is written at the same time as a proof of its certification.  One often then wants to "extract" the executable code or "ignore" the proof part of the terms when actually running the code, for performance reasons; Coq and Agda include mechanisms designed for this.

It is also possible to write a program in some less strongly typed language and provide an "external" certification for it, rather than one built into the program itself.  Computer proof assistants like Coq and Agda are also used for this, using a formal representation of some other programming language.  There are also other program analysis tools which can produce automated proofs of certain aspects of a computer program, such as safety and termination (although of course a *complete* solution to termination-checking is impossible, being the [[halting problem]]).

So far, fully certified programming in the type-theoretic sense is largely an academic endeavor, see for instance ([SpittersKrebbersvdWeegen](#SpittersKrebbersvdWeegen)); the tools available at present usually require too much time and effort to be worth the payoff in industry.  As automation progresses, this may change.

From [Ghani et al. 15](#GhaniEtAl15):

> The cost of software failure is truly staggering. Well known individual cases include the Mars Climate Orbiter failure (&#163;80 million), Ariane Rocket disaster (&#163;350 million), Pentium Chip Division failure (&#163;300 million), and more recently the heartbleed bug (est. &#163;400 million). There are many, many more examples. Even worse,  failures such as one in the Patriot Missile System and another  in the Therac-25 radiation system have cost lives. More generally, a  2008 study by the US government estimated that faulty software costs the US economy &#163;100 billion annually. 

> There are many successful approaches to software verification (testing, model checking etc). One approach is to find mathematical [[proofs]] that guarantees of software correctness. However, the complexity of modern software means that hand-written mathematical proofs can be untrustworthy and this has led to a growing desire for computer-checked proofs of software correctness.  Programming languages and interactive proof systems like [[Coq]], [[Agda]], [[NuPRL]] and Idris have been developed based on a formal system called [[Martin-Löf type theory]]. In these systems, we can not only write programs, but we can also express properties of programs using [[types]], and write programs to express proofs that our programs are correct.

> In this way, both large mathematical [[theorems]] such as the [[four color theorem|Four Colour Theorem]], and large software systems such as the CompCert C compiler have been formally verified. However, in such large projects, the issue of scalability arises: how can we use these systems to build large libraries of verified software in an effective way?

> This is related to the problem of reusability and modularity: a component in a software system should be replaceable by another which behaves the same way even though it may be constructed in a completely different way. That is, we need an "[[identity type|extensional equality]]" which is computationally well behaved (that is, we want to run programs using this equality). Finding such an equality is a fundamental and difficult problem which has remained unresolved for over 40 years.

> But now it looks like we might have a solution! Fields medallist [[Vladimir Voevodsky]] has come up with a completely different take on the problem by thinking of equalities as paths such as those which occur in one of the most abstract branches of mathematics, namely [[homotopy theory]], leading to [[homotopy type theory|Homotopy Type Theory]] (HoTT). In HoTT, two objects are completely interchangeable if they behave the same way. However, most presentations of HoTT involve [[axioms]] which lack computational justification and, as a result, we do not have programming languages or verification systems based upon HoTT. The goal of our project is to fix that, thereby develop the first of a new breed of HoTT-based programming languages and verification systems, and develop case studies which demonstrate the power of HoTT to programmers and those interested in formal verification.


## Examples

* The [[completion monad]] has been used to produce code for [[real number]] computations with certified approximation bounds. See at _[[completion monad]]_ for more.

## References

### General

Introduction:

* Patrick Cousot, Radhia Cousot, *A gentle introduction to formal verification of computer systems by abstract interpretation*, NATO Science for Peace and Security Series - D: Information and Communication Security, Volume 25: Logics and Languages for Reliability and Security (2009)([doi:10.3233/978-1-60750-100-8-1](https://dx.doi.org/10.3233/978-1-60750-100-8-1))

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

* [[Adam Petcher]], Greg Morrisett, *The Foundational Cryptography Framework*,  In: R. Focardi, A. Myers (eds.) *Principles of Security and Trust* POST 2015. Lecture Notes in Computer Science, vol 9036. Springer, Berlin, Heidelberg ([doi:10.1007/978-3-662-46666-7_4](https://doi.org/10.1007/978-3-662-46666-7_4))

* Andrew W. Appel, *Verification of a Cryptographic Primitive: SHA-256*, ACM Transactions on Programming Languages and SystemsApril 2015 Article No.: 7 ([doi:10.1145/2701415](https://doi.org/10.1145/2701415), [pdf](https://www.cs.princeton.edu/~appel/papers/verif-sha.pdf))


* Andres Erbsen, Jade Philipoom, Jason Gross, Robert Sloan, [[Adam Chlipala]], *Simple High-Level Code for Cryptographic Arithmetic - With Proofs, Without Compromises*, [2019 IEEE Symposium on Security and Privacy (SP)](https://ieeexplore.ieee.org/xpl/conhome/8826229/proceeding) ([doi:10.1109/SP.2019.00005](https://doi.org/10.1109/SP.2019.00005))

* [[Mihhail Aizatulin]], *Verifying Cryptographic Security Implementations in C Using Automated Model Extraction* ([arXiv:2001.00806](https://arxiv.org/abs/2001.00806))


### Via type theory

Verification of [[cryptography]] via [[type theory]]:

* Cédric Fournet, Karthikeyan Bhargavan, Andrew D. Gordon, *Cryptographic Verification by Typing for a Sample Protocol Implementation*, In: Aldini A., Gorrieri R. (eds) Foundations of Security Analysis and Design VI. FOSAD 2011. Lecture Notes in Computer Science, vol 6858. Springer (2011) ([doi:10.1007/978-3-642-23082-0_3]( https://doi.org/10.1007/978-3-642-23082-0_3))

* Cédric Fournet, Markulf Kohlweiss, Pierre-Yves Strub, *Modular code-based cryptographic verification*, CCS '11: Proceedings of the 18th ACM conference on Computer and communications securityOctober 2011 Pages 341–350 ([doi:10.1145/2046707.2046746](https://doi.org/10.1145/2046707.2046746))

### Via dependent type theory

Software verification via [[dependent type theory]] (such as in [[Coq]]):

* [[Adam Chlipala]], _Implementing Certified Programming Language Tools in Dependent Type Theory_ PhD (2007) ([pdf](http://adam.chlipala.net/papers/ChlipalaPhD/ChlipalaPhD.pdf),  [web](http://adam.chlipala.net/papers/ChlipalaPhD/))

* [[Adam Chlipala]], _Certified programming with dependent types_, MIT Press 2013 ([ISBN:9780262026659 ](https://mitpress.mit.edu/books/certified-programming-dependent-types), [pdf](http://adam.chlipala.net/cpdt/cpdt.pdf),  [book webpage](http://adam.chlipala.net/cpdt/))

* Aleksandar Nanevski, Anindya Banerjee, Deepak Garg, *Dependent Type Theory for Verification of Information Flow and Access Control Policies*,  ACM Transactions on Programming Languages and Systems July 2013 Article No.: 6 ([doi:10.1145/2491522.2491523](https://doi.org/10.1145/2491522.2491523))


### Via homotopy type theory

Proposals for verification specifically via [[homotopy type theory]]:

* {#GhaniEtAl15} [[Neil Ghani]], [[Conor McBride]], EPSRC research grant _[Homotopy Type Theory: Programming and Verification](https://gow.epsrc.ukri.org/NGBOViewGrant.aspx?GrantRef=EP/M016951/1)_, 2015 

* [[Klaus Mainzer]], *From Proof Theory to Proof Assistants -- Challenges of Responsible Software and AI*, talk at *[Arbeitstagung Bern-München, ABM Spring 2019](https://cj-xu.github.io/abm19/)* ([pdf](https://cj-xu.github.io/abm19/mainzer.pdf), [[MainzerResponsibleSoftware2019.pdf:file]])

* [[Klaus Mainzer]], *Proof and Computation. Perspectives for Mathematics, Computer Science, and Philosophy*, Chapter 1 in: Klaus Mainzer, Peter Schuster, Helmut Schwichtenberg (eds.), *Proof and Computation II -- From Proof Theory and Univalent Mathematics to Program Extraction and Verification*, World Scientific 2021 ([doi:10.1142/12263](https://doi.org/10.1142/12263))

and here again specifically for [[cryptography]]:

* [[Paventhan Vivekanandan]], *A Homotopical Approach to Cryptography*, talk at [FCS 2018](https://www.andrew.cmu.edu/user/liminjia/events/fcs2018/papers/s33.pdf) ([pdf](https://www.andrew.cmu.edu/user/liminjia/events/fcs2018/papers/s33.pdf), [easychair:GLtQ#](https://easychair.org/smart-slide/slide/GLtQ#)), In: Charles Morisset and Limin Jia (eds.) FCS Informal Proceedings  **[55](http://t-news.cn/Floc2018/FLoC2018-pages/volume55.html)** (2018) 

* [[Paventhan Vivekanandan]], *HoTT-Crypt: A Study in Homotopy Type Theory based on Cryptography*, Kalpa Publications in Computing Volume 9, 2018, Pages 75-90 ([doi:10.29007/tvpp](https://doi.org/10.29007/tvpp), [web slides](https://easychair.org/smart-slide/slide/WSST#), [[VivekanandanHoTTCryptography.pdf:file]])


### For quantum programming languages

Verification of [[quantum programming languages]] such as [[Quipper]]:

* Linda Anticoli, Carla Piazza, Leonardo Taglialegne, Paolo Zuliani, _Towards Quantum Programs Verification: From Quipper Circuits to QPMC_, In: Devitt S., Lanese I. (eds) Reversible Computation. RC 2016. Lecture Notes in Computer Science, vol 9720. Springer, Cham ([doi:10.1007/978-3-319-40578-0_16](https://doi.org/10.1007/978-3-319-40578-0_16))
 

[[!redirects verified software]]
[[!redirects software verification]]

[[!redirects verified programming]]



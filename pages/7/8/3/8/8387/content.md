
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[program]]. A construction of a [[term]] of some [[type]]. The topic of [[computability theory]].

## Related concepts

* [[computability]]

* [[programs as proofs]]

* [[computational type theory]]

* [[canonical form]]

* [[computational trilogy]]

* [[computational consistency]]

* [[programming language]]

* [[parallel computing]]

* [[distributed computing]]

* [[reversible computation]]

* [[nondeterministic computing]]

* [[quantum computation]], [[computable physics]]

* [[hypercomputation]]

[[!include computable mathematics -- table]]

## References

### General

On the theory of computation and introducing the notion of [[denotational semantics]] of [[programming languages]]:

* [[Dana S. Scott]], *Outline of a mathematical theory of computation*, in: Proceedings of the *Fourth Annual Princeton Conference on Information Sciences and Systems* (1970) 169–176. &lbrack;[pdf](https://ropas.snu.ac.kr/~kwang/520/readings/sco70.pdf), [[Scott-TheoryOfComputation.pdf:file]]&rbrack;

* [[Dana S. Scott]], [[Christopher Strachey]], *Toward a Mathematical Semantics for Computer Languages*, Oxford University Computing Laboratory, Technical Monograph PRG-6 (1971) &lbrack;[pdf](https://www.cs.ox.ac.uk/files/3228/PRG06.pdf), [[ScottStrachey-MathematicalSemantics.pdf:file]]&rbrack;


Textbook accounts:

* [[Michael Sipser]], *Introduction to the Theory Of Computation*, 3rd ed: Cengage Learning (2012) &lbrack;ISBN:978-1-133-18779-0,[pdf](https://www.mog.dog/files/SP2019/Sipser_Introduction.to.the.Theory.of.Computation.3E.pdf), [pdf](https://fuuu.be/polytech/INFOF408/Introduction-To-The-Theory-Of-Computation-Michael-Sipser.pdf)&rbrack;

An account with focus on [[programming languages]]:

* [[Robert Harper]], *[[Practical Foundations for Programming Languages]]*, Cambridge University Press (2016) &lbrack;[ISBN:9781107150300](http://www.cambridge.org/us/academic/subjects/computer-science/programming-languages-and-applied-logic/practical-foundations-programming-languages-2nd-edition?format=HB), [pdf](https://www.cs.cmu.edu/~rwh/pfpl/2nded.pdf)&rbrack;

An account going from classical computation to [[quantum computation]]:

* [[Alexei Y. Kitaev]], A. H. Shen, M. N. Vyalyi, *Classical and Quantum Computation*, Graduate Studies in Mathematics **47** (2002) &lbrack;[doi:10.1090/gsm/047](http://dx.doi.org/10.1090/gsm/047)&rbrack;


\linebreak


### As path lifting
{#ReferencesConceptualizationViaPathLifting}

A conceptualization of computation as something at least close to [[path]]-[[lifting]] and/or as [[functors]] between [[path groupoids]] of [[topological spaces]] (a "semantical mapping" from an "action space" parameterizing the possible computing instructions to a "knowledge space" expressing their executions):

* {#vanLeeuwen15} [[Jan van Leeuwen]], *The Philosophy of Computation*, p. xix-xxx in: Proceedings of *IIT.SRC 2015 -- Student Research Conference* Bratislava (2015) &lbrack;full proceedings: [pdf](http://www2.fiit.stuba.sk/iitsrc/iit-src2015-proceedings.pdf), [web](https://www.fiit.stuba.sk/iit-src2015/proceedings.html?page_id=4340); article: [pdf](https://webspace.science.uu.nl/~leeuw112/Bratislava-2015.pdf); slides: [pdf](https://www.fiit.stuba.sk/buxus/docs/IIT.SRC/2015/iit-src-2015_leeuwen_philosophy-of-computation.pdf)&rbrack;

\begin{imagefromfile}
    "file_name": "vanLeeuwen-Computation.jpg",
    "width": 570,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [van Leeuwen 2015](#vanLeeuwen15))"
\end{imagefromfile}



* {#vanLeeuwenWiedermann15} [[Jan van Leeuwen]], [[Jiří Wiedermann]]: *What is Computation -- An Epistemic Approach*, p. 1-13 in Proceedings of *[SOFSEM 2015](http://www.sofsem.cz/sofsem15/): Theory and Practice of Computer Science*, Lecture Notes in Computer Science **8939**, Springer (2015) &lbrack;[doi:10.1007/978-3-662-46078-8](https://doi.org/10.1007/978-3-662-46078-8), talk slides: [pdf](http://www.sofsem.cz/sofsem15/files/presentations/invited/vanLeeuwenWiedermann.pdf)&rbrack;


* {#vanLeeuwenWiedermann17} [[Jan van Leeuwen]], [[Jiří Wiedermann]]: *Knowledge, Representation and the Dynamics of Computation*, pp. 69-89 in: *Representation and Reality in Humans, Other Living Organisms and Intelligent Machines*, Studies in Applied Philosophy, Epistemology and Rational Ethics **28**, Springer (2017) &lbrack;[doi:10.1007/978-3-319-43784-2_5](https://doi.org/10.1007/978-3-319-43784-2_5), [[LeeuwenWiedermann-Computation.pdf:file]]&rbrack;


\begin{imagefromfile}
    "file_name": "LeeuwenWiedermann-Computation.jpg",
    "width": 570,
    "unit": "px",
    "margin": {
        "top": -30,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "(from [van Leeuwen and Wiedermann 2017](#vanLeeuwenWiedermann17))"
\end{imagefromfile}

* {#vanLeeuwenWiedermann19} [[Jan van Leeuwen]], [[Jiří Wiedermann]], *Understanding Computation -- A General Theory of Computational Processes*, Technical Report UU-CS-2019-012, Utrecht University (2019) &lbrack;[dspace:1874/390075](https://dspace.library.uu.nl/handle/1874/390075), [pdf](http://www.cs.uu.nl/research/techreps/repo/CS-2019/2019-012.pdf), [pdf](https://dspace.library.uu.nl/bitstream/handle/1874/390075/2019_012.pdf?sequence=1&isAllowed=y)&rbrack;


Related discussion for [[quantum computation]], with [[quantum circuits]] regarded as paths:

* [[Paolo Zanardi]], [[Mario Rasetti]], p. 1 of: *Holonomic Quantum Computation*, Phys. Lett. A **264** (1999) 94-99 &lbrack;<a href="https://doi.org/10.1016/S0375-9601(99)00803-8">doi:10.1016/S0375-9601(99)00803-8</a>, [arXiv:quant-ph/9904011](https://arxiv.org/abs/quant-ph/9904011)&rbrack;

* {#NielsenDowlingGuDoherty06} [[Michael A. Nielsen]], [[Mark R. Dowling]], [[Mile Gu]], [[Andrew C. Doherty]], *Quantum Computation as Geometry*, Science, **311** 5764 (2006) 1133-1135 &lbrack;[doi:10.1126/science.1121541](https://doi.org/10.1126/science.1121541), [arXiv:quant-ph/0603161](https://arxiv.org/abs/quant-ph/0603161)&rbrack; 

* [[Mark R. Dowling]], [[Michael A. Nielsen]], *The geometry of quantum computation*, Quantum Information & Computation **8** 10 (2008) 861–899 &lbrack;[doi:10.5555/2016985.2016986](https://dl.acm.org/doi/abs/10.5555/2016985.2016986), [arXiv:quant-ph/0701004](https://arxiv.org/abs/quant-ph/0701004)&rbrack;

* [[David Jaz Myers]], [[Hisham Sati]] [[Urs Schreiber]], §3 in: *[[schreiber:Topological Quantum Gates in Homotopy Type Theory]]* &lbrack;[arXiv:2303.02382](https://arxiv.org/abs/2303.02382)&rbrack;



[[!redirects computations]]

[[!redirects classical computation]]
[[!redirects classical computations]]

[[!redirects computing]]

[[!redirects computer]]
[[!redirects computers]]

[[!redirects classical computer]]
[[!redirects classical computers]]

[[!redirects computational]]


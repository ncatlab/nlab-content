
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
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
La
## Idea

_Quantum computation_ is [[computation]] in terms of [[quantum information theory]], possibly implemented on _quantum computers_, hence on [[physical systems]] for which phenomena of [[quantum mechanics]] are not negligible. In terms of [[computational trinitarianism]] quantum computation is the computation corresponding to (some kind of) [[quantum logic]].

Specifically, _[[topological quantum computation]]_ is (or is meant to be) quantum computation implemented on [[physical systems]] governed by [[topological quantum field theory]], such as [[Chern-Simons theory]]. A prominent example of this is the (fractional) [[quantum Hall effect]] in [[solid state physics]].

There are arguments that a good formal context for quantum computing is (via [[computational trinitarianism]]) [[linear logic]]/[[linear type theory]] (e.g. [Lago-Faffian 12](#LagoFaffian12)). See also at _[[quantum logic]]_.

\linebreak

Any practical quantum computer will be *classically controlled* ([Knill 96](#Knill96), [Ömer 03](#Omer03), [Nagarajan, Papanikolaou & Williams 07](#NagarajanPapanikolaouWilliams07)):


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






## Related entries

* [[Bloch region]], [[quantum operation]]

* [[Grover's algorithm]]

* [[Shor's algorithm]]

* [[quantum error correction]]

* [[quantum information theory]]

* [[quantum circuit]]

* [[quantum logic]], [[linear logic]]

* [[topological quantum computing]]

* [[quantum Hall effect]], [[Chern-Simons theory]].

* [[superoperator]]

* [[computable physics]]

* [[quantum probability]]

## References

### General

The idea of quantum computation was first expressed in:

* Paul Benioff, *The computer as a physical system: A microscopic quantum mechanical Hamiltonian model of computers as represented by Turing machines*, J Stat Phys 22, 563–591 (1980) ([doi:10.1007/BF01011339](https://doi.org/10.1007/BF01011339))

* [[Richard Feynman]], *Simulating physics with computers*,  Int J Theor Phys 21, 467–488 (1982) ([doi:10.1007/BF02650179](https://doi.org/10.1007/BF02650179))

It became a plausible practical possibility with the understanding of [[quantum error correction]] in 

* {#Shor95} [[Peter W. Shor]], *Scheme for reducing decoherence in quantum computer memory*, Phys. Rev. A 52, R2493(R) 1995 ([doi:10.1103/PhysRevA.52.R2493](https://doi.org/10.1103/PhysRevA.52.R2493))

* {#Steane96} [[Andrew M. Steane]], *Error Correcting Codes in Quantum Theory*, Phys. Rev. Lett. 77, 793 1996 ([doi:10.1103/PhysRevLett.77.793](https://doi.org/10.1103/PhysRevLett.77.793))

* {#CalderbankShor96} [[Robert Calderbank]], [[Peter W. Shor]], *Good Quantum Error-Correcting Codes Exist*, Phys. Rev. A, Vol. 54, No. 2, pp. 1098-1106, 1996 ([doi:10.1103/PhysRevA.54.1098](https://doi.org/10.1103/PhysRevA.54.1098))
    
   
Introduction and survey:

* Michael A. Nielsen, Isaac L. Chuang, _Quantum computation and quantum information_, Cambridge University Press 2000 ([[NielsenChuangQuantumComputation.pdf:file]])

* [[Giuliano Benenti]], [[Giulio Casati]], [[Davide Rossini]], *Principles of Quantum Computation and Information*, World Scientific (2004, 2018)  ([doi:10.1142/10909](https://doi.org/10.1142/10909), [2004 pdf](http://mmrc.amss.cas.cn/tlb/201702/W020170224608149307696.pdf))


* [[John Preskill]], *Quantum Computation* lecture notes, since 2004 ([web](http://theory.caltech.edu/~preskill/ph229/))

* [[Jens Eisert]], M. M. Wolf, _Quantum computing_, In: _Handbook of Nature-Inspired and Innovative Computing_, Springer 2006 ([arXiv:quant-ph/0401019](https://arxiv.org/abs/quant-ph/0401019))

* {#Kuperberg05} [[Greg Kuperberg]], _A concise introduction to quantum probability, quantum mechanics, and quantum computation_, 2005 ([pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf))
 
* {#Loceff13} Michael Loceff, _A course in quantum computing_, 2013 ([pdf](https://www.fgamedia.org/faculty/loceff/cs_courses/cs_83a/Intro_to_QC_Vol_1_Loceff.pdf))

* Wikipedia, _[Quantum computation](http://en.wikipedia.org/wiki/Quantum_computation)_

* [[Scott Aaronson]], Lecture notes _Quantum Computing Since Democritus_ 2006 ([web](http://www.scottaaronson.com/democritus/))

* National Academies of Sciences, Engineering, and Medicine, _Quantum Computing: Progress and Prospects_, The National Academies Press 2019 ([doi:10.17226/25196](https://doi.org/10.17226/25196))



[[!include quantum programming languages -- references]]


### Classically controlled quantum computing

* {#Knill96} [[Emanuel Knill]], *Conventions for quantum pseudocode*, 1996 ([LA-UR-96-2724](https://www.osti.gov/biblio/366453-conventions-quantum-pseudocode), [pdf](https://www.osti.gov/servlets/purl/366453))

* {#Omer03} [[Bernhard Ömer]], *Structured Quantum Programming*, 2003/2009 ([pdf](http://www.itp.tuwien.ac.at/~oemer/doc/structquprog.pdf))

* {#NagarajanPapanikolaouWilliams07} Rajagopal Nagarajan, Nikolaos Papanikolaou, David Williams, *Simulating and Compiling Code for the Sequential Quantum Random Access Machine*, Electronic Notes in Theoretical Computer Science Volume 170, 6 March 2007, Pages 101-124 ([doi:10.1016/j.entcs.2006.12.014](https://doi.org/10.1016/j.entcs.2006.12.014))

* {#Miszczak11} [[Jarosław Adam Miszczak]], *Models of quantum computation and quantum programming languages*, Bull. Pol. Acad. Sci.-Tech. Sci., Vol. 59, No. 3 (2011), pp. 305-324 ([arXiv:1012.6035](https://arxiv.org/abs/1012.6035))



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

* [[Michael Freedman]], Michael Larsen, [[Zhenghan Wang]], _A modular functor which is universal for quantum computation_ ([arXiv:quant-ph/0001108](http://arxiv.org/abs/quant-ph/0001108))

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


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

_Quantum computation_ is [[computation]] in terms of [[quantum information theory]], possibly implemented on _quantum computers_, hence on [[physical systems]] for which phenomena of [[quantum mechanics]] are not negligible. In terms of [[computational trinitarianism]] quantum computation is the computation corresponding to (some kind of) [[quantum logic]].

Specifically, _[[topological quantum computation]]_ is (or is meant to be) quantum computation implemented on [[physical systems]] governed by [[topological quantum field theory]], such as [[Chern-Simons theory]]. A prominent example of this is the (fractional) [[quantum Hall effect]] in [[solid state physics]].

There are arguments that a good formal context for quantum computing is (via [[computational trinitarianism]]) [[linear logic]]/[[linear type theory]] (e.g. [Lago-Faffian 12](#LagoFaffian12)). See also at _[[quantum logic]]_.



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

General discussions:

* Michael A. Nielsen, Isaac L. Chuang, _Quantum computation and quantum information_, Cambridge University Press 2000 ([[NielsenChuangQuantumComputation.pdf:file]])

* [[Jens Eisert]], M. M. Wolf, _Quantum computing_, In: _Handbook of Nature-Inspired and Innovative Computing_, Springer 2006 ([arXiv:quant-ph/0401019](https://arxiv.org/abs/quant-ph/0401019))

* {#Kuperberg05} [[Greg Kuperberg]], _A concise introduction to quantum probability, quantum mechanics, and quantum computation_, 2005 ([pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf))
 
* {#Loceff13} Michael Loceff, _A course in quantum computing_, 2013 ([pdf](https://www.fgamedia.org/faculty/loceff/cs_courses/cs_83a/Intro_to_QC_Vol_1_Loceff.pdf))

* Wikipedia, _[Quantum computation](http://en.wikipedia.org/wiki/Quantum_computation)_

* [[Scott Aaronson]], Lecture notes _Quantum Computing Since Democritus_ 2006 ([web](http://www.scottaaronson.com/democritus/))

* National Academies of Sciences, Engineering, and Medicine, _Quantum Computing: Progress and Prospects_, The National Academies Press 2019 ([doi:10.17226/25196](https://doi.org/10.17226/25196))


### Quantum programming languages

[[quantum programming languages]]:

* Simon Gay, _Quantum  programming languages: Survey and bibliography, Mathematical Structures in Computer Science16(2006) ([doi](https://doi.org/10.1017/S0960129506005378),  [pdf](http://www.dcs.gla.ac.uk/~simon/publications/QPLsurvey.pdf))


[[functional programming languages]] for [[quantum computation]]:


[[QPL]]:

* {#Selinger04} [[Peter Selinger]], _Towards a quantum programming language_, Mathematical Structures in Computer Science 14(4):527–586, 2004 ([doi:10.1017/S0960129504004256](https://doi.org/10.1017/S0960129504004256), [pdf](https://www.mathstat.dal.ca/~selinger/papers/qpl.pdf),  [web](https://www.mathstat.dal.ca/~selinger/papers.html#qpl))

* [[Peter Selinger]], _The Quipper Language_ ([web](http://www.mathstat.dal.ca/~selinger/quipper/))


[[QML]]:

* {#AltenkirchGrattage05} [[Thorsten Altenkirch]], [[Jonathan Grattage]], _A functional quantum programming language_, Logic in Computer Science, 2005. Proceedings. 20th Annual IEEE Symposium on, 26-29 June 2005 Page(s):249 - 258 ([arXiv:quant-ph/0409065](https://arxiv.org/abs/quant-ph/0409065), [doi:https://doi.org/10.1109/LICS.2005.1](https://doi.org/10.1109/LICS.2005.1), [pdf](http://www.cs.nott.ac.uk/~txa/publ/qml.pdf))

* [[Jonathan Grattage]], _An overview of QML with a concrete implementation in Haskell_, Quantum Physics and Logic 2008 ([arXiv:0806.2735](https://arxiv.org/abs/0806.2735))


### Quantum programming via monads
 {#ReferencesInTermsOfMonads}

Discussion of aspects of quantum programming in terms of [[monad (in computer science)|monads]] in [[functional programming]] are in 

* [[Thorsten Altenkirch]], Alexander Green, _The quantum IO monad_, in _Semantic Techniques in Quantum Computation_, January 2009, appeared in 2010 ([pdf](http://www.cs.nott.ac.uk/~txa/publ/qio-chapter.pdf), [talk slides](http://www.cs.nott.ac.uk/~txa/talks/qnet06.pdf))


* J. K. Vizzotto, [[Thorsten Altenkirch]], A. Sabry, _Structuring quantum effects: superoperators as arrows_ ([arXiv:quant-ph/0501151](http://arxiv.org/abs/quant-ph/0501151))



### In terms of dagger-compact categories

Discussion in terms of [[finite quantum mechanics in terms of dagger-compact categories]]:

* [[Jamie Vicary]], Section 3 of: _The Topology of Quantum Algorithms_, (LICS 2013) Proceedings of 28th Annual ACM/IEEE Symposium on Logic in Computer Science, pages 93-102 ([arXiv:1209.3917](https://arxiv.org/abs/1209.3917))


### As linear logic
 {#ReferencesAsLinearLogic}

Discussion of quantum computation as the [[internal logic|internal]] [[linear logic]]/[[linear type theory]] of [[compact closed categories]] is in

* {#AbramskyDuncan05} [[Samson Abramsky]], [[Ross Duncan]], _A Categorical Quantum Logic_, Mathematical Structures in Computer Science, 2006 ([arXiv:quant-ph/0512114](http://arxiv.org/abs/quant-ph/0512114))
 

* {#Duncan06} [[Ross Duncan]], _Types for quantum mechanics_, 2006 ([pdf](http://personal.strath.ac.uk/ross.duncan/papers/rduncan-thesis.pdf), [slides](http://www.cs.ox.ac.uk/people/ross.duncan/talks/2005/pps-22-05-2005.pdf))
 

* {#LagoFaffian12} [[Ugo Dal Lago]], Claudia Faggian, _On Multiplicative Linear Logic, Modality and Quantum Circuits_ ([arXiv:1210.0613](http://arxiv.org/abs/1210.0613))
 

An exposition along these lines is in

* [[John Baez]], [[Mike Stay]], _Physics, topology, logic and computation: a rosetta stone_, [arxiv/0903.0340](http://arxiv.org/abs/0903.0340); in "New Structures for Physics", ed. Bob Coecke, Lecture Notes in Physics __813__, Springer, Berlin, 2011, pp. 95-174




### Topological quantum computing

[[topological quantum computation]] is discussed in

* [[Michael Freedman]], [[Alexei Kitaev]], Michael J. Larsen, Zhenghan Wang, _Topological Quantum Computation_ ([arXiv:quant-ph/0101025](http://arxiv.org/abs/quant-ph/0101025))

* Zhenghan Wang, _Topologization of electron liquids with Chern-Simons theory and quantum computation_ ([arXiv:cond-mat/0601285](http://arxiv.org/abs/cond-mat/0601285))

* [[Michael Freedman]], Michael Larsen, [[Zhenghan Wang]], _A modular functor which is universal for quantum computation_ ([arXiv:quant-ph/0001108](http://arxiv.org/abs/quant-ph/0001108))

* [[Alexei Kitaev]], _Fault-tolerant quantum computation by anyons_, Annals Phys. 303 (2003) 2-30 ([arXiv:quant-ph/9707021](http://arxiv.org/abs/quant-ph/9707021))


### Relation to tensor networks

Relation to [[tensor networks]], specifically [[matrix product states]]:

* Yiqing Zhou, E. Miles Stoudenmire, Xavier Waintal, _What limits the simulation of quantum computers?_, [arXiv:2002.07730](https://arxiv.org/abs/2002.07730)

### Experimental achievements

* Han-Shen Zhong et al. _Quantum computational advantage using photons_, Science 370, n. 6523 (2020) 1460-1463 [doi](https://doi.org/10.1126/science.abe8770)

category: computer science, physics

[[!redirects quantum computing]]
[[!redirects quantum computations]]

[[!redirects quantum computer]]
[[!redirects quantum computers]]



[[!redirects QML]]

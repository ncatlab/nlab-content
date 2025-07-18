
### Quantum programming languages

The first proposal towards formalizing quantum programming languages was:

* {#Knill96} [[Emanuel Knill]], *Conventions for quantum pseudocode*, Los Alamos Technical Report (1996) $[$[LA-UR-96-2724](https://www.osti.gov/biblio/366453-conventions-quantum-pseudocode), [doi:10.2172/366453](https://doi.org/10.2172/366453), [pdf](https://www.osti.gov/servlets/purl/366453), [[Knill-QuantumPseudocode.pdf:file]]$]$

and early formalization via [[quantum lambda-calculus]] invoking [[linear logic]]/[[linear type theory|linear types]] (cf. [Pratt 1992](#Pratt92) etc.):

* [[Benoît Valiron]], *A functional programming language for quantum computation with classical control*, MSc thesis, University of Ottawa (2004) $[$[doi:10.20381/ruor-18372](http://dx.doi.org/10.20381/ruor-18372), [pdf](https://ruor.uottawa.ca/bitstream/10393/26790/1/MR01625.PDF)$]$

* {#SelingerValiron04} [[Peter Selinger]], [[Benoît Valiron]], *A lambda calculus for quantum computation with classical control*, Proc. of TLCA 2005 $[$[arXiv:cs/0404056](https://arxiv.org/abs/cs/0404056), [doi:10.1007/11417170_26](https://doi.org/10.1007/11417170_26)$]$

* {#SelingerValiron09} [[Peter Selinger]], [[Benoît Valiron]], *Quantum Lambda Calculus*, in: *Semantic Techniques in Quantum Computation*, Cambridge University Press (2009) 135-172 $[$[doi:10.1017/CBO9781139193313.005](https://doi.org/10.1017/CBO9781139193313.005), [pdf](https://www.mscs.dal.ca/~selinger/papers/qlambdabook.pdf)$]$

> &lbrack;[Selinger (2016)](Quipper#Selinger16):&rbrack; When the [QPL workshop series](https://www.mathstat.dal.ca/~selinger/qpl/) was first founded, it was called "*Quantum Programming Languages*". One year I wasn't participating, and while I wasn't looking they changed the name to "*Quantum Physics and Logic*" --- same acronym! 

> Back in those days in the early 21st century we were actually trying to do programming languages for quantum computing $[$[Selinger & Valiron 2004](#SelingerValiron04)$]$, but the sad thing is: In those days nobody really cared. $[...]$

> Now it's 15 years later and several of these parameters have changed: There has been a renewed interest, from government agencies and also from companies who are actually building quantum computers. $[...]$.

> So now people are working on quantum programming languages *again*.

Exposition of the general idea of [[quantum programming languages]] for [[classically controlled quantum computation]] with an eye towards the [[Quipper]]-language:

* [[Benoît Valiron]], [[Neil J. Ross]], [[Peter Selinger]], [[D. Scott Alexander]], [[Jonathan M. Smith]], *Programming the quantum future*, Communications of the ACM **58** 8 (2015) 52–61 $[$[doi:10.1145/2699415](https://doi.org/10.1145/2699415), [pdf](https://www.iro.umontreal.ca/~brassard/cours/6155/Langages%20de%20programmation%20quantique/Programming%20the%20Quantum%20Future.pdf),  [web](https://cacm.acm.org/magazines/2015/8/189851-programming-the-quantum-future/abstract), promo vid:[YT](https://youtu.be/mzce69oFdH0?list=PLn0nrSd4xjjbIHhktZoVlZuj2MbrBBC_f)$]$


On [[quantum programming languages]] ([[programming languages]] for [[quantum computation]]):

General:

* [[Jarosław Adam Miszczak]], *Models of quantum computation and quantum programming languages*, Bull. Pol. Acad. Sci.-Tech. Sci., Vol. 59, No. 3 (2011), pp. 305-324 ([arXiv:1012.6035](https://arxiv.org/abs/1012.6035))

* {#Miszczak12} [[Jarosław Adam Miszczak]], *High-level Structures for Quantum Computing*, Morgan&Claypool 2012 ([doi:10.2200/S00422ED1V01Y201205QMC006](https://doi.org/10.2200/S00422ED1V01Y201205QMC006), [pdf](https://www.morganclaypool.com/doi/pdf/10.2200/S00422ED1V01Y201205QMC006))



See also:

* Wikipedia, _[Quantum programming](https://en.wikipedia.org/wiki/Quantum_programming)_

Surveys of existing languages:

* Simon Gay, _Quantum  programming languages: Survey and bibliography_, Mathematical Structures in Computer Science16(2006) ([doi:10.1017/S0960129506005378](https://doi.org/10.1017/S0960129506005378),  [pdf](http://www.dcs.gla.ac.uk/~simon/publications/QPLsurvey.pdf))

* Sunita Garhwal, Maryam Ghorani , Amir Ahmad, *Quantum Programming Language: A Systematic Review of Research Topic and Top Cited Languages*,  Arch Computat Methods Eng 28, 289–310 (2021) ([doi:10.1007/s11831-019-09372-6](https://doi.org/10.1007/s11831-019-09372-6))

* B. Heim et al., *Quantum programming languages*, Nat Rev Phys **2** (2020) 709–722 $[$[doi:10.1038/s42254-020-00245-7](https://doi.org/10.1038/s42254-020-00245-7)$]$


Quantum programming via [[quantum logic]] understood as [[linear type theory]] [[categorical semantics|interpreted in]] [[symmetric monoidal categories]]:

* {#Pratt92} [[Vaughan Pratt]], *Linear logic for generalized quantum mechanics*, in Proc. of *[Workshop on Physics and Computation (PhysComp'92)](https://www.computer.org/csdl/proceedings/phycmp/1992/12OmNx19jVS)*, Dallas (1992) $[$[pdf](http://boole.stanford.edu/pub/ql.pdf), [[Pratt-LinearLogic.pdf:file]], [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.137.7817)$]$

* {#AbramskyCoecke04} [[Samson Abramsky]], [[Bob Coecke]], _A categorical semantics of quantum protocols_ , Proceedings of the 19th IEEE conference on Logic in Computer Science (LiCS'04). IEEE Computer Science Press (2004) ([arXiv:quant-ph/0402130](http://arxiv.org/abs/quant-ph/0402130))

* {#AbramskyDuncan05} [[Samson Abramsky]], [[Ross Duncan]], _A Categorical Quantum Logic_, Mathematical Structures in Computer Science, **16** 3 (2006) 469-489  $[$[arXiv:quant-ph/0512114](http://arxiv.org/abs/quant-ph/0512114), [doi:10.1017/S0960129506005275](https://doi.org/10.1017/S0960129506005275)$]$

* {#Duncan06} [[Ross Duncan]], *Types for Quantum Computing*, (2006) $[$[pdf](http://personal.strath.ac.uk/ross.duncan/papers/rduncan-thesis.pdf)$]$

* {#LagoFaggian12} [[Ugo Dal Lago]], [[Claudia Faggian]], _On Multiplicative Linear Logic, Modality and Quantum Circuits_, EPTCS 95 (2012) 55-66 $[$[arXiv:1210.0613](http://arxiv.org/abs/1210.0613), [doi:10.4204/EPTCS.95.6](https://doi.org/10.4204/EPTCS.95.6)$]$

* {#Staton15} [[Sam Staton]], *Algebraic Effects, Linearity, and Quantum Programming Languages*, POPL '15: Proceedings of the 42nd Annual ACM SIGPLAN-SIGACT Symposium on Principles of Programming Languages (2015) $[$[doi:10.1145/2676726.2676999](https://doi.org/10.1145/2676726.2676999), [pdf](http://www.cs.ox.ac.uk/people/samuel.staton/papers/popl2015.pdf)$]$

  > "A [[quantum programming]] language captures the ideas of [[quantum computation]] in a [[linear type theory]]."

The corresponding [[string diagrams]] are known in quantum computation as *[[quantum circuit diagrams]]*:

* [[Giuliano Benenti]], [[Giulio Casati]], [[Davide Rossini]], Chapter 3 of: *Principles of Quantum Computation and Information*, World Scientific 2018  ([doi:10.1142/10909](https://doi.org/10.1142/10909), [2004 pdf](http://mmrc.amss.cas.cn/tlb/201702/W020170224608149307696.pdf))

* [Miszczak 12, Sec. 4.3](#Miszczak12)



[[type theory|Typed]]$\;$[[functional programming languages]] for [[quantum computation]]:


**[[QPL]]:**

* {#Selinger04} [[Peter Selinger]], _Towards a quantum programming language_, Mathematical Structures in Computer Science **14** 4 (2004) 527–586 $[$[doi:10.1017/S0960129504004256](https://doi.org/10.1017/S0960129504004256), [pdf](https://www.mathstat.dal.ca/~selinger/papers/qpl.pdf),  [web](https://www.mathstat.dal.ca/~selinger/papers.html#qpl)$]$



**[[QML]]:**

* {#AltenkirchGrattage05} [[Thorsten Altenkirch]], [[Jonathan Grattage]], _A functional quantum programming language_, Logic in Computer Science, 2005. Proceedings. 20th Annual IEEE Symposium on, 26-29 June 2005 Page(s):249 - 258 ([arXiv:quant-ph/0409065](https://arxiv.org/abs/quant-ph/0409065), [doi:10.1109/LICS.2005.1](https://doi.org/10.1109/LICS.2005.1), [pdf](http://www.cs.nott.ac.uk/~txa/publ/qml.pdf))

* [[Jonathan Grattage]], _An overview of QML with a concrete implementation in Haskell_, talk at *Quantum Physics and Logic 2008*, ENTCS: Proceedings of QPL V - DCV IV, 157-165, Reykjavik, Iceland, 2008 ([arXiv:0806.2735](https://arxiv.org/abs/0806.2735))


**[[quantum IO monad]]:**

* {#AltenkirchGreen10} [[Thorsten Altenkirch]], [[Alexander Green]], *The quantum IO monad*, Ch. 5 of: Simon Gay, Ian Mackie (eds.): *Semantic Techniques in Quantum Computation* (2010) 173-205 $[$[pdf](http://www.cs.nott.ac.uk/~txa/publ/qio-chapter.pdf), [doi:10.1017/CBO9781139193313.006](https://doi.org/10.1017/CBO9781139193313.006)$]$


**[[Quipper]]:**

* [[Peter Selinger]], _The Quipper Language_ ([web](http://www.mathstat.dal.ca/~selinger/quipper/))

* {#GLRSV13} [[Alexander Green]], [[Peter LeFanu Lumsdaine]], [[Neil Ross]], [[Peter Selinger]], [[Benoît Valiron]], _Quipper: A Scalable Quantum Programming Language_, ACM SIGPLAN Notices **48** 6  (2013) 333-342 $[$[arXiv:1304.3390](https://arxiv.org/abs/1304.3390)$]$

* [[Alexander Green]], [[Peter LeFanu Lumsdaine]], [[Neil Ross]], [[Peter Selinger]], [[Benoît Valiron]], _An Introduction to Quantum Programming in Quipper_, Lecture Notes in Computer Science 7948:110-124, Springer, 2013 ([arXiv:1304.5485](https://arxiv.org/abs/1304.5485))

* [[Jonathan Smith]], [[Neil Ross]], [[Peter Selinger]], [[Benoît Valiron]], _Quipper: Concrete Resource Estimation in Quantum Algorithms_, QAPL 2014 ([arXiv:1412.0625](https://arxiv.org/abs/1412.0625))

* Francisco Rios, [[Peter Selinger]], _A Categorical Model for a Quantum Circuit Description Language_, EPTCS 266, 2018, pp. 164-178 ([arXiv:1706.02630](https://arxiv.org/abs/1706.02630))



**[[QWIRE]]:**

* {#PaykinRandZdancewic17} [[Jennifer Paykin]], [[Robert Rand]], [[Steve Zdancewic]], *QWIRE: a core language for quantum circuits*, POPL 2017: Proceedings of the 44th ACM SIGPLAN Symposium on Principles of Programming Languages (2017) 846–858 ([doi:10.1145/3009837.3009894](https://doi.org/10.1145/3009837.3009894))

  (using the [[exponential modality]] between [[linear type theory]] and [[intuitionistic type theory]])

* [[Jennifer Paykin]], *Linear/non-Linear Types For Embedded Domain-Specific Languages*, 2018 ([upenn:2752](https://repository.upenn.edu/edissertations/2752))

* {#PaykinZdancewic19} [[Jennifer Paykin]], [[Steve Zdancewic]], *A HoTT Quantum Equational Theory*, [talk at QPL2019](http://qpl2019.org/a-hott-quantum-equational-theory/) $[$[arXiv:1904.04371](https://arxiv.org/abs/1904.04371), talk slides: [pdf](https://jpaykin.github.io/talks/HoTT-3-8-2019.pdf), [[PaykinZdancewic-HoTTQuantum.pdf:file]]$]$

  > (using ambient [[homotopy type theory]])


**[[CoqQ]]:**

* {#YingEtAl22} [[Li Zhou]], [[Gilles Barthe]], Pierre-Yves Strub, Junyi Liu, [[Mingsheng Ying]], *CoqQ: Foundational Verification of Quantum Programs* $[$[arXiv:2207.11350](https://arxiv.org/abs/2207.11350)$]$


\linebreak


On [[Q Sharp]]:

*  Kartik Singhal, Kesha Hietala, Sarah Marshall, Robert Rand, *Q# as a Quantum Algorithmic Language*, Proceedings of *Quantum Physics and Logic* (2022) $[$[arXiv:2206.03532](https://arxiv.org/abs/2206.03532)$]$


On [[classically controlled quantum computation]]:

* [[Bernhard Ömer]], *Structured Quantum Programming*, 2003/2009 ([pdf](http://www.itp.tuwien.ac.at/~oemer/doc/structquprog.pdf))



Quantum programming via [[dependent linear type theory]]/[[indexed monoidal (∞,1)-categories]]:

* {#Schreiber14} [[Urs Schreiber]], _Quantization via Linear Homotopy Types_ ([arXiv:1402.7041](http://arxiv.org/abs/1402.7041))

* {#FKS20} [[Peng Fu]], [[Kohei Kishida]], [[Peter Selinger]], _Linear Dependent Type Theory for Quantum Programming Languages_, LICS '20: Proceedings of the 35th Annual ACM/IEEE Symposium on Logic in Computer ScienceJuly 2020 Pages 440–453 ([arXiv:2004.13472](https://arxiv.org/abs/2004.13472), [doi:10.1145/3373718.3394765](https://dl.acm.org/doi/10.1145/3373718.3394765), [pdf](https://depend.cs.uni-saarland.de/lics-icalp/papers/B5.F), [video](https://www.youtube.com/watch?v=GUT8j4V6Nzg))



specifically with [[Quipper]]:

* {#FKRS20} [[Peng Fu]], [[Kohei Kishida]], [[Neil Ross]], [[Peter Selinger]],  _A Tutorial Introduction to Quantum Circuit Programming in Dependently Typed Proto-Quipper_, in I. Lanese, M. Rawski  (eds.) _Reversible Computation_ RC 2020. Lecture Notes in Computer Science, vol 12227 ([arXiv:2005.08396](https://arxiv.org/abs/2005.08396), [doi:10.1007/978-3-030-52482-1_9](https://doi.org/10.1007/978-3-030-52482-1_9))

See also [QS](https://ncatlab.org/schreiber/show/QS).

On quantum **software engineering**:

* Manuel A. Serrano, Ricardo Pérez-Castillo, Mario Piattini, *Quantum Software Engineering*, Springer (2022) $[$[doi:10.1007/978-3-031-05324-5](https://doi.org/10.1007/978-3-031-05324-5)$]$

On **[[software verification]]**:

with [[QWIRE]]:

* [[Robert Rand]], [[Jennifer Paykin]], [[Steve Zdancewic]], *QWIRE Practice: Formal Verification of Quantum Circuits in Coq*, EPTCS 266, 2018, pp. 119-132 ([arXiv:1803.00699](https://arxiv.org/abs/1803.00699))

* [[Robert Rand]], [[Jennifer Paykin]], Dong-Ho Lee, [[Steve Zdancewic]], *ReQWIRE: Reasoning about Reversible Quantum Circuits*, EPTCS **287** (2019) 299-312 $[$[arXiv:1901.10118](https://arxiv.org/abs/1901.10118), [doi:10.4204/EPTCS.287.17](https://doi.org/10.4204/EPTCS.287.17)$]$

for [[Quipper]] with [[QPMC]]:

* Linda Anticoli, Carla Piazza, Leonardo Taglialegne, Paolo Zuliani, _Towards Quantum Programs Verification: From Quipper Circuits to QPMC_, In: Devitt S., Lanese I. (eds.) *Reversible Computation. RC 2016*, Lecture Notes in Computer Science **9720** Springer (2016) $[$[arXiv:1708.06312](https://arxiv.org/abs/1708.06312), [doi:10.1007/978-3-319-40578-0_16](https://doi.org/10.1007/978-3-319-40578-0_16)$]$

with [[CoqQ]]: [Ying et al. (2022)](#YingEtAl22)

with [[QBricks]]:

* [[Christophe Chareton]], [[Sébastien Bardin]], [[François Bobot]], [[Valentin Perrelle]], [[Benoit Valiron]]: *A Deductive Verification Framework for Circuit-building Quantum Programs*, in: *Programming Languages and Systems. ESOP 2021*, Lecture Notes in Computer Science **12648**, Springer (2021)  \[<a href="https://doi.org/10.1007/978-3-030-72019-3_6">doi:10.1007/978-3-030-72019-3_6</a>, [arXiv:2003.05841](https://arxiv.org/abs/2003.05841), [pdf](https://github.com/Qbricks/qbricks.github.io/files/6414263/final--ESOP-2021.pdf)\]






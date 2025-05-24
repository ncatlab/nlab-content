
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

_Quipper_ is a [[functional programming language|functional]] [[quantum programming language]], specifically a [[domain specific programming language]] for [[quantum circuits]] which is [[domain specific embedded programming language|embedded]] into [[Haskell]]. As such it is similar to *[[QWIRE]]*.

## Related concepts

* [[QML]]

* [[QPL]]

* [[QWIRE]]

* [[QBricks]]

* [[CoqQ]]

* [[quantum programming language]]

## References
 {#References}


Quipper landing page:

* [www.mathstat.dal.ca/~selinger/quipper](http://www.mathstat.dal.ca/~selinger/quipper)


### Precursors

Quipper has grown out of developments initiated in

* {#Selinger04} [[Peter Selinger]], _Towards a quantum programming language_, Mathematical Structures in Computer Science **14** 4 (2004) 527–586 &lbrack;[doi:10.1017/S0960129504004256](https://doi.org/10.1017/S0960129504004256), [pdf](https://www.mathstat.dal.ca/~selinger/papers/qpl.pdf),  [web](https://www.mathstat.dal.ca/~selinger/papers.html#qpl)&rbrack;

and specifically the [[quantum lambda-calculus]] of:

* [[Benoît Valiron]], *A functional programming language for quantum computation with classical control*, MSc thesis, University of Ottawa (2004) &lbrack;[doi:10.20381/ruor-18372](http://dx.doi.org/10.20381/ruor-18372), [pdf](https://ruor.uottawa.ca/bitstream/10393/26790/1/MR01625.PDF)&rbrack;

* {#SelingerValiron04} [[Peter Selinger]], [[Benoît Valiron]], *A lambda calculus for quantum computation with classical control*, Proc. of TLCA 2005 &lbrack;[arXiv:cs/0404056](https://arxiv.org/abs/cs/0404056), [doi:10.1007/11417170_26](https://doi.org/10.1007/11417170_26)&rbrack;

* {#SelingerValiron09} [[Peter Selinger]], [[Benoît Valiron]], *Quantum Lambda Calculus*, in: *Semantic Techniques in Quantum Computation*, Cambridge University Press (2009) 135-172 &lbrack;[doi:10.1017/CBO9781139193313.005](https://doi.org/10.1017/CBO9781139193313.005), [pdf](https://www.mscs.dal.ca/~selinger/papers/qlambdabook.pdf)&rbrack;

> &lbrack;[Selinger (2016)](Quipper#Selinger16):&rbrack; When the [QPL workshop series](https://www.mathstat.dal.ca/~selinger/qpl/) was first founded, it was called "*Quantum Programming Languages*". One year I wasn't participating, and while I wasn't looking they changed the name to "*Quantum Physics and Logic*" --- same acronym! 

> Back in those days in the early 21st century we were actually trying to do programming languages for quantum computing $[$[Selinger & Valiron 2004](#SelingerValiron04)$]$, but the sad thing is: In those days nobody really cared. $[...]$

> Now it's 15 years later and several of these parameters have changed: There has been a renewed interest, from government agencies and also from companies who are actually building quantum computers. $[...]$.

> So now people are working on quantum programming languages *again*.

On [[categorical semantics]] on [[von Neumann algebras]]:

* [[Kenta Cho]], *Semantics for a Quantum Programming Language by Operator Algebras*, EPTCS **172** (2014) 165-190 &lbrack;[arXiv:1412.8545](https://arxiv.org/abs/1412.8545), [doi:10.4204/EPTCS.172.12](https://doi.org/10.4204/EPTCS.172.12)&rbrack;


### Quipper as such

Exposition of the general idea of [[quantum programming languages]] for [[classically controlled quantum computation]] with an eye towards the `Quipper`-language:

* [[Benoît Valiron]], [[Neil J. Ross]], [[Peter Selinger]], [[D. Scott Alexander]], [[Jonathan M. Smith]], *Programming the quantum future*, Communications of the ACM **58** 8 (2015) 52–61 &lbrack;[doi:10.1145/2699415](https://doi.org/10.1145/2699415), [pdf](https://www.iro.umontreal.ca/~brassard/cours/6155/Langages%20de%20programmation%20quantique/Programming%20the%20Quantum%20Future.pdf),  [web](https://cacm.acm.org/magazines/2015/8/189851-programming-the-quantum-future/abstract), promo vid:[YT](https://youtu.be/mzce69oFdH0?list=PLn0nrSd4xjjbIHhktZoVlZuj2MbrBBC_f)&rbrack;


Original articles on Quipper:

* {#GLRSV13} [[Alexander Green]], [[Peter LeFanu Lumsdaine]], [[Neil Ross]], [[Peter Selinger]], [[Benoît Valiron]], _Quipper: A Scalable Quantum Programming Language_, ACM SIGPLAN Notices **48** 6 (2013) 333-342 &lbrack;[arXiv:1304.3390](https://arxiv.org/abs/1304.3390), [doi:10.1145/2499370.2462177](https://doi.org/10.1145/2499370.2462177)&rbrack;

* [[Jonathan Smith]], [[Neil Ross]], [[Peter Selinger]], [[Benoît Valiron]], _Quipper: Concrete Resource Estimation in Quantum Algorithms_, QAPL 2014 ([arXiv:1412.0625](https://arxiv.org/abs/1412.0625))

* [[Neil J. Ross]], Chapters 8-9 in: *Algebraic and Logical Methods in Quantum Computation*, Ph.D. thesis, Dalhousie University (2015) &lbrack;[arXiv:1510.02198](https://arxiv.org/abs/1510.02198)&rbrack;

  > (introducing Proto-Quipper)


Introduction and review:

* [[Alexander Green]], [[Peter LeFanu Lumsdaine]], [[Neil Ross]], [[Peter Selinger]], [[Benoît Valiron]], _An Introduction to Quantum Programming in Quipper_, Lecture Notes in Computer Science **7948** Springer (2013) 110-124 &lbrack;[arXiv:1304.5485](https://arxiv.org/abs/1304.5485), [doi:10.1007/978-3-642-38986-3_10](https://doi.org/10.1007/978-3-642-38986-3_10)&rbrack;

* {#Selinger16} [[Peter Selinger]], *Introduction to Quipper*, talk at [QPL2016](http://qpl2016.cis.strath.ac.uk) (2016) &lbrack;[video](https://youtu.be/59frzb__Eqo)&rbrack;

Example algorithms:

* Safat Siddiqui, Mohammed Jahirul Islam, Omar Shehab, *Five Quantum Algorithms Using Quipper* &lbrack;[arXiv:1406.4481](https://arxiv.org/abs/1406.4481)&rbrack;

On quantum [[software verification]] for/with Quipper:

* Linda Anticoli, Carla Piazza, Leonardo Taglialegne, Paolo Zuliani, _Towards Quantum Programs Verification: From Quipper Circuits to QPMC_, In: Devitt S., Lanese I. (eds) Reversible Computation. RC 2016. Lecture Notes in Computer Science, vol 9720. Springer, Cham ([doi:10.1007/978-3-319-40578-0_16](https://doi.org/10.1007/978-3-319-40578-0_16))


### Dependent linear types and categorical semantics
 {#ReferencesDependentLinearTypesAndCategoricalSemantics}

Discussion of some [[dependent linear type theory]] and [[categorical semantics]] for (proto-)[[Quipper]]:

* {#RiosSelinger18} [[Francisco Rios]], [[Peter Selinger]], *A Categorical Model for a Quantum Circuit Description Language*, EPTCS **266** (2018) 164-178 &lbrack;[arXiv:1706.02630](https://arxiv.org/abs/1706.02630), [doi:10.4204/EPTCS.266.11](https://doi.org/10.4204/EPTCS.266.11)&rbrack;

* [[Peng Fu]], [[Kohei Kishida]], [[Neil Ross]], [[Peter Selinger]],  _A Tutorial Introduction to Quantum Circuit Programming in Dependently Typed Proto-Quipper_, in I. Lanese, M. Rawski  (eds.) _Reversible Computation_ RC 2020. Lecture Notes in Computer Science, vol 12227 &lbrack;[arXiv:2005.08396](https://arxiv.org/abs/2005.08396), [doi:10.1007/978-3-030-52482-1_9](https://doi.org/10.1007/978-3-030-52482-1_9)&rbrack;

* {#FuKishidaSelinger20} [[Peng Fu]], [[Kohei Kishida]], [[Peter Selinger]], _Linear Dependent Type Theory for Quantum Programming Languages_, LICS '20: Proceedings of the 35th Annual ACM/IEEE Symposium on Logic in Computer ScienceJuly 2020 Pages 440–453 ([arXiv:2004.13472](https://arxiv.org/abs/2004.13472), [doi:10.1145/3373718.3394765](https://dl.acm.org/doi/10.1145/3373718.3394765), [pdf](https://depend.cs.uni-saarland.de/lics-icalp/papers/B5.F), [video](https://www.youtube.com/watch?v=GUT8j4V6Nzg))

* [[Francisco Rios]], *On a Categorically Sound Quantum Programming Language for Circuit Description*, Dalhousie University (2021) &lbrack;[hdl:10222/80771](http://hdl.handle.net/10222/80771)&rbrack;

* {#Lee22} [[Dongho Lee]], *Formal Methods for Quantum Programming Languages*, Paris Saclay (Dec 2022) &lbrack;[hal:tel-03895847](https://hal.science/LMF/tel-03895847)&rbrack;

Semantics on [[quantum CPOs]] (via [[quantum relations]] on [[quantum sets]]) for interpreting Quipper with term recursion:

* [[Andre Kornell]], [[Bert Lindenhovius]], [[Michael Mislove]], *Quantum CPOs*, EPTCS **340** (2021) 174-187 &lbrack;[arXiv:2109.02196](https://arxiv.org/abs/2109.02196), [doi:10.4204/EPTCS.340.9](https://doi.org/10.4204/EPTCS.340.9)&rbrack;


### Dynamic lifting
{#ReferencesDynamicLifting} 

The issue of "[[dynamic lifting]]" (of "[[bits]]" resulting from [[quantum measurement]] back into the "[[context]]"):

* brief mentioning on [GLRSV13, p. 5](#GLRSV13)

* [[Robert Rand]], *Formally Verified Quantum Programming*, UPenn (2018) &lbrack;[ediss:3175](https://repository.upenn.edu/edissertations/3175)&rbrack;

* {#LeeBardinPerrelleValiron2019} [[Dongho Lee]], Sebastien Bardin, [[Valentin Perrelle]], [[Benoît Valiron]], *Formalization of a Programming Language for Quantum Circuits with Measurement and Classical Control*, talk at *[Journées Informatique Quantique 2019](https://quantcert.github.io/GT-IQ'19/)* (Nov 2019) &lbrack;[pdf](https://quantcert.github.io/GT-IQ%2719/slides/Lee.pdf), [[LBPV_QCWithClassicalControl.pdf:file]]&rbrack;

* [[Dongho Lee]], [[Valentin Perrelle]], [[Benoît Valiron]], Zhaowei Xu, *Concrete Categorical Model of a Quantum Circuit Description Language with Measurement*, Leibniz International Proceedings in Informatics **213** (2021) 51:1-51:20 &lbrack;[arXiv:2110.02691](https://arxiv.org/abs/2110.02691), [doi:10.4230/LIPIcs.FSTTCS.2021.51](https://doi.org/10.4230/LIPIcs.FSTTCS.2021.51)&rbrack;

* [[Andrea Colledan]], [[Ugo Dal Lago]], *On Dynamic Lifting and Effect Typing in Circuit Description Languages* &lbrack;[arXiv:2202.07636](https://arxiv.org/abs/2202.07636)&rbrack;

* [[Andrea Colledan]], [[Ugo Dal Lago]], *On Dynamic Lifting and Effect Typing in Circuit Description Languages*, talk at *TYPES Workshop*, Nantes (2022)  &lbrack;[pdf](https://types22.inria.fr/files/2022/06/TYPES_2022_slides_13.pdf), [[ColledanLago-DynamicsLifting.pdf:file]]&rbrack;

* [[Peng Fu]], [[Kohei Kishida]], [[Neil J. Ross]], [[Peter Selinger]], *A biset-enriched categorical model for Proto-Quipper with dynamic lifting*, in proceedings of *[Quantum Physics and Logic 2022](https://www.qplconference.org/)* &lbrack;[arXiv:2204.13039](https://arxiv.org/abs/2204.13039)&rbrack;

* [[Peng Fu]], [[Kohei Kishida]], [[Neil J. Ross]], [[Peter Selinger]], *Proto-Quipper with dynamic lifting*, in proceedings of *[Quantum Physics and Logic 2022](https://www.qplconference.org/)* &lbrack;[arXiv:2204.13041](https://arxiv.org/abs/2204.13041)&rbrack;

* [[Dongho Lee]], *Formal Methods for Quantum Programming Languages*, Paris Saclay (Dec 2022) &lbrack;[hal:tel-03895847](https://hal.science/LMF/tel-03895847)&rbrack;

* [[Frank (Peng) Fu]], *Proto-Quipper with Dynamic Lifting*, [talk at](CQTS#PengFuOct2023) [[CQTS]] (23 Oct 2023) &lbrack;video:[YT](https://youtu.be/bBL7rlqbDWM)&rbrack;

### Reversing and control

Formalization as Proto-Quipper-C of a semantics for the reversing, control, and with-computed operations is in: 

* [[Peng Fu]], [[Kohei Kishida]], [[Neil J. Ross]], [[Peter Selinger]], *Proto-Quipper with Reversing and Control* &lbrack;[arXiv:2410.22261](https://arxiv.org/abs/2410.22261)&rbrack;


[[!redirects QPL]]

[[!redirects Proto-Quipper]]




+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Constructivism
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Constructive analysis is the incarnation of [[analysis]] in [[constructive mathematics]].  It is related to, but distinct from, _[[computable analysis]]_; the latter is developed in [[classical logic]] explicitly using [[computability theory]], whereas constructive analysis is developed in [[constructive logic]] where the computation is implicitly built-in. One can compile results in constructive analysis to computable analysis using [[realizability]].

In applications in [[computer science]] one uses for instance the _[[completion monad]]_ for _exact_ computations with [[real numbers]] (as opposed to floating point arithmetic). Therefore one also sometimes speaks of _exact analysis_. See also at _[[computable real number]]_.


## Related concepts

[[!include computable mathematics -- table]]

* [[computable real number]]

* [[exact real computer arithmetic]]

* [[computable physics]]

* [[constructive set theory]]

* [[constructive algebraic topology]]


## References
 {#References}

Introducing the formulation of [[analysis]] in [[constructive mathematics]], together with the notions of [[Bishop set]]/[[setoid]]:

* {#Bishop} [[Errett Bishop]]: *[[Foundations of Constructive Analysis]]*, McGraw-Hill (1967)

* [[Errett Bishop]], [[Douglas Bridges]]: *[[Constructive Analysis]]*, Grundlehren der mathematischen Wissenschaften **279**, Springer (1985) &lbrack;[doi:10.1007/978-3-642-61667-9](https://doi.org/10.1007/978-3-642-61667-9)&rbrack;

Introduction and review:

* [[Douglas Bridges]], *Constructive mathematics: a foundation for computable analysis*, Theoretical Computer Science **219** 1–2 (1999) 95-109 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(98)00285-0">doi:10.1016/S0304-3975(98)00285-0</a>&rbrack;

* [[Herman Geuvers]], [[Milad Niqui]], [[Bas Spitters]], [[Freek Wiedijk]], _Constructive analysis, types and exact real numbers_, Mathematical Structures in Computer Science **17** 01 (2007) 3-36 &lbrack;[doi:10.1017/S0960129506005834](https://doi.org/10.1017/S0960129506005834)&rbrack;

* [[Helmut Schwichtenberg]], *Constructive analysis with witnesses* (2013) &lbrack;[pdf](https://www.mathematik.uni-muenchen.de/~schwicht/seminars/semss13/constr13.pdf), [[Schwichtenberg-ConstructiveAnalysis.pdf:file]]&rbrack;

* {#Johansson19} Fredrik Johansson, *Reliable real computing*, talk at Mathematical Institute of Oxford (2019) &lbrack;[pdf](http://fredrikj.net/math/oxford2019.pdf)&rbrack;


See also:

* [[Helmut Schwichtenberg]], *Program Extraction in Constructive Analysis*, in *Logicism, Intuitionism, and Formalism*, Synthese Library, **341** Springer (2009) &lbrack;[doi:10.1007/978-1-4020-8926-8_13](https://doi.org/10.1007/978-1-4020-8926-8_13)&rbrack;

An undergraduate real analysis textbook taking a constructive approach using interval analysis is

* {#Bridger2019} Mark Bridger, _Real Analysis: A Constructive Approach Through Interval Arithmetic_, Pure and Applied Undergraduate Texts **38**, American Mathematical Society, 2019.

Implementations of constructive [[real number]] analysis in [[type theory]] implemented in [[Coq]] via the [[completion monad]]:

* [[Russell O'Connor]], *A Monadic, Functional Implementation of Real Numbers*, Math. Struc. Comp. Sci. **17** 1 (2007) 129-159 &lbrack;[arXiv:cs/0605058](https://arxiv.org/abs/cs/0605058), [doi:10.1017/S0960129506005871](https://doi.org/10.1017/S0960129506005871)&rbrack;

* [[Russell O'Connor]], _Certified exact transcendental real number computation in Coq_, in *Theorem Proving in Higher Order Logics. TPHOLs 2008*,  Lecture Notes in Computer Science **5170** (2008) 246-261 &lbrack;[arXiv:0805.2438](https://arxiv.org/abs/0805.2438), [doi:10.1007/978-3-540-71067-7_21](https://doi.org/10.1007/978-3-540-71067-7_21)&rbrack;

* [[Russell O'Connor]], _Incompleteness and Completeness: Formalizing Logic and Analysis in Type Theory_, PhD thesis, Radboud University Nijmegen (2009) &lbrack;[ubn:2066/76032](https://repository.ubn.ru.nl/handle/2066/76032), [author webpage](http://r6.ca/Thesis/)&rbrack;

* {#KrebbersSpitters11} [[Robbert Krebbers]], [[Bas Spitters]], *Type classes for efficient exact real arithmetic in Coq*, Logical Methods in Computer Science, **9** 1 (2013) lmcs:958 &lbrack;[arXiv:1106.3448](http://arxiv.org/abs/1106.3448/), <a href="https://doi.org/10.2168/LMCS-9(1:1)2013">doi:10.2168/LMCS-9(1:1)2013</a>&rbrack;

> (via [[ufias2012:Type classes]] in [[Coq]])

Exposition in:

* [[Bas Spitters]], *Verified Implementation of Exact Real Arithmetic in Type Theory*, talk at *Computable Analysis and Rigorous Numeric* (2013) &lbrack;[pdf](https://users-cs.au.dk/spitters/CARN.pdf), [[Spitters-ExactRealArithmetic.pdf:file]]&rbrack;


With emphasis on the use of the [[univalence axiom]]:

* {#Booij17} [[Auke Booij]], _Constructive analysis in univalent type theory_, 2017 ([pdf](https://www.cs.bham.ac.uk/~abb538/slides/2018-02-darmstadt.pdf))

* {#Booij18} [[Auke Booij]], _Extensional constructive real analysis via locators_, Mathematical Structures in Computer Science **31** 1 (2021) 64-88  &lbrack;[arXiv:1805.06781](https://arxiv.org/abs/1805.06781), [doi:10.1017/S0960129520000171](https://doi.org/10.1017/S0960129520000171)&rbrack;

* {#Booij20} [[Auke Booij]], *Analysis in Univalent Type Theory* (2020) &lbrack;[etheses:10411](http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf), [[Booij-AnalysisInUF.pdf:file]]&rbrack;

Implementation in [[Agda]] of [[Cauchy real numbers]] according to [Bishop (1967)](#Bishop67):

* [[Martin Lundfall]], *Formalizing real numbers in Agda* (2015) &lbrack;<a href="https://wcl.cs.rpi.edu/pilots/library/papers/TAGGED/4211-Lundfall%20(2015)%20-%20Formalizing%20Real%20Numbers%20in%20Agda.pdf">pdf</a>, [[Lundfall-RealNumbersInAgda.pdf:file]], [github](https://github.com/MrChico/Reals-in-agda)&rbrack;

* [[Zachary Murray]], *Constructive Analysis in the Agda Proof Assistant* &lbrack;[arXiv:2205.08354](https://arxiv.org/abs/2205.08354), [github](https://github.com/z-murray/honours-project-constructive-analysis-in-agda)&rbrack;

review:

* [[Zachary Murray]], *Constructive Real Numbers in the Agda Proof Assistant*, [talk at *CQTS*](Center+for+Quantum+and+Topological+Systems#MurrayFeb2023), (Feb 2023) &lbrack;video:[YT](https://www.youtube.com/watch?v=7Q_sjfyPJqU)&rbrack;


For the alternative [[Dedekind real numbers]] or [[HoTT book real numbers]], see the references there.



[[!redirects constructive real analysis]]

[[!redirects exact analysis]]
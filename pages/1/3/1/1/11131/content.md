
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
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

Introducing the formulation of [[analysis]] in [[constructive mathematics]], together with the notions of [[Bishop set]]/[[setoid]]:


* {#Bishop} [[Errett Bishop]], _Foundations of constructive analysis._ McGraw-Hill, (1967)



Introduction and review:

* [[Herman Geuvers]], [[Milad Niqui]], [[Bas Spitters]], [[Freek Wiedijk]], _Constructive analysis, types and exact real numbers_, Mathematical Structures in Computer Science **17** 01 (2007) 3-36 &lbrack;[doi:10.1017/S0960129506005834](https://doi.org/10.1017/S0960129506005834)&rbrack;

* [[Helmut Schwichtenberg]], *Constructive analysis with witnesses* (2013) &lbrack;[pdf](https://www.mathematik.uni-muenchen.de/~schwicht/seminars/semss13/constr13.pdf), [[Schwichtenberg-ConstructiveAnalysis.pdf:file]]&rbrack;

An undergraduate real analysis textbook taking a constructive approach using interval analysis is

* {#Bridger2019} Mark Bridger, _Real Analysis: A Constructive Approach Through Interval Arithmetic_, Pure and Applied Undergraduate Texts **38**, American Mathematical Society, 2019.

Implementations of constructive [[real number]] analysis in [[type theory]] implemented in [[Coq]] via the [[completion monad]]:

* [[Russell O'Connor]], *A Monadic, Functional Implementation of Real Numbers*, Math. Struc. Comp. Sci. **17** 1 (2007) 129-159 &lbrack;[arXiv:cs/0605058](https://arxiv.org/abs/cs/0605058), [doi:10.1017/S0960129506005871](https://doi.org/10.1017/S0960129506005871)&rbrack;

* [[Russell O'Connor]], _Certified exact transcendental real number computation in Coq_, in *Theorem Proving in Higher Order Logics. TPHOLs 2008*,  Lecture Notes in Computer Science **5170** (2008) 246-261 &lbrack;[arXiv:0805.2438](https://arxiv.org/abs/0805.2438), [doi:10.1007/978-3-540-71067-7_21](https://doi.org/10.1007/978-3-540-71067-7_21)&rbrack;

* [[Russell O'Connor]], _Incompleteness and Completeness: Formalizing Logic and Analysis in Type Theory_, PhD thesis, Radboud University Nijmegen (2009) &lbrack;[ubn:2066/76032](https://repository.ubn.ru.nl/handle/2066/76032), [author webpage](http://r6.ca/Thesis/)&rbrack;

* {#KrebbersSpitters11} Robbert Krebbers, [[Bas Spitters]], _Type classes for efficient exact real arithmetic in Coq_ ([arXiv:1106.3448](http://arxiv.org/abs/1106.3448/))

* [[Bas Spitters]], _Verified Implementation of Exact Real Arithmetic in Type Theory_, talk at _Computable Analysis and Rigorous Numeric_ ([pdf](http://www.cs.ru.nl/~spitters/CARN.pdf))

With emphasis on the use of the [[univalence axiom]]:

* {#Booij17} Auke Booij, _Constructive analysis in univalent type theory_, 2017 ([pdf](https://www.cs.bham.ac.uk/~abb538/slides/2018-02-darmstadt.pdf))

* {#Booij18} Auke Booij, _Extensional constructive real analysis via locators_ ([arXiv:1805.06781](https://arxiv.org/abs/1805.06781))

See also 

* {#Johansson19} Fredrik Johansson, _Reliable real computing_, talk at Mathematical Institute of Oxford, 2019 ([pdf](http://fredrikj.net/math/oxford2019.pdf))

[[!redirects exact analysis]]
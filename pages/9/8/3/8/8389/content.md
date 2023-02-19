
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computing
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



# Denotational semantics
* table of contents
{: toc}

## Idea

In [[computer science]] and [[formal logic]], *denotational semantics* refers [[semantics]] based on the idea that [[programs]] and the [[data]] they manipulate are symbolic realizations of abstract [[mathematics|mathematical]] [[objects]]. 

For example, the denotational semantics

*  of [[numerals]] are [[numbers]], 

*  of [[programs]] are [[functions]] (approximately). 

The idea of denotational semantics is thus to associate an appropriate  mathematical object, such as a number, a tuple, or a function, with each [[term]] of the given [[programming language]].

A key requirement on denotational semantics is that it respects the *compositionality* of programming languages, hence that the semantics of [[terms]] [[term introduction|constructed]] from sub-terms is correspondingly built from the semantics of these sub-terms.

Under the [[Curry-Howard correspondence]], proofs can be seen as programs and thus one can apply denotational semantics to proofs. In this way proofs are interpreted as functions or more generally as morphisms of some category. It is used to interpret proofs of [[intuitionistic logic]] and [[linear logic]] as morphisms of respectively [[cartesian closed categories]] and [[star-autonomous categories]].


## Related entries

* [[computation]]

* [[domain theory]]

* [[semantics]]

  * [[categorical semantics]]

  * [[operational semantics]]

  * [[distributional semantics]]

## References

Denotational semantics originates with the proposal of [[domain theory]] to regard [[data types]] as [[posets]] ([[(0,1)-categories]]):

* [[Dana S. Scott]], *Outline of a mathematical theory of computation*, in: Proceedings of the *Fourth Annual Princeton Conference on Information Sciences and Systems* (1970) 169–176. &lbrack;[pdf](https://ropas.snu.ac.kr/~kwang/520/readings/sco70.pdf), [[Scott-TheoryOfComputation.pdf:file]]&rbrack;

* [[Dana S. Scott]], [[Christopher Strachey]], *Toward a Mathematical Semantics for Computer Languages*, Oxford University Computing Laboratory, Technical Monograph PRG-6 (1971) &lbrack;[pdf](https://www.cs.ox.ac.uk/files/3228/PRG06.pdf), [[ScottStrachey-MathematicalSemantics.pdf:file]]&rbrack;

* {#Scott76} [[Dana Scott]], *Data types as lattices*. SIAM Journal of Computing **5** 3 (1976) 522--587 &lbrack;[doi:10.1137/0205037](https://doi.org/10.1137/0205037), [pdf](https://www.cs.ox.ac.uk/files/3287/PRG05.pdf)&rbrack;

Lectures and introductions:

* [[Robert D. Tennet]], *The denotational semantics of programming languages*, Communications of the ACM **19** 8 (1976) 437–453 &lbrack;[doi:10.1145/360303.360308](https://doi.org/10.1145/360303.360308), [pdf](https://dl.acm.org/doi/pdf/10.1145/360303.360308)&rbrack;

* [[Robert D. Tennet]], *Denotational semantic*, in: *[[Handbook of Logic in Computer Science]]* **3**, Oxford University Press (1995) &lbrack;[ISBN:9780198537625](https://global.oup.com/academic/product/handbook-of-logic-in-computer-science-9780198537625?cc=de&lang=en&)&rbrack;

* [[Andrew M. Pitts]], *Lecture Notes on Denotational Semantics* (2012) &lbrack;[pdf](https://www.cl.cam.ac.uk/teaching/1112/DenotSem/dens-notes-bw.pdf), [[Pitts-DenotationalSemantics.pdf:file]]&rbrack;


Textbook accounts:

* [[Glynn Winskel]], §5 of: *The Formal Semantics of Programming Languages*, MIT Press (1993) &lbrack;[ISBN:9780262731034](https://mitpress.mit.edu/9780262731034/the-formal-semantics-of-programming-languages/), [pdf](https://www.cin.ufpe.br/~if721/intranet/TheFormalSemanticsofProgrammingLanguages.pdf)&rbrack;

* [[Kenneth Slonneger]], [[Barry Kurtz]], *Denotational semantics* &lbrack;[pdf](https://homepage.divms.uiowa.edu/~slonnegr/plf/Book/Chapter9.pdf)&rbrack;, Chapter 9 of: *Formal Syntax and Semantics of Programming Languages*, Addison-Wesley (1995) &lbrack;[webpage](https://homepage.divms.uiowa.edu/~slonnegr/plf/Book/), [pdf](https://doc.lagout.org/science/Artificial%20Intelligence/Natural%20Language%20Processing/Formal%20Syntax%20and%20Semantics%20of%20Programming%20Languages%20-%20Kenneth%20Slonneger.pdf)&rbrack;

* [[David A. Schmidt]], *Denotational Semantics -- A methodology for language development*, Allyn and Bacon (1986)  &lbrack;[pdf](https://people.cs.ksu.edu/~schmidt/text/DenSem-full-book.pdf), [webpage](https://people.cs.ksu.edu/~schmidt/text/densem.html)&rbrack;

* [[Thomas Streicher]], *Domain-Theoretic Foundations of Functional Programming*, World Scientific (2006) &lbrack;[pdf](https://doc.lagout.org/programmation/Functional%20Programming/Domain-Theoretic%20Foundations%20of%20Functional%20Programming%20%5BStreicher%202006-12-04%5D.pdf), [doi:10.1142/6284](https://www.worldscientific.com/worldscibooks/10.1142/6284)&rbrack;



See also:

* Wikipedia, [Denotational semantics](http://en.wikipedia.org/wiki/Denotational_semantics)



Discussion of denotational semantics for [[Haskell]]:

* *[Haskell/Denotational semantics](https://en.wikibooks.org/wiki/Haskell/Denotational_semantics)*


category: computer science

[[!redirects denotational semantics]]

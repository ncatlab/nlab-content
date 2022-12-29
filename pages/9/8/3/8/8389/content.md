
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

For example, 

*  [[string (computer science)|strings]] of digits refer to [[numbers]], 

and 

*  [[programs]] correspond (approximately) mathematical [[functions]]. 

The idea of denotational semantics is thus to associate an appropriate  mathematical object, such as a number, a tuple, or a function, with each [[term]] of the given [[programming language]].

A key requirement on denotational semantics is that it respects the *compositionality* of programming languages, hence that the semantics of [[terms]] [[term introduction|constructed]] from sub-terms is correspondingly built from the semantics of these sub-terms.


## Related entries

* [[computation]]

* [[domain theory]]

* [[semantics]]

  * [[categorical semantics]]

  * [[operational semantics]]

  * [[distributional semantics]]

## References

Denotational semantics originates with:

* [[Dana S. Scott]], *Outline of a mathematical theory of computation*, in: Proceedings of the *Fourth Annual Princeton Conference on Information Sciences and Systems* (1970) 169–176. &lbrack;[pdf](https://ropas.snu.ac.kr/~kwang/520/readings/sco70.pdf), [[Scott-TheoryOfComputation.pdf:file]]&rbrack;

* [[Dana S. Scott]], [[Christopher Strachey]], *Toward a Mathematical Semantics for Computer Languages*, Oxford University Computing Laboratory, Technical Monograph PRG-6 (1971) &lbrack;[pdf](https://www.cs.ox.ac.uk/files/3228/PRG06.pdf), [[ScottStrachey-MathematicalSemantics.pdf:file]]&rbrack;

* {#Scott76} [[Dana Scott]], *Data types as lattices*. SIAM Journal of Computing **5** 3 (1976) 522--587 &lbrack;[doi:10.1137/0205037](https://doi.org/10.1137/0205037), [pdf](https://www.cs.ox.ac.uk/files/3287/PRG05.pdf)&rbrack;


See also:

* Wikipedia, [Denotational semantics](http://en.wikipedia.org/wiki/Denotational_semantics)


category: computer science

[[!redirects denotational semantics]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

Originally, "simple type theory" was the name of the [[type theory]] introduced by [Church (1940)](#Church40) (therefore often and more informatively: "Church's type theory" or similar). This [[type theory]] allowed (only) [[function type]]-[[type formation]] (therefore often: "simply typed [[lambda-calculus]]") based on two elementary types (a kind of [[type of natural numbers]] and a [[type of propositions]]).

In mild generalization, if one admits in addition [[product type]]-[[type formation]] then &lbrack;e.g. [Gunter (1992)](#Gunter92)&rbrack; these are the type theories whose [[categorical semantics]] is in [[cartesian closed categories]] (see also at *[[relation between category theory and type theory]]*).

More generally, the term "simple type theory" has come to refer to any [[type theory]] whose [[type formations]] are *not indexed*, in that the [[judgment]] that a [[type]] $A$ is well-formed has no other inputs, understood *in contrast* to:

* [[polymorphism|polymorphic type theory]], where types depend on a context of type variables, 

* [[dependent type theory]], where types depend on a [[context]] of more general variables.


## Related Pages

* [[pure type system]]

## References

Original articles:

* {#Russell08} [[Bertrand Russell]], _Mathematical Logic as Based on the Theory of Types_, American Journal of Mathematics, Vol. 30, No. 3 (Jul., 1908), pp. 222-262

* {#Church40} [[Alonzo Church]], §5 of: *A Formulation of the Simple Theory of Types*, The Journal of Symbolic Logic **5** 2 (1940) 56-68  &lbrack;[doi:10.2307/2266170](https://doi.org/10.2307/2266170)&rbrack;

See also 

* Stanford Encyclopedia of Philosophy, *[Church’s Type Theory](https://plato.stanford.edu/entries/type-theory-church/)*

Lecture notes:

* {#Girard89} [[Jean-Yves Girard]] (translated and with appendiced by [[Paul Taylor]] and [[Yves Lafont]]), *Proofs and Types*, Cambridge University Press (1989) &lbrack;[ISBN:978-0-521-37181-0](), [webpage](http://www.paultaylor.eu/stable/Proofs+Types.html), [pdf](https://www.paultaylor.eu/stable/prot.pdf)&rbrack;




Textbook accounts:

* [[J. Roger Hindley]], *Basic Simple Type Theory*, Cambridge University Press (1997, 2009) &lbrack;[doi:10.1017/CBO9780511608865](https://doi.org/10.1017/CBO9780511608865)&rbrack;


* {#Gunter92} [[Carl A. Gunter]], §2-3 in: *Semantics of Programming Languages -- Structures and Techniques*, MIT Press (1992) &lbrack;[ISBN:9780262570954](https://mitpress.mit.edu/9780262570954/semantics-of-programming-languages/)&rbrack;

  > (in a context of [[programming languages]])


See also:

* W. Farmer, _The seven virtues of simple type theory_, Journal of Applied Logic, Vol. 6, No. 3. (September 2008), pp. 267-286.



[[!redirects simple type theories]]

[[!redirects simply typed lambda calculus]]
[[!redirects simply typed lambda-calculus]]
[[!redirects simply typed λ-calculus]]

[[!redirects simply-typed lambda calculus]]
[[!redirects simply-typed lambda-calculus]]
[[!redirects simply-typed λ-calculus]]



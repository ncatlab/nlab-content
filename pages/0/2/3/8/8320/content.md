
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



# The contraction rule
* table of contents
{: toc}

## Idea

In [[formal logic]] and [[type theory]], the _contraction rule_ states that any valid [[deduction]] that uses a [[premise]] more than once remains valid using that premise only once.  Along with the [[weakening rule]] and the [[exchange rule]], it is one of the most commonly adopted [[structural rules]].

The contraction rule is not used in all [[logical frameworks]]: In [[substructural logics]] like [[linear logic]] and [[affine logic]] it is discarded.


## Statements

The exact form this rule takes depends on the [[logic]] used.
However, a common version of it is given below:

$$
  \frac{
    \Gamma, A, A, \Delta \vdash B
  }{
    \Gamma, A, \Delta \vdash B
  }
  (C)
$$

## Semantics

In [[categorical semantics]], the contraction rule corresponds to having [[monoidal category with diagonals|diagonals for the monoidal structure]] corresponding to the logical binary operator at hand.

## Related concepts

* [[inference rule]]

* [[structural rule]]

* [[weakening rule]]

* [[exchange rule]]


## References

The notion of contraction as a [[structural inference rule]] originates (under the German name *Zusammenziehung*) with: 

* {#Gentzen35} [[Gerhard Gentzen]], §1.2.1 in: _Untersuchungen &#252;ber das logische Schlie&#223;en I_ _Mathematische Zeitschrift_ **39** 1 (1935) &lbrack;[doi:10.1007/BF01201353](http://dx.doi.org/10.1007/BF01201353)&rbrack;

* {#Gentzen69} [[Gerhard Gentzen]], §1.21 in: *Investigations into Logical Deduction*, in M. E. Szabo (ed.), *The Collected Papers of Gerhard Gentzen*, Studies in Logic and the Foundations of Mathematics **55**, Springer (1969) 68-131 &lbrack;[ISBN:978-0-444-53419-4](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/55), [pdf](https://logic-teaching.github.io/prop/texts/Gentzen%201969%20-%20Investigations%20into%20Logical%20Deduction.pdf)&rbrack;


On the [[categorical semantics]]:

* [[Bart Jacobs]], *Semantics of weakening and contraction*, Annals of Pure and Applied Logic **69** 1 (1994) 73-106 &lbrack;<a href="https://doi.org/10.1016/0168-0072(94)90020-5">doi:10.1016/0168-0072(94)90020-5</a>&rbrack;

Discussion in [[dependent type theory]]:

* {#Jacobs98} [[Bart Jacobs]], p. 122, 585 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;

  > (emphasis on the [[categorical model of dependent types]])

* {#UFP13} [[Univalent Foundations Project]], §A of *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

  > (in the context of [[homotopy type theory]])


* {#Rijke18} [[Egbert Rijke]], *Dependent type theory* &lbrack;[pdf](https://www.andrew.cmu.edu/user/erijke/hott/dtt.pdf)&rbrack;, Lecture 1 in: *[[Introduction to Homotopy Type Theory]]*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;

  > (in the context of [[homotopy type theory]])




[[!redirects contraction rule]]
[[!redirects contraction rules]]

[[!redirects axiom UIP]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

In [[type theory]] what is called the _UIP axiom_, the axiom of _uniqueness of identity proofs_ is an [[axiom]] that when added to [[intensional type theory]] turns it into a [[set-level type theory]].

The axiom asserts that any two [[terms]] of the same [[identity type]] 
$Id_A(x,y)$ are themselves [[propositional equality|propositionally equal]] (in the corresponding higher identity type).

This is contrary to the [[univalence]] axiom, which makes sense only in the absence of UIP.

## Statement

+-- {: .num_defn}
###### Definition

The _UIP axiom_ (for types in a [[type of types|universe]] "$Type$") posits that the type 

$$
\underset{A \colon Type}{\prod} 
\underset{x,y \colon A}{\prod}
\underset{p,q \colon Id_A(x,y)}{\prod}
Id_{Id_A(x,y)}(p,q)
$$

has a term. In other words, we add to our type theory the rule

$$
\frac{}{
  \vdash uip
  \colon
  \underset{A \colon Type}{\prod} 
  \underset{x,y \colon A}{\prod}
  \underset{p,q \colon Id_A(x,y)}{\prod}
  Id_{Id_A(x,y)}(p,q)}
$$

We can modify this by making the hypotheses of the axiom into premises of the rule, if we wish.  In particular, this can be used to give a version of the rule that applies to all types not necessarily belonging to some fixed universe, using the [[judgment]] "$A\;type$" for "$A$ is a type" (as distinguished from "$A:Type$" for "$A$ belongs to the universe type $Type$").

$$
\frac{\Gamma\vdash A\; type \quad \Gamma\vdash x : A \quad \Gamma \vdash y:A \quad \Gamma \vdash p : Id_A(x,y) \quad \Gamma \vdash q:Id_A(x,y)}{
  \Gamma\vdash uip : Id_{Id_A(x,y)}(p,q)}
$$

=--

## Definitional UIP

There is also a definitional version of UIP, where any two terms of the same [[identity type]] or [[path type]] are [[definitional equality|definitionally equal]]. It is given by the following rule: 

$$
\frac{\Gamma\vdash A\; type \quad \Gamma\vdash x : A \quad \Gamma \vdash y:A \quad \Gamma \vdash p : Id_A(x,y) \quad \Gamma \vdash q:Id_A(x,y)}{\Gamma\vdash p \equiv q: Id_A(x,y)}
$$

Definitional UIP is implied by [[boundary separation]] in [[cubical type theory]]. 

## Related concepts

* [[axiom K]]

* [[boundary separation]]

## References

* "[The groupoid interpretation of type theory](http://www.tcs.ifi.lmu.de/mitarbeiter/martin-hofmann/pdfs/agroupoidinterpretationoftypetheroy.pdf)" [PDF], by Martin Hofmann and Thomas Streicher, 1996.

Discussion in [[Coq]] is in

* Pierre Corbineau, _The K axiom  in Coq (almost) for free_ ([pdf](http://coq.inria.fr/files/adt-2fev10-corbineau.pdf)) 

For definitional UIP in [[XTT]]

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _Cubical syntax for reflection-free extensional equality_. In Herman Geuvers, editor, _4th International Conference on Formal Structures for Computation and Deduction (FSCD 2019)_, volume 131 of _Leibniz International Proceedings in Informatics (LIPIcs)_, pages 31:1-31:25. ([arXiv:1904.08562](https://arxiv.org/abs/1904.08562), [doi:10.4230/LIPIcs.FCSD.2019.31](https://doi.org/10.4230/LIPIcs.FCSD.2019.31))

* [[Jonathan Sterling]], [[Carlo Angiuli]], [[Daniel Gratzer]], _A Cubical Language for Bishop Sets_, Logical Methods in Computer Science, 18 (1), 2022. ([arXiv:2003.01491](https://arxiv.org/abs/2003.01491)). 

[[!redirects uniqueness of identity proofs]]
[[!redirects UIP]]

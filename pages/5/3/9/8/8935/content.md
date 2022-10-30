+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

*Disambiguation: For axiom K as a principle of [[modal logic]], see [[axiom K (modal logic)]]*

# Contents
* table of contents
{: toc}

## Idea 

In [[type theory]], the _axiom K_ is an [[axiom]] that when added to [[intensional type theory]] turns it into [[extensional type theory]] --- or more precisely, what is called [[extensional type theory|here]] "propositionally extensional type theory". In the language of [[homotopy type theory]], this means that all types are [[h-sets]], accordingly axiom K is incompatible with the [[univalence axiom]].

Heuristically, the axiom asserts that each [[term]] of each [[identity type]] $Id_A(x,x)$ (of [[equivalences]] of a [[term]] $x \colon A$) is [[propositional equality|propositionally equal]] to the canonical [[reflexive relation|reflexivity]] equality proof $refl_x \colon Id_A(x,x)$. 

See also at _[extensional type theory -- Propositional extensionality](extensional+type+theory#PropositionalExtensionality)_.


## Statement

$$
  K 
  \colon 
  \underset{A \colon Type}{\prod} 
  \underset{x \colon A}{\prod}
  \underset{P \colon Id_A(x,x) \to Type}{\prod} 
  \left(
     P(refl_A x)
     \to  
    \underset{h \colon Id_A(x,x)}{\prod} P(h)
  \right)
$$

## Properties

Unlike its logical equivalent [[axiom UIP]], axiom K can be endowed with computational behavior: $K(A,x,P,d,refl_A x)$ computes to $d$.  This gives a way to specify a computational propositionally extensional type theory.

This sort of computational axiom K can also be implemented with, and is sufficient to imply, a general scheme of function definition by pattern-matching.  This is implemented in the proof assistant [[Agda]].  (The flag `--without-K` alters Agda's pattern-matching scheme to a weaker version appropriate for [[intensional type theory]], including [[homotopy type theory]].)


## Related concepts

* [[uniqueness of identity proofs]]

* [[boundary separation]]

## References

The axiom K was introduced in 

* [[Thomas Streicher]], _Investigations into intensional type theory_ Habilitation thesis (1993) ([pdf](http://www.mathematik.tu-darmstadt.de/~streicher/HabilStreicher.pdf))

For a review and discussion of the implementation in [[Coq]], see

* Pierre Corbineau, _The K axiom  in Coq (almost) for free_ ([pdf](http://coq.inria.fr/files/adt-2fev10-corbineau.pdf)) 

Discussion in the context of [[homotopy type theory]] is in 

* [[Univalent Foundations Project]], _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

around theorem 7.2.1

[[!redirects Streicher axiom K]]
[[!redirects Streicher's axiom K]]
[[!redirects Streicher's axiom K]]
[[!redirects Streicher\'s axiom K]]
[[!redirects Axiom K (type theory)]]
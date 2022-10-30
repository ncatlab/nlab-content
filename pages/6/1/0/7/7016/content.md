
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The principle of functional extensionality states that two [[functions]] are [[equal]] if their values are equal at every argument.


## Definition in type theory

In [[intensional type theory|intensional]] ([[Martin-Löf type theory|Martin-Löf]]) [[dependent type theory]] the existence of [[identity types]] induces a notion on [[path space objects|paths]] between [[terms]] of a given type.

In particular for two [[terms]] $f, g \in [X,Y]$

    f g: X -> Y

of _[[function type]]_, a path/[[morphism]] $f \stackrel{p}{\to} g$

    p: f == g

between them is to be thought of as a [[homotopy]] or [[natural transformation]] (a $1$-[[transfor]]). In particular it implies, one can prove, that there are families of paths $happly_{f,g,p}$ between all the values of the functions

    happly f g p: forall x: X, f x == g x .

However, from general [[intensional type theory|intensional]] [[dependent type theory]] one cannot prove the converse: 

* the existence of paths between all pairs of values does not imply that there is a path between the functions. 

This fact has a clear [[semantics|interpretation]] in [[topology]]: just the existence of a family of paths between all pairs of values of two [[continuous functions]] does not imply that there is a [[homotopy]] between them. The reason is that the family of paths may not itself depend _continuously_ on the variable $x$.

However, in the context of [[homotopy type theory]] one wants to interpret the type theory as the [[internal language of an (∞,1)-topos]], for instance of [[Top]] $\simeq$ [[∞Grpd]]. In such an [[internal logic]] context a _family_ of anything must always mean "continuous family". In other words, in such a context one wants to impose the condition that a term

    eta: forall x: X, f x == g x .

that gives a family of paths necessarily gives a _continuous_ family of paths, such that one obtains from this an actual homotopy between $f$ and $g$.

If the type theory has an extra [[axiom]] that implies this, one says that **function extensionality** holds. 

(Beware that the term "function extensionality" here is at best unrelated and at worst contradictory to the term "[[extensional type theory]]". )


## Properties

### Relation to the univalence axiom

The [[univalence axiom]] implies function extensionality. See for instance ([Bauer-Lumsdaine](#BauerLumsdaine)).


## References

An introduction to the relevant notions and a guided walk through the formal proof that univalence implies functional extensionality is at

* [[Andrej Bauer]], [[Peter LeFanu Lumsdaine]], _[[Oberwolfach HoTT-Coq tutorial]]_
  {#BauerLumsdaine}


[[!redirects function extensionality]]
[[!redirects functional extensionality]]

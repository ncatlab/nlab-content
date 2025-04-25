
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Inductive families_ generalize [[inductive types]]. Instead of defining a single type inductively, one simultaneously defines a whole family of types. An alternative term is "indexed inductive definition".

A simple example of an inductive family is the type of vectors Vect n indexed by the dimension n. This is defined by two constructors: one for the empty vector of dimension 0, and another for the operation which constructs a vector of dimension n+1 by adding a component to a vector of dimension n. The [[family of finite types]] Fin n (indexed by n) can also be defined as an inductive family: the constructor 0 is in any Fin n, and there is a successor operation which constructs an element in Fin (n+1) from an element in Fin n.

By the identification of [[propositions as types]], inductive families correspond to inductively defined predicates. For example, the [[identity type]] on a type A can be defined inductively by the reflexivity rule stipulating that a is identical to a for any a : A, that is, identity is the least reflexive relation. The identity family of types in intuitionistic type theory results from the identification of this relation with a family of types.


## Examples

* The identity types of an indexed W-type are another indexed W-type.  This has been formalized by [Huginin](#Hugunin).

* The [[inductive covers]] in [[formal topology]] and [[real analysis]] are an example of a [[higher inductive type|higher]] inductive family.

## Semantics

Standard inductive types, [[W-types]] can be interpreted in any topos with [[natural numbers object]] (Moerdijk-Palmgren). Gambino and Hyland construct initial algebras for dependent [[polynomial functors]]. [Indexed containers](#AGHMM) are the same as dependent polynomial functors.
[Indexed containers](#AGHMM) are claimed to form a foundation for inductive families.

## Higher categorical version/ homotopy type theory

[van den Berg and Moerdijk](#vdBergMoerdijk13) show that (standard) W-types can be interpreted in certain [[model categories]].

## Reduction to ordinary W-types

In [[homotopy type theory]] with [[universes]], one can reduce indexed W-types to W-types. This has been formalized [here](https://github.com/pcapriotti/agda-base/blob/master/src/container/w/core.agda), [here](https://github.com/SkySkimmer/HoTTClasses/blob/inductives/theories/theory/inductives.v) and [here](#Hugunin).
[Sattler](#Sattler) outlines a generalization of the reduction to [[homotopy type theory]] without the need of universes.

## References {#References} 



[[!include history of inductive types -- references]]





### Further developments

* {#AGHMM} [[Thorsten Altenkirch]], [[Neil Ghani]], Peter Hancock, Conor McBride, and Peter Morris, _Indexed containers_ ([pdf](http://strictlypositive.org/indexed-containers.pdf))

* [[Nicola Gambino]] and [[Martin Hyland]], *Wellfounded Trees and Dependent Polynomial Functors* [PDF](https://www.irif.fr/~mellies/mpri/mpri-ens/articles/gambino-hyland-polynomial-functors.pdf)

* [[Benno van den Berg]], [[Ieke Moerdijk]], _W-types in Homotopy Type Theory_ ([arXiv:1307.2765](http://arxiv.org/abs/1307.2765)) {#vdBergMoerdijk13}

* {#Sattler} [[Christian Sattler]], _On relating indexed W-types with ordinary ones_ [slides](http://cs.ioc.ee/types15/slides/sattler-slides.pdf)

* {#Hugunin} [[Jasper Hugunin]], _IWTypes_, <https://github.com/jashug/IWTypes>


[[!redirects inductive families]]
[[!redirects indexed inductive definition]]
[[!redirects indexed inductive type]]
[[!redirects indexed inductive types]]
[[!redirects indexed W-type]]
[[!redirects indexed W-types]]

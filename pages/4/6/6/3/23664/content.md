+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition 

Given two [[sets]] $(A, \approx_A)$ and $(B, \approx_B)$ equipped with [[equivalence relations]], we say that a [[function]] $f:A \to B$ is $\approx$-**extensional** if it preserves the equivalence relation $\approx$: for all $x \in A$ and $y \in A$, if $x \approx_A y$, then $f(x) \approx_B f(y)$. 

In [[category theory]], this means that an extensional function is a [[functor]] between two [[thin category|thin]] [[groupoids]] or a [[dagger functor]] between two thin [[dagger categories]], since equivalence relations can be modeled via the [[hom-sets]] of thin dagger categories or groupoids. 

This definition is common in the [[dependent type theory]] literature that uses [[equivalence relations]] for defining [[setoids]], but note that the carrier types are usually defined as general [[types]] instead of [[h-sets]] in this case. 

Extensional functions are important in defining [[algebraic structures]] that use [[equivalence relations]] instead of [[equality]] for the equational axioms, such as [[prelattices]] and [[Heyting prealgebras]]. 

## Generalizations

One can generalize the definition of extensional function from equivalence relations to other structures

### As functions between pseudo-equivalence relations

A [[pseudo-equivalence relation]] on a [[set]] $T$ is a [[quiver]] structure $\mathrm{hom}_T(x, y)$ on $T$ (called the [[hom-sets]]), with [[identity morphisms]] $\mathrm{id}_T(x)$ in $\mathrm{hom}_T(x, x)$, [[composition]] of [[morphisms]] $g \circ f$ in $\mathrm{hom}_T(x, z)$ for [[morphisms]] $f$ in $\mathrm{hom}_T(x, y)$ and $g$ in $\mathrm{hom}_T(y, z)$, and dagger operation $f^\dagger$ in $\mathrm{hom}_T(y, x)$ for morphism $f$ in $\mathrm{hom}_T(x, y)$. 

An **extensional function** between two [[sets]] $(A, \mathrm{hom}_A)$ and $(B, \mathrm{hom}_B)$ equipped with a [[pseudo-equivalence relation]] is then a function $f:A \to B$ with a family of functions $f_\mathrm{hom}(x, y):\mathrm{hom}_A(x, y) \to \mathrm{hom}_B(f(x), f(y))$. 

This definition is common in the [[dependent type theory]] literature that uses pseudo-equivalence relations for defining [[setoids]], but note that the [[hom-sets]] and carrier types are usually defined as general [[types]] instead of [[h-sets]]. If the pseudo-equivalence relations are the [[identity types]], then every function is extensional in this sense by the [[action on identifications]]. 

### As functions between quivers

One doesn't actually need the full structure of a [[pseudo-equivalence relation]] to define an extensional function: only the quiver structure of the hom-sets are needed. Thus, an **extensional function** between two [[quivers]] $(A, \mathrm{hom}_A)$ and $(B, \mathrm{hom}_B)$ is a function $f:A \to B$ with a family of functions $f_\mathrm{hom}(x, y):\mathrm{hom}_A(x, y) \to \mathrm{hom}_B(f(x), f(y))$. 

Thus, in [[dependent type theory]] with a [[directed interval]] type, where every type comes with [[hom-types]] defined using the directed interval, and so are [[quivers]] (and in many cases [[cubical objects]]), one can talk about functions being extensional in the above sense. In this sense, one gets the usual case of an extensional function between equivalence relations when the type is a [[thin]] [[Segal type]] where every morphism is an [[isomorphism]]. 

## Related concepts

* [[strongly extensional function]]
* [[quiver]]
* [[functor]]
* [[thin category]]
* [[setoid]]
* [[equivalence relation]]
* [[identity types]]
* [[interval type]]

## References

* [[Erik Palmgren]], *On equality of objects in categories in constructive type theory*, In 23rd International Conference on Types for Proofs and Programs (TYPES 2017). Leibniz International Proceedings in Informatics (LIPIcs), Volume 104, pp. 7:1-7:7, Schloss Dagstuhl – Leibniz-Zentrum für Informatik (2019) &lbrack;[10.4230/LIPIcs.TYPES.2017.7](https://doi.org/10.4230/LIPIcs.TYPES.2017.7), [arXiv:1708.01924](https://arxiv.org/abs/1708.01924)&rbrack;

[[!redirects extensional function]]
[[!redirects extensional functions]]
[[!redirects extensional operation]]
[[!redirects extensional operations]]
[[!redirects extensional prefunction]]
[[!redirects extensional prefunctions]]
[[!redirects extensional pre-function]]
[[!redirects extensional pre-functions]]
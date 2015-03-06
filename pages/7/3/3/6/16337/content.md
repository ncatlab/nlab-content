
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _cocartesian monoidal (∞,1)-category_ is a [[symmetric monoidal (∞,1)-category]] whose [[tensor product]] is given by the categorical [[coproduct]]. 
This is dual to the notion of [[cartesian monoidal (∞,1)-category]].

## Definition

(...)

([Lurie, def. 2.4.0.1](#Lurie))

(...)

## Properties

+-- {: .un_lemma}
###### Lemma
If $C$ is an [[(infinity,1)-category]] admitting finite coproducts, then the cocartesian symmetric monoidal structure on $C$ is equivalent to the symmetric monoidal structure obtained as the opposite of the [[cartesian monoidal (infinity,1)-category|cartesian monoidal structure]] on the [[opposite (infinity,1)-category]] $C^{op}$.
=--


+-- {: .un_theorem}
###### Theorem
If $C$ is an [[(infinity,1)-category]] with finite coproducts, then the cocartesian model structure on $C$ is universal among [[symmetric monoidal (infinity,1)-categories]] $D$ for which there exists a functor $C \to CAlg(D)$, to the [[symmetric monoidal (infinity,1)-category]] of [[commutative monoid in an (infinity,1)-category|commutative algebra objects]] in $D$.
=--

See ([Lurie, Theorme 2.4.3.18](#Lurie)).

## Examples

* If $C$ is a [[symmetric monoidal (infinity,1)-category]], then the canonical symmetric monoidal structure on $CAlg(C)$, the [[(infinity,1)-category]] of [[commutative monoid in a symmetric monoidal (infinity,1)-category|commutative algebra objects]] in $C$, is cocartesian, by ([Lurie, Proposition 3.2.4.7](#Lurie)).

## References

Section 2.4 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}


[[!redirects cocartesian monoidal (∞,1)-category]]
[[!redirects cocartesian monoidal (∞,1)-categories]]
[[!redirects cocartesian monoidal (infinity,1)-categories]]

[[!redirects coCartesian monoidal (∞,1)-category]]
[[!redirects coCartesian monoidal (∞,1)-categories]]
[[!redirects coCartesian monoidal (infinity,1)-categories]]
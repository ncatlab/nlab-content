
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition

A **split epimorphism** in a [[category]] $C$ is a [[morphism]] $e:A\to B$ which has a [[section]], meaning a morphism $s:B\to A$ such that $e \circ s = 1_B$.

In such a situation one also says that $B$ is a [[retract]] of $A$, and that $B$ is a splitting of the [[idempotent]] $s \circ e:A \to A$.

The dual notion is [[split monomorphism]].

## Properties

* Any split epimorphism is automatically a [[regular epimorphism]] (it is the [[coequalizer]] of $s\circ e$ and $1_A$), and therefore also a [[strong epimorphism]], an [[extremal epimorphism]], and (of course) an [[epimorphism]].

* The [[axiom of choice]] internal to a category $C$ can be phrased as "all epimorphisms are split."  In [[Set]] this is equivalent to the usual axiom of choice; in many other categories it is just false.

## Applications

The notion of split epimorphism arises often as a condition on fibrations in [[categories of chain complexes]]. See there for details

## Examples

* In [[Vect]], every epimorphism is split. For $\phi : V \to W$ a surjective linear map, we can find an isomorphism $V \simeq ker(\phi) \oplus V'$. Then $\phi|_{V'}$ is an isomorphism, and its inverse $W \to V' \hookrightarrow ker(\phi) \oplus V'$ is a section of $\phi$.

[[!redirects split epimorphism]]
[[!redirects split epimorphisms]]
[[!redirects split epi]]
[[!redirects split epis]]
[[!redirects split epic]]

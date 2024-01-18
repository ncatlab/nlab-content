
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Definition 

A [[binary endorelation]] $R$ on a set $A$ is **dense** if for all $x \in A$ and $y \in A$ such that $R(x, y)$ there exists an element $z \in A$ such that $R(x, z)$ and $R(z, y)$. Equivalently, a binary relation $R$ on $A$ is dense if $R$ is a [[subset]] of the composite $R \circ R$ in [[Rel]], $R \subseteq R \circ R$. 

In the [[graph theory|graph theoretic]] representation of relations as (directed loop) [[graphs]], a graph is **dense** if for every [[pair]] of [[vertices]] $a:V$ and $b:V$ with an [[edge]] $a \to b$, there exists a vertex $c:V$ with edges $a \to c$ and $c \to b$. 

## Examples

* Every [[reflexive relation]] is a dense relation

* Every (left or right) [[Euclidean relation]] is a dense relation

* An [[idempotent relation]] is a dense transitive relation

## Generalizations

The notion of dense relation in [[Rel]] can in theory be generalized to the notion of a *dense* [[morphism]] of an arbitrary [[2-poset]]: Given a 2-poset $C$ and an object $A \in \mathrm{Ob}(C)$, a morphism $R \in \mathrm{Hom}(A, A)$ is dense if $R \leq R \circ R$. 

## Dense relation structures

In [[dependent type theory]], the usual definition of a dense relation above use the phrase "there exists...". This existence in the definitions is mere existence; i.e. using the [[existential quantifier]] rather than the [[dependent sum type]]. 

The untruncated version of the dense relation using dependent sum types can be called **dense relation structure**, and fields states that 

* for all $x:A$ and $y:A$ such that $R(x, y)$, there exists as structure an element $z:A$ such that $R(x, z)$ and $R(z, y)$. 

$$\prod_{x:A} \prod_{y:A} R(x, y) \to \sum_{z:A} R(x, z) \times R(z, y)$$

## Related concepts

* [[DLO]]

* [[dense]]

* [[transitive relation]]

## References

See also:

* Wikipedia, *[Dense order -- Generalizations](https://en.wikipedia.org/wiki/Dense_order#Generalizations)*

[[!redirects dense relation]]
[[!redirects dense relations]]
[[!redirects dense binary relation]]
[[!redirects dense binary relations]]
[[!redirects dense binary endorelation]]
[[!redirects dense binary endorelations]]

[[!redirects dense directed loop graph]]
[[!redirects dense directed loop graphs]]
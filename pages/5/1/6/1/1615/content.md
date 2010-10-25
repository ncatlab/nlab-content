
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Local nets are a structure used in [[AQFT]] in order to axiomatize local algebras of observables in [[quantum field theory]].

## Definition

Let $X$ be a [[topological space]]. A co-[[presheaf]] on the [[category of open subsets]] of $X$

$$
  A : Op(X) \to T
$$

is a **net** if it is "co-flabby", i.e. if it sends every inclusion to a [[monomorphism]].

If 

* the net takes values in [[algebra]]s;

* there is given the structure of a Minkowski manifold on $X$

the net $A$ is called _local_ precisely if for all open subset $O_1, O_2 \subset O$ the images of the algebras $A(O_1)$ and $A(O_2)$ in $A(O)$ commute whenever $O_1$ and $O_2$ are completely spacelike seperated

$$
  (A local)
  \Leftrightarrow
  \left(
  (O_1 spacelike to O_2) \Rightarrow [A(O_1),A(O_2)] = 0 
  \right)
$$

This axiom encodes the the physical property known as Einstein-causality or micro-causality, which states that physical effects do not propagate faster that the speed of like.

It is to be noted that many auxiliary operators in usual [[quantum field theory]] do _not_ satisfy this axioms, for instance operators associate to currents in gauge theory. The idea is that those operators that actually do qualify as _observables_ do satisfy the axiom, however, i.e. in particular those that are gauge invariant.

## Related concepts

### Factorization algebras

There is a version of the notion of local nets for Euclidean spaces. This is closely related to the notion of [[factorization algebra]].

### Conformal nets

The notion of local net in the context of [[conformal field theory]] is a [[conformal net]].

## References

for the moment see the references at [[AQFT]].

[[!redirects local nets]]

[[!redirects Haag-Kastler net]]
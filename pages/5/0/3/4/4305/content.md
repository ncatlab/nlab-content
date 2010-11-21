
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition


In a [[monoidal category]] $(C,\otimes)$ with [[tensor product]] $\otimes$ we say that for $n \in \mathbb{N}$ a [[natural number]] and $V \in C$ any [[object]], that

$$
  V^{\otimes n} := V \otimes V \otimes \cdots \otimes V \;\; (n factors)
$$

is the $n$the **tensor power** of $V$.

There is accordingly also the $n$th tensor power of any [[morphism]] $f : V \to W$, being a morphism $f^{\otimes n} : V^{\otimes n} \to W^{\otimes n}$.  

This process defines a functor 
$$       
  (-)^{\otimes n} : C \to C 
$$

which could be called the $n$th **tensor power functor**.

## Properties

### Schur functors

If $C$ is a suitable [[linear category]], the $n$th tensor power functor is a simple example of a [[Schur functor]].

### Tensor algebra

The [[coproduct]] of all of the tensor powers of $V$ naturally inherits the structure of a [[monoid]] in $C$. This is called the __tensor algebra__ of $V$. This is the [[free monoid]] object on $V$. For more on this see [[category of monoids]].

## Examples

Often in the literature this is considered for the case $C = $ [[Vect]] of [[vector space]]s.
Given a [[vector space]] $V$, the $n$-fold [[tensor product]] of this space with itself, $V \otimes \cdots \otimes V$, is usually denoted $V^{\otimes n}$ and called the $n$th **tensor power** of $V$.  



[[!redirects tensor power]]
[[!redirects tensor powers]]
[[!redirects tensor algebra]]
[[!redirects tensor algebras]]

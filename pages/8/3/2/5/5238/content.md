

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}


## Idea

For $C$ a [[monoidal model category]] there is under mild conditions a natural [[model category]] structure on its [[category of monoids]].

## Definition

For $C$ a [[monoidal category]] with all [[colimit]]s the [[category of monoids]] comes equipped (as discussed there) with a [[free functor]]/[[forgetful functor]] [[adjunction]]

$$
  (F \dashv U) : Mon(C) \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
   C
  \,.
$$

Typically one uses on $Mon(C)$ the [[transferred model structure]] along this adjunction, if it exists.

## Properties

Suppose the transferred model structure exists on $Mon(C)$. By the discussion of <a href="http://ncatlab.org/nlab/show/category+of+monoids#FreeMonoids">free monoids</a> at [[category of monoids]] we have that then [[pushout]]s of the form

$$
  \array{
     F(A) &\stackrel{F(f)}{\to}& F(B)
     \\
     \downarrow && \downarrow
     \\
     X &\to& P
  }
$$

exist in $Mon(C)$, for all $f : A \to B$ in $C$


+-- {: .un_prop}
###### Proposition

If $f : A\to B$ is an acyclic cofibration in the model structure on $C$, then the pushout $X \to P$ as above is a weak equivalence in $Mon(C)$.

=--

This is [SchwedeShipley, lemma 6.2](#SchwedeShipley).


## Related concepts

* **model structure on monoids in a monoidal model category**

* [[model structure on algebras over an operad]]

* [[model structure on algebras over a monad]]

* [[model structure on simplicial T-algebras]]

## References

* [[Stefan Schwede]], [[Brooke Shipley]], _Algebras and modules in monoidal model categories_ Proc. London Math. Soc. (2000) 80(2): 491-511  ([pdf](http://www.math.uic.edu/~bshipley/monoidal.pdf)) 
{#SchwedeShipley}

[[!redirects model structure on monoids]]



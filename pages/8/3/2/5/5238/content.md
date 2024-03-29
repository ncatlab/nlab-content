

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

For $C$ a [[monoidal category]] with all [[colimits]], its [[category of monoids]] comes equipped (as discussed there) with a [[free functor]]/[[forgetful functor]] [[adjunction]]

$$
  (F \dashv U) : Mon(C) \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
   C
  \,.
$$

Typically one uses on $Mon(C)$ the [[transferred model structure]] along this adjunction, if it exists.

+-- {: .num_theorem}
###### Theorem

If $C$ is [[monoidal model category]] that

* satisfies the [[monoid axiom in a monoidal model category]];

* is a [[cofibrantly generated model category]];

* all objects are [[small objects]],

then the [[transferred model structure]] along the [[free functor]]/[[forgetful functor]] [[adjunction]] $(F \dashv U) : Mon(C) \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} C$ exists on its [[category of monoids]].
=--

This is part of ([SchwedeShipley, theorem 4.1](#SchwedeShipley)).


+-- {: .num_theorem}
###### Theorem

If the symmetric monoidal model category $C$ 

* is a [[cofibrantly generated model category]]

* its unit is cofibrant

* it has a suitable [[interval object]] 

then the transferred model structure on monoids exists.

=--

+-- {: .proof}
###### Proof

Regard monoids a [[algebras over an operad]] for the [[associative operad]]. Then apply the existence results discussed at _[[model structure on algebras over an operad]]_. See there for more details.

=--


## Properties


### Homotopy pushouts

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


+-- {: .num_prop}
###### Proposition

Let the monoidal model category $C$ be 

* [[symmetric monoidal category|symmetric monoidal]];

* and satisfy the [[monoid axiom in a monoidal model category]]. 

If $f : A\to B$ is an acyclic cofibration in the model structure on $C$, then the pushout $X \to P$ as above is a weak equivalence in $Mon(C)$.

=--

This is [SchwedeShipley, lemma 6.2](#SchwedeShipley).

+-- {: .proof}
###### Proof

Use the description of the pushout as a [[transfinite composition|transfinite composite]] of pushouts as described at [[category of monoids]] in the section <a href="http://ncatlab.org/nlab/show/category+of+monoids#FreeMonoids">free and relative free monoids</a>.

One sees that the [[pushout product axiom]] implies that all the intermediate pushouts produce acyclic cofibrations and the [[monoid axiom in a monoidal model category]] implies then that each $P_{n-1} \to P_n$ is a weak equivalence. Moreover, all these moprhisms are of the kind used in the monoid axioms, so also their [[transfinite composition]] is a weak equivalence.

=--

### $A_\infty$-Algebras

Under mild conditions on $C$ the model structure on monoids in $C$ is [[Quillen equivalence|Quillen equivalent]] to that of [[A-infinity algebras]] in $C$. See [[model structure on algebras over an operad]] for details.

## Related concepts

* **model structure on monoids in a monoidal model category**

  * [[model structure for ring spectra]]

* [[model structure on modules in a monoidal model category]]

* [[model structure on commutative monoids in a symmetric monoidal model category]]

* [[model structure on algebras over an operad]]

* [[model structure on algebras over a monad]]

* [[model structure on simplicial T-algebras]]

## References

* {#SchwedeShipley} [[Stefan Schwede]], [[Brooke Shipley]], _Algebras and modules in monoidal model categories_ Proc. London Math. Soc. (2000) 80(2): 491-511  ([pdf](http://www.math.uic.edu/~bshipley/monoidal.pdf)) 


* {#White14} [[David White]], _Model Structures on Commutative Monoids in General Model Categories_ ([arXiv:1403.6759](http://arxiv.org/abs/1403.6759))

[[!redirects model structure on monoids]]

[[!redirects model structures on monoids]]


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
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}


## Idea

The notion of _commutative monoid_ (or _commutative monoid object_, _commutative algebra_, _commutative algebra object_) in a [[symmetric monoidal (infinity,1)-category]] is the [[(infinity,1)-category theory|(infinity,1)-categorical]] generalization of the notion of [[commutative monoid in a symmetric monoidal category]].
It is the commutative version of [[monoid in a monoidal (infinity,1)-category]].

Note that _commutative_ here really means $E_\infty$, in the sense of [[E-infinity operad]].

## Definition

A **commutative monoid** in a [[symmetric monoidal (infinity,1)-category]] $C$ is a lax symmetric monoidal $(\infty,1)$-functor

$$
  * \to C
  \,.
$$

In more detail, this means the following:


+-- {: .un_defn}
###### Definition

Given a [[symmetric monoidal (infinity,1)-category]] in its [[quasi-category|quasi-categorical]] incarnation as a coCartesian fibration of [[simplicial set]]s

$$
  p : C^\otimes \to N(FinSet_*)
$$

a **commutative monoid** in $C$ is a [[section]]

$$
  A : N(FinSet_*) \to C^\otimes
$$

such that $A$ carries collapsing morphisms in $FinSet_*$ to coCartesian morphisms in $C^\otimes$.
=--

## $(\infty,1)$-Category of commutative monoids

### Definition

For $C$ a [[symmetric monoidal (∞,1)-category]] write $CMon(C)$ for the $(\infty,1)$-category of commutative monoids in $C$.

### Properties

+-- {: .num_theorem #LimitsInCRing}
###### Theorem

* $CMon(C)$ has all [[(∞,1)-coproduct]]s and these are computed as [[tensor product]]s in $C$.

* For $K$ a _[[sifted (infinity,1)-category]]_ , [[(∞,1)-colimits]] of shape $K$ exist in $CMon(C)$ and are computed in $C$ if $K$-colimits exist in $C$ are preserved by tensor product with any object.

* $CMon(C)$ has all [[(∞,1)-limit]]s and these are computed in $C$.

=--

This is ([Lurie DAG III, section 4](#LurieDAG3)) or ([Lurie HA, sections 3.2.2 and 3.2.3](#LurieHA)).

+-- {: .num_theorem }
###### Corollary

$(\infty,1)$-Colimits over simplicial diagrams exists in $CMon(C)$ and are computed in $C$ if they exist in $C$ and a preserved by tensor products.

=--

Because the [[simplex category]] is a [[sifted (infinity,1)-category]] (as discussed there).

## Examples

* A commutative monoid in [[∞Grpd]] is a [[E-∞ space]].

* A commutative monoid in the [[stable (infinity,1)-category of spectra]] is a [[commutative ring spectrum]] or [[E-infinity ring]].

## Related concepts

* [[monoid in a monoidal (infinity,1)-category]]
* [[infinity-algebra over an (infinity,1)-operad]]

* [[commutative monoid in a symmetric monoidal category]]
* [[module over a monoid]]

* [[∞-group completion]]

## References

* {#LurieDAG3} [[Jacob Lurie]], _[[Commutative Algebra]]_.

* {#LurieHA} [[Jacob Lurie]], _[[Higher Algebra]]_.

An equivalent reformulation of commutative monoids in terms [[(∞,1)-algebraic theories]] is in

* [[James Cranch]], _Algebraic Theories and $(\infty,1)$-Categories_ ([arXiv](http://arxiv.org/abs/1011.3243))

[[!redirects commutative monoid in a symmetric monoidal (∞,1)-category]]

[[!redirects commutative monoid in an (∞,1)-category]]
[[!redirects commutative monoid in an (infinity,1)-category]]
[[!redirects commutative monoid in a monoidal (∞,1)-category]]
[[!redirects commutative monoid in a monoidal (infinity,1)-category]]
[[!redirects commutative monoid in a symmetric monoidal (∞,1)-category]]
[[!redirects commutative monoid in a symmetric monoidal (infinity,1)-category]]

[[!redirects commutative monoids in an (∞,1)-category]]
[[!redirects commutative monoids in an (infinity,1)-category]]
[[!redirects commutative monoids in a monoidal (∞,1)-category]]
[[!redirects commutative monoids in a monoidal (infinity,1)-category]]
[[!redirects commutative monoids in a symmetric monoidal (∞,1)-category]]
[[!redirects commutative monoids in a symmetric monoidal (infinity,1)-category]]

[[!redirects commutative algebra in an (∞,1)-category]]
[[!redirects commutative algebra in an (infinity,1)-category]]
[[!redirects commutative algebra in a monoidal (∞,1)-category]]
[[!redirects commutative algebra in a symmetric monoidal (∞,1)-category]]
[[!redirects commutative algebras in an (∞,1)-category]]
[[!redirects commutative algebras in an (infinity,1)-category]]
[[!redirects commutative algebras in a monoidal (∞,1)-category]]
[[!redirects commutative algebras in a symmetric monoidal (∞,1)-category]]

[[!redirects commutative ∞-monoid]]
[[!redirects commutative ∞-monoids]]
[[!redirects commutative infinity-monoid]]
[[!redirects commutative infinity-monoids]]

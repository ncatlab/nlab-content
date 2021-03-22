
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+--{: .hide}
[[!include categorical algebra -- contents]]
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

## Definition

A [[Lawvere theory]] is encoded in its [[syntactic category]] $T$, a category with finite products such that all objects are finite products of a given object.

An **algebra over a Lawvere theory $T$**, or **$T$-algebra** for short, is a [[model]] for this [[algebraic theory]]: it is a product-preserving [[functor]]

$$
  A : T \to Set
  \,.
$$ 

The [[category]] of $T$-algebras is the [[full subcategory]] of the [[functor category]] on the product-preserving functors

$$
  T Alg := [T,Set]_\times \subset [T,Set]
  \,.
$$

For more discussion, properties and examples see for the moment [[Lawvere theory]].

## Properties

+-- {: .un_prop}
###### Proposition

The category $T Alg$ has all [[limit]]s and these are computed objectwise, hence the embedding $T Alg \to [T,Set]$ preserves these limits.

=--



+-- {: .un_prop}
###### Proposition

$T Alg$ is a [[reflective subcategory]] of $[T, Set]$:

$$
  T Alg \stackrel{\leftarrow}{\hookrightarrow} [T,Set]
  \,.
$$

=--

+-- {: .proof}
###### Proof

With the above this follows using the [[adjoint functor theorem]].

=--

+-- {: .un_corollary}
###### Corollary

The category $T Alg$ has all [[colimit]]s.

=--


for more see [[Lawvere theory]] for the moment

## Examples

* [[group]]s

* [[ring]]s

* $k$-[[associative algebra]]s

* [[smooth algebra]]s


## Related concepts

* [[algebra over a monad]]

  [[∞-algebra over an (∞,1)-monad]] 

* **algebra over an algebraic theory** 

  [[∞-algebra over an (∞,1)-algebraic theory]]

  * [[homotopy T-algebra]] / [[model structure on simplicial T-algebras]]

* [[algebra over an operad]] 

   [[∞-algebra over an (∞,1)-operad]]

   * [[model structure on algebras over an operad]]




[[!redirects algebras over a Lawvere theory]]

[[!redirects algebra over an algebraic theory]]
[[!redirects algebras over an algebraic theory]]

[[!redirects algebra for an algebraic theory]]
[[!redirects algebras for an algebraic theory]]


[[!redirects T-algebra]]
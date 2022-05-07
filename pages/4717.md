
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition


Given an [[adjunction]]

$$
  (L \dashv R)
  \colon\;
  X
    \underoverset{R}{L}{\rightleftarrows}
  Y
$$

there is a [[natural transformation]] (or more generally, a $2$-[[2-morphism|morphism]]) $\eta\colon id_X \to R \circ L$, called the __unit__ of the adjunction (in older texts, called a "front adjunction").  (A reason for the name is that $R \circ L$ is a [[monad]], which is a kind of [[monoid object]], and $\eta$ is the [[identity element|identity]] of this monoid.  Since 'identity' in this context would suggest an [[identity natural transformation]], we use the synonym 'unit'.)

Similarly, there is $2$-morphism $\epsilon\colon L \circ R \to id_Y$, called the __counit__ of the adjunction (in older texts, called a "back adjunction").  (This is the co-identity of the [[comonad]] $L \circ R$.)

## Properties

### General

Unit and counit of an adjunction satisfy the [[triangle identities]].

An [[adjunct]] is given by precomposition with a unit or postcomposition with a counit.

The left adjoint $L : X \to Y$ is [[fully faithful]] if and only if the unit $\eta : id_X \to R \circ L$ is a natural isomorphism.

If the unit is a natural isomorphism, $L$ is sometimes termed __lari__ ("left adjoint right inverse"); whilst $R$ is termed __rali__ ("right adjoint left inverse"). Dually, if the counit is a natural isomorphism, $L$ is sometimes termed __lali__ ("left adjoint left inverse"); whilst $R$ is termed __rari__ ("right adjoint right inverse"). All four classes of functor are closed under composition, and contain the equivalences.

### Relation to monads

Every [[adjunction]] $(L \dashv R)$ gives rise to a [[monad]] $T \coloneqq R \circ L$. The [[unit of a monad|unit of this monad]] $id \to T$ is the unit of the adjunction, $id \to R \circ L$.

## Related concepts

* [[adjunction]]

* [[zig-zag law]]/[[triangle identity]]

* [[unit]]

  * [[unit object]]

  * **unit of an adjunction**

    [[derived adjunction unit]]

  * [[unit of a monad]]

* [[adjunct]]



[[!redirects unit of an adjunction]]
[[!redirects unit of the adjunction]]
[[!redirects units of adjunctions]]

[[!redirects counit of an adjunction]]
[[!redirects counit of the adjunction]]
[[!redirects counits of adjunctions]]
[[!redirects counit]]
[[!redirects counits]]

[[!redirects adjunction unit]]
[[!redirects adjunction units]]

[[!redirects adjunction counit]]
[[!redirects adjunction counits]]

[[!redirects front adjunction]]
[[!redirects back adjunction]]

[[!redirects lali]]
[[!redirects rali]]
[[!redirects lari]]
[[!redirects rari]]
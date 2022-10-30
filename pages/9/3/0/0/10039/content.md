

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

Given a [[morphism]] $f \colon X \to Y$ between two [[dualizable objects]] in a [[symmetric monoidal category]], the corresponding **dual morphism**

$$
  f^\ast \colon Y^\ast \to X^\ast
$$

is the one obtained by $f$ by composing the the duality [[unit of an adjunction|unit]] of $X$, the duality [[counit of an adjunction|counit]] of $Y$ and the [[braiding]] of $X$ with $Y$...

=--

## Examples

+-- {: .num_example}
###### Example

If $A$, $B$ are [[C*-algebras]] which are [[Poincaré duality algebras]], hence [[dualizable objects]] in the [[KK-theory]]-category, then for $f \colon A \to B$ a morphism it is [[K-orientation|K-oriented]], the corresponding [[Umkehr map]] is (postcomposition) with the dual morphism of its [[opposite algebra]] version:

$$
  f! \coloneqq (f^op)^\ast
  \,.
$$

=--

See at _[KK-theory -- Push-forward in KK-theory](KK-theory#UmkehrMap)_.

## Related concepts

* [[trace]]

[[!redirects dual morphisms]]

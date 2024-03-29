
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

## Idea

A _bipermutative category_ is a semistrict [[rig category]].  More concretely, it is a [[permutative category]] $(C, \oplus)$ with a second [[symmetric monoidal category]] structure $(C, \otimes)$ that [[distributive law|distributes]] over $\oplus$, with, again, some of the [[coherence laws]] required to hold strictly.

## Definition

Two nonequivalent definitions are given in
([May, def. VI 3.3](#May)) and ([Elmendorf-Mandell, def. 3.6](#ElmendorfMandell)).

May requires the left distributivity map to be an isomorphism
and the right distributivity map to be an identity.

Elmendorf and Mandell allow both distributivity maps to be noninvertible.

A discussion of these two definitions is in ([May2, Section 12](#May2)).

## Properties

### Relation to rig categories

Every [[symmetric monoidal category|symmetric]] [[rig category]] is equivalent to a bipermutative category ([May, prop. VI 3.5]).

## Examples

* [[Ab]], $R$[[Mod]], [[Vect]] are [[symmetric monoidal category|symmetric]] [[rig categories]] under [[direct sum]] and [[tensor product of abelian groups]]/[[tensor product of modules]].  Thus, they have "strictifications" that are bipermutative.

+-- {: .num_example}
###### Example

For $R$ a plain [[ring]], regarded as a discrete [[rig category]], it is a bipermutative category. The corresponding [[K-theory of a bipermutative category]] is [[ordinary cohomology]] with [[coefficients]] in $R$, given by the [[Eilenberg-MacLane spectrum]] $H R$.

=--

+-- {: .num_example}
###### Example

Consider the category whose [[objects]] are the [[natural numbers]] and whose [[hom sets]] are

$$
  Hom(n_1, n_2) = \left\{ \array{ \Sigma_{n_1} & | n_1 = n_2 \\ \emptyset & | n_1 \neq n_2 } \right.
  \,,
$$

with $\Sigma_n$ being the [[symmetric group]] of [[permutations]] of $n$ elements. The two monoidal structures ar given by addition and multiplication of natural numbers. This is a bipermutative version of the $Core(FinSet)$, the [[core]] of the category [[FinSet]] of [[finite sets]].

The corresponding [[K-theory of a bipermutative category]] is given by the [[sphere spectrum]].

=--

## Related concepts

* [[K-theory of a bipermutative category]]

* [[BDR 2-vector bundle]]

* [[distributivity for monoidal structures]]

  * [[rig category]]

  * [[distributive monoidal category]]

  * [[distributive category]]

## References

* [[Peter May]], _$E_\infty$ Ring Spaces and $E_\infty$ Ring spectra_, Springer lectures notes in mathematics, Vol. 533, (1977) ([pdf](http://www.math.uchicago.edu/~may/BOOKS/e_infty.pdf)) chaper VI
 {#May}

* [[Peter May]], _The construction of $E_\infty$ ring spaces
from bipermutative categories_, Geometry and Topology Monographs, Vol. 16, (2009) ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Final2.pdf)) chaper VI
 {#May2}

* [[Anthony Elmendorf]], [[Michael Mandell]], _Rings, modules and algebras in infinite loop space theory_, K-Theory 0680 ([web](http://www.math.uiuc.edu/K-theory/0680/), [pdf](http://www.math.uiuc.edu/K-theory/0680/RMAsubmit.pdf))
 {#ElmendorfMandell}


[[!redirects bipermutative categories]]

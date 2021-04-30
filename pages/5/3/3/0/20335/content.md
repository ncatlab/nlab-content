
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

A general [[monoidal category]] $(C,\otimes)$ does not admit [[diagonal]] [[natural transformations]] of the form $x \longrightarrow x\otimes x$, unlike the case of a [[cartesian monoidal category]] (where the monoidal product is the [[Cartesian product]]). A **monoidal category with diagonals** is a monoidal category with the extra [[structure]] of a consistent system of such [[diagonal morphisms]].

## Definition

A consistent system of diagonal maps $\Delta_x\colon x \to x \otimes x$ as $x$ varies through the [[objects]] of a [[monoidal category]] $(C,\otimes,I)$ should be [[natural transformation|natural]], so that $(f \otimes f)\circ \Delta_x = \Delta_y \circ f$, for any $f\colon x\to y$. Hence such a system is a [[natural transformation]] from the [[identity functor]] on $C$ to the [[composition|composite]] $C \to C \times C \stackrel{\otimes}{\to} C$ of the [[diagonal functor]] with the given [[monoidal category|monoidal product functor]].

Another desirable property is that the diagonal map $\Delta_I\colon I \to I\otimes I$ on the [[tensor unit]] $I$ is the [[inverse morphism|inverse]] of the left [[unitor]] $\ell_I\colon I \otimes I \stackrel{\sim}{\to} I$ (which is the same as the right unitor $r_I$).

## Examples

### General

* Any [[cartesian monoidal category]] has a canonical structure of diagonal maps given by the actual [[diagonal morphisms]].

* Given a [[cartesian monoidal category]], the [[wide subcategory]] consisting of the [[monomorphisms]] is a monoidal category with the same product and unit. The [[diagonal morphism]] of the original category, always a [[monomorphism]], plays the role of the diagonal maps in the subcategory. Now there are no projections, since, for instance, in [[Set]], the projection maps are almost never injective.


[[!include smash-monoidal diagonals -- section]]





## Related concepts

* [[relevance monoidal category]]

* [[semicartesian monoidal category]]

* [[monoidal category]]


## References

The stronger notion of relevance monoidal category is discussed in

* K. Dosen and Z. Petric, _Relevant Categories and Partial Functions_, Publications de l'Institut Mathématique, Nouvelle Série, Vol. 82(96), pp. 17–23 (2007) ([arXiv:0504133](http://arxiv.org/abs/math/0504133)

When a [[premonoidal category]] comes equipped with a morphism $\Delta_x\colon x\to x\otimes x$ for all $x$, such as in the [[Kleisli category]] for a [[strong monad]] on a cartesian category, or in any [[Freyd category]], then the $f$ for which $(f\otimes f)\circ \Delta_x = \Delta_y \circ f$ are called "copyable".

* C. Führmann. *Varieties of effects*, Proc. Fossacs 2002. Doi:[10.1007/3-540-45931-6_11](https://doi.org/10.1007/3-540-45931-6_11)



[[!redirects monoidal categories with diagonals]]

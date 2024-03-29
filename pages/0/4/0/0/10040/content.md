

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The operation $V \mapsto V^*$ of forming [[dual vector spaces]] extends to a [[contravariant functor]].

+-- {: .num_defn}
###### Definition (transpose map)
The **dual linear map** or __transpose map__ of a [[linear map]] $A\colon V\to W$, is the linear map $A^* = A^T\colon W^*\to V^*$, given by
$$ \langle{A^*(w), v}\rangle = \langle{w, A(v)}\rangle $$
for all $w$ in $W^*$ and $v$ in $V$.
=--

+-- {: .num_remark}
###### Remark

This functor is, of course, the [[representable functor]] represented by $K$ as a vector space over itself (a [[line]]).

=--

+-- {: .num_remark}
###### Remark

This construction is the notion of [[dual morphism]] applied in the [[monoidal category]] [[Vect]] with its [[tensor product]] monoidal structure.

=--

## Related concepts

* [[Chevalley-Eilenberg algebra]]

* [[duality]]

[[!redirects dual linear maps]]

[[!redirects transpose linear map]]
[[!redirects transpose linear maps]]

[[!redirects linear dual map]]
[[!redirects linear dual maps]]

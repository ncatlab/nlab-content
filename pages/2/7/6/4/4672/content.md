
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The [[category]] **LieAlg** is that whose [[object]]s are [[Lie algebra]]s $(\mathfrak{g}, [-,-]_{\mathfrak{g}})$ and whose morphisms are Lie algebra [[homomorphisms]], that is linear maps $\phi : \mathfrak{g} \to \mathfrak{h}$ such that for all $x,y \in \mathfrak{g}$ we have

$$
  \phi( [x,y]_{\mathfrak{g}}) = [\phi(x),\phi(y)]_\mathfrak{h}
  \,.
$$

If Lie algebras are expressed in terms of their [[Chevalley-Eilenberg algebra]]s (and if restricted to finite-dimensional Lie algebras), this may equivalently be characterized as follows: 

$LieAlg$ is the [[full subcategory]] of the [[opposite category]] of the category [[dgAlg]] of [[dg-algebras]] on those dg-algebras whose underlying graded algebra is a [[Grassmann algebra]], i.e. of the form $\wedge^\bullet \mathfrak{g}$.

## Special objects

* [[simple Lie algebra]]

* [[semisimple Lie algebra]]

category: categories
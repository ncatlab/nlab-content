
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A [[simplicial set]] $X$ is (sometimes) called _reduced_ if it has a single vertex, $X_0 \simeq *$.

More generally, for $n \in \mathbb{N}$ a simplicial set is _$n$-reduced_ if its $n$-[[skeleton]] is the point, $sk_n X = \Delta[0]$. 

## Properties

### Reflection

Write $sSet_0 \hookrightarrow$ [[sSet]] for the [[full subcategory]] inclusion of the reduced simplicial sets into all of them.

This is a [[reflective subcategory]]. The reflector

$$
  red : sSet \to sSet_0
$$

identifies all vertices of a simplicial set.

Write $sSet^{*/}$ for the category of [[pointed object|pointed]] simplicial sets. There is also a full inclusion $sSet_0 \hookrightarrow sSet^{*/}$. This has a right adjoint $red : sSet^{*/} \to sSet_0$ which sends a pointed simplicial set to the subobject all whose $n$-cells have as 0-faces the given point.

### Coreflection

The inclusion $sSet_0 \hookrightarrow sSet^{*/}$ into [[pointed object|pointed]] simplicial sets is [[coreflective subcategory|coreflective]]. The coreflector is the [[Eilenberg subcomplex]] construction in degree 1.

### Model structure

There is a [[model structure on reduced simplicial sets]] (see there) which serves as a [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-category]] of [[pointed object|pointed]] [[connected]] [[∞-groupoids]].

## Related concepts

* [[Eilenberg subcomplex]]

* [[simplicial group]]

[[!redirects reduced simplicial sets]]
